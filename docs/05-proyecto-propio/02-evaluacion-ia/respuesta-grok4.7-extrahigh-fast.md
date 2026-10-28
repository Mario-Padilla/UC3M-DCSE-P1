# Evaluación general de requisitos — Grok 4.7

- **Proveedor:** SpaceXAI, según la identificación de la sesión en la que se generó esta evaluación. No consta otro proveedor que pueda confirmar.
- **Modelo:** Grok 4.7. No se facilitó un identificador de compilación, revisión ni alias de API más específico. El nombre de este archivo, `respuesta-grok4.7-extrahigh-fast.md`, es la denominación usada para archivarla; no es un identificador de modelo confirmado.
- **Herramienta:** Cursor, con lectura del repositorio local.
- **Fecha:** 28 de octubre de 2026.
- **Prompt utilizado:** bloque «Prompt» de [prompt.md](prompt.md).
- **Versión de las fuentes:** no se registró el commit del repositorio en la evaluación original. Los documentos citados entonces como `docs/05-proyecto-propio/contexto-y-alcance.md` y `docs/05-proyecto-propio/requisitos-v1.md` están ahora en [contexto y alcance](../01-requisitos-iniciales/contexto-y-alcance.md) y [requisitos iniciales v1](../01-requisitos-iniciales/requisitos-v1.md).
- **Estado:** respuesta original de IA. Las decisiones posteriores del equipo están en [evaluación y decisiones](evaluacion-y-decisiones.md) y no forman parte de esta evidencia.

## 1. Documentos y limitaciones

He leído estos tres documentos:

1. [Enunciado de la práctica](../../enunciado/P1.docx.pdf), completo (3 páginas, apartados 1.1 a 1.8). Para esta tarea he usado el apartado 1.4 y, por tratarse del proyecto del equipo, el 1.7. El texto del PDF se obtuvo por extracción; las tres páginas y los apartados son legibles.
2. [Contexto y alcance](../01-requisitos-iniciales/contexto-y-alcance.md), completo. En la evaluación se citó como `docs/05-proyecto-propio/contexto-y-alcance.md`.
3. [Requisitos iniciales v1](../01-requisitos-iniciales/requisitos-v1.md), completo: GMP-RF-001 a GMP-RF-015 y GMP-RNF-001 a GMP-RNF-004. En la evaluación se citó como `docs/05-proyecto-propio/requisitos-v1.md`.

No he podido leer `requisitos_sistema.md`, citado como fuente al inicio del contexto. Ese archivo no está en el repositorio. Tampoco están definidos, en ningún archivo del repositorio, los objetivos OE1, OE2 y OE3 que el contexto dice haber usado. La evaluación de necesidades, límites e interacciones se apoya solo en lo que el contexto y los requisitos recogen. No he usado el caso de la máquina de café ni evaluaciones de IA anteriores.

Esta es una evaluación general del ejercicio 2. No aplica reglas INCOSE ni sustituye la decisión del equipo. No es una aprobación, un rechazo ni una versión revisada de los requisitos.

## 2. Cobertura de la revisión individual

Hay 19 requisitos. Todos están en la tabla. «Con observaciones» indica un problema fundamentado; no es un rechazo del requisito. Ninguno ha quedado como «No evaluable»: en todos había texto suficiente para valorar la obligación y señalar qué dato falta.

| ID | Resultado | Categorías con hallazgos | Referencias a hallazgos |
| --- | --- | --- | --- |
| GMP-RF-001 | Con observaciones | Ambigüedad | H-001, H-002 |
| GMP-RF-002 | Con observaciones | Ambigüedad; información incompleta | H-003, H-004, H-016 |
| GMP-RF-003 | Con observaciones | Ambigüedad; posible omisión | H-005, H-006, H-036 |
| GMP-RF-004 | Con observaciones | Ambigüedad; falta de verificabilidad; posible omisión | H-007, H-008, H-034, H-036 |
| GMP-RF-005 | Con observaciones | Ambigüedad; posible omisión | H-009, H-035 |
| GMP-RF-006 | Con observaciones | Ambigüedad; información incompleta; posible omisión | H-010, H-011, H-012, H-013, H-036, H-037 |
| GMP-RF-007 | Con observaciones | Ambigüedad; información incompleta | H-014, H-015 |
| GMP-RF-008 | Con observaciones | Información incompleta; contradicción | H-017, H-018 |
| GMP-RF-009 | Con observaciones | Información incompleta; contradicción | H-018, H-019 |
| GMP-RF-010 | Con observaciones | Ambigüedad; contradicción | H-018, H-020 |
| GMP-RF-011 | Con observaciones | Ambigüedad; información incompleta; contradicción | H-021, H-022, H-023, H-030 |
| GMP-RF-012 | Con observaciones | Ambigüedad; falta de verificabilidad | H-024, H-025 |
| GMP-RF-013 | Con observaciones | Ambigüedad; contradicción | H-026, H-027 |
| GMP-RF-014 | Con observaciones | Ambigüedad; contradicción | H-027, H-028 |
| GMP-RF-015 | Con observaciones | Información incompleta; ambigüedad | H-029, H-031 |
| GMP-RNF-001 | Con observaciones | Contradicción; ambigüedad | H-030, H-031 |
| GMP-RNF-002 | Con observaciones | Falta de verificabilidad | H-032 |
| GMP-RNF-003 | Con observaciones | Ambigüedad | H-033 |
| GMP-RNF-004 | Con observaciones | Falta de verificabilidad | H-034 |

**Balance:** 19 requisitos revisados, todos con observaciones. Ninguno se clasifica como «Sin problemas detectados» ni como «No evaluable». «Con observaciones» no equivale a rechazo.

## 3. Hallazgos detallados

Hay observaciones fundamentadas en ambigüedad, información incompleta, falta de verificabilidad, contradicción y posible omisión. No he encontrado redundancia entre obligaciones. El reparto por categoría y los solapamientos que no considero redundantes están en la sección 4.

### H-001. Extracción de PDF y criterio «correctamente»

- **Requisito(s) o sección(es):** GMP-RF-001
- **Categoría:** ambigüedad
- **Naturaleza:** aclaración necesaria
- **Evidencia:** GMP-RF-001 admite «texto plano, Markdown y PDF». El criterio exige que «el contenido se extrae y visualiza correctamente».
- **Justificación y consecuencia:** «Correctamente» no fija el resultado comparable. Lectura A: basta con que los enunciados queden disponibles para segmentarlos, aunque cambie el maquetado. Lectura B: hay que recuperar el contenido de cualquier PDF, también de un PDF formado por imágenes. La lectura B añade reconocimiento de texto sobre imágenes; la A no. El mismo archivo puede cumplir o incumplir el criterio según la lectura.
- **Propuesta o pregunta para el equipo:** ¿Qué PDF es válido y qué debe coincidir entre el archivo y lo mostrado para dar por buena la extracción?
- **Tipo de propuesta:** redacción
- **¿Necesita decisión del equipo?:** sí. Los documentos no separan el PDF con texto extraíble del PDF de imagen ni el grado de fidelidad.

### H-002. Alcance de la especificación ingerida

- **Requisito(s) o sección(es):** GMP-RF-001, GMP-RF-002; glosario del contexto
- **Categoría:** ambigüedad
- **Naturaleza:** aclaración necesaria
- **Evidencia:** GMP-RF-001 habla de «documentos de requisitos de ciberseguridad». Su descripción dice: «Carga la especificación funcional y de seguridad». El glosario define el requisito de ciberseguridad como una «declaración funcional o de seguridad» que especifica una regla de control de acceso o una restricción de autorización. GMP-RF-002 segmenta «los requisitos individuales» sin repetir ese filtro.
- **Justificación y consecuencia:** Lectura A: solo entran enunciados que expresan control de acceso, aunque estén redactados como frase funcional. Lectura B: se carga y se segmenta la especificación funcional completa, incluidos enunciados ajenos al acceso. Con la lectura B, esos enunciados seguirían hacia el modelo, las pruebas y el denominador de cobertura. El glosario apoya la lectura A; la descripción y RF-002 no dicen que el resto se descarte.
- **Propuesta o pregunta para el equipo:** ¿Un enunciado que no especifica una regla de acceso se ignora, se segmenta solo para mostrarlo, o entra en el resto del flujo?
- **Tipo de propuesta:** redacción
- **¿Necesita decisión del equipo?:** sí. La condición de filtro no está cerrada.

### H-003. Segmentación en prosa y edición del requisito

- **Requisito(s) o sección(es):** GMP-RF-002; necesidad y caso de uso de ingesta del contexto
- **Categoría:** ambigüedad
- **Naturaleza:** problema dentro del alcance
- **Evidencia:** La necesidad del analista incluye «documentos estructurados o no estructurados». GMP-RF-002 obliga a «identificar y segmentar automáticamente los requisitos individuales». La descripción añade que «permite su revisión, edición o corrección manual». El caso de uso permite «modificar manualmente el texto o los identificadores». El criterio solo usa «10 requisitos de seguridad numerados» y comprueba que aparecen «10 entidades».
- **Justificación y consecuencia:** Lectura A: solo se separan enunciados ya delimitados, como los numerados del criterio. Lectura B: también se infieren requisitos en prosa. Las dos lecturas producen distintos números de entidades sobre el mismo documento, y el criterio no puede fallar la lectura A. Además, el enunciado obligatorio no incluye editar; la descripción y el caso de uso sí. Un sistema que segmenta y no deja corregir el texto cumple el enunciado y no cumple la descripción.
- **Propuesta o pregunta para el equipo:** ¿Qué unidad cuenta como requisito individual en un texto no delimitado? ¿La corrección del texto forma parte de GMP-RF-002?
- **Tipo de propuesta:** redacción
- **¿Necesita decisión del equipo?:** sí. Hay que fijar la frontera de segmentación y si la edición es obligatoria. El criterio actual solo cubre el caso numerado.

### H-004. Unicidad después de editar un identificador

- **Requisito(s) o sección(es):** GMP-RF-002; caso de uso «Ingestar y segmentar requisitos»
- **Categoría:** información incompleta
- **Naturaleza:** aclaración necesaria
- **Evidencia:** GMP-RF-002 asigna «un identificador único a cada requisito detectado». El caso de uso permite modificar «los identificadores asignados».
- **Justificación y consecuencia:** La unicidad está exigida al asignar el identificador. No se dice si sigue siendo obligatoria después de la edición ni qué hace el sistema si el analista introduce un duplicado. Dos implementaciones pueden aceptar el duplicado o rechazarlo y ambas encajan en los textos actuales.
- **Propuesta o pregunta para el equipo:** Si el analista cambia un identificador, ¿debe seguir siendo único y qué ocurre ante un duplicado?
- **Tipo de propuesta:** redacción o cambio de comportamiento, según la reacción que elija el equipo
- **¿Necesita decisión del equipo?:** sí. La reacción ante el duplicado no está escrita.

### H-005. Quién asigna la etiqueta

- **Requisito(s) o sección(es):** GMP-RF-003; función «Ingesta y Segmentación»; caso de uso de ingesta
- **Categoría:** ambigüedad
- **Naturaleza:** problema dentro del alcance
- **Evidencia:** GMP-RF-003 dice «permitir clasificar y etiquetar». El criterio comprueba que «el sistema sugiere o asigna» las etiquetas. La función de alcance dice «clasificarlos según estándares de referencia». El caso de uso da como resultado requisitos «etiquetados con estándares (OWASP/NIST)».
- **Justificación y consecuencia:** Lectura A: el usuario clasifica y el sistema solo lo permite. Lectura B: el sistema asigna la etiqueta. Lectura C: el sistema sugiere y el usuario confirma. «Sugiere o asigna» hace pasar el criterio con cualquiera de las dos últimas. El resultado visible y la responsabilidad de la etiqueta cambian.
- **Propuesta o pregunta para el equipo:** ¿Quién asigna la etiqueta final y la sugerencia automática es obligatoria?
- **Tipo de propuesta:** redacción; puede implicar cambio de comportamiento si la obligación definitiva no es la que cada lectura supone
- **¿Necesita decisión del equipo?:** sí. Los tres textos exigen actores distintos.

### H-006. Catálogo de OWASP ASVS V4 y NIST

- **Requisito(s) o sección(es):** GMP-RF-003; tabla «Estándares y Artefactos de Referencia» del contexto
- **Categoría:** ambigüedad
- **Naturaleza:** aclaración necesaria
- **Evidencia:** GMP-RF-003 usa «p. ej., OWASP ASVS o NIST» y la descripción cita «control de acceso, autenticación o gestión de sesiones». El criterio acepta etiquetas de «OWASP ASVS V4 (Control de Acceso) o NIST SP 800-53». La tabla fija dos filas: «OWASP ASVS V4», con enfoque «Control de Acceso y Gestión de Sesiones», y «NIST SP 800-53», con enfoque «Controles de Seguridad AC».
- **Justificación y consecuencia:** «ASVS V4» admite, como mínimo, la versión 4 del estándar o el capítulo de control de acceso. El paréntesis del criterio apunta al capítulo; la tabla, al juntar control de acceso y gestión de sesiones bajo el mismo nombre, encaja mejor con la versión. El «o» del criterio se cumple con uno solo de los dos marcos. «P. ej.» y la mención de autenticación dejan abierto un catálogo distinto del de la tabla. Tratar la autenticación como categoría obligatoria del flujo sería una ampliación respecto de esa tabla. Sin revisión de NIST SP 800-53 ni el nivel de la etiqueta (familia o control), dos etiquetas pueden considerarse correctas.
- **Propuesta o pregunta para el equipo:** ¿Qué designa «OWASP ASVS V4», cuál es el catálogo cerrado, si un requisito lleva una etiqueta o varias, qué revisión de NIST se usa y a qué nivel se etiqueta?
- **Tipo de propuesta:** redacción
- **¿Necesita decisión del equipo?:** sí. El catálogo y el nivel de etiqueta no están cerrados. Incluir autenticación como obligación nueva sería ampliación opcional.

### H-007. Selección entre RBAC y ABAC

- **Requisito(s) o sección(es):** GMP-RF-004; tabla de estándares del contexto
- **Categoría:** ambigüedad
- **Naturaleza:** aclaración necesaria
- **Evidencia:** GMP-RF-004 pide generar el modelo «(RBAC/ABAC)» y «sujetos/roles, recursos, acciones, atributos y reglas». La tabla asocia OWASP ASVS V4 con «RBAC» y NIST SP 800-53 con «ABAC».
- **Justificación y consecuencia:** La barra y la columna «Modelos Soportados» admiten tres comportamientos: el estándar elige el tipo; el usuario lo elige; el sistema produce ambos o un híbrido. Tampoco se dice si los atributos son obligatorios en todo modelo o solo en ABAC. Un modelo RBAC sin atributos puede ser incompleto o correcto según la lectura.
- **Propuesta o pregunta para el equipo:** ¿Qué regla selecciona RBAC, ABAC o ambos, y cuándo son obligatorios los atributos?
- **Tipo de propuesta:** redacción
- **¿Necesita decisión del equipo?:** sí. La tabla no dice que la asociación sea una regla de selección, y RF-004 tampoco elige otra.

### H-008. El criterio de generación no cubre la obligación

- **Requisito(s) o sección(es):** GMP-RF-004
- **Categoría:** falta de verificabilidad
- **Naturaleza:** problema dentro del alcance
- **Evidencia:** El requisito enumera «sujetos/roles, recursos, acciones, atributos y reglas». El criterio introduce «3 roles y 2 reglas de restricción» y solo pide «la estructura lógica de sujetos, permisos y condiciones asociadas».
- **Justificación y consecuencia:** El resultado puede superar el criterio sin recursos, acciones ni atributos, y sin que los 3 roles o las 2 reglas de la entrada aparezcan en el modelo. No se puede decidir, con ese criterio, si se cumplió la obligación escrita.
- **Propuesta o pregunta para el equipo:** ¿El resultado de ese escenario debe reflejar los 3 roles, las 2 reglas y el resto de elementos nombrados en el requisito? Conviene alinear el criterio con la decisión de H-007, sin añadir elementos que los documentos no listen.
- **Tipo de propuesta:** redacción
- **¿Necesita decisión del equipo?:** sí, para fijar el resultado esperado del escenario. Los documentos no dicen que esas cantidades deban reaparecer en la salida.

### H-009. Confirmación del modelo antes de generar pruebas

- **Requisito(s) o sección(es):** GMP-RF-005; secuencia de casos de uso del contexto
- **Categoría:** ambigüedad
- **Naturaleza:** aclaración necesaria
- **Evidencia:** GMP-RF-005 exige «visualizar, editar y confirmar el modelo lógico generado antes de proceder a la generación de pruebas». El criterio comprueba que una edición «se persiste y condiciona la generación posterior». No comprueba qué ocurre si el usuario no confirma.
- **Justificación y consecuencia:** Lectura A: la generación de pruebas permanece bloqueada hasta una confirmación explícita. Lectura B: confirmar es una acción disponible, y se puede generar pruebas desde un modelo no confirmado. «Permitir confirmar» y «antes de proceder» admiten las dos. El criterio solo observa la edición.
- **Propuesta o pregunta para el equipo:** ¿La ausencia de confirmación impide generar pruebas?
- **Tipo de propuesta:** redacción; la lectura A supone un cambio de comportamiento respecto de un flujo que hoy podría continuar sin confirmación
- **¿Necesita decisión del equipo?:** sí. Los documentos no dicen si la confirmación es una compuerta.

### H-010. Casos autorizados y denegados por regla o por conjunto

- **Requisito(s) o sección(es):** GMP-RF-006; caso de uso «Generar casos de prueba»
- **Categoría:** ambigüedad
- **Naturaleza:** aclaración necesaria
- **Evidencia:** GMP-RF-006 pide casos «para caminos nominales (acceso permitido) y excepcionales/ataque (acceso denegado o no autorizado)». El criterio pide que «se producen tanto casos de autorización legítima como casos de intento de acceso no autorizado». El caso de uso dice: «deriva pruebas de acceso autorizado y denegado vinculadas a cada regla del modelo lógico».
- **Justificación y consecuencia:** Lectura A: el conjunto contiene al menos un caso de cada tipo. El criterio se satisface así. Lectura B: cada regla del modelo tiene un caso autorizado y otro denegado. Una política con muchas reglas y un solo par de casos cumple A y no cumple B.
- **Propuesta o pregunta para el equipo:** ¿El par autorizado/denegado es obligatorio para cada regla o para el conjunto?
- **Tipo de propuesta:** redacción
- **¿Necesita decisión del equipo?:** sí. El requisito, el criterio y el caso de uso no fijan la misma cantidad.

### H-011. Escalado lateral y vertical

- **Requisito(s) o sección(es):** GMP-RF-006; función «Generación de Casos de Prueba» y definición de caso excepcional en el contexto
- **Categoría:** ambigüedad
- **Naturaleza:** aclaración necesaria
- **Evidencia:** El requisito habla de «acceso denegado o no autorizado». El contexto equipara lo excepcional o de ataque con «acceso denegado». El criterio exige «intento de acceso no autorizado (escalado lateral/vertical)».
- **Justificación y consecuencia:** El paréntesis no dice «por ejemplo». Lectura A: todo caso no autorizado debe representar escalado lateral o vertical. Lectura B: el escalado es un ejemplo, y cualquier denegación basta. Una suite de denegaciones simples cumple el requisito y el contexto, y puede fallar el criterio si se adopta la lectura A.
- **Propuesta o pregunta para el equipo:** ¿El escalado lateral y el vertical son obligatorios o es suficiente una denegación?
- **Tipo de propuesta:** redacción
- **¿Necesita decisión del equipo?:** sí. Solo el criterio introduce el escalado.

### H-012. Datos de entrada del caso de prueba

- **Requisito(s) o sección(es):** GMP-RF-006; introducción de `requisitos-v1.md`; glosario del contexto
- **Categoría:** información incompleta
- **Naturaleza:** problema dentro del alcance
- **Evidencia:** La introducción del documento de requisitos describe las pruebas como «datos, precondiciones y aserciones». El glosario incluye «datos de entrada» en el caso de prueba. GMP-RF-006 lista «precondiciones, rol/sujeto solicitante, recurso objetivo, acción solicitada y el resultado esperado», sin los datos de entrada.
- **Justificación y consecuencia:** El caso puede cumplir RF-006 y no contener los datos de entrada que el propio alcance usa para definirlo. Quien implemente o pruebe no sabe si un caso sin datos de entrada es válido.
- **Propuesta o pregunta para el equipo:** ¿Los datos de entrada forman parte de cada caso generado? Si la respuesta es sí, hay que incorporarlos a la obligación y al criterio, con los elementos que el glosario ya nombra.
- **Tipo de propuesta:** redacción
- **¿Necesita decisión del equipo?:** sí, para confirmar que la definición del glosario es obligatoria en RF-006. No hay una lista de datos distinta de esa definición.

### H-013. Regeneración con temperatura y prompt

- **Requisito(s) o sección(es):** caso de uso «Generar casos de prueba»; no hay un GMP que lo cubra. Relacionado con GMP-RF-006 y GMP-RNF-003
- **Categoría:** posible omisión
- **Naturaleza:** problema dentro del alcance
- **Evidencia:** La situación alternativa del caso de uso dice: «El usuario puede solicitar regenerar pruebas específicas ajustando los parámetros de temperatura/prompt del motor». GMP-RNF-003 obliga a almacenar prompts y parámetros, no a que el usuario los ajuste ni a regenerar casos concretos.
- **Justificación y consecuencia:** La regeneración selectiva y el ajuste de temperatura o prompt están descritos en el alcance y no son comprobables con ningún requisito. Un sistema que solo genera el conjunto una vez cumple RF-006 y no ofrece esa situación alternativa.
- **Propuesta o pregunta para el equipo:** ¿Esa alternativa debe convertirse en obligación? En caso afirmativo, el requisito nuevo debería limitarse a regenerar pruebas específicas y a los parámetros ya nombrados: temperatura y prompt.
- **Tipo de propuesta:** requisito nuevo
- **¿Necesita decisión del equipo?:** sí. Hay que confirmar que la alternativa es una obligación y no solo una escena descriptiva. No están escritos los rangos ni otros parámetros.

### H-014. Revisar o corregir los casos pendientes

- **Requisito(s) o sección(es):** GMP-RF-007; supuesto de supervisión humana
- **Categoría:** ambigüedad
- **Naturaleza:** aclaración necesaria
- **Evidencia:** GMP-RF-007 permite «guardar, revisar o exportar» las pruebas en estado «Pendiente». El supuesto dice que el analista tiene «la capacidad de modificar el modelo lógico o corregir casos de prueba antes de autorizar la ejecución».
- **Justificación y consecuencia:** Lectura A: revisar es consultar. Lectura B: revisar incluye corregir el caso, como dice el supuesto. Con la lectura A, el analista no puede corregir una aserción errónea antes de ejecutar. Con la B, RF-007 no dice qué campos del caso, entre los del glosario, son editables.
- **Propuesta o pregunta para el equipo:** ¿El analista puede corregir casos en estado Pendiente y, si puede, qué campos?
- **Tipo de propuesta:** redacción si la lectura B ya era la intención; cambio de comportamiento si hoy se entiende como solo consulta
- **¿Necesita decisión del equipo?:** sí. El supuesto y el verbo «revisar» no describen la misma capacidad.

### H-015. Formato de exportación de las pruebas

- **Requisito(s) o sección(es):** GMP-RF-007
- **Categoría:** información incompleta
- **Naturaleza:** aclaración necesaria
- **Evidencia:** GMP-RF-007 incluye «exportar las pruebas en estado Pendiente». GMP-RF-015 fija PDF y JSON solo para «el informe de resultados consolidado».
- **Justificación y consecuencia:** La exportación de pruebas es una obligación distinta del informe. Sin formato, un archivo PDF, JSON, CSV u otro puede considerarse cumplimiento. No uso el formato de RF-015 como si ya valiera para las pruebas.
- **Propuesta o pregunta para el equipo:** ¿En qué formato se exportan las pruebas pendientes?
- **Tipo de propuesta:** redacción
- **¿Necesita decisión del equipo?:** sí. El formato no aparece en los documentos.

### H-016. Momento y efecto de editar un requisito

- **Requisito(s) o sección(es):** GMP-RF-002; caso de uso de ingesta. Afecta después a modelo, pruebas, trazabilidad y métricas
- **Categoría:** información incompleta
- **Naturaleza:** aclaración necesaria
- **Evidencia:** La alternativa de ingesta permite modificar «el texto o los identificadores» cuando la extracción detecta enunciados ambiguos. Está situada en ese caso de uso. Ningún requisito dice si el texto sigue siendo editable después de generar el modelo o las pruebas, ni el efecto sobre los artefactos ya creados.
- **Justificación y consecuencia:** Si la edición solo existe durante la ingesta inicial, no hace falta un comportamiento de propagación. Si existe más tarde, un cambio de texto puede dejar modelo, pruebas y trazabilidad desalineados, y no está escrito si se conservan, se marcan o se regeneran.
- **Propuesta o pregunta para el equipo:** ¿Hasta qué momento se puede editar el texto segmentado? Si es después de generar otros artefactos, ¿qué efecto es obligatorio?
- **Tipo de propuesta:** redacción si solo se acota el momento; requisito nuevo si se exige propagar o invalidar artefactos
- **¿Necesita decisión del equipo?:** sí. Los documentos no fijan el momento ni el efecto.

### H-017. Validación sintáctica, semántica y lógica

- **Requisito(s) o sección(es):** GMP-RF-008
- **Categoría:** información incompleta
- **Naturaleza:** problema dentro del alcance
- **Evidencia:** GMP-RF-008 exige validar «la consistencia sintáctica, semántica y lógica» y detecta «contradicciones entre políticas, permisos huérfanos, referencias a roles inexistentes o casos de prueba incoherentes con el modelo». El criterio solo introduce «un permiso no definido en el modelo lógico».
- **Justificación y consecuencia:** Los ejemplos de la descripción son defectos de referencia o de lógica. No hay una condición observable para separar sintaxis, semántica y lógica. Un validador que solo detecte un permiso ausente supera el criterio sin realizar las otras dos comprobaciones. No propongo categorías nuevas de defecto.
- **Propuesta o pregunta para el equipo:** ¿Qué condición concreta corresponde a cada uno de los tres tipos, usando los defectos que RF-008 ya nombra o indicando cuál de esos tipos aún no tiene ejemplo?
- **Tipo de propuesta:** redacción
- **¿Necesita decisión del equipo?:** sí. Falta la condición que distingue los tres tipos.

### H-018. Validación previa y ejecución con fallos críticos

- **Requisito(s) o sección(es):** introducción de `requisitos-v1.md`; GMP-RF-008, GMP-RF-009 y GMP-RF-010; supuesto de validación y caso de uso «Validar artefactos estáticamente»
- **Categoría:** contradicción
- **Naturaleza:** aclaración necesaria
- **Evidencia:** La introducción dice que la validación garantiza «la consistencia interna antes de cualquier interacción con el entorno real o simulado». El supuesto dice: «La fase de validación estática es obligatoria previa a la ejecución dinámica; el sistema puede advertir al usuario si intenta ejecutar pruebas sobre un modelo con fallos críticos no corregidos». El caso de uso «marca las alertas y recomienda corregir». GMP-RF-010 y su criterio lanzan 3 de 10 casos y comprueban que «únicamente procesa y reporta dichos 3 casos», sin condición de validación.
- **Justificación y consecuencia:** Escenario: el modelo tiene un fallo crítico y el usuario ordena ejecutar un subconjunto. Una lectura exige que no haya interacción con la API hasta que la validación se haya ejecutado y la consistencia quede garantizada. Otra permite ejecutar, porque el sistema solo «puede advertir» o «recomienda» corregir, y RF-010 obliga a procesar los casos seleccionados. Esas salidas no pueden darse a la vez.
- **Propuesta o pregunta para el equipo:** Con fallos críticos, ¿se impide la ejecución, se advierte y se permite continuar, o la validación se ejecuta siempre antes y solo bloquea en un nivel de severidad concreto?
- **Tipo de propuesta:** cambio de comportamiento
- **¿Necesita decisión del equipo?:** sí. Los documentos exigen resultados incompatibles y ningún requisito elige uno.

### H-019. Error, Advertencia y cobertura

- **Requisito(s) o sección(es):** GMP-RF-009
- **Categoría:** información incompleta
- **Naturaleza:** aclaración necesaria
- **Evidencia:** GMP-RF-009 pide clasificar las incidencias «por severidad». La descripción habla de «errores de lógica o advertencias de cobertura». El criterio, ante «contradicciones deliberadas», exige alertas «Error» y «Advertencia».
- **Justificación y consecuencia:** No está la condición que separa Error de Advertencia. La descripción asocia la advertencia a la cobertura, pero no dice a partir de qué situación de cobertura aparece. Un conjunto que solo contiene contradicciones no explica, con los textos actuales, por qué debe aparecer también una advertencia. El criterio puede superarse etiquetando las mismas contradicciones con los dos nombres.
- **Propuesta o pregunta para el equipo:** ¿Qué hallazgo ya nombrado es Error, cuál es Advertencia y qué situación de cobertura produce la advertencia?
- **Tipo de propuesta:** redacción
- **¿Necesita decisión del equipo?:** sí. No hay umbral ni regla de clasificación; no propongo un porcentaje.

### H-020. Selección manual, filtros y severidad

- **Requisito(s) o sección(es):** GMP-RF-010
- **Categoría:** ambigüedad
- **Naturaleza:** aclaración necesaria
- **Evidencia:** GMP-RF-010 pide «selección manual o automatizada» y filtrar «por severidad, requisito o tipo de prueba». El caso de uso solo dice que «el analista selecciona las pruebas». El criterio selecciona «3 de 10» manualmente. Los tipos nominal y excepcional salen de GMP-RF-006. Ningún requisito asigna severidad al caso de prueba; Error y Advertencia pertenecen al informe de GMP-RF-009.
- **Justificación y consecuencia:** Lectura A: «automatizada» significa aplicar los filtros, frente a marcar casos uno a uno. Lectura B: el sistema elige solo un subconjunto con una regla que no está escrita. Para la severidad, lectura C: los casos tienen una severidad propia no definida. Lectura D: se filtra por la severidad de la validación asociada. Sin validación previa, D no tiene valores. El criterio no distingue estas lecturas.
- **Propuesta o pregunta para el equipo:** ¿Hay selección autónoma y, si la hay, con qué regla ya prevista en el alcance? ¿Qué dato es la severidad por la que se filtra?
- **Tipo de propuesta:** redacción
- **¿Necesita decisión del equipo?:** sí. La regla automática y el atributo de severidad no están definidos. No hace falta decidir el filtro por requisito ni por tipo nominal/excepcional: esos sí están descritos.

### H-021. Pass, Fail, Error y uso del payload

- **Requisito(s) o sección(es):** GMP-RF-011; glosario, actor «API Objetivo» y caso de uso de ejecución
- **Categoría:** ambigüedad
- **Naturaleza:** aclaración necesaria
- **Evidencia:** GMP-RF-011 «evalúa las respuestas HTTP/código de estado» y asigna «Pass, Fail, Error». El criterio, para una prueba de acceso denegado, captura «403 Forbidden» y asigna «Pass». El actor aporta «códigos de estado y payloads para determinar el veredicto». El caso de uso reserva Error a cuando la API «no responde o devuelve un error no controlado de red».
- **Justificación y consecuencia:** El ejemplo del 403 encaja con que Pass signifique coincidencia con el resultado esperado. Otra lectura es que Pass signifique acceso concedido; entonces un 403 sería Fail. Fail no tiene regla. Un HTTP 500 puede ser Error o una respuesta comparable con lo esperado. El payload determina el veredicto según el actor, y no según RF-011. Una denegación expresada solo en el cuerpo, con un código distinto de 403, cambia de veredicto entre esas lecturas.
- **Propuesta o pregunta para el equipo:** ¿Pass es la coincidencia con el resultado esperado? ¿Qué respuesta concreta es Fail y cuál sigue siendo Error? ¿El payload puede cambiar el veredicto cuando el código ya está disponible?
- **Tipo de propuesta:** redacción
- **¿Necesita decisión del equipo?:** sí. Error de red está descrito; Pass, Fail y el uso del payload no quedan cerrados. No propongo una tabla de códigos.

### H-022. Designación de la API y traducción a HTTP

- **Requisito(s) o sección(es):** GMP-RF-011; interacción con la API en el contexto
- **Categoría:** información incompleta
- **Naturaleza:** aclaración necesaria
- **Evidencia:** GMP-RF-011 obliga a «enviar las peticiones de prueba» contra «una API objetivo o entorno de simulación». El contexto dice que la frontera recibe «peticiones de prueba HTTP/API». El supuesto dice que esa API «expone interfaces HTTP/REST accesibles e inocuas». No hay destino configurable ni regla que una rol, recurso, acción y datos con una petición.
- **Justificación y consecuencia:** La obligación de enviar la petición está dentro del alcance, pero dos implementaciones pueden construir peticiones distintas y las dos cumplen el texto. El criterio del 403 solo es reproducible si la API simulada y la petición ya están acordadas fuera de estos documentos.
- **Propuesta o pregunta para el equipo:** ¿Cómo designa el analista la API y qué correspondencia hay entre el caso de prueba y la petición HTTP? Si la designación del destino es una función propia, sería un requisito nuevo; la correspondencia puede quedar como condición de RF-011.
- **Tipo de propuesta:** redacción o requisito nuevo, según dónde sitúe el equipo la configuración del destino
- **¿Necesita decisión del equipo?:** sí. La correspondencia no está en los documentos y no debe inventarse aquí.

### H-023. API objetivo, simulación o entorno real

- **Requisito(s) o sección(es):** GMP-RF-011; función de ejecución, introducción de los requisitos, supuesto de la API y exclusiones del contexto
- **Categoría:** ambigüedad
- **Naturaleza:** aclaración necesaria
- **Evidencia:** GMP-RF-011 dice «API objetivo o entorno de simulación». La función de alcance dice «API de referencia/simulación». La introducción menciona «el entorno real o simulado». La exclusión deja fuera «la ejecución destructiva o no autorizada de pruebas sobre entornos de producción reales». El supuesto habla de una API de simulación «inocua».
- **Justificación y consecuencia:** Lectura A: el único destino es la API de simulación o referencia. Lectura B: también cabe una API real cuando la prueba no es destructiva ni no autorizada. La exclusión no cierra por sí sola la lectura B, porque solo alcanza ese tipo de ejecución. Elegir una u otra cambia el alcance de RF-011.
- **Propuesta o pregunta para el equipo:** ¿«API objetivo» es solo la simulación o referencia ya descrita?
- **Tipo de propuesta:** redacción
- **¿Necesita decisión del equipo?:** sí. Hay que alinear las cuatro formulaciones. No propongo abrir ni cerrar producción más allá de lo que el equipo confirme.

### H-024. Granularidad y cardinalidad de la trazabilidad

- **Requisito(s) o sección(es):** GMP-RF-012; definición de trazabilidad del contexto
- **Categoría:** ambigüedad
- **Naturaleza:** aclaración necesaria
- **Evidencia:** GMP-RF-012 exige la matriz «Requisito de Seguridad ↔ Elemento del Modelo Lógico ↔ Caso de Prueba». La descripción rastrea «qué regla de control de acceso y requisito originó cada caso». El criterio resalta «el requisito de seguridad de origen y la regla del modelo lógico correspondiente», en singular.
- **Justificación y consecuencia:** «Elemento» puede ser la regla, o también el rol, el recurso, la acción o el atributo. El criterio usa una regla y un requisito. Lectura A: cada caso se enlaza con exactamente un requisito y una regla. Lectura B: un caso puede enlazar con varios. La matriz y lo que se resalta en pantalla cambian.
- **Propuesta o pregunta para el equipo:** ¿El enlace obligatorio llega solo hasta la regla, y un caso tiene un único requisito de origen?
- **Tipo de propuesta:** redacción
- **¿Necesita decisión del equipo?:** sí. La granularidad y la cardinalidad no están fijadas.

### H-025. La comprobación solo recorre un sentido de la matriz

- **Requisito(s) o sección(es):** GMP-RF-012
- **Categoría:** falta de verificabilidad
- **Naturaleza:** problema dentro del alcance
- **Evidencia:** El requisito pide una matriz «bidireccional». El criterio solo selecciona «un caso de prueba» y comprueba el requisito y la regla de origen.
- **Justificación y consecuencia:** Ese recorrido demuestra caso → origen. No demuestra requisito → elementos y casos, ni elemento → requisito y casos. Una pantalla con un solo sentido puede superar el criterio sin que la matriz se recorra en el otro.
- **Propuesta o pregunta para el equipo:** ¿El criterio debe recorrer también los sentidos que salen del requisito y del elemento? La obligación de bidireccionalidad ya está escrita.
- **Tipo de propuesta:** redacción
- **¿Necesita decisión del equipo?:** sí, solo para confirmar que la comprobación de interfaz debe mostrar los dos sentidos. No añade un enlace distinto del ya exigido.

### H-026. Definición de cobertura y de tasa de éxito

- **Requisito(s) o sección(es):** GMP-RF-013
- **Categoría:** ambigüedad
- **Naturaleza:** aclaración necesaria
- **Evidencia:** GMP-RF-013 define \(C = R_{\text{cubiertos}} / R_{\text{totales}} \times 100\), «acompañada del porcentaje de pruebas superadas». El criterio carga 10 requisitos, genera pruebas para 8, ejecuta 5, espera «80% de cobertura» y que la tasa de éxito se calcule «sobre las 5 ejecuciones».
- **Justificación y consecuencia:** El 80% fija, para ese escenario, que cubierto significa requisito con pruebas generadas, no requisito ejecutado o superado. La fórmula, aislada, también admite esas otras lecturas. \(R_{\text{totales}}\) no dice si excluye enunciados ajenos al control de acceso (H-002). La tasa de éxito puede ser los Pass entre las 5 ejecuciones, los Pass entre Pass y Fail dejando Error fuera, u otro cociente. El criterio no da cuántas de las 5 superan, así que esa parte no se puede dar por cumplida o incumplida.
- **Propuesta o pregunta para el equipo:** ¿Se confirman estas lecturas del propio criterio: cubierto igual a «tiene al menos un caso generado» y denominador de éxito igual a las ejecuciones realizadas? ¿Error cuenta en ese denominador? ¿Qué requisitos entran en \(R_{\text{totales}}\)?
- **Tipo de propuesta:** redacción
- **¿Necesita decisión del equipo?:** sí. El criterio cierra un ejemplo de cobertura y deja abierta la tasa de éxito.

### H-027. Cobertura absoluta y baseline

- **Requisito(s) o sección(es):** supuesto de métricas; GMP-RF-013; GMP-RF-014; caso de uso «Evaluar cobertura y comparar con baseline»
- **Categoría:** contradicción
- **Naturaleza:** aclaración necesaria
- **Evidencia:** El supuesto dice: «El cálculo de métricas de cobertura y precisión toma como estándar de comparación (ground truth) los datos importados como baseline manual». El criterio de GMP-RF-013 espera 80% de cobertura sin mencionar baseline. La alternativa del caso de uso dice: «Si no se ha importado un baseline manual, el sistema muestra únicamente las métricas absolutas de cobertura y ejecución». El criterio de GMP-RF-014 «compara la cobertura» con el modelo manual.
- **Justificación y consecuencia:** Escenario: no hay baseline y 8 de 10 requisitos tienen pruebas. RF-013 pide mostrar 80%. El caso de uso pide mostrar cobertura y ejecución absolutas. El supuesto, si «cobertura» es una sola métrica, impide calcularla sin baseline. Esas tres salidas no se sostienen juntas. Pueden dejar de chocar si el equipo declara que la cobertura absoluta de RF-013 no usa baseline, que la comparación de RF-014 solo aparece cuando hay baseline, y que el supuesto se refiere a la precisión u otra cobertura comparada. Eso no está dicho.
- **Propuesta o pregunta para el equipo:** Sin baseline, ¿se muestran la cobertura y el éxito absolutos de RF-013? ¿La frase del supuesto afecta a esa cobertura, solo a la precisión, o a una métrica comparada distinta?
- **Tipo de propuesta:** redacción; el comportamiento visible cambia según la opción
- **¿Necesita decisión del equipo?:** sí. Hay afirmaciones incompatibles y no elijo una.

### H-028. Métricas de la comparación con el baseline

- **Requisito(s) o sección(es):** GMP-RF-014; glosario de baseline; GMP-RNF-004
- **Categoría:** ambigüedad
- **Naturaleza:** problema dentro del alcance
- **Evidencia:** GMP-RF-014 compara «métricas de precisión, número de reglas detectadas y casos de prueba válidos». El criterio importa «un modelo de referencia manual» y compara «la cobertura y número de casos de prueba». El glosario define el baseline como «modelos de autorización y casos de prueba». GMP-RNF-004 mide otra cifra, «precisión en la extracción de reglas» y «tasa de concordancia», con umbral del 85%.
- **Justificación y consecuencia:** Precisión, cobertura, reglas detectadas, casos válidos y número de casos no son la misma obligación. El criterio puede superarse comparando cobertura y recuento, sin precisión ni reglas. «Válido» puede significar que pasa la validación estática, que coincide con el baseline o que obtiene Pass. El criterio no importa los casos manuales que el requisito y el glosario incluyen. No está el formato de importación. No doy por hecho que la precisión de RF-014 sea la concordancia de RNF-004: una es la capacidad de comparar y la otra es un umbral.
- **Propuesta o pregunta para el equipo:** ¿Qué valor se compara, cuándo una regla o un caso cuenta como coincidente o válido, el baseline incluye siempre modelo y casos, y en qué formato se importa? ¿La precisión de RF-014 es la misma concordancia de RNF-004?
- **Tipo de propuesta:** redacción
- **¿Necesita decisión del equipo?:** sí. Faltan las definiciones y el criterio actual comprueba otras métricas.

### H-029. Contenido del informe consolidado

- **Requisito(s) o sección(es):** GMP-RF-015; introducción de `requisitos-v1.md`; caso de uso de evaluación
- **Categoría:** información incompleta
- **Naturaleza:** aclaración necesaria
- **Evidencia:** GMP-RF-015 exporta «el informe de resultados consolidado» en PDF y JSON. El criterio exige en ambos «la matriz de trazabilidad, métricas y detalles de ejecución». La introducción dice que el informe consolidado lleva «métricas de trazabilidad y cobertura frente a referencias manuales». El caso de uso, sin baseline, muestra solo métricas absolutas.
- **Justificación y consecuencia:** «Detalles de ejecución» no tiene contenido mínimo: veredictos, códigos, payloads o identificadores de caso encajan por igual. La introducción incluye la comparación con referencias manuales y el criterio no la nombra. No es una lista cerrada, así que no hay contradicción directa, pero un informe puede cumplir el criterio y omitir la comparación, o incluirla siempre aunque no exista baseline, en contra de la alternativa del caso de uso. Tampoco se dice si el informe de validación de GMP-RF-009 entra en el consolidado.
- **Propuesta o pregunta para el equipo:** ¿Qué apartados son obligatorios y cuáles solo aparecen si hubo ejecución o si hay baseline? ¿El informe estático de RF-009 forma parte de esa exportación?
- **Tipo de propuesta:** redacción
- **¿Necesita decisión del equipo?:** sí. El contenido mínimo no coincide entre la introducción y el criterio.

### H-030. Pass y Fail frente a la interfaz en español

- **Requisito(s) o sección(es):** GMP-RNF-001; GMP-RF-011; glosario, «Veredicto»
- **Categoría:** contradicción
- **Naturaleza:** aclaración necesaria
- **Evidencia:** GMP-RNF-001 exige que «los textos de la interfaz de usuario, mensajes de estado e informes» estén en español. Su criterio pide que «todos los avisos y etiquetas» lo estén. El glosario y GMP-RF-011 fijan el veredicto como «Pass, Fail, Error». El criterio de RF-011 espera el veredicto «Pass».
- **Justificación y consecuencia:** En la pantalla de ejecución, la etiqueta visible del veredicto es a la vez un aviso o etiqueta de RNF-001 y el valor Pass/Fail de RF-011. Si toda etiqueta visible debe estar en español, «Pass» y «Fail» incumplen RNF-001. Si el veredicto debe mostrarse como Pass o Fail, se incumple la lectura estricta de RNF-001. «Error», «Advertencia» y «Pendiente» sí pueden mantenerse en español. El conflicto práctico está en Pass y Fail.
- **Propuesta o pregunta para el equipo:** ¿Esas dos palabras se muestran traducidas, se mantienen como códigos visibles, o el código almacenado puede diferir de la etiqueta en español?
- **Tipo de propuesta:** redacción; cambia el texto visible según la opción
- **¿Necesita decisión del equipo?:** sí. Las dos obligaciones, leídas a la vez sobre la misma etiqueta, no se pueden cumplir.

### H-031. Idioma del texto ingerido y de las claves JSON

- **Requisito(s) o sección(es):** GMP-RNF-001; GMP-RF-015; supuesto de idioma de los documentos
- **Categoría:** ambigüedad
- **Naturaleza:** aclaración necesaria
- **Evidencia:** El supuesto admite documentos «en español o inglés». GMP-RNF-001 cubre «textos de la interfaz», «mensajes de estado e informes». El criterio recorre los flujos y exige que «todos los avisos y etiquetas» estén en español.
- **Justificación y consecuencia:** Lectura A: quedan en español los textos propios de la interfaz y la redacción del informe; el enunciado ingerido se conserva en su idioma. Lectura B: también el contenido extraído, el modelo mostrado y las citas del informe deben estar en español. La lectura B obliga a traducir documentos que el supuesto admite en inglés. Un informe JSON puede además separar las claves del texto visible; RF-015 no dice en qué idioma van las claves.
- **Propuesta o pregunta para el equipo:** ¿El texto de origen en inglés se conserva? ¿Las claves del JSON quedan fuera de RNF-001?
- **Tipo de propuesta:** redacción
- **¿Necesita decisión del equipo?:** sí. Traducir el material de entrada sería un comportamiento que el supuesto no pide.

### H-032. Condiciones del plazo de 15 segundos

- **Requisito(s) o sección(es):** GMP-RNF-002; frontera con el motor de IA en el contexto
- **Categoría:** falta de verificabilidad
- **Naturaleza:** problema dentro del alcance
- **Evidencia:** GMP-RNF-002 fija que la creación de un modelo inicial «hasta 10 requisitos de ciberseguridad» «no deberá superar los 15 segundos». El criterio cronometra desde «el envío de la solicitud de generación hasta el despliegue del modelo» y exige \(\le 15\) s. El contexto sitúa el LLM como sistema externo, disponible «a través de su correspondiente API web».
- **Justificación y consecuencia:** El intervalo incluye la llamada externa, pero no fija el modelo, la red, el arranque ni el tamaño de cada requisito. El mismo sistema puede quedar por debajo o por encima de 15 segundos según esas condiciones. Una sola medición del criterio no permite decidir el cumplimiento de la obligación. No propongo otro umbral.
- **Propuesta o pregunta para el equipo:** ¿En qué condiciones de modelo, red y tamaño se mide el plazo, y ese plazo incluye la latencia del LLM externo?
- **Tipo de propuesta:** redacción
- **¿Necesita decisión del equipo?:** sí. Las condiciones de medida no están en los documentos.

### H-033. Versiones de modelos y reproducibilidad

- **Requisito(s) o sección(es):** GMP-RNF-003
- **Categoría:** ambigüedad
- **Naturaleza:** aclaración necesaria
- **Evidencia:** GMP-RNF-003 almacena «el histórico de prompts, parámetros de la IA, versiones de modelos y casos de prueba» para «auditabilidad y reproducibilidad». El criterio busca «el modelo de IA, la semilla/configuración, el prompt enviado y la fecha de ejecución». En el resto de los documentos, «modelo» es el modelo lógico.
- **Justificación y consecuencia:** «Versiones de modelos» puede ser el historial del modelo lógico editado o la identidad y versión del LLM. El criterio solo comprueba la segunda. Reproducibilidad también admite dos lecturas: recuperar exactamente lo guardado, o repetir la llamada y obtener el mismo artefacto. La semilla apoya la segunda, pero el supuesto de la API externa no dice que exista una semilla. La barra «semilla/configuración» puede exigir una semilla o aceptar la configuración. El requisito nombra casos de prueba y el criterio no los comprueba; el criterio nombra la fecha y el requisito no. Un registro puede cumplir uno y fallar el otro.
- **Propuesta o pregunta para el equipo:** ¿Qué versión es obligatoria y reproducibilidad significa recuperar lo almacenado o regenerar el mismo resultado? De los datos ya nombrados en el requisito o en el criterio —prompt, parámetros, versión, casos, modelo de IA, semilla, configuración y fecha—, ¿cuáles son imprescindibles si el proveedor no devuelve una semilla?
- **Tipo de propuesta:** redacción
- **¿Necesita decisión del equipo?:** sí. Hay que elegir el significado y la lista obligatoria. No añado campos que ninguno de los dos textos nombre.

### H-034. Precisión del 85 %

- **Requisito(s) o sección(es):** GMP-RNF-004; relacionado con GMP-RF-014
- **Categoría:** falta de verificabilidad
- **Naturaleza:** problema dentro del alcance
- **Evidencia:** GMP-RNF-004 exige «una precisión en la extracción de reglas de control de acceso de al menos el 85%» frente a «la referencia manual». El criterio usa «un lote de 20 requisitos» y una «tasa de concordancia de reglas extraídas» que «alcanza o supera el 85%».
- **Justificación y consecuencia:** Precisión y concordancia no fijan qué es la misma regla ni cuál es el denominador: las reglas del baseline, las extraídas o el recuento de coincidencias exactas. Dos recuentos distintos pueden situarse a un lado y al otro del 85%. El lote de 20 no está identificado, y el resultado depende del LLM externo. No se puede decidir el cumplimiento de forma repetible. No propongo la fórmula ni otro porcentaje. La relación con la precisión de RF-014 queda en H-028.
- **Propuesta o pregunta para el equipo:** ¿Qué coincidencia cuenta como regla concordante, cuál es el denominador y sobre qué conjunto identificado se mide el 85%?
- **Tipo de propuesta:** redacción
- **¿Necesita decisión del equipo?:** sí. La definición de la métrica y el conjunto de referencia no están escritos.

### H-035. Interpretación de un requisito ambiguo

- **Requisito(s) o sección(es):** supuesto final del contexto; GMP-RF-004 y GMP-RF-005
- **Categoría:** posible omisión
- **Naturaleza:** problema dentro del alcance
- **Evidencia:** El supuesto afirma: «Si un requisito de ciberseguridad es ambiguo, la IA sugerirá una interpretación dentro del modelo lógico que el usuario deberá revisar o validar». RF-004 obliga a generar el modelo y RF-005 a permitir visualizarlo, editarlo y confirmarlo. Ninguno dice que, ante ambigüedad, la salida sea una interpretación propuesta ni que esa revisión sea obligatoria.
- **Justificación y consecuencia:** Ante un requisito ambiguo, el sistema podría omitir la regla, detenerse o producir una interpretación sin que el comportamiento del supuesto sea comprobable. La confirmación de H-009 no distingue ese caso. No añado un marcado de ambigüedad que el supuesto no pide.
- **Propuesta o pregunta para el equipo:** ¿Esa frase del supuesto debe quedar como obligación comprobable, redactada sobre RF-004 y RF-005 o como requisito propio?
- **Tipo de propuesta:** requisito nuevo, o redacción de RF-004 y RF-005 si el equipo prefiere no crear otro identificador
- **¿Necesita decisión del equipo?:** sí. Hay que decidir si el supuesto pasa a ser una obligación verificable.

### H-036. Tratamiento de la gestión de sesiones

- **Requisito(s) o sección(es):** tabla de estándares del contexto; GMP-RF-003, GMP-RF-004 y GMP-RF-006
- **Categoría:** posible omisión
- **Naturaleza:** aclaración necesaria
- **Evidencia:** La tabla asigna a OWASP ASVS V4 el enfoque «Control de Acceso y Gestión de Sesiones» y el modelo RBAC. La descripción de GMP-RF-003 cita «gestión de sesiones». RF-004 y RF-006 solo desarrollan un modelo y pruebas de autorización. Ningún requisito dice qué ocurre con un enunciado etiquetado como gestión de sesiones.
- **Justificación y consecuencia:** Puede quedar solo como etiqueta, entrar en el mismo modelo RBAC/ABAC si contiene una restricción de acceso, o exigir pruebas de sesión que el alcance no describe. Las tres lecturas producen flujos distintos. No propongo una función de sesión nueva.
- **Propuesta o pregunta para el equipo:** ¿Qué tratamiento es obligatorio para un requisito clasificado como gestión de sesiones?
- **Tipo de propuesta:** redacción si solo se aclara que sigue el flujo ya definido; requisito nuevo si debe tener un tratamiento distinto
- **¿Necesita decisión del equipo?:** sí. La tabla lo incluye en el enfoque y los requisitos no dicen el tratamiento.

### H-037. «Modelo lógico verificado»

- **Requisito(s) o sección(es):** función «Generación de Casos de Prueba» y secuencia de la sección 6 del contexto; GMP-RF-006
- **Categoría:** ambigüedad
- **Naturaleza:** aclaración necesaria
- **Evidencia:** La función dice: «a partir del modelo lógico verificado». La secuencia es «Revisión/Edición humana → Generación de casos de prueba → Validación estática». La validación estática está definida como comprobación entre requisitos, modelo y pruebas.
- **Justificación y consecuencia:** Lectura A: «verificado» significa confirmado por el analista, y las pruebas se generan antes de la validación estática. La secuencia apoya esta lectura. Lectura B: el modelo debe haber superado la validación estática antes de generar pruebas. Esa lectura invierte el orden escrito en la sección 6 y choca con el hecho de que la validación también examina las pruebas. Conviene no dejar el término a la interpretación de quien implemente el orden.
- **Propuesta o pregunta para el equipo:** ¿«Modelo lógico verificado» significa el modelo confirmado por el analista?
- **Tipo de propuesta:** redacción
- **¿Necesita decisión del equipo?:** sí, para sustituir o confirmar el término. La secuencia ya ordena las fases, pero la palabra sigue chocando con «validación».

## 4. Observaciones sobre el conjunto

**Contradicciones.** Hay tres, y las tres necesitan una decisión antes de corregir texto:

- H-018: la validación previa se formula como garantía antes de cualquier interacción, como fase obligatoria, como aviso o recomendación, y a la vez RF-010 ejecuta el subconjunto sin esa condición.
- H-027: la cobertura absoluta de RF-013 y la alternativa sin baseline chocan con el supuesto de que la cobertura usa el baseline como verdad de referencia. RF-014 entra porque su criterio también «compara la cobertura».
- H-030: las etiquetas Pass y Fail chocan con la obligación de interfaz en español si toda etiqueta visible debe estar traducida.

**Redundancia.** No he encontrado dos requisitos que impongan la misma obligación sin una diferencia útil.

He revisado y no trato como redundancia estos pares: GMP-RF-008 detecta incoherencias y GMP-RF-009 las informa con severidad; GMP-RF-013 calcula cobertura y éxito, y GMP-RF-014 compara con un baseline; GMP-RF-014 aporta la comparación y GMP-RNF-004 un umbral del 85%, todavía sin fórmula común (H-028 y H-034); GMP-RF-007 conserva pruebas en Pendiente y GMP-RNF-003 conserva histórico para auditoría. La separación entre generación y ejecución está explicada en la introducción y hecha obligatoria en GMP-RF-007; no es otro requisito repetido.

**Posibles omisiones dentro de lo ya descrito.**

- H-013: regenerar pruebas específicas ajustando temperatura y prompt.
- H-035: ante un requisito ambiguo, la IA propone una interpretación que el usuario revisa.
- H-036: no hay tratamiento para un requisito etiquetado como gestión de sesiones.
- H-012: los datos de entrada forman parte de la definición de caso y no de RF-006.

**Criterios que no cubren la obligación.** Se repite en H-008, H-011, H-017, H-020, H-025 y H-028: el escenario de comprobación pide menos que el enunciado, pide otra métrica o solo recorre un sentido. Además, varios resultados generados dependen de un LLM externo no fijado. H-032 y H-034 hacen que el tiempo y el 85% no sean repetibles; H-008 muestra el mismo límite en el resultado del modelo. No propongo sustituir el LLM ni fijar un modelo concreto.

**Efecto de editar el modelo.** No lo trato como defecto. El supuesto dice que la edición manual actualiza «las precondiciones de generación para los casos de prueba posteriores». Las pruebas ya guardadas pueden seguir existiendo, y GMP-RF-008 ya pide detectar casos incoherentes con el modelo. Invalidarlas o regenerarlas automáticamente sería una ampliación, salvo que el equipo la quiera.

**Exclusiones.** No hay ningún requisito que pida reentrenar el LLM, corregir el código de la API, convertir el modelo en políticas ejecutables de un motor externo ni auditar físicamente la red. La exclusión de pruebas destructivas o no autorizadas sobre producción real sigue abierta solo en el sentido de H-023: RF-011 dice «API objetivo» y otros pasajes dicen simulación, referencia o entorno real.

**Supuestos que no convierto en requisitos.** El idioma español o inglés de los documentos y la disponibilidad del LLM externo están formulados como condiciones de operación. No hay un requisito que las contradiga. No propongo duplicarlas, ni añadir el comportamiento cuando el LLM no responde, ni la autenticación del analista, ni la confidencialidad del histórico de prompts, ni un conector de integración continua distinto de la exportación ya exigida. Esos puntos no están en las necesidades, funciones o casos de uso.

**Términos que no elevo a defecto.** «Requisito de Seguridad» y «Requisito de Ciberseguridad» se usan en el glosario para el mismo elemento de la trazabilidad. «Transparente», en GMP-RF-007, va seguido del resultado observable: no ejecutar, guardar en Pendiente y poder revisar o exportar. «Experiencia fluida» y «fiabilidad técnica» están en descripciones cuyo enunciado sí aporta una condición medible; el problema de esas condiciones está en H-032 y H-034, no en el adjetivo.

**H-037** afecta al orden de todo el flujo: generar pruebas desde un modelo confirmado por la persona, o exigir antes la validación estática. La secuencia de la sección 6 apoya lo primero.

## 5. Preguntas para el equipo

1. **H-001.** ¿Qué PDF es admisible y qué coincidencia entre archivo y pantalla valida la extracción?
2. **H-002.** ¿Qué se hace con un enunciado que no especifica una regla de control de acceso?
3. **H-003.** ¿Qué cuenta como requisito individual en prosa no delimitada, y la edición del texto forma parte de GMP-RF-002?
4. **H-004.** Si el analista cambia un identificador, ¿debe seguir siendo único y qué ocurre si lo duplica?
5. **H-005.** ¿La etiqueta la asigna el sistema, la sugiere para confirmación o la pone solo el usuario?
6. **H-006.** ¿Qué significa «OWASP ASVS V4», cuál es el catálogo cerrado, cuántas etiquetas puede llevar un requisito, qué revisión de NIST SP 800-53 se usa y a qué nivel se etiqueta? ¿La autenticación queda fuera?
7. **H-007.** ¿Qué selecciona RBAC, ABAC o ambos, y los atributos son obligatorios en todo modelo?
8. **H-008.** En el escenario de 3 roles y 2 reglas, ¿qué elementos y cantidades deben aparecer en el modelo generado?
9. **H-009.** ¿Sin confirmación explícita del modelo se puede generar pruebas?
10. **H-010.** ¿Cada regla necesita un caso autorizado y otro denegado, o basta con que el conjunto tenga ambos?
11. **H-011.** ¿El escalado lateral y el vertical son obligatorios?
12. **H-012.** ¿Cada caso debe incluir datos de entrada, como indica el glosario?
13. **H-013.** ¿Regenerar pruebas concretas, ajustando temperatura y prompt, pasa a ser un requisito?
14. **H-014.** ¿El analista puede corregir casos en Pendiente y qué campos?
15. **H-015.** ¿En qué formato se exportan esas pruebas?
16. **H-016.** ¿Hasta qué momento se puede editar un requisito segmentado y qué efecto tiene sobre los artefactos ya generados?
17. **H-017.** ¿Qué condición observable separa la validación sintáctica, la semántica y la lógica?
18. **H-018.** Con fallos críticos, ¿la ejecución se bloquea, se advierte y continúa, o la validación se lanza siempre antes?
19. **H-019.** ¿Qué hallazgo es Error, cuál es Advertencia y cuándo aparece la advertencia de cobertura?
20. **H-020.** ¿Existe selección autónoma y qué dato es la severidad usada como filtro?
21. **H-021.** ¿Pass significa coincidencia con lo esperado? ¿Qué respuesta es Fail, qué respuesta sigue siendo Error y el payload puede cambiar el veredicto?
22. **H-022.** ¿Cómo se designa la API y cómo se traduce el caso de prueba a una petición HTTP?
23. **H-023.** ¿La API objetivo es únicamente la de simulación o referencia?
24. **H-024.** ¿La trazabilidad enlaza el caso solo con una regla y un requisito?
25. **H-025.** ¿La comprobación de la matriz debe mostrar también los sentidos que salen del requisito y del elemento?
26. **H-026.** ¿«Cubierto» significa que el requisito tiene al menos un caso generado? ¿La tasa de éxito usa como denominador todas las ejecuciones, Error incluido? ¿Qué entra en el total de requisitos?
27. **H-027.** Sin baseline, ¿se muestran cobertura y éxito absolutos? ¿A qué métrica aplica el supuesto de verdad de referencia?
28. **H-028.** ¿Qué se compara con el baseline, qué coincidencia cuenta, el baseline incluye modelo y casos, en qué formato se importa, y esa precisión es la misma de GMP-RNF-004?
29. **H-029.** ¿Qué apartados obliga el informe consolidado, cuáles dependen de la ejecución o del baseline, y el informe de validación entra en la exportación?
30. **H-030.** ¿Pass y Fail se traducen, se muestran como códigos o se separan de la etiqueta en español?
31. **H-031.** ¿El texto ingerido en inglés se conserva, y las claves JSON quedan fuera del requisito de idioma?
32. **H-032.** ¿Bajo qué modelo, red y tamaño se miden los 15 segundos, incluida o no la llamada al LLM externo?
33. **H-033.** ¿Qué versión debe guardarse, qué significa reproducibilidad y cuáles de los datos ya nombrados son obligatorios si no hay semilla?
34. **H-034.** ¿Cómo se decide que dos reglas concuerdan, cuál es el denominador y sobre qué conjunto se exige el 85%?
35. **H-035.** ¿La interpretación propuesta ante un requisito ambiguo, con revisión del usuario, debe ser comprobable?
36. **H-036.** ¿Qué hace el sistema con un requisito clasificado como gestión de sesiones?
37. **H-037.** ¿«Modelo lógico verificado» significa confirmado por el analista antes de generar pruebas?

No he redactado una versión nueva de los requisitos. Cada pregunta queda abierta para que el equipo acepte, rechace o concrete el cambio.

**Comprobación final:** la tabla contiene los 15 identificadores funcionales y los 4 no funcionales, una sola vez cada uno. Se han buscado las seis categorías. No hay hallazgo de redundancia. Los 37 hallazgos contienen evidencia, justificación y una propuesta o pregunta. Se distinguen problemas del alcance, aclaraciones necesarias y la ampliación opcional de la autenticación en H-006. Esta evidencia no incorpora las decisiones posteriores ni modifica los documentos fuente.
