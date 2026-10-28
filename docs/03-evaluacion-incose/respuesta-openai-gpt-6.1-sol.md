# Evaluación independiente INCOSE de los requisitos v2

## 1. Identidad, entradas y alcance

**Proveedor: OpenAI. Modelo: `gpt-6.1-sol`.** La identidad está confirmada por las instrucciones del entorno de esta ejecución. No se conoce una revisión adicional a ese identificador.

Se han leído íntegramente las siguientes entradas, disponibles y legibles:

- `AGENTS.md` y `README.md`.
- `docs/enunciado/P1.docx.pdf` (3 páginas), especialmente el apartado 1.5 de la página 2.
- `docs/03-evaluacion-incose/reglas-seleccionadas.md`.
- `docs/03-evaluacion-incose/incose_rwg_gtwr_v4_summary_sheet.pdf` (7 páginas): características de la página 2, reglas de la página 3 y matriz de correspondencia de la página 4.
- `docs/02-evaluacion-ia/requisitos-v2.md`: introducción, 24 requisitos funcionales y 2 no funcionales, con sus descripciones y comprobaciones previstas.
- `docs/01-requisitos-iniciales/contexto-y-alcance.md`: alcance, glosario, catálogo, recetas, supuestos y decisiones documentadas.

La única fuente normativa INCOSE utilizada es **INCOSE Guide to Writing Requirements v4 – Summary Sheet, INCOSE-TP-2010-006-04, junio de 2023**, junto con la selección y los criterios contextuales de `reglas-seleccionadas.md`. No se ha consultado la guía completa. La matriz de la página 4 orienta las relaciones entre características y reglas; no amplía la selección.

La base es v2, procedente del ejercicio 2 cerrado por el equipo. Se evalúa el **enunciado** de cada requisito; descripción, comprobación y contexto se utilizan para interpretarlo, sin convertir ejemplos de prueba en obligaciones ni resultados ejecutados. Esta revisión se ha realizado sin consultar respuestas de otros modelos ni la evidencia previa `respuesta-ia.md`.

El apartado 1.5 pide revisar la escritura, separar funcionalidades cuando corresponda y realizar posteriormente comparación y valoración crítica. Este documento aporta el análisis individual y la matriz de esta evaluación. Las propuestas no son decisiones del equipo, no alteran v2 y no declaran terminado el ejercicio.

## 2. Método y referencias

### 2.1. Aspectos y referencias exactas

Los códigos siguientes se usan en la matriz para mantenerla legible. **C identifica características; R identifica reglas.** Las páginas son las numeradas en la hoja-resumen.

| Aspecto | Referencias utilizadas |
| --- | --- |
| Singularidad (S) | C5 — Singular (p. 2); R18 — Single Thought Sentence y R19 — Combinators (p. 3). |
| Claridad (CL) | C3 — Unambiguous (p. 2); R4 — Defined Terms, R8 — Escape Clauses y R24 — Pronouns (p. 3). |
| Estructura gramatical (G) | R1 — Structured Statements y R12 — Correct Grammar; apoyo de R2 — Active Voice y R3 — Appropriate Subject-Verb (p. 3). |
| Términos subjetivos (T) | R7 — Vague Terms (p. 3). |
| Condiciones de aplicación (A) | R27 — Explicit Conditions y R28 — Multiple Conditions; apoyo de R11 — Separate Clauses (p. 3). |
| Verificabilidad (V) | C7 — Verifiable (p. 2); cuando corresponda R33 — Range of Values, R34 — Measurable Performance y R35 — Temporal Dependencies (p. 3). |

### 2.2. Valoraciones de esta evaluación

- **Sin problema detectado (SPD):** el análisis no identifica un defecto concreto en ese aspecto; no equivale a aprobación ni certificación.
- **Observación propuesta (OP):** se identifica un problema de escritura sustentado y se propone una corrección para revisión.
- **Requiere aclaración (RA):** la documentación no permite resolver una cuestión necesaria para valorar o concretar el texto.
- **No aplica (NA):** no existe el objeto al que se aplicaría una regla o condición particular; se justifica en la fila.

Estas etiquetas no son categorías oficiales de INCOSE. En filas con varias reglas, la justificación delimita qué se puede valorar. En particular, todas las filas G tienen RA exclusivamente por la limitación común de R1; no se atribuyen 26 defectos gramaticales.

R4 exige definir los términos en glosario o diccionario asociado. Se han considerado tanto la tabla de términos como las definiciones operativas del contexto y las descripciones. No se certifica un diccionario exhaustivo de todas las palabras del lenguaje natural; se buscan carencias terminológicas que afecten realmente a la interpretación. No se han detectado cláusulas de escape vagas ni referencias pronominales que motiven observaciones independientes bajo R8 o R24.

R19 recomienda evitar combinadores; aquí se examina qué combinan, conforme al criterio seleccionado. Una lista de campos, una condición compuesta o una calificación de la misma obligación no se trata automáticamente como varias funcionalidades. R7 tampoco se aplica como búsqueda mecánica de palabras: «suficientes» queda determinado por receta y vasos, y «cualquier etapa» delimita todas las etapas posteriores a la autorización, sin cuantificación vaga.

En verificabilidad, las comprobaciones mencionadas son posibilidades de verificación documental o de comportamiento, **no pruebas realizadas**. No se exigen tiempos máximos ni tolerancias físicas fuera del alcance: los consumos son datos comunicados por los mecanismos. R34 no resulta aplicable a ninguno de estos enunciados como exigencia de rendimiento cuantitativo. Las dependencias entre eventos sí se revisan con R35 cuando existen; «antes» o «después» no constituyen por sí solos un defecto si los eventos y su orden están definidos.

## 3. Observaciones, en el orden de la base

Los IDs son estables dentro de esta respuesta y deben citarse junto con el proveedor/modelo en la revisión posterior. Los IDs con sufijos `-A` y `-B` son provisionales y conservan como origen el requisito indicado.

### INC-OBS-001 — Patrón acordado no disponible para comprobar R1

- **Requisito:** CAF-RF-001; observación transversal aplicable también al resto de los 26 requisitos.
- **Fragmento de entrada:** «El sistema deberá mostrar…». En el conjunto predomina «El sistema deberá…» y CAF-RNF-001 utiliza «Los textos de la interfaz… deberán estar…».
- **Aspecto y fuente:** estructura gramatical; **R1 — Structured Statements (p. 3)**. R12 — Correct Grammar, R2 — Active Voice y R3 — Appropriate Subject-Verb (p. 3) permiten examinar por separado la construcción lingüística.
- **Valoración:** **requiere aclaración**. Es una limitación de comprobación, no un defecto demostrado de los enunciados. `reglas-seleccionadas.md` declara que no hay un patrón formal documentado. La regularidad de las frases no demuestra acuerdo sobre un patrón, y tampoco prueba que el sujeto de CAF-RNF-001 sea incorrecto.
- **Efecto:** no se puede afirmar conformidad con la parte de R1 que exige uno de los patrones acordados. Sí se observan frases completas, sujetos identificables y predicados adecuados en la base.
- **Solución propuesta:** que el equipo indique si ya existe un patrón aprobado y dónde está documentado o, en la fase posterior, acuerde uno adecuado para acciones y propiedades. No se introduce una plantilla obligatoria por iniciativa de la IA.
- **Redacción alternativa:** pendiente de conocer el patrón. Mientras no se aclare, se propone conservar los enunciados en este punto; por ejemplo, CAF-RF-001 conserva «El sistema deberá mostrar el nombre, el precio y la disponibilidad de cada bebida del catálogo antes de que el cliente la seleccione».
- **Pendiente del equipo:** aportar o acordar el patrón y decidir si hace falta adaptar algún enunciado. Esta observación se referencia una sola vez, aunque aparezca en todas las filas G.

### INC-OBS-002 — Momento del descuento de vasos no explícito

- **Requisito:** CAF-RF-009.
- **Fragmento:** «descontar de las existencias los vasos realmente consumidos durante una preparación».
- **Aspectos y fuente:** condiciones de aplicación y verificabilidad; **R27 — Explicit Conditions (p. 3), C7 — Verifiable (p. 2) y R35 — Temporal Dependencies (p. 3)**.
- **Valoración:** **observación propuesta**. «Durante una preparación» caracteriza el consumo, pero no fija inequívocamente el momento del descuento. La descripción aclara la fuente de la cantidad y el caso de consumo cero, no ese momento. El contexto, apartado 3, ya establece actualizar las existencias al finalizar la preparación, incluso si falla.
- **Efecto:** el enunciado aislado permite interpretar descuento a medida que se consumen vasos o descuento al finalizar; la comprobación propuesta del saldo final no distingue ambas lecturas. No se necesita inventar una latencia máxima.
- **Solución propuesta:** incorporar al enunciado el evento de actualización ya documentado, manteniendo el consumo real comunicado por los mecanismos.
- **Redacción alternativa, origen CAF-RF-009:** «Al finalizar una preparación, tanto si se completa como si falla, el sistema deberá descontar de las existencias el número de vasos consumidos que comuniquen los mecanismos de la máquina».
- **Pendiente del equipo:** revisar la incorporación del momento ya indicado en el contexto; no se propone cambiar la política de consumo.

### INC-OBS-003 — Dos asociaciones comprobables de forma independiente

- **Requisito:** CAF-RF-015, situado antes de CAF-RF-014 en la base.
- **Fragmento:** «asociar cada resultado de autorización con el intento de pago correspondiente y permitir vincular una solicitud de devolución con el intento autorizado que la origina».
- **Aspecto y fuente:** singularidad; **C5 — Singular (p. 2), R18 — Single Thought Sentence y R19 — Combinators (p. 3)**.
- **Valoración:** **observación propuesta**. El problema no es la mera presencia de «y»: hay dos relaciones distintas, resultado–intento y devolución–intento autorizado. Se puede realizar correctamente una y no la otra. La segunda no es una condición o un dato de la primera, aunque compartan la finalidad de correlación.
- **Efecto:** un único estado de cumplimiento oculta cuál de las dos asociaciones está satisfecha.
- **Solución propuesta:** separar las dos obligaciones y conservar la libertad de distribución de la referencia entre aplicación y terminal.
- **Redacciones alternativas:**
  - **CAF-RF-015-A**, origen CAF-RF-015: «El sistema deberá asociar cada resultado de autorización recibido del terminal con el intento de pago correspondiente».
  - **CAF-RF-015-B**, origen CAF-RF-015: «El sistema deberá permitir vincular cada solicitud de devolución con el intento de pago autorizado que la origina».
- **Pendiente del equipo:** aceptar o rechazar la separación y asignar IDs definitivos posteriormente. No se propone un protocolo ni un almacén de referencias.

### INC-OBS-004 — Aplicabilidad de la orden de vaso implícita

- **Requisito:** CAF-RF-019.
- **Fragmento:** «ordenar la dispensación de un vaso para entregar la bebida preparada».
- **Aspecto y fuente:** condiciones de aplicación; **R27 — Explicit Conditions (p. 3)**.
- **Valoración:** **observación propuesta**. La frase expresa una finalidad, pero no explicita que la orden pertenece a la preparación iniciada para la operación de compra. Esa condición se reconstruye a partir del módulo y del flujo documentado. No se concluye que el vaso tenga que dispensarse después de preparar el líquido: el texto no acuerda ese orden físico.
- **Efecto:** queda implícito cuándo es aplicable la obligación; resulta menos directo delimitar las operaciones que deben generar la orden.
- **Solución propuesta:** hacer explícita la pertenencia a la preparación en curso, sin imponer un punto de la secuencia física ni nuevas condiciones de negocio.
- **Redacción alternativa, origen CAF-RF-019:** «Durante la preparación iniciada para la operación de compra, el sistema deberá ordenar la dispensación de un vaso destinado a la entrega de la bebida seleccionada».
- **Pendiente del equipo:** revisar que esta explicitación preserva el alcance. El punto físico de dispensación no se fija en esta propuesta y no se reclama como una nueva decisión necesaria para evaluar este requisito.

### INC-OBS-005 — Contenido de la información durante la preparación

- **Requisito:** CAF-RF-020.
- **Fragmento:** «informar al cliente mientras la bebida se esté preparando».
- **Aspectos y fuente:** claridad y verificabilidad; **C3 — Unambiguous (p. 2) y C7 — Verifiable (p. 2)**.
- **Valoración:** **observación propuesta**. El enunciado indica destinatario y periodo, pero no qué debe comunicarse. La descripción busca distinguir preparación y espera de pago; la comprobación propone un mensaje de preparación en curso. Ese contenido no debe quedar obligado únicamente por un ejemplo de comprobación.
- **Efecto:** bajo una lectura literal, cualquier información mostrada durante ese periodo podría satisfacer la frase, aunque no comunique que la bebida se está preparando.
- **Solución propuesta:** expresar el contenido informativo que ya sustenta la descripción, sin introducir porcentaje de progreso, frecuencia de actualización o texto literal de interfaz.
- **Redacción alternativa, origen CAF-RF-020:** «Mientras la bebida se esté preparando, el sistema deberá informar al cliente de que la preparación está en curso».
- **Pendiente del equipo:** revisar la explicitación. No se exige un tiempo numérico ni un indicador adicional. No se etiqueta como infracción de R7: la carencia es el objeto de la información, no un adjetivo o cuantificador vago.

### INC-OBS-006 — Solicitar devolución y comunicar su solicitud son dos acciones

- **Requisito:** CAF-RF-023.
- **Fragmento:** «solicitar la devolución íntegra del importe asociado al intento autorizado y comunicar al cliente que la devolución fue solicitada».
- **Aspecto y fuente:** singularidad; **C5 — Singular (p. 2), R18 — Single Thought Sentence y R19 — Combinators (p. 3)**.
- **Valoración:** **observación propuesta**. Solicitar una devolución al sistema externo y avisar al cliente son obligaciones con destinatarios y evidencias distintos. La aplicación podría emitir una solicitud sin mostrar el aviso, o mostrar el aviso sin emitirla. Compartir condición no las convierte en una única acción.
- **Efecto:** el cumplimiento parcial queda agrupado bajo un solo ID. La secuencia «fue solicitada» sí expresa que el aviso debe referirse a una solicitud efectuada; no se detecta por ello otro problema temporal independiente.
- **Solución propuesta:** separar ambas acciones conservando la asociación al intento autorizado, el importe íntegro, la condición de fallo y la secuencia del aviso. No extender el requisito al éxito bancario ni a fallos de la solicitud de devolución, excluidos por el equipo.
- **Redacciones alternativas:**
  - **CAF-RF-023-A**, origen CAF-RF-023: «Si, tras autorizarse el pago, un fallo impide entregar la bebida, el sistema deberá solicitar la devolución íntegra del importe asociado al intento de pago autorizado».
  - **CAF-RF-023-B**, origen CAF-RF-023: «Cuando el sistema haya solicitado la devolución prevista en CAF-RF-023-A por un fallo que impide entregar la bebida, el sistema deberá comunicar al cliente que la devolución fue solicitada».
- **Pendiente del equipo:** decidir la separación y los IDs definitivos, manteniendo las exclusiones actuales.

## 4. Matriz completa de evaluación de v2

Se presentan **156 filas: 26 requisitos × 6 aspectos**, en el orden del documento, incluido CAF-RF-015 antes de CAF-RF-014. Los códigos de aspecto, los títulos y las páginas se desarrollan en §2.1. «—» en la última columna significa que no se genera observación en ese aspecto. Las valoraciones corresponden al texto original v2, no a las alternativas propuestas.

### Selección

| ID | Aspecto | C/R aplicables | Valoración | Justificación | Observaciones |
| --- | --- | --- | --- | --- | --- |
| CAF-RF-001 | S | C5; R18, R19 | SPD | Mostrar tres campos de cada bebida es una sola presentación de catálogo, no tres funcionalidades independientes. | — |
| CAF-RF-001 | CL | C3; R4, R8, R24 | SPD | Catálogo y disponibilidad están definidos; «la» remite inequívocamente a cada bebida seleccionable. Sin escape vago. | — |
| CAF-RF-001 | G | R1, R12; R2, R3 | RA | Frase completa con sistema como sujeto y mostrar como acción; falta patrón acordado para R1. | INC-OBS-001 |
| CAF-RF-001 | T | R7 | SPD | Nombre, precio y disponibilidad son campos concretos; cada bebida delimita el conjunto. | — |
| CAF-RF-001 | A | R27; R11 | SPD | La presentación debe preceder a la selección por el cliente; R28 no requiere una combinación adicional. | — |
| CAF-RF-001 | V | C7; R35 | SPD | Se inspeccionan campos y estados antes del evento de selección. R33/R34 no requieren tolerancia ni rendimiento aquí. | — |
| CAF-RF-002 | S | C5; R18, R19 | SPD | Una única capacidad de selección con límite de una bebida por compra. | — |
| CAF-RF-002 | CL | C3; R4, R8, R24 | SPD | Bebida disponible, catálogo y operación se interpretan con el alcance de una bebida por compra; sin escape ni referente dudoso. | — |
| CAF-RF-002 | G | R1, R12; R2, R3 | RA | Sujeto y predicado completos y adecuados; R1 pendiente de patrón acordado. | INC-OBS-001 |
| CAF-RF-002 | T | R7 | SPD | «Una bebida» es el límite concreto de selección, no una cuantificación vaga. | — |
| CAF-RF-002 | A | R27; R11 | SPD | Disponibilidad y pertenencia al catálogo califican explícitamente la bebida seleccionable en una compra. | — |
| CAF-RF-002 | V | C7; R33 | SPD | Se comprueba asociación de una sola bebida disponible a la compra; límite cardinal exacto, sin tolerancia física. R34/R35 no pertinentes. | — |
| CAF-RF-003 | S | C5; R18, R19 | SPD | Seleccionar otra bebida sin cancelar es una capacidad calificada por la indisponibilidad, no dos acciones exigidas. | — |
| CAF-RF-003 | CL | C3; R4, R8, R24 | SPD | «Otra bebida» significa sustitución según descripción y contexto; no es un pronombre de referencia incierta. | — |
| CAF-RF-003 | G | R1, R12; R2, R3 | RA | Condicional y oración principal completas, sujeto sistema; patrón de R1 no documentado. | INC-OBS-001 |
| CAF-RF-003 | T | R7 | SPD | La indisponibilidad tiene criterio de ingredientes y vasos; no hay gradación subjetiva. | — |
| CAF-RF-003 | A | R27; R11 | SPD | La falta de disponibilidad es condición explícita; la ausencia de cancelación previa califica la misma selección. | — |
| CAF-RF-003 | V | C7; R35 | SPD | Se puede comprobar sustitución directa sin evento previo de cancelación; la descripción delimita los demás cambios. Sin plazo necesario. | — |

### Existencias

| ID | Aspecto | C/R aplicables | Valoración | Justificación | Observaciones |
| --- | --- | --- | --- | --- | --- |
| CAF-RF-004 | S | C5; R18, R19 | SPD | La comprobación por ingrediente es una única comprobación de suficiencia de receta. | — |
| CAF-RF-004 | CL | C3; R4, R8, R24 | SPD | Ingrediente y receta están definidos; «alcanzan» significa existencias al menos iguales a las cantidades de receta. | — |
| CAF-RF-004 | G | R1, R12; R2, R3 | RA | El sistema comprueba una proposición completa; R1 no contrastable sin patrón aprobado. | INC-OBS-001 |
| CAF-RF-004 | T | R7 | SPD | «Alcanzan» no queda a juicio del evaluador: el umbral procede de la receta referida. | — |
| CAF-RF-004 | A | R27; R11 | SPD | Bebida seleccionada, ingredientes requeridos y comprobación anterior al pago están explícitos. | — |
| CAF-RF-004 | V | C7; R33, R35 | SPD | Se comparan cantidades con umbrales de receta, incluidos sus límites; el evento de pago delimita el orden. No se exige tolerancia física. | — |
| CAF-RF-005 | S | C5; R18, R19 | SPD | Una comprobación del número mínimo de vasos. | — |
| CAF-RF-005 | CL | C3; R4, R8, R24 | SPD | Vaso disponible se interpreta como recurso para entregar la bebida; «al menos uno» tiene sentido inequívoco. | — |
| CAF-RF-005 | G | R1, R12; R2, R3 | RA | Sujeto sistema y acción comprobar completos; falta patrón para R1. | INC-OBS-001 |
| CAF-RF-005 | T | R7 | SPD | El mínimo de un vaso es objetivo y explícito. | — |
| CAF-RF-005 | A | R27; R11 | SPD | La comprobación queda situada antes de solicitar el pago. | — |
| CAF-RF-005 | V | C7; R33, R35 | SPD | Umbral entero ≥1 comprobable con cero y uno; orden relativo al pago definido, sin latencia numérica necesaria. | — |
| CAF-RF-006 | S | C5; R18, R19 | SPD | Una inhibición de autorización bajo dos causas alternativas; no dos funcionalidades por «o». | — |
| CAF-RF-006 | CL | C3; R4, R8, R24 | SPD | La falta se determina con receta y vaso; solicitud de autorización tiene interfaz externa identificada. | — |
| CAF-RF-006 | G | R1, R12; R2, R3 | RA | Sujeto y verbo adecuados para bloquear una solicitud; R1 pendiente de patrón. | INC-OBS-001 |
| CAF-RF-006 | T | R7 | SPD | «Faltan» se determina con los recursos de la bebida, sin apreciación subjetiva. | — |
| CAF-RF-006 | A | R27, R28; R11 | SPD | Basta falta de ingredientes o de vasos; la disyunción de causas de bloqueo es explícita. | — |
| CAF-RF-006 | V | C7 | SPD | Se observa ausencia de solicitud al terminal en cada causa y en su combinación. No necesita rendimiento, rango o plazo adicional. | — |
| CAF-RF-007 | S | C5; R18, R19 | SPD | Un aviso de indisponibilidad por causas alternativas, no avisos funcionalmente distintos por cada recurso. | — |
| CAF-RF-007 | CL | C3; R4, R8, R24 | SPD | Descripción delimita un aviso de indisponibilidad sin detalle del recurso; el enunciado no contiene referentes dudosos. | — |
| CAF-RF-007 | G | R1, R12; R2, R3 | RA | Oración completa con destinatario y condición; R1 sin patrón comprobable. | INC-OBS-001 |
| CAF-RF-007 | T | R7 | SPD | No hay adjetivo vago en el enunciado; el carácter genérico de la descripción se concreta como no identificar el recurso. | — |
| CAF-RF-007 | A | R27, R28; R11 | SPD | La selección no disponible por ingredientes o vasos activa explícitamente el aviso. | — |
| CAF-RF-007 | V | C7; R35 | SPD | Se comprueba el aviso al darse cada causa; el evento está definido. No hay tiempo máximo acordado que exigir. | — |
| CAF-RF-008 | S | C5; R18, R19 | SPD | Un descuento de ingredientes, calificado para éxito y fallo; no dos obligaciones independientes por sus desenlaces. | — |
| CAF-RF-008 | CL | C3; R4, R8, R24 | SPD | Consumo real significa cantidades comunicadas por mecanismos, incluidas preparaciones parciales, según descripción y supuesto. | — |
| CAF-RF-008 | G | R1, R12; R2, R3 | RA | Sistema como sujeto, descuento como acción, subcláusulas correctas; R1 pendiente. | INC-OBS-001 |
| CAF-RF-008 | T | R7 | SPD | «Realmente consumidas» remite a un dato comunicado, no a una apreciación cualitativa. | — |
| CAF-RF-008 | A | R27, R28; R11 | SPD | Finalización de preparación, completa o fallida, explícita como ámbito de actualización. | — |
| CAF-RF-008 | V | C7; R33, R35 | SPD | Se compara descuento con consumo comunicado al finalizar. No se evalúa precisión física ni se requiere un rango fijo de consumo. | — |
| CAF-RF-009 | S | C5; R18, R19 | SPD | Una actualización del stock de vasos; el fallo califica su aplicación. | — |
| CAF-RF-009 | CL | C3; R4, R8, R24 | SPD | La descripción define cantidad comunicada y descuento cero sin consumo; no hay ambigüedad del recurso o de la fuente. | — |
| CAF-RF-009 | G | R1, R12; R2, R3 | RA | Oración completa y sujeto responsable identificado; patrón R1 no documentado. | INC-OBS-001 |
| CAF-RF-009 | T | R7 | SPD | «Realmente consumidos» se cuantifica mediante los mecanismos; no es subjetivo. | — |
| CAF-RF-009 | A | R27; R11 | OP | La preparación y el fallo están delimitados, pero el momento de aplicar el descuento queda implícito. | INC-OBS-002 |
| CAF-RF-009 | V | C7; R33, R35 | OP | La cantidad es comprobable; falta explicitar el evento de actualización que el contexto sitúa al finalizar. | INC-OBS-002 |

### Pago

| ID | Aspecto | C/R aplicables | Valoración | Justificación | Observaciones |
| --- | --- | --- | --- | --- | --- |
| CAF-RF-010 | S | C5; R18, R19 | SPD | Una solicitud al terminal, con importe y precondición. | — |
| CAF-RF-010 | CL | C3; R4, R8, R24 | SPD | Precio procede del catálogo y disponibilidad incluye ingredientes y vasos; «su» tiene referente bebida seleccionada. | — |
| CAF-RF-010 | G | R1, R12; R2, R3 | RA | Sistema solicita autorización al terminal; frase completa, pero patrón R1 pendiente. | INC-OBS-001 |
| CAF-RF-010 | T | R7 | SPD | Precio y disponibilidad tienen referencias concretas. | — |
| CAF-RF-010 | A | R27; R11 | SPD | Se explicita comprobación previa de disponibilidad; su sentido positivo se interpreta con definición y bloqueo de CAF-RF-006. | — |
| CAF-RF-010 | V | C7; R33, R35 | SPD | Importe comparado con precio exacto de catálogo y solicitud posterior a comprobación; sin rango de rendimiento necesario. | — |
| CAF-RF-011 | S | C5; R18, R19 | SPD | Una prohibición de inicio bajo dos condiciones; el «o» no introduce otra capacidad. | — |
| CAF-RF-011 | CL | C3; R4, R8, R24 | SPD | Pendiente/denegado y fallo impeditivo están delimitados; la comunicación de fallo no es una cláusula de escape. | — |
| CAF-RF-011 | G | R1, R12; R2, R3 | RA | Construcción completa con sistema responsable de impedir el inicio; R1 sin patrón. | INC-OBS-001 |
| CAF-RF-011 | T | R7 | SPD | Fallo que impide la entrega se define por su efecto comunicado; no se gradúa su gravedad subjetivamente. | — |
| CAF-RF-011 | A | R27, R28; R11 | SPD | No autorización o fallo comunicado bastan para impedir el inicio; disyunción explícita. | — |
| CAF-RF-011 | V | C7; R35 | SPD | Se verifica ausencia de inicio con autorización pendiente, denegada o fallo comunicado previo al inicio. | — |
| CAF-RF-012 | S | C5; R18, R19 | SPD | Un aviso ante denegación. | — |
| CAF-RF-012 | CL | C3; R4, R8, R24 | SPD | Denegación es un resultado del terminal; la descripción concreta que el aviso informa del pago no autorizado. | — |
| CAF-RF-012 | G | R1, R12; R2, R3 | RA | Sujeto, acción, destinatario y condicional completos; R1 pendiente de patrón. | INC-OBS-001 |
| CAF-RF-012 | T | R7 | SPD | No hay calificativos o cantidades vagos. | — |
| CAF-RF-012 | A | R27; R11 | SPD | El terminal deniega el pago como condición explícita del aviso. | — |
| CAF-RF-012 | V | C7; R35 | SPD | Un resultado de denegación permite comprobar el mensaje correspondiente; evento definido sin exigir plazo inventado. | — |
| CAF-RF-013 | S | C5; R18, R19 | SPD | Una capacidad de reintento, calificada por ausencia de límite; no dos funcionalidades. | — |
| CAF-RF-013 | CL | C3; R4, R8, R24 | SPD | Reintento refiere a la misma bebida y operación según descripción; ausencia de máximo significa no imponer un contador límite. | — |
| CAF-RF-013 | G | R1, R12; R2, R3 | RA | Frase completa con sujeto sistema y acción permitir reintento; patrón R1 no disponible. | INC-OBS-001 |
| CAF-RF-013 | T | R7 | SPD | «Después de cada denegación» y «sin… máximo» son una política explícita, no cantidad vagamente suficiente. | — |
| CAF-RF-013 | A | R27; R11 | SPD | Cada denegación habilita el reintento; no se incluye cancelación como una nueva acción exigida por esta frase. | — |
| CAF-RF-013 | V | C7; R35 | SPD | Escenarios finitos comprueban el flujo; inspección de lógica/configuración comprueba ausencia de límite. No exige ejecutar infinitos intentos. | — |
| CAF-RF-015 | S | C5; R18, R19 | OP | Asociación resultado–intento y vínculo devolución–intento autorizado son obligaciones separadamente comprobables. | INC-OBS-003 |
| CAF-RF-015 | CL | C3; R4, R8, R24 | SPD | «Correspondiente» y «que la origina» identifican relaciones explícitas; la introducción no impone quién conserva la referencia. | — |
| CAF-RF-015 | G | R1, R12; R2, R3 | RA | Predicados coordinados gramaticalmente válidos, aunque se propone separar por singularidad; patrón R1 pendiente. | INC-OBS-001 |
| CAF-RF-015 | T | R7 | SPD | «Correspondiente» expresa identidad del intento, no adecuación subjetiva. | — |
| CAF-RF-015 | A | R27; R11 | SPD | Cada resultado tiene intento; la relación de devolución se restringe expresamente al intento autorizado que la origina. | — |
| CAF-RF-015 | V | C7 | SPD | Ambas asociaciones son comprobables con intentos diferenciados, aunque convenga separarlas. No requiere métrica o plazo. | — |

### Cancelación

| ID | Aspecto | C/R aplicables | Valoración | Justificación | Observaciones |
| --- | --- | --- | --- | --- | --- |
| CAF-RF-014 | S | C5; R18, R19 | SPD | Una capacidad de cancelación con dos ventanas de aplicación. | — |
| CAF-RF-014 | CL | C3; R4, R8, R24 | SPD | Operación y solicitud de autorización se delimitan con descripción y supuestos; no hay referencias indeterminadas. | — |
| CAF-RF-014 | G | R1, R12; R2, R3 | RA | Frase completa, coordinaciones de condiciones correctas; R1 pendiente. | INC-OBS-001 |
| CAF-RF-014 | T | R7 | SPD | Las ventanas se refieren a eventos concretos, sin términos subjetivos. | — |
| CAF-RF-014 | A | R27, R28; R11 | SPD | (Selección y antes de solicitud) o (denegación recibida y antes de reintento) expresa las dos ventanas. | — |
| CAF-RF-014 | V | C7; R35 | SPD | Se acepta cancelación entre los eventos que delimitan cada ventana; no se necesita duración numérica. | — |
| CAF-RF-016 | S | C5; R18, R19 | SPD | Una prohibición de cancelación en estados alternativos. | — |
| CAF-RF-016 | CL | C3; R4, R8, R24 | SPD | Solicitud pendiente y pago autorizado son estados identificables de la operación, ampliados en descripción. | — |
| CAF-RF-016 | G | R1, R12; R2, R3 | RA | Sistema como sujeto de impedir; la subordinada identifica acción del cliente; R1 no comprobable. | INC-OBS-001 |
| CAF-RF-016 | T | R7 | SPD | No hay cuantificadores o adjetivos vagos. | — |
| CAF-RF-016 | A | R27, R28; R11 | SPD | Pendiente o autorizado son causas explícitas de rechazo de cancelación. | — |
| CAF-RF-016 | V | C7; R35 | SPD | Se comprueba rechazo antes y después de resolver la autorización positivamente, incluidas las etapas descritas. | — |

### Preparación y comunicación de incidencias

| ID | Aspecto | C/R aplicables | Valoración | Justificación | Observaciones |
| --- | --- | --- | --- | --- | --- |
| CAF-RF-017 | S | C5; R18, R19 | SPD | Un inicio de preparación sujeto a tres condiciones; sus conjunciones no son acciones independientes. | — |
| CAF-RF-017 | CL | C3; R4, R8, R24 | SPD | Disponibilidad y autorización están definidas; «siempre que» introduce condición concreta de ausencia de fallo comunicado, no escape vago. | — |
| CAF-RF-017 | G | R1, R12; R2, R3 | RA | Sistema inicia; subordinadas gramaticalmente completas por elipsis compartida; patrón R1 pendiente. | INC-OBS-001 |
| CAF-RF-017 | T | R7 | SPD | La condición de fallo se define por impedir entrega, no por gravedad indeterminada. | — |
| CAF-RF-017 | A | R27, R28; R11 | SPD | Disponibilidad comprobada y pago autorizado y ausencia de fallo comunicado son condiciones conjuntivas explícitas. | — |
| CAF-RF-017 | V | C7; R35 | SPD | Se observa inicio tras cumplir condiciones y ausencia de inicio al faltar alguna. No se inventa latencia máxima. | — |
| CAF-RF-018 | S | C5; R18, R19 | SPD | Una coordinación de preparación conforme a receta, no una obligación por ingrediente. | — |
| CAF-RF-018 | CL | C3; R4, R8, R24 | SPD | Receta remite explícitamente al contexto; coordinar se interpreta como control software de mecanismos, no fabricación ni medición física. | — |
| CAF-RF-018 | G | R1, R12; R2, R3 | RA | Sujeto sistema y verbo coordinar adecuados al software; no se acredita patrón R1. | INC-OBS-001 |
| CAF-RF-018 | T | R7 | SPD | Las cantidades no se describen como adecuadas: son las indicadas en una referencia concreta. | — |
| CAF-RF-018 | A | R27; R11 | SPD | La obligación califica la preparación de la bebida seleccionada con su receta; no introduce otro disparador distinto de CAF-RF-017. | — |
| CAF-RF-018 | V | C7; R33 | SPD | Se comparan cantidades ordenadas con recetas referidas. La precisión física queda fuera del alcance; no falta tolerancia software acordada. | — |
| CAF-RF-019 | S | C5; R18, R19 | SPD | Una orden de dispensación de un vaso; la finalidad no constituye otra acción exigida al software. | — |
| CAF-RF-019 | CL | C3; R4, R8, R24 | SPD | Vaso y bebida preparada son objetos identificables; el destinatario físico se interpreta con descripción y límite del sistema. | — |
| CAF-RF-019 | G | R1, R12; R2, R3 | RA | Sujeto sistema y acción ordenar completos y adecuados; patrón R1 pendiente. | INC-OBS-001 |
| CAF-RF-019 | T | R7 | SPD | Un vaso es cantidad precisa; no hay término subjetivo. | — |
| CAF-RF-019 | A | R27; R11 | OP | El enunciado expresa finalidad pero deja implícita su aplicación a la preparación iniciada para la compra. | INC-OBS-004 |
| CAF-RF-019 | V | C7; R33 | SPD | La emisión de una orden de un vaso es observable; no se prescribe secuencia física o rendimiento que exija cuantificación. | — |
| CAF-RF-020 | S | C5; R18, R19 | SPD | Una comunicación durante un estado; no contiene obligaciones independientes. | — |
| CAF-RF-020 | CL | C3; R4, R8, R24 | OP | Falta el contenido que debe comunicarse; la descripción orienta la intención, pero no lo hace explícito en el enunciado. | INC-OBS-005 |
| CAF-RF-020 | G | R1, R12; R2, R3 | RA | «Informar al cliente» forma una construcción gramatical válida; la falta de contenido es semántica. R1 pendiente. | INC-OBS-001 |
| CAF-RF-020 | T | R7 | SPD | No hay adjetivos o cuantificadores vagos; el problema de contenido no es una infracción léxica de R7. | — |
| CAF-RF-020 | A | R27; R11 | SPD | El estado de preparación es condición temporal explícita de la comunicación. | — |
| CAF-RF-020 | V | C7; R35 | OP | El intervalo está definido, pero no el contenido con el que decidir si la comunicación cumple el enunciado. | INC-OBS-005 |
| CAF-RF-021 | S | C5; R18, R19 | SPD | Un aviso de recogida bajo confirmación conjunta de preparación y entrega; no dos funcionalidades por la conjunción. | — |
| CAF-RF-021 | CL | C3; R4, R8, R24 | SPD | «Correctamente» remite a confirmación de preparación y entrega de la máquina, no a valoración subjetiva del software. | — |
| CAF-RF-021 | G | R1, R12; R2, R3 | RA | Sistema como sujeto del aviso y cláusulas completas; la impersonal de confirmación no oculta el responsable principal. R1 pendiente. | INC-OBS-001 |
| CAF-RF-021 | T | R7 | SPD | Lista para recoger y terminación correcta tienen criterio de resultado comunicado según supuesto, no gusto del cliente. | — |
| CAF-RF-021 | A | R27, R28; R11 | SPD | Se requiere confirmación de preparación y entrega en vaso terminadas correctamente; la conjunción es explícita. | — |
| CAF-RF-021 | V | C7; R35 | SPD | Se controla que el aviso siga a confirmación conjunta y no se emita ante fallo impeditivo; sin imponer sensor ni plazo. | — |
| CAF-RF-022 | S | C5; R18, R19 | SPD | Una comunicación de resultado sin entrega con dos datos complementarios; no se exige aquí ejecutar la terminación de la compra. | — |
| CAF-RF-022 | CL | C3; R4, R8, R24 | SPD | «Terminó el despacho sin entrega» se interpreta como fin del servicio fallido, explicado en descripción y contexto. | — |
| CAF-RF-022 | G | R1, R12; R2, R3 | RA | Condicional y acción de informar completas; dos complementos de contenido, no error gramatical. R1 pendiente. | INC-OBS-001 |
| CAF-RF-022 | T | R7 | SPD | «En cualquier etapa» abarca etapas posteriores a autorización, enumeradas en descripción; no equivale a cantidad vaga. | — |
| CAF-RF-022 | A | R27, R28; R11 | SPD | Pago autorizado y fallo que impide entregar son condiciones explícitas; se abarca antes, durante y después de preparar. | — |
| CAF-RF-022 | V | C7; R35 | SPD | Se comprueba el contenido de servicio terminado sin entrega ante fallo posterior a autorización en cada etapa. | — |
| CAF-RF-023 | S | C5; R18, R19 | OP | Solicitud externa de devolución y aviso al cliente son dos acciones con evidencia independiente. | INC-OBS-006 |
| CAF-RF-023 | CL | C3; R4, R8, R24 | SPD | «Íntegra» refiere al importe del intento autorizado; se informa de solicitud, no de reintegro bancario. | — |
| CAF-RF-023 | G | R1, R12; R2, R3 | RA | Coordinación verbal gramaticalmente válida aunque no singular; patrón R1 no documentado. | INC-OBS-001 |
| CAF-RF-023 | T | R7 | SPD | «Íntegra» define igualdad con el importe autorizado, no una aproximación subjetiva. | — |
| CAF-RF-023 | A | R27, R28; R11 | SPD | Autorización previa y fallo impeditivo explícitos; la observación de dos acciones se registra en singularidad sin duplicarla. | — |
| CAF-RF-023 | V | C7; R33, R35 | SPD | Se observa importe íntegro, asociación y aviso posterior a solicitud. No se exige verificar el éxito del procesamiento externo. | — |
| CAF-RF-024 | S | C5; R18, R19 | SPD | Terminar sin reinicio automático es una transición con una restricción sobre su resultado, no acciones nuevas que deban ejecutarse. | — |
| CAF-RF-024 | CL | C3; R4, R8, R24 | SPD | Terminar operación significa fin de compra sin entrega según contexto; no prescribe estado interno o implementación. | — |
| CAF-RF-024 | G | R1, R12; R2, R3 | RA | Sujeto sistema y acción terminar completos, cláusula negativa calificadora correcta; R1 pendiente. | INC-OBS-001 |
| CAF-RF-024 | T | R7 | SPD | «Automáticamente» distingue inicio autónomo de nueva acción del cliente, no grado subjetivo. | — |
| CAF-RF-024 | A | R27, R28; R11 | SPD | Fallo impeditivo y pago autorizado delimitan la terminación sin reinicio; no se añaden condiciones de recuperación. | — |
| CAF-RF-024 | V | C7; R35 | SPD | Se observa cierre tras fallo y ausencia de nueva orden/compra automática; no exige inventar un tiempo máximo de cierre. | — |

### Requisitos no funcionales

| ID | Aspecto | C/R aplicables | Valoración | Justificación | Observaciones |
| --- | --- | --- | --- | --- | --- |
| CAF-RNF-001 | S | C5; R18, R19 | SPD | Una propiedad de idioma de todos los textos dirigidos al cliente. | — |
| CAF-RNF-001 | CL | C3; R4, R8, R24 | SPD | La interfaz y el destinatario delimitan los textos; español es idioma identificable, sin escape o referencia dudosa. | — |
| CAF-RNF-001 | G | R1, R12; R2, R3 | RA | Sujeto textos y predicado estar en español adecuados a una propiedad; no es una pasiva de agente omitido. R1 pendiente. | INC-OBS-001 |
| CAF-RNF-001 | T | R7 | SPD | No exige español «adecuado» o «fácil» sin criterio; solo idioma determinado. | — |
| CAF-RNF-001 | A | R27 | NA | Propiedad incondicional de los textos dirigidos al cliente; no hay un disparador o combinación de estados que deba añadirse. | — |
| CAF-RNF-001 | V | C7 | SPD | La inspección de textos de pantallas y avisos comprueba el idioma. No requiere rango, rendimiento ni dependencia temporal. | — |
| CAF-RNF-002 | S | C5; R18, R19 | SPD | Una propiedad de exactitud monetaria aplicada a pagos y devoluciones; «sin errores» califica esa misma propiedad. | — |
| CAF-RNF-002 | CL | C3; R4, R8, R24 | SPD | La descripción concreta igualdad con precio/pago autorizado en céntimos; no impone por sí sola una representación interna concreta. | — |
| CAF-RNF-002 | G | R1, R12; R2, R3 | RA | Sistema maneja importes; frase completa y sujeto adecuado, patrón R1 pendiente. | INC-OBS-001 |
| CAF-RNF-002 | T | R7 | SPD | «Exactos» y «sin errores de redondeo» fijan igualdad, no una calidad vagamente elevada. | — |
| CAF-RNF-002 | A | R27 | NA | Propiedad aplicable a los importes de pago y devolución definidos; no existe una condición opcional de activación. | — |
| CAF-RNF-002 | V | C7; R33 | SPD | Se comparan céntimos solicitados con catálogo e importe autorizado: diferencia admitida cero, sin inventar tolerancia o métrica de rendimiento. | — |

## 5. Resumen de hallazgos y cuestiones pendientes

### 5.1. Cobertura y resultados originales de v2

- **Base revisada:** 24 CAF-RF y 2 CAF-RNF; todos frente a los seis aspectos, 156 valoraciones.
- **Seis observaciones:** cinco observaciones propuestas de escritura (INC-OBS-002 a INC-OBS-006) y una cuestión transversal que requiere aclaración (INC-OBS-001).
- **Cinco requisitos con observación propuesta:** CAF-RF-009, CAF-RF-015, CAF-RF-019, CAF-RF-020 y CAF-RF-023.
- **Singularidad:** dos propuestas de separación, CAF-RF-015 y CAF-RF-023. Las condiciones múltiples y listas de datos del resto no justifican por sí solas separaciones.
- **Claridad:** una propuesta de explicitar el contenido de la información en CAF-RF-020.
- **Condiciones:** propuestas para hacer explícito el momento del descuento de vasos (CAF-RF-009) y el ámbito de aplicación de la orden de vaso (CAF-RF-019).
- **Verificabilidad:** las observaciones de CAF-RF-009 y CAF-RF-020 afectan respectivamente al momento de actualización y al contenido verificable del mensaje; se agrupan con sus causas, sin duplicar hallazgos.
- **Estructura:** no se ha detectado un defecto gramatical concreto; no puede comprobarse la conformidad con un patrón acordado de R1. Esta limitación aparece en 26 filas, con una sola observación transversal.
- **R7:** no se detectan términos vagos que generen una observación sustentada en este contexto. No se han inventado métricas, plazos o tolerancias.

| Valoración de las filas | Número |
| --- | ---: |
| Sin problema detectado | 121 |
| Observación propuesta | 7 |
| Requiere aclaración | 26 |
| No aplica | 2 |
| **Total** | **156** |

Las siete filas OP corresponden a cinco problemas: uno afecta a dos aspectos en CAF-RF-009 y otro a dos aspectos en CAF-RF-020. Los totales no representan una puntuación de calidad ni el número de requisitos aprobados. Los requisitos sin OP mantienen la limitación común de R1.

### 5.2. Atención requerida del equipo

1. **INC-OBS-001:** aportar el patrón formal previamente acordado, si existe, o decidirlo en la fase posterior. Hasta entonces no procede declarar conformidad con esa parte de R1 ni redactar adaptaciones obligatorias a una plantilla inferida.
2. **INC-OBS-002:** revisar la incorporación del momento de descuento de vasos ya documentado en el contexto, sin modificar la política de consumo real.
3. **INC-OBS-003:** decidir si se separan las dos asociaciones de CAF-RF-015 y asignar IDs definitivos conservando el origen.
4. **INC-OBS-004:** revisar la explicitación del ámbito de la orden de vaso sin fijar una secuencia física no acordada.
5. **INC-OBS-005:** revisar que el aviso de CAF-RF-020 indique expresamente preparación en curso, sin introducir progreso cuantificado ni plazo nuevo.
6. **INC-OBS-006:** decidir si se separan solicitud de devolución y aviso al cliente, manteniendo asociación, importe y exclusiones actuales.

**Todas las correcciones y redacciones alternativas son propuestas de la IA pendientes de revisión.** No hay aceptación ni rechazo del equipo en este documento. Una respuesta posterior ambigua requiere aclaración. Las decisiones y su justificación deberán registrarse después en `matriz-y-decisiones.md`, vinculadas al requisito, a OpenAI `gpt-6.1-sol` y a cada INC-OBS, distinguiendo hallazgo original, decisión y ajuste posterior. La aceptación futura no cambia estas valoraciones originales de v2. Los cambios acordados se trasladarán a v3 en la fase correspondiente, conservando los requisitos no afectados y las relaciones de origen.

## Atribución de la fuente

International Council on Systems Engineering (INCOSE), Requirements Working Group, *INCOSE Guide to Writing Requirements v4 – Summary Sheet*, INCOSE-TP-2010-006-04, junio de 2023, pp. 2–4; aviso de uso en p. 7.

Copyright (c) 2023 by INCOSE, subject to the following restrictions:

> Use. Given this is summary of the Guide for Writing Requirements, permission to reproduce and use this summary is granted, with attribution to INCOSE and the original author(s) where practical, provided this copyright notice is included with all reproductions and derivative works.
