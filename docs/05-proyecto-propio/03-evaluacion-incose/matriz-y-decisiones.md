# Matriz de cumplimiento INCOSE — proyecto propio

## 1. Base, fuente y estado

**Estado: ejercicio 5 cerrado por confirmación del equipo. El equipo ha revisado y confirmado las recomendaciones individualizadas de §4, los ajustes REV-001 a REV-005, [requisitos v3](requisitos-v3.md) y la [comparativa y valoración crítica](comparativa-evaluaciones.md). INC-OBS-001 se conserva como limitación, sin declarar conformidad con R1.**

La base es [requisitos v2](../02-evaluacion-ia/requisitos-v2.md), confirmada por el equipo el 28 de octubre de 2026. La evidencia de esta evaluación es una sola respuesta: [SpaceXAI Grok 4.7](respuesta-spacexai-grok-4.7.md). En la cafetera hubo dos modelos; aquí no hay una segunda evaluación con la que comparar.

| Clave | Evaluación | Contenido |
| --- | --- | --- |
| GK | [Grok 4.7](respuesta-spacexai-grok-4.7.md) | §3: 18 observaciones. §4: 120 valoraciones, una por requisito y aspecto. |

Las reglas son las de [reglas seleccionadas](reglas-seleccionadas.md), los mismos seis aspectos del ejercicio 3. Las valoraciones **OP**, **RA**, **SPD** y **NA** son etiquetas de esa respuesta, no categorías oficiales de INCOSE ni decisiones del equipo.

La matriz completa está en la respuesta, §4. Esta página recoge las valoraciones originales por requisito y las decisiones confirmadas por el equipo. Las aceptaciones parciales y los ajustes de §§4–5 determinan el texto final; confirmar el problema no implica aceptar literalmente toda la redacción original de Grok.

La revisión de §§4–5 ha sido revisada y confirmada por el equipo. No es otra respuesta original de Grok. Las etiquetas de §2 siguen describiendo la evaluación de v2; no califican la v3 revisada.

## 2. Cumplimiento por requisito

INC-OBS-001 afecta a los 20 requisitos: es la falta de un patrón formal para R1, no un defecto gramatical de cada frase. «Sin otra observación» significa que no hay un INC-OBS específico además de ese.

| Requisito | S | CL | G | T | A | V | Observaciones |
| --- | --- | --- | --- | --- | --- | --- | --- |
| GMP-RF-001 | SPD | SPD | RA | SPD | SPD | SPD | Solo INC-OBS-001 |
| GMP-RF-002 | OP | SPD | RA | SPD | SPD | SPD | INC-OBS-001, INC-OBS-002 |
| GMP-RF-003 | OP | OP | RA | SPD | SPD | SPD | INC-OBS-001, INC-OBS-003, INC-OBS-004 |
| GMP-RF-004 | OP | OP | RA | SPD | OP | SPD | INC-OBS-001, INC-OBS-005, INC-OBS-006 |
| GMP-RF-005 | OP | SPD | RA | SPD | OP | SPD | INC-OBS-001, INC-OBS-007 |
| GMP-RF-006 | SPD | SPD | RA | SPD | SPD | SPD | Solo INC-OBS-001 |
| GMP-RF-007 | OP | SPD | RA | SPD | SPD | SPD | INC-OBS-001, INC-OBS-008 |
| GMP-RF-016 | SPD | OP | RA | OP | SPD | SPD | INC-OBS-001, INC-OBS-009 |
| GMP-RF-008 | OP | OP | RA | SPD | SPD | OP | INC-OBS-001, INC-OBS-010 |
| GMP-RF-009 | OP | OP | RA | SPD | OP | OP | INC-OBS-001, INC-OBS-011 |
| GMP-RF-010 | SPD | OP | RA | SPD | OP | OP | INC-OBS-001, INC-OBS-012 |
| GMP-RF-011 | SPD | OP | RA | SPD | SPD | OP | INC-OBS-001, INC-OBS-013 |
| GMP-RF-012 | SPD | SPD | RA | SPD | SPD | SPD | Solo INC-OBS-001 |
| GMP-RF-013 | OP | OP | RA | SPD | SPD | OP | INC-OBS-001, INC-OBS-014 |
| GMP-RF-014 | SPD | OP | RA | OP | SPD | OP | INC-OBS-001, INC-OBS-015 |
| GMP-RF-015 | SPD | OP | RA | SPD | OP | OP | INC-OBS-001, INC-OBS-016 |
| GMP-RNF-001 | SPD | OP | RA | SPD | OP | SPD | INC-OBS-001, INC-OBS-017 |
| GMP-RNF-002 | SPD | SPD | RA | SPD | SPD | SPD | Solo INC-OBS-001 |
| GMP-RNF-003 | SPD | SPD | RA | SPD | NA | SPD | Solo INC-OBS-001 |
| GMP-RNF-004 | SPD | OP | RA | SPD | SPD | OP | INC-OBS-001, INC-OBS-018 |

Recuento de las 120 celdas: 36 OP, 20 RA, 1 NA y 63 SPD. Las 20 RA son INC-OBS-001.

## 3. Observaciones y decisiones confirmadas

El hallazgo y la redacción íntegros están en la respuesta. Esta tabla no los sustituye.

| Registro | Requisito | Valoración | Hallazgo | Propuesta | Decisión del equipo |
| --- | --- | --- | --- | --- | --- |
| INC-OBS-001 | Los 20 requisitos | RA | No hay un patrón formal documentado para comprobar R1. | Aportar el patrón existente o acordar uno. Mantener mientras tanto los enunciados en este punto. | Limitación confirmada; sin patrón adoptado ni reescritura por este motivo |
| INC-OBS-002 | GMP-RF-002 | OP | Segmentar y corregir pueden cumplirse por separado. El rechazo del identificador duplicado está solo en la descripción. | Separar en GMP-RF-002-A y GMP-RF-002-B. | Aceptada y aplicada en v3; justificación en §4 |
| INC-OBS-003 | GMP-RF-003 | OP | Proponer etiquetas y no generar el modelo hasta confirmarlas son dos obligaciones. | Separar en GMP-RF-003-A y GMP-RF-003-B. | Aceptada y aplicada en v3; justificación en §4 |
| INC-OBS-004 | GMP-RF-003 | OP | «Una etiqueta» no fija el catálogo ni si puede haber varias. | Incluir en GMP-RF-003-A el catálogo, la cardinalidad y la exclusión de autenticación ya aceptados. | Aceptada y aplicada en v3; justificación en §4 |
| INC-OBS-005 | GMP-RF-004 | OP | RBAC para OWASP y ABAC para NIST son resultados distintos. Faltan en el enunciado los elementos de cada modelo y el caso de las dos etiquetas. | Separar en GMP-RF-004-A, GMP-RF-004-B y GMP-RF-004-C. | Aceptada parcialmente: A/B cubren ambas etiquetas sin C independiente (REV-001); justificación en §4 |
| INC-OBS-006 | GMP-RF-004 | OP | La interpretación de un requisito ambiguo, ya aceptada, está solo en la descripción. | Añadir GMP-RF-004-D con esa regla, sin definir «ambiguo» de otra manera. | Aceptada con la limitación de §4 y la revisión humana de REV-002 |
| INC-OBS-007 | GMP-RF-005 | OP | Mostrar, editar y exigir confirmación son tres obligaciones. El efecto sobre los casos Pendiente no está en el enunciado. | Separar en GMP-RF-005-A, GMP-RF-005-B y GMP-RF-005-C. | Aceptada con la adaptación de REV-002/003; justificación en §4 |
| INC-OBS-008 | GMP-RF-007 | OP | Guardar sin ejecutar, corregir y exportar tienen resultados distintos. | Separar en GMP-RF-007-A, GMP-RF-007-B y GMP-RF-007-C. El formato sigue sin fijarse. | Aceptada y aplicada en v3; justificación en §4 |
| INC-OBS-009 | GMP-RF-016 | OP | «Casos concretos» no dice que los elige el analista. | Nombrar en el enunciado los casos en Pendiente que indique el analista. | Aceptada y aplicada en v3; justificación en §4 |
| INC-OBS-010 | GMP-RF-008 | OP | La consistencia sintáctica, la semántica y la lógica se comprueban por separado y su criterio está solo en la descripción. | Separar en GMP-RF-008-A, GMP-RF-008-B y GMP-RF-008-C. | Aceptada parcialmente con la delimitación de REV-002; justificación en §4 |
| INC-OBS-011 | GMP-RF-009 | OP | Emitir el informe, clasificar y condicionar la ejecución son obligaciones distintas. El sentido de Error y Advertencia está solo en la descripción. | Separar en GMP-RF-009-A, GMP-RF-009-B y GMP-RF-009-C. | Aceptada con la vigencia de REV-003; justificación en §4 |
| INC-OBS-012 | GMP-RF-010 | OP | «Filtros» no nombra los tres filtros ya aceptados ni la condición del filtro de severidad. | Trasladar esos filtros al enunciado, sin añadir otro selector. | Aceptada y aplicada en v3; justificación en §4 |
| INC-OBS-013 | GMP-RF-011 | OP | Pass, Fail y Error se nombran sin la regla de asignación ya aceptada. | Separar la ejecución, GMP-RF-011-A, de la regla de veredicto, GMP-RF-011-B. Se mantiene el 403 como único código fijado. | Aceptada por explicitación y organización; no se atribuye defecto de singularidad a la fuente (§4) |
| INC-OBS-014 | GMP-RF-013 | OP | Cobertura y tasa de éxito tienen fórmulas distintas y ninguna está en el enunciado. | Separar en GMP-RF-013-A y GMP-RF-013-B, con los cálculos ya escritos en v2. | Aceptada con la condición límite de REV-005; justificación en §4 |
| INC-OBS-015 | GMP-RF-014 | OP | «Casos válidos» no tiene criterio en el enunciado. | Sustituirlo por casos sin Error de validación estática. | Aceptada y aplicada en v3; justificación en §4 |
| INC-OBS-016 | GMP-RF-015 | OP | «Informe consolidado» no dice qué contiene ni cuándo entran las comparaciones del baseline. | Trasladar al enunciado el contenido ya aceptado en la descripción. | Aceptada y aplicada en v3; incluye las comparaciones confirmadas en REV-005 |
| INC-OBS-017 | GMP-RNF-001 | OP | El enunciado obliga a redactar en español sin las excepciones ya aceptadas para veredictos, texto ingerido y claves JSON. | Incorporar esas excepciones al enunciado. | Aceptada y aplicada en v3; justificación en §4 |
| INC-OBS-018 | GMP-RNF-004 | OP | El 85 % no tiene en el enunciado la coincidencia ni el denominador. «Extraídas» y «generadas» pueden no ser el mismo conjunto. | Pasar al enunciado la fórmula de la descripción y decir «generadas». | Aceptada con los límites de interpretación de §4 y REV-005 |

## 4. Recomendaciones confirmadas y justificación por observación

**El equipo ha confirmado las recomendaciones siguientes tras revisar la documentación.** La columna conserva la formulación de cada recomendación y la justificación adoptada; las decisiones resultantes se recogen en §3. Se aceptan las adaptaciones y limitaciones indicadas, no automáticamente toda alternativa de la respuesta original.

| Observación | Recomendación confirmada | Justificación y aplicación en v3 |
| --- | --- | --- |
| INC-OBS-001 | Mantener como limitación | No hay patrón formal documentado. No se puede declarar conformidad con R1 ni interpretar la carencia como 20 errores gramaticales. El equipo confirma mantener esta limitación sin adoptar un patrón en esta fase. |
| INC-OBS-002 | Aceptar la separación | Segmentar constituye la entrada; editar es otra capacidad con una condición observable ante duplicados. A/B permiten localizar cuál falla. El rechazo del duplicado califica la edición y no necesita otro identificador. |
| INC-OBS-003 | Aceptar la separación | Proponer etiquetas no garantiza bloquear la generación. A/B separan la propuesta de datos de la compuerta de confirmación, sin separar las alternativas confirmar/corregir. |
| INC-OBS-004 | Aceptar la aclaración | El catálogo y la cardinalidad ya están en la descripción de v2. Incorporarlos evita que «una etiqueta» se lea como exactamente una y no crea una categoría nueva. |
| INC-OBS-005 | Aceptar parcialmente | Se conservan A/B por sus entradas y resultados distintos. No se recomienda C independiente: ambas condiciones siguen siendo verdaderas con doble etiqueta y ya obligan a generar ambos tipos. REV-001 conserva esa comprobación en A/B, sin eliminar el comportamiento. |
| INC-OBS-006 | Aceptar la explicitación con limitación | D hace visible la interpretación propuesta ante ambigüedad. No acredita que el sistema detecte exhaustivamente toda ambigüedad; el criterio necesita una entrada de referencia cuya interpretación revise el analista (REV-002). |
| INC-OBS-007 | Aceptar la separación y adaptar la confirmación | Mostrar, editar y confirmar pueden fallar por separado. C debe concretar qué revisa el analista y su relación con el requisito de origen (REV-002). Conservar casos anteriores no exime de volver a validar tras cambios (REV-003). |
| INC-OBS-008 | Aceptar la separación | Guardar, corregir y exportar tienen evidencias distintas. Cada operación conserva la restricción de no ejecutar. Se mantiene la libertad de formato de exportación de casos; PDF/JSON siguen exigidos para el informe consolidado. |
| INC-OBS-009 | Aceptar la aclaración | Identificar al analista como quien elige los casos evita un selector autónomo no acordado. Elegir parámetros y sustituir solo esos casos califica la misma regeneración. |
| INC-OBS-010 | Aceptar parcialmente | Separar los tres tipos de defecto facilita su comprobación, pero sus ejemplos solo acreditan consistencia interna. Se propone delimitar la fidelidad al requisito mediante revisión humana explícita (REV-002), sin presentar esa delimitación como equivalente automático a toda la obligación amplia de v2. |
| INC-OBS-011 | Aceptar la separación y ampliar la vigencia | Informe, clasificación y bloqueo son obligaciones observables distintas. Que un informe exista no acredita los artefactos actuales; REV-003 añade la revalidación tras cambios. |
| INC-OBS-012 | Aceptar la explicitación | Se trasladan los filtros ya descritos y su condición de disponibilidad. No se añade una selección autónoma. El criterio de v3 debe comprobar también el filtro de severidad con informe existente. |
| INC-OBS-013 | Aceptar la explicitación y la organización en A/B | La propia matriz de Grok marca singularidad SPD. Separar la regla de veredicto se recomienda para localizarla y comprobarla, no como prueba de un defecto de singularidad reconocido por la fuente. El código esperado de cada caso debe ser conocido al verificar. |
| INC-OBS-014 | Aceptar la separación con condición límite | Las dos fórmulas tienen denominadores y condiciones diferentes. REV-005 define el total cero en cobertura; la falta de ejecuciones ya estaba tratada en v2. Calcular y mostrar una misma métrica se conserva como una capacidad. |
| INC-OBS-015 | Aceptar la definición | «Sin Error de validación estática» determina el recuento, pero no equivale a prueba superada ni a representación fiel del requisito. REV-005 añade una métrica distinta para hacer visibles las reglas omitidas. |
| INC-OBS-016 | Aceptar la explicitación | Los contenidos y la condición de baseline ya estaban en v2. PDF y JSON son formatos de la misma exportación; no se separan solo por ser dos formatos. Las comparaciones exportadas incluyen la métrica confirmada en RF-014. |
| INC-OBS-017 | Aceptar las excepciones explícitas | Evita exigir traducir Pass/Fail o los textos de entrada mientras otro requisito conserva esos valores. No introduce una traducción automática. |
| INC-OBS-018 | Aceptar la fórmula y limitar su interpretación | La coincidencia y el denominador hacen calculable el 85 %. No demuestran completitud, viabilidad del umbral ni independencia del baseline elegido. REV-005 distingue precisión y reglas representadas sin inventar un umbral adicional. |

La revisión no propone dividir toda conjunción: una acción puede tener campos, resultados, prohibiciones y condiciones asociados. El aumento de IDs no se usa como indicador de calidad. El caso C de INC-OBS-005 se revisa aquí por redundancia como análisis adicional; no se atribuye a R30 ni se amplía retrospectivamente la selección de reglas aplicada por Grok.

## 5. Asuntos técnicos de la revisión posterior

Estos asuntos no son hallazgos originales INC-OBS. El equipo ha confirmado los ajustes de la v3 y las limitaciones indicadas; no alteran la aceptación histórica E5-001 a E5-037 ni la v2. En REV-004 se aprueba el protocolo como marco, pero sus entradas y entorno concretos quedan por determinar antes de la verificación.

| Asunto | Evidencia y consecuencia | Ajuste confirmado y comprobación prevista | Aplicación y estado |
| --- | --- | --- | --- |
| REV-001 — Descomposición sin repetición | GMP-RF-004-C repetía la conjunción de las obligaciones A/B cuando las dos etiquetas están presentes. | Integrar la comprobación de doble etiqueta en A/B y mantener sus condiciones no excluyentes. | Confirmado: v3 contiene 30 RF y 4 RNF; aceptación parcial de INC-OBS-005. |
| REV-002 — Fidelidad requisito–modelo | V2 RF-008 exige consistencia respecto de los requisitos. Detectar campos ausentes o referencias inválidas no detecta un permiso erróneo entre elementos existentes. | El sistema presenta requisito y reglas, y exige revisión humana del sujeto/rol, recurso, acción, efecto y condiciones. Usar el contraejemplo «solo administrador» con permiso también al lector para comprobar la posibilidad de contraste y la compuerta. | Confirmado en RF-005-C y descripción de RF-008-A: revisión humana de fidelidad y controles automáticos de consistencia interna. |
| REV-003 — Vigencia de validación | RF-005-B conserva casos al editar el modelo y RF-007-B permite corregirlos. Un informe sin Error puede quedar obsoleto. | Validar las versiones actuales antes de ejecutar y repetir tras cambios en requisitos, modelo o casos del alcance validado. Probar una modificación que introduzca una referencia inválida después de un informe favorable. | Confirmado en RF-009-A. No implica regenerar casos automáticamente. |
| REV-004 — Rendimiento reproducible | H-032 señaló ausencia de condiciones; E5-032 mantuvo 15 s sin fijar todas ellas. INCOSE calificó SPD la verificabilidad de RNF-002 sin resolver el entorno ni la extensión de entrada. | Usar el protocolo de v3 §3: corpus, configuración de IA, entorno, red, carga, escenarios y repeticiones identificados; registrar fallos y tiempos. | Confirmado: RNF-002 mantiene el compromiso de 15 s y amplía el criterio. Falta concretar corpus, configuración, entorno y repeticiones antes de verificar. |
| REV-005 — Métricas y denominadores | RF-013-A divide por cero sin requisitos. RNF-004 puede dar 100 % de precisión generando una sola regla correcta de 20 manuales. | Cobertura «No aplicable» con total cero; añadir porcentaje de reglas manuales representadas con coincidencia de RNF-004, sin duplicar el recuento manual ni fijar umbral. Comprobar 100 % de precisión frente a 5 % de reglas representadas en el ejemplo. | Confirmado en RF-013-A y RF-014; RF-015 exporta las comparaciones correspondientes. Sin nuevo umbral de completitud. |

## 6. Resultado y revisión del equipo

La [comparativa y valoración crítica](comparativa-evaluaciones.md) desarrolla la relación entre ambas evaluaciones y sus límites. El equipo ha confirmado las decisiones individualizadas, los ajustes REV-001 a REV-005, la v3 y ese análisis. Se registra el cierre documental del ejercicio 5.

Se conserva la limitación de R1 y quedan por concretar las condiciones de ejecución del protocolo de rendimiento antes de verificarlo. El cierre no declara pruebas ejecutadas ni conformidad INCOSE de la v3; las valoraciones originales siguen correspondiendo a v2.
