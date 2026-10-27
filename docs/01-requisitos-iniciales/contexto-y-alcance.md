# Contexto y alcance del sistema

**Fuentes:** [enunciado de la práctica](../enunciado/P1.docx.pdf), apartados 1.2 y 1.3, y el documento `documento_requisitos_v1.md` facilitado para contraste. Este documento prepara la redacción de [requisitos v1](requisitos-v1.md), que todavía no contiene requisitos. La metodología se recoge en el [README](../../README.md).

## 1. Descripción general del sistema

El sistema objeto de estudio es el software de una máquina de café de vending. Su propósito es permitir que una persona seleccione una bebida y complete su compra y preparación, recibiendo información sobre las incidencias que puedan impedir el servicio.

El enunciado establece cinco funcionalidades principales: seleccionar bebidas, gestionar el pago, comprobar la disponibilidad de ingredientes, preparar la bebida y comunicar incidencias al usuario. El alcance debe ser acotado; no se pretende desarrollar un sistema industrial completo.

La frontera del sistema comprende el software que coordina la selección, el pago, la comprobación de existencias, la preparación y la comunicación de incidencias de una máquina de bebidas calientes en vaso. El software intercambia información con el terminal de tarjeta sin contacto y con los sensores y mecanismos de preparación. No incluye funciones de administración para un operador. El diseño y la fabricación del hardware quedan fuera del alcance.

**Límite del sistema e interacciones identificadas:**

```mermaid
flowchart LR
    C[Cliente] -->|selección y operación de compra| S
    S -->|información, bebida o incidencia| C
    S <-->|solicitud de pago y resultado| T[Terminal de tarjeta sin contacto]
    S <-->|lecturas de sensores y órdenes de preparación| H[Sensores y mecanismos de la máquina]
    S[[Software de control de la máquina]]
```

El cliente interactúa mediante una pantalla y botones.

**Términos utilizados:**

| Término | Significado en este documento |
| --- | --- |
| Bebida | Producto que el cliente puede seleccionar para su preparación. El catálogo y las recetas iniciales figuran en el apartado 3. |
| Ingrediente | Recurso necesario para preparar una bebida. Los ingredientes y las cantidades se concretarán con las recetas. |
| Disponibilidad | Existencia de los ingredientes necesarios para preparar la bebida seleccionada. |
| Incidencia | Situación que impide o altera el servicio y que debe comunicarse al usuario. Los casos concretos se definirán en los requisitos. |
| Receta | Definición de los ingredientes y cantidades necesarios para preparar una bebida. Las recetas iniciales se indican en el apartado 3. |
| Autorización de pago | Resultado comunicado por el terminal de tarjeta para indicar si se autoriza el cobro de la operación. |

## 2. Actores

| Actor | Necesidad u objetivo | Tipo |
| --- | --- | --- |
| Cliente | Seleccionar una bebida, pagar con tarjeta sin contacto y recibir la bebida o información sobre una incidencia. | Único actor humano. |
| Terminal de tarjeta sin contacto | Autorizar o denegar el pago solicitado por la aplicación. | Sistema externo con el que interactúa la aplicación. |

El procesamiento bancario se realiza externamente; la aplicación recibe el resultado de autorización del terminal. No se incluyen monedas ni efectivo.

### Necesidades de los interesados

Estas necesidades resumen lo que espera cada actor del sistema.

| Interesado | Necesidad |
| --- | --- |
| Cliente | Conocer las bebidas disponibles y su precio antes de elegir. |
| Cliente | Pagar la bebida seleccionada con tarjeta sin contacto. |
| Cliente | Recibir la bebida seleccionada o conocer por qué no se ha podido entregar y recuperar el importe cuando corresponda. |

## 3. Alcance funcional

Las funciones siguientes delimitan el comportamiento general del software.

| Función | Descripción |
| --- | --- |
| Selección de bebidas | Mostrar el catálogo y permitir al cliente seleccionar una bebida y un nivel de azúcar de 0 a 3. |
| Gestión del pago | Solicitar al terminal el pago de la bebida mediante tarjeta sin contacto y recibir el resultado. |
| Comprobación de ingredientes y existencias | Comprobar si hay ingredientes y vasos suficientes para la bebida y actualizar las existencias tras su preparación. |
| Preparación de la bebida | Preparar y entregar en vaso la bebida conforme a la receta, usando el depósito de agua, sensores y mecanismos de preparación. |
| Comunicación de incidencias | Informar al cliente de problemas que impidan o afecten al servicio y comunicar el progreso y fin de la preparación. |

**Catálogo y recetas iniciales:**

| Código | Bebida | Precio | Café molido (g) | Leche en polvo (g) | Cacao (g) | Agua (ml) |
| --- | --- | ---: | ---: | ---: | ---: | ---: |
| B1 | Café solo | 1,00 € | 7 | — | — | 40 |
| B2 | Café largo | 1,10 € | 7 | — | — | 120 |
| B3 | Cortado | 1,10 € | 7 | 4 | — | 60 |
| B4 | Café con leche | 1,20 € | 7 | 10 | — | 150 |
| B5 | Capuchino | 1,40 € | 7 | 14 | — | 150 |
| B6 | Chocolate | 1,30 € | — | — | 25 | 150 |

El cliente puede seleccionar un nivel de azúcar de 0 a 3. El agua procede de un depósito interno. Cada operación corresponde a una bebida. El catálogo, los precios y las recetas son datos iniciales; la aplicación no incluye funciones para modificarlos ni para registrar reposiciones.

## 4. Fuera del alcance

El alcance del software no incluye el diseño ni la fabricación del hardware ni el procesamiento bancario. La aplicación solicita el pago al terminal de tarjeta sin contacto y recibe su resultado de autorización.

## 5. Supuestos

El sistema se define con los siguientes supuestos:

| Supuesto |
| --- |
| Se modela una única máquina y una bebida por operación de compra. |
| El único medio de pago es tarjeta sin contacto; no se gestionan monedas ni efectivo. |
| No hay actor operador ni funciones de administración. El catálogo, los precios, las recetas y las existencias iniciales son datos de partida. |
| La máquina dispone de sensores, depósito interno de agua y mecanismos de dispensación de vasos y preparación. |
| La cancelación se permite antes de iniciar la preparación. Si un fallo impide entregar la bebida después de iniciarla, se devuelve el importe al medio de pago. |

Al redactar los requisitos habrá que concretar:

- Dosis por nivel de azúcar.
- Umbral que define cuándo el nivel de un ingrediente es bajo.
- Señales concretas de los sensores.
- Comportamiento ante denegación del pago con tarjeta.
- Secuencia detallada de selección, comprobación, pago y preparación.
- Mensajes concretos de incidencias.

## 6. Casos de uso principales

Los casos siguientes resumen las interacciones principales del sistema. No fijan todavía toda la secuencia de compra ni sustituyen a los requisitos y escenarios verificables.

| Caso de uso | Actor principal | Interacción y resultado esperado | Alternativas por concretar |
| --- | --- | --- | --- |
| Seleccionar una bebida | Cliente | El cliente consulta las opciones ofrecidas y elige una bebida; el sistema registra la selección para continuar la compra. | Cambio de selección y opciones de personalización. |
| Pagar la bebida seleccionada | Cliente | El cliente paga con tarjeta sin contacto; la aplicación solicita la operación al terminal y recibe el resultado. | Pago denegado. |
| Cancelar una compra | Cliente | El cliente puede cancelar antes de iniciar la preparación y se devuelve el importe al medio de pago. | La cancelación deja de estar disponible al iniciarse la preparación. |
| Solicitar la preparación de una bebida | Cliente | La aplicación comprueba ingredientes y vasos, prepara la receta seleccionada y entrega la bebida. | Si un fallo impide entregar la bebida después de iniciada la preparación, se devuelve el importe al medio de pago. |
| Consultar una incidencia comunicada por la máquina | Cliente | La aplicación informa de un problema relacionado con la compra o preparación. | Mensaje y acciones posteriores según la incidencia y el estado de la operación. |

La comprobación de ingredientes forma parte de la compra y preparación; no se inicia como una operación independiente del cliente.
