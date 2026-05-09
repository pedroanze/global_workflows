---
description: Instala y configura Prettier o el formateador moderno adecuado según el lenguaje del proyecto.
---

Te ayudaré a configurar el formateador de código adecuado para tu proyecto, asegurando un estilo consistente y automatizado basado en estándares de desarrollo modernos.

Guardrails

Pregunta siempre el lenguaje o stack principal antes de generar configuraciones.

No sobrescribas archivos de configuración existentes (.prettierrc, eslint.config.js, etc.) sin consultar primero.

Mantén el estándar moderno de JS/TS: comillas simples, sin punto y coma innecesario (dependiendo del equipo), y trailing commas.

Redacta todo en español y sin usar emojis.

Para ecosistemas que no usan Prettier por defecto (Python, Dart), sugiere la herramienta estándar de la industria (Ruff/Black o dart format).

Steps

1. Detectar el Ecosistema

Analiza o pregunta cuál es el stack del proyecto:

JS / TS / React: Usar Prettier nativo.

Astro: Usar Prettier + prettier-plugin-astro.

Java: Usar Prettier + prettier-plugin-java.

Python: Sugerir ruff (recomendado moderno) o black. Si el usuario exige Prettier estricto, usar @prettier/plugin-python.

Dart / Flutter: Usar el comando nativo dart format. No usar Prettier.

2. Instalar Dependencias

Proporciona los comandos exactos según el gestor de paquetes (npm, pnpm, yarn, pip, etc.).

Ejemplo JS/TS/Astro: npm install --save-dev prettier prettier-plugin-astro

Ejemplo Java: npm install --save-dev prettier prettier-plugin-java

3. Generar Archivo de Configuración

Crea el archivo .prettierrc (o el correspondiente .prettierrc.mjs) con reglas modernas y limpias.

Base recomendada para JS/TS/Astro:

{
"printWidth": 100,
"semi": true,
"singleQuote": true,
"trailingComma": "all",
"tabWidth": 2,
"plugins": ["prettier-plugin-astro"],
"overrides": [
{
"files": "*.astro",
"options": {
"parser": "astro"
}
}
]
}

4. Configurar Scripts y Entorno

Añade automatización para que el formateo no sea manual.

Scripts (package.json):
Añade comandos para formatear todo el proyecto:
"format": "prettier --write ."
"format:check": "prettier --check ."

Configuración del IDE (.vscode/settings.json):
Sugiere la configuración para formatear al guardar:

{
"editor.formatOnSave": true,
"editor.defaultFormatter": "esbenp.prettier-vscode"
}

5. Integración con Linters (Opcional)

Si detectas ESLint en el proyecto, instruye la instalación de eslint-config-prettier para desactivar las reglas de formato de ESLint y evitar conflictos.

Principles

Consistencia sobre preferencia personal: el formateador decide, el desarrollador se enfoca en la lógica.

Cero conflictos: si hay un linter, el formateador debe tener la última palabra en el estilo visual.

Automatización: el código debe formatearse solo al guardar (format on save) o mediante hooks de Git (pre-commit).
