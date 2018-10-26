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
ms.openlocfilehash: 2c1f73ab263e5851c78b33b6157d6d44c9e5e404
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586231"
---
# <a name="sending-messages-transport-provider-tasks"></a>Env�o de mensajes: Tareas de proveedor de transporte

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
 **Para transmitir un mensaje, los proveedores de transporte**
  
- Establezca la propiedad del mensaje **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) en TRUE después de que el proveedor de transporte se envió el mensaje o ha intentado enviar el mensaje. If an attempt to send a message fails, transport providers should call [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) to generate a nondelivery report. Si el mensaje se envió correctamente y la propiedad **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) está establecida en TRUE, cree una estructura [ADRLIST](adrlist.md) que contiene a los destinatarios correctos, al establecer la propiedad **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) para cada uno y llame a **StatusRecips** para generar un informe de entrega. For more information about creating delivery and non-delivery reports, see the following topics: [Mensajes de informe MAPI](mapi-report-messages.md), [Propiedades del mensaje requerido del informe](required-report-message-properties.md), [Propiedades de mensajes de informe opcionales](optional-report-message-properties.md), and [Enviar informes de entrega de mensajes](sending-message-delivery-reports.md).
    
- Establecer el grupo de **PR_SENDER** del mensaje de propiedades a la identidad del usuario que ha iniciado sesi�n. Este grupo se incluyen: **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)), **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)), **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)), **PR_SENDER_ADDRTYPE** ([ PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) y **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)).
    
- Establezca las propiedades del mensaje **PR_SENT_REPRESENTING**, si es posible, en cualquiera de los dos la identidad del usuario que ha iniciado sesi�n o a una identidad de delegado v�lido. Las propiedades **PR_SENT_REPRESENTING** se usan para implementar el env�o de mensajes por un usuario en nombre de otro usuario. Los proveedores de transporte que no admiten estas propiedades deben omitir a ellos en los mensajes salientes. 
    
- Establezca la propiedad del mensaje **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) para indicar cuando el cliente llama a [IMessage::SubmitMessage](imessage-submitmessage.md).
    
- Establezca la propiedad del mensaje **PR_PROVIDER_SUBMIT_TIME** ([PidTagProviderSubmitTime](pidtagprovidersubmittime-canonical-property.md)) para indicar la fecha y hora en que el proveedor de almacén de mensajes marca el mensaje como tener se ha enviado. 
    
Cuando se env�a un mensaje a una variedad de destinatarios con varios sistemas de mensajer�a, cada copia transmitido tendr� una identidad de remitente diferentes. 
  
El proveedor de transporte o el almac�n de mensajes acoplado y el transporte tambi�n es responsable de autor y responder a informaci�n de configuraci�n. Informaci�n de autor se almacena en las propiedades **PR_ORIGINATOR** y responder a la informaci�n se almacena en las propiedades PR_REPLY. El cliente puede establecer estas propiedades; Sin embargo, el proveedor de transporte se puede pasar por alto y sobrescribir la configuraci�n del cliente. 
  

