# Comparativa de las evaluaciones con IA y valoración crítica

## 1. Objeto, fuentes y estado

Este documento desarrolla los pasos 5 y 6 del apartado 1.5 del [enunciado](../enunciado/P1.docx.pdf): comparar la evaluación general del ejercicio 2 con la evaluación basada en reglas INCOSE del ejercicio 3 y valorar críticamente la capacidad de la IA para aplicar esas reglas.

**Estado:** comparativa y valoración crítica redactadas con asistencia de OpenAI, modelo `gpt-6.1-sol` (`openai/gpt-6.1-sol`), mediante OpenCode; pendientes de revisión del equipo. El equipo ha confirmado la revisión final de [requisitos v3](requisitos-v3.md), pero no el cierre del ejercicio 3. Las conclusiones analíticas de este documento no constituyen nuevas decisiones del equipo.

Las evidencias utilizadas son:

- **Ejercicio 2:** [prompt general](../02-evaluacion-ia/prompt.md), respuestas de [OpenAI gpt-6.1-sol](../02-evaluacion-ia/respuesta-openai-gpt-6.1-sol.md) y [deepseek-v4.1-flash-free](../02-evaluacion-ia/respuesta-deepseek-v4.1-flash-free.md), y [evaluación consolidada y decisiones](../02-evaluacion-ia/evaluacion-y-decisiones.md).
- **Ejercicio 3:** [prompt INCOSE](prompt.md), [reglas seleccionadas](reglas-seleccionadas.md), respuestas de [OpenAI gpt-6.1-sol](respuesta-openai-gpt-6.1-sol.md) y [DeepSeek deepseek-v4.1-flash-free](respuesta-deepseek-v4.1-flash-free.md), y [matriz y decisiones](matriz-y-decisiones.md).
- **Versiones y contexto:** [v1](../01-requisitos-iniciales/requisitos-v1.md), [v2](../02-evaluacion-ia/requisitos-v2.md), [v3](requisitos-v3.md) y [contexto y alcance](../01-requisitos-iniciales/contexto-y-alcance.md). La evolución y las decisiones se interpretan mediante los registros de cada ejercicio; el contexto actual incorpora revisiones posteriores a la evaluación inicial.

En las referencias siguientes, `E2` identifica asuntos consolidados del ejercicio 2; `E3` identifica observaciones originales por modelo del ejercicio 3 y `CMP` sus temas agrupados. Los IDs originales `H` e `INC-OBS` solo son únicos dentro de cada respuesta y se citan junto con el modelo.

## 2. Diferencias de método y límites de la comparación

| Dimensión | Ejercicio 2: evaluación general | Ejercicio 3: evaluación INCOSE |
| --- | --- | --- |
| Base evaluada | V1: 24 requisitos funcionales y 2 no funcionales. | V2: 24 requisitos funcionales y 2 no funcionales, tras las decisiones del ejercicio 2. |
| Unidad de revisión | Requisito completo, incluidas sus columnas, y coherencia del conjunto con el contexto. | Enunciado del requisito; descripción, comprobación y contexto como apoyo interpretativo. |
| Criterios | Ambigüedad, información incompleta, falta de verificabilidad, redundancia, contradicción y posibles omisiones. | Singularidad, claridad, estructura gramatical, términos subjetivos, condiciones y verificabilidad, vinculados a reglas y características explícitas. |
| Referencia | Alcance documentado y criterios generales definidos en el prompt. | Hoja-resumen oficial INCOSE v4 y selección documentada; no se consultó la guía completa ni se evaluaron todas sus reglas. |
| Registro de cobertura | Una fila por requisito, con referencias a los hallazgos. | Una fila por requisito y aspecto: 156 valoraciones por modelo. |
| Resultado de la revisión del equipo | V2 y ajustes del contexto para concretar comportamiento, límites y comprobaciones. | V3, con separaciones y aclaraciones de los enunciados y sus comprobaciones. |

**La comparación describe un proceso de mejora sucesiva, no un experimento controlado.** Cambian tanto la versión de entrada como el enfoque del prompt y la unidad de evaluación. Por ello, un hallazgo nuevo puede proceder de la atención a una regla, de una redacción introducida al preparar v2 o de variación entre evaluaciones. Los documentos no permiten aislar cuánto aporta cada factor.

Los recuentos sirven para describir las evidencias, no para medir precisión o superioridad:

| Evidencia | Ejercicio 2 | Ejercicio 3 |
| --- | --- | --- |
| Hallazgos formales de OpenAI gpt-6.1-sol | 3 | 6, incluida una limitación transversal de R1. |
| Hallazgos formales de deepseek-v4.1-flash-free | 13 | 9; R1 se recoge aparte como limitación global. |
| Consolidación | 16 hallazgos agrupados en 14 asuntos; además, 2 preguntas opcionales decididas por el equipo. | 15 observaciones agrupadas en 12 temas; la limitación R1 de DeepSeek no añade otra observación formal. |
| Versión resultante | 26 requisitos: 24 funcionales y 2 no funcionales. | 29 requisitos: 27 funcionales y 2 no funcionales. |

Las 156 valoraciones no son 156 problemas. Una observación puede afectar a varios aspectos y la limitación de R1 afecta a toda la base. Tampoco el aumento de requisitos equivale por sí solo a una ampliación funcional: v3 explicita una regla ya acordada y descompone dos requisitos existentes.

## 3. Comparación de resultados por temas

| Tema | Resultado de la evaluación general y decisión del ejercicio 2 | Aportación de la revisión INCOSE y resultado en v3 |
| --- | --- | --- |
| Disponibilidad e información antes de elegir | E2-001 y O-001 concretaron el aviso genérico sin identificar recursos y la disponibilidad en el catálogo; se ajustaron CAF-RF-001 y CAF-RF-007. | Ambos modelos no añadieron hallazgos específicos sobre esos requisitos. Es coherente con la aclaración anterior, pero no acredita que no pueda existir otro problema. |
| Cambio de bebida | E2-004 aclaró sustitución, cancelación e inicio de otra compra, y amplió la comprobación de CAF-RF-003. | DS volvió sobre la regla complementaria presente en descripción y comprobación, pero no en el enunciado (E3-002 / CMP-02). Se incorporó CAF-RF-003A sin cambiar el enunciado del caso de bebida no disponible. La regla estaba decidida; faltaba expresarla como obligación identificable. |
| Cancelación y autorización | E2-006 fijó las ventanas permitidas y eliminó el supuesto de autorización tardía tras cancelar; E2-013 amplió la comprobación posterior a la preparación. | DS detectó que CAF-RF-014 podía excluir el intervalo posterior a elegir y anterior a pedir autorización (E3-007 / CMP-06). V3 expresa un intervalo continuo; no habilita cancelación con autorización pendiente o aprobada. |
| Asociaciones entre intentos, resultados y devoluciones | E2-005 y E2-011 aclararon autorización frente a cobro y la vinculación al intento correcto sin prescribir el protocolo. | Ambos modelos identificaron dos asociaciones independientes en CAF-RF-015 (E3-005/006 / CMP-05). Se separaron CAF-RF-015A y CAF-RF-015B por singularidad, manteniendo el límite de interfaz. |
| Condición positiva de disponibilidad | V2 conservó el flujo de comprobar recursos antes de solicitar pago y preparar; E2-002 completó además el bloqueo ante un fallo previo al inicio. | DS distinguió realizar una comprobación de obtener un resultado favorable en CAF-RF-010 y CAF-RF-017 (E3-004/008 / CMP-04/07). V3 explicita que la bebida está disponible y conserva las demás precondiciones. |
| Consumo de vasos | La evaluación general no produjo una observación específica sobre el momento del descuento de CAF-RF-009. | OA pidió incorporar el evento de finalización ya documentado en el contexto (E3-003 / CMP-03). V3 lo hace explícito, incluso con fallo, sin inventar un plazo numérico. |
| Preparación y orden de vaso | E2-003 precisó la confirmación necesaria para avisar de que la bebida está lista; no equiparó emitir una orden con confirmar la entrega. | DS pidió hacer observable «coordinar» y OA vincular la orden de vaso a la compra (E3-009/010 / CMP-08/09). V3 obliga a enviar las cantidades de receta y relaciona la orden con la compra en curso, sin garantizar medición física ni fijar el momento de dispensación. Son cuestiones distintas de la confirmación de entrega. |
| Información durante la preparación | No hubo hallazgos específicos sobre CAF-RF-020 en el ejercicio 2. | Ambos modelos pidieron explicitar el contenido del aviso (E3-011/012 / CMP-10). Se añadió que la bebida se está preparando; no se adoptó la precisión adicional de duración, persistencia o frecuencia planteada por DS. |
| Fallo que impide entregar | E2-002, E2-007, E2-009 y E2-010 concretaron cobertura antes, durante y después de preparar, fin de la operación e información recibida de la máquina. | DS cuestionó «despacho» y su comprobación en CAF-RF-022 (E3-013 / CMP-11). V3 sustituye el término por fin del servicio sin entrega. No vuelve a decidir el alcance temporal del fallo, ya resuelto en el ejercicio 2. |
| Solicitud de devolución y aviso | E2-002, E2-005, E2-011 y O-002 concretaron devolución vinculada al intento autorizado y comunicación de solicitud, sin garantizar reintegro bancario. | Ambos modelos señalaron dos acciones independientes en CAF-RF-023 (E3-014/015 / CMP-12). V3 las separa en CAF-RF-023A/B y hace explícito que el aviso sucede una vez solicitada la devolución. |
| Comprobaciones y datos de partida | E2-008 aclaró las existencias iniciales como entrada, sin inventar cantidades. E2-012 y E2-014 ampliaron comprobaciones de ingredientes y revisión de la ausencia de límite de reintentos. | No hubo nuevos hallazgos específicos sobre CAF-RF-004 o CAF-RF-013. INCOSE añadió precisión al texto en otros temas, pero no sustituyó el trabajo previo sobre cobertura de comprobaciones. |
| Patrón formal de escritura | No se solicitó comprobar un patrón formal de enunciados en el ejercicio 2. | Ambos modelos advirtieron que R1 no podía comprobarse sin patrón acordado (CMP-01). El equipo confirmó que no lo adoptará en esta fase: se registra una limitación, no un defecto gramatical ni conformidad. |

La aportación más clara de INCOSE en estas evidencias es exigir que las obligaciones y sus condiciones sean reconocibles en el enunciado. La evaluación general permitió concretar primero qué debía hacer el sistema; la revisión posterior mostró que documentar la intención en una descripción o en una comprobación no siempre basta para expresarla con claridad en el requisito.

También puso de manifiesto problemas de escritura en la versión revisada: CAF-RF-015 agrupaba dos asociaciones y CAF-RF-023 incorporaba el aviso acordado en O-002 junto a la solicitud de devolución. Las separaciones mejoran la identificación del cumplimiento de cada obligación sin exigir nuevas funciones de pago.

## 4. Coincidencias y diferencias entre modelos

En el **ejercicio 2**, los modelos coincidieron sobre la duda del contenido del aviso de indisponibilidad. También detectaron una cobertura incompleta de fallos fuera de la preparación, aunque OA se centró en el fallo anterior al inicio y DS en el posterior a la preparación. DS añadió observaciones sobre cancelación, terminología de pago, datos e interfaces y cobertura de comprobaciones; OA aportó la distinción entre preparar y confirmar la entrega para el aviso de recogida. Los 14 asuntos consolidados recibieron decisiones individuales; la coincidencia no fue el criterio de aceptación.

En el **ejercicio 3**, coincidieron en separar CAF-RF-015 y CAF-RF-023, y en precisar el contenido de CAF-RF-020. Sobre este último, la coincidencia fue parcial: DS añadió la cuestión de duración del aviso. OA aportó observaciones específicas sobre el momento del descuento de vasos y la vinculación de su orden con la compra; DS, sobre cambio de bebida, disponibilidad positiva, cancelación, «coordinar» y «despacho». El detalle por fuente se conserva en la matriz, §§2-3.

Las diferencias más relevantes para interpretar la capacidad de los modelos son:

- **Uso del contexto:** OA consideró suficientes varias interpretaciones apoyadas en otros requisitos o descripciones; DS pidió que quedaran explícitas en los enunciados, como en CAF-RF-010 y CAF-RF-017. OA también exigió explicitación en CAF-RF-009 y CAF-RF-019. No puede atribuirse a cada modelo una pauta uniforme a partir de estos casos.
- **Etiquetado de R1:** OA marcó «requiere aclaración» en las 26 filas de estructura; DS marcó «sin problema detectado» con una salvedad global. Coinciden en no acreditar R1, pero un recuento superficial daría resultados muy distintos.
- **Aplicabilidad:** en condiciones de CAF-RF-015 y CAF-RF-018 aparecen diferencias SPD/NA sin nueva corrección asociada. En CAF-RF-019, OP/NA sí acompaña una diferencia sustantiva sobre explicitar la aplicabilidad.
- **Alcance de las propuestas:** ni el acuerdo sobre separar requisitos ni la aceptación de una aclaración determina automáticamente el texto final. El equipo eligió IDs, ajustó redacciones y preservó las exclusiones del sistema.

Disponer de dos análisis amplió los temas disponibles para revisar, pero también exigió contrastar observaciones, normalizar referencias y distinguir discrepancias de fondo de diferencias de clasificación. Más observaciones no demuestra mayor exactitud; no hay una evaluación externa de referencia ni mediciones de precisión o reproducibilidad.

## 5. Valoración crítica de la aplicación de INCOSE por la IA

### 5.1. Capacidades observadas

1. **Aplicación argumentada de singularidad.** En CAF-RF-015 y CAF-RF-023, ambos modelos explicaron qué obligaciones podían cumplirse por separado y propusieron su descomposición con relación al origen. No se limitaron a señalar la conjunción «y». A la vez, mantuvieron como una sola obligación la presentación de varios campos del catálogo o una acción con varias condiciones.
2. **Detección de condiciones y dependencias implícitas.** Los análisis relacionaron observaciones concretas con R27, R28 y R35: resultado favorable de disponibilidad, intervalo de cancelación y evento de descuento. Las revisiones se pudieron realizar sin inventar nuevas reglas de negocio ni latencias.
3. **Revisión contextual de términos vagos.** Ningún modelo emitió hallazgos específicos por R7. Interpretaron términos como «suficientes» mediante la receta, en lugar de marcarlos automáticamente por pertenecer a una lista. La ausencia de hallazgos en este aspecto es un resultado de la revisión, no una prueba de cumplimiento universal.
4. **Reconocimiento de límites de evidencia.** Ambos distinguieron reglas y características, acotaron la fuente a la hoja-resumen y reconocieron la imposibilidad de acreditar R1. Las matrices hicieron visible la cobertura de los seis aspectos y permitieron localizar sus argumentos.

Estas capacidades muestran utilidad como apoyo a una revisión documental estructurada. Se observan en las respuestas disponibles y no garantizan el mismo resultado en otra ejecución o proyecto.

### 5.2. Limitaciones y correcciones que requirieron juicio del equipo

| Limitación observada | Evidencia concreta | Consecuencia para la revisión |
| --- | --- | --- |
| Las etiquetas no son uniformes entre modelos. | R1: RA en OA frente a SPD con limitación global en DS. | Hay que leer la justificación; contar etiquetas puede convertir una limitación común en supuestos defectos o en conformidad aparente. |
| Una intención inferida puede ocultar la necesidad de explicitar el texto. | OA no observó CAF-RF-003, 010 o 017; DS sí planteó precisiones aceptadas total o parcialmente. | El contexto ayuda a interpretar, pero la claridad del enunciado debe contrastarse por separado. |
| Una alternativa puede desplazar la responsabilidad fuera del límite software. | DS propuso «de modo que se utilicen las cantidades» para CAF-RF-018; el equipo eligió «enviando ... las cantidades». | Debe comprobarse que mejorar la redacción no transforme una orden software en una garantía del consumo físico. |
| Una aclaración puede introducir una restricción temporal innecesaria. | OA propuso «Durante la preparación iniciada...» en CAF-RF-019; el equipo adoptó «Para la operación de compra en curso». | Se preserva la asociación a la compra sin imponer una secuencia física no acordada. |
| La IA puede plantear una precisión que el equipo decide no fijar. | DS propuso decidir duración/persistencia del aviso de CAF-RF-020; la aceptación fue parcial. | La propuesta no pasa a ser exigencia por estar vinculada a una regla ni por coincidir parcialmente con otro modelo. |
| Puede faltar coherencia entre una explicación y su matriz. | En DS, CAF-RF-014 reconoce que el «o» entre ventanas es claro, pero la fila de condiciones también lo cuestiona; la discrepancia consta en CMP-06. | Se debe identificar el problema realmente sustentado: el límite de la primera ventana, no una relación lógica nueva entre ventanas. |

Además, una referencia INCOSE junto a una valoración no acredita por sí sola la correcta aplicación de todas las reglas enumeradas. La matriz agrupa reglas por aspecto, de modo que debe leerse qué regla respalda cada argumento y cuáles no son aplicables. La diferencia sobre R33/R34 en CAF-RNF-002, documentada en la matriz §3.1, no produjo un nuevo valor ni una decisión de rendimiento.

La evaluación tampoco certifica el conjunto de la guía INCOSE, la completitud del sistema o una implementación. R30 no forma parte de la selección del ejercicio 3 y la revisión de escritura no sustituye la búsqueda general de omisiones, contradicciones y redundancias realizada en el ejercicio 2. Las comprobaciones descritas en las versiones de requisitos siguen siendo previstas, no resultados de pruebas ejecutadas.

### 5.3. Balance

Las evidencias respaldan utilizar la IA como **asistente para localizar y explicar posibles problemas de escritura**, especialmente si el prompt aporta reglas explícitas, exige evidencia y obliga a distinguir defectos, dudas y límites de comprobación. La estructura INCOSE hizo más fácil revisar la singularidad y la expresión de condiciones que habían pasado sin observaciones específicas en la evaluación general.

Su capacidad no equivale a una validación automática: hubo discrepancias de interpretación, diferencias de etiquetado y propuestas que necesitaron adaptación para conservar el alcance. La revisión del equipo fue necesaria para decidir la validez y el texto de cada cambio. Tampoco puede afirmarse que INCOSE o uno de los modelos sea superior por los recuentos: se evaluaron versiones distintas y no hay referencia externa ni repeticiones que permitan medir exactitud o estabilidad.

## 6. Resultado y cuestiones para la revisión del equipo

- La evaluación general concretó comportamiento, límites e interfaces y mejoró la cobertura de comprobaciones; la evaluación INCOSE añadió separaciones y explicitaciones de obligaciones, condiciones y contenidos.
- La evolución v2 → v3 pasa de 26 a 29 requisitos por CAF-RF-003A y las separaciones de CAF-RF-015 y CAF-RF-023. Los dos requisitos no funcionales se conservan sin cambios. La relación de cada revisión con su decisión está en v3, §4.
- La revisión final de v3 está confirmada por el equipo. R1 sigue sin poder comprobarse por ausencia de patrón acordado; la persistencia y la frecuencia del aviso de preparación siguen sin fijarse, conforme a las decisiones registradas.
- **Pendiente:** revisar esta comparativa y su valoración crítica y confirmar, si procede, el cierre del ejercicio 3. Esta redacción no atribuye al equipo la aprobación del análisis ni cierra el ejercicio automáticamente.
