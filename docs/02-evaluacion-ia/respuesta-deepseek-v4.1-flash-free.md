# Evaluación general de requisitos — deepseek-v4.1-flash-free

- **Proveedor:** no especificado. El identificador de la sesión incluye `opencode`, pero no se ha podido confirmar un proveedor independiente.
- **Modelo:** `deepseek-v4.1-flash-free` (identificador exacto de la sesión: `opencode/deepseek-v4.1-flash-free`). No se dispone de una versión adicional.
- **Herramienta:** OpenCode.
- **Fecha:** 28 de octubre de 2026.
- **Prompt utilizado:** bloque «Prompt» de [prompt.md](prompt.md), facilitado por el usuario en esta conversación.
- **Versión de las fuentes del repositorio:** commit `474e10173ac51b4cdf0580cad8090bb53e51dcef`. El árbol no estaba limpio al iniciar la evaluación: había cambios locales en `README.md` y `prompt.md`, y `respuesta-gpt-sol.md` sin seguimiento. Los documentos evaluados, `contexto-y-alcance.md` y `requisitos-v1.md`, no figuraban como modificados.
- **Estado:** respuesta de IA pendiente de revisión y decisiones justificadas del equipo.

## 1. Documentos y limitaciones

He leído los tres documentos de entrada:

1. [Enunciado de la práctica](../enunciado/P1.docx.pdf), mediante extracción de texto. He revisado sus tres páginas y, en particular, el apartado 1.4 relativo al ejercicio 2.
2. [Contexto y alcance](../01-requisitos-iniciales/contexto-y-alcance.md), incluidos catálogo, recetas, límites, exclusiones, supuestos y decisiones comunicadas por el equipo.
3. [Requisitos iniciales v1](../01-requisitos-iniciales/requisitos-v1.md), incluidos el texto, la descripción, el módulo y el criterio «Cómo comprobarlo» de los 24 requisitos funcionales y los 2 no funcionales.

También he leído [README.md](../../README.md) como índice del repositorio, sin usarlo como fuente de requisitos.

Limitaciones:

- El contexto cita `documento_requisitos_v1.md` como referencia, pero ese archivo no se ha localizado en el repositorio. No puedo comprobar si el contexto reproduce fielmente ese documento; la evaluación se limita a contrastar `requisitos-v1.md` con el contexto disponible y con el enunciado.
- La evaluación es documental. Los criterios «Cómo comprobarlo» describen comprobaciones previstas; no se han ejecutado pruebas ni se ha comprobado una implementación o un dispositivo físico.
- La extracción del PDF es textual. La sección 1.4 es legible y no se ha detectado una pérdida relevante para esta tarea.
- La evaluación se refiere únicamente a `requisitos-v1.md`; no se han evaluado versiones posteriores.
- No se han usado como evidencia las evaluaciones previas de `docs/02-evaluacion-ia/`. Las observaciones siguientes se basan en la versión v1 y en el contexto.

**Aclaración posterior (28 de octubre de 2026):** la referencia a `documento_requisitos_v1.md` tenía un nombre incorrecto y no designaba un tercer documento histórico. Los documentos correctos de entrada fueron [Contexto y alcance](../01-requisitos-iniciales/contexto-y-alcance.md) y [Requisitos iniciales v1](../01-requisitos-iniciales/requisitos-v1.md), ambos leídos para esta evaluación. Por tanto, no existía una limitación de acceso a esas fuentes. Esta nota corrige la limitación consignada arriba y conserva la formulación original como evidencia de la evaluación generada.

Esta es una evaluación general del ejercicio 2. No es una evaluación frente a reglas INCOSE. Las propuestas siguientes no constituyen decisiones ni requisitos aprobados.

## 2. Cobertura de la revisión individual

Se han revisado los 26 requisitos frente a las seis categorías solicitadas, considerando conjuntamente sus cinco columnas y el contexto. «Sin problemas detectados» no equivale a aprobación. Una observación sobre el criterio de verificación no implica necesariamente que el texto del requisito sea incorrecto.

| ID | Resultado | Categorías con hallazgos | Referencias a hallazgos |
| --- | --- | --- | --- |
| CAF-RF-001 | Sin problemas detectados | — | — |
| CAF-RF-002 | Sin problemas detectados | — | — |
| CAF-RF-003 | Con observaciones | Información incompleta; falta de verificabilidad | H-001 |
| CAF-RF-004 | Con observaciones | Falta de verificabilidad | H-011 |
| CAF-RF-005 | Sin problemas detectados | — | — |
| CAF-RF-006 | Sin problemas detectados | — | — |
| CAF-RF-007 | Con observaciones | Ambigüedad; información incompleta | H-007 |
| CAF-RF-008 | Sin problemas detectados | — | — |
| CAF-RF-009 | Sin problemas detectados | — | — |
| CAF-RF-010 | Con observaciones | Información incompleta | H-010 |
| CAF-RF-011 | Con observaciones | Ambigüedad; información incompleta | H-004 |
| CAF-RF-012 | Con observaciones | Ambigüedad; información incompleta | H-004 |
| CAF-RF-013 | Con observaciones | Falta de verificabilidad | H-013 |
| CAF-RF-014 | Con observaciones | Ambigüedad; información incompleta | H-004 |
| CAF-RF-015 | Con observaciones | Ambigüedad; información incompleta; falta de verificabilidad | H-003, H-004, H-005, H-010 |
| CAF-RF-016 | Con observaciones | Ambigüedad; falta de verificabilidad | H-004, H-012 |
| CAF-RF-017 | Con observaciones | Ambigüedad; información incompleta | H-004 |
| CAF-RF-018 | Sin problemas detectados | — | — |
| CAF-RF-019 | Con observaciones | Contradicción; posible omisión | H-002 |
| CAF-RF-020 | Sin problemas detectados | — | — |
| CAF-RF-021 | Sin problemas detectados | — | — |
| CAF-RF-022 | Con observaciones | Contradicción; posible omisión; información incompleta | H-002, H-009 |
| CAF-RF-023 | Con observaciones | Contradicción; ambigüedad; información incompleta | H-002, H-003, H-009, H-010 |
| CAF-RF-024 | Con observaciones | Ambigüedad; falta de verificabilidad; información incompleta | H-005, H-009 |
| CAF-RNF-001 | Sin problemas detectados | — | — |
| CAF-RNF-002 | Sin problemas detectados | — | — |

**Balance:** 26 requisitos revisados, 15 con observaciones y 11 sin problemas detectados. Ninguno se clasifica globalmente como «No evaluable»: hay información para revisar sus obligaciones, aunque algunos detalles requieren aclaración.

H-006, sobre las existencias iniciales, es transversal a los requisitos de existencias; no se atribuye a una fila concreta porque los textos de `CAF-RF-004`, `CAF-RF-005`, `CAF-RF-006`, `CAF-RF-008` y `CAF-RF-009` son claros. La carencia está en los datos de partida y afecta a la puesta en marcha y a la reproducibilidad de las pruebas. H-008, sobre el alcance de las incidencias, también es transversal a la función de comunicación de incidencias.

## 3. Hallazgos detallados

### H-001. La regla de cambio de bebida está solo en la descripción de CAF-RF-003 y no se verifica

- **Requisito(s) o sección(es):** CAF-RF-003; [contexto y alcance](../01-requisitos-iniciales/contexto-y-alcance.md), §5.
- **Categoría:** información incompleta; falta de verificabilidad.
- **Naturaleza:** problema dentro del alcance ya acordado.
- **Evidencia:** el requisito dice: «Si la bebida seleccionada no está disponible, el sistema deberá permitir seleccionar otra bebida sin exigir una cancelación previa». La descripción añade: «La nueva selección sustituye a la anterior y se comprueba su disponibilidad antes de solicitar el pago. En los demás casos, cambiar de bebida requiere cancelar la operación mientras esté permitido». El criterio solo comprueba el caso de bebida no disponible: «Seleccionar un cortado sin café suficiente y después elegir un chocolate con existencias suficientes. Comprobar que se permite el cambio y se comprueba la nueva receta antes de solicitar el pago». El contexto repite la regla: «En los demás casos, cambiar de bebida requiere cancelar la operación actual mientras esté permitido e iniciar una nueva».
- **Justificación y consecuencia:** la regla de que cambiar de bebida en los demás casos exige cancelar es una obligación de comportamiento, pero está solo en la descripción y no se verifica. Además, el criterio no comprueba que la nueva selección sustituya realmente a la anterior. Una implementación que permita cambiar de bebida sin cancelar cuando la bebida está disponible o el pago está pendiente, o que mantenga la bebida anterior en la operación, podría pasar la comprobación descrita e incumplir el contexto.
- **Propuesta o pregunta para el equipo:** decidir si la regla se incorpora al texto de CAF-RF-003 o a un requisito independiente de cambio de selección, y añadir comprobaciones para el cambio sin cancelación y para la sustitución de la bebida anterior. Si no se quiere exigir, retirarla de la descripción.
- **Tipo de propuesta:** redacción y cambio de comportamiento.
- **¿Necesita decisión del equipo?:** sí. Hay que decidir el comportamiento esperado al cambiar de bebida y si la selección queda bloqueada después de la autorización.

### H-002. El fallo posterior a la preparación tiene cobertura distinta en CAF-RF-022, CAF-RF-023 y el contexto

- **Requisito(s) o sección(es):** CAF-RF-019, CAF-RF-022 y CAF-RF-023; [contexto y alcance](../01-requisitos-iniciales/contexto-y-alcance.md), §4 y §6.
- **Categoría:** contradicción; posible omisión.
- **Naturaleza:** problema dentro del alcance.
- **Evidencia:** CAF-RF-022 exige informar «Si un fallo **durante la preparación** impide entregar la bebida». CAF-RF-023 exige devolución «Si un fallo impide entregar una bebida ya cobrada», sin limitarlo a la preparación. El contexto indica: «Si un fallo impide entregar una bebida ya cobrada, se solicita la devolución íntegra» y «Si un fallo impide entregar una bebida cobrada, se informa al cliente y se solicita la devolución». CAF-RF-019 incluye la dispensación del vaso para entregar la bebida preparada.
- **Justificación y consecuencia:** un fallo posterior a la preparación pero anterior o durante la entrega, por ejemplo en el dispensador de vasos, impide entregar una bebida ya cobrada. En ese caso CAF-RF-023 obliga a solicitar la devolución, pero CAF-RF-022 no obliga a informar al cliente porque el fallo no ocurrió «durante la preparación». El cliente podría recibir una devolución sin saber por qué no se le entregó la bebida, y el requisito de comunicación quedaría incompleto respecto del contexto.
- **Propuesta o pregunta para el equipo:** decidir si CAF-RF-022 debe ampliar su disparador a «fallo que impida entregar una bebida ya cobrada», alineándolo con CAF-RF-023 y el contexto, o si el alcance se limita expresamente a fallos durante la preparación. En el primer caso, añadir un caso de prueba de fallo después de la preparación.
- **Tipo de propuesta:** cambio de comportamiento y redacción.
- **¿Necesita decisión del equipo?:** sí. Es una decisión de alcance y de comportamiento observable.

### H-003. «Bebida ya cobrada» frente a «pago autorizado»

- **Requisito(s) o sección(es):** CAF-RF-023, CAF-RF-015 y CAF-RF-010; [contexto y alcance](../01-requisitos-iniciales/contexto-y-alcance.md), §1 y §4.
- **Categoría:** ambigüedad; información incompleta.
- **Naturaleza:** problema dentro del alcance.
- **Evidencia:** CAF-RF-023 habla de «una bebida ya cobrada» y su comprobación dice «Cobrar 1,30 € por un chocolate». CAF-RF-015 habla de que «el terminal autoriza el pago». El contexto define «Autorización de pago» como el resultado que indica «si se autoriza el cobro» y añade que «el procesamiento bancario se realiza fuera de la aplicación». El contexto también usa «se ha cobrado una compra».
- **Justificación y consecuencia:** el software solo recibe del terminal una autorización o una denegación; no necesariamente conoce si el cobro se ha capturado o liquidado. «Cobrada» puede interpretarse como «pago autorizado» o como «importe efectivamente cargado». De esa interpretación depende cuándo se solicita la devolución. La comprobación «Cobrar 1,30 €» tampoco es observable si el software solo ve la autorización.
- **Propuesta o pregunta para el equipo:** definir si, en este alcance, «cobrada» equivale a «pago autorizado por el terminal» y usar esa terminología de forma consistente, o bien explicar cómo conoce el software el cobro efectivo si se refiere a la captura.
- **Tipo de propuesta:** redacción y aclaración.
- **¿Necesita decisión del equipo?:** sí. Determina el disparador de la devolución y lo que se puede comprobar.

### H-004. Condición de carrera entre cancelación y autorización o denegación

- **Requisito(s) o sección(es):** CAF-RF-011, CAF-RF-012, CAF-RF-014, CAF-RF-015, CAF-RF-016 y CAF-RF-017; [contexto y alcance](../01-requisitos-iniciales/contexto-y-alcance.md), §5.
- **Categoría:** ambigüedad; información incompleta.
- **Naturaleza:** problema dentro del alcance.
- **Evidencia:** CAF-RF-014 permite cancelar «mientras no haya recibido la autorización del pago». CAF-RF-016 impide cancelar «una vez recibida la autorización del pago». CAF-RF-015 regula la autorización que llega «después de haberse cancelado la operación». CAF-RF-012 exige informar «cuando el terminal deniegue el pago».
- **Justificación y consecuencia:** si la cancelación y la autorización, o la cancelación y una denegación, llegan simultáneamente o mientras una de las dos está en curso, los requisitos no definen qué evento prevalece. Los resultados posibles son incompatibles: cancelación aceptada con devolución, o cancelación rechazada con preparación. Tampoco se define si una denegación tardía tras cancelar debe mostrarse al cliente o ignorarse. Las pruebas no pueden determinar el resultado esperado en ese escenario.
- **Propuesta o pregunta para el equipo:** definir una regla de ordenación de eventos, por ejemplo si la cancelación solo es efectiva cuando se procesa antes de la autorización, y decidir qué se hace con una denegación tardía después de cancelar. No se propone una regla concreta porque es una decisión del equipo.
- **Tipo de propuesta:** cambio de comportamiento y aclaración.
- **¿Necesita decisión del equipo?:** sí. Es una condición de carrera con efectos distintos sobre el cobro y la preparación.

### H-005. «Finalizar la operación» y «no reactivar la compra» no son estados observables

- **Requisito(s) o sección(es):** CAF-RF-024 y CAF-RF-015; [contexto y alcance](../01-requisitos-iniciales/contexto-y-alcance.md), §6.
- **Categoría:** ambigüedad; falta de verificabilidad.
- **Naturaleza:** problema dentro del alcance.
- **Evidencia:** CAF-RF-024 exige «finalizar la operación sin iniciar automáticamente otra preparación», y su comprobación pide «comprobar que termina la operación sin emitir una nueva orden de preparación». La descripción de CAF-RF-015 afirma: «La autorización tardía no reactiva la compra ni inicia la preparación», pero su comprobación solo verifica la devolución y que no se inicia la preparación.
- **Justificación y consecuencia:** «finalizar la operación» y «no reactivar la compra» no se traducen en un estado observable. Una implementación podría dejar la transacción abierta o la pantalla en un estado de pago sin emitir una nueva orden de preparación y aun así pasar la comprobación. El cliente podría quedar sin poder iniciar una nueva compra o ver información obsoleta.
- **Propuesta o pregunta para el equipo:** definir el estado final observable de la operación —por ejemplo, operación cerrada, cliente devuelto a la selección o pantalla sin pago activo— y añadir una comprobación; o bien limitar el requisito a la obligación verificable de no iniciar otra preparación y retirar las afirmaciones de estado no verificadas.
- **Tipo de propuesta:** redacción y aclaración.
- **¿Necesita decisión del equipo?:** sí. Hay que decidir qué significa «operación finalizada» en la interfaz y en el estado interno.

### H-006. Faltan las existencias iniciales que el documento declara como datos de partida

- **Requisito(s) o sección(es):** introducción de [requisitos v1](../01-requisitos-iniciales/requisitos-v1.md); [contexto y alcance](../01-requisitos-iniciales/contexto-y-alcance.md), §3 y §5.
- **Categoría:** información incompleta.
- **Naturaleza:** aclaración necesaria; posible dato externo.
- **Evidencia:** `requisitos-v1.md` afirma: «El catálogo, los precios, las recetas y las existencias iniciales se proporcionan como datos de partida». El contexto repite: «El catálogo, los precios, las recetas y las existencias iniciales son datos de partida». Sin embargo, la tabla del §3 incluye catálogo, precios y recetas, pero no cantidades iniciales de café, leche, cacao, agua o vasos. Las comprobaciones de CAF-RF-004, CAF-RF-005, CAF-RF-008 y CAF-RF-009 usan cantidades concretas, pero no definen el estado inicial del sistema.
- **Justificación y consecuencia:** sin existencias iniciales no se puede establecer el estado de arranque de la máquina ni reproducir las pruebas de descuento de existencias. Cada implementación o prueba podría asumir valores distintos. El documento promete unos datos que no aparecen en los documentos de entrada.
- **Propuesta o pregunta para el equipo:** indicar dónde están definidas las existencias iniciales —archivo, anexo o configuración— o incorporarlas a los documentos. Aclarar si son datos de entrada de la aplicación o datos de prueba. No se proponen valores concretos porque no están sustentados por los documentos.
- **Tipo de propuesta:** documentación de datos de partida; si se exige que la aplicación los cargue o valide, incorporación de un requisito nuevo.
- **¿Necesita decisión del equipo?:** sí. Hay que decidir dónde viven esos datos y si forman parte del alcance.

### H-007. CAF-RF-007 no concreta si el aviso debe indicar el recurso que falta

- **Requisito(s) o sección(es):** CAF-RF-007.
- **Categoría:** ambigüedad; información incompleta.
- **Naturaleza:** problema dentro del alcance.
- **Evidencia:** el requisito exige informar «cuando la bebida seleccionada no esté disponible por falta de ingredientes o vasos». La descripción añade: «El cliente debe conocer el motivo por el que no puede continuar la compra». La comprobación solo pide «un aviso de falta de disponibilidad» y, para el caso sin vasos, «comprobar que también se informa de la incidencia».
- **Justificación y consecuencia:** un mensaje genérico de «bebida no disponible» satisface el texto y la comprobación, pero no necesariamente la descripción, que parece exigir el motivo. No queda claro si el cliente debe saber qué ingrediente o recurso falta. La implementación y la aceptación de la prueba pueden diferir.
- **Propuesta o pregunta para el equipo:** decidir si el aviso debe identificar el recurso que falta o si basta con indicar que la bebida no está disponible; alinear texto, descripción y comprobación.
- **Tipo de propuesta:** redacción y aclaración.
- **¿Necesita decisión del equipo?:** sí. Es una decisión sobre el contenido del mensaje al cliente.

### H-008. El alcance de «comunicación de incidencias» no está delimitado

- **Requisito(s) o sección(es):** [contexto y alcance](../01-requisitos-iniciales/contexto-y-alcance.md), §3 y §6; CAF-RF-007, CAF-RF-012 y CAF-RF-022.
- **Categoría:** posible omisión; aclaración necesaria.
- **Naturaleza:** aclaración necesaria; posible ampliación opcional.
- **Evidencia:** el contexto define «Comunicación de incidencias» como «Informar al cliente de las incidencias que afecten al servicio, así como del progreso y de la finalización de la preparación». El caso de uso «Consultar una incidencia comunicada por la máquina» añade: «El mensaje y las acciones posteriores dependen de la incidencia y del estado de la operación». Los requisitos solo regulan la falta de disponibilidad (CAF-RF-007), la denegación del pago (CAF-RF-012) y el fallo durante la preparación (CAF-RF-022).
- **Justificación y consecuencia:** el contexto presenta una función de comunicación de incidencias más amplia que los tres casos enumerados, pero no define qué otras incidencias existen ni si quedan fuera del alcance. Tampoco hay una exclusión expresa. No se puede valorar la completitud de la función ni saber si la implementación debe cubrir, por ejemplo, la falta de respuesta del terminal o un fallo de sensores o del dispensador fuera de la preparación. No se afirma que esos casos estén exigidos; se señala que el alcance no está cerrado.
- **Propuesta o pregunta para el equipo:** decidir si el alcance de incidencias se limita a los casos ya enumerados y ajustar el caso de uso del contexto, o si se añaden requisitos para otras incidencias que el equipo considere dentro del alcance. No se proponen incidencias concretas como exigidas.
- **Tipo de propuesta:** redacción y, si se amplía, requisito nuevo.
- **¿Necesita decisión del equipo?:** sí. Es una decisión de alcance.

### H-009. No está definido cómo detecta el software el fallo de preparación

- **Requisito(s) o sección(es):** supuesto de [requisitos v1](../01-requisitos-iniciales/requisitos-v1.md); [contexto y alcance](../01-requisitos-iniciales/contexto-y-alcance.md), §1 y §5; CAF-RF-022, CAF-RF-023 y CAF-RF-024.
- **Categoría:** información incompleta.
- **Naturaleza:** problema dentro del alcance; aclaración de supuesto.
- **Evidencia:** el supuesto dice: «Se supone que los mecanismos comunican al software las cantidades de ingredientes y vasos realmente consumidos, incluso ante un fallo». El contexto añade que los mecanismos comunican «las cantidades de ingredientes y el número de vasos realmente consumidos, incluso cuando la preparación falla». La comprobación de CAF-RF-022 pide «Introducir una señal de fallo del mecanismo de preparación que impida la entrega». El diagrama de límites habla de «lecturas de sensores y órdenes de preparación».
- **Justificación y consecuencia:** el supuesto garantiza las cantidades consumidas, pero no una señal de fallo ni un estado de error. Los requisitos de informar, devolver y finalizar dependen de que el software sepa que la preparación falló. Si los mecanismos solo comunican cantidades, el software podría no distinguir un fallo parcial de una finalización normal. La prueba introduce una «señal de fallo» que no está descrita en el límite ni en los supuestos.
- **Propuesta o pregunta para el equipo:** confirmar y documentar si los sensores o mecanismos comunican un estado o señal de fallo, o definir cómo se detecta el fallo a partir de las lecturas. Añadirlo al límite y a los supuestos, y ajustar las comprobaciones.
- **Tipo de propuesta:** aclaración y, si faltase, requisito de interfaz.
- **¿Necesita decisión del equipo?:** sí. Determina si los requisitos de fallo son verificables y qué información debe intercambiar la máquina.

### H-010. Falta la referencia que asocia un pago con su autorización tardía o su devolución

- **Requisito(s) o sección(es):** CAF-RF-010, CAF-RF-013, CAF-RF-015 y CAF-RF-023; [contexto y alcance](../01-requisitos-iniciales/contexto-y-alcance.md), §2.
- **Categoría:** información incompleta.
- **Naturaleza:** problema dentro del alcance.
- **Evidencia:** CAF-RF-010 solo exige solicitar «el cobro del precio de la bebida seleccionada». CAF-RF-015 y CAF-RF-023 exigen la devolución «al medio de pago utilizado». Sus comprobaciones piden una devolución «asociada a ese pago» y «asociada al pago original». CAF-RF-013 permite reintentos sin un número máximo de intentos. El contexto indica que el procesamiento bancario es externo y que la aplicación recibe el resultado del terminal.
- **Justificación y consecuencia:** con varios intentos de pago, posiblemente con tarjetas distintas, «el medio de pago utilizado» no identifica por sí solo el intento que se autorizó. Tampoco se define qué referencia de operación o de pago intercambia o conserva el software para solicitar la devolución correcta. Una implementación podría devolver el importe contra el intento equivocado o no poder asociar una autorización tardía con la operación cancelada.
- **Propuesta o pregunta para el equipo:** definir qué referencia de pago u operación se intercambia con el terminal y se conserva para las devoluciones, o aclarar si el terminal realiza esa asociación y cómo identifica la operación el software. No se prescribe un protocolo ni un formato concreto.
- **Tipo de propuesta:** aclaración y, si se concreta, requisito nuevo de interfaz.
- **¿Necesita decisión del equipo?:** sí. Afecta a la corrección de las devoluciones y a la trazabilidad de los intentos.

### H-011. CAF-RF-004 no cubre en su comprobación todos los ingredientes ni los ingredientes no usados

- **Requisito(s) o sección(es):** CAF-RF-004.
- **Categoría:** falta de verificabilidad.
- **Naturaleza:** problema dentro del alcance, en la cobertura de la comprobación.
- **Evidencia:** el requisito exige comprobar «las existencias de **cada ingrediente**». La descripción precisa: «Incluye el agua y los ingredientes de la receta, sin exigir ingredientes que esa bebida no utiliza». La comprobación solo prueba un caso con café, leche y agua suficientes y un caso con 6 g de café, es decir, solo la insuficiencia de café.
- **Justificación y consecuencia:** una implementación que compruebe únicamente el café, o que ignore el agua, podría pasar la comprobación descrita. Tampoco se prueba que una bebida que no usa un ingrediente no lo exija: por ejemplo, un chocolate sin café ni leche disponibles debería superar la comprobación. La verificación no cubre la obligación tal como está expresada.
- **Propuesta o pregunta para el equipo:** ampliar la comprobación con casos de leche insuficiente, agua insuficiente y una bebida que no usa un ingrediente, además del caso límite de cantidad exacta. Son casos derivados de las recetas del contexto; no requieren valores nuevos.
- **Tipo de propuesta:** mejora de verificación y redacción.
- **¿Necesita decisión del equipo?:** no para el comportamiento, que ya está claro; sí para aceptar la ampliación de la comprobación.

### H-012. CAF-RF-016 no cubre en su comprobación el periodo posterior a la preparación

- **Requisito(s) o sección(es):** CAF-RF-016.
- **Categoría:** falta de verificabilidad.
- **Naturaleza:** problema dentro del alcance, en la cobertura temporal de la comprobación.
- **Evidencia:** el requisito impide cancelar «una vez recibida la autorización del pago», sin limitarlo a la preparación. La comprobación solo pide intentar cancelar «antes de iniciar la preparación» y «durante la preparación».
- **Justificación y consecuencia:** la obligación se extiende a todo el periodo posterior a la autorización, incluido el momento en que la bebida ya está preparada o lista para recoger (CAF-RF-021). Una implementación que bloquee la cancelación antes y durante la preparación, pero la permita después, podría pasar la comprobación. El efecto de cancelar una bebida ya preparada no está definido.
- **Propuesta o pregunta para el equipo:** añadir un caso de intento de cancelación después de completar la preparación o cuando la bebida está lista para recoger, y comprobar que no se acepta.
- **Tipo de propuesta:** mejora de verificación.
- **¿Necesita decisión del equipo?:** no para el comportamiento; sí para aceptar la ampliación de la comprobación.

### H-013. CAF-RF-013 no demuestra la ausencia de un límite de intentos

- **Requisito(s) o sección(es):** CAF-RF-013.
- **Categoría:** falta de verificabilidad.
- **Naturaleza:** problema dentro del alcance, en la evidencia de verificación.
- **Evidencia:** el requisito exige reintentar «sin imponer un número máximo de intentos». La comprobación pide «Revisar que no existe un límite de intentos configurado».
- **Justificación y consecuencia:** revisar la configuración no descarta un límite embebido en el código o en otra capa. Probar un número finito de intentos tampoco demuestra que no exista un máximo. Una implementación con un límite fijo podría pasar la comprobación y incumplir el requisito.
- **Propuesta o pregunta para el equipo:** definir la evidencia aceptable —por ejemplo, inspección de la lógica de reintentos y de la configuración, o una prueba con un número definido más inspección— o reformular el requisito si lo que se quiere prohibir es solo un límite configurable. No se propone un número máximo porque el equipo ha decidido que no lo haya.
- **Tipo de propuesta:** mejora de verificación y redacción.
- **¿Necesita decisión del equipo?:** no para el comportamiento, que ya está decidido; sí para acordar la evidencia de verificación.

## 4. Observaciones sobre el conjunto

Las cinco funciones generales del enunciado están representadas: selección, pago, comprobación de existencias, preparación e información de incidencias. La secuencia selección → disponibilidad → pago → preparación → entrega está reflejada y es coherente con el contexto. Las recetas y los precios utilizados en los ejemplos coinciden con el catálogo: café con leche 1,20 €, cortado 1,10 €, chocolate 1,30 € y cortado 7 g de café, 4 g de leche y 60 ml de agua.

Resultado de la búsqueda de las seis categorías:

| Categoría | Resultado de la revisión |
| --- | --- |
| Ambigüedad | H-003: «cobrada» frente a «autorizado». H-004: orden entre cancelación y autorización o denegación. H-005: estados finales no observables. H-007: contenido mínimo del aviso de falta de disponibilidad. |
| Información incompleta | H-001: regla de cambio de bebida solo en la descripción. H-003: significado de «cobrada». H-004: denegación tardía y eventos simultáneos. H-006: existencias iniciales. H-009: detección del fallo. H-010: referencia de pago para devoluciones. |
| Falta de verificabilidad | H-001: cambio de bebida y sustitución no comprobados. H-004: resultado indeterminado ante eventos simultáneos. H-005: «finalizar» y «no reactivar» no observables. H-011: CAF-RF-004 solo prueba el café. H-012: CAF-RF-016 no prueba después de la preparación. H-013: la inspección de configuración no descarta un límite embebido. |
| Redundancia | No se detectan duplicaciones sin una diferencia relevante de obligación o condición. |
| Contradicción | H-002: el disparador de CAF-RF-022 es más estrecho que el del contexto y CAF-RF-023. H-003 es una inconsistencia terminológica y H-004 una condición no definida, no contradicciones lógicas directas. |
| Posible omisión | H-002: aviso ante un fallo posterior a la preparación que impide la entrega. H-008: otras incidencias del alcance no delimitadas. H-006 es un dato de partida ausente, no una omisión de comportamiento. |

La proximidad temática no constituye por sí sola redundancia:

- CAF-RF-004 y CAF-RF-005 comprueban recursos; CAF-RF-006 impide solicitar el pago y CAF-RF-007 informa al cliente. Sus resultados son diferentes.
- CAF-RF-011 prohíbe preparar sin autorización; CAF-RF-017 exige comenzar bajo las condiciones de la operación vigente. Expresan una prohibición y una obligación positiva complementarias.
- CAF-RF-015 cubre la autorización tardía de una operación cancelada; CAF-RF-023 cubre la falta de entrega por fallo de una bebida cobrada.
- CAF-RF-008 y CAF-RF-009 actualizan recursos distintos y se apoyan en el supuesto expreso de comunicación del consumo real.
- CAF-RF-022 y CAF-RF-024 comparten el fallo, pero una exige informar y la otra finalizar la operación.
- CAF-RNF-002 se solapa con los importes de CAF-RF-010, CAF-RF-015 y CAF-RF-023, pero añade una condición de precisión verificable; no se considera redundancia material.

Se respetan los límites acordados: una máquina, una bebida por compra, pago sin contacto, catálogo fijo, ausencia de administración y personalización, medición física fuera del alcance y fallos de la solicitud de devolución excluidos. No se considera un defecto que no haya un tiempo máximo para comunicar disponibilidad, ya que su ausencia es explícita. Tampoco se considera un defecto permitir reintentos de pago sin máximo; el criterio combina intentos observados con revisión de la existencia de un límite, aunque H-013 señala que esa revisión no demuestra por sí sola la ausencia de un límite embebido.

Sobre terminología y módulos: los módulos «Compra» e «Interfaz» no aparecen como funciones del contexto, y «Información al cliente» no coincide literalmente con «Comunicación de incidencias». El propio documento aclara que los módulos son agrupaciones por función, no componentes de una arquitectura; no se considera un defecto material, pero el equipo puede alinear los nombres si quiere facilitar la trazabilidad con el contexto.

Sobre verificación: los criterios son en general concretos y usan valores del catálogo. Las carencias principales son H-011, H-012 y H-013. La comprobación de CAF-RF-013 por inspección de configuración es una evidencia razonable, pero no demuestra por sí sola la ausencia de un límite embebido; se recoge en H-013.

Se incluyen dos posibles ampliaciones opcionales, no exigidas por los documentos: mostrar la disponibilidad en el catálogo antes de elegir y comunicar al cliente que se ha solicitado la devolución. Se formulan como preguntas en el apartado 5 y no se presentan como requisitos acordados.

**Valoración global:** `requisitos-v1.md` constituye una base coherente y mayoritariamente observable, con la secuencia de compra bien reflejada y los valores del catálogo correctamente utilizados. Los riesgos principales son la detección del fallo, la asociación de pagos y devoluciones, el límite cancelación/autorización y la delimitación de las incidencias. No se emite aprobación ni rechazo del conjunto; las observaciones se presentan para que el equipo decida.

## 5. Preguntas para el equipo

1. **H-001:** ¿debe impedirse cambiar de bebida sin cancelar cuando la bebida está disponible o el pago está pendiente? ¿Y después de la autorización? ¿La nueva selección debe sustituir siempre a la anterior?
2. **H-002:** ¿la obligación de informar por un fallo se aplica a cualquier fallo que impida entregar una bebida cobrada, incluido un fallo posterior a la preparación, o solo a los fallos ocurridos durante la preparación?
3. **H-003:** ¿«bebida cobrada» significa «pago autorizado por el terminal» o «importe efectivamente capturado»? Si es lo segundo, ¿cómo lo conoce el software?
4. **H-004:** si la cancelación y la autorización o denegación llegan a la vez o mientras una está en curso, ¿qué evento prevalece? ¿Debe ignorarse una denegación tardía después de cancelar?
5. **H-005:** ¿qué estado observable debe alcanzar la operación al «finalizar» o «no reactivarse»? ¿Debe volver a la selección, cerrar la transacción o quedar en otro estado?
6. **H-006:** ¿dónde están definidas las existencias iniciales? ¿Son datos de entrada de la aplicación, datos de prueba o quedan pendientes de definir?
7. **H-007:** ¿el aviso de no disponibilidad debe indicar qué ingrediente o recurso falta, o basta con un mensaje genérico?
8. **H-008:** ¿qué incidencias adicionales, si alguna, entran en el alcance de comunicación? ¿Se limita el alcance a las ya enumeradas?
9. **H-009:** ¿los sensores o mecanismos comunican un estado o señal de fallo, o solo cantidades consumidas? ¿Cómo debe detectar el software que la preparación ha fallado?
10. **H-010:** ¿qué referencia de pago u operación se intercambia con el terminal y se conserva para asociar una autorización tardía o una devolución con el intento correcto, especialmente después de varios reintentos?
11. **H-011, H-012 y H-013:** ¿se aceptan las ampliaciones de comprobación propuestas para CAF-RF-004, CAF-RF-016 y CAF-RF-013, o el equipo prefiere otra evidencia de verificación?
12. **Ampliación opcional:** ¿la necesidad de «conocer las bebidas disponibles y su precio antes de elegir» exige mostrar la disponibilidad en el catálogo, o basta con mostrar todo el catálogo e informar después de la selección como en CAF-RF-007?
13. **Ampliación opcional:** ¿debe informarse al cliente de que se ha solicitado la devolución, además de avisar de que el servicio no se completó?

**Comprobación final:** la tabla contiene los 24 IDs funcionales y los 2 no funcionales, una sola vez cada uno. Se han buscado las seis categorías; los trece hallazgos contienen evidencia, justificación y propuestas o preguntas. Se distinguen problemas del alcance, aclaraciones necesarias y ampliaciones opcionales. Todas las observaciones quedan pendientes de revisión del equipo; no se ha creado una versión revisada de los requisitos ni se han modificado los documentos fuente.

**Aclaración posterior sobre la denominación (28 de octubre de 2026):** la referencia histórica al modelo y la ruta `respuesta-gpt-sol.md` en esta evidencia corresponden a OpenAI, modelo `openai/gpt-6.1-sol`. Se conserva la redacción original de la evaluación; el archivo de respuesta se identifica ahora como `respuesta-openai-gpt-6.1-sol.md`.
