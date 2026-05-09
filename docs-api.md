---
description: Genera documentación TSDoc/JSDoc para funciones, servicios de Firebase y hooks.
---

Guardrails

Documenta a partir de la implementación real.

Incluye las interfaces de TypeScript exactas que usa la función.

Documenta explícitamente los posibles errores y los logs asociados (logger.error).

Steps

Analizar la Función/Servicio:

Identifica los parámetros de entrada (Request), la salida (Response) y validaciones (ej. JWT, 2 decimales para moneda).

Extraer Tipos:

Anota las interfaces exactas involucradas para evitar ambigüedades (no any).

Generar Bloque TSDoc:

Propósito: Qué hace la función.

Params: Descripción de cada parámetro.

Returns: Qué devuelve exactamente.

Throws: Qué errores dispara y cómo se registran.

Añadir Ejemplo:

Incluye un ejemplo de uso realista y copiable.

Principles

Explica el por qué de la lógica de negocio, no solo traduzcas el código a texto.

Mantén la documentación junto al código (comentarios en línea) o en un archivo .md específico si es un módulo grande.
