# Instrucciones para agentes de IA

## Propósito y alcance

Estas instrucciones se aplican a toda la repo. El proyecto corresponde a la práctica de ingeniería de requisitos asistida por IA de una máquina de café de vending y a su aplicación al proyecto propio del equipo.

Leer [README.md](README.md) antes de realizar cambios. El README contiene la metodología del equipo, las convenciones y los criterios de cierre; este archivo concreta cómo debe colaborar un agente. Consultar el [enunciado](docs/enunciado/P1.docx.pdf) cuando sea necesario comprobar una exigencia académica. No presentar las convenciones internas como obligaciones impuestas por el profesor.

## Procedimiento al iniciar una tarea

1. Identificar la petición, la fase afectada y sus entregables en el README.
2. Revisar el estado de Git y los archivos pertinentes antes de editar. Respetar el trabajo existente, incluidos cambios sin confirmar y archivos sin seguimiento.
3. Identificar la versión de requisitos que sirve de entrada y comprobar si está propuesta, en revisión o aprobada por el equipo.
4. Consultar las decisiones y los supuestos asociados antes de interpretar o modificar un requisito.
5. Si falta información, avanzar en las partes independientes y señalar la decisión pendiente. Pedir aclaración cuando la incertidumbre impida una edición correcta.

## Ubicación de los cambios

| Trabajo | Destino |
| --- | --- |
| Metodología, índice, estado y comandos de uso | `README.md` |
| Instrucciones operativas para agentes | `AGENTS.md` |
| Fuentes del enunciado | `docs/enunciado/` |
| Alcance y requisitos iniciales de la cafetera | `docs/01-requisitos-iniciales/` |
| Evaluación general con IA y v2 | `docs/02-evaluacion-ia/` |
| Evaluación INCOSE, comparativa y v3 | `docs/03-evaluacion-incose/` |
| Plan, matriz de trazabilidad e informe de verificación | `docs/04-verificacion/` |
| Requisitos y evaluaciones del proyecto propio | `docs/05-proyecto-propio/` |
| Conclusiones basadas en el trabajo realizado | `docs/conclusiones.md` |
| Artefactos de especificación dirigida | `openspec/` |
| Implementación | `src/` |
| Pruebas automatizadas | `tests/` |

Crear archivos adicionales solo cuando la tarea lo requiera, con nombres descriptivos y enlaces desde los documentos pertinentes. Conservar los `TODO` ajenos al trabajo solicitado. Un `.gitkeep` puede retirarse cuando su carpeta ya contenga archivos versionables reales.

## Requisitos y control de versiones

- Seguir los prefijos y campos de tabla establecidos en el README: `CAF-RF`, `CAF-RNF`, `PROY-RF` y `PROY-RNF`.
- Comprobar los IDs existentes antes de asignar uno nuevo. No reutilizar IDs retirados.
- Mantener el ID al refinar la misma obligación; asignar nuevos IDs al dividirla y registrar las relaciones de origen y sustitución.
- Conservar las versiones de cada fase. No trasladar correcciones de v2 o v3 a v1 para hacer desaparecer el historial de problemas.
- Registrar toda corrección de una versión ya revisada con origen, destino, IDs afectados y motivo. Si cambia una base aprobada, identificarla como propuesta pendiente de validación humana y registrar el impacto.
- Distinguir obligación, descripción, supuesto, decisión y criterio de verificación. No convertir una sugerencia de implementación en requisito sin justificación.
- Formular criterios observables. No inventar umbrales, tiempos, precios, recetas o políticas de pago como si los hubiera aprobado el equipo; identificarlos como propuestas o decisiones pendientes.
- No ampliar el alcance por iniciativa propia al detectar una posible omisión. Documentarla y relacionarla con la necesidad que podría justificarla.

## Uso de IA y conservación de evidencias

La IA asiste en el análisis y la redacción; la aceptación de observaciones y la aprobación de requisitos corresponden al equipo.

- Al realizar una evaluación, identificar el prompt exacto, la herramienta, el modelo disponible, la fecha y los documentos y versiones aportados. Si un dato se desconoce, declararlo.
- Evaluar los requisitos solicitados de forma individual y relacionar cada hallazgo con su ID. Registrar también los requisitos sin hallazgos.
- Separar la respuesta generada de las decisiones humanas. No editar una respuesta original para adaptarla a una decisión posterior.
- Si se conservan extractos, señalar su carácter parcial y las omisiones. Guardar las ejecuciones adicionales en archivos diferenciados según la convención del README.
- Un análisis retrospectivo de esta sesión no debe presentarse como una ejecución independiente de otra herramienta o modelo.
- Al proponer decisiones, marcarlas como `Pendiente` o como propuestas para revisión. No atribuir aceptación, rechazo, autoría de revisión o aprobación al equipo sin evidencia explícita.
- Si el usuario comunica una decisión humana, registrarla fielmente con su justificación disponible. No inventar motivos ni responsables.
- No completar las conclusiones con experiencias o resultados que aún no han ocurrido.

## Evaluación INCOSE

- Utilizar la edición y las reglas realmente consultadas. Verificar los identificadores y no atribuir numeración o citas a una fuente no disponible.
- Si la guía no está accesible, señalar la referencia pendiente. Se puede proponer una lista de aspectos de revisión, identificándola como propuesta y sin afirmar cumplimiento de reglas concretas no contrastadas.
- Evaluar cada requisito frente a las reglas seleccionadas, indicando evidencia y justificación. Mantener separados el juicio de la IA y la decisión del equipo.
- Documentar la versión evaluada en cada ejecución. Si se compara la evaluación general de v1 con la evaluación INCOSE de v2, explicitar que las entradas son distintas.
- Conservar cualquier evaluación adicional sobre una entrada común como ejecución identificada; no sustituir silenciosamente la evaluación previa.

## Especificaciones e implementación

- El ejercicio 4 figura como opcional en el enunciado. Seguir la decisión comunicada por el equipo y la tarea solicitada; la estructura de carpetas por sí sola no implica que deba implementarse.
- Actualmente no existe una tecnología de aplicación acordada ni comandos establecidos. Comprobar el estado real de la repo antes de asumir lenguaje, framework o dependencias.
- Derivar los comportamientos de los requisitos aprobados y especificar escenarios normales, errores y límites relevantes antes de implementarlos.
- Si no hay una base aprobada y se solicita preparar borradores, identificarlos como provisionales.
- Utilizar los artefactos y convenciones de la versión de OpenSpec o herramienta equivalente realmente utilizada. No inventar archivos generados ni afirmar que una herramienta se ejecutó si no ocurrió.
- Mantener las decisiones de diseño dentro del alcance y registrar las dudas que afecten al comportamiento observable.
- Añadir al README los comandos reales de instalación, ejecución y pruebas cuando existan y hayan sido comprobados.

## Pruebas, trazabilidad y resultados

- Diseñar pruebas a partir de requisitos y escenarios; incluir los casos normales, errores y condiciones límite relevantes. Usar los IDs para facilitar la relación.
- Mantener las columnas y el formato UTF-8 del CSV de trazabilidad. Registrar una fila por relación de verificación conforme al README.
- Actualizar las relaciones afectadas cuando cambien requisitos, escenarios, código o pruebas. Hacer visibles las relaciones aún pendientes.
- `PASS` y `FAIL` solo pueden corresponder a ejecuciones reales identificadas. Si no se ejecutó una prueba, usar `Pendiente` o `Bloqueada`, explicando el motivo.
- Registrar comando o pasos manuales, entorno relevante, fecha, revisión de código evaluada y evidencia de resultados en el informe de verificación.
- No equiparar cobertura de código con cumplimiento de requisitos ni considerar implementado un escenario como evidencia de que pasa una prueba.
- Tras cambios que invaliden una ejecución anterior, marcar como pendiente la verificación afectada hasta repetirla. Conservar la referencia a resultados previos si es relevante para el informe.
- Documentar los fallos y las limitaciones de ejecución. No ocultarlos ni presentar como comprobado lo que solo se ha inspeccionado.

## Verificación antes de finalizar

Aplicar comprobaciones proporcionales a los cambios:

1. Revisar el diff para detectar modificaciones accidentales o contenido ajeno a la tarea.
2. En documentación, comprobar rutas, enlaces locales, nombres de archivos, versiones e IDs referenciados. Ejecutar `git diff --check` para detectar errores de espacios.
3. En tablas y CSV, comprobar columnas y formato, así como relaciones o estados afectados.
4. Si cambia código, ejecutar las pruebas pertinentes con los comandos disponibles. Si no se pueden ejecutar, indicar el bloqueo sin afirmar que pasan.
5. Actualizar el README si cambian estructura, comandos o estado de los entregables. No marcar un bloque como completado sin la revisión humana exigida por la metodología.
6. Resumir los archivos modificados, las comprobaciones realizadas y los pendientes concretos.

Para cambios exclusivamente documentales no hace falta introducir un framework de pruebas ni nuevas dependencias.

## Estilo y colaboración

- Escribir la documentación en español, conservar los nombres de archivo existentes y utilizar Markdown legible y enlaces relativos.
- Mantener una sola explicación completa de la metodología en el README; enlazarla desde otros documentos cuando sea suficiente.
- Identificar claramente ejemplos hipotéticos para que no se confundan con requisitos aprobados, archivos existentes o resultados reales.
- Hacer cambios centrados en la tarea. No eliminar documentos o evidencias ni sobrescribir cambios del equipo sin investigar su propósito.
- No realizar commits, publicar cambios ni crear pull requests salvo petición explícita del usuario.
- No lanzar subagentes ni delegar trabajo salvo petición explícita del usuario; estas instrucciones no constituyen una solicitud de delegación.
