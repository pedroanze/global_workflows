---
description: Generación de pruebas unitarias efectivas, aisladas y legibles para lógica, componentes o servicios.
---

Guardrails

Detecta primero el framework (Vitest, Jest, etc.). Si no hay, pregunta antes de asumir.

Prueba el comportamiento de la función, no su implementación interna.

Las pruebas deben ser independientes y no depender de servicios externos reales (usar mocks).

Nombra los bloques y pruebas en español, de forma muy descriptiva.

Steps

Entender qué Probar:

Identifica entradas, salidas esperadas y casos extremos (nulos, vacíos).

Manejo de Dependencias:

Prepara mocks para llamadas a Firebase, APIs externas o fechas/tiempos dinámicos.

Escribir Pruebas (Patrón AAA):

Arrange (Preparar): Configura los datos de prueba y mocks.

Act (Actuar): Ejecuta la función o renderiza el componente.

Assert (Afirmar): Verifica el resultado esperado.

Verificar Manejo de Errores:

Escribe pruebas específicas para asegurar que los errores disparen el log correspondiente (logger.error).

Principles

Mantén las pruebas rápidas y deterministas (cero dependencias temporales no controladas).

Prioriza probar la lógica de negocio compleja y los servicios de backend sobre componentes puramente visuales.
