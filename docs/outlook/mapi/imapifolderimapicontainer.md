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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 64a64029c3507d9ac4b520076a44e23170dd9bd4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817262"
---
# <a name="imapifolder--imapicontainer"></a>IMAPIFolder: IMAPIContainer

  
  
**Se aplica a**: Outlook 
  
Realiza operaciones en los mensajes y subcarpetas en una carpeta.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Expuestos por:  <br/> |Objetos de carpeta  <br/> |
|Se implementa mediante:  <br/> |Proveedores de almacén de mensajes  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y MAPI  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIFolder  <br/> |
|Tipo de puntero:  <br/> |LPMAPIFOLDER  <br/> |
|Modelo de transacciones:  <br/> |Nontransacted  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[CreateMessage](imapifolder-createmessage.md) <br/> |Crea un nuevo mensaje.  <br/> |
|[CopyMessages](imapifolder-copymessages.md) <br/> |Copia o mueve uno o más mensajes.  <br/> |
|[DeleteMessages](imapifolder-deletemessages.md) <br/> |Elimina uno o más mensajes.  <br/> |
|[CreateFolder](imapifolder-createfolder.md) <br/> |Crea una nueva subcarpeta.  <br/> |
|[CopyFolder](imapifolder-copyfolder.md) <br/> |Copia o mueve una subcarpeta.  <br/> |
|[DeleteFolder](imapifolder-deletefolder.md) <br/> |Elimina una subcarpeta.  <br/> |
|[SetReadFlags](imapifolder-setreadflags.md) <br/> |Establece o borra el indicador MSGFLAG_READ en la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) de uno o varios de los mensajes de la carpeta y administra el envío de informes de lectura.  <br/> |
|[GetMessageStatus](imapifolder-getmessagestatus.md) <br/> |Obtiene el estado asociado a un mensaje de una carpeta determinada.  <br/> |
|[SetMessageStatus](imapifolder-setmessagestatus.md) <br/> |Establece el estado asociado a un mensaje.  <br/> |
|[SaveContentsSort](imapifolder-savecontentssort.md) <br/> |Establece el criterio de ordenación predeterminado para la tabla de contenido de una carpeta.  <br/> |
|[EmptyFolder](imapifolder-emptyfolder.md) <br/> |Elimina todos los mensajes y subcarpetas de una carpeta sin eliminar la propia carpeta.  <br/> |
   
|**Propiedades necesarias**|**Access**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))  <br/> |Es de lectura y escritura.  <br/> |
|**Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))  <br/> |Es de lectura y escritura.  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |Solo lectura  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Solo lectura  <br/> |
   
## <a name="see-also"></a>Ver también



[Interfaces MAPI](mapi-interfaces.md)

