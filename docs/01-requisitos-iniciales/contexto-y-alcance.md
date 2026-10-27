# Contexto y alcance del sistema

**Estado:** pendiente de revisión del equipo.

**Fuente:** [enunciado de la práctica](../enunciado/P1.docx.pdf), apartados 1.2 y 1.3. Este documento prepara la redacción de [requisitos v1](requisitos-v1.md), que todavía no contiene requisitos. La metodología se recoge en el [README](../../README.md).

**Responsable y revisor del equipo:** TODO: identificar cuando el equipo los comunique.

## 1. Descripción general del sistema

El sistema objeto de estudio es el software de una máquina de café de vending. Su propósito es permitir que una persona seleccione una bebida y complete su compra y preparación, recibiendo información sobre las incidencias que puedan impedir el servicio.

El enunciado establece cinco funcionalidades principales: seleccionar bebidas, gestionar el pago, comprobar la disponibilidad de ingredientes, preparar la bebida y comunicar incidencias al usuario. El alcance debe ser acotado; no se pretende desarrollar un sistema industrial completo.

La frontera del sistema comprende la lógica de software que coordina estas funciones. El usuario interactúa mediante una interfaz cuyo formato está pendiente de definir. Los mecanismos de pago, los datos de disponibilidad y los elementos físicos de preparación constituyen puntos de interacción que deberán concretarse al redactar los requisitos. Esta descripción no presupone un hardware ni una tecnología específicos.

Si se realiza el ejercicio 4, el enunciado permite implementar una simulación software. La decisión de realizarlo y el alcance de esa implementación siguen pendientes.

**Términos utilizados:**

| Término | Significado en este documento |
| --- | --- |
| Bebida | Producto que el usuario puede seleccionar para su preparación. El catálogo está pendiente de definir. |
| Ingrediente | Recurso necesario para preparar una bebida. Los ingredientes y las cantidades se concretarán con las recetas. |
| Disponibilidad | Existencia de los ingredientes necesarios para preparar la bebida seleccionada. |
| Incidencia | Situación que impide o altera el servicio y que debe comunicarse al usuario. Los casos concretos se definirán en los requisitos. |

## 2. Actores

| Actor | Necesidad u objetivo | Situación |
| --- | --- | --- |
| Usuario de la máquina | Seleccionar una bebida, realizar el pago y recibir la bebida o información sobre la incidencia que impide obtenerla. | Actor principal identificado a partir del caso de estudio. |
| Personal de reposición y mantenimiento | Reponer ingredientes y resolver problemas de funcionamiento de la máquina. | Actor contextual propuesto. Pendiente de confirmar si interactuará con el software; no se incluyen todavía funciones de administración o mantenimiento. |

Los posibles sistemas externos de pago no se consideran actores confirmados hasta que el equipo concrete el medio de pago y sus interfaces.

## 3. Alcance funcional

Las siguientes funciones proceden del apartado 1.2 del enunciado. Describen el alcance general y todavía no constituyen requisitos detallados ni aprobados.

| Función | Descripción | Aspectos por concretar |
| --- | --- | --- |
| Selección de bebidas | Permitir al usuario elegir una bebida entre las opciones ofrecidas. | Catálogo y posibles opciones de personalización. |
| Gestión del pago | Gestionar el pago asociado a la bebida seleccionada. | Medios de pago, precios, confirmación del pago y tratamiento de pagos incompletos, cancelaciones y devoluciones. |
| Comprobación de ingredientes | Comprobar si existen ingredientes suficientes para preparar la bebida elegida. | Recetas, cantidades, representación de existencias y momento de comprobación respecto al pago. |
| Preparación de la bebida | Coordinar la preparación de la bebida seleccionada. | Condiciones de inicio, finalización, actualización de existencias y tratamiento de fallos. |
| Comunicación de incidencias | Informar al usuario de los problemas que afecten al servicio. | Incidencias contempladas, contenido de los mensajes y opciones disponibles tras cada incidencia. |

## 4. Fuera del alcance

El enunciado excluye el desarrollo de un sistema industrial completo. Para concretar ese límite, se proponen las siguientes exclusiones, pendientes de validación del equipo:

- Diseño y fabricación del hardware de la máquina.
- Gestión de proveedores, compras y logística de reposición.
- Gestión remota de una red de máquinas y análisis comercial de ventas.
- Cuentas de usuario, programas de fidelización y promociones.
- Procedimientos físicos de limpieza, reparación y reposición. Su eventual interacción con el software requiere una decisión de alcance.

Estas exclusiones son propuestas de acotación, no obligaciones adicionales del enunciado.

## 5. Supuestos

Los siguientes supuestos son propuestas para facilitar el análisis. No deben convertirse en requisitos aprobados sin revisión del equipo.

| Supuesto propuesto | Implicación | Estado |
| --- | --- | --- |
| El estudio se limita a una única máquina. | No se modela la coordinación entre varias máquinas. | Pendiente de validación. |
| Cada operación de compra corresponde a una bebida. | Las compras de varias bebidas en una sola operación no se incluyen en el borrador. | Pendiente de validación. |
| El catálogo, los precios, las recetas y las existencias iniciales estarán disponibles como datos del sistema. | Será necesario definir esos datos; su configuración mediante una interfaz de administración no se da por incluida. | Pendiente de validación. |

Antes de cerrar el alcance y redactar los comportamientos detallados, el equipo debe concretar:

- El catálogo de bebidas y las opciones de personalización, si las hay.
- Los medios de pago, los precios y las políticas de cancelación, cambio y devolución que correspondan.
- Las recetas, las cantidades de ingredientes y la forma de representar su disponibilidad.
- La secuencia entre selección, comprobación de ingredientes, pago y preparación, incluido el tratamiento de incidencias después del pago.
- La inclusión o exclusión de interacciones de reposición y mantenimiento con el software.
- Los supuestos y las exclusiones propuestos en este documento.

La decisión sobre el ejercicio 4 y su tecnología puede abordarse posteriormente; no impide preparar los requisitos iniciales del ejercicio 1.

## 6. Casos de uso principales

Los casos siguientes son una descripción preliminar derivada de las cinco funciones del enunciado. No fijan todavía la secuencia completa de compra ni sustituyen a los futuros requisitos y escenarios verificables.

| Caso de uso | Actor principal | Interacción y resultado esperado | Alternativas por concretar |
| --- | --- | --- | --- |
| Seleccionar una bebida | Usuario de la máquina | El usuario consulta las opciones ofrecidas y elige una bebida; el sistema registra la selección para continuar la compra. | Cambio de selección y opciones de personalización. |
| Pagar la bebida seleccionada | Usuario de la máquina | El usuario realiza el pago por un medio admitido; el sistema determina si se ha completado. | Pago insuficiente, rechazado o interrumpido; cancelación y devolución. |
| Solicitar la preparación de una bebida | Usuario de la máquina | Como parte de la compra, el sistema comprueba los ingredientes y coordina la preparación cuando se cumplen las condiciones que se definan en los requisitos. | Falta de ingredientes o fallo durante la preparación, con atención al estado del pago. |
| Consultar una incidencia comunicada por la máquina | Usuario de la máquina | El sistema informa de un problema relacionado con la compra o preparación para que el usuario conozca la situación. | Mensaje y acciones posteriores según la incidencia y el estado de la operación. |

La comprobación de ingredientes forma parte de la compra y preparación; no se presupone que el usuario tenga que iniciarla como una operación independiente.
