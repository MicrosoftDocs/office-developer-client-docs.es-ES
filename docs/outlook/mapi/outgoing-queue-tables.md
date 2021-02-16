---
title: Tablas de cola salientes
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
# <a name="outgoing-queue-tables"></a>Tablas de cola salientes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una tabla de cola saliente contiene información sobre todos los mensajes salientes de un almacén de mensajes. Los proveedores de almacenamiento de mensajes implementan tablas de cola salientes para que la cola MAPI la use. Los almacenes que no admiten el envío o la recepción de mensajes no necesitan implementar esta tabla. 
  
Para obtener acceso a una tabla de cola saliente, la cola MAPI llama al método [IMsgStore::GetOutgoingQueue.](imsgstore-getoutgoingqueue.md) 
  
Es necesario que los mensajes se preprocesan y envíen al proveedor de transporte en el mismo orden en que los envió la aplicación cliente. La cola MAPI está diseñada para aceptar mensajes del almacén de mensajes en orden ascendente del tiempo de envío. Debido a este requisito, puede haber algún retraso antes de que algunos mensajes aparezcan en la tabla de cola saliente. 
  
Los almacenes de mensajes deben permitir la ordenación en la tabla de cola saliente para que la cola MAPI pueda ordenar los mensajes por hora de envío o el criterio de ordenación predeterminado debe ser por tiempo de envío ascendente. 
  
La tabla de colas salientes debe enviar notificaciones cuando cambia el contenido de la cola.
  
Las siguientes propiedades son la columna necesaria establecida en las tablas de cola salientes:
  
|||
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
|**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))  <br/> | <br/> |
   
Para obtener más información acerca de cómo se usa la tabla de colas salientes, vea [Enviar mensajes mediante proveedores de almacén de mensajes.](sending-messages-by-using-message-store-providers.md)
  
## <a name="see-also"></a>Consulte también



[Tablas MAPI](mapi-tables.md)

