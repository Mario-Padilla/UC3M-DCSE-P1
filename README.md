# UC3M-DCSE-P1

Práctica 1 — Ingeniería de requisitos asistida por IA y desarrollo dirigido por especificación.

## Objetivo

Desarrollar el ciclo de ingeniería de requisitos de una máquina de café de vending: definición del alcance, escritura y evaluación de requisitos, revisión según INCOSE y, si se aborda el ejercicio 4, implementación y verificación de una simulación mediante un flujo dirigido por especificaciones.

Las decisiones y la validación final corresponden al equipo. El ejercicio 5 aplica el flujo al proyecto propio.

## Cómo utilizar esta repo

1. Leer el [enunciado](docs/enunciado/P1.docx.pdf) y esta metodología.
2. Acordar el reparto de trabajo y el alcance antes de redactar requisitos.
3. Seguir las fases de la sección **Metodología**, guardando cada resultado en el archivo indicado.
4. Conservar las versiones y las evidencias de evaluación: deben poder reconstruirse los cambios y sus motivos.
5. Revisar el trabajo en equipo y actualizar el estado del bloque en el índice de entregables.

Este README es la referencia de trabajo para las personas. [AGENTS.md](AGENTS.md) contiene las instrucciones operativas para los asistentes de IA que colaboren en la repo. La metodología y las convenciones aquí descritas son acuerdos de organización propuestos para el equipo; los requisitos de la entrega proceden del enunciado.

## Estructura

```text
UC3M-DCSE-P1/
├── README.md
├── AGENTS.md
├── docs/
│   ├── enunciado/
│   │   └── P1.docx.pdf
│   ├── 01-requisitos-iniciales/
│   │   ├── contexto-y-alcance.md
│   │   └── requisitos-v1.md
│   ├── 02-evaluacion-ia/
│   │   ├── prompt.md
│   │   ├── respuesta-ia.md
│   │   ├── evaluacion-y-decisiones.md
│   │   └── requisitos-v2.md
│   ├── 03-evaluacion-incose/
│   │   ├── reglas-seleccionadas.md
│   │   ├── prompt.md
│   │   ├── respuesta-ia.md
│   │   ├── matriz-y-decisiones.md
│   │   ├── requisitos-v3.md
│   │   └── comparativa-evaluaciones.md
│   ├── 04-verificacion/
│   │   ├── plan-de-pruebas.md
│   │   ├── trazabilidad.csv
│   │   └── informe-verificacion.md
│   ├── 05-proyecto-propio/
│   │   ├── contexto-y-alcance.md
│   │   ├── requisitos-v1.md
│   │   └── evaluaciones/
│   └── conclusiones.md
├── openspec/
├── src/
└── tests/
```

Las carpetas sin contenido incluyen un archivo `.gitkeep` para conservarlas en Git.

## Índice de entregables

| Bloque | Documentos | Estado |
| --- | --- | --- |
| Enunciado | [PDF de la práctica](docs/enunciado/P1.docx.pdf) | Disponible |
| Ejercicio 1 | [Contexto y alcance](docs/01-requisitos-iniciales/contexto-y-alcance.md), [requisitos v1](docs/01-requisitos-iniciales/requisitos-v1.md) | Pendiente |
| Ejercicio 2 | [Prompt](docs/02-evaluacion-ia/prompt.md), [respuesta de IA](docs/02-evaluacion-ia/respuesta-ia.md), [evaluación y decisiones](docs/02-evaluacion-ia/evaluacion-y-decisiones.md), [requisitos v2](docs/02-evaluacion-ia/requisitos-v2.md) | Pendiente |
| Ejercicio 3 | [Reglas seleccionadas](docs/03-evaluacion-incose/reglas-seleccionadas.md), [prompt](docs/03-evaluacion-incose/prompt.md), [respuesta de IA](docs/03-evaluacion-incose/respuesta-ia.md), [matriz y decisiones](docs/03-evaluacion-incose/matriz-y-decisiones.md), [requisitos v3](docs/03-evaluacion-incose/requisitos-v3.md), [comparativa](docs/03-evaluacion-incose/comparativa-evaluaciones.md) | Pendiente |
| Ejercicio 4 | [OpenSpec](openspec/), [código](src/), [pruebas](tests/), [plan de pruebas](docs/04-verificacion/plan-de-pruebas.md), [trazabilidad](docs/04-verificacion/trazabilidad.csv), [informe de verificación](docs/04-verificacion/informe-verificacion.md) | Pendiente; opcional según el apartado 1.6 |
| Ejercicio 5 | [Contexto y alcance](docs/05-proyecto-propio/contexto-y-alcance.md), [requisitos v1](docs/05-proyecto-propio/requisitos-v1.md), [evaluaciones](docs/05-proyecto-propio/evaluaciones/) | Pendiente |
| Conclusiones | [Ventajas y limitaciones de la IA](docs/conclusiones.md) | Pendiente |

## Metodología

El flujo principal es:

```text
Contexto y alcance → requisitos v1 → evaluación general con IA → requisitos v2
→ evaluación INCOSE → requisitos v3 → especificaciones → código → pruebas
```

Las decisiones humanas y las evidencias se registran durante todo el proceso. El ejercicio 5 reutiliza el método para el proyecto propio.

### 0. Coordinar el trabajo

- Asignar un responsable de redacción y un revisor por bloque. Una misma persona puede asumir varias tareas; la revisión debe quedar identificada.
- Acordar las funcionalidades incluidas y excluidas, las herramientas y la forma de registrar las decisiones.
- Utilizar estos estados en el índice: `Pendiente`, `En curso`, `En revisión` y `Completado`. Si un bloque no se realiza, indicar `No realizado` y el motivo.
- Registrar en el documento principal de cada bloque su responsable, revisor, fecha, estado y entradas utilizadas. Mientras no se hayan asignado, usar `TODO`.
- Dividir las tareas por entregables o conjuntos de requisitos y acordar quién edita cada archivo para reducir conflictos.

**Punto pendiente de aclaración:** el ejercicio 4 aparece como opcional en el apartado 1.6, aunque sus entregables figuran en la entrega agregada. Confirmar con el profesor cómo se aplica esa opcionalidad y documentar la decisión del equipo.

### 1. Definir el contexto y redactar los requisitos iniciales

**Entrada:** caso de estudio del enunciado.

1. Identificar los actores, sus necesidades y las funcionalidades principales.
2. Acordar los límites del sistema, sus interfaces, los supuestos y las exclusiones.
3. Definir un glosario para utilizar los mismos términos en todos los documentos.
4. Redactar requisitos funcionales y no funcionales, con identificadores únicos y criterios observables de verificación.
5. Revisar en equipo que cada requisito responde a una necesidad dentro del alcance.

| Archivo | Contenido esperado |
| --- | --- |
| `docs/01-requisitos-iniciales/contexto-y-alcance.md` | Actores, necesidades, funcionalidades, límites, interfaces, supuestos, exclusiones y glosario. Las decisiones pendientes deben estar identificadas. |
| `docs/01-requisitos-iniciales/requisitos-v1.md` | Tabla inicial con ID, texto, descripción, módulo si procede y criterio de verificación. Incluir el tipo funcional o no funcional. |

**Cierre:** el equipo ha revisado el alcance y la v1; los requisitos tienen identificador y criterio de verificación. Conservar esta versión como entrada de la siguiente fase, sin corregirla retrospectivamente para ocultar problemas detectados después.

### 2. Evaluar la calidad con IA y obtener v2

**Entrada:** requisitos v1 y su contexto.

1. Preparar un prompt que solicite una evaluación individual de todos los requisitos.
2. Solicitar ambigüedades, información incompleta, falta de verificabilidad, redundancias, contradicciones y omisiones, con justificación de los hallazgos.
3. Guardar el prompt exacto, la respuesta y los datos de la ejecución.
4. Revisar cada observación: aceptarla, rechazarla o aceptarla parcialmente, justificando la decisión. Las pendientes deben quedar señaladas.
5. Generar v2 a partir de las decisiones del equipo y registrar los cambios respecto a v1.

| Archivo | Contenido esperado |
| --- | --- |
| `docs/02-evaluacion-ia/prompt.md` | Prompt exacto, documentos de entrada y versión evaluada. |
| `docs/02-evaluacion-ia/respuesta-ia.md` | Respuesta original y metadatos de ejecución. Identificar cualquier extracto u omisión. |
| `docs/02-evaluacion-ia/evaluacion-y-decisiones.md` | Matriz de calidad por requisito, observaciones identificadas, decisiones justificadas y registro de cambios. Señalar también requisitos sin problemas detectados. |
| `docs/02-evaluacion-ia/requisitos-v2.md` | Tabla completa revisada y referencia a las decisiones que originan los cambios. |

**Cierre:** todos los requisitos han sido evaluados y cada observación tiene una decisión justificada del equipo. La v2 es coherente con esas decisiones. Las omisiones propuestas por la IA solo se incorporan si el equipo confirma su necesidad y su encaje en el alcance.

### 3. Evaluar con INCOSE y obtener v3

**Entrada habitual:** requisitos v2, contexto y reglas seleccionadas de la guía INCOSE.

1. Consultar la *INCOSE Guide to Writing Requirements* y registrar la edición y la referencia utilizada.
2. Seleccionar reglas explícitas y documentar sus identificadores, significado y forma de evaluación. Verificar los identificadores en la edición consultada.
3. Preparar un prompt que evalúe cada requisito frente a esas reglas y justifique los resultados.
4. Revisar singularidad, claridad, estructura gramatical, términos subjetivos, condiciones de aplicación y verificabilidad, entre los aspectos seleccionados.
5. Revisar las observaciones, justificar las decisiones y separar los requisitos que agrupen varias obligaciones cuando corresponda.
6. Generar v3 y comparar los resultados con la evaluación general del ejercicio 2.

| Archivo | Contenido esperado |
| --- | --- |
| `docs/03-evaluacion-incose/reglas-seleccionadas.md` | Edición y fuente consultadas, reglas seleccionadas y criterios de aplicación. Distinguir las reglas de la guía de las adaptaciones del equipo. |
| `docs/03-evaluacion-incose/prompt.md` | Prompt exacto, reglas proporcionadas y versión evaluada. |
| `docs/03-evaluacion-incose/respuesta-ia.md` | Respuesta original con metadatos de ejecución. |
| `docs/03-evaluacion-incose/matriz-y-decisiones.md` | Evaluación por requisito y regla, evidencia, decisión humana justificada y cambios derivados. |
| `docs/03-evaluacion-incose/requisitos-v3.md` | Tabla completa revisada y relaciones con los requisitos de versiones anteriores. |
| `docs/03-evaluacion-incose/comparativa-evaluaciones.md` | Coincidencias, diferencias, hallazgos nuevos, observaciones erróneas y valoración crítica de la aplicación de INCOSE por la IA. |

Para la matriz se pueden utilizar `Cumple`, `No cumple`, `No aplica` y `No evaluado`, siempre con justificación cuando proceda.

**Comparación de métodos:** si el ejercicio 2 evalúa v1 y el ejercicio 3 evalúa v2, las entradas son distintas. Indicarlo en la comparativa: una diferencia de hallazgos puede deberse a las correcciones previas. Para comparar ambos métodos sobre la misma entrada, se puede añadir una evaluación INCOSE de v1, conservándola como una ejecución adicional identificada.

**Cierre:** cada requisito ha sido evaluado frente a las reglas seleccionadas, las decisiones están justificadas y v3 recoge los cambios aprobados. El equipo identifica expresamente qué versión queda aprobada para derivar las especificaciones.

### 4. Derivar especificaciones, implementar y verificar

**Entrada:** versión de requisitos aprobada y decisión sobre la realización del ejercicio 4.

1. Concretar el alcance funcional de la simulación a partir de los requisitos aprobados.
2. Inicializar OpenSpec o la herramienta equivalente acordada y registrar su versión. Utilizar su estructura de propuesta, especificaciones, diseño y tareas cuando corresponda.
3. Derivar escenarios verificables, identificando los requisitos de origen. Contemplar situaciones normales, errores y condiciones límite relevantes.
4. Implementar los comportamientos especificados y mantener la relación con los elementos de código.
5. Diseñar las pruebas a partir de los requisitos y sus escenarios; automatizarlas cuando sea viable.
6. Ejecutarlas, conservar las evidencias y corregir los incumplimientos detectados. Repetir las pruebas afectadas tras las correcciones.
7. Completar la trazabilidad y el informe de verificación. Añadir al README los comandos reales de instalación, ejecución y pruebas cuando se elija la tecnología.

| Ubicación | Contenido esperado |
| --- | --- |
| `openspec/` | Artefactos reales de la herramienta: propuestas, especificaciones, diseño y tareas según el flujo utilizado. |
| `src/` | Código fuente de la aplicación. |
| `tests/` | Pruebas automatizadas y recursos necesarios para ejecutarlas. |
| `docs/04-verificacion/plan-de-pruebas.md` | Requisito y escenario cubiertos, precondiciones, datos de entrada, pasos, resultado esperado y método manual o automatizado. |
| `docs/04-verificacion/trazabilidad.csv` | Relaciones entre requisitos originales y aprobados, escenarios, implementación, pruebas y resultados. |
| `docs/04-verificacion/informe-verificacion.md` | Fecha, entorno y revisión de código evaluada, comandos ejecutados, resultados observados, referencias a evidencias e incumplimientos pendientes. |

**Cierre:** la aplicación se puede ejecutar con las instrucciones documentadas; todos los requisitos del alcance tienen un estado de verificación y las pruebas ejecutadas cuentan con evidencia. Los fallos y lo no verificado deben figurar explícitamente; una entrega cerrada no implica que todo haya pasado.

### 5. Aplicar el flujo al proyecto propio

**Entrada:** descripción y objetivos del proyecto del equipo.

1. Definir su contexto, actores, necesidades y alcance en `docs/05-proyecto-propio/contexto-y-alcance.md`.
2. Redactar su primera tabla de requisitos en `docs/05-proyecto-propio/requisitos-v1.md`, con un prefijo de identificadores diferente al de la cafetera.
3. Aplicar las evaluaciones anteriores y guardar en `docs/05-proyecto-propio/evaluaciones/` los prompts, respuestas, reglas y decisiones de cada evaluación realizada, con nombres que identifiquen fase y ejecución.
4. Guardar las versiones revisadas junto a v1 como `requisitos-v2.md`, `requisitos-v3.md`, según se generen, y enlazarlas desde el índice de entregables.

**Cierre:** existe una primera versión de requisitos del proyecto y está documentado el flujo de revisión aplicado. Acordar con el profesor cualquier duda sobre la profundidad esperada; el ejercicio 5 no describe expresamente una segunda implementación completa.

### 6. Redactar las conclusiones y revisar la entrega

Completar `docs/conclusiones.md` con ejemplos reales del trabajo: aportaciones útiles de la IA, errores o sugerencias rechazadas, limitaciones al aplicar INCOSE y valor de la revisión humana. Si se realiza el ejercicio 4, incluir la experiencia al derivar especificaciones y verificar la aplicación.

Antes de entregar, comprobar:

- Están disponibles los requisitos iniciales y todas las versiones utilizadas.
- Los prompts y las respuestas relevantes identifican sus entradas y su ejecución.
- Las matrices de calidad y de INCOSE permiten seguir las decisiones del equipo.
- El análisis comparativo identifica las versiones evaluadas y sus limitaciones.
- El ejercicio 5 y las conclusiones están documentados.
- Si se realiza el ejercicio 4, se incluyen sus artefactos, código, pruebas, resultados y trazabilidad.
- Los enlaces del README funcionan y los estados reflejan el avance real.
- Los `TODO` restantes están resueltos o identificados como pendientes de la entrega.

## Convenciones de documentación

### Identificadores y tabla de requisitos

| Tipo | Patrón | Ejemplo ilustrativo |
| --- | --- | --- |
| Funcional de la cafetera | `CAF-RF-NNN` | `CAF-RF-001` |
| No funcional de la cafetera | `CAF-RNF-NNN` | `CAF-RNF-001` |
| Funcional del proyecto propio | `PROY-RF-NNN` | `PROY-RF-001` |
| No funcional del proyecto propio | `PROY-RNF-NNN` | `PROY-RNF-001` |

Utilizar como mínimo esta estructura en las tablas:

```text
ID | Tipo | Texto | Descripción | Módulo | Criterio de verificación
```

- El texto expresa la obligación; la descripción aporta contexto o justificación.
- El criterio de verificación define cómo observar el cumplimiento y el resultado esperado. Evitar expresiones sin medida como «funciona correctamente».
- Si no hay módulo aplicable, indicar `No aplica` y mantener el criterio en todas las versiones.
- Mantener el identificador cuando se refine la misma obligación. La versión se identifica en el documento, no cambiando el ID.
- Al dividir un requisito, asignar nuevos IDs y registrar de cuál proceden. Marcar el original como sustituido en el registro de cambios.
- No reutilizar IDs retirados para obligaciones distintas.
- Conservar v1, v2 y v3 como evidencias de sus fases. Una corrección posterior debe quedar registrada; no reescribir silenciosamente una versión ya revisada.

### Evidencias y decisiones sobre IA

Cada ejecución debe permitir identificar: herramienta, modelo o versión disponible, fecha, prompt, documentos y versiones de entrada. Si un dato no está disponible, indicarlo expresamente.

En `respuesta-ia.md`, separar los metadatos de la salida original. Mantener las respuestas sin corregirlas para que coincidan con las decisiones posteriores. Si se conserva solo un extracto relevante, señalarlo y explicar qué se ha omitido. Las nuevas ejecuciones se guardan en archivos identificados, por ejemplo `prompt-02.md` y `respuesta-ia-02.md`, enlazados desde el documento de decisiones.

La revisión humana puede utilizar esta tabla:

```text
Observación | Requisito(s) | Hallazgo y justificación de la IA |
Decisión del equipo | Justificación del equipo | Cambio y requisito resultante
```

Usar `Aceptada`, `Rechazada`, `Aceptada parcialmente` o `Pendiente`. Una propuesta generada por IA conserva el estado pendiente hasta que el equipo la revise. El registro de cambios debe relacionar versión de origen, versión de destino, IDs afectados, modificación y motivo.

## Cómo mantener la trazabilidad

La matriz [trazabilidad.csv](docs/04-verificacion/trazabilidad.csv) permite comprobar que cada requisito se ha desarrollado y verificado, y localizar qué elementos se verían afectados por un cambio.

```text
Requisito original → requisito aprobado → escenario → implementación → prueba → resultado/evidencia
```

| Columna del CSV | Qué registrar | Cuándo rellenarla |
| --- | --- | --- |
| `requisito_original` | ID y versión inicial de origen. Si aparece después, indicar la versión en que se introdujo. | Al establecer las relaciones entre versiones. |
| `requisito_aprobado` | ID y versión aprobados para implementar. | Al aprobar la base de requisitos. |
| `especificacion_escenario` | Ruta y nombre o identificador del escenario verificable. | Al derivar especificaciones. |
| `elemento_implementado` | Ruta y función, clase o componente responsable. | Al implementar. |
| `prueba` | Ruta e identificador de prueba automatizada, o caso manual del plan. | Al diseñar las pruebas. |
| `resultado` | `Pendiente`, `PASS`, `FAIL`, `Bloqueada` o `No aplica` con justificación. | Pendiente antes de ejecutar; resultado real después. |
| `evidencia` | Ruta o enlace al informe o registro de la ejecución, con fecha y revisión evaluada. | Tras ejecutar o justificar la no aplicación. |

Ejemplo ilustrativo; no representa requisitos aprobados ni archivos implementados:

```csv
requisito_original,requisito_aprobado,especificacion_escenario,elemento_implementado,prueba,resultado,evidencia
CAF-RF-004 v1,CAF-RF-004 v3,TODO: escenario de ingredientes insuficientes,TODO: componente de inventario,TODO: prueba de stock insuficiente,Pendiente,
```

- Utilizar una fila por relación de verificación. Si un requisito necesita varias pruebas, repetir el ID en varias filas; si una prueba cubre varios requisitos, registrar cada relación.
- Mantener una fila pendiente para requisitos aún sin escenario, implementación o prueba; así las carencias permanecen visibles.
- Las divisiones de requisitos pueden producir varias filas que compartan el requisito original.
- Los requisitos retirados se justifican en el registro de cambios; los aprobados fuera del alcance implementado deben señalarse expresamente, sin presentarlos como verificados.
- Registrar resultados de una ejecución identificada y coherente con el informe. Después de un cambio que invalide la evidencia anterior, marcar la verificación afectada como pendiente hasta repetirla.
- Editar el CSV en UTF-8 con comas como separador, usando comillas dobles si un campo contiene comas o saltos de línea. Puede abrirse en un editor, Excel o LibreOffice Calc.

## Colaboración y revisión

1. Acordar el bloque y los archivos que se van a editar. Para cambios en paralelo, utilizar ramas descriptivas, por ejemplo `docs/evaluacion-ia`.
2. Realizar cambios centrados en una tarea y conservar las fuentes, versiones y evidencias asociadas.
3. Solicitar al revisor que compruebe contenido, coherencia con los requisitos y ubicación de los artefactos. Registrar quién revisó y las decisiones adoptadas en el documento del bloque.
4. Integrar el trabajo mediante el procedimiento acordado por el equipo, utilizando una pull request si se trabaja en GitHub.
5. Actualizar el índice del README cuando cambie el estado o se añadan entregables. `Completado` requiere revisión humana y cumplimiento del criterio de cierre de la fase.

## Estado de la base del proyecto

Los entregables están preparados con marcadores `TODO`; la matriz de trazabilidad contiene únicamente la cabecera. Las carpetas `openspec/`, `src/` y `tests/` están reservadas para el ejercicio 4. Todavía no se ha definido una tecnología de implementación ni hay comandos de ejecución o pruebas establecidos. El índice de entregables debe mantenerse actualizado a medida que avance el trabajo.
