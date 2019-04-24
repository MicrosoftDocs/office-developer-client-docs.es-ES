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
ms.openlocfilehash: 1d7fea7f92a315b9671d17c82a82d5d7d180f4bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325665"
---
# <a name="writing-a-remote-viewer"></a>Escribir un visor remoto

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un visor remoto es una ventana de una aplicación cliente que proporciona acceso controlado a los mensajes almacenados en otro equipo. Este acceso controlado puede funcionar en un vínculo de comunicaciones lentas. En lugar de recuperar una selección completa de los mensajes disponibles cada vez que un usuario abre una carpeta, el visor remoto muestra primero sólo los encabezados. A continuación, el usuario selecciona de los encabezados los mensajes para mostrar en su totalidad. Los clientes del visor remoto pueden permitir que los usuarios eliminen mensajes antes de que se descarguen. 
  
## <a name="to-retrieve-the-headers-of-messages-stored-remotely"></a>Para recuperar los encabezados de los mensajes almacenados de forma remota
  
1. Llame a [IMAPISession:: GetStatusTable](imapisession-getstatustable.md) para obtener acceso a la tabla de estado. 
    
2. Llame [al IMAPITable:: Restrict](imapitable-restrict.md) para limitar la tabla de estado a solo aquellas filas que tienen la columna **tipo de\_recurso\_RP** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))\_establecida\_en el proveedor de transporte MAPI. 
    
3. Llame al [IMAPITable:: SetColumns](imapitable-setcolumns.md) para incluir las siguientes columnas en la tabla de estado: 
   - **EntryID\_de PR** ([PidTagEntryId](pidtagentryid-canonical-property.md))
   - **Métodos\_de\_recursos de PR** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))
   - **Tipo\_de\_recurso PR**, **presentación del\_\_proveedor de PR** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
   - **Código\_de\_estado de PR** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)).
    
4. Llame a [HrQueryAllRows](hrqueryallrows.md) para recuperar todas las filas de la tabla de estado. 
    
5. Pase el identificador de entrada para cada fila de la tabla en una llamada a [IMAPISession:: OpenEntry](imapisession-openentry.md). Debido a que se calculan las referencias de esta interfaz desde el contexto del proceso del administrador de trabajos de la cola MAPI hasta el contexto del proceso del cliente (a diferencia de las interfaces que normalmente se obtienen de la libreta de direcciones o los proveedores de almacenamiento de mensajes), los problemas relacionados con el subprocesamiento 
    
6. Llame al método [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d.aspx) del objeto status, pasando IID_IMAPIFolder como identificador de interfaz, para recuperar la carpeta remota. La carpeta remota no es una implementación completa de la carpeta; admite sólo un subconjunto de propiedades y métodos de carpeta. Uno de los métodos obligatorios, [IMAPIProp:: GetProps](imapiprop-getprops.md), admite la recuperación de las siguientes propiedades:
    
    |||
    |:-----|:-----|
    |**Acceso\_de PR** ([PidTagAccess](pidtagaccess-canonical-property.md))  <br/> |**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))  <br/> |
    |**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> |**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))  <br/> |
    |**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |
    |**SubCARPETAs PR\_** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))  <br/> |**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |
    |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |
    
    Las carpetas remotas también deben admitir los métodos [IMAPIProp:: GetPropList](imapiprop-getproplist.md), [IMAPIContainer:: GetContentsTable](imapicontainer-getcontentstable.md)y [IMAPIFolder:: SetMessageStatus](imapifolder-setmessagestatus.md) . Las tablas de contenido de carpetas remotas suelen ser compatibles con las siguientes columnas: 
        
    |||
    |:-----|:-----|
    |**\_Mostrar\_PR a** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |**EntryID\_de PR** <br/> |
    |**PR\_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))  <br/> |**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))  <br/> |
    |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |
    |**PR\_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
    |**PR\_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |
    |**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** <br/> |
    |**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
    |**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))  <br/> |
    |**PR\_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
   
7. Llame al método [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) del proveedor de transporte la primera vez que se selecciona una de las opciones de transferencia. Se debe establecer la marca de proceso REFRESH_XP_HEADER_CACHE o PROCESS_XP_HEADER_CACHE, así como la marca SHOW_XP_SSESSION_UI para permitir que se muestre la interfaz de usuario. 
    
   > [!NOTE]
   > Para marcar un encabezado de mensaje determinado para la descarga o la eliminación, un cliente llama a [IMAPIFolder:: SetMessageStatus](imapifolder-setmessagestatus.md) y establece la marca MSGSTATUS_REMOTE_DOWNLOAD o MSGSTATUS_REMOTE_DELETE. 
  

