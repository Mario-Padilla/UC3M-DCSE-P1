# Práctica 1 — Ingeniería de requisitos asistida por IA y desarrollo dirigido por especificación

**Universidad Carlos III de Madrid**

**Asignatura:** Digitization of Complex Systems Engineering

## Integrantes del equipo

- Mario Padilla Franco
- Gustavo Lucca Padilla
- Matteo Davidhi
- Ian Herman
- Javier López Morales

## Presentación

Esta entrega recoge la definición y revisión de los requisitos del software de una máquina de café de vending y la aplicación del mismo proceso al proyecto propio del equipo: un sistema de generación automática de modelos y pruebas de ciberseguridad mediante IA generativa.

El trabajo parte de una especificación inicial, continúa con una evaluación general de calidad y una revisión frente a reglas seleccionadas de INCOSE, y concluye con el análisis crítico de los resultados. Se incluyen las sucesivas versiones de requisitos, los prompts, las respuestas originales de las evaluaciones y las decisiones justificadas del equipo.

**Referencia académica:** [enunciado de la práctica](docs/enunciado/P1.docx.pdf).

## Síntesis de resultados

| Caso de estudio | Requisitos iniciales (v1) | Evaluación general (v2) | Revisión INCOSE (v3) |
| --- | --- | --- | --- |
| Máquina de café | 24 funcionales y 2 no funcionales | 24 funcionales y 2 no funcionales | 27 funcionales y 2 no funcionales |
| Proyecto propio | 15 funcionales y 4 no funcionales | 16 funcionales y 4 no funcionales | 30 funcionales y 4 no funcionales |

La evaluación general permitió concretar comportamientos, límites y criterios de verificación. La revisión INCOSE contribuyó a explicitar condiciones y separar obligaciones independientes. El aumento del número de requisitos refleja estas descomposiciones y las decisiones documentadas; no se utiliza como indicador de calidad.

## Ejercicio 1. Requisitos iniciales de la máquina de café

Se identifican los actores, las necesidades, los límites y los supuestos del sistema. La especificación incluye selección de bebidas, disponibilidad de ingredientes y vasos, pago, cancelación, preparación y comunicación de incidencias.

- [Contexto y alcance](docs/01-requisitos-iniciales/contexto-y-alcance.md).
- [Requisitos iniciales — v1](docs/01-requisitos-iniciales/requisitos-v1.md): identificador, enunciado, descripción, módulo y criterio de verificación.

## Ejercicio 2. Evaluación general de calidad mediante IA

Se revisan ambigüedades, información incompleta, verificabilidad, redundancias, contradicciones y posibles omisiones. Las dos evaluaciones se consolidan en 14 asuntos, además de dos preguntas adicionales, con decisiones justificadas del equipo.

- [Prompt de evaluación](docs/02-evaluacion-ia/prompt.md).
- Evaluaciones originales: [OpenAI gpt-6.1-sol](docs/02-evaluacion-ia/respuesta-openai-gpt-6.1-sol.md) y [DeepSeek deepseek-v4.1-flash-free](docs/02-evaluacion-ia/respuesta-deepseek-v4.1-flash-free.md).
- [Evaluación consolidada y decisiones](docs/02-evaluacion-ia/evaluacion-y-decisiones.md).
- [Requisitos revisados — v2](docs/02-evaluacion-ia/requisitos-v2.md).

## Ejercicio 3. Evaluación frente a reglas INCOSE

La revisión aborda singularidad, claridad, estructura gramatical, términos subjetivos, condiciones de aplicación y verificabilidad. Se utiliza la hoja-resumen oficial de la *INCOSE Guide to Writing Requirements v4* y una selección explícita de reglas. Las 15 observaciones de los dos modelos se agrupan en 12 temas para su revisión y decisión.

- [Reglas seleccionadas y alcance de la evaluación](docs/03-evaluacion-incose/reglas-seleccionadas.md).
- [Hoja-resumen oficial INCOSE v4](docs/03-evaluacion-incose/incose_rwg_gtwr_v4_summary_sheet.pdf).
- [Prompt de evaluación INCOSE](docs/03-evaluacion-incose/prompt.md).
- Evaluaciones originales: [OpenAI gpt-6.1-sol](docs/03-evaluacion-incose/respuesta-openai-gpt-6.1-sol.md) y [DeepSeek deepseek-v4.1-flash-free](docs/03-evaluacion-incose/respuesta-deepseek-v4.1-flash-free.md).
- [Matriz de evaluación y decisiones](docs/03-evaluacion-incose/matriz-y-decisiones.md).
- [Requisitos revisados — v3](docs/03-evaluacion-incose/requisitos-v3.md).
- [Comparativa de evaluaciones y valoración crítica](docs/03-evaluacion-incose/comparativa-evaluaciones.md).

## Ejercicio 5. Aplicación al proyecto propio

El proyecto propio transforma requisitos de control de acceso en modelos lógicos RBAC/ABAC y casos de prueba, con supervisión del analista. Su especificación distingue generación, validación estática y ejecución sobre una API de simulación o de referencia, e incluye trazabilidad y métricas.

### Requisitos iniciales

- [Enunciado del proyecto final](docs/05-proyecto-propio/01-requisitos-iniciales/PROYECTO_FINAL.pdf).
- [Contexto y alcance](docs/05-proyecto-propio/01-requisitos-iniciales/contexto-y-alcance.md).
- [Requisitos iniciales — v1](docs/05-proyecto-propio/01-requisitos-iniciales/requisitos-v1.md).

### Evaluación general de calidad

- [Prompt de evaluación](docs/05-proyecto-propio/02-evaluacion-ia/prompt.md).
- [Evaluación original de Grok 4.7](docs/05-proyecto-propio/02-evaluacion-ia/respuesta-grok4.7-extrahigh-fast.md).
- [Evaluación y decisiones sobre los 37 hallazgos](docs/05-proyecto-propio/02-evaluacion-ia/evaluacion-y-decisiones.md).
- [Requisitos revisados — v2](docs/05-proyecto-propio/02-evaluacion-ia/requisitos-v2.md).

### Evaluación INCOSE y análisis crítico

- [Reglas seleccionadas](docs/05-proyecto-propio/03-evaluacion-incose/reglas-seleccionadas.md).
- [Prompt de evaluación INCOSE](docs/05-proyecto-propio/03-evaluacion-incose/prompt.md).
- [Evaluación original de Grok 4.7](docs/05-proyecto-propio/03-evaluacion-incose/respuesta-spacexai-grok-4.7.md).
- [Matriz y decisiones sobre las 18 observaciones](docs/05-proyecto-propio/03-evaluacion-incose/matriz-y-decisiones.md).
- [Requisitos revisados — v3](docs/05-proyecto-propio/03-evaluacion-incose/requisitos-v3.md).
- [Comparativa de evaluaciones y valoración crítica](docs/05-proyecto-propio/03-evaluacion-incose/comparativa-evaluaciones.md).

## Conclusiones

La IA resultó útil para identificar posibles problemas y estructurar la revisión, mientras que el criterio del equipo fue necesario para valorar las propuestas, preservar el alcance y decidir los cambios. La comparación de evaluaciones también mostró límites de interpretación, clasificación y suficiencia de los criterios de verificación.

- [Conclusiones sobre las ventajas y limitaciones de la IA generativa](docs/conclusiones.md).

## Alcance de los resultados

Las versiones v3 de ambos casos y sus análisis comparativos están revisados y confirmados por el equipo. Las versiones anteriores y las respuestas originales se conservan como evidencia de la evolución documental.

La evaluación INCOSE se limita a las reglas seleccionadas y no declara conformidad con toda la guía. R1 conserva una limitación por ausencia de un patrón formal acordado. En el proyecto propio, el protocolo de rendimiento mantiene pendientes la selección del corpus, la configuración, el entorno y las repeticiones de medida. Los criterios de verificación incluidos en los requisitos describen comprobaciones previstas.
