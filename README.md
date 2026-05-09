---
description: crear workflow
---

# Global Workflows

Workflows globales para antigravity.
Cada archivo `.md` en este directorio define un workflow que el asistente puede ejecutar.

## Estructura de un workflow

```
---
description: <Descripcion corta de lo que hace el workflow>
---

Guardrails

<Reglas estrictas que el agente debe seguir obligatoriamente.
Cada regla en una linea aparte, sin viñetas.>

Steps

<Pasos secuenciales numerados. Cada paso describe una accion
concreta que el agente debe realizar. Pueden tener
sub-pasos indentados.>

Principles (opcional)

<Principios rectores de estilo o filosofia.
Cada principio en una linea aparte.>
```

## Convenciones

- **Idioma:** espanol
- **Emojis:** no usar
- **Extension:** `.md`
- **Naming:** `<categoria>-<nombre>.md` (ej. `test-unit.md`, `security-audit.md`)
- **Frontmatter:** YAML con campo `description` obligatorio
- **Tono:** tecnico, conciso, directo al grano

## Como crear un nuevo workflow

1. Crea un archivo `<categoria>-<nombre>.md` en este directorio
2. Escribe el frontmatter con `description`
3. Define `Guardrails`, `Steps` y opcionalmente `Principles`
4. El archivo es detectado automaticamente por antigravity

## Como cargarlo a antigravity

antigravity lee automaticamente todos los archivos `.md` de
`~/.gemini/antigravity/global_workflows/`. No requiere configuracion adicional.

Para respaldar y versionar los cambios:

```bash
git add <archivo>.md
git commit -m "feat: add <nombre> workflow"
git push origin main
```

## Ejemplo

Archivo `mi-workflow.md`:

```markdown
---
description: Descripcion breve del workflow.
---

Guardrails

Regla obligatoria 1.
Regla obligatoria 2.

Steps

Paso 1: Hacer algo concreto.
Paso 2: Hacer otra cosa.
Paso 3: Verificar el resultado.

Principles

Principio rector 1.
Principio rector 2.
```

## Workflows actuales

| Archivo                | Descripcion                       |
| ---------------------- | --------------------------------- |
| `docs-api.md`          | Genera documentacion TSDoc/JSDoc  |
| `docs-architecture.md` | Crea diagramas Mermaid            |
| `docs-readme.md`       | Genera README.md                  |
| `formatter-code.md`    | Configura formateador             |
| `git-pr.md`            | Describe Pull Requests            |
| `security-audit.md`    | Audita seguridad del codigo       |
| `security-deps.md`     | Gestiona dependencias vulnerables |
| `test-a11y.md`         | Audita accesibilidad              |
| `test-review.md`       | Revisa calidad del codigo         |
| `test-unit.md`         | Genera pruebas unitarias          |
