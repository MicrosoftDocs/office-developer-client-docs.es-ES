---
title: IMAPIFolder IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder
api_type:
- COM
ms.assetid: bc2e8d17-7687-43c2-8f01-b677703f7288
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5e31896354141999e02f2cba117ef9739340be61
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329494"
---
# <a name="imapifolder--imapicontainer"></a>IMAPIFolder : IMAPIContainer

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Realiza operaciones en los mensajes y subcarpetas de una carpeta.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
|Expuesto por:  <br/> |Objetos Folder  <br/> |
|Implementado por:  <br/> |Proveedores de almacenamiento de mensajes  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y MAPI  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIFolder  <br/> |
|Tipo de puntero:  <br/> |LPMAPIFOLDER  <br/> |
|Modelo de transacción:  <br/> |No transactd  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[CreateMessage](imapifolder-createmessage.md) <br/> |Crea un nuevo mensaje.  <br/> |
|[CopyMessages](imapifolder-copymessages.md) <br/> |Copia o mueve uno o más mensajes.  <br/> |
|[DeleteMessages](imapifolder-deletemessages.md) <br/> |Elimina uno o más mensajes.  <br/> |
|[CreateFolder](imapifolder-createfolder.md) <br/> |Crea una subcarpeta nueva.  <br/> |
|[CopyFolder](imapifolder-copyfolder.md) <br/> |Copia o mueve una subcarpeta.  <br/> |
|[DeleteFolder](imapifolder-deletefolder.md) <br/> |Elimina una subcarpeta.  <br/> |
|[SetReadFlags](imapifolder-setreadflags.md) <br/> |Establece o borra la marca MSGFLAG_READ en la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) de uno o más de los mensajes de la carpeta y administra el envío de informes de lectura.  <br/> |
|[GetMessageStatus](imapifolder-getmessagestatus.md) <br/> |Obtiene el estado asociado a un mensaje en una carpeta concreta.  <br/> |
|[SetMessageStatus](imapifolder-setmessagestatus.md) <br/> |Establece el estado asociado a un mensaje.  <br/> |
|[SaveContentsSort](imapifolder-savecontentssort.md) <br/> |Establece el criterio de ordenación predeterminado para la tabla de contenido de una carpeta.  <br/> |
|[EmptyFolder](imapifolder-emptyfolder.md) <br/> |Elimina todos los mensajes y subcarpetas de una carpeta sin eliminar la carpeta en sí.  <br/> |
   
|**Propiedades requeridas**|**Access**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))  <br/> |Lectura y escritura  <br/> |
|**** Es ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))  <br/> |Lectura y escritura  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Solo lectura  <br/> |
   
## <a name="see-also"></a>Vea también



[Interfaces MAPI](mapi-interfaces.md)

