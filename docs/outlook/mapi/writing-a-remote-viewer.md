---
title: Escribir un visor remoto
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f4d7d42f-688a-4199-b972-dd42528c0cdf
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0125bd57f0f2958c112fb03e7bf4166a7017cd03
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584768"
---
# <a name="writing-a-remote-viewer"></a>Escribir un visor remoto

**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Un visor remoto es una ventana en una aplicación cliente que proporciona acceso controlado a los mensajes almacenados en otro equipo. Este acceso controlado puede funcionar en un vínculo de comunicaciones lento. En lugar de recuperar una selección completa de mensajes disponibles cada vez que un usuario abre una carpeta, el visor remoto primero muestra sólo los encabezados. A continuación, selecciona el usuario de los encabezados de cuál de los mensajes para mostrar en su totalidad. Los clientes de visor remoto pueden permitir que sus usuarios eliminar los mensajes antes de que nunca se descargan. 
  
## <a name="to-retrieve-the-headers-of-messages-stored-remotely"></a>Para recuperar los encabezados de los mensajes almacenados de forma remota
  
1. Llame a [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para obtener acceso a la tabla de estado. 
    
2. Llamar a [IMAPITable:: Restrict](imapitable-restrict.md) para limitar la tabla de estado a sólo las filas que tienen sus **PR\_recursos\_tipo** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) columna establecida en MAPI\_transporte\_proveedor. 
    
3. Llame a [IMAPITable::SetColumns](imapitable-setcolumns.md) para incluir las siguientes columnas en la tabla de estado: 
   - **Precio:\_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
   - **Precio:\_recursos\_métodos** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))
   - **Precio:\_recursos\_tipo**, **PR\_proveedor\_para mostrar** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
   - **Precio:\_estado\_código** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)).
    
4. Llame a [HrQueryAllRows](hrqueryallrows.md) para recuperar todas las filas de la tabla de estado. 
    
5. Pase el identificador de entrada para cada fila de la tabla en una llamada a [IMAPISession::OpenEntry](imapisession-openentry.md). Debido a que esta interfaz se calculan las referencias de contexto del proceso de la cola MAPI al contexto de proceso del cliente, a diferencia de las interfaces que normalmente se obtienen de la libreta de direcciones o un mensaje los proveedores de almacén: problemas con respecto a multithreading son de mayor importancia. 
    
6. Llamar al método [IUnknown:: QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d.aspx) del objeto de estado, pasando IID_IMAPIFolder como el identificador de interfaz, para recuperar la carpeta remota. La carpeta remota no es una implementación completa de la carpeta; admite solo un subconjunto de las propiedades y métodos de carpeta. Uno de los métodos necesarios, [IMAPIProp::GetProps](imapiprop-getprops.md), admite la recuperación de las siguientes propiedades:
    
    |||
    |:-----|:-----|
    |**Precio:\_acceso** ([PidTagAccess](pidtagaccess-canonical-property.md))  <br/> |**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))  <br/> |
    |**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> |**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))  <br/> |
    |**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |
    |**Precio:\_las SUBCARPETAS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))  <br/> |**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |
    |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |
    
    Carpetas remotas también deben admitir los métodos [IMAPIProp::GetPropList](imapiprop-getproplist.md), [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)y [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) . Normalmente, las tablas de contenido de carpeta remota admiten las siguientes columnas: 
        
    |||
    |:-----|:-----|
    |**Precio:\_para mostrar\_para** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |**Precio:\_ENTRYID** <br/> |
    |**Precio:\_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))  <br/> |**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))  <br/> |
    |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |
    |**Precio:\_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
    |**Precio:\_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |
    |**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** <br/> |
    |**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
    |**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))  <br/> |
    |**Precio:\_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
   
7. Hora en el primer método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) del proveedor de transporte que se selecciona una de las opciones de transferencia de llamadas. Debe establecerse el REFRESH_XP_HEADER_CACHE o la PROCESS_XP_HEADER_CACHE indicador de proceso, así como la marca SHOW_XP_SSESSION_UI para permitir que la interfaz de usuario para que se muestren. 
    
   > [!NOTE]
   > Para marcar un encabezado de mensaje en particular para descargar o eliminación, un cliente llama a [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) y establece la marca de la MSGSTATUS_REMOTE_DOWNLOAD o MSGSTATUS_REMOTE_DELETE. 
  

