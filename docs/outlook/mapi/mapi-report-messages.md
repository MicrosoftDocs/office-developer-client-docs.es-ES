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

Los proveedores de almacenamiento de mensajes inician los informes de estado de lectura mediante una llamada al método [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) y se envían al destinatario representado por el identificador de entrada en la propiedad **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)). Los informes de estado de lectura no se generan automáticamente; las aplicaciones cliente que quieran recibirlas deben solicitarlas explícitamente.
  
Un informe de lectura indica que se ha establecido la marca de lectura de un mensaje, lo que puede ocurrir cuando se abre, imprime, mueve o copia el mensaje. Si un proveedor de al almacenamiento de mensajes genera o no un informe de lectura en respuesta a una operación de movimiento o copia depende de dónde vaya el mensaje. Si se mueve o copia a otro almacén de mensajes, lo más probable es que siempre se envíe un informe de lectura. Si se mueve o copia en el almacén de mensajes actual, es posible que se envíe un informe de lectura. 
  
Un informe no leído indica que la marca de lectura de un mensaje no está establecida y que el mensaje no se abrió antes de colocarse en la carpeta Elementos eliminados o antes de la expiración de un límite de tiempo. Los clientes pueden llamar al [método IMessage::SetReadFlag](imessage-setreadflag.md) o [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) para establecer o borrar la marca de lectura de un mensaje. 
  
## <a name="delivery-status-reports"></a>Informes de estado de entrega

El estado de entrega se refleja en un informe de entrega, que se envía cuando un mensaje llega a su destinatario previsto, y en un informe de no entrega, que se envía cuando un mensaje no puede llegar a un destinatario. Los informes de estado de entrega se envían al destinatario representado por el identificador de entrada de la propiedad **PR_REPORT_ENTRYID** o al remitente si esta propiedad no está presente. 
  
Los informes de entrega se envían solo mediante solicitud y no incluyen el mensaje original. Los informes Nondelivery se envían automáticamente a menos que se haga una solicitud para suprimirlos. Los informes de no entrega incluyen el mensaje original como datos adjuntos para permitir que el destinatario del informe vuelva a enviar el mensaje en caso de que cualquier cosa que bloquee la entrega ya no sea un problema. El mensaje adjunto se asemeja al original tal como existía cuando se llamó al método [IMessage::SubmitMessage](imessage-submitmessage.md) para enviarlo inicialmente. 
  
Los proveedores de transporte generan uno o más informes de estado de entrega cuando llaman al método [IMAPISupport::StatusRecips.](imapisupport-statusrecips.md) Los proveedores de transporte componen una lista de destinatarios para un mensaje. Si un destinatario recibe o no un informe y el tipo de informe que se genera depende de lo siguiente: 
  
- Los informes de entrega van a destinatarios que establecen la propiedad **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) en TRUE antes de colocar el mensaje en el almacén de mensajes.
    
- Los informes nondelivery van a destinatarios que no han establecido la propiedad **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) en FALSE. 
    
Casi toda la información necesaria para mostrar un informe de no entrega se encuentra en la tabla de destinatarios del mensaje adjunto. Algunas propiedades son del propio informe. Para los informes de entrega, la información necesaria se incluye en la tabla de destinatarios del informe y en algunas propiedades del informe. 
  
Los informes son mensajes con clases de mensaje distintas, en función de la clase del mensaje enviado. La mayoría de los proveedores de servicios usan una convención de nomenclatura por la que la clase de mensaje se compone de varias partes separadas por puntos. La primera parte es "Informe" y la última parte es una constante que representa el tipo de informe. La parte central está reservada para la clase del mensaje enviado. Por ejemplo, dado que un informe de entrega usa la recuperación ante desastres constante, la clase de mensaje para un informe de entrega sobre un IPM. El mensaje de nota **sería Report.IPM.Note.DR**.
  
En la tabla siguiente se muestran las constantes que representan los tipos de informes.
  
|**Tipo de informe**|**Constante usada en la clase de mensaje**|
|:-----|:-----|
|Lectura  <br/> |IPNRN  <br/> |
|No leído  <br/> |IPNNRN  <br/> |
|Delivery  <br/> |Recuperación ante desastres  <br/> |
|Nondelivery  <br/> |NDR  <br/> |
   
Los clientes interactivos pueden mostrar mensajes de informe mediante formularios estándar proporcionados por MAPI o formularios personalizados que se han registrado con el administrador de formularios para la clase de mensaje del informe. Clientes que reciben un informe de no entrega para un IPM. El mensaje de nota, por ejemplo, puede mostrar el formulario MAPI estándar que presenta una lista de los destinatarios con errores y un motivo sugerido para el error. El formulario también permite al usuario volver a enviar el mensaje, si lo desea. 
  
## <a name="see-also"></a>Consulte también



[Mensajes MAPI](mapi-messages.md)

