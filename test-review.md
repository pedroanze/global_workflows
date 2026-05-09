---
description: Auditoría exhaustiva del código enfocada en legibilidad, seguridad, mantenibilidad y cumplimiento estricto del stack.
---

Guardrails

Enfócate en la arquitectura (SOLID, DRY) y legibilidad (KISS), no en micro-optimizaciones.

Exige el uso de Tailwind v4 y TypeScript estricto (cero any).

No sugieras refactorizaciones masivas sin preguntar primero.

Mantén el reporte estrictamente en español y sin emojis.

Steps

Entender el Contexto:

Pregunta el propósito del cambio: ¿Es un feature, bugfix o refactor?

Revisión de Arquitectura y Lógica:

Verifica que el código sea explícito. Renombra variables si son ambiguas.

Confirma que no haya estilos en línea ni CSS puro.

Revisa el manejo de errores (debe usar formato estructurado como logger.error).

Revisión de Seguridad (Firebase/JWT):

Verifica validación de inputs.

Asegura que las operaciones de BD tengan middleware o validación de tokens.

Documentar Hallazgos:

Por cada problema, indica: Gravedad (Alta/Media/Baja), Archivo/Línea, Problema y Sugerencia de solución.

Gestión de Deuda Técnica:

Si se aprueba código con valores quemados (hardcoded), exige o inserta el comentario // TODO: [Explicación detallada].

Principles

Sé constructivo: Explica el por qué de la sugerencia basado en las reglas del proyecto.

Prioriza cambios de alto impacto que mejoren la claridad del código.
