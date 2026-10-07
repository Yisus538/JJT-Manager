JJT MANAGER · DOCUMENTO DE GESTIÓN DE PROYECTOS

# **Definición del Stack Tecnológico**

Sistema de Gestión y Facturación Ágil integrado con ARCA

| Campo | Detalle |
| :---- | :---- |
| Código | JJT-GPI-14 |
| Actividad | 2.1 Definición de stack tecnológico (Lista de Actividades v1.2) |
| Sponsor | Julio Gutierrez |
| Director de proyecto | Tomás Disandro |
| Fecha / Versión / Estado | 07/10/2026 · 1.0 · Aprobado por el equipo |

| Versión | Fecha | Cambios |
| :---- | :---- | :---- |
| 1.0 | 07/10/2026 | Emisión inicial. Documento emitido fuera del plazo previsto (semana 3). Aprobado por el equipo el 07/10/2026. |

> Define el stack del proyecto y la justificación de cada decisión. Es el entregable de la actividad 2.1 y condiciona 2.2, 2.3 y todo el paquete 4.0. Las decisiones de librerías para ARCA se confirman o corrigen en el spike 2.3; si el spike las invalida, se actualiza este documento por el proceso de control de cambios (Alcance §7).

## **1. Criterios de decisión**

Los criterios salen de los requerimientos y de las restricciones del Acta; no son preferencias de herramienta.

| Criterio | Origen | Peso |
| :---- | :---- | :----: |
| Un solo lenguaje en frontend y backend, para que cualquier integrante pueda tocar cualquier módulo y reducir el impacto de una ausencia | Equipo fijo de 3 (RNF-10; riesgo R5) | Alto |
| Soporte maduro para firma CMS (PKCS#7) y SOAP, que exigen WSAA y WSFEv1 | RF-06, RF-08; riesgo R1 | Alto |
| Despliegue simple en Railway, dentro de USD 5/mes | Acta, presupuesto | Alto |
| Interfaz web responsive, sin app nativa | RNF-06; Acta (excluido) | Medio |
| Esquema de datos flexible para categorías y variantes por configuración | RNF-01 a 03; RF-32 | Alto |
| Secretos fuera del repositorio | RNF-04, RNF-05 | Alto |

## **2. Decisión**

| Capa | Elección | Justificación |
| :---- | :---- | :---- |
| Lenguaje | TypeScript (Node.js, versión LTS vigente) en frontend y backend | Un solo lenguaje y tipado estático para compartir tipos de comprobante, montos e IVA entre cliente y servidor. |
| Backend | Node.js + Fastify | API REST ligera, buen soporte de validación de esquemas y poco consumo de memoria en un servidor de USD 5/mes. |
| Base de datos | PostgreSQL | Transacciones y restricciones de integridad para stock, cuentas corrientes y comprobantes; tipo `JSONB` con índices para los atributos de variante configurables (ver Modelo de Datos, JJT-GPI-15). Servicio administrado de Railway. |
| Acceso a datos | Prisma (ORM con migraciones versionadas) | Migraciones en el repositorio y tipos generados del esquema. Las consultas de reportes pueden usar SQL directo. |
| Frontend | React + TypeScript + Vite | Interfaz web responsive (RNF-06) como aplicación de una sola página; ecosistema amplio y tiempos de compilación bajos. |
| Estilos | Tailwind CSS | Diseño responsive con utilidades; sin librería de componentes propietaria. |
| Autenticación y roles | Sesión con JWT de corta duración + hash de contraseñas con Argon2; autorización por rol (administrador, cajero) en el servidor | Cubre RF-28 a RF-30. Las reglas de permisos viven en el backend, no en la interfaz. |
| Firma y SOAP (ARCA) | Firma CMS con `node-forge` (o `openssl`) y cliente SOAP con el paquete `soap`; **candidato alternativo: el SDK `@afipsdk/afip.js`** | Se evalúan ambas opciones en el spike 2.3 (riesgo R12): si el SDK cubre WSAA y WSFEv1 con ticket cacheado y manejo de errores, se adopta; si no, se usa la implementación propia. |
| PDF de comprobantes | `pdfkit` + `qrcode` | Generación de PDF liviana, sin navegador embebido, con el código QR del comprobante (RF-11). |
| Pasarela simulada | Servicio interno que emula aprobación/rechazo | Cumple RF-21 sin integrar pasarelas reales. |
| Pruebas | Vitest (unitarias y de integración), Playwright (extremo a extremo y responsive) | Cubre los niveles de prueba del Plan de Calidad §4. |
| Control de versiones y CI | Git (repositorio único del proyecto) y GitHub Actions | Ejecuta lint, pruebas y escaneo de secretos en cada integración (Plan de Calidad §2). |
| Hosting | Railway (aplicación y PostgreSQL) | Ya incluido en el presupuesto (USD 5/mes × 5 meses). |

## **3. Alternativas consideradas**

| Alternativa | Ventajas | Por qué no se elige |
| :---- | :---- | :---- |
| Python + Django con `pyafipws` | La librería de ARCA más difundida y probada | Dos lenguajes en el equipo (Python en backend y TypeScript en frontend) y mayor consumo de memoria; se mantiene como **contingencia del riesgo R1**: si el spike no logra CAE con el stack elegido, se evalúa aislar la integración ARCA en un servicio Python. |
| PHP + Laravel | Hosting económico, ecosistema maduro | Mismo problema de dos lenguajes y librerías de ARCA menos mantenidas. |
| Java / .NET | Soporte SOAP nativo y robusto | Mayor complejidad de despliegue y consumo de recursos para un servidor de USD 5/mes. |

## **4. Estructura del repositorio y entornos**

- **Repositorio único** con las carpetas `frontend/`, `backend/`, `qa/` y `docs/`, respetando el ownership definido en el `CLAUDE.md` raíz. Convención de commits: `[frontend|backend|qa|docs] descripción breve`.
- **Configuración y secretos** por variables de entorno (`.env` ignorado por git): ambiente de ARCA (`homologacion` por defecto, RNF-09), CUIT, ruta del certificado y la clave, URL de la base de datos y clave de firma de sesiones. Nada de esto se versiona (RNF-04) ni se escribe en logs (RNF-05).
- **Entornos:** local (contra homologación de ARCA), Railway para pruebas, y producción solo para la validación final opcional (Acta).
- **Calidad en CI:** lint, pruebas unitarias, escaneo de secretos y compilación en cada integración.

## **5. Riesgos y supuestos de la decisión**

| N.º | Supuesto o riesgo | Tratamiento |
| :----: | :---- | :---- |
| 1 | El paquete `soap` y la firma con `node-forge` cubren la conversación con WSAA y WSFEv1. | Se verifica en el spike 2.3; si falla, SDK `@afipsdk/afip.js` o servicio Python (R1, R12). |
| 2 | El servidor de USD 5/mes alcanza para aplicación y base de datos durante el desarrollo y las demostraciones. | Se monitorea el consumo en H2; un aumento de costo es un cambio de presupuesto (Alcance §7). |
| 3 | El equipo trabaja cómodamente en TypeScript. | Pares entre módulos desde H2 para reducir el impacto de una ausencia (R5). |
| 4 | Las versiones exactas de las dependencias se fijan en el primer commit del backend y del frontend. | Se registran en los archivos de bloqueo (`package-lock.json`). |

## **6. Aprobación**

*Aprobado por el equipo el 07/10/2026. Firma y fecha de cada persona, a registrar en la tabla.*

| Rol | Nombre | Firma / Conformidad | Fecha |
| :---- | :---- | :---- | :---- |
| Director de proyecto y Backend | Tomás Disandro | | |
| Frontend | Juan Cruz Bulatovich | | |
| QA y QC | Jesus Manuel Martinez | | |
