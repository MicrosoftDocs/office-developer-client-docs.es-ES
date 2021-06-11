---
title: Env�o de mensajes Tareas de proveedor de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bd722f48-b166-4670-8dba-897ac50caf37
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 431e3d2f66616db2c586b76387a8521832ed985f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426551"
---
# <a name="sending-messages-transport-provider-tasks"></a>Enviar mensajes: tareas del proveedor de transporte

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 **Para transmitir un mensaje, los proveedores de transporte**
  
- Establezca la propiedad **PR_RESPONSIBILITY** del mensaje ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) en TRUE después de que el proveedor de transporte haya enviado el mensaje o haya intentado enviar el mensaje. If an attempt to send a message fails, transport providers should call [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) to generate a nondelivery report. Si el mensaje se envía correctamente y la propiedad **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) se establece en TRUE, cree una estructura [ADRLIST](adrlist.md) que contenga los destinatarios correctos, establezca la propiedad **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) para cada uno y llame a **StatusRecips** para generar un informe de entrega. For more information about creating delivery and non-delivery reports, see the following topics: [Mensajes de informe MAPI](mapi-report-messages.md), [Propiedades del mensaje requerido del informe](required-report-message-properties.md), [Propiedades de mensajes de informe opcionales](optional-report-message-properties.md), and [Enviar informes de entrega de mensajes](sending-message-delivery-reports.md).
    
- Establecer el grupo de **PR_SENDER** del mensaje de propiedades a la identidad del usuario que ha iniciado sesi�n. Este grupo incluye: **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)), **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)), **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)), **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) y **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)).
    
- Establezca las propiedades del mensaje **PR_SENT_REPRESENTING**, si es posible, en cualquiera de los dos la identidad del usuario que ha iniciado sesi�n o a una identidad de delegado v�lido. Las propiedades **PR_SENT_REPRESENTING** se usan para implementar el env�o de mensajes por un usuario en nombre de otro usuario. Los proveedores de transporte que no admiten estas propiedades deben omitir a ellos en los mensajes salientes. 
    
- Establezca la propiedad PR_CLIENT_SUBMIT_TIME **del** mensaje ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) para indicar cuándo el cliente llamó [a IMessage::SubmitMessage](imessage-submitmessage.md).
    
- Establezca la propiedad **PR_PROVIDER_SUBMIT_TIME** del mensaje ([PidTagProviderSubmitTime](pidtagprovidersubmittime-canonical-property.md)) para indicar la fecha y hora en que el proveedor del almacén de mensajes marcó el mensaje como enviado. 
    
Cuando se env�a un mensaje a una variedad de destinatarios con varios sistemas de mensajer�a, cada copia transmitido tendr� una identidad de remitente diferentes. 
  
El proveedor de transporte o el almac�n de mensajes acoplado y el transporte tambi�n es responsable de autor y responder a informaci�n de configuraci�n. Informaci�n de autor se almacena en las propiedades **PR_ORIGINATOR** y responder a la informaci�n se almacena en las propiedades PR_REPLY. El cliente puede establecer estas propiedades; Sin embargo, el proveedor de transporte se puede pasar por alto y sobrescribir la configuraci�n del cliente. 
  

