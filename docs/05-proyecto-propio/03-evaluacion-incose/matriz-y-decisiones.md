# Matriz de cumplimiento INCOSE — proyecto propio

## 1. Base, fuente y estado

**Estado: propuestas registradas, pendientes de confirmación del equipo. No hay requisitos v3.**

La base es [requisitos v2](../02-evaluacion-ia/requisitos-v2.md), confirmada por el equipo el 28 de octubre de 2026. La evidencia de esta evaluación es una sola respuesta: [SpaceXAI Grok 4.7](respuesta-spacexai-grok-4.7.md). En la cafetera hubo dos modelos; aquí no hay una segunda evaluación con la que comparar.

| Clave | Evaluación | Contenido |
| --- | --- | --- |
| GK | [Grok 4.7](respuesta-spacexai-grok-4.7.md) | §3: 18 observaciones. §4: 120 valoraciones, una por requisito y aspecto. |

Las reglas son las de [reglas seleccionadas](reglas-seleccionadas.md), las mismas seis del ejercicio 3. Las valoraciones **OP**, **RA**, **SPD** y **NA** son etiquetas de esa respuesta, no categorías oficiales de INCOSE ni decisiones del equipo.

La matriz completa está en la respuesta, §4. Esta página recoge el cumplimiento por requisito y deja cada observación a la espera de que el equipo la acepte, la rechace o la modifique. Aceptar el problema no obliga a aceptar la redacción literal ni los identificadores provisionales.

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

## 3. Observaciones pendientes de decisión

El hallazgo y la redacción íntegros están en la respuesta. Esta tabla no los sustituye.

| Registro | Requisito | Valoración | Hallazgo | Propuesta | Decisión del equipo |
| --- | --- | --- | --- | --- | --- |
| INC-OBS-001 | Los 20 requisitos | RA | No hay un patrón formal documentado para comprobar R1. | Aportar el patrón existente o acordar uno. Mantener mientras tanto los enunciados en este punto. | Pendiente de confirmación del equipo |
| INC-OBS-002 | GMP-RF-002 | OP | Segmentar y corregir pueden cumplirse por separado. El rechazo del identificador duplicado está solo en la descripción. | Separar en GMP-RF-002-A y GMP-RF-002-B. | Pendiente de confirmación del equipo |
| INC-OBS-003 | GMP-RF-003 | OP | Proponer etiquetas y no generar el modelo hasta confirmarlas son dos obligaciones. | Separar en GMP-RF-003-A y GMP-RF-003-B. | Pendiente de confirmación del equipo |
| INC-OBS-004 | GMP-RF-003 | OP | «Una etiqueta» no fija el catálogo ni si puede haber varias. | Incluir en GMP-RF-003-A el catálogo, la cardinalidad y la exclusión de autenticación ya aceptados. | Pendiente de confirmación del equipo |
| INC-OBS-005 | GMP-RF-004 | OP | RBAC para OWASP y ABAC para NIST son resultados distintos. Faltan en el enunciado los elementos de cada modelo y el caso de las dos etiquetas. | Separar en GMP-RF-004-A, GMP-RF-004-B y GMP-RF-004-C. | Pendiente de confirmación del equipo |
| INC-OBS-006 | GMP-RF-004 | OP | La interpretación de un requisito ambiguo, ya aceptada, está solo en la descripción. | Añadir GMP-RF-004-D con esa regla, sin definir «ambiguo» de otra manera. | Pendiente de confirmación del equipo |
| INC-OBS-007 | GMP-RF-005 | OP | Mostrar, editar y exigir confirmación son tres obligaciones. El efecto sobre los casos Pendiente no está en el enunciado. | Separar en GMP-RF-005-A, GMP-RF-005-B y GMP-RF-005-C. | Pendiente de confirmación del equipo |
| INC-OBS-008 | GMP-RF-007 | OP | Guardar sin ejecutar, corregir y exportar tienen resultados distintos. | Separar en GMP-RF-007-A, GMP-RF-007-B y GMP-RF-007-C. El formato sigue sin fijarse. | Pendiente de confirmación del equipo |
| INC-OBS-009 | GMP-RF-016 | OP | «Casos concretos» no dice que los elige el analista. | Nombrar en el enunciado los casos en Pendiente que indique el analista. | Pendiente de confirmación del equipo |
| INC-OBS-010 | GMP-RF-008 | OP | La consistencia sintáctica, la semántica y la lógica se comprueban por separado y su criterio está solo en la descripción. | Separar en GMP-RF-008-A, GMP-RF-008-B y GMP-RF-008-C. | Pendiente de confirmación del equipo |
| INC-OBS-011 | GMP-RF-009 | OP | Emitir el informe, clasificar y condicionar la ejecución son obligaciones distintas. El sentido de Error y Advertencia está solo en la descripción. | Separar en GMP-RF-009-A, GMP-RF-009-B y GMP-RF-009-C. | Pendiente de confirmación del equipo |
| INC-OBS-012 | GMP-RF-010 | OP | «Filtros» no nombra los tres filtros ya aceptados ni la condición del filtro de severidad. | Trasladar esos filtros al enunciado, sin añadir otro selector. | Pendiente de confirmación del equipo |
| INC-OBS-013 | GMP-RF-011 | OP | Pass, Fail y Error se nombran sin la regla de asignación ya aceptada. | Separar la ejecución, GMP-RF-011-A, de la regla de veredicto, GMP-RF-011-B. Se mantiene el 403 como único código fijado. | Pendiente de confirmación del equipo |
| INC-OBS-014 | GMP-RF-013 | OP | Cobertura y tasa de éxito tienen fórmulas distintas y ninguna está en el enunciado. | Separar en GMP-RF-013-A y GMP-RF-013-B, con los cálculos ya escritos en v2. | Pendiente de confirmación del equipo |
| INC-OBS-015 | GMP-RF-014 | OP | «Casos válidos» no tiene criterio en el enunciado. | Sustituirlo por casos sin Error de validación estática. | Pendiente de confirmación del equipo |
| INC-OBS-016 | GMP-RF-015 | OP | «Informe consolidado» no dice qué contiene ni cuándo entran las comparaciones del baseline. | Trasladar al enunciado el contenido ya aceptado en la descripción. | Pendiente de confirmación del equipo |
| INC-OBS-017 | GMP-RNF-001 | OP | El enunciado obliga a redactar en español sin las excepciones ya aceptadas para veredictos, texto ingerido y claves JSON. | Incorporar esas excepciones al enunciado. | Pendiente de confirmación del equipo |
| INC-OBS-018 | GMP-RNF-004 | OP | El 85 % no tiene en el enunciado la coincidencia ni el denominador. «Extraídas» y «generadas» pueden no ser el mismo conjunto. | Pasar al enunciado la fórmula de la descripción y decir «generadas». | Pendiente de confirmación del equipo |

## 4. Qué no hace esta matriz

No reescribe v2 ni crea v3. No evalúa si dos requisitos repiten la misma obligación. No compara esta respuesta con otro modelo. El análisis crítico de la IA corresponde a un paso posterior, cuando el equipo haya decidido estas filas.
