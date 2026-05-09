---
description: Escaneo de la base de código en busca de vulnerabilidades, secretos expuestos y violaciones de seguridad orientadas al stack.
---

Guardrails

NUNCA expongas secretos reales encontrados en el output de respuesta (ocúltalos con asteriscos).

Prioriza los problemas de inyección, exposición de Firebase y validación de tokens JWT.

Sugiere código corregido alineado con el stack (Astro/React/TS), no solo indiques el problema.

Steps

Entender el Alcance:

Define si se audita el frontend (Astro/React), endpoints del backend o archivos de configuración.

Búsqueda de Secretos Expuestos:

Revisa patrones de claves (API keys de Firebase, tokens JWT quemados, contraseñas).

Confirma que toda variable sensible resida exclusivamente en .env.

Revisión de Autenticación/Autorización (RBAC):

Verifica que las rutas protegidas y endpoints validen el token JWT.

Confirma que las reglas de negocio críticas se validen en el backend y no asuman confianza en el cliente.

Validación de Entradas (Inputs):

Asegura que toda mutación hacia Firebase u otra base de datos esté estrictamente tipada con TS y sanitizada.

Busca posibles inyecciones XSS en el renderizado de React/Astro.

Generar Reporte y Soluciones:

Crea una tabla resumen: Gravedad, Problema, Archivo/Línea, Sugerencia.

Proveer el código corregido. Si es necesario un log de seguridad, usa: logger.error({id, user}, 'Intento de brecha de seguridad').

Principles

Confianza cero: asume que toda entrada de datos (del cliente o externa) es maliciosa.

Mantén los secretos fuera del código fuente de manera absoluta.

La seguridad no debe sacrificar la legibilidad del código
