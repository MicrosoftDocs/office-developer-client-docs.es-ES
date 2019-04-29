---
title: Tablas de colas de salida
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 070377ca-ba9e-42ef-ac6b-ff7548b5ccf5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4bf935f58fb20460bbf6baf4b1434be1f3ab8156
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437577"
---
# <a name="outgoing-queue-tables"></a>Tablas de colas de salida

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una tabla de cola de salida contiene información sobre todos los mensajes salientes de un almacén de mensajes. Los proveedores de almacenamiento de mensajes implementan tablas de colas de salida para que la cola MAPI la use. Los almacenes que no admiten el envío o la recepción de mensajes no necesitan implementar esta tabla. 
  
Para tener acceso a una tabla de colas de salida, la cola MAPI llama al método [IMsgStore:: GetOutgoingQueue](imsgstore-getoutgoingqueue.md) . 
  
Hay un requisito de que los mensajes se preprocesen y se envíen al proveedor de transporte en el mismo orden en el que los envió la aplicación cliente. La cola MAPI está diseñada para aceptar mensajes del almacén de mensajes en orden ascendente de tiempo de envío. Debido a este requisito, puede haber algún retraso antes de que aparezcan mensajes en la tabla cola de salida. 
  
Los almacenes de mensajes deben permitir la ordenación en la tabla cola de salida para que la cola MAPI pueda ordenar los mensajes por hora de envío o el criterio de ordenación predeterminado debería ser mediante la hora de envío ascendente. 
  
La tabla cola de salida debe enviar notificaciones cuando cambia el contenido de la cola.
  
Las siguientes propiedades componen el conjunto de columnas necesario en las tablas de colas de salida:
  
|||
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |
|**** Es ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
|**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))  <br/> | <br/> |
   
Para obtener más información acerca de cómo se usa la tabla cola de salida, vea [enviar mensajes mediante proveedores de almacenamiento de mensajes](sending-messages-by-using-message-store-providers.md).
  
## <a name="see-also"></a>Ver también



[Tablas MAPI](mapi-tables.md)

