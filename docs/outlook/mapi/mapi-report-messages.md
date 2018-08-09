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
ms.openlocfilehash: addf93cadae418017a40ba448328d2e1fc1decf6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818192"
---
# <a name="mapi-report-messages"></a>Mensajes de informe MAPI

  
  
**Hace referencia a**: Outlook 
  
Notificar mensajes presentar estado la información acerca de un mensaje al remitente.
  
Hay dos tipos generales de mensajes de informe:
  
- Informes de estado de lectura.
    
- Informes de estado de entrega.
    
## <a name="read-status-reports"></a>Informes de estado de lectura

Informes de estado de lectura están iniciados por los proveedores de almacén de mensajes a través de una llamada al método [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) y se envían al destinatario representado por el identificador de entrada en el **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)) propiedad. Informes de estado de lectura no se generan automáticamente; las aplicaciones de cliente que desea recibir ellos deben solicitar explícitamente ellos.
  
Un informe de lectura indica que se ha establecido el indicador de lectura de un mensaje, que puede producirse cuando se abre, imprimir, mover o copiar el mensaje. Si un proveedor de almacén de mensajes genera un informe de lectura en respuesta a un movimiento u operación de copia depende de dónde se dirige el mensaje. Si es que se mueven o se copian a otro almacén de mensajes, un informe de lectura seguramente siempre se envíen. Si es que se va a mover o copiar en el almacén de mensajes actual, un informe de lectura es posible que o es posible que no se enviarán. 
  
Un informe nonread indica que no está establecido el indicador de lectura de un mensaje y que no se abrió el mensaje antes de que se coloca en la carpeta Elementos eliminados o antes de la expiración de un límite de tiempo. Los clientes pueden llamar al método [IMessage::SetReadFlag](imessage-setreadflag.md) o [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) para establecer o Borrar marca de lectura de un mensaje. 
  
## <a name="delivery-status-reports"></a>Informes de estado de entrega

Estado de entrega se refleja en un informe de entrega, que se envía cuando un mensaje ha alcanzado su destinatario, y en un informe de no entrega, que se envía cuando un mensaje no pudo llegar a un destinatario. Si esta propiedad no está presente, informes de estado de entrega se envían al destinatario representado por el identificador de entrada en la propiedad **PR_REPORT_ENTRYID** o al remitente. 
  
Informes de entrega se envían a petición solo y no incluir el mensaje original. Se envían automáticamente los informes de no entrega a menos que se realiza una solicitud para suprimir ellos. Informes de no entrega incluyen el mensaje original como datos adjuntos para habilitar el destinatario del informe para volver a enviar el mensaje en caso de que todo lo que bloquea la entrega ya no es un problema. El mensaje adjunto es similar a la original que existía cuando se llamó al método de [IMessage::SubmitMessage](imessage-submitmessage.md) para enviarlo inicialmente. 
  
Uno o más informes de estado de entrega se generan por los proveedores de transporte cuando llama al método [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) . Los proveedores de transporte de redacción una lista de destinatarios de un mensaje. Si un destinatario recibe un informe y el tipo de informe que se genera depende de lo siguiente: 
  
- Informes de entrega se vaya a destinatarios que establece la propiedad **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) en TRUE antes de que el mensaje se colocó en el almacén de mensajes.
    
- Informes de no entrega vaya a destinatarios que no se ha establecido la propiedad **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) en FALSE. 
    
Casi toda la información necesaria para mostrar un informe de no entrega está contenida en la tabla de destinatarios del mensaje adjunto. Algunas propiedades están en el informe de sí mismo. Para los informes de entrega, incluida la información necesaria en la tabla de destinatarios del informe y en algunas propiedades de informe. 
  
Los informes son mensajes con clases de mensaje distintos, en función de la clase del mensaje enviado. La mayoría de los proveedores de servicios usar una convención de nomenclatura por el cual la clase de mensaje se compone de varias partes, separados por puntos. La primera parte es "Informe" y la última parte es una constante que representa el tipo de informe. La parte central está reservada para la clase del mensaje enviado. Por ejemplo, dado que un informe de entrega usa la recuperación ante desastres constante, la clase de mensaje para la entrega de un informe sobre un IPM. Mensaje de nota sería **Report.IPM.Note.DR**.
  
La siguiente tabla muestran las constantes que representan los tipos de informes.
  
|**Tipo de informe**|**Constante que se utiliza en la clase de mensaje**|
|:-----|:-----|
|Read  <br/> |IPNRN  <br/> |
|Nonread  <br/> |IPNNRN  <br/> |
|Entrega  <br/> |RECUPERACIÓN ANTE DESASTRES  <br/> |
|No entrega  <br/> |NDR  <br/> |
   
Los clientes interactivos pueden mostrar mensajes de informe mediante el uso de formularios estándar de MAPI o formularios personalizados que se han registrado con el Administrador de formulario para la clase de mensaje del informe. Clientes que reciben un informe de no entrega para un IPM. Mensaje de nota, por ejemplo, puede mostrar el formulario estándar de MAPI que presenta una lista de los destinatarios con errores y sugerido motivo del error. El formulario también permite al usuario volver a enviar el mensaje, si así lo desea. 
  
## <a name="see-also"></a>Vea también



[Mensajes MAPI](mapi-messages.md)

