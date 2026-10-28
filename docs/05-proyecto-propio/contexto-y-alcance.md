# Requisitos iniciales del sistema — v1

## 1. Introducción

Este documento define los requisitos iniciales del software para el **Sistema de Generación Automática de Modelos y Pruebas desde Requisitos basados en IA Generativa**. El sistema se concibe como una herramienta interactiva capaz de procesar especificaciones de requisitos en lenguaje natural o semiestructurado, extraer su semántica mediante modelos de IA generativa, sintetizar elementos de un modelo lógico y derivar casos de prueba vinculados de forma trazable a los requisitos de origen.

El alcance inicial contempla la ingesta de especificaciones de requisitos, la generación interactiva del modelo lógico, la generación de casos de prueba sintéticos o ejecutables, la ejecución de un subconjunto de dichas pruebas contra un entorno de simulación o API objetivo, y la emisión de un informe consolidado con métricas de trazabilidad y cobertura.

El sistema establece una separación conceptual y funcional estricta entre las fases de **Generación**, **Validación** y **Ejecución** de pruebas:
* **Generación:** Creación asistida por IA de modelos lógicos y conjuntos de datos/pasos de prueba.
* **Validación:** Comprobación sintáctica, semántica y de consistencia lógica entre requisito, modelo y prueba, previa a cualquier ejecución.
* **Ejecución:** Corrida efectiva de los casos de prueba seleccionados sobre el sistema bajo prueba y captura de veredictos.

Los requisitos se dividen en funcionales (`GMP-RF`) y no funcionales (`GMP-RNF`). La columna «Cómo comprobarlo» recoge el criterio de verificación previsto para auditar el cumplimiento del requisito.

---

## 2. Requisitos funcionales

### Ingesta y Análisis de Requisitos

| ID | Requisito | Descripción | Módulo | Cómo comprobarlo |
| --- | --- | --- | --- | --- |
| GMP-RF-001 | El sistema deberá permitir la ingesta de documentos de requisitos en formato texto plano, Markdown y PDF. | Permite al usuario cargar la especificación funcional que servirá de entrada al motor de IA generativa. | Ingesta | Cargar un documento en cada uno de los formatos admitidos (TXT, MD, PDF) y verificar que el contenido textual se extrae y visualiza correctamente en la interfaz. |
| GMP-RF-002 | El sistema deberá identificar y segmentar automáticamente los requisitos individuales dentro del documento cargado. | Asigna un identificador único a cada requisito detectado y permite su revisión o corrección manual. | Ingesta | Cargar un documento con 10 requisitos numerados y comprobar que el sistema identifica 10 entidades de requisitos independientes con sus respectivos identificadores. |

### Generación de Modelos Lógicos

| ID | Requisito | Descripción | Módulo | Cómo comprobarlo |
| --- | --- | --- | --- | --- |
| GMP-RF-003 | El sistema deberá generar automáticamente los elementos de un modelo lógico a partir de los requisitos analizados. | Entidades, relaciones, estados, entradas/salidas y reglas de negocio derivadas explícitamente mediante IA generativa. | Generación de Modelos | Introducir un requisito con 3 entidades y 2 reglas de transición. Comprobar que la IA genera la estructura correspondiente de entidades, campos y estados en el modelo lógico. |
| GMP-RF-004 | El sistema deberá permitir al usuario visualizar, editar y confirmar el modelo lógico generado antes de proceder a la generación de pruebas. | Garantiza la supervisión humana (*human-in-the-loop*) previa a las etapas siguientes. | Generación de Modelos | Generar un modelo lógico, modificar el nombre de una entidad y añadir una restricción manual. Verificar que los cambios se guardan y son considerados en los pasos posteriores. |

### Generación de Casos de Prueba

| ID | Requisito | Descripción | Módulo | Cómo comprobarlo |
| --- | --- | --- | --- | --- |
| GMP-RF-005 | El sistema deberá generar automáticamente casos de prueba a partir del modelo lógico y de los requisitos de origen. | Cada caso de prueba incluye precondiciones, pasos de ejecución, datos de entrada y resultados esperados (aserciones). | Generación de Pruebas | Solicitar la generación de pruebas para un requisito dado y comprobar que se producen casos para caminos nominales (éxito) y excepcionales (fallo). |
| GMP-RF-006 | El sistema deberá separar de forma transparente la fase de generación de pruebas de la fase de ejecución. | Generar pruebas no implica su ejecución automática; el usuario puede almacenar, revisar o exportar las pruebas sin ejecutarlas. | Generación de Pruebas | Generar un conjunto de 5 casos de prueba. Verificar que las pruebas quedan guardadas en estado «Pendiente» sin que se haya emitido ninguna llamada o ejecución sobre el sistema objetivo. |

### Validación de Artefactos

| ID | Requisito | Descripción | Módulo | Cómo comprobarlo |
| --- | --- | --- | --- | --- |
| GMP-RF-007 | El sistema deberá validar la consistencia sintáctica y semántica del modelo lógico y de las pruebas respecto a los requisitos sin realizar ejecuciones. | Detecta lagunas, inconsistencias de tipo, referencias huérfanas o contradicciones lógicas entre artefactos. | Validación | Introducir un caso de prueba que hace referencia a un campo inexistente en el modelo lógico. Comprobar que la función de validación detecta el error antes de permitir la ejecución. |
| GMP-RF-008 | El sistema deberá proporcionar un informe de validación estática previo a la ejecución indicando el grado de coherencia del modelo. | Permite corregir discrepancias en la etapa de diseño sintético. | Validación | Ejecutar el validador sobre un conjunto con discrepancias conocidas y comprobar que se genera un reporte con alertas clasificadas por severidad (Error, Advertencia). |

### Ejecución de Pruebas

| ID | Requisito | Descripción | Módulo | Cómo comprobarlo |
| --- | --- | --- | --- | --- |
| GMP-RF-009 | El sistema deberá permitir la selección manual o automatizada de un subconjunto de casos de prueba para su ejecución. | El usuario no está obligado a ejecutar la suite completa en cada corrida. | Ejecución | Seleccionar 3 de 10 casos de prueba generados y lanzar la orden de ejecución. Verificar que solo se procesan y reportan los 3 casos seleccionados. |
| GMP-RF-010 | El sistema deberá ejecutar el subconjunto de pruebas seleccionado contra un entorno de simulación o API objetivo y capturar los resultados. | Registra las respuestas reales, tiempos de ejecución y determina el veredicto (*Pass*, *Fail*, *Error*). | Ejecución | Lanzar la ejecución de una prueba sobre un endpoint simulado y comprobar que se registra la respuesta real del servidor y se asigna el veredicto adecuado según la aserción. |

### Trazabilidad e Informes

| ID | Requisito | Descripción | Módulo | Cómo comprobarlo |
| --- | --- | --- | --- | --- |
| GMP-RF-011 | El sistema deberá mantener una matriz de trazabilidad bidireccional que vincule Requisito $\leftrightarrow$ Elemento de Modelo $\leftrightarrow$ Caso de Prueba. | Cada caso de prueba debe rastrearse inequívocamente hasta el requisito que valida. | Trazabilidad | Seleccionar un caso de prueba en la interfaz y verificar que se highlighting / muestra el requisito original y el elemento del modelo lógico del que fue derivado. |
| GMP-RF-012 | El sistema deberá calcular y presentar métricas básicas de cobertura de requisitos y tasa de éxito de ejecución. | Incluye la tasa de cobertura $C = \frac{R_{\text{cubiertos}}}{R_{\text{totales}}} \times 100$ y el porcentaje de pruebas superadas. | Informes | Introducir 10 requisitos, generar pruebas para 8 de ellos y ejecutar 5. Verificar que el cuadro de mando indica 80% de cobertura de requisitos y calcula correctamente la tasa de éxito de los 5 ejecutados. |
| GMP-RF-013 | El sistema deberá exportar el informe de resultados consolidado en formato PDF y JSON. | Facilita la integración con herramientas externas de gestión de pruebas o CI/CD. | Informes | Generar un informe tras la ejecución y exportarlo en PDF y JSON. Comprobar que ambos archivos contienen los datos de la corrida, matriz de trazabilidad y métricas. |

---

## 3. Requisitos no funcionales

| ID | Requisito | Descripción | Módulo | Cómo comprobarlo |
| --- | --- | --- | --- | --- |
| GMP-RNF-001 | La interfaz de usuario y los mensajes del sistema deberán presentarse en español. | Mantiene un idioma común en el panel de control, validaciones y reportes generados. | Interfaz | Recorrer los flujos de ingesta, visualización de modelos, validación y reporte. Comprobar que todos los textos fijos e instrucciones están en español. |
| GMP-RNF-002 | El tiempo de respuesta de la IA generativa para la creación de un modelo lógico básico (hasta 10 requisitos) no deberá superar los 15 segundos. | Garantiza una experiencia interactiva ágil durante las sesiones de modelado. | Rendimiento | Cargar un documento con 10 requisitos, cronometrar desde la solicitud de generación de modelo hasta su despliegue en pantalla y verificar que no excede los 15 segundos. |
| GMP-RNF-003 | El sistema deberá almacenar el histórico de prompts, versiones de modelos y casos de prueba generados para garantizar la auditabilidad y reproducibilidad. | Registra la configuración de la IA y la semilla/versión utilizada para cada artefacto generado. | Seguridad y Auditoría | Consultar el registro de auditoría de una ejecución anterior y verificar que se detallan la versión de la IA, el prompt enviado y el identificador de la corrida. |