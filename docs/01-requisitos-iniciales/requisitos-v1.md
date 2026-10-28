# Requisitos iniciales del sistema — v1

## 1. Introducción

Este documento define los requisitos iniciales del software de una máquina expendedora de café. Se basa en el [contexto y alcance del sistema](contexto-y-alcance.md) y en el apartado 1.3 del [enunciado de la práctica](../enunciado/P1.docx.pdf).

Se contempla una única máquina, con una bebida por compra y pago exclusivamente con tarjeta sin contacto. El catálogo, los precios, las recetas y las existencias iniciales se proporcionan como datos de partida. La aplicación no incluye funciones de administración ni de personalización de las bebidas.

Los requisitos se agrupan en funcionales (`CAF-RF`) y no funcionales (`CAF-RNF`). Los módulos son agrupaciones por función, no componentes de una arquitectura ya implementada. La columna «Cómo comprobarlo» recoge el criterio de verificación; describe comprobaciones previstas, no pruebas ejecutadas.

Las reglas de cancelación, reintentos, devolución y consumo real, así como los dos requisitos no funcionales, incorporan las decisiones comunicadas por el equipo. Se supone que los mecanismos comunican al software las cantidades de ingredientes y vasos realmente consumidos, incluso ante un fallo; la medición física queda fuera del alcance. Estas decisiones no se presentan como exigencias adicionales del enunciado. El tratamiento de fallos de la solicitud de devolución queda fuera del alcance y no se fija un tiempo máximo de respuesta para comunicar la disponibilidad.

## 2. Requisitos funcionales

### Selección

| ID | Requisito | Descripción | Módulo | Cómo comprobarlo |
| --- | --- | --- | --- | --- |
| CAF-RF-001 | El sistema deberá mostrar el nombre y el precio de cada bebida del catálogo. | Permite conocer la oferta antes de comprar. El catálogo está definido en el documento de contexto y alcance. | Selección | Abrir la pantalla de selección y comparar los nombres y precios mostrados con las seis bebidas del catálogo. |
| CAF-RF-002 | El sistema deberá permitir seleccionar una bebida del catálogo por operación de compra. | Cada compra corresponde a una única bebida. | Selección | Seleccionar un cortado y comprobar que la operación queda asociada a esa bebida, sin incluir otras bebidas. |
| CAF-RF-003 | Si la bebida seleccionada no está disponible, el sistema deberá permitir seleccionar otra bebida sin exigir una cancelación previa. | La nueva selección sustituye a la anterior y se comprueba su disponibilidad antes de solicitar el pago. En los demás casos, cambiar de bebida requiere cancelar la operación mientras esté permitido. | Selección | Seleccionar un cortado sin café suficiente y después elegir un chocolate con existencias suficientes. Comprobar que se permite el cambio y se comprueba la nueva receta antes de solicitar el pago. |

### Existencias

| ID | Requisito | Descripción | Módulo | Cómo comprobarlo |
| --- | --- | --- | --- | --- |
| CAF-RF-004 | El sistema deberá comprobar, antes de solicitar el pago, que las existencias de cada ingrediente alcanzan para preparar la bebida seleccionada según su receta. | Incluye el agua y los ingredientes de la receta, sin exigir ingredientes que esa bebida no utiliza. | Existencias | Seleccionar un cortado con 7 g de café, 4 g de leche y 60 ml de agua disponibles. Comprobar que supera la comprobación. Repetir con 6 g de café y comprobar que se detecta la falta de disponibilidad antes de solicitar el pago. |
| CAF-RF-005 | El sistema deberá comprobar que hay al menos un vaso disponible antes de solicitar el pago. | La bebida se entrega en un vaso dispensado por la máquina. | Existencias | Seleccionar una bebida con ingredientes suficientes y ningún vaso disponible. Comprobar que se detecta la falta de vasos antes de solicitar el pago. Repetir con un vaso disponible y comprobar que esta condición se cumple. |
| CAF-RF-006 | El sistema deberá impedir la solicitud de pago si faltan ingredientes o vasos para preparar la bebida seleccionada. | Evita cobrar una bebida que no puede servirse. | Existencias | Seleccionar una bebida sin ingredientes suficientes y comprobar que no se envía una solicitud al terminal de pago. Repetir con ingredientes suficientes, pero sin vasos. |
| CAF-RF-007 | El sistema deberá informar al cliente cuando la bebida seleccionada no esté disponible por falta de ingredientes o vasos. | El cliente debe conocer el motivo por el que no puede continuar la compra. | Información al cliente | Seleccionar una bebida sin un ingrediente necesario y comprobar que aparece un aviso de falta de disponibilidad. Repetir sin vasos y comprobar que también se informa de la incidencia. |
| CAF-RF-008 | El sistema deberá descontar de las existencias las cantidades de ingredientes realmente consumidas al finalizar una preparación, tanto si se completa como si falla. | En una preparación completa, el consumo corresponde a la receta. Ante un fallo parcial, el sistema utiliza las cantidades comunicadas por los mecanismos y no descuenta la receta completa si solo se ha consumido una parte. | Existencias | Preparar un cortado y comprobar que se descuentan 7 g de café, 4 g de leche y 60 ml de agua, sin cambiar el cacao. Simular después un fallo con un consumo comunicado de 7 g de café, 0 g de leche y 20 ml de agua; comprobar que solo se descuentan esas cantidades. |
| CAF-RF-009 | El sistema deberá descontar de las existencias los vasos realmente consumidos durante una preparación, aunque un fallo impida entregar la bebida. | El sistema utiliza la cantidad de vasos comunicada por los mecanismos. Si no se consume ningún vaso, las existencias no cambian. | Existencias | Completar una preparación con dos vasos disponibles y comprobar que queda uno. Repetir con un fallo después de consumir un vaso y comprobar el mismo descuento. Provocar un fallo sin consumir vaso y comprobar que siguen disponibles los dos. |

### Pago

| ID | Requisito | Descripción | Módulo | Cómo comprobarlo |
| --- | --- | --- | --- | --- |
| CAF-RF-010 | El sistema deberá solicitar al terminal de pago sin contacto el cobro del precio de la bebida seleccionada, una vez comprobada su disponibilidad. | El procesamiento bancario corresponde al sistema externo. | Pago | Seleccionar un café con leche con existencias suficientes y comprobar que el terminal recibe una solicitud de 1,20 € después de comprobar ingredientes y vasos. |
| CAF-RF-011 | El sistema deberá impedir el inicio de la preparación mientras el terminal no haya autorizado el pago. | Una solicitud pendiente o denegada no permite preparar la bebida. | Pago | Mantener pendiente la respuesta del terminal y comprobar que no comienza la preparación. Repetir con una respuesta de pago denegado. |
| CAF-RF-012 | El sistema deberá informar al cliente cuando el terminal deniegue el pago. | Distingue una denegación de pago de un problema de disponibilidad. | Información al cliente | Hacer que el terminal devuelva una denegación y comprobar que aparece un mensaje que indica que el pago no ha sido autorizado. |
| CAF-RF-013 | El sistema deberá permitir reintentar el pago después de cada denegación, sin imponer un número máximo de intentos. | El cliente puede volver a intentarlo sin seleccionar de nuevo la bebida o cancelar mientras no haya autorización. | Pago | Denegar sucesivos intentos de pago de un cortado y comprobar que tras cada denegación se puede solicitar de nuevo el pago de 1,10 € para la misma bebida o cancelar. Revisar que no existe un límite de intentos configurado. |

### Cancelación

| ID | Requisito | Descripción | Módulo | Cómo comprobarlo |
| --- | --- | --- | --- | --- |
| CAF-RF-014 | El sistema deberá permitir cancelar la operación mientras no haya recibido la autorización del pago. | Incluye la cancelación antes de solicitar el pago, mientras la respuesta está pendiente y después de una denegación. Una operación cancelada no inicia la preparación. | Compra | Cancelar antes de solicitar el pago, con respuesta pendiente y tras una denegación. Comprobar en cada caso que se acepta la cancelación y no se emiten órdenes de preparación. |
| CAF-RF-015 | Si el terminal autoriza el pago después de haberse cancelado la operación, el sistema deberá solicitar la devolución del importe completo al medio de pago utilizado. | La autorización tardía no reactiva la compra ni inicia la preparación. El tratamiento de un fallo de la solicitud de devolución queda fuera del alcance. | Pago | Cancelar una compra de café con leche con el pago pendiente y después comunicar una autorización de 1,20 €. Comprobar que se solicita una devolución de 1,20 € asociada a ese pago y no se inicia la preparación. |
| CAF-RF-016 | El sistema deberá impedir la cancelación de la compra por el cliente una vez recibida la autorización del pago. | El bloqueo se aplica aunque la preparación todavía no haya comenzado. No impide solicitar la devolución por falta de entrega. | Compra | Autorizar el pago e intentar cancelar antes de iniciar la preparación. Comprobar que no se acepta. Repetir durante la preparación. |

### Preparación

| ID | Requisito | Descripción | Módulo | Cómo comprobarlo |
| --- | --- | --- | --- | --- |
| CAF-RF-017 | El sistema deberá iniciar la preparación de la bebida seleccionada cuando se haya comprobado su disponibilidad y autorizado el pago, siempre que la operación no se haya cancelado. | Mantiene la secuencia de selección, comprobación, pago y preparación. | Preparación | Seleccionar una bebida con ingredientes y vasos suficientes, autorizar el pago y comprobar que se inicia su preparación. Repetir con la operación cancelada y comprobar que no se inicia. |
| CAF-RF-018 | El sistema deberá coordinar la preparación de la bebida seleccionada con las cantidades indicadas en su receta. | Las recetas son las del documento de contexto y alcance. | Preparación | Preparar cada una de las seis bebidas y comparar las cantidades indicadas a los mecanismos de preparación con las de su receta. |
| CAF-RF-019 | El sistema deberá ordenar la dispensación de un vaso para entregar la bebida preparada. | La entrega se realiza mediante los mecanismos físicos de la máquina. | Preparación | Completar una compra y comprobar que se ordena dispensar un vaso para esa bebida. |
| CAF-RF-020 | El sistema deberá informar al cliente mientras la bebida se esté preparando. | Permite distinguir la preparación de la espera del pago. | Información al cliente | Autorizar el pago e iniciar la preparación. Comprobar que se muestra un mensaje de preparación en curso. |
| CAF-RF-021 | El sistema deberá avisar al cliente cuando la bebida esté lista para recoger. | Comunica la finalización de la preparación y la entrega. | Información al cliente | Completar la preparación y comprobar que aparece un aviso para recoger la bebida. |

### Incidencias durante la preparación

| ID | Requisito | Descripción | Módulo | Cómo comprobarlo |
| --- | --- | --- | --- | --- |
| CAF-RF-022 | Si un fallo durante la preparación impide entregar la bebida, el sistema deberá informar al cliente de que no se ha podido completar el servicio. | El cliente debe conocer que no recibirá la bebida comprada. | Información al cliente | Introducir una señal de fallo del mecanismo de preparación que impida la entrega. Comprobar que aparece un aviso de servicio no completado. |
| CAF-RF-023 | Si un fallo impide entregar una bebida ya cobrada, el sistema deberá solicitar la devolución del importe completo al medio de pago utilizado. | Se solicita la devolución por falta de entrega, no por cancelación voluntaria después del pago. El tratamiento de un fallo de la solicitud de devolución queda fuera del alcance. | Pago | Cobrar 1,30 € por un chocolate y provocar un fallo que impida entregarlo. Comprobar que se solicita una devolución de 1,30 € asociada al pago original. Repetir con un fallo anterior al inicio de la preparación y posterior al cobro. |
| CAF-RF-024 | Si un fallo durante la preparación impide entregar la bebida, el sistema deberá finalizar la operación sin iniciar automáticamente otra preparación. | Cualquier nueva compra requiere una operación independiente. | Compra | Provocar un fallo que impida entregar la bebida y comprobar que termina la operación sin emitir una nueva orden de preparación. |

## 3. Requisitos no funcionales

Los siguientes requisitos de calidad han sido aprobados por el equipo durante la revisión de decisiones. Son decisiones del equipo, no exigencias atribuidas al enunciado.

| ID | Requisito | Descripción | Módulo | Cómo comprobarlo |
| --- | --- | --- | --- | --- |
| CAF-RNF-001 | Los textos de la interfaz dirigidos al cliente deberán estar en español. | Mantiene un idioma común en las pantallas y los avisos. | Interfaz | Recorrer la selección, el pago, la cancelación, la preparación y las incidencias. Comprobar que las instrucciones y los mensajes están en español. |
| CAF-RNF-002 | El sistema deberá manejar los importes de pago y devolución en céntimos exactos, sin errores de redondeo respecto a los precios del catálogo. | El importe solicitado debe coincidir con el precio, también al devolverlo. | Pago | Solicitar pagos y devoluciones para las seis bebidas del catálogo. Comparar los importes transmitidos al terminal, expresados en céntimos, con los valores del catálogo. |
