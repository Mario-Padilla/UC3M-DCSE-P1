# Evaluación general de requisitos — gpt-6.1-sol
- **Modelo:** `openai/gpt-6.1-sol`
- **Herramienta:** OpenCode.
- **Fecha:** 28 de octubre de 2026.
- **Prompt utilizado:** bloque «Prompt» de [prompt.md](prompt.md), facilitado por el usuario en esta conversación.
- **Versión de las fuentes del repositorio:** commit `474e10173ac51b4cdf0580cad8090bb53e51dcef`, sin cambios locales al iniciar la evaluación.
- **Estado:** respuesta de IA pendiente de revisión y decisiones justificadas del equipo.

## 1. Documentos y limitaciones

He leído los tres documentos de entrada:

1. [Enunciado de la práctica](../enunciado/P1.docx.pdf), sus tres páginas, especialmente el apartado 1.4 relativo al ejercicio 2.
2. [Contexto y alcance](../01-requisitos-iniciales/contexto-y-alcance.md), incluidos catálogo, recetas, exclusiones, supuestos y decisiones comunicadas por el equipo.
3. [Requisitos iniciales v1](../01-requisitos-iniciales/requisitos-v1.md), incluidos el texto, la descripción, el módulo y el criterio «Cómo comprobarlo» de los 24 requisitos funcionales y los 2 no funcionales.

La evaluación es documental. Los criterios de verificación son comprobaciones previstas; no se han ejecutado pruebas ni se ha comprobado una implementación o un dispositivo físico. No se ha consultado el documento histórico `documento_requisitos_v1.md`, mencionado como fuente en el contexto, porque no forma parte de los tres documentos de entrada disponibles. Se evalúa la versión actual del repositorio, no ese antecedente.

**Aclaración posterior (28 de octubre de 2026):** la referencia a `documento_requisitos_v1.md` tenía un nombre incorrecto y no designaba un tercer documento histórico. Los documentos correctos de entrada fueron [Contexto y alcance](../01-requisitos-iniciales/contexto-y-alcance.md) y [Requisitos iniciales v1](../01-requisitos-iniciales/requisitos-v1.md), ambos leídos para esta evaluación. Por tanto, no existía una limitación de acceso a esas fuentes. Se conserva la formulación original de la respuesta como evidencia de la evaluación generada.

Esta es una evaluación general del ejercicio 2. No es una evaluación frente a reglas INCOSE. Las propuestas siguientes no constituyen decisiones ni requisitos aprobados.

## 2. Cobertura de la revisión individual

Se han revisado los 26 requisitos frente a las seis categorías solicitadas, considerando conjuntamente sus cinco columnas y el contexto. «Sin problemas detectados» no equivale a aprobación. Una observación sobre el criterio de verificación no implica necesariamente que el texto del requisito sea incorrecto.

| ID | Resultado | Categorías con hallazgos | Referencias a hallazgos |
| --- | --- | --- | --- |
| CAF-RF-001 | Sin problemas detectados | — | — |
| CAF-RF-002 | Sin problemas detectados | — | — |
| CAF-RF-003 | Sin problemas detectados | — | — |
| CAF-RF-004 | Sin problemas detectados | — | — |
| CAF-RF-005 | Sin problemas detectados | — | — |
| CAF-RF-006 | Sin problemas detectados | — | — |
| CAF-RF-007 | Con observaciones | Ambigüedad; información incompleta | H-001 |
| CAF-RF-008 | Sin problemas detectados | — | — |
| CAF-RF-009 | Sin problemas detectados | — | — |
| CAF-RF-010 | Sin problemas detectados | — | — |
| CAF-RF-011 | Sin problemas detectados | — | — |
| CAF-RF-012 | Sin problemas detectados | — | — |
| CAF-RF-013 | Sin problemas detectados | — | — |
| CAF-RF-014 | Sin problemas detectados | — | — |
| CAF-RF-015 | Sin problemas detectados | — | — |
| CAF-RF-016 | Sin problemas detectados | — | — |
| CAF-RF-017 | Con observaciones | Información incompleta | H-002 |
| CAF-RF-018 | Sin problemas detectados | — | — |
| CAF-RF-019 | Con observaciones | Información incompleta | H-003 |
| CAF-RF-020 | Sin problemas detectados | — | — |
| CAF-RF-021 | Con observaciones | Información incompleta | H-003 |
| CAF-RF-022 | Con observaciones | Posible omisión | H-002 |
| CAF-RF-023 | Sin problemas detectados | — | — |
| CAF-RF-024 | Con observaciones | Posible omisión | H-002 |
| CAF-RNF-001 | Sin problemas detectados | — | — |
| CAF-RNF-002 | Sin problemas detectados | — | — |

**Balance:** 26 requisitos revisados, 6 con observaciones y 20 sin problemas detectados. Ninguno se clasifica globalmente como «No evaluable»: hay información para revisar sus obligaciones, aunque algunos detalles requieren aclaración. CAF-RF-023 sirve como evidencia de H-002; su obligación de solicitar la devolución sí cubre expresamente el escenario señalado.

## 3. Hallazgos detallados

### H-001. El aviso de falta de disponibilidad no precisa si debe comunicar la causa

- **Requisito(s) o sección(es):** CAF-RF-007; contexto y alcance, apartado 2, «Necesidades de los interesados».
- **Categoría:** ambigüedad e información incompleta.
- **Naturaleza:** aclaración necesaria.
- **Evidencia:** el texto de CAF-RF-007 pide «informar al cliente cuando la bebida seleccionada no esté disponible por falta de ingredientes o vasos»; su descripción añade que «el cliente debe conocer el motivo». El criterio solo exige «un aviso de falta de disponibilidad» y comprobar que «también se informa de la incidencia» al faltar vasos. El contexto incluye la necesidad de «conocer el motivo si no se entrega la bebida».
- **Justificación y consecuencia:** hay dos interpretaciones razonables: mostrar un aviso genérico de bebida no disponible, o identificar que faltan ingredientes o vasos. El criterio actual puede dar por válida la primera, aunque la descripción parece exigir la segunda. Tampoco se determina si, al faltar ingredientes, basta con esa categoría o debe identificarse el ingrediente concreto. Esto permite resultados diferentes en la interfaz y en su aceptación.
- **Propuesta o pregunta para el equipo:** ¿el aviso debe distinguir falta de ingredientes y falta de vasos? En el primer caso, ¿debe identificar el ingrediente o basta con indicar la categoría? Tras resolverlo, alinear el texto y el criterio con el nivel de detalle acordado, sin inventar mensajes literales.
- **Tipo de propuesta:** redacción del requisito y su criterio; si el equipo exige un detalle no contemplado hasta ahora, deberá reconocerlo como concreción de comportamiento.
- **¿Necesita decisión del equipo?:** sí, porque los documentos no fijan inequívocamente la información mínima del aviso.

### H-002. El fallo posterior al cobro y anterior a la preparación tiene cobertura parcial

- **Requisito(s) o sección(es):** CAF-RF-017, CAF-RF-022 y CAF-RF-024; CAF-RF-023 como evidencia del escenario; contexto y alcance, apartado 6, caso de uso «Solicitar la preparación de una bebida».
- **Categoría:** información incompleta y posible omisión.
- **Naturaleza:** problema dentro del alcance.
- **Evidencia:** CAF-RF-023 exige devolución si «un fallo impide entregar una bebida ya cobrada» y su criterio incluye expresamente «un fallo anterior al inicio de la preparación y posterior al cobro». CAF-RF-022 y CAF-RF-024 limitan el aviso y la finalización a «un fallo durante la preparación». CAF-RF-017 ordena iniciar la preparación tras comprobar disponibilidad y autorizar el pago, «siempre que la operación no se haya cancelado». El caso de uso del contexto establece que, «si un fallo impide entregar una bebida cobrada, se informa al cliente y se solicita la devolución».
- **Justificación y consecuencia:** el escenario no es hipotético ni una ampliación: aparece expresamente en la verificación de CAF-RF-023. La devolución está cubierta, pero falta una obligación equivalente de aviso antes del inicio de la preparación. Tampoco queda determinado en los requisitos cómo finaliza la operación en ese caso ni cómo se inhibe el inicio exigido por CAF-RF-017 ante el fallo ya detectado. Una implementación podría solicitar la devolución y dejar la operación activa o no informar al cliente. No se afirma una contradicción demostrada: CAF-RF-023 no exige iniciar la preparación y las otras obligaciones pueden concretarse de forma compatible.
- **Propuesta o pregunta para el equipo:** extender la cobertura del aviso al fallo ya contemplado antes de preparar. Pedir al equipo que determine si ese fallo debe finalizar también la operación sin iniciar la preparación ni reintentarla automáticamente y, con esa decisión, alinear CAF-RF-017 y CAF-RF-024 o incorporar un requisito específico. Añadir comprobaciones del fallo posterior al cobro y previo a la preparación para aviso, estado final y ausencia de órdenes de preparación, además de la devolución ya prevista.
- **Tipo de propuesta:** redacción para cubrir el aviso ya descrito en el contexto; cambio de comportamiento o requisito nuevo para concretar el cierre y la inhibición del inicio, según decida el equipo.
- **¿Necesita decisión del equipo?:** sí, para validar la omisión y concretar el estado final y la actuación ante el fallo previo al inicio. No es necesario decidir aquí el tratamiento de fallos de devolución, que está excluido.

### H-003. La comprobación del aviso de recogida no distingue preparación y entrega efectiva

- **Requisito(s) o sección(es):** CAF-RF-019 y CAF-RF-021; contexto y alcance, apartados 3 y 6.
- **Categoría:** información incompleta en el criterio de verificación y en la condición de disponibilidad para recogida.
- **Naturaleza:** aclaración necesaria.
- **Evidencia:** CAF-RF-019 exige «ordenar la dispensación de un vaso» y su criterio solo comprueba que se emita la orden. CAF-RF-021 exige avisar «cuando la bebida esté lista para recoger», con una descripción que habla de «la preparación y la entrega»; su criterio pide «completar la preparación» y comprobar el aviso. El contexto distingue «preparación → entrega» y contempla fallos que impiden entregar la bebida.
- **Justificación y consecuencia:** emitir la orden de dispensación no demuestra que el vaso se haya dispensado, y finalizar la preparación no demuestra por sí solo que la bebida pueda recogerse. Queda por precisar si el evento de fin de preparación ya incluye la entrega correcta en vaso o si se necesita otra confirmación. En el primer caso, el criterio es suficiente solo si se documenta ese significado; en el segundo, el criterio puede aceptar un aviso prematuro mientras falla la entrega. La obligación de avisar cuando la bebida está lista es comprensible; el problema se centra en cómo identificar y comprobar ese estado en las interacciones del software.
- **Propuesta o pregunta para el equipo:** ¿qué información de los mecanismos confirma que la bebida está lista para recoger? ¿La finalización de preparación incluye la dispensación y la entrega correctas? Precisar el significado del evento o condición existente y comprobar que no se muestra el aviso de recogida cuando se comunica un fallo que impide la entrega. No se propone diseñar sensores ni exigir un mecanismo físico nuevo.
- **Tipo de propuesta:** redacción de la condición de activación y del criterio de verificación; si la información necesaria no existe en la interfaz prevista, su incorporación requerirá una decisión de comportamiento.
- **¿Necesita decisión del equipo?:** sí, porque no se documenta el significado de la confirmación de preparación/entrega recibida por el software.

## 4. Observaciones sobre el conjunto

Las cinco funciones generales del enunciado están representadas: selección, pago, comprobación de existencias, preparación e información de incidencias. Los módulos son coherentes con su definición como agrupaciones funcionales. Las recetas y los precios utilizados en los ejemplos coinciden con el catálogo.

Resultado de la búsqueda de las seis categorías:

| Categoría | Resultado de la revisión |
| --- | --- |
| Ambigüedad | H-001: contenido mínimo del aviso de falta de disponibilidad. |
| Información incompleta | H-001: detalle del aviso; H-002: actuación previa al inicio ante un fallo ya cobrado; H-003: condición y comprobación de bebida lista para recoger. |
| Falta de verificabilidad | No se detecta un requisito íntegramente no verificable con la información disponible. H-001 y H-003 afectan a la precisión o suficiencia de sus criterios; requieren concretarlos, no declarar imposible toda verificación. |
| Redundancia | No se detectan duplicaciones sin una diferencia relevante de obligación o condición. |
| Contradicción | No se detectan afirmaciones que exijan resultados incompatibles bajo las mismas condiciones. H-002 es una cobertura parcial que requiere completar la coordinación de obligaciones. |
| Posible omisión | H-002: aviso y cierre de la operación ante el fallo posterior al cobro y previo a la preparación; el aviso está respaldado explícitamente por el contexto y el cierre requiere decisión. |

La proximidad temática no constituye por sí sola redundancia:

- CAF-RF-004 y CAF-RF-005 comprueban recursos; CAF-RF-006 impide solicitar el pago y CAF-RF-007 informa al cliente. Sus resultados son diferentes.
- CAF-RF-011 prohíbe preparar sin autorización; CAF-RF-017 exige comenzar bajo las condiciones de la operación vigente. Expresan una prohibición y una obligación positiva complementarias.
- CAF-RF-015 cubre la autorización tardía de una operación cancelada; CAF-RF-023 cubre la falta de entrega por fallo de una bebida cobrada.
- CAF-RF-008 y CAF-RF-009 actualizan recursos distintos y se apoyan en el supuesto expreso de comunicación del consumo real.

Se respetan los límites acordados: una máquina, una bebida por compra, pago sin contacto, catálogo fijo, ausencia de administración y personalización, medición física fuera del alcance y fallos de la solicitud de devolución excluidos. No se considera un defecto que no haya un tiempo máximo para comunicar disponibilidad, ya que su ausencia es explícita. Tampoco se considera un defecto permitir reintentos de pago sin máximo; el criterio combina intentos observados con revisión de la existencia de un límite, por lo que no exige ejecutar infinitos intentos.

No se proponen ampliaciones opcionales: los hallazgos se refieren a obligaciones o escenarios existentes y a aclaraciones de sus interacciones. No hay base suficiente para exigir nuevas funcionalidades de explotación industrial o umbrales de calidad adicionales como parte de esta evaluación.

## 5. Preguntas para el equipo

1. **H-001:** ¿el aviso de falta de disponibilidad debe distinguir entre falta de ingredientes y falta de vasos? Cuando falte un ingrediente, ¿debe identificarlo o basta con indicar esa categoría?
2. **H-002:** ante un fallo posterior al cobro y anterior a la preparación, ¿debe finalizarse la operación sin iniciar ni reintentar automáticamente la preparación, además del aviso descrito en el contexto y la devolución ya exigida? ¿Se acepta completar los requisitos y sus criterios para cubrir ese escenario?
3. **H-003:** ¿qué información recibida de los mecanismos confirma que la bebida está lista para recoger? ¿El fin de preparación incluye entrega correcta en vaso, o son estados distintos que deben comprobarse por separado?

**Comprobación final:** la tabla contiene los 24 IDs funcionales y los 2 no funcionales, una sola vez cada uno. Se han buscado las seis categorías; los tres hallazgos contienen evidencia, justificación y propuestas o preguntas. Se distinguen problemas del alcance y aclaraciones necesarias. Todas las observaciones quedan pendientes de revisión del equipo; no se ha creado una versión revisada de los requisitos.
