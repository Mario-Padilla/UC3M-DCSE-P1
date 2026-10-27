# Contexto y alcance del sistema

**Fuentes:** apartados 1.2 y 1.3 del [enunciado de la práctica](../enunciado/P1.docx.pdf) y documento `documento_requisitos_v1.md`, facilitado como referencia.

## 1. Descripción general del sistema

El sistema objeto de estudio es el software de una máquina expendedora de café. Permite al cliente seleccionar y comprar una bebida. Además, coordina su preparación e informa de las incidencias que puedan afectar al servicio.

El enunciado establece cinco funcionalidades principales: seleccionar bebidas, gestionar el pago, comprobar la disponibilidad de ingredientes, preparar la bebida y comunicar incidencias al usuario. El alcance debe ser acotado; no se pretende desarrollar un sistema industrial completo.

El software controla las operaciones de una máquina de bebidas calientes en vaso: selección, pago, comprobación de existencias, preparación y comunicación de incidencias. Intercambia información con el terminal de pago sin contacto, los sensores y los mecanismos de preparación. No incluye funciones de administración. El diseño y la fabricación del hardware quedan fuera del alcance.

**Límite del sistema e interacciones identificadas:**

```mermaid
flowchart LR
    C[Cliente] -->|selección y operación de compra| S
    S -->|información sobre la compra, la preparación y las incidencias| C
    S <-->|solicitud de pago y resultado| T[Terminal de pago sin contacto]
    S <-->|lecturas de sensores y órdenes de preparación| H[Sensores y mecanismos de la máquina]
    S[[Software de control de la máquina]]
```

El cliente interactúa con la aplicación a través de una pantalla y de los botones de la máquina.

**Términos utilizados:**

| Término | Significado en este documento |
| --- | --- |
| Bebida | Producto que el cliente puede seleccionar para su preparación. El catálogo y las recetas iniciales figuran en el apartado 3. |
| Ingrediente | Recurso necesario para preparar una bebida. Las cantidades figuran en las recetas del apartado 3, salvo las dosis de azúcar, que están pendientes de definir. |
| Disponibilidad | Existencia de los ingredientes necesarios para preparar la bebida seleccionada. |
| Incidencia | Situación que impide prestar el servicio o altera su funcionamiento y que debe comunicarse al cliente. Los casos concretos se definirán en los requisitos. |
| Receta | Definición de los ingredientes y cantidades necesarios para preparar una bebida. Las recetas iniciales se indican en el apartado 3. |
| Autorización de pago | Resultado comunicado por el terminal de pago sin contacto para indicar si se autoriza el cobro de la operación. |

## 2. Actores

| Actor | Necesidad u objetivo | Tipo |
| --- | --- | --- |
| Cliente | Seleccionar y comprar una bebida, recibirla y conocer las incidencias que puedan afectar a la compra. | Actor humano |
| Terminal de pago sin contacto | Comunicar la autorización o la denegación del pago solicitado por la aplicación. | Sistema externo |

El procesamiento bancario se realiza fuera de la aplicación. Esta recibe el resultado de la solicitud de pago a través del terminal. No se admiten pagos en efectivo.

### Necesidades de los interesados

Las siguientes necesidades describen lo que el cliente espera del sistema:

| Interesado | Necesidad |
| --- | --- |
| Cliente | Conocer las bebidas disponibles y su precio antes de elegir. |
| Cliente | Pagar la bebida seleccionada con tarjeta sin contacto. |
| Cliente | Recibir la bebida seleccionada. |
| Cliente | Conocer el motivo si no se entrega la bebida y recuperar el importe cuando corresponda. |

## 3. Alcance funcional

Las funciones siguientes delimitan el comportamiento general del software.

| Función | Descripción |
| --- | --- |
| Selección de bebidas | Mostrar el catálogo. Permitir que el cliente elija una bebida y un nivel de azúcar de 0 a 3. |
| Gestión del pago | Solicitar el pago de la bebida al terminal de pago sin contacto. Recibir el resultado de la solicitud. |
| Comprobación de ingredientes y existencias | Comprobar que hay ingredientes y vasos suficientes para preparar la bebida seleccionada. Actualizar las existencias una vez finalizada la preparación. |
| Preparación de la bebida | Coordinar la preparación de la bebida según su receta y su entrega en un vaso. Para ello, utilizar los sensores y los mecanismos de la máquina, que dispone de un depósito interno de agua. |
| Comunicación de incidencias | Informar al cliente de las incidencias que afecten al servicio, así como del progreso y de la finalización de la preparación. |

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

Quedan fuera del alcance el diseño y la fabricación del hardware, así como el procesamiento bancario. La aplicación solicita el pago al terminal de pago sin contacto y recibe el resultado de la solicitud.

## 5. Supuestos

El sistema se define con los siguientes supuestos:

| Supuesto |
| --- |
| Se modela una única máquina y una bebida por operación de compra. |
| Solo se admite el pago con tarjeta sin contacto. |
| La aplicación no contempla un operador ni funciones de administración. El catálogo, los precios, las recetas y las existencias iniciales son datos de partida. |
| La máquina dispone de sensores, un depósito interno de agua y mecanismos para dispensar vasos y preparar bebidas. |
| El cliente puede cancelar la compra antes de que comience la preparación. Si ya se ha efectuado el cobro, se devuelve el importe al medio de pago utilizado. Si un fallo durante la preparación impide entregar la bebida, también se devuelve el importe. |

Al redactar los requisitos habrá que concretar:

- Las dosis de azúcar correspondientes a cada nivel.
- El umbral que determina cuándo las existencias de un ingrediente son bajas.
- Las señales concretas de los sensores.
- El comportamiento ante la denegación del pago con tarjeta.
- La secuencia detallada de selección, comprobación, pago y preparación.
- Los mensajes concretos para comunicar incidencias.

## 6. Casos de uso principales

Los siguientes casos de uso resumen las interacciones principales del sistema. Su desarrollo detallado se recogerá en los requisitos y en los escenarios de verificación.

| Caso de uso | Actor principal | Interacción y resultado esperado | Alternativas por concretar |
| --- | --- | --- | --- |
| Seleccionar una bebida | Cliente | El cliente consulta el catálogo y elige una bebida. El sistema registra la selección para continuar la compra. | Cambio de selección y opciones de personalización. |
| Pagar la bebida seleccionada | Cliente | El cliente utiliza una tarjeta sin contacto para pagar. La aplicación solicita el pago al terminal y recibe el resultado. | Pago denegado. |
| Cancelar una compra | Cliente | El cliente cancela la compra antes de que comience la preparación. Si ya se ha efectuado el cobro, se devuelve el importe al medio de pago utilizado. | La cancelación deja de estar disponible al iniciarse la preparación. |
| Solicitar la preparación de una bebida | Cliente | La aplicación comprueba que hay ingredientes y vasos suficientes. A continuación, coordina la preparación y la entrega de la bebida seleccionada. | Si un fallo durante la preparación impide entregar la bebida, se devuelve el importe al medio de pago utilizado. |
| Consultar una incidencia comunicada por la máquina | Cliente | La aplicación informa al cliente de un problema relacionado con la compra o con la preparación. | El mensaje y las acciones posteriores dependen de la incidencia y del estado de la operación. |

La comprobación de ingredientes forma parte del proceso de compra y preparación. El cliente no la inicia como una operación independiente.
