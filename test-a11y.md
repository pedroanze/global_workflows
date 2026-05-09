---
description: Auditoría de accesibilidad (a11y) para componentes de Astro y React, asegurando compatibilidad sin romper la UI.
---

Guardrails

Prioriza siempre el uso de HTML semántico nativo antes de sugerir atributos ARIA.

Asegura que cualquier corrección visual respete las variables y clases de Tailwind v4.

Mantén la coherencia con el diseño existente del proyecto.

Steps

Analizar el Componente:

Identifica si es React o Astro.

Revisa el uso actual de etiquetas y el manejo del foco.

Revisión Semántica:

Verifica el uso correcto de header, main, nav, button vs a, y niveles de encabezados (h1-h6).

Revisión de Interactividad:

Confirma que los elementos interactivos sean accesibles mediante teclado.

Asegura que los formularios tengan etiquetas (label) correctamente asociadas.

Documentar Soluciones:

Entrega el código corregido aplicando Tailwind v4 donde sea necesario (ej. sr-only para textos exclusivos de lectores de pantalla).

Principles

HTML nativo siempre es mejor que ARIA.

Mejora progresiva: Las funciones básicas deben ser accesibles para todos.
