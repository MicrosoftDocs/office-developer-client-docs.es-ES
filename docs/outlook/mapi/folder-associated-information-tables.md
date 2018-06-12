---
title: Tablas de información asociada a la carpeta
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b72a0d36-c489-41d6-af57-72fbf4b7a3f5
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 09cac591aac9d266571348531e378974b86a3a9d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816842"
---
# <a name="folder-associated-information-tables"></a>Tablas de información asociada a la carpeta

  
  
**Se aplica a**: Outlook 
  
MAPI define el indicador MAPI_ASSOCIATED para diversos componentes MAPI usar cuando trabaja con tablas de información asociada. Cada carpeta en un almacén de mensajes debe tener una tabla de contenido asociada junto con su tabla de contenido estándar. Las aplicaciones cliente almacenan mensajes especiales en tabla de contenido asociada de una carpeta para contener los formularios y vistas. De hecho, para admitir los formularios y vistas, el proveedor de almacén de mensajes debe implementar las tablas de contenido asociada.
  
Para implementar las tablas de contenido asociado, su proveedor de almacenamiento debe hacer lo siguiente:
  
- Admite el indicador MAPI_ASSOCIATED en el método [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) por lo que las aplicaciones cliente pueden obtener la tabla de contenido asociados de la carpeta en lugar de la tabla de contenido estándar. 
    
- Admite el indicador MAPI_ASSOCIATED en el método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) para que aplicaciones cliente pueden agregar los mensajes a la tabla de contenido asociada de una carpeta. 
    
- Establecer el bit MAPI_ACCESS_CREATE_ASSOCIATED en la propiedad **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) de objetos de carpeta.
    
- Admite el indicador DEL_ASSOCIATED en el método [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md) . 
    
- Establecer el MSGFLAG_ASSOCIATED de bit en la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) para los mensajes en la tabla de contenido asociada.
    
- Exponer y responder a la propiedad **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) en las carpetas.
    
- Mantener la propiedad **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) en las carpetas.
    
No hay ningún bit en la propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) para indicar si el proveedor de almacén de mensajes es compatible con las tablas de contenido asociada. Si su proveedor de almacén de mensajes no es compatible con ellos, debe devolver MAPI_E_NO_SUPPORT cuando llama a aplicaciones cliente de cualquiera de los métodos anteriores con la marca MAPI_ASSOCIATED.
  
## <a name="see-also"></a>Ver también



[Caracter�sticas de almac�n de mensajes](message-store-features.md)

