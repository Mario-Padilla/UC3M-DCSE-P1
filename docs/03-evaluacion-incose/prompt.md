# Prompt para la evaluación INCOSE

## Uso y entradas

Prompt preparado para el ejercicio 3 (apartado 1.5 del enunciado). Su preparación no implica que la evaluación se haya ejecutado. Las rutas del bloque siguiente son relativas a la raíz del repositorio; si se utiliza una herramienta sin acceso a los archivos, se deben adjuntar sus contenidos y el PDF de referencia.

La base es [requisitos v2](../02-evaluacion-ia/requisitos-v2.md), versión resultante del ejercicio 2, cerrado por decisión del equipo con las evaluaciones y decisiones actuales. Los resultados de este prompt deberán conservarse como evidencia de IA, separados de las decisiones acordadas con el equipo.

El proceso acordado es obtener primero dos análisis completos e independientes, uno por modelo, y revisar después ambos resultados para registrar las decisiones justificadas del equipo y preparar v3.

## Prompt

```text
Actúa como revisor de escritura de requisitos para el software de una máquina
de café de vending. Trabaja en español.

Antes de evaluar, lee:
- AGENTS.md y README.md.
- docs/enunciado/P1.docx.pdf, especialmente el apartado 1.5.
- docs/03-evaluacion-incose/reglas-seleccionadas.md.
- docs/03-evaluacion-incose/incose_rwg_gtwr_v4_summary_sheet.pdf.
- docs/02-evaluacion-ia/requisitos-v2.md.
- docs/01-requisitos-iniciales/contexto-y-alcance.md.

Si alguna entrada no está disponible o no puedes leerla, indícalo y pide la
entrada necesaria antes de emitir conclusiones que dependan de ella.

OBJETIVO Y BASE
Evalúa individualmente todos los requisitos funcionales y no funcionales de
requisitos-v2.md. Esta versión es la base del ejercicio 3 y procede del
ejercicio 2, cerrado por el equipo. Considera el enunciado de cada requisito como
unidad de evaluación y consulta su descripción, su criterio de comprobación
y el contexto documentado para interpretarlo. No inventes alcance, decisiones,
valores, resultados de pruebas ni comportamientos del sistema.

Identifica al comenzar el proveedor y el modelo que realiza la evaluación,
incluida la versión si se conoce. Si no puedes confirmarlos, dilo expresamente.

FUENTE Y REGLAS EXPLÍCITAS
Utiliza exclusivamente la hoja-resumen oficial INCOSE Guide to Writing
Requirements v4 – Summary Sheet, INCOSE-TP-2010-006-04, junio de 2023, y la
selección documentada en reglas-seleccionadas.md. Distingue características
(C) de reglas (R). No afirmes haber consultado la guía completa.

Limita la evaluación a estos seis aspectos:
1. Singularidad: C5 – Singular; R18 – Single Thought Sentence;
   R19 – Combinators.
2. Claridad: C3 – Unambiguous; R4 – Defined Terms;
   R8 – Escape Clauses; R24 – Pronouns.
3. Estructura gramatical: R1 – Structured Statements;
   R12 – Correct Grammar; como apoyo, R2 – Active Voice y
   R3 – Appropriate Subject-Verb.
4. Términos subjetivos: R7 – Vague Terms.
5. Condiciones de aplicación: R27 – Explicit Conditions;
   R28 – Multiple Conditions; como apoyo, R11 – Separate Clauses.
6. Verificabilidad: C7 – Verifiable; cuando corresponda,
   R33 – Range of Values, R34 – Measurable Performance y
   R35 – Temporal Dependencies.

Las características están en la página 2 del PDF, las reglas en la página 3
y su matriz de correspondencia en la página 4. Justifica cada observación
con las reglas o características concretas que realmente la respalden.

CRITERIOS DE APLICACIÓN
- Evalúa cada requisito frente a los seis aspectos, aunque no detectes problemas.
- Distingue entre «sin problema detectado», «observación propuesta»,
  «requiere aclaración» y «no aplica», justificando brevemente cada valoración.
  Son etiquetas de esta evaluación, no categorías oficiales de INCOSE.
- No confundas singularidad con duplicidad entre requisitos (R30 no forma
  parte de la selección). Separa obligaciones independientes cuando proceda;
  una lista de datos o varias condiciones para una misma acción no implica
  automáticamente varias funcionalidades. R18 admite subcláusulas pertinentes.
- No marques incumplimientos solo por encontrar una conjunción o palabra de
  la lista de R7. Explica qué obligación independiente, vaguedad o ambigüedad
  genera en ese caso concreto. Distingue el contenido de la regla del criterio
  contextual utilizado para aplicarla.
- Revisa si las condiciones y sus relaciones lógicas son explícitas. No añadas
  condiciones de negocio no acordadas. Una referencia temporal solo merece
  observación si deja una dependencia relevante sin definir; no inventes plazos.
- No exijas métricas de rendimiento ni tolerancias numéricas a requisitos
  que no las necesiten. Cuando sean necesarias pero falte su valor, solicita
  aclaración al equipo en lugar de inventarlo.
- Considera la descripción y las referencias explícitas, pero no uses una
  intención inferida o un ejemplo de prueba para ocultar un defecto del texto.
- No declares conformidad con un patrón formal de R1 que no esté documentado
  y acordado. Señala la limitación si no puede comprobarse esa parte.
- No amplíes la evaluación a otras reglas o a nuevas funcionalidades.

ANÁLISIS COMPLETO EN UNA RESPUESTA
Realiza una revisión completa de la base y presenta todas las observaciones en el
orden de los requisitos del documento. Si un requisito tiene varios problemas
independientes, asígnales observaciones separadas. Agrupa en una sola observación
los aspectos que expliquen el mismo problema, evitando duplicarlo.

Identifica proveedor/modelo y confirma las entradas utilizadas al comenzar.
Para cada observación:
- Asigna un identificador estable, por ejemplo INC-OBS-001.
- Indica el ID del requisito y cita el fragmento afectado.
- Identifica el aspecto y los IDs/títulos INCOSE aplicables, con su página.
- Explica brevemente el problema concreto y su efecto en la interpretación
  o comprobación; distingue un defecto sustentado de una duda por aclarar.
- Propón una solución y una redacción alternativa que preserve la intención
  acordada. Si implica separación, muestra los enunciados propuestos con IDs
  provisionales y conserva la relación con el requisito de origen.
- Si falta información para concretar la solución, indica qué debe aclarar
  el equipo y deja la propuesta pendiente de esa aclaración. Continúa con
  el resto del análisis sin esperar una respuesta por cada observación.

MATRIZ COMPLETA Y RESUMEN
Incluye en esta misma respuesta la matriz completa de evaluación de la base v2:
ID de requisito, aspecto, reglas/características aplicables, valoración,
justificación y referencia a las observaciones. Utiliza una fila por requisito
y aspecto para hacer explícita la evaluación de los seis aspectos en todos los
requisitos, incluidos aquellos sin problemas detectados.

Termina con un resumen de los hallazgos y las cuestiones que requieren
aclaración o decisión del equipo. Todas las correcciones y redacciones
alternativas son propuestas de la IA pendientes de revisión.

DECISIONES DEL EQUIPO EN UNA FASE POSTERIOR
Las decisiones se tomarán después de disponer de los análisis completos de
ambos modelos. Realiza esta evaluación de manera independiente, sin consultar
ni utilizar la respuesta del otro modelo. No registres decisiones ni modifiques
matriz-y-decisiones.md, requisitos-v2.md o requisitos-v3.md en esta ejecución.

En la revisión posterior, las decisiones explícitas y su justificación se
registrarán en docs/03-evaluacion-incose/matriz-y-decisiones.md, vinculadas
al requisito, al modelo y a la observación correspondiente. Se distinguirá
el hallazgo original de la IA de la decisión del equipo y de cualquier ajuste
posterior. Una respuesta ambigua requiere aclaración, no implica aceptación.
La aceptación de una corrección no cambia retrospectivamente la valoración
original de v2. Los cambios acordados se incorporarán a requisitos-v3.md al
preparar la versión revisada, manteniendo los requisitos no afectados y las
relaciones de origen.

No declares aprobados o terminados los requisitos ni el ejercicio sin
confirmación del equipo. La comparación con el ejercicio 2 y la valoración
crítica de la IA corresponden a los pasos posteriores del ejercicio 3.

ARCHIVO DE RESPUESTA POR MODELO
Este prompt se utilizará por separado con OpenAI y DeepSeek, con las mismas
entradas y reglas. En cada ejecución, crea únicamente el archivo correspondiente
al proveedor y modelo que realmente está respondiendo, dentro de
docs/03-evaluacion-incose/. Utiliza estos nombres si se confirma esa identidad:
- OpenAI gpt-6.1-sol: respuesta-openai-gpt-6.1-sol.md.
- DeepSeek deepseek-v4.1-flash-free:
  respuesta-deepseek-v4.1-flash-free.md.

Para otro modelo confirmado, utiliza respuesta-<proveedor>-<modelo>.md,
incluyendo la versión si se conoce. Si no puedes confirmar la identidad, dilo
en el contenido y utiliza «no-confirmado» en la parte desconocida del nombre;
no deduzcas el modelo por el nombre de archivo solicitado.

Crea el archivo con la respuesta original completa de esta evaluación:
proveedor/modelo, entradas utilizadas, todas las observaciones, matriz completa
de evaluación de la base v2 y resumen de hallazgos y cuestiones pendientes.
No dividas la entrega en turnos de aprobación de observaciones.

El archivo de respuesta es evidencia de la IA. Registra las decisiones del
equipo por separado en matriz-y-decisiones.md, después del acuerdo explícito.
No mezcles respuestas de distintos modelos, no uses respuesta-ia.md como
destino común y no sobrescribas evidencia existente. Si el archivo ya existe,
pide un nombre diferenciado al equipo antes de guardar una nueva evaluación.

Si no tienes acceso de escritura, devuelve íntegramente el contenido que
debería guardarse e indica su ruta y nombre, sin afirmar que creaste el archivo.
No inventes datos de ejecución. Antes de terminar una edición en el repositorio,
revisa el diff y ejecuta git diff --check.
```
