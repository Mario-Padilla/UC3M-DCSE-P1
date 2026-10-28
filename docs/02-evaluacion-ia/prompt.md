# Prompt para la evaluación general de requisitos con IA

## Instrucciones de uso

Para ejecutar este prompt, adjunta los tres documentos indicados. Si la herramienta de IA puede leer el repositorio, pídele que use las rutas incluidas. Escribir una ruta no da acceso al archivo por sí solo.

Conserva el prompt utilizado y la respuesta completa de la IA como evidencias del ejercicio. El equipo revisará las observaciones y decidirá cuáles acepta, rechaza o modifica; la salida de la IA no constituye una versión aprobada de los requisitos.

## Prompt

```text
# Objetivo y rol

Actúa como revisor de calidad de requisitos de software. Evalúa los requisitos iniciales del software de una máquina expendedora de café y proporciona observaciones justificadas que ayuden al equipo a decidir si debe corregirlos.

El equipo es responsable de validar la evaluación y de decidir qué cambios realizar. No apruebes, rechaces ni reescribas definitivamente los requisitos en nombre del equipo.

# Documentos de entrada

Lee estos documentos adjuntos. Si la herramienta tiene acceso al repositorio, puedes leerlos desde las rutas indicadas:

1. `docs/enunciado/P1.docx.pdf`
   Fuente de las instrucciones académicas y del caso de estudio. Para esta tarea, consulta especialmente el apartado 1.4, «Ejercicio 2. Evaluación de la calidad mediante IA generativa».

2. `docs/01-requisitos-iniciales/contexto-y-alcance.md`
   Referencia para entender las necesidades, los límites, las interacciones y los supuestos acordados para el sistema.

3. `docs/01-requisitos-iniciales/requisitos-v1.md`
   Documento principal que debes evaluar. Revisa cada requisito funcional y no funcional, incluido su texto, descripción, módulo y criterio «Cómo comprobarlo».

Confirma al inicio qué documentos has podido leer. Si no puedes acceder a alguno, indícalo y explica qué partes de la evaluación quedan limitadas. No supongas el contenido de archivos que no hayas leído.

# Alcance de esta evaluación

Realiza una evaluación general de calidad, correspondiente al ejercicio 2. Evalúa tanto los requisitos individualmente como la coherencia del conjunto con el contexto y alcance.

No presentes esta tarea como una evaluación de cumplimiento de reglas INCOSE ni inventes una lista de reglas INCOSE. Esa evaluación corresponde al ejercicio 3.

Evalúa la completitud respecto del alcance documentado. Distingue entre:

- Un problema dentro del alcance ya acordado.
- Una cuestión que necesita aclaración del equipo.
- Una posible ampliación opcional del alcance.

Respeta las exclusiones y los supuestos expresos. Si alguno produce una incoherencia con otro documento o requisito, señala la evidencia y pide una decisión; no sustituyas silenciosamente la decisión del equipo.

# Criterios de revisión

Evalúa cada requisito funcional y no funcional buscando:

1. **Ambigüedad:** existen dos o más interpretaciones razonables que podrían producir comportamientos distintos.
2. **Información incompleta:** falta una condición, dato o resultado necesario para interpretar o comprobar una obligación que sí está expresada.
3. **Falta de verificabilidad:** no se puede determinar objetivamente, con la información disponible, si el requisito se cumple.
4. **Redundancia:** dos o más requisitos expresan esencialmente la misma obligación sin una diferencia relevante de condición, alcance o resultado.
5. **Contradicción:** dos o más requisitos o documentos exigen resultados incompatibles bajo las mismas condiciones.
6. **Posible omisión:** una necesidad, función, interacción o escenario descrito dentro del alcance no está cubierto por ningún requisito.

Comprueba también que la descripción y el criterio de verificación correspondan al requisito, que se mantenga la terminología de los documentos y que las propuestas no excedan el alcance acordado.

Para cada categoría, informa de los problemas que puedas fundamentar. Si no detectas ninguno, indícalo; no inventes observaciones para completar una categoría.

# Evidencias y propuestas

Por cada hallazgo:

- Indica el ID del requisito afectado o las secciones/documentos implicados.
- Cita brevemente el texto concreto que sustenta la observación.
- Nombra la categoría del problema.
- Explica por qué es un problema y qué consecuencia práctica tendría.
- Si hay ambigüedad, presenta las interpretaciones alternativas.
- Si hay contradicción, cita las dos afirmaciones incompatibles y describe el escenario en que entran en conflicto.
- Si hay una posible omisión, señala la necesidad o escenario del alcance que sirve de evidencia.
- Propón una corrección o formula una pregunta concreta al equipo.
- Indica si la propuesta es una corrección de redacción, un cambio de comportamiento o la incorporación de un requisito nuevo.
- Si se necesita una decisión o información que no aparece en los documentos, déjala como pregunta; no inventes su respuesta.

No conviertas una preferencia de estilo en un defecto si no afecta a la interpretación, la comprobación, la coherencia o el alcance. No propongas valores numéricos, funciones ni decisiones que no estén sustentados por los documentos.

# Formato de la respuesta

Responde en español, con lenguaje claro y conciso. Organiza el resultado en estas secciones:

## 1. Documentos y limitaciones

Indica qué documentos leíste y cualquier limitación que afecte a la evaluación.

## 2. Cobertura de la revisión individual

Presenta una tabla con una fila para cada requisito de `requisitos-v1.md`. Incluye:

| ID | Resultado | Categorías con hallazgos | Referencias a hallazgos |
| --- | --- | --- | --- |

Utiliza uno de estos resultados:

- **Con observaciones:** has identificado uno o más problemas fundamentados.
- **Sin problemas detectados:** no has encontrado un problema fundamentado con la información disponible; no significa que el requisito esté aprobado.
- **No evaluable:** no hay información suficiente para valorar algún aspecto; explica cuál.

Incluye todos los IDs de requisitos funcionales y no funcionales que aparezcan en el documento. Comprueba que la tabla no omite ninguno.

## 3. Hallazgos detallados

Asigna identificadores consecutivos (H-001, H-002, etc.). Para cada hallazgo usa:

- **Requisito(s) o sección(es):**
- **Categoría:** ambigüedad, información incompleta, falta de verificabilidad, redundancia, contradicción o posible omisión.
- **Naturaleza:** problema dentro del alcance, aclaración necesaria o ampliación opcional.
- **Evidencia:** citas breves con el ID y/o la sección de origen.
- **Justificación y consecuencia:**
- **Propuesta o pregunta para el equipo:**
- **Tipo de propuesta:** redacción, cambio de comportamiento o requisito nuevo.
- **¿Necesita decisión del equipo?:** sí/no, con motivo.

## 4. Observaciones sobre el conjunto

Resume contradicciones, redundancias o posibles omisiones que afecten al conjunto. Referencia los hallazgos detallados para no duplicarlos.

## 5. Preguntas para el equipo

Enumera únicamente las preguntas necesarias para resolver observaciones o valorar ampliaciones opcionales. No respondas por el equipo.

# Comprobación final

Antes de terminar, verifica que:

- Has evaluado individualmente cada requisito funcional y no funcional.
- Has buscado las seis categorías indicadas.
- Cada hallazgo contiene evidencia y justificación, o identifica claramente la información que falta.
- Has distinguido problemas del alcance actual de preguntas y ampliaciones opcionales.
- No has presentado tus propuestas como decisiones acordadas ni has creado una versión revisada de los requisitos.
```
