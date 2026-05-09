---
description: Analiza los commits y genera una descripción completa y estructurada para un Pull Request.
---

Guardrails

Analiza los commits de la rama actual frente a la rama destino.

No modifiques código, solo genera el contenido del PR en formato Markdown.

Redacta todo estrictamente en español, sin emojis, priorizando la claridad técnica.

Sigue la plantilla de PR del proyecto si existe (.github/PULL_REQUEST_TEMPLATE.md).

Steps

Entender el Contexto:

Pregunta la rama destino (ej. main o develop), si hay un ticket/issue enlazado, y el tipo de cambio.

Analizar Cambios:

Simula o solicita la salida del diff de Git y el historial de commits para contextualizar las modificaciones.

Generar Contenido:

Título: <tipo>: <descripción breve>

Descripción: Resumen directo de lo que soluciona o aporta este PR.

Cambios: Viñetas con las modificaciones específicas (archivos clave, lógica actualizada).

Issue Relacionado: Referencia al ticket (ej. Cierra #123).

Tipo de Cambio: Especificar (Feature, Bug fix, Refactor, Documentación).

Pruebas: Indicar cómo se probaron los cambios localmente.

Refinar:

Muestra el Markdown generado y pregunta al usuario si desea iterar alguna sección antes de publicarlo.

Principles

Sé conciso pero completo. Ayuda a los revisores a entender el por qué de los cambios.

Destaca cualquier cambio que rompa compatibilidad (breaking changes) de forma prominente.
