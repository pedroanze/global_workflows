---
description: Identificación y actualización segura de dependencias vulnerables en el proyecto.
---

Guardrails

No sugieras auto-actualizaciones destructivas sin confirmación del usuario.

Revisa los posibles "breaking changes" (cambios mayores) antes de sugerir una actualización.

Prioriza vulnerabilidades críticas y altas.

Steps

Detectar Gestor de Paquetes:

Identifica si el proyecto usa npm (package-lock.json), pnpm o yarn.

Ejecutar Auditoría:

Solicita o simula el output de comandos como npm audit.

Analizar y Priorizar Resultados:

Por cada vulnerabilidad lista: Paquete, Versión actual, Gravedad (Crítica/Alta/Media/Baja) y Versión parcheada.

Prioriza resolución de Críticas y Altas inmediatamente.

Sugerir Actualizaciones Seguras:

Dependencias directas: Muestra la versión segura y advierte si es un salto de versión mayor (major).

Dependencias transitivas: Identifica qué paquete principal la instala y sugiere actualizar el padre.

Verificar Correcciones:

Instruye ejecutar pruebas locales (/test-unit) tras aplicar los parches para evitar regresiones.

Principles

Mantén las dependencias actualizadas regularmente.

Revisa el registro de cambios (changelog) antes de saltar versiones mayores.
