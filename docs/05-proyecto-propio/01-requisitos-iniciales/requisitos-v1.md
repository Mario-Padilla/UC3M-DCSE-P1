# Requisitos iniciales del sistema — v1

## 1. Introducción

Este documento define los requisitos iniciales del software para el **Sistema de Generación Automática de Modelos y Pruebas de Ciberseguridad mediante IA Generativa**. El sistema tiene como propósito transformar especificaciones de requisitos de ciberseguridad en lenguaje natural o semiestructurado (alineados con estándares como OWASP ASVS y NIST) en modelos lógicos de autorización y casos de prueba automatizados para verificar políticas de control de acceso.

El alcance del sistema contempla la ingesta y segmentación de requisitos de ciberseguridad, la síntesis interactiva de modelos lógicos de control de acceso (basados en roles o atributos), la generación de casos de prueba nominales y de denegación, la validación estática de coherencia entre artefactos, la ejecución de un subconjunto de pruebas contra un entorno de simulación o API de referencia, y la generación de un informe consolidado con métricas de trazabilidad y cobertura frente a referencias manuales.

El sistema establece una separación conceptual y funcional estricta entre las tres fases principales del ciclo de prueba:
* **Generación:** Análisis asistido por IA generativa para sintetizar modelos lógicos de control de acceso y derivar especificaciones de pruebas (datos, precondiciones y aserciones).
* **Validación:** Comprobación estática (sintáctica, semántica y lógica) entre requisitos, modelo lógico y pruebas, garantizando la consistencia interna antes de cualquier interacción con el entorno real o simulado.
* **Ejecución:** Corrida efectiva de las pruebas seleccionadas sobre la API o sistema de referencia bajo prueba y captura de veredictos (*Pass*, *Fail*, *Error*).

Los requisitos se dividen en funcionales (`GMP-RF`) y no funcionales (`GMP-RNF`). Los módulos agrupan capacidades funcionales del sistema. La columna «Cómo comprobarlo» define el criterio de verificación previsto para auditar el cumplimiento del requisito durante la fase de evaluación.

---

## 2. Requisitos funcionales

### Ingesta y Análisis de Requisitos de Ciberseguridad

| ID | Requisito | Descripción | Módulo | Cómo comprobarlo |
| --- | --- | --- | --- | --- |
| GMP-RF-001 | El sistema deberá permitir la ingesta de documentos de requisitos de ciberseguridad en formato texto plano, Markdown y PDF. | Carga la especificación funcional y de seguridad que servirá de entrada al motor de IA generativa. | Ingesta | Cargar un documento en cada uno de los formatos admitidos (TXT, MD, PDF) y verificar que el contenido se extrae y visualiza correctamente en la interfaz. |
| GMP-RF-002 | El sistema deberá identificar y segmentar automáticamente los requisitos individuales dentro del documento cargado. | Asigna un identificador único a cada requisito detectado y permite su revisión, edición o corrección manual. | Ingesta | Cargar una especificación con 10 requisitos de seguridad numerados y comprobar que el sistema identifica 10 entidades independientes con sus identificadores. |
| GMP-RF-003 | El sistema deberá permitir clasificar y etiquetar los requisitos según estándares de ciberseguridad de referencia (p. ej., OWASP ASVS o NIST). | Asocia categorías de seguridad como control de acceso, autenticación o gestión de sesiones a los requisitos extraídos. | Ingesta | Cargar requisitos de control de acceso y verificar que el sistema sugiere o asigna etiquetas correspondientes a OWASP ASVS V4 (Control de Acceso) o NIST SP 800-53. |

### Generación de Modelos Lógicos de Control de Acceso

| ID | Requisito | Descripción | Módulo | Cómo comprobarlo |
| --- | --- | --- | --- | --- |
| GMP-RF-004 | El sistema deberá generar automáticamente los elementos de un modelo lógico de autorización a partir de los requisitos analizados. | Sintetiza sujetos/roles, recursos, acciones, atributos y reglas de política de control de acceso (RBAC/ABAC) mediante IA generativa. | Generación de Modelos | Introducir requisitos de control de acceso con 3 roles y 2 reglas de restricción. Comprobar que la IA genera la estructura lógica de sujetos, permisos y condiciones asociadas. |
| GMP-RF-005 | El sistema deberá permitir al usuario visualizar, editar y confirmar el modelo lógico generado antes de proceder a la generación de pruebas. | Garantiza la supervisión humana (*human-in-the-loop*) previa a la creación de pruebas de seguridad. | Generación de Modelos | Generar un modelo lógico, modificar un permiso asignado a un rol y añadir una regla de restricción manual. Verificar que los cambios se persisten y condicionan la generación posterior. |

### Generación de Casos de Prueba de Seguridad

| ID | Requisito | Descripción | Módulo | Cómo comprobarlo |
| --- | --- | --- | --- | --- |
| GMP-RF-006 | El sistema deberá generar automáticamente casos de prueba de control de acceso para caminos nominales (acceso permitido) y excepcionales/ataque (acceso denegado o no autorizado). | Cada caso de prueba define precondiciones, rol/sujeto solicitante, recurso objetivo, acción solicitada y el resultado esperado (autorizado/denegado). | Generación de Pruebas | Solicitar la generación de pruebas para una política dada y comprobar que se producen tanto casos de autorización legítima como casos de intento de acceso no autorizado (escalado lateral/vertical). |
| GMP-RF-007 | El sistema deberá separar de forma transparente la fase de generación de pruebas de la fase de ejecución. | Generar pruebas no implica su ejecución automática; el usuario puede guardar, revisar o exportar las pruebas en estado «Pendiente». | Generación de Pruebas | Generar un conjunto de 5 casos de prueba de seguridad. Verificar que quedan guardados en estado «Pendiente» sin que se emita ninguna llamada HTTP o solicitud a la API objetivo. |

### Validación de Artefactos

| ID | Requisito | Descripción | Módulo | Cómo comprobarlo |
| --- | --- | --- | --- | --- |
| GMP-RF-008 | El sistema deberá validar la consistencia sintáctica, semántica y lógica del modelo lógico y de los casos de prueba respecto a los requisitos sin realizar ejecuciones. | Detecta contradicciones entre políticas, permisos huérfanos, referencias a roles inexistentes o casos de prueba incoherentes con el modelo. | Validación | Introducir un caso de prueba que solicita un permiso no definido en el modelo lógico. Comprobar que la función de validación detecta la inconsistencia antes de la ejecución. |
| GMP-RF-009 | El sistema deberá proporcionar un informe de validación estática previo a la ejecución, clasificando las incidencias detectadas por severidad. | Informa al usuario de errores de lógica o advertencias de cobertura antes de lanzar pruebas contra el entorno de destino. | Validación | Ejecutar el validador sobre un modelo con contradicciones deliberadas y verificar que se genera un reporte con alertas clasificadas en *Error* y *Advertencia*. |

### Ejecución de Pruebas

| ID | Requisito | Descripción | Módulo | Cómo comprobarlo |
| --- | --- | --- | --- | --- |
| GMP-RF-010 | El sistema deberá permitir la selección manual o automatizada de un subconjunto de casos de prueba para su ejecución. | El usuario puede filtrar por severidad, requisito o tipo de prueba sin necesidad de ejecutar toda la suite. | Ejecución | Seleccionar 3 de 10 casos de prueba generados y lanzar la orden de ejecución. Verificar que el motor de ejecución únicamente procesa y reporta dichos 3 casos. |
| GMP-RF-011 | El sistema deberá ejecutar el subconjunto de pruebas seleccionado contra una API objetivo o entorno de simulación y registrar las respuestas. | Envía las peticiones de prueba, evalúa las respuestas HTTP/código de estado devuelto y asigna un veredicto (*Pass*, *Fail*, *Error*). | Ejecución | Lanzar la ejecución de una prueba de acceso denegado contra la API simulada; comprobar que se captura la respuesta (p. ej., `403 Forbidden`) y se asigna el veredicto *Pass*. |

### Trazabilidad e Informes

| ID | Requisito | Descripción | Módulo | Cómo comprobarlo |
| --- | --- | --- | --- | --- |
| GMP-RF-012 | El sistema deberá mantener una matriz de trazabilidad bidireccional entre Requisito de Seguridad $\leftrightarrow$ Elemento del Modelo Lógico $\leftrightarrow$ Caso de Prueba. | Permite rastrear qué regla de control de acceso y requisito originó cada caso de prueba. | Trazabilidad | Seleccionar un caso de prueba en la interfaz y verificar que el sistema resalta el requisito de seguridad de origen y la regla del modelo lógico correspondiente. |
| GMP-RF-013 | El sistema deberá calcular y presentar métricas de cobertura de requisitos y tasa de éxito de ejecución. | La tasa de cobertura de requisitos se calcula como $C = \frac{R_{\text{cubiertos}}}{R_{\text{totales}}} \times 100$, acompañada del porcentaje de pruebas superadas. | Informes | Cargar 10 requisitos, generar pruebas para 8 de ellos y ejecutar 5. Verificar que la pantalla de métricas indica un 80% de cobertura de requisitos y calcula la tasa de éxito sobre las 5 ejecuciones. |
| GMP-RF-014 | El sistema deberá permitir la evaluación comparativa entre los artefactos generados por IA y un conjunto de referencia elaborado manualmente (*baseline*). | Compara métricas de precisión, número de reglas detectadas y casos de prueba válidos frente a modelos y pruebas manuales. | Evaluación | Importar un modelo de referencia manual y comparar la cobertura y número de casos de prueba generados automáticamente con los del modelo manual. |
| GMP-RF-015 | El sistema deberá exportar el informe de resultados consolidado en formato PDF y JSON. | Facilita la auditoría de seguridad y la integración con herramientas externas de gestión de pruebas o CI/CD. | Informes | Generar un informe tras la ejecución y exportarlo en PDF y JSON. Comprobar que ambos archivos contienen la matriz de trazabilidad, métricas y detalles de ejecución. |

---

## 3. Requisitos no funcionales

| ID | Requisito | Descripción | Módulo | Cómo comprobarlo |
| --- | --- | --- | --- | --- |
| GMP-RNF-001 | Los textos de la interfaz de usuario, mensajes de estado e informes deberán presentarse en español. | Mantiene un idioma uniforme en el panel de control, validaciones estáticas y reportes finales. | Interfaz | Recorrer los flujos de ingesta, edición de modelos, validación, ejecución y reporte. Comprobar que todos los avisos y etiquetas están en español. |
| GMP-RNF-002 | El tiempo de respuesta de la IA generativa para la creación de un modelo lógico inicial (hasta 10 requisitos de ciberseguridad) no deberá superar los 15 segundos. | Asegura una experiencia fluida e interactiva durante las sesiones de modelado. | Rendimiento | Cargar 10 requisitos de ciberseguridad, cronometrar desde el envío de la solicitud de generación hasta el despliegue del modelo y verificar que el tiempo es $\le 15$ s. |
| GMP-RNF-003 | El sistema deberá almacenar el histórico de prompts, parámetros de la IA, versiones de modelos y casos de prueba para garantizar auditabilidad y reproducibilidad. | Permite auditar exactamente qué configuración y versión de LLM generó cada artefacto de seguridad. | Auditoría y Seguridad | Consultar el registro de auditoría de una ejecución previa y verificar que constan el modelo de IA, la semilla/configuración, el prompt enviado y la fecha de ejecución. |
| GMP-RNF-004 | El sistema deberá lograr una precisión en la extracción de reglas de control de acceso de al menos el 85% en comparación con la referencia manual. | Garantiza la fiabilidad técnica del motor generativo al sintetizar políticas de seguridad. | Calidad de IA | Evaluar un lote de 20 requisitos frente al patrón de referencia manual y comprobar que la tasa de concordancia de reglas extraídas alcanza o supera el 85%. |
