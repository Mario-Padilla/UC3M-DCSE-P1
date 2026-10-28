# Reglas INCOSE seleccionadas para la evaluación

## Fuente

International Council on Systems Engineering (INCOSE), Requirements Working Group, *INCOSE Guide to Writing Requirements v4 – Summary Sheet*, INCOSE-TP-2010-006-04, junio de 2023. Hoja-resumen oficial de siete páginas, disponible gratuitamente: [PDF oficial](https://www.incose.org/wp-content/uploads/legacy/working-groups/requirements-wg/guidetowritingrequirements/incose_rwg_gtwr_v4_summary_sheet.pdf) y [copia aportada al repositorio](incose_rwg_gtwr_v4_summary_sheet.pdf).

La hoja-resumen distingue las características de los requisitos individuales (p. 2) de las reglas de redacción (p. 3), y ofrece una matriz de correspondencia entre ambas (p. 4). La tabla identifica los números y títulos de las reglas seleccionadas y resume su aplicación en español. Los resúmenes no sustituyen el texto inglés de la fuente.

## Criterios seleccionados

| Aspecto acordado | Regla/característica INCOSE seleccionada (título original y referencia) | Criterio de revisión aplicado |
| --- | --- | --- |
| **Singularidad** | **C5 – Singular** (p. 2); **R18 – Single Thought Sentence** y **R19 – Combinators** (p. 3). | El enunciado debe expresar una sola capacidad, característica, restricción o factor de calidad. Revisar si contiene más de una idea o si conectores unen obligaciones independientes. Las subcláusulas que condicionan o califican una misma acción no implican por sí solas varios requisitos: R18 contempla una idea condicionada/calificada por subcláusulas pertinentes. Proponer separar solo obligaciones independientes. |
| **Claridad** | **C3 – Unambiguous** (p. 2); **R4 – Defined Terms**, **R8 – Escape Clauses** y **R24 – Pronouns** (p. 3). | El propósito debe poder interpretarse de una sola manera por los destinatarios. Revisar términos no definidos en glosario/diccionario asociado, cláusulas de escape con condiciones o posibilidades vagas y pronombres personales o indefinidos que oscurezcan la referencia. Interpretar con la descripción y contexto disponibles, sin dar por resuelta una ambigüedad solo porque el evaluador pueda inferir una intención. |
| **Estructura gramatical** | **R1 – Structured Statements** y **R12 – Correct Grammar** (p. 3). | El texto debe conformarse a un patrón acordado y formar una frase gramatical completa. Revisar que se identifiquen la entidad responsable como sujeto y su acción, en consonancia también con **R2 – Active Voice** y **R3 – Appropriate Subject-Verb**. Como no se ha documentado un patrón formal del proyecto en este archivo, no se tratará una plantilla no acordada como requisito adicional. |
| **Términos subjetivos** | **R7 – Vague Terms** (p. 3), relacionada en la matriz de la p. 4 con la característica **C3 – Unambiguous**. | Buscar cuantificadores vagos y adjetivos vagos. La regla enumera, entre otros, «some», «any», «many», «about», «sufficient», «adequate», «appropriate», «efficient», «effective» y «reasonable». En español se comprobarán equivalentes según el contexto. La presencia de una palabra solo genera observación si deja sin criterio claro el alcance o la evaluación; podrá estar definida en el requisito o en una referencia aplicable. |
| **Condiciones de aplicación** | **R27 – Explicit Conditions** y **R28 – Multiple Conditions** (p. 3). | Explicitar a qué condiciones aplica el requisito, en lugar de dejar su aplicabilidad a inferencia contextual; cuando haya varias condiciones para una acción, hacer explícita su relación lógica. R11 – Separate Clauses también indica separar cláusulas por condición o calificación. No añadir condiciones de negocio que el equipo no haya acordado. |
| **Verificabilidad** | **C7 – Verifiable** (p. 2); para cuantificación, **R33 – Range of Values**, **R34 – Measurable Performance** y **R35 – Temporal Dependencies** (p. 3). | El enunciado debe estar estructurado y redactado de modo que su realización pueda verificarse. Cuando aplique, comprobar que cantidades tengan rangos apropiados, que el desempeño tenga objetivos medibles y que las dependencias temporales estén definidas explícitamente. La columna «Cómo comprobarlo» aporta contexto, pero no corrige por sí sola un enunciado cuyo cumplimiento no pueda determinarse. |

### Distinciones para no ampliar el alcance

- **R30 – Unique Expression** (p. 3) trata que cada requisito se exprese una sola vez en el conjunto; no equivale a la singularidad interna de un enunciado (C5, R18 y R19). No se evaluará duplicidad entre requisitos como parte del aspecto acordado de singularidad, salvo que el equipo amplíe el alcance.
- «Términos subjetivos» es el nombre del aspecto acordado para esta evaluación; en la hoja-resumen la regla pertinente se titula **R7 – Vague Terms**. Se aplicará el contenido de R7, no una lista externa de subjetividad.
- La matriz de la p. 4 relaciona las reglas con las características de calidad; estas relaciones orientan la evaluación, pero no significan que se estén seleccionando todas las reglas de INCOSE.

## Alcance y registro

- La unidad de evaluación será cada enunciado de requisito de `../02-evaluacion-ia/requisitos-v2.md`; se consultarán sus descripciones, criterios de comprobación y el contexto cuando ayuden a interpretar el texto.
- Se informarán observaciones concretas con el identificador del requisito, el aspecto aplicable, la justificación y una posible redacción alternativa.
- Una observación o redacción alternativa es una propuesta hasta que el equipo la acepte. La decisión y su justificación se registrarán después en `matriz-y-decisiones.md`.
- Los seis aspectos se han fijado a partir del alcance del enunciado y del acuerdo del equipo. La versión base de la evaluación es `requisitos-v2.md`, resultante del ejercicio 2, cerrado por decisión del equipo con las evaluaciones y decisiones actuales.

## Referencias del trabajo

- Enunciado de la práctica, apartado 1.5: `../enunciado/P1.docx.pdf`.
- Base acordada para evaluar: `../02-evaluacion-ia/requisitos-v2.md`.

La hoja-resumen incluye este aviso de derechos: «Copyright (c) 2023 by INCOSE». INCOSE permite reproducir y usar el resumen con atribución, siempre que se incluya el aviso de copyright en las reproducciones y obras derivadas.
