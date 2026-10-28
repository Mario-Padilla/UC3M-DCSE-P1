# Evaluación INCOSE de los requisitos v2 del proyecto propio

## 1. Identidad, entradas y alcance

**Proveedor: SpaceXAI. Modelo: Grok 4.7.** La identidad corresponde a la indicada para esta sesión en Cursor. No consta un identificador de compilación o de API más específico.

Entradas leídas:

- `AGENTS.md` y `README.md`.
- `docs/enunciado/P1.docx.pdf`, apartados 1.5 y 1.7.
- `docs/05-proyecto-propio/03-evaluacion-incose/reglas-seleccionadas.md`.
- `docs/03-evaluacion-incose/incose_rwg_gtwr_v4_summary_sheet.pdf` (7 páginas): características en la p. 2, reglas en la p. 3 y correspondencia en la p. 4.
- `docs/05-proyecto-propio/02-evaluacion-ia/requisitos-v2.md`: 16 requisitos funcionales y 4 no funcionales. El equipo aceptó el 28 de octubre de 2026 las aplicaciones E5-001 a E5-037.
- `docs/05-proyecto-propio/01-requisitos-iniciales/contexto-y-alcance.md`, incluido el glosario.

La única fuente normativa INCOSE es la hoja-resumen v4, junto con la selección ya usada en el ejercicio 3. No se ha consultado la guía completa. No hay una segunda evaluación de otro modelo: a diferencia de la cafetera, esta respuesta es la única evidencia INCOSE de esta base.

Se evalúa el enunciado. La descripción, la comprobación y el contexto interpretan la frase; no sustituyen una obligación que la frase no expresa. Las propuestas no modifican v2 y no son decisiones del equipo.

## 2. Método

| Aspecto | Referencias |
| --- | --- |
| Singularidad (S) | C5 — Singular (p. 2); R18 — Single Thought Sentence y R19 — Combinators (p. 3). |
| Claridad (CL) | C3 — Unambiguous (p. 2); R4 — Defined Terms, R8 — Escape Clauses y R24 — Pronouns (p. 3). |
| Estructura gramatical (G) | R1 — Structured Statements y R12 — Correct Grammar; apoyo de R2 — Active Voice y R3 — Appropriate Subject-Verb (p. 3). |
| Términos subjetivos (T) | R7 — Vague Terms (p. 3). |
| Condiciones de aplicación (A) | R27 — Explicit Conditions y R28 — Multiple Conditions; apoyo de R11 — Separate Clauses (p. 3). |
| Verificabilidad (V) | C7 — Verifiable (p. 2); cuando corresponda, R33 — Range of Values, R34 — Measurable Performance y R35 — Temporal Dependencies (p. 3). |

Etiquetas de esta evaluación, no categorías oficiales de INCOSE:

- **SPD**, sin problema detectado en ese aspecto.
- **OP**, observación propuesta, con una redacción para revisar.
- **RA**, requiere aclaración.
- **NA**, la regla no tiene objeto en ese enunciado.

Todas las filas G están en RA por INC-OBS-001. Eso no cuenta como 20 defectos gramaticales. R12, R2 y R3 se comentan dentro de esa misma fila.

R4 se contrasta con el glosario y con las definiciones del propio enunciado. No se exige un diccionario de todas las palabras corrientes. R8 y R24 no han motivado observaciones propias: no hay cláusulas de escape del tipo «si es posible» ni pronombres cuya referencia quede oscura. «Su» y «sus» apuntan al requisito, al modelo o al caso ya nombrados en la misma frase.

Una lista de campos de un mismo artefacto se mantiene en un solo requisito. Se propone separar cuando una parte puede cumplirse y la otra no. Las redacciones recogen comportamiento ya aceptado en v2; no añaden formatos, umbrales ni contratos HTTP.

## 3. Observaciones

Los identificadores son estables dentro de esta respuesta. Los sufijos `-A`, `-B`, `-C` y `-D` son provisionales y conservan el requisito de origen.

### INC-OBS-001 — Patrón de R1 no documentado

- **Requisito:** los 20 enunciados. El origen de registro es GMP-RF-001.
- **Fragmento:** «El sistema deberá…». GMP-RNF-001, GMP-RNF-002 y GMP-RNF-004 usan como sujeto la propiedad restringida, no «el sistema».
- **Aspecto y fuente:** estructura gramatical; R1 — Structured Statements (p. 3). R12, R2 y R3 permiten mirar la gramática aparte.
- **Valoración:** requiere aclaración. No hay un patrón formal documentado, como ya registra la selección del ejercicio 3. La regularidad de «El sistema deberá» más infinitivo no demuestra que ese patrón esté acordado.
- **Efecto:** no puede afirmarse la parte de R1 que exige un patrón acordado. Las frases sí son completas y tienen sujeto y predicado reconocibles. El sujeto de los tres requisitos de propiedad no se trata como error gramatical.
- **Solución propuesta:** indicar si ya existe un patrón o acordar uno que cubra acciones del sistema y propiedades restringidas. Mientras tanto, conservar los enunciados en este punto.
- **Pendiente del equipo:** aportar o acordar el patrón. Esta observación se cita una sola vez, aunque aparezca en las 20 filas G.

### INC-OBS-002 — Segmentar y corregir son obligaciones independientes

- **Requisito:** GMP-RF-002.
- **Fragmento:** «segmentar como requisitos individuales los enunciados…, asignarles un identificador único y permitir corregir su texto y su identificador durante la revisión de la ingesta».
- **Aspecto y fuente:** singularidad; C5 (p. 2), R18 y R19 (p. 3).
- **Valoración:** observación propuesta. Asignar el identificador forma parte de dejar constituido cada requisito segmentado. Permitir corregir texto e identificador es otra capacidad: puede haber segmentación correcta y no haber corrección, o al revés. El rechazo del identificador duplicado, ya aceptado, está solo en la descripción.
- **Efecto:** un solo cumplimiento tapa cuál de las dos capacidades falla. «Numerados o en prosa» y «regla de control de acceso o restricción de autorización» sí son alternativas de la misma selección; el glosario trata esas dos fórmulas como el contenido de un requisito de ciberseguridad.
- **Redacciones alternativas:**
  - **GMP-RF-002-A**, origen GMP-RF-002: «El sistema deberá segmentar como requisitos individuales los enunciados, numerados o en prosa, que especifican una regla de control de acceso o una restricción de autorización, y asignar a cada uno un identificador único».
  - **GMP-RF-002-B**, origen GMP-RF-002: «Durante la revisión de la ingesta, y antes de confirmar el modelo lógico, el sistema deberá permitir corregir el texto y el identificador de un requisito segmentado. Si el identificador indicado ya existe, el sistema deberá rechazar el cambio y conservar el identificador anterior».
- **Pendiente del equipo:** aceptar o rechazar la separación y los identificadores provisionales.

### INC-OBS-003 — Proponer etiquetas y bloquear la generación son dos obligaciones

- **Requisito:** GMP-RF-003.
- **Fragmento:** «proponer una etiqueta para cada requisito segmentado y no generar el modelo hasta que el analista confirme o corrija esas etiquetas».
- **Aspecto y fuente:** singularidad; C5 (p. 2), R18 y R19 (p. 3).
- **Valoración:** observación propuesta. El sistema puede proponer etiquetas y, aun así, generar el modelo sin confirmación. También puede bloquear la generación sin haber propuesto etiqueta alguna. «Confirme o corrija» es la relación lógica de una sola compuerta y no hace falta separarla.
- **Efecto:** el cumplimiento parcial queda oculto bajo un identificador.
- **Redacciones alternativas:** el catálogo de etiquetas se precisa en INC-OBS-004 y debe quedar en GMP-RF-003-A.
  - **GMP-RF-003-A**, origen GMP-RF-003: «El sistema deberá proponer, para cada requisito segmentado, una o más etiquetas entre control de acceso y gestión de sesiones, según OWASP ASVS versión 4, y la familia AC de NIST SP 800-53. La autenticación no es una etiqueta. Un enunciado de gestión de sesiones solo continúa hacia el modelo si especifica una restricción de autorización».
  - **GMP-RF-003-B**, origen GMP-RF-003: «El sistema no deberá generar el modelo lógico hasta que el analista confirme o corrija las etiquetas propuestas para cada requisito segmentado».
- **Pendiente del equipo:** aceptar la separación. La segunda frase de GMP-RF-003-A incorpora el comportamiento ya aceptado en la descripción; no abre una función de sesión nueva.

### INC-OBS-004 — «Una etiqueta» no fija el catálogo ni la cantidad

- **Requisito:** GMP-RF-003.
- **Fragmento:** «proponer una etiqueta para cada requisito segmentado».
- **Aspecto y fuente:** claridad; C3 (p. 2) y R4 — Defined Terms (p. 3).
- **Valoración:** observación propuesta. El enunciado no dice qué etiquetas son admisibles. La descripción acepta control de acceso, gestión de sesiones y la familia AC, permite más de una etiqueta por requisito y excluye la autenticación. «Una etiqueta» puede leerse como exactamente una, en tensión con esa descripción. Esas palabras no están en el glosario.
- **Efecto:** dos lectores pueden exigir catálogos o cardinalidades distintos. La comprobación nombra las etiquetas, pero esa columna no forma parte del enunciado.
- **Solución propuesta:** dejar el catálogo, la cardinalidad y la exclusión en el enunciado, como en GMP-RF-003-A de INC-OBS-003.
- **Pendiente del equipo:** confirmar que esa redacción conserva E5-006 y E5-036, ya aceptadas.

### INC-OBS-005 — RBAC para OWASP y ABAC para NIST son dos resultados

- **Requisito:** GMP-RF-004.
- **Fragmento:** «generar un modelo lógico RBAC para los requisitos etiquetados con OWASP ASVS y un modelo lógico ABAC para los etiquetados con NIST SP 800-53».
- **Aspectos y fuente:** singularidad, claridad y condiciones; C5, R18 y R19; C3 y R4; R27, R28 y R11 (pp. 2 y 3).
- **Valoración:** observación propuesta. Cada rama tiene entrada y resultado distintos, y una puede cumplirse sin la otra. El enunciado tampoco dice qué elementos lleva cada modelo ni qué ocurre si un requisito tiene las dos etiquetas. El glosario define el modelo lógico con atributos y condiciones para RBAC y ABAC a la vez; la descripción, ya aceptada, exige atributos solo en ABAC.
- **Efecto:** no queda explícita la relación entre las dos condiciones, y «modelo RBAC» puede incluir o no atributos según se lea el glosario o la descripción.
- **Redacciones alternativas:**
  - **GMP-RF-004-A**, origen GMP-RF-004: «El sistema deberá generar un modelo lógico RBAC para cada requisito etiquetado con OWASP ASVS. Ese modelo incluye sujetos o roles, recursos, acciones y reglas, y no exige atributos».
  - **GMP-RF-004-B**, origen GMP-RF-004: «El sistema deberá generar un modelo lógico ABAC para cada requisito etiquetado con NIST SP 800-53. Ese modelo incluye sujetos o roles, recursos, acciones, reglas, atributos y condiciones».
  - **GMP-RF-004-C**, origen GMP-RF-004: «Si un requisito tiene a la vez una etiqueta OWASP ASVS y una etiqueta NIST SP 800-53, el sistema deberá generar para ese requisito los elementos RBAC y los elementos ABAC».
- **Pendiente del equipo:** aceptar la separación y la explicitación de los elementos ya escritos en la descripción. La interpretación de un requisito ambiguo se trata aparte en INC-OBS-006.

### INC-OBS-006 — La interpretación de un requisito ambiguo no está en el enunciado

- **Requisito:** GMP-RF-004.
- **Fragmento:** el enunciado no menciona la ambigüedad. La descripción dice: «Si el requisito es ambiguo, la IA propone una interpretación en el modelo; no omite la regla ni detiene la ingesta».
- **Aspecto y fuente:** condiciones de aplicación; R27 — Explicit Conditions (p. 3).
- **Valoración:** observación propuesta. Esa conducta fue aceptada con E5-035 y solo aparece en la descripción. El enunciado no dice en qué condición se propone una interpretación ni qué queda prohibido.
- **Efecto:** quien lea solo la frase de obligación no puede exigir ni comprobar esa salida.
- **Redacción alternativa:** **GMP-RF-004-D**, origen GMP-RF-004: «Si un requisito de ciberseguridad es ambiguo, el sistema deberá proponer una interpretación en el modelo lógico. No deberá omitir la regla ni detener la ingesta por esa ambigüedad».
- **Pendiente del equipo:** decidir si esta regla pasa al enunciado. No se propone una definición nueva de «ambiguo» ni un criterio que v2 no tenga.

### INC-OBS-007 — Mostrar, editar y confirmar son tres obligaciones

- **Requisito:** GMP-RF-005.
- **Fragmento:** «mostrar el modelo generado, permitir editar sus elementos y exigir la confirmación del analista antes de generar casos de prueba».
- **Aspectos y fuente:** singularidad y condiciones; C5, R18 y R19; R27 (pp. 2 y 3).
- **Valoración:** observación propuesta. Se puede mostrar el modelo sin permitir editarlo, editarlo sin exigir confirmación, o exigir confirmación sin mostrar el modelo. El efecto ya aceptado —la edición no reescribe los casos Pendiente— está solo en la descripción, así que la condición de la edición no es explícita en el enunciado.
- **Efecto:** el identificador único no dice qué parte falla. La conservación de los casos ya creados no puede exigirse desde la frase.
- **Redacciones alternativas:**
  - **GMP-RF-005-A**, origen GMP-RF-005: «El sistema deberá mostrar el modelo lógico generado».
  - **GMP-RF-005-B**, origen GMP-RF-005: «El sistema deberá permitir editar los elementos del modelo lógico mostrado. La edición deberá actualizar el modelo guardado y las precondiciones de la generación posterior, y no deberá reescribir los casos ya guardados en estado Pendiente».
  - **GMP-RF-005-C**, origen GMP-RF-005: «El sistema deberá exigir la confirmación del analista sobre el modelo lógico antes de generar casos de prueba y no deberá generarlos sin esa confirmación».
- **Pendiente del equipo:** aceptar o rechazar la separación. No se añade propagación automática a los casos ya guardados; v2 la excluyó.

### INC-OBS-008 — Guardar sin ejecutar, corregir y exportar son obligaciones distintas

- **Requisito:** GMP-RF-007.
- **Fragmento:** «guardar los casos generados en estado Pendiente, sin ejecutarlos, y permitir revisarlos, corregir sus campos y exportarlos».
- **Aspecto y fuente:** singularidad; C5 (p. 2), R18 y R19 (p. 3).
- **Valoración:** observación propuesta. Guardar en Pendiente sin ejecutar puede cumplirse aunque no exista exportación. Exportar un archivo es un resultado distinto de corregir campos. Revisar y corregir se mantienen juntos: corregir es la revisión de los campos del mismo caso. El enunciado tampoco dice que corregir o exportar no envía peticiones; eso está en la descripción.
- **Efecto:** una exportación ausente, o una corrección que dispara la API, puede quedar tapada por el hecho de que los casos se guardaron en Pendiente.
- **Redacciones alternativas:**
  - **GMP-RF-007-A**, origen GMP-RF-007: «El sistema deberá guardar los casos generados en estado Pendiente y no ejecutarlos al guardarlos».
  - **GMP-RF-007-B**, origen GMP-RF-007: «Antes de autorizar la ejecución, el sistema deberá permitir revisar los casos en estado Pendiente y corregir sus campos. Revisar o corregir no deberá enviar peticiones a la API de simulación o de referencia».
  - **GMP-RF-007-C**, origen GMP-RF-007: «El sistema deberá permitir exportar los casos en un archivo que contenga sus campos. Esta exportación no fija el formato del archivo y no deberá enviar peticiones a la API de simulación o de referencia».
- **Pendiente del equipo:** aceptar la separación. El formato sigue sin fijarse, como ya decidió el equipo.

### INC-OBS-009 — «Casos concretos» no dice quién los elige

- **Requisito:** GMP-RF-016.
- **Fragmento:** «regenerar casos concretos que estén en Pendiente, con el prompt y la temperatura indicados por el analista».
- **Aspectos y fuente:** claridad y términos vagos; C3 (p. 2), R4 y R7 — Vague Terms (p. 3).
- **Valoración:** observación propuesta. «Concretos» no fija el criterio de selección. La descripción dice que se sustituyen los casos seleccionados. El estado Pendiente y los dos parámetros sí están explícitos en el enunciado, y no se propone un rango de temperatura.
- **Efecto:** podría regenerarse un subconjunto elegido por el sistema, no por el analista, y la frase seguiría teniendo una lectura posible.
- **Redacción alternativa, origen GMP-RF-016:** «El sistema deberá permitir regenerar los casos en estado Pendiente que indique el analista, con el prompt y la temperatura que él indique. La regeneración deberá sustituir solo esos casos y no deberá ejecutarlos».
- **Pendiente del equipo:** confirmar que la elección es del analista, como ya dice la descripción. No se añade otro parámetro.

### INC-OBS-010 — Las tres consistencias se comprueban por separado y su criterio no está en la frase

- **Requisito:** GMP-RF-008.
- **Fragmento:** «validar… la consistencia sintáctica, semántica y lógica del modelo y de los casos respecto de los requisitos».
- **Aspectos y fuente:** singularidad, claridad y verificabilidad; C5, R18 y R19; C3 y R4; C7 (pp. 2 y 3).
- **Valoración:** observación propuesta. Un modelo puede superar la comprobación sintáctica y fallar la lógica. El enunciado no dice qué hecho corresponde a cada clase. Esas tres condiciones están en la descripción y la comprobación ya las provoca por separado. No es una mera lista de adjetivos de una sola salida indiferenciada.
- **Efecto:** un resultado global de «validado» no dice qué clase se comprobó, y la frase sola no permite decidir si un permiso inexistente es error semántico.
- **Redacciones alternativas:** las tres conservan la condición, ya escrita, de no ejecutar ni llamar a la API.
  - **GMP-RF-008-A**, origen GMP-RF-008: «Sin ejecutar pruebas ni llamar a la API, el sistema deberá detectar como Error sintáctico la falta de un campo obligatorio del modelo o del caso».
  - **GMP-RF-008-B**, origen GMP-RF-008: «Sin ejecutar pruebas ni llamar a la API, el sistema deberá detectar como Error semántico la referencia a un rol, recurso, acción o permiso que no existe en el modelo».
  - **GMP-RF-008-C**, origen GMP-RF-008: «Sin ejecutar pruebas ni llamar a la API, el sistema deberá detectar como Error lógico una contradicción entre reglas, un permiso huérfano o un rol sin permisos».
- **Pendiente del equipo:** aceptar la separación. No se añaden clases de defecto distintas de las ya nombradas en v2.

### INC-OBS-011 — Emitir el informe, clasificar y dejar ejecutar son obligaciones distintas

- **Requisito:** GMP-RF-009.
- **Fragmento:** «emitir el informe de validación estática antes de cualquier petición a la API y clasificar cada incidencia como Error o Advertencia».
- **Aspectos y fuente:** singularidad, claridad, condiciones y verificabilidad; C5, R18 y R19; C3 y R4; R27 y R28; C7 (pp. 2 y 3).
- **Valoración:** observación propuesta. Emitir el informe antes de llamar a la API puede cumplirse sin clasificar las incidencias. Clasificar no dice, en el enunciado, qué hallazgo es Error, qué hallazgo es Advertencia, ni el efecto de cada uno sobre la ejecución. Esas tres reglas están aceptadas en la descripción.
- **Efecto:** la frase se cumple con cualquier par de etiquetas, aunque un Error deje ejecutar o una Advertencia lo impida.
- **Redacciones alternativas:**
  - **GMP-RF-009-A**, origen GMP-RF-009: «El sistema deberá emitir el informe de validación estática antes de cualquier petición a la API».
  - **GMP-RF-009-B**, origen GMP-RF-009: «El sistema deberá clasificar cada incidencia de la validación estática como Error o Advertencia. Son Error los hallazgos de error sintáctico, semántico y lógico. Es Advertencia que un requisito de ciberseguridad segmentado no tenga ningún caso».
  - **GMP-RF-009-C**, origen GMP-RF-009: «Un Error deberá impedir iniciar la ejecución. Una Advertencia deberá mostrarse y no deberá impedir la ejecución».
- **Pendiente del equipo:** aceptar la separación y el traslado al enunciado de las reglas ya aceptadas. No se añade un umbral de cobertura.

### INC-OBS-012 — «Filtros» no nombra los filtros aceptados

- **Requisito:** GMP-RF-010.
- **Fragmento:** «seleccionar un subconjunto de casos, de uno en uno o mediante filtros, para ejecutarlo».
- **Aspectos y fuente:** claridad, condiciones y verificabilidad; C3 y R4; R27 y R28; C7 (pp. 2 y 3).
- **Valoración:** observación propuesta. «De uno en uno o mediante filtros» explicita dos modos, pero no los filtros. La descripción limita los filtros al requisito de origen, al tipo autorizado o denegado y, solo si ya hay informe, a la severidad. También excluye otra selección hecha por el sistema. Nada de eso está en el enunciado. La singularidad se mantiene: hay una sola acción de seleccionar.
- **Efecto:** un filtro distinto de los tres aceptados satisfaría la frase. La condición de la severidad queda implícita.
- **Redacción alternativa, origen GMP-RF-010:** «El sistema deberá permitir al analista seleccionar un subconjunto de casos, de uno en uno o mediante los filtros de requisito de origen, de tipo autorizado o denegado y, solo si ya existe el informe de validación, de severidad Error o Advertencia de las incidencias asociadas al caso. No deberá añadir casos que el analista no haya indicado con esa selección».
- **Pendiente del equipo:** confirmar el traslado de los filtros ya aceptados. No se crea un selector nuevo.

### INC-OBS-013 — Pass, Fail y Error se nombran sin regla de asignación

- **Requisito:** GMP-RF-011.
- **Fragmento:** «registrar el código de estado y el payload, y asignar Pass, Fail o Error».
- **Aspectos y fuente:** claridad y verificabilidad; C3 y R4 (p. 2 y p. 3); C7 (p. 2).
- **Valoración:** observación propuesta. El glosario define «veredicto» como Pass, Fail o Error, sin decir cuándo corresponde cada uno. La regla aceptada —coincidencia con el código asociado al resultado esperado, 403 en la denegación de la comprobación, otro código como Fail, falta de respuesta o error de red como Error, y payload que no decide el veredicto— está en la descripción. Ejecutar el subconjunto contra la API indicada sí es una obligación legible; por eso no se propone partir la ejecución.
- **Efecto:** la asignación puede hacerse con otra tabla de códigos y el enunciado seguiría siendo verdadero. El 403 y la diferencia entre Fail y Error no pueden comprobarse desde la frase.
- **Redacciones alternativas:**
  - **GMP-RF-011-A**, origen GMP-RF-011: «El sistema deberá ejecutar solo el subconjunto seleccionado contra la API de simulación o de referencia indicada por el analista, y registrar el código de estado y el payload. El destino no es un entorno de producción. La petición transporta el sujeto o rol, el recurso, la acción y los datos de entrada; este requisito no fija la ruta, el método ni el esquema del cuerpo».
  - **GMP-RF-011-B**, origen GMP-RF-011: «El sistema deberá asignar a cada ejecución el veredicto Pass, Fail o Error. Pass significa que el código recibido es el que el caso asocia a su resultado esperado; en un caso de denegación de la comprobación, 403 Forbidden es Pass. Fail significa que se recibió otro código. Error significa que la API no responde o que se produce un error de red no controlado. El payload queda registrado y no cambia por sí solo el veredicto».
- **Pendiente del equipo:** aceptar que la regla de veredicto pase al enunciado. No se añade ningún código distinto del 403 ya fijado.

### INC-OBS-014 — Cobertura y tasa de éxito tienen fórmulas y condiciones distintas

- **Requisito:** GMP-RF-013.
- **Fragmento:** «calcular y mostrar la cobertura de requisitos y, cuando haya ejecuciones, la tasa de éxito, sin usar el baseline».
- **Aspectos y fuente:** singularidad, claridad y verificabilidad; C5, R18 y R19; C3 y R4; C7 y R34 — Measurable Performance (pp. 2 y 3). R35 no se invoca: «cuando haya ejecuciones» ya nombra la condición.
- **Valoración:** observación propuesta. La cobertura puede mostrarse bien y la tasa mal. Las dos fórmulas aceptadas están en la descripción, no en el enunciado ni en el glosario. Sin ellas, «cobertura» y «tasa de éxito» no tienen un cálculo único. «Sin usar el baseline» sí está en la frase.
- **Efecto:** el 80 % de la comprobación no puede exigirse desde el enunciado, y un denominador distinto seguiría cabiendo en las dos palabras.
- **Redacciones alternativas:**
  - **GMP-RF-013-A**, origen GMP-RF-013: «El sistema deberá calcular y mostrar la cobertura de requisitos sin usar el baseline. El total es el número de requisitos de ciberseguridad segmentados. Un requisito cubierto es el que tiene al menos un caso generado. La cobertura es el número de cubiertos dividido por el total, multiplicado por 100».
  - **GMP-RF-013-B**, origen GMP-RF-013: «Cuando haya ejecuciones, el sistema deberá calcular y mostrar la tasa de éxito sin usar el baseline. La tasa es el número de veredictos Pass dividido por el número de ejecuciones. Fail y Error cuentan en el denominador y no son éxito. Si no hay ejecuciones, el sistema deberá mostrar la cobertura y no deberá mostrar una tasa numérica».
- **Pendiente del equipo:** aceptar la separación y las fórmulas ya escritas en v2. No se cambia el cálculo.

### INC-OBS-015 — «Casos válidos» no tiene criterio en el enunciado

- **Requisito:** GMP-RF-014.
- **Fragmento:** «el número de casos válidos generados y manuales».
- **Aspectos y fuente:** claridad, términos vagos y verificabilidad; C3 y R4; R7 — Vague Terms (p. 3); C7 (p. 2).
- **Valoración:** observación propuesta. «Válidos» es un adjetivo de calidad sin criterio en la frase. La descripción lo fija como caso sin Error de validación estática. La condición de importar el baseline, la referencia a la precisión de GMP-RNF-004 y los recuentos de reglas sí están en el enunciado. La singularidad se mantiene: es una sola presentación de comparaciones, con una lista de datos.
- **Efecto:** «válido» puede significar Pass, caso confirmado o caso sin Error. El recuento no queda determinado.
- **Redacción alternativa, origen GMP-RF-014:** «Si el analista importa un baseline con el modelo manual y los casos manuales, el sistema deberá mostrar la precisión definida para las reglas de control de acceso, el número de reglas generadas y el de reglas manuales, y el número de casos sin Error de validación estática, generados y manuales. Sin baseline, el sistema no deberá mostrar estas comparaciones».
- **Pendiente del equipo:** sustituir «válidos» por el criterio ya aceptado. La frase de precisión debe leerse junto con INC-OBS-018 si también se acepta aquel cambio de título.

### INC-OBS-016 — «Informe consolidado» no dice qué contiene

- **Requisito:** GMP-RF-015.
- **Fragmento:** «exportar el informe consolidado en PDF y en JSON».
- **Aspectos y fuente:** claridad, condiciones y verificabilidad; C3 y R4; R27; C7 (pp. 2 y 3).
- **Valoración:** observación propuesta. PDF y JSON son dos formatos de la misma exportación, con relación conjuntiva explícita; no se separan. «Informe consolidado» no está en el glosario. El contenido, la condición de incluir las comparaciones solo si hay baseline, el idioma, los veredictos y la exclusión del informe de GMP-RF-009 están en la descripción.
- **Efecto:** cualquier PDF y cualquier JSON satisfacen la frase, aunque falten la matriz, la cobertura o los veredictos.
- **Redacción alternativa, origen GMP-RF-015:** «El sistema deberá exportar el informe consolidado en PDF y en JSON. Ambos incluyen la matriz de trazabilidad, la cobertura, la tasa de éxito cuando exista y, por cada ejecución, el identificador del caso, el resultado esperado, el código de estado, el payload y el veredicto. Si hay baseline, también incluyen las comparaciones del baseline. La redacción del informe está en español y los veredictos se exportan como Pass, Fail o Error. El informe de validación estática no forma parte de esta exportación».
- **Pendiente del equipo:** aceptar el traslado del contenido ya acordado. No se añade un apartado nuevo.

### INC-OBS-017 — El enunciado de idioma no recoge las excepciones aceptadas

- **Requisito:** GMP-RNF-001.
- **Fragmento:** «Los textos de la interfaz, los mensajes de estado y la redacción de los informes deberán estar en español».
- **Aspectos y fuente:** claridad y condiciones; C3 (p. 2); R27 — Explicit Conditions (p. 3).
- **Valoración:** observación propuesta. La lista de textos es una sola restricción de idioma. Las excepciones aceptadas —Pass, Fail, Error, Pendiente, las severidades, el texto ingerido y las claves JSON— están solo en la descripción. Sin ellas, la frase también obliga a traducir los veredictos, en tensión con GMP-RF-011.
- **Efecto:** la interfaz puede incumplir la lectura estricta del enunciado precisamente por cumplir los veredictos ya aceptados.
- **Redacción alternativa, origen GMP-RNF-001:** «Los textos de la interfaz, los mensajes de estado y la redacción de los informes deberán estar en español. Conservan su forma definida los valores Pass, Fail y Error, el estado Pendiente, las severidades Error y Advertencia, y el texto ingerido en su idioma original. Las claves del JSON no tienen que estar en español».
- **Pendiente del equipo:** incorporar las excepciones ya aceptadas en E5-030 y E5-031. No se pide traducir el material de entrada.

### INC-OBS-018 — «Precisión» y «extraídas» no fijan el cálculo aceptado

- **Requisito:** GMP-RNF-004.
- **Fragmento:** «la precisión de las reglas de control de acceso extraídas deberá ser de al menos el 85 %».
- **Aspectos y fuente:** claridad y verificabilidad; C3 y R4; C7, R33 — Range of Values y R34 — Measurable Performance (pp. 2 y 3).
- **Valoración:** observación propuesta. El 85 % y la condición de que exista baseline sí están en el enunciado. «Precisión» no está definida en el glosario. La descripción fija la coincidencia, el denominador y el caso de cero reglas, y avisa de que esa coincidencia se escribió para poder comprobar el porcentaje. Además, el enunciado dice «extraídas» y la fórmula habla de reglas generadas. R33 tiene un límite inferior; le falta el criterio de la magnitud que se compara con ese límite.
- **Efecto:** otro emparejamiento de reglas, u otro denominador, también podría presentarse como un 85 %. «Extraídas» y «generadas» pueden no ser el mismo conjunto.
- **Redacción alternativa, origen GMP-RNF-004:** «Cuando exista un baseline, la precisión de las reglas de control de acceso generadas deberá ser de al menos el 85 %. Una regla generada coincide con una del baseline cuando comparten sujeto o rol, recurso, acción y efecto de autorización; en un modelo ABAC también coinciden atributos y condiciones. La precisión es el número de reglas generadas coincidentes dividido por el número de reglas generadas, multiplicado por 100. Si no hay reglas generadas, la precisión no se calcula. Sin baseline, este requisito no se evalúa».
- **Pendiente del equipo:** aceptar el paso de la fórmula ya escrita en la descripción y el cambio de «extraídas» por «generadas». Si el equipo prefiere otra coincidencia, esta propuesta no la inventa: hay que sustituirla antes de cerrar el enunciado.

## 4. Matriz completa

Una fila por requisito y aspecto. INC-OBS-001 acompaña a todas las filas G y no se repite en la justificación de cada una.

| Requisito | Aspecto | Referencias | Valoración | Justificación |
| --- | --- | --- | --- | --- |
| GMP-RF-001 | S | C5, R18, R19 | SPD | Ingerir y mostrar los enunciados recuperados es el mismo resultado. La segmentación está en GMP-RF-002. |
| GMP-RF-001 | CL | C3, R4, R8, R24 | SPD | TXT, MD y PDF con texto extraíble quedan nombrados en la frase. No hay pronombre oscuro ni cláusula de escape. |
| GMP-RF-001 | G | R1, R12, R2, R3 | RA | INC-OBS-001. La frase es completa y el sujeto es el sistema. |
| GMP-RF-001 | T | R7 | SPD | No hay cuantificador ni adjetivo vago. «Extraíble» es la condición del PDF, precisada por el caso negativo de la descripción. |
| GMP-RF-001 | A | R27, R28, R11 | SPD | Los tres formatos son el dominio de la ingesta. La relación es de formatos admitidos, no la exigencia de un archivo que sea los tres a la vez; así lo lee también la comprobación, que carga uno de cada tipo. |
| GMP-RF-001 | V | C7, R33, R34, R35 | SPD | Se comprueba viendo los enunciados en la interfaz y la ausencia de requisitos desde un PDF sin texto. R33, R34 y R35 no tienen magnitud ni plazo en esta frase. |
| GMP-RF-002 | S | C5, R18, R19 | OP | INC-OBS-002. Segmentar y corregir pueden cumplirse por separado. |
| GMP-RF-002 | CL | C3, R4, R8, R24 | SPD | «Su texto y su identificador» remiten al requisito segmentado. Las dos fórmulas de acceso se leen como una clase, según el glosario. |
| GMP-RF-002 | G | R1, R12, R2, R3 | RA | INC-OBS-001. La frase es completa y está en voz activa. |
| GMP-RF-002 | T | R7 | SPD | «Único» es comprobable por la ausencia de duplicados, no es un cuantificador vago. |
| GMP-RF-002 | A | R27, R28, R11 | SPD | «Numerados o en prosa» y la ventana «durante la revisión de la ingesta» están escritos. El rechazo del duplicado se trata al separar, en INC-OBS-002. |
| GMP-RF-002 | V | C7, R33, R34, R35 | SPD | La segmentación y la corrección son observables. R33, R34 y R35 no añaden una magnitud a esta frase. |
| GMP-RF-003 | S | C5, R18, R19 | OP | INC-OBS-003. Proponer etiquetas y no generar el modelo son obligaciones independientes. |
| GMP-RF-003 | CL | C3, R4, R8, R24 | OP | INC-OBS-004. «Una etiqueta» no fija el catálogo ni si puede haber varias. |
| GMP-RF-003 | G | R1, R12, R2, R3 | RA | INC-OBS-001. Sujeto y acción son identificables. |
| GMP-RF-003 | T | R7 | SPD | No hay adjetivo vago en el enunciado. |
| GMP-RF-003 | A | R27, R28, R11 | SPD | «Hasta que el analista confirme o corrija» explicita la compuerta y la relación entre confirmar y corregir. |
| GMP-RF-003 | V | C7, R33, R34, R35 | SPD | La compuerta es comprobable. El catálogo, que es el problema de claridad, no impide ver si el modelo se genera antes de una acción del analista. |
| GMP-RF-004 | S | C5, R18, R19 | OP | INC-OBS-005. RBAC para OWASP y ABAC para NIST pueden cumplirse por separado. |
| GMP-RF-004 | CL | C3, R4, R8, R24 | OP | INC-OBS-005. El glosario atribuye atributos a todo modelo lógico y la descripción solo a ABAC. |
| GMP-RF-004 | G | R1, R12, R2, R3 | RA | INC-OBS-001. La frase es completa y está en voz activa. |
| GMP-RF-004 | T | R7 | SPD | RBAC y ABAC no se usan aquí como adjetivos vagos. |
| GMP-RF-004 | A | R27, R28, R11 | OP | INC-OBS-005 para las dos etiquetas a la vez. INC-OBS-006 para el requisito ambiguo, cuya condición está solo en la descripción. |
| GMP-RF-004 | V | C7, R33, R34, R35 | SPD | Generar un modelo por etiqueta es observable. Las carencias de elementos y de ambigüedad están en claridad y condiciones, no en una magnitud ausente. |
| GMP-RF-005 | S | C5, R18, R19 | OP | INC-OBS-007. Mostrar, editar y exigir confirmación son tres obligaciones. |
| GMP-RF-005 | CL | C3, R4, R8, R24 | SPD | «Sus elementos» remite al modelo generado. El modelo lógico está en el glosario. |
| GMP-RF-005 | G | R1, R12, R2, R3 | RA | INC-OBS-001. La frase es completa y está en voz activa. |
| GMP-RF-005 | T | R7 | SPD | No hay término vago en el enunciado. |
| GMP-RF-005 | A | R27, R28, R11 | OP | INC-OBS-007. La confirmación previa es explícita; el efecto sobre los casos Pendiente ya creados no lo es. |
| GMP-RF-005 | V | C7, R33, R34, R35 | SPD | Mostrar, editar y bloquear la generación son comprobables. R33, R34 y R35 no aplican una cifra a esta frase. |
| GMP-RF-006 | S | C5, R18, R19 | SPD | Generar el par autorizado y denegado por regla es una sola generación, con un mínimo que califica el mismo resultado. |
| GMP-RF-006 | CL | C3, R4, R8, R24 | SPD | «Caso», «autorizado» y «denegado» remiten al glosario de caso de prueba. Los campos del caso están en esa definición. |
| GMP-RF-006 | G | R1, R12, R2, R3 | RA | INC-OBS-001. La frase es completa y está en voz activa. |
| GMP-RF-006 | T | R7 | SPD | «Al menos un» es un mínimo explícito, no un cuantificador vago. |
| GMP-RF-006 | A | R27, R28, R11 | SPD | El modelo confirmado y el momento anterior a la validación estática están en la frase. R35 queda cubierto por ese orden. |
| GMP-RF-006 | V | C7, R33, R35 | SPD | El par por regla y el momento son comprobables. R34 no pide aquí un rendimiento temporal. |
| GMP-RF-007 | S | C5, R18, R19 | OP | INC-OBS-008. Guardar sin ejecutar, corregir y exportar tienen resultados distintos. |
| GMP-RF-007 | CL | C3, R4, R8, R24 | SPD | «Sus campos» remite a los campos del caso ya definido. Pendiente es el estado nombrado. |
| GMP-RF-007 | G | R1, R12, R2, R3 | RA | INC-OBS-001. La frase es completa y está en voz activa. |
| GMP-RF-007 | T | R7 | SPD | No hay adjetivo vago. La ausencia de formato es una exclusión explícita de la descripción, no una vaguedad del verbo exportar. |
| GMP-RF-007 | A | R27, R28, R11 | SPD | «Sin ejecutarlos» acompaña a guardar. Que corregir y exportar tampoco llaman a la API se incorpora al separar, en INC-OBS-008. |
| GMP-RF-007 | V | C7, R33, R34, R35 | SPD | Estado Pendiente, ausencia de petición al guardar y existencia del archivo son comprobables. |
| GMP-RF-016 | S | C5, R18, R19 | SPD | Regenerar unos casos con dos parámetros es una sola acción. |
| GMP-RF-016 | CL | C3, R4, R8, R24 | OP | INC-OBS-009. «Concretos» no identifica quién selecciona los casos. |
| GMP-RF-016 | G | R1, R12, R2, R3 | RA | INC-OBS-001. La frase es completa y está en voz activa. |
| GMP-RF-016 | T | R7 | OP | INC-OBS-009. «Concretos» deja el conjunto sin criterio. |
| GMP-RF-016 | A | R27, R28, R11 | SPD | El estado Pendiente y los dos parámetros indicados por el analista están en la frase. |
| GMP-RF-016 | V | C7, R33, R34, R35 | SPD | Prompt, temperatura y permanencia en Pendiente son comprobables. R33 no exige un rango de temperatura: v2 lo excluye. |
| GMP-RF-008 | S | C5, R18, R19 | OP | INC-OBS-010. Cada clase de consistencia puede cumplirse sin las otras. |
| GMP-RF-008 | CL | C3, R4, R8, R24 | OP | INC-OBS-010. Sintáctica, semántica y lógica no tienen criterio en la frase. |
| GMP-RF-008 | G | R1, R12, R2, R3 | RA | INC-OBS-001. La frase es completa y está en voz activa. |
| GMP-RF-008 | T | R7 | SPD | Los tres adjetivos designan clases que la descripción ya concreta; el defecto es que esa concreción no está en el enunciado, no un uso vago suelto. |
| GMP-RF-008 | A | R27, R28, R11 | SPD | «Sin ejecutar pruebas ni llamar a la API» es la condición común y está en la frase. |
| GMP-RF-008 | V | C7, R33, R34, R35 | OP | INC-OBS-010. Sin el criterio de cada clase no puede decidirse si la validación pedida se ha hecho. |
| GMP-RF-009 | S | C5, R18, R19 | OP | INC-OBS-011. Emitir el informe y clasificar pueden separarse; el efecto sobre la ejecución es una tercera obligación. |
| GMP-RF-009 | CL | C3, R4, R8, R24 | OP | INC-OBS-011. Error y Advertencia no quedan definidos en la frase. |
| GMP-RF-009 | G | R1, R12, R2, R3 | RA | INC-OBS-001. La frase es completa y está en voz activa. |
| GMP-RF-009 | T | R7 | SPD | Error y Advertencia funcionan como nombres de clase. Lo que falta es su criterio, tratado en claridad. |
| GMP-RF-009 | A | R27, R28, R11 | OP | INC-OBS-011. El momento anterior a la API es explícito; el efecto de cada severidad no lo es. |
| GMP-RF-009 | V | C7, R33, R34, R35 | OP | INC-OBS-011. Una etiqueta cualquiera no permite comprobar el bloqueo ya aceptado. |
| GMP-RF-010 | S | C5, R18, R19 | SPD | Seleccionar un subconjunto, de uno en uno o por filtros, es una sola acción. |
| GMP-RF-010 | CL | C3, R4, R8, R24 | OP | INC-OBS-012. «Filtros» no está definido en la frase ni en el glosario. |
| GMP-RF-010 | G | R1, R12, R2, R3 | RA | INC-OBS-001. La frase es completa y está en voz activa. |
| GMP-RF-010 | T | R7 | SPD | No se usa un cuantificador vago. La indefinición de los filtros es de término, no de la lista de R7. |
| GMP-RF-010 | A | R27, R28, R11 | OP | INC-OBS-012. Falta la condición de que el filtro de severidad solo existe si ya hay informe. |
| GMP-RF-010 | V | C7, R33, R34, R35 | OP | INC-OBS-012. Sin la lista de filtros no puede decidirse si el subconjunto es el aceptado. |
| GMP-RF-011 | S | C5, R18, R19 | SPD | Ejecutar, registrar y asignar veredicto son los resultados de la misma ejecución. La separación propuesta en INC-OBS-013 sirve para sacar la regla del veredicto, no porque el «y» original sea por sí solo varias funciones. |
| GMP-RF-011 | CL | C3, R4, R8, R24 | OP | INC-OBS-013. El glosario nombra Pass, Fail y Error, y no dice cuándo se asigna cada uno. |
| GMP-RF-011 | G | R1, R12, R2, R3 | RA | INC-OBS-001. La frase es completa y está en voz activa. |
| GMP-RF-011 | T | R7 | SPD | No hay adjetivo vago en el enunciado. |
| GMP-RF-011 | A | R27, R28, R11 | SPD | «Solo el subconjunto seleccionado» y la API indicada por el analista están en la frase. |
| GMP-RF-011 | V | C7, R33, R34, R35 | OP | INC-OBS-013. Sin la regla de asignación no puede comprobarse el veredicto. R34 no pide un tiempo de respuesta. |
| GMP-RF-012 | S | C5, R18, R19 | SPD | El enlace entre caso, requisito y regla es una sola relación, con su cardinalidad. |
| GMP-RF-012 | CL | C3, R4, R8, R24 | SPD | «Bidireccional», requisito de ciberseguridad y regla quedan delimitados por el glosario y por la propia frase, que fija una regla y un requisito. |
| GMP-RF-012 | G | R1, R12, R2, R3 | RA | INC-OBS-001. La frase es completa y está en voz activa. |
| GMP-RF-012 | T | R7 | SPD | «Único» fija la cardinalidad; no es un cuantificador vago. |
| GMP-RF-012 | A | R27, R28, R11 | SPD | La obligación aplica a cada caso. No hay una segunda condición que quede implícita. |
| GMP-RF-012 | V | C7, R33, R34, R35 | SPD | Los tres sentidos del enlace son comprobables. R33, R34 y R35 no añaden una cifra. |
| GMP-RF-013 | S | C5, R18, R19 | OP | INC-OBS-014. Cobertura y tasa de éxito pueden cumplirse por separado. |
| GMP-RF-013 | CL | C3, R4, R8, R24 | OP | INC-OBS-014. Ninguna de las dos magnitudes está definida en la frase ni en el glosario. |
| GMP-RF-013 | G | R1, R12, R2, R3 | RA | INC-OBS-001. La frase es completa y está en voz activa. |
| GMP-RF-013 | T | R7 | SPD | No hay un adjetivo de calidad suelto. La falta de fórmula se trata como definición ausente. |
| GMP-RF-013 | A | R27, R28, R11 | SPD | «Cuando haya ejecuciones» y «sin usar el baseline» están en la frase. |
| GMP-RF-013 | V | C7, R34, R35 | OP | INC-OBS-014. R34 pide un desempeño medible y la frase no contiene el cálculo. |
| GMP-RF-014 | S | C5, R18, R19 | SPD | Mostrar la precisión y los recuentos es una sola presentación. Los datos no son funciones distintas. |
| GMP-RF-014 | CL | C3, R4, R8, R24 | OP | INC-OBS-015. «Casos válidos» no está definido en la frase. |
| GMP-RF-014 | G | R1, R12, R2, R3 | RA | INC-OBS-001. La frase condicional es completa. |
| GMP-RF-014 | T | R7 | OP | INC-OBS-015. «Válidos» deja el recuento sin criterio. |
| GMP-RF-014 | A | R27, R28, R11 | SPD | «Si el analista importa un baseline» explicita la condición. La precisión se remite a GMP-RNF-004. |
| GMP-RF-014 | V | C7, R33, R34, R35 | OP | INC-OBS-015. El recuento de casos no es medible mientras «válidos» no tenga criterio. |
| GMP-RF-015 | S | C5, R18, R19 | SPD | PDF y JSON son dos formatos de la misma exportación. |
| GMP-RF-015 | CL | C3, R4, R8, R24 | OP | INC-OBS-016. «Informe consolidado» no está definido. |
| GMP-RF-015 | G | R1, R12, R2, R3 | RA | INC-OBS-001. La frase es completa y está en voz activa. |
| GMP-RF-015 | T | R7 | SPD | «Consolidado» se trata como término sin definición, no como un adjetivo de la lista de R7 usado de forma vaga aparte de ese problema. |
| GMP-RF-015 | A | R27, R28, R11 | OP | INC-OBS-016. La inclusión de las comparaciones solo cuando hay baseline no está en la frase. |
| GMP-RF-015 | V | C7, R33, R34, R35 | OP | INC-OBS-016. Sin el contenido, cualquier pareja de archivos satisface el enunciado. |
| GMP-RNF-001 | S | C5, R18, R19 | SPD | Interfaz, mensajes e informes son los objetos de una sola restricción de idioma. |
| GMP-RNF-001 | CL | C3, R4, R8, R24 | OP | INC-OBS-017. Sin las excepciones, la frase también obliga a traducir Pass, Fail y Error. |
| GMP-RNF-001 | G | R1, R12, R2, R3 | RA | INC-OBS-001. El sujeto es la propiedad restringida. No se marca como defecto de R3. |
| GMP-RNF-001 | T | R7 | SPD | No hay adjetivo vago. |
| GMP-RNF-001 | A | R27, R28, R11 | OP | INC-OBS-017. Las excepciones son condiciones de aplicación y están solo en la descripción. |
| GMP-RNF-001 | V | C7, R33, R34, R35 | SPD | El idioma de la interfaz es comprobable. El conflicto con los veredictos es de claridad y de condiciones. |
| GMP-RNF-002 | S | C5, R18, R19 | SPD | Un solo límite temporal para una sola generación. |
| GMP-RNF-002 | CL | C3, R4, R8, R24 | SPD | El intervalo medido y la inclusión de la respuesta del LLM están en la frase. |
| GMP-RNF-002 | G | R1, R12, R2, R3 | RA | INC-OBS-001. El sujeto es «el tiempo». No se marca como defecto de R3. |
| GMP-RNF-002 | T | R7 | SPD | «Como máximo» y «no deberá superar» son límites, no cuantificadores vagos. |
| GMP-RNF-002 | A | R27, R28, R11 | SPD | La condición es un modelo inicial de como máximo 10 requisitos ya segmentados. |
| GMP-RNF-002 | V | C7, R33, R34, R35 | SPD | 15 segundos, desde la solicitud hasta mostrar el modelo, es una medida con extremos definidos. Si el LLM no responde, el plazo no llega a cumplirse. |
| GMP-RNF-003 | S | C5, R18, R19 | SPD | Guardar y recuperar es una sola obligación, aplicada a una lista de datos. |
| GMP-RNF-003 | CL | C3, R4, R8, R24 | SPD | Prompt, parámetros, LLM, versión del modelo lógico, casos y fecha están enumerados. «Identidad o versión» es una alternativa explícita. |
| GMP-RNF-003 | G | R1, R12, R2, R3 | RA | INC-OBS-001. La frase es completa y está en voz activa. |
| GMP-RNF-003 | T | R7 | SPD | No hay adjetivo vago. La semilla no está exigida por el enunciado. |
| GMP-RNF-003 | A | R27, R28, R11 | NA | La obligación no depende de una condición de aplicación. No falta una condición que el enunciado esté dejando implícita. |
| GMP-RNF-003 | V | C7, R33, R34, R35 | SPD | Abrir el histórico y encontrar esos datos es comprobable. R34 no pide repetir la llamada ni obtener el mismo texto. |
| GMP-RNF-004 | S | C5, R18, R19 | SPD | Un solo umbral de precisión, condicionado a que exista baseline. |
| GMP-RNF-004 | CL | C3, R4, R8, R24 | OP | INC-OBS-018. «Precisión» y «extraídas» no fijan el conjunto ni la coincidencia. |
| GMP-RNF-004 | G | R1, R12, R2, R3 | RA | INC-OBS-001. El sujeto es «la precisión». No se marca como defecto de R3. |
| GMP-RNF-004 | T | R7 | SPD | El 85 % no es un término vago. Lo que falta es la definición de la magnitud. |
| GMP-RNF-004 | A | R27, R28, R11 | SPD | «Cuando exista un baseline» está en la frase. |
| GMP-RNF-004 | V | C7, R33, R34 | OP | INC-OBS-018. R33 fija el 85 % y R34 no puede aplicarse mientras el cálculo no esté en el enunciado. |

## 5. Resumen

La base tiene 20 requisitos y 120 valoraciones: 36 observaciones propuestas, 20 aclaraciones de R1, 1 no aplica y 63 sin problema detectado en ese aspecto. Las 20 aclaraciones son la misma limitación, INC-OBS-001, y no son 20 defectos de gramática.

Hay 18 observaciones. Aparte de R1, no reciben observación propia GMP-RF-001, GMP-RF-006, GMP-RF-012, GMP-RNF-002 y GMP-RNF-003.

| Qué debe decidir el equipo | Observaciones |
| --- | --- |
| Si existe un patrón de redacción o si se acuerda ahora | INC-OBS-001 |
| Si se separan obligaciones que pueden cumplirse una sin la otra | INC-OBS-002, INC-OBS-003, INC-OBS-005, INC-OBS-007, INC-OBS-008, INC-OBS-010, INC-OBS-011 y INC-OBS-014 |
| Si las reglas ya aceptadas en la descripción pasan al enunciado | INC-OBS-004, INC-OBS-005, INC-OBS-006, INC-OBS-007, INC-OBS-009, INC-OBS-010, INC-OBS-011, INC-OBS-012, INC-OBS-013, INC-OBS-014, INC-OBS-015, INC-OBS-016, INC-OBS-017 y INC-OBS-018 |
| Si «extraídas» pasa a «generadas» en el umbral del 85 % | INC-OBS-018 |

No se ha creado una v3. Los identificadores con sufijo son provisionales. Aceptar una separación no obliga a aceptar la redacción literal propuesta. El contexto sigue teniendo tres frases que la sección 3 de v2 lee de otra manera; esta evaluación no reescribe el contexto.

No se propone formato de archivo, contrato HTTP, rango de temperatura, código distinto de 403 ni un porcentaje nuevo. R30, la duplicidad entre requisitos, no se ha evaluado.
