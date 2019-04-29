---
title: Mensajes de informe MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 824eb670-16b7-49bf-9992-39fe0586a552
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: aab5c76fb268729f1a50a33e4764905fe3d53405
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405768"
---
# <a name="mapi-report-messages"></a>Mensajes de informe MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los mensajes de informe presentan información de estado sobre un mensaje a su remitente.
  
Hay dos tipos generales de mensajes de informe:
  
- Leer informes de estado.
    
- Informes de estado de entrega.
    
## <a name="read-status-reports"></a>Leer informes de estado

Los proveedores de almacenamiento de mensajes inician los informes de estado de lectura mediante una llamada al método [IMAPISupport:: ReadReceipt](imapisupport-readreceipt.md) y se envían al destinatario representado por el identificador de entrada en el **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)) Inspector. Los informes de estado de lectura no se generan automáticamente; las aplicaciones cliente que quieren recibirlos deben solicitarlos de forma explícita.
  
Un informe de lectura indica que se ha establecido el indicador de lectura de un mensaje, lo que puede ocurrir cuando se abre, se imprime, se mueve o se copia el mensaje. El hecho de que un proveedor de almacenamiento de mensajes genere o no un informe de lectura en respuesta a una operación de mover o copiar depende de dónde se vaya a enviar el mensaje. Si se está moviendo o copiando a otro almacén de mensajes, es probable que se envíe un informe de lectura siempre. Si se mueve o se copia en el almacén de mensajes actual, puede o no enviarse un informe de lectura. 
  
Un informe no leído indica que no se ha establecido el marcador de lectura de un mensaje y que el mensaje no se ha abierto antes de que se coloque en la carpeta elementos eliminados o antes de que expire un límite de tiempo. Los clientes pueden llamar al método [IMessage:: SetReadFlag](imessage-setreadflag.md) o [IMAPIFolder:: SetReadFlags](imapifolder-setreadflags.md) para establecer o borrar el marcador de lectura de un mensaje. 
  
## <a name="delivery-status-reports"></a>Informes de estado de entrega

El estado de entrega se refleja en un informe de entrega, que se envía cuando un mensaje llega a su destinatario y en un informe de no entrega, que se envía cuando un mensaje no puede llegar a un destinatario. Los informes de estado de entrega se envían al destinatario que representa el identificador de entrada en la propiedad **PR_REPORT_ENTRYID** o al remitente si esta propiedad no está presente. 
  
Los informes de entrega se envían por solicitud solamente y no incluyen el mensaje original. Los informes de no entrega se envían automáticamente a menos que se realice una solicitud para suprimirlos. Los informes de no entrega incluyen el mensaje original como datos adjuntos para permitir que el destinatario del informe reenvíe el mensaje en caso de que la entrega bloqueada ya no sea un problema. El mensaje adjunto es similar al original tal como existía cuando el método [IMessage:: SubmitMessage](imessage-submitmessage.md) se llamaba para enviarlo inicialmente. 
  
Los proveedores de transporte generan uno o varios informes de estado de entrega cuando llaman al método [IMAPISupport:: StatusRecips](imapisupport-statusrecips.md) . Los proveedores de transporte componen una lista de destinatarios de un mensaje. Si un destinatario recibe o no un informe y el tipo de informe que se genera depende de lo siguiente: 
  
- Los informes de entrega van a los destinatarios que establecen la propiedad **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PIDTAGORIGINATORDELIVERYREPORTREQUESTED](pidtagoriginatordeliveryreportrequested-canonical-property.md)) en true antes de que el mensaje se colocó en el almacén de mensajes.
    
- Los informes de no entrega van a los destinatarios que no han establecido la propiedad **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PIDTAGORIGINATORNONDELIVERYREPORTREQUESTED](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) en false. 
    
Casi toda la información necesaria para mostrar un informe de no entrega se incluye en la tabla de destinatarios del mensaje adjunto. Algunas propiedades son del propio informe. Para los informes de entrega, la información necesaria se incluye en la tabla de destinatarios del informe y en algunas propiedades del informe. 
  
Los informes son mensajes con distintas clases de mensajes, según la clase del mensaje enviado. La mayoría de los proveedores de servicios usan una Convención de nomenclatura mediante la cual la clase de mensaje se compone de varias partes separadas por puntos. La primera parte es "rePort" y la última parte es una constante que representa el tipo de informe. La parte intermedia está reservada para la clase del mensaje enviado. Por ejemplo, dado que un informe de entrega utiliza la constante DR, la clase de mensaje de un informe de entrega sobre IPM. Nota el mensaje sería **Report. IPM. Note. Dr**.
  
En la siguiente tabla se muestran las constantes que representan los tipos de informes.
  
|**Tipo de informe**|**Constante usada en la clase de mensaje**|
|:-----|:-----|
|Lectura  <br/> |IPNRN  <br/> |
|Leídos  <br/> |IPNNRN  <br/> |
|Delivery  <br/> |RECUPERACIÓN ante desastres  <br/> |
|No entrega  <br/> |5.2.4  <br/> |
   
Los clientes interActivos pueden mostrar mensajes de informe mediante formularios estándar proporcionados por MAPI o formularios personalizados que se han registrado con el administrador de formularios para la clase de mensaje del informe. Clientes que reciben un informe de no entrega para un IPM. Nota el mensaje, por ejemplo, puede mostrar el formulario MAPI estándar que presenta una lista de los destinatarios erróneos y un motivo sugerido para el error. El formulario también permite al usuario volver a enviar el mensaje, si lo desea. 
  
## <a name="see-also"></a>Ver también



[Mensajes MAPI](mapi-messages.md)

