---
title: Folder-Associated de información
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b72a0d36-c489-41d6-af57-72fbf4b7a3f5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2332c2a2f7eb46816eab5305b73344e25b2832d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426418"
---
# <a name="folder-associated-information-tables"></a>Folder-Associated de información

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI define la marca MAPI_ASSOCIATED para varios componentes MAPI que se deben usar al tratar con tablas de información asociadas. Cada carpeta de un almacén de mensajes debe tener una tabla de contenido asociada junto con su tabla de contenido estándar. Las aplicaciones cliente almacenan mensajes especiales en la tabla de contenido asociada de una carpeta para contener formularios y vistas. De hecho, para admitir formularios y vistas, el proveedor del almacén de mensajes debe implementar tablas de contenido asociadas.
  
Para implementar tablas de contenido asociadas, el proveedor de la tienda debe hacer lo siguiente:
  
- Admite la marca MAPI_ASSOCIATED en el método [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) para que las aplicaciones cliente puedan obtener la tabla de contenido asociada de la carpeta en lugar de la tabla de contenido estándar. 
    
- Admite la MAPI_ASSOCIATED en el método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) para que las aplicaciones cliente puedan agregar mensajes a la tabla de contenido asociada de una carpeta. 
    
- Establezca el bit MAPI_ACCESS_CREATE_ASSOCIATED en la **propiedad PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) en objetos de carpeta.
    
- Admite la DEL_ASSOCIATED en el [método IMAPIFolder::EmptyFolder.](imapifolder-emptyfolder.md) 
    
- Establezca el bit MSGFLAG_ASSOCIATED en la **propiedad PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) para los mensajes de la tabla de contenido asociada.
    
- Exponer y responder a la **propiedad PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) en las carpetas.
    
- Mantenga la **propiedad PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) en las carpetas.
    
No hay ningún bit en la **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) para indicar si el proveedor del almacén de mensajes admite tablas de contenido asociadas. Si el proveedor del almacén de mensajes no los admite, debe devolver MAPI_E_NO_SUPPORT cuando las aplicaciones cliente llamen a cualquiera de los métodos anteriores con la marca MAPI_ASSOCIATED mensaje.
  
## <a name="see-also"></a>Consulte también



[Caracter�sticas de almac�n de mensajes](message-store-features.md)

