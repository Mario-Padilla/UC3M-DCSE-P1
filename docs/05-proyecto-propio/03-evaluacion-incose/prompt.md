# Prompt para la evaluación INCOSE del proyecto propio

## Uso y entradas

Prompt del apartado 1.5 aplicado al ejercicio 5 (apartado 1.7). Adapta el [prompt de la cafetera](../../03-evaluacion-incose/prompt.md) a la base ya confirmada del proyecto propio. Las rutas son relativas a la raíz del repositorio.

La base es [requisitos v2](../02-evaluacion-ia/requisitos-v2.md). El equipo aceptó el 28 de octubre de 2026 las aplicaciones E5-001 a E5-037 registradas en [evaluación y decisiones](../02-evaluacion-ia/evaluacion-y-decisiones.md). La respuesta de esta ejecución se conserva como evidencia, separada de las decisiones que el equipo tome después.

En la cafetera se obtuvieron dos análisis independientes. En el proyecto propio, la evaluación general usó un solo modelo. Este prompt puede repetirse con otro modelo, en un archivo nuevo, sin sobrescribir la respuesta ya guardada.

## Prompt

```text
Actúa como revisor de escritura de requisitos del Sistema de Generación
Automática de Modelos y Pruebas de Ciberseguridad mediante IA Generativa.
Trabaja en español.

Antes de evaluar, lee:
- AGENTS.md y README.md.
- docs/enunciado/P1.docx.pdf, apartados 1.5 y 1.7.
- docs/05-proyecto-propio/03-evaluacion-incose/reglas-seleccionadas.md.
- docs/03-evaluacion-incose/incose_rwg_gtwr_v4_summary_sheet.pdf.
- docs/05-proyecto-propio/02-evaluacion-ia/requisitos-v2.md.
- docs/05-proyecto-propio/01-requisitos-iniciales/contexto-y-alcance.md.

Si alguna entrada no está disponible, indícalo antes de concluir sobre ella.

OBJETIVO Y BASE
Evalúa individualmente los 16 requisitos funcionales y los 4 no funcionales
de requisitos-v2.md. El equipo ya aceptó esa versión. La unidad de evaluación
es el enunciado. Consulta la descripción, la comprobación y el contexto para
interpretarlo. No inventes alcance, decisiones, umbrales ni comportamientos.

Identifica al comenzar el proveedor y el modelo, incluida la versión si se
conoce. Si no puedes confirmarlos, dilo expresamente.

FUENTE Y REGLAS EXPLÍCITAS
Utiliza la hoja-resumen INCOSE Guide to Writing Requirements v4 – Summary
Sheet, INCOSE-TP-2010-006-04, junio de 2023, y la selección de
reglas-seleccionadas.md. Distingue características (C) de reglas (R). No
afirmes haber consultado la guía completa.

Limita la evaluación a estos seis aspectos:
1. Singularidad: C5; R18 y R19.
2. Claridad: C3; R4, R8 y R24.
3. Estructura gramatical: R1 y R12; como apoyo, R2 y R3.
4. Términos subjetivos: R7.
5. Condiciones de aplicación: R27 y R28; como apoyo, R11.
6. Verificabilidad: C7; cuando corresponda, R33, R34 y R35.

Justifica cada observación con las reglas o características que la respalden.

CRITERIOS DE APLICACIÓN
- Evalúa cada requisito frente a los seis aspectos, aunque no haya problema.
- Usa «sin problema detectado», «observación propuesta», «requiere
  aclaración» y «no aplica». Son etiquetas de esta evaluación.
- No confundas singularidad con duplicidad entre requisitos. R30 no forma
  parte de la selección. Separa obligaciones independientes. Una lista de
  datos o varias condiciones de una misma acción no implica varias
  funcionalidades.
- No marques un incumplimiento solo por una conjunción o por una palabra de
  la lista de R7. Explica el efecto en ese enunciado.
- No añadas condiciones que el equipo no haya aceptado. Puedes proponer que
  el enunciado recoja una regla que ya esté en la descripción de v2.
- No inventes plazos, formatos, contratos HTTP ni porcentajes.
- La columna de comprobación no corrige un enunciado incompleto.
- No declares conformidad con un patrón formal de R1 que no esté documentado.
- No amplíes la evaluación a otras reglas ni a funciones nuevas.

RESPUESTA
Haz la revisión completa en una respuesta, en el orden de v2. Si un requisito
tiene varios problemas independientes, sepáralos. Agrupa en una observación
los aspectos que expliquen el mismo problema.

Identifica proveedor y modelo, y confirma las entradas. Para cada observación:
identificador INC-OBS, requisito, fragmento, aspecto y referencias con página,
problema, efecto, redacción alternativa con IDs provisionales si hay
separación, y qué debe decidir el equipo.

Incluye la matriz completa: una fila por requisito y aspecto, con valoración,
justificación breve y referencia a las observaciones. Termina con el resumen
de hallazgos y las decisiones pendientes.

Las redacciones son propuestas. No modifiques requisitos-v2.md ni redactes
una v3 en esta ejecución. No marques una propuesta como aceptada.

ARCHIVO
Guarda la respuesta original en
docs/05-proyecto-propio/03-evaluacion-incose/, con el nombre
respuesta-<proveedor>-<modelo>.md del modelo que realmente responde.
No sobrescribas una respuesta existente. El registro de decisiones del equipo
irá después en matriz-y-decisiones.md.
```
