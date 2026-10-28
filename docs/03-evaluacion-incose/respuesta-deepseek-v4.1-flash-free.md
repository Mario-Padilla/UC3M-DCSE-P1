# Evaluación INCOSE de requisitos v2 — DeepSeek deepseek-v4.1-flash-free

## 1. Identidad del evaluador

- **Proveedor/modelo:** DeepSeek `deepseek-v4.1-flash-free`, ejecutado a través de OpenCode CLI.
- **ID de ejecución:** `opencode/deepseek-v4.1-flash-free`.
- **Versión:** la identificación disponible incluye `v4.1-flash-free`; no se ha podido confirmar un número de compilación o versión adicional distinto. Se indica esta limitación de forma expresa.
- **Evaluación:** revisión de escritura de requisitos, no de implementación ni de pruebas ejecutadas. No se declara ningún requisito aprobado ni el ejercicio terminado.

## 2. Entradas utilizadas

Todas las entradas solicitadas estaban disponibles y se han leído:

| Entrada | Comprobación |
| --- | --- |
| `AGENTS.md` | Leído. Instrucciones de trabajo y conservación de evidencias. |
| `README.md` | Leído. Índice del trabajo y estado del ejercicio 3. |
| `docs/enunciado/P1.docx.pdf` | Leído. 3 páginas; apartado 1.5 en la página 2. |
| `docs/03-evaluacion-incose/reglas-seleccionadas.md` | Leído. Selección de seis aspectos y criterios de aplicación. |
| `docs/03-evaluacion-incose/incose_rwg_gtwr_v4_summary_sheet.pdf` | Leído. 7 páginas; características en la p. 2, reglas en la p. 3 y matriz de correspondencia en la p. 4. |
| `docs/02-evaluacion-ia/requisitos-v2.md` | Leído. Base de evaluación: 24 requisitos funcionales y 2 no funcionales. |
| `docs/01-requisitos-iniciales/contexto-y-alcance.md` | Leído. Contexto, glosario, alcance, catálogo, recetas y supuestos. |

**Fuente normativa:** exclusivamente la hoja-resumen oficial *INCOSE Guide to Writing Requirements v4 – Summary Sheet*, INCOSE-TP-2010-006-04, junio de 2023, y la selección documentada en `reglas-seleccionadas.md`. No se ha consultado la guía completa de INCOSE; no se afirma haberlo hecho.

**Independencia:** la evaluación se ha realizado con las entradas anteriores. No se ha utilizado como fuente la respuesta del otro modelo. Las propuestas de este documento son de la IA y no constituyen decisiones del equipo.

## 3. Alcance, método y limitaciones

- **Unidad de evaluación:** cada enunciado de requisito de `requisitos-v2.md`. Se han consultado su descripción, su criterio de comprobación y el contexto documentado.
- **Cobertura:** 26 requisitos × 6 aspectos = 156 valoraciones en la matriz final. Una misma observación puede afectar a varios aspectos; se agrupa para no duplicar el problema.
- **Etiquetas de esta evaluación:** «sin problema detectado», «observación propuesta», «requiere aclaración» y «no aplica». No son categorías oficiales de INCOSE.
- **Sin duplicidad entre requisitos:** R30 – Unique Expression no forma parte de la selección. No se evalúa si dos requisitos repiten una obligación; solo la singularidad interna de cada enunciado.
- **R1 – Structured Statements:** el proyecto no documenta un patrón formal de enunciado acordado. Por ello **no se declara conformidad con R1** en ninguna fila. La valoración de «Estructura gramatical» se refiere a R12 – Correct Grammar y, como apoyo, a R2 – Active Voice y R3 – Appropriate Subject-Verb; también se comprueba que el enunciado sea una frase completa. La limitación es global (L1) y no se repite como observación en cada requisito.
- **R4 – Defined Terms:** el contexto contiene una tabla de términos, pero no un glosario exhaustivo. No se señalan palabras comunes cuyo significado no afecte a la interpretación; solo se observan términos cuya falta de definición produce una ambigüedad material (L2).
- **Términos subjetivos (R7):** no se marca una palabra solo por pertenecer a una lista. Se ha comprobado si el contexto o una referencia aplicable acota su significado. Se explican los casos dudosos en la matriz.
- **Verificabilidad (C7):** se evalúa si el enunciado está estructurado y redactado para poder verificarse. No se han ejecutado pruebas; las columnas «Cómo comprobarlo» son planes, no resultados (L4). No se inventan métricas, plazos ni tolerancias.
- **Condiciones:** no se añaden condiciones de negocio no acordadas. Cuando una condición o su relación lógica no es explícita, se propone aclararla; no se supone una regla nueva.
- **R1 y patrón formal:** si el equipo documenta y acuerda un patrón, deberá revisarse de nuevo la conformidad con R1. Esta evaluación no lo suple.

## 4. Correspondencia de aspectos y reglas utilizadas

| Aspecto | IDs y títulos | Página |
| --- | --- | --- |
| Singularidad | C5 – Singular; R18 – Single Thought Sentence; R19 – Combinators | C5 p. 2; R18 y R19 p. 3 |
| Claridad | C3 – Unambiguous; R4 – Defined Terms; R8 – Escape Clauses; R24 – Pronouns | C3 p. 2; R4, R8 y R24 p. 3 |
| Estructura gramatical | R1 – Structured Statements; R12 – Correct Grammar; apoyo: R2 – Active Voice y R3 – Appropriate Subject-Verb | R1, R2, R3 y R12 p. 3 |
| Términos subjetivos | R7 – Vague Terms | p. 3 |
| Condiciones de aplicación | R27 – Explicit Conditions; R28 – Multiple Conditions; apoyo: R11 – Separate Clauses | p. 3 |
| Verificabilidad | C7 – Verifiable; cuando procede: R33 – Range of Values, R34 – Measurable Performance y R35 – Temporal Dependencies | C7 p. 2; R33, R34 y R35 p. 3 |

La matriz de correspondencia entre reglas y características está en la p. 4 de la hoja-resumen. Se ha usado como orientación, sin ampliar la selección a otras reglas.

## 5. Observaciones

### INC-OBS-001 — CAF-RF-003

- **Requisito:** CAF-RF-003.
- **Fragmento:** «Si la bebida seleccionada no está disponible, el sistema deberá permitir seleccionar otra bebida sin exigir una cancelación previa.»
- **Aspecto:** Condiciones de aplicación (principal), Claridad y Verificabilidad.
- **INCOSE aplicable:** R27 – Explicit Conditions (p. 3), R28 – Multiple Conditions (p. 3), R11 – Separate Clauses (p. 3); C3 – Unambiguous (p. 2) y C7 – Verifiable (p. 2).
- **Problema:** el enunciado regula solo el caso de indisponibilidad. La descripción añade una regla para «los demás casos» —cambiar de bebida exige cancelar la operación mientras esté permitido e iniciar una nueva— y el criterio de comprobación incluye, además, que no se permita el cambio con una autorización pendiente o después de su aprobación. Esa regla complementaria no está en el enunciado. Un lector del requisito aislado podría inferir que, si la bebida está disponible, no se exige cancelación, o que la regla es exhaustiva.
- **Efecto:** la aplicabilidad del requisito queda abierta fuera del caso de indisponibilidad. El criterio de comprobación prueba comportamientos que no se derivan del texto, por lo que no puede usarse para completar el enunciado. No se trata de una duplicidad entre requisitos ni de una nueva condición de negocio: la regla ya está documentada en el contexto y en la descripción.
- **Naturaleza:** duda por aclarar sobre el alcance del requisito. El texto es claro para el caso de no disponibilidad; falta decidir si la regla complementaria pertenece a este requisito o a otro.
- **Solución propuesta:** mantener CAF-RF-003 para la sustitución directa cuando la bebida no está disponible y trasladar la regla de los demás casos a un requisito separado, con su propia descripción y comprobación. La restricción de no cambiar con autorización pendiente o aprobada se deriva de ese requisito y de CAF-RF-016; no debe duplicarse.
- **Redacción alternativa:**
  - **CAF-RF-003 (sin cambio):** «Si la bebida seleccionada no está disponible, el sistema deberá permitir seleccionar otra bebida sin exigir una cancelación previa.»
  - **CAF-RF-003A (provisional):** «Si la bebida seleccionada está disponible y la operación no tiene una solicitud de autorización pendiente ni un pago autorizado, el sistema deberá exigir la cancelación de la operación para cambiar de bebida.»
- **Pendiente:** el equipo debe confirmar si acepta la separación y la redacción de CAF-RF-003A. Si prefiere mantener una sola regla, deberá decidir cómo evitar que el enunciado exprese dos obligaciones independientes.

### INC-OBS-002 — CAF-RF-010

- **Requisito:** CAF-RF-010.
- **Fragmento:** «una vez comprobada su disponibilidad».
- **Aspecto:** Condiciones de aplicación (principal) y Verificabilidad.
- **INCOSE aplicable:** R27 – Explicit Conditions (p. 3); C7 – Verifiable (p. 2).
- **Problema:** «comprobada su disponibilidad» afirma que se realizó la comprobación, no que el resultado fuera favorable. Leído literalmente, el sistema podría solicitar la autorización después de una comprobación que haya concluido que la bebida no está disponible. Eso contradice CAF-RF-006 y deja sin definir el valor de verdad de la condición. La descripción y el criterio de comprobación asumen que la disponibilidad es positiva.
- **Efecto:** un verificador no puede determinar de forma unívoca si debe solicitarse el pago tras una comprobación negativa. El pronombre posesivo «su» tiene antecedente inmediato («bebida seleccionada») y el contexto lo confirma; no se plantea una observación independiente por R24.
- **Naturaleza:** defecto sustentado de redacción de la condición. La intención está documentada en el contexto y en CAF-RF-006; no falta una decisión de negocio.
- **Solución propuesta:** explicitar que la comprobación debe ser satisfactoria, sin cambiar el precio ni el terminal.
- **Redacción alternativa:** «El sistema deberá solicitar al terminal la autorización del pago por el precio de la bebida seleccionada, solo después de comprobar que está disponible.»
- **Pendiente:** confirmar que la intención es «disponibilidad confirmada» y no «comprobación realizada». Si fuera lo segundo, deberá aclararse la relación con CAF-RF-006.

### INC-OBS-003 — CAF-RF-015

- **Requisito:** CAF-RF-015.
- **Fragmento:** «El sistema deberá asociar cada resultado de autorización con el intento de pago correspondiente y permitir vincular una solicitud de devolución con el intento autorizado que la origina.»
- **Aspecto:** Singularidad.
- **INCOSE aplicable:** C5 – Singular (p. 2); R18 – Single Thought Sentence (p. 3); R19 – Combinators (p. 3).
- **Problema:** el enunciado contiene dos obligaciones independientes unidas por «y»: (1) asociar cada resultado de autorización con el intento de pago correspondiente; (2) permitir vincular una solicitud de devolución con el intento autorizado que la origina. Tienen objetos distintos y pueden cumplirse una sin la otra. La segunda no es una mera subcláusula que califique la primera; añade una capacidad propia. El propósito común de trazabilidad no convierte ambas en una sola capacidad bajo C5/R18.
- **Efecto:** la verificación y la posible corrección de una parte quedan mezcladas con la otra. Un cambio en la asociación de resultados puede afectar a la devolución, pero no son la misma obligación.
- **Naturaleza:** defecto sustentado de singularidad. No requiere información nueva; solo separar y redistribuir descripción y comprobación.
- **Solución propuesta:** separar en dos requisitos, conservando CAF-RF-015 como origen común.
- **Redacción alternativa:**
  - **CAF-RF-015A (provisional):** «El sistema deberá asociar cada resultado de autorización con el intento de pago correspondiente.»
  - **CAF-RF-015B (provisional):** «El sistema deberá poder asociar una solicitud de devolución con el intento de pago autorizado que la origina.»
- **Pendiente:** el equipo debe aceptar la separación y decidir si «poder asociar» recoge mejor la intención que «permitir vincular». La descripción y la comprobación deben repartirse: 015A verifica la correspondencia resultado-intento en denegación y autorización; 015B verifica que la devolución se vincula al intento autorizado y a su importe.

### INC-OBS-004 — CAF-RF-014

- **Requisito:** CAF-RF-014.
- **Fragmento:** «durante la selección y antes de iniciar una solicitud de autorización, o tras recibir una denegación y antes de otro intento».
- **Aspecto:** Condiciones de aplicación (principal), Claridad y Verificabilidad.
- **INCOSE aplicable:** R27 – Explicit Conditions (p. 3), R28 – Multiple Conditions (p. 3), R11 – Separate Clauses (p. 3); C3 – Unambiguous (p. 2) y C7 – Verifiable (p. 2).
- **Problema:** la primera ventana se expresa con «y»: «durante la selección y antes de iniciar una solicitud de autorización». Puede leerse como dos condiciones acumulativas. Si la selección termina cuando el cliente elige la bebida, la cancelación después de elegir y antes de solicitar autorización podría no estar cubierta, aunque el contexto y el criterio de comprobación la admiten. La relación entre las dos ventanas («o») sí es clara; la falta de precisión está en el límite de la primera.
- **Efecto:** un verificador no puede saber si debe aceptar la cancelación en todo el intervalo previo a la autorización o solo mientras se está eligiendo. R11 pide una cláusula separada para cada condición o calificación; R28 pide explicitar la naturaleza proposicional de la condición.
- **Naturaleza:** defecto sustentado de delimitación de la condición. La ventana acordada está en el contexto; no se añade una condición nueva.
- **Solución propuesta:** expresar la primera ventana como un intervalo continuo desde el inicio de la selección hasta antes de la solicitud de autorización.
- **Redacción alternativa:** «El sistema deberá permitir cancelar la operación desde el inicio de la selección hasta antes de iniciar una solicitud de autorización, o tras recibir una denegación y antes de otro intento.»
- **Pendiente:** confirmar que la cancelación se admite también después de seleccionar la bebida y antes de la solicitud de autorización, tal como indica el criterio de comprobación. Si el equipo quisiera limitarla estrictamente al acto de selección, deberá definirlo.

### INC-OBS-005 — CAF-RF-017

- **Requisito:** CAF-RF-017.
- **Fragmento:** «cuando se haya comprobado su disponibilidad y autorizado el pago».
- **Aspecto:** Condiciones de aplicación (principal) y Verificabilidad.
- **INCOSE aplicable:** R27 – Explicit Conditions (p. 3); C7 – Verifiable (p. 2).
- **Problema:** igual que en INC-OBS-002, «se haya comprobado su disponibilidad» no exige que el resultado sea favorable. El sistema podría iniciar la preparación tras una comprobación que haya detectado falta de disponibilidad, siempre que el pago esté autorizado y no se haya comunicado un fallo. Esto contradice la secuencia documentada y CAF-RF-006.
- **Efecto:** la condición de inicio no determina unívocamente si la disponibilidad debe ser positiva. La pasiva «se haya comprobado» no identifica al agente, pero el sistema es el responsable de la comprobación según CAF-RF-004 y CAF-RF-005; el defecto material es el resultado omitido.
- **Naturaleza:** defecto sustentado de redacción de la condición. La intención está documentada en el contexto.
- **Solución propuesta:** explicitar el resultado favorable de la comprobación y conservar las demás condiciones.
- **Redacción alternativa:** «El sistema deberá iniciar la preparación de la bebida seleccionada cuando se haya comprobado que la bebida seleccionada está disponible y se haya autorizado el pago, siempre que no se haya comunicado un fallo que impida la entrega.»
- **Pendiente:** confirmar que «siempre que no se haya comunicado un fallo» se refiere a un fallo comunicado antes del inicio; el contexto lo interpreta así. No se propone añadir condiciones nuevas.

### INC-OBS-006 — CAF-RF-018

- **Requisito:** CAF-RF-018.
- **Fragmento:** «coordinar la preparación de la bebida seleccionada con las cantidades indicadas en su receta».
- **Aspecto:** Claridad (principal) y Verificabilidad.
- **INCOSE aplicable:** C3 – Unambiguous (p. 2); C7 – Verifiable (p. 2).
- **Problema:** «coordinar» es un verbo amplio que no define por sí mismo una conducta observable: puede significar secuenciar las etapas, sincronizar los mecanismos, comunicar las cantidades o verificar la receta. La frase «con las cantidades indicadas» sugiere que deben usarse esas cantidades, pero el enunciado no afirma que el sistema deba conseguir que se utilicen. El criterio de comprobación interpreta que deben compararse las cantidades indicadas a los mecanismos con la receta; esa interpretación no se deriva de forma única del texto.
- **Efecto:** la verificación depende de una interpretación del verbo. No es un caso de R7: R7 se refiere a cuantificadores y adjetivos vagos, y «coordinar» es un verbo de acción amplio; el problema se sitúa en C3.
- **Naturaleza:** defecto sustentado de claridad. La intención se puede preservar sin prescribir hardware ni medición física.
- **Solución propuesta:** mantener la coordinación como acción del sistema y explicitar el resultado observable: que se utilicen las cantidades de la receta.
- **Redacción alternativa:** «El sistema deberá coordinar la preparación de la bebida seleccionada de modo que se utilicen las cantidades de ingredientes indicadas en su receta.»
- **Pendiente:** si el equipo prefiere conservar «coordinar» sin cambio, deberá definirlo en el glosario con el mismo significado que el criterio de comprobación. La alternativa «controlar la preparación para que se utilicen...» también es posible, pero puede leerse como más prescriptiva; la decisión es del equipo.

### INC-OBS-007 — CAF-RF-020

- **Requisito:** CAF-RF-020.
- **Fragmento:** «El sistema deberá informar al cliente mientras la bebida se esté preparando.»
- **Aspecto:** Claridad (principal) y Verificabilidad.
- **INCOSE aplicable:** C3 – Unambiguous (p. 2); C7 – Verifiable (p. 2); R35 – Temporal Dependencies (p. 3), como apoyo.
- **Problema:** el enunciado no dice qué información debe recibir el cliente ni si el aviso debe ser único o mantenerse durante toda la preparación. La descripción indica que permite distinguir la preparación de la espera del pago, y el criterio de comprobación exige un mensaje de «preparación en curso». Esa es una interpretación posible, pero no la única: «informar mientras» puede cumplirse con un aviso al inicio, con un aviso persistente o con actualizaciones periódicas.
- **Efecto:** no puede determinarse si una sola comunicación satisface el requisito. R35 apoya la necesidad de definir la dependencia temporal del aviso respecto al inicio y al fin de la preparación. No se propone un plazo ni una frecuencia no acordados.
- **Naturaleza:** duda por aclarar. El equipo debe decidir el contenido y la duración del aviso.
- **Solución propuesta:** decidir entre (a) un aviso al iniciar la preparación, (b) un aviso mantenido durante toda la preparación o (c) actualizaciones periódicas. La opción (b) es la más próxima a «mientras», pero no se presume.
- **Redacción alternativa (si se elige b):** «El sistema deberá mostrar al cliente un aviso de que la bebida se está preparando desde el inicio de la preparación hasta su finalización.»
- **Redacción alternativa (si se elige a):** «El sistema deberá informar al cliente de que la bebida se está preparando al iniciar la preparación.»
- **Pendiente:** la elección entre a, b o c y el contenido exacto del aviso. La propuesta queda pendiente de esa decisión.

### INC-OBS-008 — CAF-RF-022

- **Requisito:** CAF-RF-022.
- **Fragmento:** «informar al cliente de que el servicio no se ha completado y de que terminó el despacho sin entrega».
- **Aspecto:** Claridad (principal) y Verificabilidad.
- **INCOSE aplicable:** C3 – Unambiguous (p. 2); R4 – Defined Terms (p. 3); C7 – Verifiable (p. 2).
- **Problema:** «despacho» no está definido en el glosario ni en el contexto. Puede significar la acción de dispensar, la transacción de venta o el servicio. La frase «terminó el despacho sin entrega» se solapa con «el servicio no se ha completado» y resulta próxima a una contradicción: si no hubo entrega, no queda claro qué terminó. Además, el criterio de comprobación solo verifica que se informe de que el servicio no se completó; no comprueba el segundo contenido.
- **Efecto:** el cliente o el verificador no pueden interpretar de forma única el segundo contenido, y este no queda cubierto por la comprobación. No es un problema de singularidad: hay una sola acción de informar con dos contenidos; el defecto es de claridad y verificabilidad del contenido.
- **Naturaleza:** duda por aclarar. El equipo debe decidir si ambos contenidos son obligatorios.
- **Solución propuesta:** si el segundo contenido solo pretende reforzar que no hubo entrega, integrarlo en una sola frase clara y eliminar «despacho». Si se mantiene como mensaje separado, definirlo en el glosario y añadir una comprobación específica.
- **Redacción alternativa (una sola comunicación):** «Si, tras autorizarse el pago, un fallo impide entregar la bebida en cualquier etapa, el sistema deberá informar al cliente de que el servicio no se ha completado porque la bebida no se entregó.»
- **Pendiente:** confirmar si se elimina el segundo contenido o se define «despacho». La alternativa no añade ni elimina condiciones de negocio; solo aclara el contenido.

### INC-OBS-009 — CAF-RF-023

- **Requisito:** CAF-RF-023.
- **Fragmento:** «el sistema deberá solicitar la devolución íntegra del importe asociado al intento autorizado y comunicar al cliente que la devolución fue solicitada».
- **Aspecto:** Singularidad.
- **INCOSE aplicable:** C5 – Singular (p. 2); R18 – Single Thought Sentence (p. 3); R19 – Combinators (p. 3).
- **Problema:** el enunciado contiene dos obligaciones independientes unidas por «y»: (1) solicitar la devolución íntegra del importe asociado al intento autorizado; (2) comunicar al cliente que la devolución fue solicitada. Tienen acciones, destinatarios y evidencias de verificación distintos; una puede cumplirse sin la otra. La condición común de fallo no las convierte en una sola capacidad. R19 señala «and» como conector que puede unir cláusulas independientes.
- **Efecto:** la verificación de la devolución y la del aviso quedan mezcladas. La separación permite comprobar por separado la solicitud económica y la comunicación al cliente.
- **Naturaleza:** defecto sustentado de singularidad. No requiere información nueva; solo separar y repartir descripción y comprobación.
- **Solución propuesta:** separar en dos requisitos, conservando CAF-RF-023 como origen común y la misma condición.
- **Redacción alternativa:**
  - **CAF-RF-023A (provisional):** «Si, tras autorizarse el pago, un fallo impide entregar la bebida, el sistema deberá solicitar la devolución íntegra del importe asociado al intento autorizado.»
  - **CAF-RF-023B (provisional):** «Si, tras autorizarse el pago, un fallo impide entregar la bebida, el sistema deberá comunicar al cliente que la devolución fue solicitada.»
- **Pendiente:** el equipo debe aceptar la separación y decidir si CAF-RF-023B debe decir «una vez solicitada la devolución» para hacer explícita la secuencia. No se propone añadir un plazo ni afirmar que el reintegro ya se produjo; el procesamiento bancario sigue fuera del alcance.

## 6. Matriz completa de evaluación de la base v2

**Leyenda de valoración:** «Sin problema detectado» = no se detecta un incumplimiento material en el aspecto; «Observación propuesta» = defecto de redacción sustentado, con propuesta de mejora; «Requiere aclaración» = falta una decisión o precisión del equipo para poder cerrar la evaluación; «No aplica» = el aspecto no tiene contenido que evaluar en ese enunciado (por ejemplo, no hay condiciones de aplicación).

**Limitaciones globales citadas:** L1 = R1 no verificable por ausencia de patrón acordado; L2 = glosario no exhaustivo, solo se observan términos materiales; L3 = no se consultó la guía completa de INCOSE; L4 = no se ejecutaron pruebas, los criterios son planes.

| ID | Aspecto | Reglas/características | Valoración | Justificación | Obs. |
| --- | --- | --- | --- | --- | --- |
| CAF-RF-001 | Singularidad | C5; R18; R19 | Sin problema detectado | Una sola acción (mostrar) con tres datos de la misma bebida; la enumeración no crea obligaciones independientes. | — |
| CAF-RF-001 | Claridad | C3; R4; R8; R24 | Sin problema detectado | «Disponibilidad» está definida en el contexto; «catálogo» y «precio» se concretan en el catálogo del apartado 3; no hay pronombres ni cláusulas de escape. | — |
| CAF-RF-001 | Estructura gramatical | R1; R12; R2; R3 | Sin problema detectado | Oración completa, sujeto «El sistema», verbo «deberá mostrar» y complementos claros; R1 no verificable por L1. | — |
| CAF-RF-001 | Términos subjetivos | R7 | Sin problema detectado | «Cada» es universal y «disponibilidad» está acotada; no hay cuantificadores o adjetivos vagos. | — |
| CAF-RF-001 | Condiciones de aplicación | R27; R28; R11 | Sin problema detectado | La condición temporal «antes de que el cliente la seleccione» es explícita y única. | — |
| CAF-RF-001 | Verificabilidad | C7; R33; R34; R35 | Sin problema detectado | Se comprueba mostrando las seis bebidas y los estados de disponibilidad; no hay metas numéricas de rendimiento (R33/R34 no aplican) y la dependencia temporal está definida. | — |
| CAF-RF-002 | Singularidad | C5; R18; R19 | Sin problema detectado | Una sola acción (permitir seleccionar) con la cardinalidad «por operación de compra». | — |
| CAF-RF-002 | Claridad | C3; R4; R8; R24 | Sin problema detectado | «Bebida disponible» y «operación de compra» se interpretan con el contexto y la descripción; una bebida por compra está declarado. | — |
| CAF-RF-002 | Estructura gramatical | R1; R12; R2; R3 | Sin problema detectado | Oración completa; sujeto y verbo adecuados; R1 no verificable por L1. | — |
| CAF-RF-002 | Términos subjetivos | R7 | Sin problema detectado | «Disponible» está definido; «una» no es vago. | — |
| CAF-RF-002 | Condiciones de aplicación | R27; R28; R11 | Sin problema detectado | «Por operación de compra» explicita la aplicabilidad y la cardinalidad; no hay condición adicional. | — |
| CAF-RF-002 | Verificabilidad | C7; R33; R34; R35 | Sin problema detectado | La prueba selecciona un cortado y comprueba la asociación; no hay magnitudes ni dependencias temporales que exijan R33/R34/R35. | — |
| CAF-RF-003 | Singularidad | C5; R18; R19 | Sin problema detectado | Una sola acción (permitir seleccionar otra sin cancelación) bajo una condición. | — |
| CAF-RF-003 | Claridad | C3; R4; R8; R24 | Requiere aclaración | El enunciado solo cubre el caso de no disponibilidad; la regla complementaria de la descripción y la prueba no está en el texto. | INC-OBS-001 |
| CAF-RF-003 | Estructura gramatical | R1; R12; R2; R3 | Sin problema detectado | Oración condicional completa; sujeto y verbo adecuados; el defecto es de alcance, no gramatical; R1 no verificable por L1. | — |
| CAF-RF-003 | Términos subjetivos | R7 | Sin problema detectado | «Disponible» está definido; «otra» y «previa» no son vagos. | — |
| CAF-RF-003 | Condiciones de aplicación | R27; R28; R11 | Requiere aclaración | La condición «si no está disponible» es explícita, pero el límite con los «demás casos» queda fuera del enunciado y el criterio prueba comportamientos no incluidos. | INC-OBS-001 |
| CAF-RF-003 | Verificabilidad | C7; R33; R34; R35 | Requiere aclaración | El caso enunciado es verificable, pero el criterio incluye cambio con bebida disponible y estados de autorización que no se derivan del texto; debe aclararse el alcance. | INC-OBS-001 |
| CAF-RF-004 | Singularidad | C5; R18; R19 | Sin problema detectado | Una sola comprobación para todos los ingredientes requeridos; «cada» no multiplica la obligación. | — |
| CAF-RF-004 | Claridad | C3; R4; R8; R24 | Sin problema detectado | «Existencias», «ingrediente requerido» y «receta» se concretan en el contexto; «alcanzan» significa al menos la cantidad de la receta y la prueba aclara la igualdad. | — |
| CAF-RF-004 | Estructura gramatical | R1; R12; R2; R3 | Sin problema detectado | Oración completa con subordinada sustantiva; sujeto y verbo adecuados; R1 no verificable por L1. | — |
| CAF-RF-004 | Términos subjetivos | R7 | Sin problema detectado | «Cada» es universal; no hay adjetivos vagos. | — |
| CAF-RF-004 | Condiciones de aplicación | R27; R28; R11 | Sin problema detectado | «Antes de solicitar el pago» es una condición temporal explícita; «según su receta» califica la comprobación. | — |
| CAF-RF-004 | Verificabilidad | C7; R33; R34; R35 | Sin problema detectado | Las cantidades de la receta fijan el umbral; la prueba cubre igualdad y defecto en cada ingrediente. R33 se satisface con la receta; R34 no aplica y R35 está explícita. | — |
| CAF-RF-005 | Singularidad | C5; R18; R19 | Sin problema detectado | Una sola comprobación (existencia de al menos un vaso). | — |
| CAF-RF-005 | Claridad | C3; R4; R8; R24 | Sin problema detectado | «Al menos un vaso» es una cantidad mínima explícita; «vaso» se usa de forma consistente en el contexto. | — |
| CAF-RF-005 | Estructura gramatical | R1; R12; R2; R3 | Sin problema detectado | Oración completa; sujeto y verbo adecuados; R1 no verificable por L1. | — |
| CAF-RF-005 | Términos subjetivos | R7 | Sin problema detectado | «Al menos un» es un cuantificador explícito, no vago. | — |
| CAF-RF-005 | Condiciones de aplicación | R27; R28; R11 | Sin problema detectado | «Antes de solicitar el pago» es explícita. | — |
| CAF-RF-005 | Verificabilidad | C7; R33; R34; R35 | Sin problema detectado | La prueba cubre cero y un vaso; R33 tiene cota inferior explícita; R34/R35 no aplican. | — |
| CAF-RF-006 | Singularidad | C5; R18; R19 | Sin problema detectado | Una sola prohibición con dos causas alternativas para la misma acción. | — |
| CAF-RF-006 | Claridad | C3; R4; R8; R24 | Sin problema detectado | «Faltan ingredientes o vasos para preparar» se interpreta como insuficiencia según la disponibilidad definida; no hay pronombres ni escape. | — |
| CAF-RF-006 | Estructura gramatical | R1; R12; R2; R3 | Sin problema detectado | Oración completa; sujeto y verbo adecuados; R1 no verificable por L1. | — |
| CAF-RF-006 | Términos subjetivos | R7 | Sin problema detectado | «Faltan» se acota por «para preparar la bebida»; no hay término vago. | — |
| CAF-RF-006 | Condiciones de aplicación | R27; R28; R11 | Sin problema detectado | La condición es explícita; el «o» no cambia la prohibición porque ambas causas conducen a ella. | — |
| CAF-RF-006 | Verificabilidad | C7; R33; R34; R35 | Sin problema detectado | La prueba verifica ingredientes y vasos por separado; no hay métricas ni dependencias temporales adicionales. | — |
| CAF-RF-007 | Singularidad | C5; R18; R19 | Sin problema detectado | Una sola acción de informar, con dos causas de indisponibilidad. | — |
| CAF-RF-007 | Claridad | C3; R4; R8; R24 | Sin problema detectado | El contenido del aviso se acota por la condición y la descripción (aviso genérico, sin detallar el recurso). | — |
| CAF-RF-007 | Estructura gramatical | R1; R12; R2; R3 | Sin problema detectado | Oración completa; sujeto y verbo adecuados; R1 no verificable por L1. | — |
| CAF-RF-007 | Términos subjetivos | R7 | Sin problema detectado | «Genérico» está en la descripción, no en el enunciado; no hay vaguedad en el texto. | — |
| CAF-RF-007 | Condiciones de aplicación | R27; R28; R11 | Sin problema detectado | «Cuando ... no esté disponible por falta de ingredientes o vasos» es explícita. | — |
| CAF-RF-007 | Verificabilidad | C7; R33; R34; R35 | Sin problema detectado | La prueba cubre ambas causas y el aviso genérico; no hay magnitudes ni dependencias temporales que exijan R33/R34/R35. | — |
| CAF-RF-008 | Singularidad | C5; R18; R19 | Sin problema detectado | Una sola acción (descontar) con dos desenlaces para la misma preparación. | — |
| CAF-RF-008 | Claridad | C3; R4; R8; R24 | Sin problema detectado | «Realmente consumidas» se define por las cantidades comunicadas por los mecanismos en el contexto; «al finalizar» se refiere al fin de la preparación, con éxito o fallo. | — |
| CAF-RF-008 | Estructura gramatical | R1; R12; R2; R3 | Sin problema detectado | Oración completa; sujeto y verbo adecuados; «se completa» tiene como antecedente «una preparación»; R1 no verificable por L1. | — |
| CAF-RF-008 | Términos subjetivos | R7 | Sin problema detectado | «Realmente» remite a cantidades comunicadas; no es un cuantificador vago. | — |
| CAF-RF-008 | Condiciones de aplicación | R27; R28; R11 | Sin problema detectado | «Al finalizar ... tanto si se completa como si falla» explicita los casos; no hay condición implícita. | — |
| CAF-RF-008 | Verificabilidad | C7; R33; R34; R35 | Sin problema detectado | La prueba usa cantidades concretas y un fallo parcial; R33/R34 no aplican y R35 está definida por el evento de finalización. | — |
| CAF-RF-009 | Singularidad | C5; R18; R19 | Sin problema detectado | Una sola acción (descontar vasos) con la concesión de fallo. | — |
| CAF-RF-009 | Claridad | C3; R4; R8; R24 | Sin problema detectado | «Vasos realmente consumidos» se concreta con la cantidad comunicada por los mecanismos; el plural no impone un número distinto de uno. | — |
| CAF-RF-009 | Estructura gramatical | R1; R12; R2; R3 | Sin problema detectado | Oración completa; sujeto y verbo adecuados; R1 no verificable por L1. | — |
| CAF-RF-009 | Términos subjetivos | R7 | Sin problema detectado | «Realmente» no es vago en este contexto; no hay adjetivos evaluativos. | — |
| CAF-RF-009 | Condiciones de aplicación | R27; R28; R11 | Sin problema detectado | «Durante una preparación, aunque un fallo impida entregar» explicita el marco y la concesión. | — |
| CAF-RF-009 | Verificabilidad | C7; R33; R34; R35 | Sin problema detectado | La prueba cubre éxito, fallo con consumo y fallo sin consumo; R33/R34/R35 no añaden requisitos. | — |
| CAF-RF-010 | Singularidad | C5; R18; R19 | Sin problema detectado | Una sola acción (solicitar autorización) con precio y condición. | — |
| CAF-RF-010 | Claridad | C3; R4; R8; R24 | Sin problema detectado | «Su» tiene antecedente inmediato («bebida seleccionada») y el contexto lo confirma; no se fuerza R24. La ambigüedad de la condición se trata en Condiciones. | — |
| CAF-RF-010 | Estructura gramatical | R1; R12; R2; R3 | Sin problema detectado | Oración completa; obligación en voz activa; la subordinada pasiva «una vez comprobada» no cambia el sujeto responsable; R1 no verificable por L1. | — |
| CAF-RF-010 | Términos subjetivos | R7 | Sin problema detectado | «Precio» se concreta en el catálogo; no hay término vago. | — |
| CAF-RF-010 | Condiciones de aplicación | R27; R28; R11 | Observación propuesta | «Una vez comprobada su disponibilidad» dice que se hizo la comprobación, no que el resultado fuera favorable; debe explicitarse el resultado positivo. | INC-OBS-002 |
| CAF-RF-010 | Verificabilidad | C7; R33; R34; R35 | Observación propuesta | La prueba asume disponibilidad positiva; con el texto actual la condición no determina unívocamente cuándo solicitar el pago. R33/R34 no aplican y R35 es explícita. | INC-OBS-002 |
| CAF-RF-011 | Singularidad | C5; R18; R19 | Sin problema detectado | Una sola prohibición (impedir inicio) con dos condiciones alternativas. | — |
| CAF-RF-011 | Claridad | C3; R4; R8; R24 | Sin problema detectado | «Terminal», «autorización» y «fallo que impide la entrega» se definen en el contexto; no hay pronombres oscuros ni escape vago. | — |
| CAF-RF-011 | Estructura gramatical | R1; R12; R2; R3 | Sin problema detectado | Oración completa; sujeto «El sistema» y verbo «deberá impedir»; la pasiva «se ha comunicado» describe un evento cuyo emisor es la máquina en el contexto; R1 no verificable por L1. | — |
| CAF-RF-011 | Términos subjetivos | R7 | Sin problema detectado | «No haya autorizado» y «fallo» están acotados; no hay cuantificadores vagos. | — |
| CAF-RF-011 | Condiciones de aplicación | R27; R28; R11 | Sin problema detectado | Las dos condiciones y su relación disyuntiva son explícitas; no se requiere añadir condiciones de negocio. | — |
| CAF-RF-011 | Verificabilidad | C7; R33; R34; R35 | Sin problema detectado | La prueba cubre pendiente, denegación y fallo tras autorización; no hay magnitudes ni dependencia temporal indefinida. | — |
| CAF-RF-012 | Singularidad | C5; R18; R19 | Sin problema detectado | Una sola acción de informar. | — |
| CAF-RF-012 | Claridad | C3; R4; R8; R24 | Sin problema detectado | «Deniegue el pago» se define por el resultado del terminal; no hay términos oscuros. | — |
| CAF-RF-012 | Estructura gramatical | R1; R12; R2; R3 | Sin problema detectado | Oración completa; sujeto y verbo adecuados; R1 no verificable por L1. | — |
| CAF-RF-012 | Términos subjetivos | R7 | Sin problema detectado | No hay términos subjetivos. | — |
| CAF-RF-012 | Condiciones de aplicación | R27; R28; R11 | Sin problema detectado | «Cuando el terminal deniegue el pago» es explícita. | — |
| CAF-RF-012 | Verificabilidad | C7; R33; R34; R35 | Sin problema detectado | La prueba provoca una denegación y comprueba el mensaje; R33/R34/R35 no aplican. | — |
| CAF-RF-013 | Singularidad | C5; R18; R19 | Sin problema detectado | Una sola capacidad (reintentar) con una restricción cuantitativa (sin máximo). | — |
| CAF-RF-013 | Claridad | C3; R4; R8; R24 | Sin problema detectado | «Reintentar el pago» se refiere al pago denegado; la descripción aclara que es para la misma bebida o cancelar; no hay ambigüedad material. | — |
| CAF-RF-013 | Estructura gramatical | R1; R12; R2; R3 | Sin problema detectado | Oración completa; sujeto y verbo adecuados; R1 no verificable por L1. | — |
| CAF-RF-013 | Términos subjetivos | R7 | Sin problema detectado | «Sin imponer un número máximo» es una prohibición precisa, no un término vago. | — |
| CAF-RF-013 | Condiciones de aplicación | R27; R28; R11 | Sin problema detectado | «Después de cada denegación» es explícita; la restricción «sin máximo» califica la misma acción. | — |
| CAF-RF-013 | Verificabilidad | C7; R33; R34; R35 | Sin problema detectado | Es verificable mediante intentos repetidos y revisión de diseño/configuración; C7 no exige prueba exhaustiva. R34 no aplica y R35 está definida. | — |
| CAF-RF-015 | Singularidad | C5; R18; R19 | Observación propuesta | Dos obligaciones independientes unidas por «y»: asociar resultados y vincular devoluciones. | INC-OBS-003 |
| CAF-RF-015 | Claridad | C3; R4; R8; R24 | Sin problema detectado | Los términos «resultado de autorización», «intento de pago» y «solicitud de devolución» se interpretan con el contexto; la descripción no impone un componente. | — |
| CAF-RF-015 | Estructura gramatical | R1; R12; R2; R3 | Sin problema detectado | Oración gramatical completa; el predicado compuesto no es un error de R12; la separación se propone por C5/R18/R19; R1 no verificable por L1. | — |
| CAF-RF-015 | Términos subjetivos | R7 | Sin problema detectado | No hay cuantificadores o adjetivos vagos; «cada» es universal. | — |
| CAF-RF-015 | Condiciones de aplicación | R27; R28; R11 | No aplica | No establece condiciones de aplicación; «intento autorizado que la origina» es una relación, no una condición. | — |
| CAF-RF-015 | Verificabilidad | C7; R33; R34; R35 | Sin problema detectado | La prueba diferencia denegación y autorización y comprueba la devolución; es verificable, aunque la separación mejora la trazabilidad. | — |
| CAF-RF-014 | Singularidad | C5; R18; R19 | Sin problema detectado | Una sola acción (permitir cancelar) con dos ventanas temporales. | — |
| CAF-RF-014 | Claridad | C3; R4; R8; R24 | Observación propuesta | La primera ventana «durante la selección y antes de iniciar...» puede leerse como dos condiciones acumulativas y no define el límite tras seleccionar. | INC-OBS-004 |
| CAF-RF-014 | Estructura gramatical | R1; R12; R2; R3 | Sin problema detectado | Oración completa; sujeto y verbo adecuados; R1 no verificable por L1. | — |
| CAF-RF-014 | Términos subjetivos | R7 | Sin problema detectado | No hay términos subjetivos; las ventanas se refieren a eventos concretos. | — |
| CAF-RF-014 | Condiciones de aplicación | R27; R28; R11 | Observación propuesta | La relación «y» dentro de la primera ventana y el «o» entre ventanas no quedan unívocamente expresados; R27/R28/R11 piden explicitarla. | INC-OBS-004 |
| CAF-RF-014 | Verificabilidad | C7; R33; R34; R35 | Observación propuesta | La prueba exige cancelar antes de solicitar autorización, pero el texto puede no cubrir el intervalo posterior a la selección; la verificación no es única. | INC-OBS-004 |
| CAF-RF-016 | Singularidad | C5; R18; R19 | Sin problema detectado | Una sola prohibición (impedir cancelar) con dos condiciones. | — |
| CAF-RF-016 | Claridad | C3; R4; R8; R24 | Sin problema detectado | «Solicitud pendiente» y «pago autorizado» se definen en el contexto; no hay pronombres ni escape. | — |
| CAF-RF-016 | Estructura gramatical | R1; R12; R2; R3 | Sin problema detectado | Oración completa; sujeto y verbo adecuados; R1 no verificable por L1. | — |
| CAF-RF-016 | Términos subjetivos | R7 | Sin problema detectado | No hay términos vagos. | — |
| CAF-RF-016 | Condiciones de aplicación | R27; R28; R11 | Sin problema detectado | Las dos condiciones y su relación disyuntiva son explícitas. | — |
| CAF-RF-016 | Verificabilidad | C7; R33; R34; R35 | Sin problema detectado | La prueba cubre pendiente, autorización previa, durante la preparación y bebida lista; no hay magnitudes ni dependencia temporal indefinida. | — |
| CAF-RF-017 | Singularidad | C5; R18; R19 | Sin problema detectado | Una sola acción (iniciar preparación) con tres condiciones. | — |
| CAF-RF-017 | Claridad | C3; R4; R8; R24 | Sin problema detectado | «Su disponibilidad» tiene antecedente claro; la ambigüedad del resultado de la comprobación se trata en Condiciones. | — |
| CAF-RF-017 | Estructura gramatical | R1; R12; R2; R3 | Sin problema detectado | Oración completa; obligación activa; las pasivas de las condiciones no ocultan al sujeto responsable; R1 no verificable por L1. | — |
| CAF-RF-017 | Términos subjetivos | R7 | Sin problema detectado | «Siempre que» introduce una condición específica, no una cláusula de escape vaga; no hay términos subjetivos. | — |
| CAF-RF-017 | Condiciones de aplicación | R27; R28; R11 | Observación propuesta | «Se haya comprobado su disponibilidad» no exige que el resultado sea favorable; debe explicitarse para no permitir el inicio tras una comprobación negativa. | INC-OBS-005 |
| CAF-RF-017 | Verificabilidad | C7; R33; R34; R35 | Observación propuesta | La prueba asume disponibilidad positiva; la condición actual no determina unívocamente el inicio. R33/R34 no aplican y R35 está definida. | INC-OBS-005 |
| CAF-RF-018 | Singularidad | C5; R18; R19 | Sin problema detectado | Una sola acción (coordinar la preparación). | — |
| CAF-RF-018 | Claridad | C3; R4; R8; R24 | Observación propuesta | «Coordinar ... con las cantidades» no define una conducta observable única; puede significar secuenciar, comunicar o verificar cantidades. | INC-OBS-006 |
| CAF-RF-018 | Estructura gramatical | R1; R12; R2; R3 | Sin problema detectado | Oración completa; «coordinar» es un verbo transitivo adecuado al sujeto; la ambigüedad es de C3, no de R12; R1 no verificable por L1. | — |
| CAF-RF-018 | Términos subjetivos | R7 | Sin problema detectado | No hay cuantificadores o adjetivos vagos de R7; «coordinar» es un verbo amplio y se evalúa en Claridad. | — |
| CAF-RF-018 | Condiciones de aplicación | R27; R28; R11 | No aplica | No establece condiciones de aplicación; la remisión a la receta es una referencia, no una condición. | — |
| CAF-RF-018 | Verificabilidad | C7; R33; R34; R35 | Observación propuesta | El criterio de prueba compara cantidades enviadas a los mecanismos, interpretación que no se deriva unívocamente del enunciado; la verificación depende de aclarar «coordinar». | INC-OBS-006 |
| CAF-RF-019 | Singularidad | C5; R18; R19 | Sin problema detectado | Una sola acción (ordenar la dispensación de un vaso). | — |
| CAF-RF-019 | Claridad | C3; R4; R8; R24 | Sin problema detectado | «Un vaso» y «bebida preparada» se entienden con el contexto; el propósito no crea ambigüedad material. | — |
| CAF-RF-019 | Estructura gramatical | R1; R12; R2; R3 | Sin problema detectado | Oración completa; sujeto y verbo adecuados; R1 no verificable por L1. | — |
| CAF-RF-019 | Términos subjetivos | R7 | Sin problema detectado | No hay términos subjetivos. | — |
| CAF-RF-019 | Condiciones de aplicación | R27; R28; R11 | No aplica | No establece una condición de aplicación; «para entregar la bebida preparada» es una finalidad, no una condición. | — |
| CAF-RF-019 | Verificabilidad | C7; R33; R34; R35 | Sin problema detectado | La prueba completa una compra y comprueba la orden de dispensación; no hay magnitudes ni dependencias temporales que exijan R33/R34/R35. | — |
| CAF-RF-020 | Singularidad | C5; R18; R19 | Sin problema detectado | Una sola acción (informar) durante la preparación. | — |
| CAF-RF-020 | Claridad | C3; R4; R8; R24 | Requiere aclaración | No se especifica qué información debe recibir el cliente ni si el aviso debe ser único o mantenerse durante toda la preparación. | INC-OBS-007 |
| CAF-RF-020 | Estructura gramatical | R1; R12; R2; R3 | Sin problema detectado | Oración completa; «mientras» introduce una subordinada temporal; el problema es de contenido y duración, no de gramática; R1 no verificable por L1. | — |
| CAF-RF-020 | Términos subjetivos | R7 | Sin problema detectado | No hay cuantificadores o adjetivos vagos de R7; «mientras» es temporal y se evalúa en Claridad/Verificabilidad. | — |
| CAF-RF-020 | Condiciones de aplicación | R27; R28; R11 | Sin problema detectado | La condición temporal «mientras la bebida se esté preparando» está enunciada; la falta de contenido y duración se trata en la observación. | INC-OBS-007 |
| CAF-RF-020 | Verificabilidad | C7; R33; R34; R35 | Requiere aclaración | No puede determinarse si una sola comunicación al inicio satisface «mientras» o si se exige un aviso continuo; R35 apoya la necesidad de definir la dependencia temporal. | INC-OBS-007 |
| CAF-RF-021 | Singularidad | C5; R18; R19 | Sin problema detectado | Una sola acción (avisar) condicionada por la finalización correcta de preparación y entrega. | — |
| CAF-RF-021 | Claridad | C3; R4; R8; R24 | Sin problema detectado | «Correctamente» se interpreta con el contexto como ausencia de fallo que impida la entrega; «confirmarse» se refiere a la información disponible de la máquina, sin prescribir sensor. No hay R4/R8/R24 material. | — |
| CAF-RF-021 | Estructura gramatical | R1; R12; R2; R3 | Sin problema detectado | Oración completa; obligación activa; la subordinada pasiva no cambia el sujeto responsable; R1 no verificable por L1. | — |
| CAF-RF-021 | Términos subjetivos | R7 | Sin problema detectado | «Correctamente» está acotado por el contexto (preparación y entrega sin fallo que impida entregar); no se detecta vaguedad material bajo R7. | — |
| CAF-RF-021 | Condiciones de aplicación | R27; R28; R11 | Sin problema detectado | La condición «cuando ... después de confirmarse que ... terminaron correctamente» es explícita; el «y» exige ambos resultados. | — |
| CAF-RF-021 | Verificabilidad | C7; R33; R34; R35 | Sin problema detectado | La prueba comunica finalización correcta y fallo; R35 está definida por el evento de confirmación; no hay magnitudes que exijan R33/R34. | — |
| CAF-RF-022 | Singularidad | C5; R18; R19 | Sin problema detectado | Una sola acción de informar con dos contenidos; no son dos acciones independientes. | — |
| CAF-RF-022 | Claridad | C3; R4; R8; R24 | Requiere aclaración | «Despacho» no está definido y la segunda frase se solapa con «servicio no completado»; el criterio solo comprueba la primera. | INC-OBS-008 |
| CAF-RF-022 | Estructura gramatical | R1; R12; R2; R3 | Sin problema detectado | Oración completa; «y de que» coordina contenidos, no predicados independientes; R1 no verificable por L1. | — |
| CAF-RF-022 | Términos subjetivos | R7 | Sin problema detectado | «Cualquier etapa» es una cuantificación universal acotada por «tras autorizarse el pago» y «que impida entregar»; el problema es «despacho» en Claridad. | — |
| CAF-RF-022 | Condiciones de aplicación | R27; R28; R11 | Sin problema detectado | La condición «si, tras autorizarse el pago, un fallo impide entregar ... en cualquier etapa» es explícita; el alcance de etapas se acota por el contexto. | — |
| CAF-RF-022 | Verificabilidad | C7; R33; R34; R35 | Requiere aclaración | El segundo contenido no se verifica en el criterio y su término es ambiguo; la verificación completa depende de definir «despacho» o eliminarlo. | INC-OBS-008 |
| CAF-RF-023 | Singularidad | C5; R18; R19 | Observación propuesta | Dos obligaciones independientes unidas por «y»: solicitar la devolución y comunicar al cliente. | INC-OBS-009 |
| CAF-RF-023 | Claridad | C3; R4; R8; R24 | Sin problema detectado | «Devolución íntegra», «importe» e «intento autorizado» se entienden con el contexto; no hay término oscuro. | — |
| CAF-RF-023 | Estructura gramatical | R1; R12; R2; R3 | Sin problema detectado | Oración completa; el predicado compuesto no es un error de R12; la separación se propone por C5/R18/R19; R1 no verificable por L1. | — |
| CAF-RF-023 | Términos subjetivos | R7 | Sin problema detectado | «Íntegra» está acotada por el importe del intento autorizado; no es vaga. | — |
| CAF-RF-023 | Condiciones de aplicación | R27; R28; R11 | Sin problema detectado | La condición «si, tras autorizarse el pago, un fallo impide entregar» es explícita. | — |
| CAF-RF-023 | Verificabilidad | C7; R33; R34; R35 | Sin problema detectado | La prueba comprueba importe, intento y aviso; es verificable; la separación mejora la trazabilidad. | — |
| CAF-RF-024 | Singularidad | C5; R18; R19 | Sin problema detectado | Una sola acción (terminar la operación) con una prohibición de inicio automático. | — |
| CAF-RF-024 | Claridad | C3; R4; R8; R24 | Sin problema detectado | «Terminar la operación» se concreta por la descripción y la prueba (no iniciar otra preparación o compra); no prescribe estado interno. | — |
| CAF-RF-024 | Estructura gramatical | R1; R12; R2; R3 | Sin problema detectado | Oración completa; sujeto y verbo adecuados; R1 no verificable por L1. | — |
| CAF-RF-024 | Términos subjetivos | R7 | Sin problema detectado | «Automáticamente» se entiende como sin una nueva operación del cliente; no es un término vago en este contexto. | — |
| CAF-RF-024 | Condiciones de aplicación | R27; R28; R11 | Sin problema detectado | La condición «si un fallo impide entregar una bebida cuyo pago fue autorizado» es explícita. | — |
| CAF-RF-024 | Verificabilidad | C7; R33; R34; R35 | Sin problema detectado | La prueba provoca fallos en distintas etapas y comprueba que no se inicia otra preparación o compra; no hay magnitudes ni dependencia temporal que exijan R33/R34/R35. | — |
| CAF-RNF-001 | Singularidad | C5; R18; R19 | Sin problema detectado | Una sola cualidad (idioma de los textos). | — |
| CAF-RNF-001 | Claridad | C3; R4; R8; R24 | Sin problema detectado | «Textos dirigidos al cliente» se acota por la interfaz y la descripción; «español» es inequívoco. | — |
| CAF-RNF-001 | Estructura gramatical | R1; R12; R2; R3 | Sin problema detectado | Oración completa; sujeto y verbo adecuados; R1 no verificable por L1. | — |
| CAF-RNF-001 | Términos subjetivos | R7 | Sin problema detectado | No hay términos subjetivos. | — |
| CAF-RNF-001 | Condiciones de aplicación | R27; R28; R11 | No aplica | No establece condiciones; es una cualidad aplicable a todos los textos dirigidos al cliente. | — |
| CAF-RNF-001 | Verificabilidad | C7; R33; R34; R35 | Sin problema detectado | Se verifica recorriendo los flujos y comprobando los textos; C7 no exige métricas. R33/R34/R35 no aplican. | — |
| CAF-RNF-002 | Singularidad | C5; R18; R19 | Sin problema detectado | Una sola cualidad (manejo exacto de importes) aplicada a pago y devolución. | — |
| CAF-RNF-002 | Claridad | C3; R4; R8; R24 | Sin problema detectado | «Céntimos exactos» y «sin errores de redondeo respecto a los precios del catálogo» son criterios precisos; la devolución se vincula al pago autorizado. | — |
| CAF-RNF-002 | Estructura gramatical | R1; R12; R2; R3 | Sin problema detectado | Oración completa; sujeto y verbo adecuados; R1 no verificable por L1. | — |
| CAF-RNF-002 | Términos subjetivos | R7 | Sin problema detectado | «Exactos» cuantifica precisión, no vaguedad; no hay adjetivos evaluativos. | — |
| CAF-RNF-002 | Condiciones de aplicación | R27; R28; R11 | No aplica | No establece condiciones; es una cualidad aplicable a todos los importes de pago y devolución. | — |
| CAF-RNF-002 | Verificabilidad | C7; R33; R34; R35 | Sin problema detectado | Se verifica comparando importes transmitidos con el catálogo en céntimos; R33/R34 aportan la unidad y la precisión; no se requiere tolerancia adicional. | — |

## 7. Trazabilidad de las observaciones

| Observación | Requisito | Aspecto(s) | Tipo | Propuesta |
| --- | --- | --- | --- | --- |
| INC-OBS-001 | CAF-RF-003 | Condiciones, Claridad, Verificabilidad | Requiere aclaración | Mantener CAF-RF-003 y separar la regla de cambio con bebida disponible en CAF-RF-003A. |
| INC-OBS-002 | CAF-RF-010 | Condiciones, Verificabilidad | Observación propuesta | Explicitar que la disponibilidad comprobada debe ser positiva. |
| INC-OBS-003 | CAF-RF-015 | Singularidad | Observación propuesta | Separar en CAF-RF-015A (asociar resultado e intento) y CAF-RF-015B (vincular devolución e intento autorizado). |
| INC-OBS-004 | CAF-RF-014 | Condiciones, Claridad, Verificabilidad | Observación propuesta | Expresar la ventana como intervalo continuo desde el inicio de la selección hasta antes de la autorización. |
| INC-OBS-005 | CAF-RF-017 | Condiciones, Verificabilidad | Observación propuesta | Explicitar que la disponibilidad comprobada debe ser positiva antes de iniciar la preparación. |
| INC-OBS-006 | CAF-RF-018 | Claridad, Verificabilidad | Observación propuesta | Precisar «coordinar» con un resultado observable: que se utilicen las cantidades de la receta. |
| INC-OBS-007 | CAF-RF-020 | Claridad, Verificabilidad | Requiere aclaración | Decidir contenido y duración del aviso: único al inicio, mantenido o periódico. |
| INC-OBS-008 | CAF-RF-022 | Claridad, Verificabilidad | Requiere aclaración | Definir «despacho» o eliminar el segundo contenido y dejar una comunicación clara. |
| INC-OBS-009 | CAF-RF-023 | Singularidad | Observación propuesta | Separar en CAF-RF-023A (solicitar devolución) y CAF-RF-023B (comunicar al cliente). |

## 8. Resumen de hallazgos y cuestiones pendientes

### 8.1. Recuento

- **Requisitos evaluados:** 24 funcionales y 2 no funcionales.
- **Valoraciones:** 156 (26 requisitos × 6 aspectos).
- **Observaciones únicas:** 9.
  - **Observación propuesta:** 6 (INC-OBS-002, 003, 004, 005, 006 y 009).
  - **Requiere aclaración:** 3 (INC-OBS-001, 007 y 008).
- **Incidencias por aspecto** (una observación puede afectar a varios):
  - Singularidad: 2 (CAF-RF-015 y CAF-RF-023).
  - Claridad: 5 (CAF-RF-003, 014, 018, 020 y 022).
  - Estructura gramatical: 0; se mantiene la limitación global L1 sobre R1.
  - Términos subjetivos: 0. Se revisaron especialmente «correctamente» (CAF-RF-021), «cualquier etapa» (CAF-RF-022), «realmente» (CAF-RF-008 y 009), «íntegra» (CAF-RF-023) y «exactos» (CAF-RNF-002); el contexto los acota y no se ha considerado procedente forzar una observación por R7.
  - Condiciones de aplicación: 4 (CAF-RF-003, 010, 014 y 017).
  - Verificabilidad: 7 (CAF-RF-003, 010, 014, 017, 018, 020 y 022).

### 8.2. Hallazgos principales

1. **Dos requisitos contienen dos obligaciones independientes:** CAF-RF-015 y CAF-RF-023. Se propone separarlos y conservar la relación de origen mediante IDs provisionales.
2. **Cuatro requisitos tienen condiciones de aplicación que deben precisarse:** CAF-RF-003 (alcance de la regla de cambio), CAF-RF-010 y CAF-RF-017 (resultado positivo de la comprobación de disponibilidad) y CAF-RF-014 (límite de la ventana de cancelación).
3. **Tres requisitos presentan ambigüedad de contenido o de término:** CAF-RF-018 («coordinar»), CAF-RF-020 (qué se informa y durante cuánto tiempo) y CAF-RF-022 («despacho» y contenido duplicado).
4. **No se detectan defectos de estructura gramatical R12/R2/R3** en los enunciados. No se declara conformidad con R1 porque no hay patrón formal documentado y acordado; esta es una limitación del proyecto, no un incumplimiento demostrado de los requisitos.
5. **No se detectan términos subjetivos R7 que dejen el alcance sin criterio**, una vez interpretados con el contexto. Esto no significa que el glosario sea exhaustivo; L2 sigue siendo una limitación.

### 8.3. Cuestiones que requieren aclaración o decisión del equipo

1. **CAF-RF-003:** decidir si la regla de cambio de bebida cuando la bebida está disponible se incorpora a CAF-RF-003 o se separa en CAF-RF-003A. Confirmar la redacción propuesta.
2. **CAF-RF-010 y CAF-RF-017:** confirmar que «comprobada la disponibilidad» significa «comprobado que está disponible» y aceptar la redacción que explicita el resultado positivo.
3. **CAF-RF-014:** confirmar que la cancelación se admite desde el inicio de la selección hasta antes de la solicitud de autorización, incluido el intervalo posterior a la selección. Aceptar o ajustar la redacción propuesta.
4. **CAF-RF-015 y CAF-RF-023:** decidir si se acepta la separación en dos requisitos y si se conservan los IDs provisionales, descripciones y comprobaciones propuestos.
5. **CAF-RF-018:** decidir si se define «coordinar» en el glosario o se adopta una redacción con resultado observable, como «de modo que se utilicen las cantidades de la receta».
6. **CAF-RF-020:** decidir si el aviso debe ser único al inicio, mantenido durante toda la preparación o periódico, y cuál es su contenido exacto. No se ha fijado un plazo ni una frecuencia.
7. **CAF-RF-022:** decidir si se define «despacho» o se elimina el segundo contenido. Si se mantiene, añadir una comprobación específica.
8. **R1:** documentar y acordar un patrón formal de enunciado para poder verificar R1 en una revisión posterior. Sin ese patrón, la conformidad con R1 no puede declararse.
9. **R4:** valorar si el glosario debe ampliarse. En esta evaluación solo se ha observado «despacho» como término materialmente indefinido; no se propone convertir el glosario en una lista exhaustiva de palabras comunes.

### 8.4. Estado

No se registra ninguna decisión del equipo. No se modifican `requisitos-v2.md`, `requisitos-v3.md` ni `matriz-y-decisiones.md`. No se declara aprobado ningún requisito ni terminado el ejercicio 3. Todas las correcciones y redacciones alternativas son propuestas de la IA pendientes de revisión y decisión del equipo.
