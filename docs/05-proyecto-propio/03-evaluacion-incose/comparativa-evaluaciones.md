# Comparativa de las evaluaciones y valoración crítica — proyecto propio

## 1. Objeto, fuentes y estado

Este documento aplica al proyecto propio los pasos 5 y 6 del apartado 1.5 del [enunciado de P1](../../enunciado/P1.docx.pdf), conforme al flujo solicitado en el apartado 1.7: comparar la evaluación general con la evaluación INCOSE y valorar críticamente el apoyo de la IA.

**Estado:** análisis revisado y confirmado por el equipo junto con las decisiones de la matriz y la v3. El equipo ha confirmado el cierre documental del ejercicio 5, con las limitaciones indicadas.

Fuentes:

- Evaluación general: [prompt](../02-evaluacion-ia/prompt.md), [respuesta original de Grok 4.7](../02-evaluacion-ia/respuesta-grok4.7-extrahigh-fast.md) y [decisiones E5-001 a E5-037](../02-evaluacion-ia/evaluacion-y-decisiones.md).
- Evaluación INCOSE: [reglas seleccionadas](reglas-seleccionadas.md), [prompt](prompt.md), [respuesta original de Grok 4.7](respuesta-spacexai-grok-4.7.md) y [matriz y recomendaciones](matriz-y-decisiones.md).
- Versiones: [v1](../01-requisitos-iniciales/requisitos-v1.md), [v2 confirmada](../02-evaluacion-ia/requisitos-v2.md) y [v3 confirmada](requisitos-v3.md). El [contexto vigente](../01-requisitos-iniciales/contexto-y-alcance.md) se ha alineado después de las evaluaciones y no debe tratarse como copia exacta del contexto leído entonces por la IA.

Los metadatos originales identifican al proveedor como SpaceXAI y al modelo como Grok 4.7 según la sesión en Cursor; no consta identificador de compilación o API más específico. Este análisis conserva esa atribución como dato de la evidencia, sin verificarla de forma independiente. Tampoco consta el commit de las entradas de la evaluación general.

## 2. Comparación de métodos y evolución

| Dimensión | Evaluación general | Evaluación INCOSE |
| --- | --- | --- |
| Entrada | V1: 15 RF y 4 RNF. | V2: 16 RF y 4 RNF, tras las decisiones de la evaluación general. |
| Unidad | Requisito completo, con descripción, módulo y criterio; coherencia con contexto. | Enunciado, con las otras columnas y contexto como apoyo. |
| Criterios | Ambigüedad, información incompleta, verificabilidad, redundancia, contradicción y omisiones. | Singularidad, claridad, gramática, términos vagos, condiciones y verificabilidad, vinculados a reglas y características explícitas. |
| Referencia | Alcance y criterios generales del prompt. | Hoja-resumen INCOSE v4 y selección documentada; no la guía completa. |
| Evidencia | Una respuesta: 37 hallazgos H y cobertura individual de 19 requisitos. | Una respuesta: 18 observaciones INC-OBS y 120 valoraciones requisito–aspecto. |
| Resultado | 37 aplicaciones aceptadas según el registro del equipo; v2 confirmada. | Decisiones individualizadas, ajustes REV-001 a REV-005 y v3 confirmados por el equipo. |

La v1 tiene 19 requisitos, la v2 tiene 20 y la v3 revisada tiene 34 (30 RF y 4 RNF). En la fase general se incorpora RF-016 para regenerar casos. El crecimiento posterior procede principalmente de separar obligaciones y explicitar condiciones; REV-002 a REV-005 también proponen concreciones o ampliaciones de comportamiento y verificación que no deben presentarse como simples cambios de estilo.

Las 120 celdas originales contienen 36 OP, 20 RA, 1 NA y 63 SPD. Las 20 RA corresponden a una misma limitación transversal de R1; no son 20 errores gramaticales. Las celdas no son hallazgos independientes ni una puntuación de calidad.

**No es un experimento controlado.** Cambian la versión evaluada, la unidad de análisis y el prompt. No se puede atribuir cada hallazgo nuevo exclusivamente a INCOSE ni concluir que una evaluación sea más precisa por producir más observaciones. El análisis posterior de OpenAI tampoco es una segunda ejecución del mismo prompt sobre la misma base.

## 3. Comparación de resultados por temas

| Tema | Aportación de la evaluación general | Aportación INCOSE y revisión posterior |
| --- | --- | --- |
| Ingesta y corrección | E5-001 a E5-004 concretan PDF con texto, selección de restricciones de acceso, prosa y rechazo de IDs duplicados. | INC-OBS-002 separa segmentar de corregir y hace explícita la reacción al duplicado. La unicidad es comprobable, pero no acredita por sí sola segmentar correctamente cualquier prosa. |
| Etiquetado y modelos | E5-005 a E5-008 y E5-036 fijan quién propone/confirma, catálogo, asociación OWASP–RBAC y NIST–ABAC y tratamiento de sesiones. | INC-OBS-003 a INC-OBS-005 trasladan catálogo, cardinalidad y ramas al enunciado. REV-001 evita un requisito C que repita el caso conjunto de A/B y conserva la comprobación de doble etiqueta. |
| Supervisión humana | E5-009 y E5-035 exigen confirmación e interpretación propuesta ante ambigüedad. | INC-OBS-006/007 hacen identificables interpretación, visualización, edición y confirmación. REV-002 propone explicitar el contraste con el requisito de origen, no limitarlo a pulsar una confirmación. |
| Generación y regeneración | E5-010 a E5-015 y E5-037 precisan el par autorizado/denegado por regla, campos, RF-016 y separación respecto de ejecución. | INC-OBS-008/009 separan guardar, corregir y exportar, y aclaran que el analista elige qué regenerar. No se fija otro formato ni se ejecutan casos al regenerarlos. |
| Validación y bloqueo | E5-017 a E5-019 concretan errores, advertencias y bloqueo antes de llamar a la API. | INC-OBS-010/011 separan tipos de defecto, informe, clasificación y efecto. REV-002 señala el límite de la consistencia interna; REV-003 propone validar las versiones actuales tras cambios. |
| Selección y ejecución | E5-020 a E5-023 precisan filtros, destino de simulación/referencia y veredictos. | INC-OBS-012/013 hacen explícitos filtros y reglas de Pass/Fail/Error. La revisión distingue seleccionar un caso con Error de tener autorización para ejecutarlo. |
| Trazabilidad | E5-024/025 fijan una regla y un requisito por caso, con navegación en ambos sentidos. | No hay observación específica adicional en INCOSE, salvo R1. Eso no acredita trazabilidad implementada ni fidelidad semántica. |
| Métricas e informes | E5-026 a E5-029 y E5-034 separan métricas absolutas y baseline, definen coincidencia de reglas y contenidos exportados. | INC-OBS-014 a INC-OBS-016 e INC-OBS-018 trasladan fórmulas, contenidos y condiciones. REV-005 trata denominadores cero y hace visibles reglas del baseline omitidas mediante una métrica adicional confirmada por el equipo. |
| Idioma y auditoría | E5-030/031 aclaran excepciones; E5-033 distingue recuperación de artefactos de repetir una salida idéntica del LLM. | INC-OBS-017 explicita excepciones de idioma. RNF-003 no recibe otra observación específica, pero eso no demuestra reproducibilidad estadística del modelo. |
| Rendimiento | H-032 y E5-032 identifican la dependencia externa y mantienen 15 s sin terminar de fijar las condiciones. | La matriz INCOSE califica SPD la verificabilidad de RNF-002. REV-004 cuestiona esa suficiencia y propone un protocolo antes de afirmar cumplimiento general. |

La evaluación general concreta primero qué debe hacer el sistema y dónde se sitúan sus límites. INCOSE ayuda a expresar esas decisiones como obligaciones identificables, especialmente cuando estaban solo en descripciones. Sin embargo, algunas limitaciones sobreviven a ambas fases: una redacción más explícita no basta para demostrar que una restricción es realizable o que su comprobación representa todo el dominio.

## 4. Valoración crítica de la IA

### Capacidades observadas

1. **Cobertura sistemática.** Ambas respuestas recorren todos los requisitos de sus bases. La matriz INCOSE permite localizar cada uno de los seis aspectos, incluso sin hallazgo.
2. **Detección de incoherencias de flujo.** H-018 contrapone consistencia previa, aviso y ejecución; E5-018 fija el bloqueo por Error. H-037 distingue confirmación humana de validación estática y ordena las fases sin exigir ejecutar para validar.
3. **Descomposición argumentada.** Separar mostrar, editar y confirmar (INC-OBS-007), o guardar, corregir y exportar (INC-OBS-008), permite identificar incumplimientos parciales. No depende solo de encontrar la conjunción «y».
4. **Conservación de límites.** Las respuestas señalan ausencias de fuentes y evitan inventar protocolos HTTP, formatos o porcentajes. El reconocimiento de la limitación de R1 impide aparentar una certificación inexistente.

### Limitaciones que requieren criterio del equipo

| Limitación | Evidencia | Consecuencia |
| --- | --- | --- |
| Un problema detectado puede permanecer tras aceptar su aplicación. | H-032 pedía modelo, red y tamaño de entrada; E5-032 mantiene el máximo de 10 requisitos y 15 s. INCOSE, fila V de RNF-002, considera suficientes los extremos del cronómetro. | Medir un ensayo es posible, pero no caracteriza el rendimiento de forma general sin corpus y entorno. REV-004 mantiene la limitación visible. |
| Una propuesta de separación puede repetir obligaciones. | INC-OBS-005 propone A/B/C, siendo C el caso de ambas etiquetas ya aplicable por A y B. | Se recomienda aceptación parcial: mantener ambas ramas y probar su intersección sin otro ID. La recomendación no cambia la respuesta original. |
| Las categorías no siempre sustentan la organización propuesta. | En RF-011 la respuesta marca singularidad SPD y propone A/B para explicitar el veredicto. | La separación puede ser útil, pero no debe justificarse como un incumplimiento de singularidad que esa fuente no detectó. |
| Consistencia interna no equivale a fidelidad. | Los controles de RF-008 pueden aceptar un modelo que otorga permiso al lector cuando el requisito lo reserva al administrador, si las referencias existen y no hay contradicción interna. | REV-002 introduce contraste humano explícito y limita lo que acredita el validador. El equipo ha confirmado esa distribución de responsabilidad. |
| Una métrica correcta puede dar una imagen incompleta. | Una regla correcta generada de 20 manuales da 100 % de precisión con la fórmula de RNF-004. | La precisión no acredita ausencia de omisiones. REV-005 añade reglas manuales representadas (5 % en ese ejemplo), sin umbral nuevo, conforme a la decisión confirmada del equipo. |
| La revisión puede pasar por alto cambios de estado. | V2 permite editar modelo y casos, pero un informe emitido antes de editar no acredita los artefactos posteriores. | REV-003 propone revalidación. No se atribuye a la IA original la detección de este escenario. |

Los ejemplos anteriores son contraejemplos de razonamiento documental y comprobaciones propuestas, no fallos observados en una aplicación ejecutada. La confirmación humana tampoco demuestra por sí sola que un analista no vaya a equivocarse; hace explícita la responsabilidad y permite auditar qué se revisó.

Solo hay una respuesta por fase y no hay referencia externa de defectos, repeticiones ni medición de precisión de las evaluaciones. La aceptación registrada de los 37 asuntos no demuestra ni aceptación automática ni corrección universal. Deben leerse las justificaciones y comprobarse si cada cambio resuelve el problema. Tampoco se ha ejecutado una nueva matriz INCOSE sobre la v3 revisada: las etiquetas disponibles corresponden a v2.

## 5. Balance y cierre confirmado

La IA ha sido útil para localizar ambigüedades y organizar la revisión por reglas explícitas. Su principal ventaja en estas evidencias es convertir dudas y obligaciones implícitas en asuntos revisables con referencias. Sus límites aparecen al evaluar la suficiencia de una comprobación, las omisiones semánticas y el significado real de una métrica. La responsabilidad del equipo consiste en contrastar esas propuestas y decidir la obligación final, no solo conservar el texto que genera la herramienta.

La revisión confirmada mantiene la v1 y la v2, alinea el contexto vigente y justifica individualmente las 18 observaciones y las adaptaciones REV-001 a REV-005 de v3. El equipo ha revisado y confirmado las decisiones, la v3 y este análisis, cerrando el ejercicio 5. Se mantiene la limitación de R1 y quedan por concretar corpus, configuración, entorno y repeticiones del protocolo de rendimiento antes de verificar. No se declara conformidad con toda la guía INCOSE ni se presentan criterios previstos como resultados de pruebas.
