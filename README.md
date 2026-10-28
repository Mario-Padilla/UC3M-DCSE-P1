# UC3M-DCSE-P1

Práctica 1 — Ingeniería de requisitos asistida por IA y desarrollo dirigido por especificación.

## Objetivo

Documentar el ciclo de ingeniería de requisitos de una máquina de café de vending y aplicar el proceso al proyecto propio del equipo. El ejercicio 4 —implementación y verificación— es opcional según el apartado 1.6 del [enunciado](docs/enunciado/P1.docx.pdf).

## Cómo usar esta repo

Esta repo sirve como **estructura e índice del trabajo**. Los documentos de cada carpeta contienen lo realizado; el estado de la tabla siguiente indica el progreso actual. Git conserva el historial de cambios.

### Cómo iniciar una solicitud a la IA

```text
Antes de responder o hacer cambios, lee README.md y AGENTS.md para
entender el contexto del proyecto y seguir sus instrucciones.

Al generar una evaluación con IA, indica el proveedor y el modelo utilizado
(incluida la versión si se conoce) en la respuesta y en el nombre del archivo.
Si no se puede confirmar el modelo, indícalo expresamente en vez de inferirlo.

Mi solicitud es: [escribe aquí lo que necesitas].
```

## Índice de ejercicios y entregables

| Bloque | Entregables | Estado |
| --- | --- | --- |
| Enunciado | [PDF de la práctica](docs/enunciado/P1.docx.pdf) | Disponible |
| Ejercicio 1: requisitos iniciales | [Contexto y alcance](docs/01-requisitos-iniciales/contexto-y-alcance.md), [requisitos v1](docs/01-requisitos-iniciales/requisitos-v1.md) | Cerrado por confirmación del equipo; v1 se conserva como versión inicial y las revisiones posteriores se recogen en v2 y v3 |
| Ejercicio 2: evaluación general con IA | [Prompt común](docs/02-evaluacion-ia/prompt.md), [respuesta OpenAI gpt-6.1-sol](docs/02-evaluacion-ia/respuesta-openai-gpt-6.1-sol.md), [respuesta deepseek-v4.1-flash-free](docs/02-evaluacion-ia/respuesta-deepseek-v4.1-flash-free.md), [evaluación y decisiones](docs/02-evaluacion-ia/evaluacion-y-decisiones.md), [requisitos v2](docs/02-evaluacion-ia/requisitos-v2.md) | Cerrado por decisión del equipo con las evaluaciones actuales, las decisiones registradas y los requisitos v2; podrán incorporarse otros modelos como ampliación futura |
| Ejercicio 3: evaluación INCOSE | [Reglas seleccionadas](docs/03-evaluacion-incose/reglas-seleccionadas.md), [prompt](docs/03-evaluacion-incose/prompt.md), [respuesta OpenAI gpt-6.1-sol](docs/03-evaluacion-incose/respuesta-openai-gpt-6.1-sol.md), [respuesta DeepSeek deepseek-v4.1-flash-free](docs/03-evaluacion-incose/respuesta-deepseek-v4.1-flash-free.md), [matriz y decisiones](docs/03-evaluacion-incose/matriz-y-decisiones.md), [requisitos v3](docs/03-evaluacion-incose/requisitos-v3.md), [comparativa](docs/03-evaluacion-incose/comparativa-evaluaciones.md) | Decisiones registradas para 15 observaciones en 12 temas; CAF-RF-003A confirmado y v3 preparada con 27 requisitos funcionales y 2 no funcionales. Pendientes la revisión final de v3 por el equipo, la comparativa con el ejercicio 2 y la valoración crítica de los análisis |
| Ejercicio 4: implementación y verificación | [OpenSpec](openspec/), [código](src/), [pruebas](tests/), [plan de pruebas](docs/04-verificacion/plan-de-pruebas.md), [trazabilidad](docs/04-verificacion/trazabilidad.csv), [informe](docs/04-verificacion/informe-verificacion.md) | Pendiente; opcional según el apartado 1.6 |
| Ejercicio 5: proyecto propio | [Contexto y alcance](docs/05-proyecto-propio/contexto-y-alcance.md), [requisitos v1](docs/05-proyecto-propio/requisitos-v1.md), [prompt](docs/05-proyecto-propio/evaluaciones/prompt.md), [evaluación y decisiones](docs/05-proyecto-propio/evaluaciones/evaluacion-y-decisiones.md), [requisitos v2](docs/05-proyecto-propio/evaluaciones/requisitos-v2.md) | Requisitos v2 preparados a partir de la evaluación Grok 4.7; pendiente la confirmación del equipo. El contexto no se ha modificado |
| Conclusiones | [Ventajas y limitaciones de la IA](docs/conclusiones.md) | Pendiente |

## Orden general del trabajo

1. Definir contexto, alcance y requisitos iniciales de la cafetera.
2. Evaluar los requisitos con IA y preparar la versión revisada.
3. Evaluarlos frente a reglas seleccionadas de INCOSE y preparar la siguiente versión y comparativa.
4. Si se realiza el ejercicio opcional, derivar especificaciones, implementar y verificar.
5. Aplicar el proceso al proyecto propio y redactar las conclusiones.

Conservar las versiones de requisitos y las evidencias de las evaluaciones que se realicen. Las respuestas originales de IA deben distinguirse de las decisiones del equipo. No presentar propuestas como decisiones acordadas.

## Organización de archivos

```text
docs/
├── enunciado/
├── 01-requisitos-iniciales/
├── 02-evaluacion-ia/
├── 03-evaluacion-incose/
├── 04-verificacion/
├── 05-proyecto-propio/
└── conclusiones.md
openspec/   # Ejercicio 4, si se realiza
src/        # Ejercicio 4, si se realiza
tests/      # Ejercicio 4, si se realiza
```

La matriz de trazabilidad forma parte de los entregables de verificación si se realiza el ejercicio 4. No es necesario mantenerla durante el trabajo ordinario de documentación.
