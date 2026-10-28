# Matriz de comparación y decisiones — evaluación INCOSE de v2

## 1. Base, fuentes y estado

**Estado: ejercicio 3 cerrado por confirmación del equipo. Comparación y decisiones registradas para los 12 temas y las 15 observaciones originales; CAF-RF-003A confirmado, requisitos v3, comparativa con el ejercicio 2 y valoración crítica revisados por el equipo. Se conservan las limitaciones documentadas.**

Esta matriz reúne los hallazgos de las dos evaluaciones de [requisitos v2](../02-evaluacion-ia/requisitos-v2.md), base del ejercicio 3 procedente del ejercicio 2 cerrado por el equipo. Se han contrastado los análisis con las descripciones y comprobaciones de v2, el [contexto y alcance](../01-requisitos-iniciales/contexto-y-alcance.md) y las [reglas seleccionadas](reglas-seleccionadas.md).

| Clave de fuente | Evaluación original | Referencia interna |
| --- | --- | --- |
| OA | [OpenAI gpt-6.1-sol](respuesta-openai-gpt-6.1-sol.md) | §3: 6 observaciones; §4: matriz de 156 valoraciones. |
| DS | [DeepSeek deepseek-v4.1-flash-free](respuesta-deepseek-v4.1-flash-free.md) | §5: 9 observaciones; §6: matriz de 156 valoraciones; §3: limitación transversal de R1. |

Las observaciones se identifican con el modelo y el ID de su evaluación original. Las decisiones comunicadas por el equipo se registran en §5, separadas de los hallazgos originales.

- Los identificadores `INC-OBS` solo son únicos dentro de cada respuesta: deben citarse siempre con la fuente y el modelo. Por ejemplo, OA INC-OBS-001 y DS INC-OBS-001 son hallazgos distintos.
- `E3-001` a `E3-015` identifican los **15 hallazgos originales por modelo**. `CMP-01` a `CMP-12` agrupan los **12 temas de revisión**. Agrupar no elimina observaciones ni unifica sus valoraciones.
- Las valoraciones originales se conservan: **OP** = observación propuesta; **RA** = requiere aclaración; **SPD** = sin problema detectado; **NA** = no aplica. Son etiquetas de las evaluaciones, no categorías oficiales de INCOSE.
- Las reglas R y las características C mantienen las referencias de las fuentes: C3, C5 y C7 en la p. 2 de la hoja-resumen; reglas en la p. 3 y correspondencias en la p. 4. Las referencias por hallazgo se transcriben en el registro, sin ampliar la selección.
- La coincidencia de dos modelos no implica aceptación. La ausencia de un hallazgo en uno tampoco supone rechazo del otro ni aprobación del requisito.
- La comparación de §3 conserva los puntos planteados antes de las decisiones. Las decisiones explícitas, sus justificaciones y los textos acordados se registran por separado en §5. Una respuesta ambigua requiere aclaración.
- Los textos alternativos y los IDs de §2 pertenecen a las propuestas originales. Los IDs y textos confirmados por el equipo figuran en §5.1; su incorporación a [v3](requisitos-v3.md) se registra en §5 y §5.2.

## 2. Registro de hallazgos originales por modelo

Se sigue el orden de v2, incluido CAF-RF-015 antes de CAF-RF-014. El patrón R1 se registra primero por su carácter transversal. Las celdas de hallazgo y propuesta son resúmenes; los fragmentos, argumentos y redacciones íntegros permanecen en las fuentes enlazadas en §1.

| Registro | Tema | Requisito | Fuente / observación original | Valoración original | Aspectos y referencias originales | Hallazgo original resumido | Propuesta original resumida |
| --- | --- | --- | --- | --- | --- | --- | --- |
| E3-001 | CMP-01 | Los 26 requisitos; origen de registro CAF-RF-001 | OA — INC-OBS-001 | RA | Estructura gramatical; R1, con R12/R2/R3 para distinguir la gramática. | Falta un patrón formal acordado para comprobar R1; no es un defecto gramatical demostrado. | Aportar el patrón existente o acordarlo; mantener por ahora los enunciados en este punto. Redacción pendiente del patrón. |
| E3-002 | CMP-02 | CAF-RF-003 | DS — INC-OBS-001 | RA | Condiciones, claridad y verificabilidad; R27/R28/R11, C3 y C7. | La descripción y la comprobación incluyen reglas de cambio en los demás casos que no aparecen en el enunciado condicional. | Mantener CAF-RF-003 y proponer CAF-RF-003A para exigir cancelación al cambiar una bebida disponible cuando no hay autorización pendiente ni pago autorizado. |
| E3-003 | CMP-03 | CAF-RF-009 | OA — INC-OBS-002 | OP | Condiciones y verificabilidad; R27, C7 y R35. | «Durante una preparación» caracteriza el consumo de vasos, pero no fija inequívocamente el momento del descuento. | Incorporar «Al finalizar una preparación, tanto si se completa como si falla», usando el número comunicado por los mecanismos. |
| E3-004 | CMP-04 | CAF-RF-010 | DS — INC-OBS-002 | OP | Condiciones y verificabilidad; R27 y C7. | «Una vez comprobada su disponibilidad» no explicita que el resultado debe ser favorable. | Solicitar autorización «solo después de comprobar que está disponible». |
| E3-005 | CMP-05 | CAF-RF-015 | OA — INC-OBS-003 | OP | Singularidad; C5, R18 y R19. | Asociar resultado-intento y vincular devolución-intento autorizado son obligaciones comprobables por separado. | Separar en CAF-RF-015-A y CAF-RF-015-B; precisar resultado recibido del terminal y vínculo de cada solicitud de devolución. |
| E3-006 | CMP-05 | CAF-RF-015 | DS — INC-OBS-003 | OP | Singularidad; C5, R18 y R19. | Las dos asociaciones tienen objetos distintos y pueden cumplirse una sin la otra. | Separar en CAF-RF-015A y CAF-RF-015B; usar «poder asociar una solicitud de devolución» en la segunda. |
| E3-007 | CMP-06 | CAF-RF-014 | DS — INC-OBS-004 | OP | Condiciones, claridad y verificabilidad; R27/R28/R11, C3 y C7. | La primera ventana de cancelación puede no cubrir el intervalo posterior a la elección y previo a solicitar autorización. | Expresar un intervalo «desde el inicio de la selección hasta antes de iniciar una solicitud de autorización»; conservar la ventana tras denegación. |
| E3-008 | CMP-07 | CAF-RF-017 | DS — INC-OBS-005 | OP | Condiciones y verificabilidad; R27 y C7. | Comprobar disponibilidad no expresa inequívocamente un resultado favorable como condición de inicio. | Explicitar que la bebida está disponible, además del pago autorizado y la ausencia de fallo comunicado que impida entregar. |
| E3-009 | CMP-08 | CAF-RF-018 | DS — INC-OBS-006 | OP | Claridad y verificabilidad; C3 y C7. | «Coordinar ... con las cantidades» permite interpretaciones distintas de la conducta observable. | Añadir «de modo que se utilicen las cantidades de ingredientes indicadas en su receta» o definir «coordinar». |
| E3-010 | CMP-09 | CAF-RF-019 | OA — INC-OBS-004 | OP | Condiciones; R27. | La finalidad de entregar la bebida no explicita la aplicabilidad de la orden a la preparación iniciada para la compra. | Introducir «Durante la preparación iniciada para la operación de compra», sin fijar un punto físico de dispensación. |
| E3-011 | CMP-10 | CAF-RF-020 | OA — INC-OBS-005 | OP | Claridad y verificabilidad; C3 y C7. | Falta el contenido que se debe comunicar; el periodo sí se considera definido. | «Mientras la bebida se esté preparando, el sistema deberá informar al cliente de que la preparación está en curso». |
| E3-012 | CMP-10 | CAF-RF-020 | DS — INC-OBS-007 | RA | Claridad y verificabilidad; C3, C7 y apoyo de R35. | Faltan el contenido y la precisión de si el aviso es único, persistente o periódico. | Decidir contenido y duración; propone alternativas de aviso al inicio o mantenido desde el inicio hasta la finalización. |
| E3-013 | CMP-11 | CAF-RF-022 | DS — INC-OBS-008 | RA | Claridad y verificabilidad; C3, R4 y C7. | «Despacho» no está definido; el segundo contenido se solapa con el primero y no se comprueba expresamente en el criterio. | Definir el término y comprobar el segundo contenido, o integrar ambos en una comunicación de servicio no completado porque no se entregó la bebida. |
| E3-014 | CMP-12 | CAF-RF-023 | OA — INC-OBS-006 | OP | Singularidad; C5, R18 y R19. | Solicitar devolución y avisar al cliente son acciones independientes; «fue solicitada» ya expresa una secuencia. | Separar en CAF-RF-023-A y CAF-RF-023-B; la segunda se activa cuando se haya solicitado la devolución prevista en la primera. |
| E3-015 | CMP-12 | CAF-RF-023 | DS — INC-OBS-009 | OP | Singularidad; C5, R18 y R19. | Solicitud económica y comunicación al cliente tienen evidencias y destinatarios distintos. | Separar en CAF-RF-023A y CAF-RF-023B con la misma condición de fallo; deja pendiente si añadir «una vez solicitada la devolución» a la segunda. |

La limitación R1 de DS no tiene ID `INC-OBS`: se conserva como referencia complementaria en CMP-01, sin crear una décima observación formal de ese modelo.

## 3. Comparación de coincidencias y diferencias

**Las preguntas siguientes conservan los puntos planteados para la discusión. Las decisiones posteriores del equipo constan en §5; esta comparación no las sustituye.**

| Tema | Registros relacionados | Comparación de los análisis | Punto planteado al equipo |
| --- | --- | --- | --- |
| CMP-01 — Patrón R1 | E3-001; DS §3 y filas de estructura | Coinciden en que no puede declararse conformidad con un patrón no documentado y en no detectar defectos gramaticales concretos. OA registra una RA transversal en las 26 filas; DS registra SPD con la salvedad L1 y no crea observación formal. Es una diferencia de etiquetado, no de conclusión sobre R1. | Indicar si existe un patrón acordado o si debe acordarse. No convertir la diferencia de etiquetas en 26 defectos ni en conformidad acreditada. |
| CMP-02 — Cambio de bebida | E3-002 | DS pide aclarar la cobertura del enunciado frente a las reglas complementarias de descripción y comprobación. OA valora SPD claridad, condiciones y verificabilidad, interpretando la sustitución y los demás cambios con descripción y contexto. | Determinar si la regla complementaria debe explicitarse en un requisito separado o si las referencias actuales bastan. Si se acepta la propuesta, comprobar que se conserva cancelar **e iniciar una nueva operación** y la restricción en estados de autorización; no asumir que impedir cancelar equivale por sí solo a impedir cambiar. |
| CMP-03 — Momento del descuento de vasos | E3-003 | Solo OA observa que el enunciado no fija el evento de actualización. DS valora SPD condiciones y verificabilidad al considerar explícito el marco de preparación y fallo. Ambos entienden la cantidad como consumo real comunicado. | Valorar si debe incorporarse el momento «al finalizar» ya recogido en contexto §3, sin cambiar el consumo real ni inventar una latencia. |
| CMP-04 — Disponibilidad antes de solicitar pago | E3-004 | DS distingue comprobación realizada de resultado favorable. OA considera explícita la precondición y obtiene el sentido positivo de la definición de disponibilidad y CAF-RF-006. | Decidir si se necesita explicitar el resultado favorable en CAF-RF-010. Revisar conjuntamente CMP-07 por compartir el problema, conservando decisiones por hallazgo. |
| CMP-05 — Asociaciones de pago | E3-005 y E3-006 | Coincidencia en el hallazgo y la separación de CAF-RF-015. Las alternativas difieren: OA añade «recibido del terminal» y «cada solicitud»; DS conserva «cada resultado» y propone «poder asociar una solicitud». Los sufijos provisionales también difieren. | Decidir la validez de la separación y, por separado, la formulación y los IDs definitivos. Preservar ambas relaciones y la libertad sobre quién conserva la referencia. |
| CMP-06 — Ventana de cancelación | E3-007 | DS identifica ambigüedad sobre el periodo entre selección y autorización. OA considera explícitas las dos ventanas y sus relaciones lógicas. Dentro de DS, la explicación admite que el «o» entre ventanas es claro, mientras la fila de condiciones cuestiona también esa relación; debe precisarse qué se acepta del hallazgo. | Confirmar el intervalo de cancelación y si la mejora es necesaria. Contrastar el enunciado con descripción, comprobación y contexto §5, sin introducir una ventana nueva por inferencia. |
| CMP-07 — Disponibilidad antes de preparar | E3-008 | DS pide explicitar resultado favorable; OA considera explícita la conjunción disponibilidad comprobada, pago autorizado y ausencia de fallo. | Revisar coherencia con CMP-04 y con CAF-RF-006/011. Si se ajusta el texto, conservar todas las precondiciones del inicio y distinguir comprobación de resultado. |
| CMP-08 — Significado de «coordinar» | E3-009 | DS considera insuficientemente observable el verbo. OA lo interpreta como control software de los mecanismos con cantidades de la receta y valora SPD claridad y verificabilidad. | Determinar si el contexto y la referencia a receta bastan o si se precisa el verbo/resultado. Revisar que una alternativa no convierta el control software en garantía de medición física, excluida del alcance. |
| CMP-09 — Aplicabilidad de la orden de vaso | E3-010 | OA pide explicitar su pertenencia a la preparación de la compra. DS marca NA en condiciones: considera «para entregar» una finalidad, no una condición. Ninguno pide fijar una secuencia física concreta como requisito nuevo. | Decidir si la aplicabilidad está implícita y necesita aclararse. Si se adopta «durante la preparación», comprobar que esa expresión no impone una secuencia física no acordada. |
| CMP-10 — Información durante preparación | E3-011 y E3-012 | Coinciden en que falta el contenido de la información. OA lo registra como OP y considera definido el periodo. DS lo registra como RA y añade la cuestión de duración/persistencia. No son propuestas totalmente equivalentes: DS plantea opciones que requieren decisión. | Resolver por separado el contenido «preparación en curso» y si hace falta precisar la duración del aviso. Un acuerdo sobre el contenido no acepta automáticamente un aviso persistente o periódico. |
| CMP-11 — Aviso de servicio sin entrega | E3-013 | DS cuestiona «despacho», el solapamiento de contenidos y su comprobación. OA interpreta «despacho sin entrega» como fin del servicio fallido con el contexto y valora SPD claridad y verificabilidad. Ambos consideran una sola acción de informar. | Decidir si definir/sustituir el término o mantenerlo; distinguir comunicar que no se entregó la bebida de comunicar que la operación terminó. Si se fusionan contenidos, revisar que no se pierda esa información. |
| CMP-12 — Devolución y aviso | E3-014 y E3-015 | Coinciden en separar CAF-RF-023. OA hace explícita la dependencia del aviso respecto de la solicitud y no encuentra un problema temporal independiente. DS mantiene la misma condición de fallo en ambos enunciados y deja pendiente si explicitar esa secuencia. | Decidir separación y formulación, conservando que se avisa de una solicitud efectuada, no de un reintegro garantizado. Resolver los IDs definitivos y mantener las exclusiones bancarias y de fallos de solicitud. |

### 3.1. Lectura de las matrices completas

Además de los hallazgos formales, se han comparado las valoraciones de los seis aspectos en los 26 requisitos. Las diferencias de etiquetado relevantes para leer la comparación son:

- **Estructura gramatical en toda la base:** OA usa RA por R1; DS usa SPD con limitación global. Se conserva esta diferencia en CMP-01, sin homogeneizar retrospectivamente las fuentes.
- **Condiciones de CAF-RF-015 y CAF-RF-018:** OA usa SPD para relaciones/calificaciones explícitas; DS usa NA porque no identifica condiciones de aplicación. Son diferencias de clasificación sin observación correctiva adicional. En CAF-RF-019 la diferencia OP/NA sí corresponde al hallazgo CMP-09.
- **CAF-RF-020, condiciones:** ambos usan SPD; DS referencia además INC-OBS-007 para contenido/duración. La referencia no convierte esa fila en una nueva observación sobre aplicabilidad.
- **Aplicabilidad de reglas de cuantificación:** OA declara que R34 no exige rendimiento cuantitativo en esta base; DS cita R33/R34 como apoyo a unidad y precisión en CAF-RNF-002. Se conserva la diferencia de justificación; ninguno propone un valor nuevo. Las listas de reglas de ambas matrices no se interpretan como hallazgos automáticos para cada regla citada.
- En singularidad ambos mantienen la distinción entre dos obligaciones independientes y una sola acción con lista de datos, condiciones o calificaciones. Ambos informan ausencia de hallazgos específicos por R7. No se usa el número de filas OP/RA/SPD/NA como puntuación de calidad de un modelo.

## 4. Cobertura por requisito

Esta tabla permite localizar los temas de cada requisito; las matrices individuales completas siguen en las fuentes. **CMP-01 afecta a todos los requisitos**, también a los que no tienen otro hallazgo formal. «Sin otro hallazgo formal» significa únicamente que no se añadió un `INC-OBS` específico.

| Requisito | Temas específicos | Resultado de la comparación |
| --- | --- | --- |
| CAF-RF-001 | — | Sin otro hallazgo formal; limitación común CMP-01. |
| CAF-RF-002 | — | Sin otro hallazgo formal. |
| CAF-RF-003 | CMP-02 | Hallazgo DS; OA considera suficiente la interpretación con descripción y contexto. |
| CAF-RF-004 | — | Sin otro hallazgo formal. |
| CAF-RF-005 | — | Sin otro hallazgo formal. |
| CAF-RF-006 | — | Sin otro hallazgo formal. |
| CAF-RF-007 | — | Sin otro hallazgo formal. |
| CAF-RF-008 | — | Sin otro hallazgo formal. |
| CAF-RF-009 | CMP-03 | Hallazgo OA sobre momento del descuento; DS no lo observa. |
| CAF-RF-010 | CMP-04 | Hallazgo DS sobre resultado favorable; OA lo interpreta con contexto y bloqueo. |
| CAF-RF-011 | — | Sin otro hallazgo formal. |
| CAF-RF-012 | — | Sin otro hallazgo formal. |
| CAF-RF-013 | — | Sin otro hallazgo formal. |
| CAF-RF-015 | CMP-05 | Coinciden en separar las dos asociaciones; diferencias de redacción y de etiqueta de condiciones. |
| CAF-RF-014 | CMP-06 | Hallazgo DS sobre ventana de cancelación; OA no lo observa. |
| CAF-RF-016 | — | Sin otro hallazgo formal. |
| CAF-RF-017 | CMP-07 | Hallazgo DS sobre resultado favorable de disponibilidad; OA no lo observa. |
| CAF-RF-018 | CMP-08 | Hallazgo DS sobre «coordinar»; OA lo interpreta como control software. |
| CAF-RF-019 | CMP-09 | Hallazgo OA sobre aplicabilidad; DS marca condiciones NA. |
| CAF-RF-020 | CMP-10 | Coinciden en falta de contenido; OA lo valora OP y DS añade duración y lo valora RA. |
| CAF-RF-021 | — | Sin otro hallazgo formal. |
| CAF-RF-022 | CMP-11 | Hallazgo DS sobre «despacho» y contenido; OA lo interpreta con contexto. |
| CAF-RF-023 | CMP-12 | Coinciden en separar solicitud y aviso; diferencias en formulación de la dependencia temporal. |
| CAF-RF-024 | — | Sin otro hallazgo formal. |
| CAF-RNF-001 | — | Sin otro hallazgo formal. |
| CAF-RNF-002 | — | Sin otro hallazgo formal; diferencia de justificación sobre cuantificación indicada en §3.1. |

## 5. Decisiones del equipo y ajustes posteriores

Las decisiones siguientes proceden de la revisión de CMP-01 a CMP-12 realizada con el equipo en esta conversación. Las justificaciones resumen las explicaciones aceptadas junto con cada opción; no son nuevas evaluaciones ni citas literales del equipo. Cada observación conserva su fuente, su valoración original en §2 y su decisión individual, aunque comparta tema con otra.

La aceptación de una aclaración no significa aceptar automáticamente toda la propuesta original del modelo. En las aceptaciones parciales se distingue la parte acordada de las formulaciones o precisiones que no se adoptan. §5.1 recoge las acciones y los textos confirmados; una acción acordada sin enunciado íntegro confirmado no se presenta como una redacción literal aprobada.

Las decisiones no cambian retrospectivamente las valoraciones de v2. Se ha preparado [requisitos v3](requisitos-v3.md) con las acciones y los textos acordados; la columna de aplicación indica los requisitos de destino. Los ajustes posteriores se registran en su propia columna, sin sobrescribir el hallazgo ni confundir una propuesta original con el texto acordado. El equipo ha confirmado posteriormente la revisión final de v3 y, tras revisar la comparativa y la valoración crítica, el cierre del ejercicio.

| Registro | Fuente / observación | Tema | Decisión del equipo | Justificación del equipo | Redacción o acción acordada | Ajuste posterior a la decisión | Aplicación a v3 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| E3-001 | OA — INC-OBS-001 | CMP-01 | Limitación confirmada; adopción de patrón aplazada | El equipo confirma que no hay patrón acordado y que no lo implantará ahora por el alcance acotado; podrá considerarlo en el futuro. | Mantener los enunciados por este motivo y dejar R1 sin comprobar; no declarar conformidad ni imponer una plantilla. Véase §5.1, CMP-01. | Sin ajuste posterior registrado | Limitación recogida en la introducción de v3; sin cambio por R1 |
| E3-002 | DS — INC-OBS-001 | CMP-02 | Aceptar parcialmente | Se acepta explicitar la regla complementaria de cambio de bebida; no se acepta automáticamente la redacción original de DS como definitiva. | Conservar CAF-RF-003 e incorporar CAF-RF-003A con la regla confirmada de cancelar e iniciar una nueva operación; véase §5.1, CMP-02. | Tras la aceptación parcial, el equipo confirma expresamente el ID CAF-RF-003A y el nuevo texto propuesto en la conversación. | Aplicada: CAF-RF-003 y CAF-RF-003A; descripción y comprobación repartidas |
| E3-003 | OA — INC-OBS-002 | CMP-03 | Aceptar parcialmente | Conviene explicitar el momento de actualización ya documentado, manteniendo el número real comunicado por los mecanismos y sin añadir un plazo. | Indicar que el descuento se actualiza al finalizar la preparación, incluso si falla. Se acuerda la acción, no un enunciado íntegro literal; véase §5.1, CMP-03. | Sin ajuste posterior registrado | Aplicada: CAF-RF-009, redactado conforme a la acción acordada |
| E3-004 | DS — INC-OBS-002 | CMP-04 | Aceptar parcialmente | Se mejora la precisión de «comprobada la disponibilidad» sin cambiar el flujo ni introducir una condición de negocio nueva. | Explicitar que se ha comprobado que la bebida está disponible antes de solicitar el pago. Véase §5.1, CMP-04. | Sin ajuste posterior registrado | Aplicada: CAF-RF-010, redactado conforme a la acción acordada |
| E3-005 | OA — INC-OBS-003 | CMP-05 | Aceptar | Las dos asociaciones son comprobables de forma independiente; el equipo acepta separarlas y confirma los dos textos. | CAF-RF-015A y CAF-RF-015B, origen CAF-RF-015, con los textos de §5.1, CMP-05. Los IDs definitivos acordados no llevan guion antes de A/B. | Sin ajuste posterior registrado | Aplicada: CAF-RF-015A y CAF-RF-015B |
| E3-006 | DS — INC-OBS-003 | CMP-05 | Aceptar | Se acepta el mismo hallazgo de singularidad y la separación; la formulación definitiva es la confirmada por el equipo, no toda alternativa original de DS. | CAF-RF-015A y CAF-RF-015B, con «permitir vincular cada solicitud» en el segundo. Véase §5.1, CMP-05. | Sin ajuste posterior registrado | Aplicada: CAF-RF-015A y CAF-RF-015B |
| E3-007 | DS — INC-OBS-004 | CMP-06 | Aceptar | Expresar el intervalo continuo evita excluir la cancelación después de elegir y antes de solicitar autorización, sin ampliar la regla de negocio. | Adoptar el texto confirmado de CAF-RF-014 en §5.1, CMP-06; conservar la ventana tras denegación. | Sin ajuste posterior registrado | Aplicada: CAF-RF-014 |
| E3-008 | DS — INC-OBS-005 | CMP-07 | Aceptar | Se aplica la misma precisión de resultado positivo que en CMP-04, conservando las demás condiciones del inicio. | Explicitar disponibilidad positiva, pago autorizado y ausencia de fallo comunicado que impida entregar. Véase §5.1, CMP-07. | Sin ajuste posterior registrado | Aplicada: CAF-RF-017, redactado conforme a la acción acordada |
| E3-009 | DS — INC-OBS-006 | CMP-08 | Aceptar parcialmente | Se acepta precisar una acción observable del software, limitada al envío de las cantidades; no una garantía de consumo o medición física. | Adoptar la aclaración confirmada de CAF-RF-018 en §5.1, CMP-08, en lugar de la alternativa original «de modo que se utilicen». | Sin ajuste posterior registrado | Aplicada: CAF-RF-018 |
| E3-010 | OA — INC-OBS-004 | CMP-09 | Aceptar | Se acepta explicitar la vinculación con la compra en curso, sin fijar cuándo ocurre la dispensación física. | Adoptar CAF-RF-019 con «Para la operación de compra en curso», según §5.1, CMP-09, en lugar de imponer «durante la preparación». | Sin ajuste posterior registrado | Aplicada: CAF-RF-019 |
| E3-011 | OA — INC-OBS-005 | CMP-10 | Aceptar | El contenido «la bebida se está preparando» debe quedar explícito y no depender solo del criterio de comprobación. | Adoptar el texto confirmado de CAF-RF-020 en §5.1, CMP-10, sin fijar persistencia ni frecuencia. | Sin ajuste posterior registrado | Aplicada: CAF-RF-020 |
| E3-012 | DS — INC-OBS-007 | CMP-10 | Aceptar parcialmente | Se acepta aclarar el contenido; no se adopta una exigencia adicional de aviso único, persistente o periódico. | Mismo texto de CAF-RF-020 que E3-011. No se fija persistencia ni frecuencia; véase §5.1, CMP-10. | Sin ajuste posterior registrado | Aplicada en su parte aceptada: CAF-RF-020 |
| E3-013 | DS — INC-OBS-008 | CMP-11 | Aceptar | Se sustituye el término «despacho» por un mensaje explícito que conserva fin del servicio y ausencia de entrega. | Adoptar el texto confirmado de CAF-RF-022 y ajustar su comprobación para verificar ese contenido. Véase §5.1, CMP-11. | Sin ajuste posterior registrado | Aplicada: CAF-RF-022 y su comprobación |
| E3-014 | OA — INC-OBS-006 | CMP-12 | Aceptar | Solicitar devolución y comunicarla son acciones independientes; se confirma que el aviso depende de una solicitud efectuada. | CAF-RF-023A y CAF-RF-023B, origen CAF-RF-023, con los textos de §5.1, CMP-12. Los IDs definitivos acordados no llevan guion antes de A/B. | Sin ajuste posterior registrado | Aplicada: CAF-RF-023A y CAF-RF-023B |
| E3-015 | DS — INC-OBS-009 | CMP-12 | Aceptar | Se acepta la separación y se resuelve la cuestión de secuencia con «Una vez solicitada la devolución prevista en CAF-RF-023A». | Mismos IDs y textos que E3-014; se conserva la relación con el intento autorizado y no se garantiza el resultado bancario. Véase §5.1, CMP-12. | Sin ajuste posterior registrado | Aplicada: CAF-RF-023A y CAF-RF-023B |

La decisión de CMP-01 también recoge la limitación R1 descrita por DS en §3 de su respuesta. No se le asigna un ID de observación inexistente. Confirmar esa limitación no equivale a aprobar R1.

### 5.1. Acciones y redacciones acordadas por tema

#### CMP-01 — Patrón R1 (E3-001)

El equipo confirma: «no hay un patrón acordado» y «en un futuro se puede implementar; ahora no». Se conserva la limitación de comprobación de R1. No se adopta una plantilla nueva ni se modifican los 26 enunciados por este motivo. La posible adopción futura no constituye una tarea comprometida para esta fase.

#### CMP-02 — Cambio de bebida (E3-002)

Se acepta parcialmente explicitar la regla complementaria en un requisito separado. Se mantiene CAF-RF-003 para la bebida no disponible. La regla complementaria debe conservar la cancelación y el inicio de una nueva operación en los demás casos, respetando las restricciones de autorización ya documentadas.

**Confirmación posterior a la aceptación parcial:** el equipo confirma el ID **CAF-RF-003A**, origen **CAF-RF-003**, y el siguiente texto:

> Cuando la bebida seleccionada esté disponible, el sistema deberá exigir al cliente cancelar la operación actual antes de permitirle seleccionar otra bebida en una nueva operación de compra.

Esta confirmación resuelve el texto y el ID que habían quedado pendientes. La decisión original sigue siendo una aceptación parcial del hallazgo DS; no implica aceptar retrospectivamente su alternativa íntegra. En v3 se conserva el enunciado de CAF-RF-003 y se distribuyen las descripciones y comprobaciones entre ambos requisitos, con referencia a CAF-RF-014 y CAF-RF-016 para las restricciones de cancelación.

#### CMP-03 — Descuento de vasos (E3-003)

Se acepta parcialmente explicitar que el descuento se actualiza **al finalizar la preparación, incluso si falla**, usando el número real de vasos comunicado por los mecanismos. No se añade un plazo de actualización ni se cambia la política de consumo. Se conserva el ID CAF-RF-009.

Se acordó esta acción de reescritura; su enunciado íntegro se ha redactado en v3 conforme a ella, sin presentarlo como una confirmación literal adicional del equipo.

#### CMP-04 — Disponibilidad antes del pago (E3-004)

Se acepta parcialmente aclarar que la disponibilidad debe confirmarse antes de solicitar el pago, expresando **«una vez comprobado que está disponible»**. Se mantienen el terminal, el precio de la bebida seleccionada y el flujo ya previsto. No se interpreta como una condición de negocio nueva. Se conserva el ID CAF-RF-010; el enunciado íntegro se ha preparado en v3 conforme a esta acción.

#### CMP-05 — Asociaciones de pago (E3-005 y E3-006)

El equipo acepta la separación y confirma expresamente los siguientes IDs y textos para v3:

- **CAF-RF-015A**, origen **CAF-RF-015**: «El sistema deberá asociar cada resultado de autorización recibido del terminal con el intento de pago correspondiente.»
- **CAF-RF-015B**, origen **CAF-RF-015**: «El sistema deberá permitir vincular cada solicitud de devolución con el intento de pago autorizado que la origina.»

La comprobación se repartirá entre la asociación de resultados de autorización y denegación con sus intentos (015A) y el vínculo de la solicitud de devolución con el intento autorizado correcto (015B). Se mantiene la libertad sobre qué componente conserva la referencia. Los IDs con guion `015-A` y `015-B` permanecen únicamente como propuestas originales de OA en §2.

#### CMP-06 — Ventana de cancelación (E3-007)

Se acepta la aclaración y la redacción propuesta para **CAF-RF-014**:

> El sistema deberá permitir cancelar la operación desde el inicio de la selección hasta antes de iniciar una solicitud de autorización, o tras recibir una denegación y antes de otro intento.

Se conserva la ventana posterior a una denegación. La aclaración incluye el intervalo posterior a elegir la bebida y previo a solicitar autorización; no habilita cancelaciones con autorización pendiente o aprobada.

#### CMP-07 — Disponibilidad antes de preparar (E3-008)

Se acepta explicitar que la comprobación de disponibilidad debe ser **positiva**, además de exigir pago autorizado y ausencia de un fallo comunicado que impida entregar la bebida. Se conserva CAF-RF-017 y la coherencia con la aclaración de CAF-RF-010. Se ha aplicado esta acción al enunciado íntegro de v3 sin eliminar ninguna precondición.

#### CMP-08 — Coordinación de preparación (E3-009)

Se acepta parcialmente la observación y se confirma la siguiente aclaración para **CAF-RF-018**:

> El sistema deberá coordinar la preparación de la bebida seleccionada enviando a los mecanismos de preparación las cantidades de ingredientes indicadas en su receta.

La obligación se concreta en el envío de las cantidades por el software; no en medir ni garantizar el consumo físico. Se adapta la propuesta original del modelo a este límite del sistema.

#### CMP-09 — Orden de vaso (E3-010)

Se acepta aclarar la pertenencia de la orden a la compra en curso. Se confirma para **CAF-RF-019**:

> Para la operación de compra en curso, el sistema deberá ordenar la dispensación de un vaso para entregar la bebida preparada.

Se adapta la propuesta original de OA: no se impone la expresión «durante la preparación» ni se fija el momento físico de dispensación.

#### CMP-10 — Aviso de preparación (E3-011 y E3-012)

Se acepta aclarar el contenido para **CAF-RF-020** con este texto:

> Durante la preparación, el sistema deberá informar al cliente de que la bebida se está preparando.

La decisión acepta el hallazgo sobre contenido de ambos modelos. La observación de DS se acepta parcialmente: no se adopta una exigencia de persistencia o frecuencia, ni se elige entre aviso único, continuo o periódico. Esas características quedan sin fijar; no se presentan como una decisión aceptada por omisión.

#### CMP-11 — Servicio terminado sin entrega (E3-013)

Se acepta sustituir «despacho» por una formulación explícita. Se confirma para **CAF-RF-022**:

> Si, tras autorizarse el pago, un fallo impide entregar la bebida en cualquier etapa, el sistema deberá informar al cliente de que el servicio terminó sin que la bebida se entregara.

La comprobación deberá verificar que el mensaje comunica el fin del servicio sin entrega. Se conserva la condición de fallo tras autorización y se adapta la alternativa original para comunicar también que el servicio terminó.

#### CMP-12 — Devolución y aviso (E3-014 y E3-015)

El equipo acepta la separación y confirma expresamente los siguientes IDs y textos:

- **CAF-RF-023A**, origen **CAF-RF-023**: «Si, tras autorizarse el pago, un fallo impide entregar la bebida, el sistema deberá solicitar la devolución íntegra del importe asociado al intento autorizado.»
- **CAF-RF-023B**, origen **CAF-RF-023**: «Una vez solicitada la devolución prevista en CAF-RF-023A, el sistema deberá comunicar al cliente que la devolución fue solicitada.»

La segunda obligación depende explícitamente de la solicitud de la primera. Se conserva la devolución íntegra asociada al intento autorizado, sin afirmar que el reintegro ya se haya procesado. Se mantienen las exclusiones del procesamiento bancario y de fallos de la solicitud de devolución. Los IDs con guion `023-A` y `023-B` se conservan únicamente en las propuestas originales de OA.

### 5.2. Aplicación a requisitos v3

Se ha preparado [requisitos-v3.md](requisitos-v3.md) con **27 requisitos funcionales y 2 no funcionales**: se añade CAF-RF-003A y las dos separaciones aumentan en uno el número de requisitos cada una. CAF-RF-015 y CAF-RF-023 se mantienen como orígenes, no como requisitos activos duplicados en v3.

Los IDs y textos confirmados se incorporan literalmente. CAF-RF-009, CAF-RF-010 y CAF-RF-017 se redactan conforme a las acciones acordadas; su preparación no se presenta como una aprobación literal adicional. Se adaptan las descripciones y comprobaciones afectadas y se conservan íntegramente las filas no afectadas. El apartado 4 de v3 relaciona cada revisión con los registros E3 correspondientes.

Las comprobaciones son previstas, no ejecutadas. El equipo ha confirmado la revisión final de la versión y el cierre del ejercicio 3, sin declarar conformidad con R1.

## 6. Resumen y siguiente paso

- Se han registrado **15 hallazgos originales**: 6 de OA y 9 de DS, en **12 temas**. Las tres parejas de observaciones formales coincidentes se refieren a CAF-RF-015, CAF-RF-020 y CAF-RF-023; en CAF-RF-020 la coincidencia es parcial por la duración del aviso.
- La limitación de R1 también es compartida, pero DS la documenta sin un `INC-OBS` formal. Se conserva su diferencia de etiquetado.
- Se registran **2 hallazgos específicos solo de OA** (CAF-RF-009 y CAF-RF-019) y **6 solo de DS** (CAF-RF-003, 010, 014, 017, 018 y 022). «Solo» indica su procedencia, no su validez.
- **Decisiones registradas:** los 12 temas se han revisado y los 15 registros tienen decisión. Se distinguen aceptaciones, aceptaciones parciales y la limitación confirmada de R1 con adopción de patrón aplazada. Las decisiones compartidas siguen vinculadas a cada observación de origen.
- **Concreción confirmada:** el equipo ha confirmado CAF-RF-003A y su texto complementario. Se conserva el hallazgo DS original y se distingue la confirmación posterior de la aceptación parcial inicial.
- **V3 revisada por el equipo:** se han incorporado los textos confirmados de §5.1 y redactado CAF-RF-009, CAF-RF-010 y CAF-RF-017 conforme a las acciones acordadas, conservando los requisitos no afectados, los orígenes de las separaciones y las descripciones y comprobaciones correspondientes. El equipo ha confirmado su revisión final.
- El patrón R1 queda sin adoptar en esta fase y su conformidad no puede comprobarse. La persistencia y la frecuencia del aviso de CAF-RF-020 quedan sin fijar; no se registran como exigencias nuevas.
- Las decisiones no cambian retrospectivamente las valoraciones originales de v2. El equipo ha revisado la [comparativa con el ejercicio 2 y la valoración crítica](comparativa-evaluaciones.md) y ha confirmado el cierre del ejercicio 3, con las limitaciones documentadas.
