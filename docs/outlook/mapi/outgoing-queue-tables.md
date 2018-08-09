---
title: Tablas de cola saliente
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 070377ca-ba9e-42ef-ac6b-ff7548b5ccf5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 10890c1fe430ddbc45c16908df3ac340284c9f18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818452"
---
# <a name="outgoing-queue-tables"></a>Tablas de cola saliente

  
  
**Hace referencia a**: Outlook 
  
Una tabla de cola saliente contiene información sobre todos los mensajes salientes para un almacén de mensajes. Los proveedores de almacén de mensajes implementan tablas de cola saliente para la cola MAPI usar. Almacenes que no admiten el envío o recepción de mensajes, no necesita implementar esta tabla. 
  
Para obtener acceso a una tabla de cola saliente, la cola MAPI llama al método de [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) . 
  
Hay un requisito que los mensajes se preprocesan y se envía al proveedor de transporte en el mismo orden tal y como se enviaron por la aplicación cliente. La cola MAPI está diseñada para aceptar los mensajes desde el almacén de mensajes en orden ascendente de tiempo de envío. Debido a este requisito, puede haber algunas retraso antes de que algunos mensajes aparecen en la tabla cola saliente. 
  
Almacenes de mensaje ya sea deben permitir que la ordenación en la tabla cola saliente de modo que la cola MAPI puede ordenar los mensajes por hora de envío, o el criterio de ordenación predeterminado debería estar por orden ascendente de tiempo de envío. 
  
En la tabla cola saliente debe enviar notificaciones cuando cambia el contenido de la cola.
  
Las siguientes propiedades que conforman la columna requiere establecer en las tablas de cola saliente:
  
|||
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |**PR_DISPLAY_TO de MAPI** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |
|**Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
|**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))  <br/> | <br/> |
   
Para obtener más información acerca de cómo se usa la tabla de cola saliente, vea [Enviar mensajes mediante el uso de los proveedores de almacén de mensajes](sending-messages-by-using-message-store-providers.md).
  
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

