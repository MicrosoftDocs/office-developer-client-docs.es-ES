---
title: Tablas de información asociada a la carpeta
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b72a0d36-c489-41d6-af57-72fbf4b7a3f5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 09cac591aac9d266571348531e378974b86a3a9d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816842"
---
# <a name="folder-associated-information-tables"></a><span data-ttu-id="153e6-103">Tablas de información asociada a la carpeta</span><span class="sxs-lookup"><span data-stu-id="153e6-103">Folder-Associated Information Tables</span></span>

  
  
<span data-ttu-id="153e6-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="153e6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="153e6-105">MAPI define el indicador MAPI_ASSOCIATED para diversos componentes MAPI usar cuando trabaja con tablas de información asociada.</span><span class="sxs-lookup"><span data-stu-id="153e6-105">MAPI defines the MAPI_ASSOCIATED flag for various MAPI components to use when dealing with associated information tables.</span></span> <span data-ttu-id="153e6-106">Cada carpeta en un almacén de mensajes debe tener una tabla de contenido asociada junto con su tabla de contenido estándar.</span><span class="sxs-lookup"><span data-stu-id="153e6-106">Each folder in a message store should have an associated contents table along with its standard contents table.</span></span> <span data-ttu-id="153e6-107">Las aplicaciones cliente almacenan mensajes especiales en tabla de contenido asociada de una carpeta para contener los formularios y vistas.</span><span class="sxs-lookup"><span data-stu-id="153e6-107">Client applications store special messages in a folder's associated contents table to hold forms and views.</span></span> <span data-ttu-id="153e6-108">De hecho, para admitir los formularios y vistas, el proveedor de almacén de mensajes debe implementar las tablas de contenido asociada.</span><span class="sxs-lookup"><span data-stu-id="153e6-108">In fact, to support forms and views, your message store provider must implement associated contents tables.</span></span>
  
<span data-ttu-id="153e6-109">Para implementar las tablas de contenido asociado, su proveedor de almacenamiento debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="153e6-109">To implement associated contents tables, your store provider must do the following:</span></span>
  
- <span data-ttu-id="153e6-110">Admite el indicador MAPI_ASSOCIATED en el método [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) por lo que las aplicaciones cliente pueden obtener la tabla de contenido asociados de la carpeta en lugar de la tabla de contenido estándar.</span><span class="sxs-lookup"><span data-stu-id="153e6-110">Support the MAPI_ASSOCIATED flag in the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method so client applications can get the folder's associated contents table instead of the standard contents table.</span></span> 
    
- <span data-ttu-id="153e6-111">Admite el indicador MAPI_ASSOCIATED en el método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) para que aplicaciones cliente pueden agregar los mensajes a la tabla de contenido asociada de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="153e6-111">Support the MAPI_ASSOCIATED flag in the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method so client applications can add messages to a folder's associated contents table.</span></span> 
    
- <span data-ttu-id="153e6-112">Establecer el bit MAPI_ACCESS_CREATE_ASSOCIATED en la propiedad **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) de objetos de carpeta.</span><span class="sxs-lookup"><span data-stu-id="153e6-112">Set the MAPI_ACCESS_CREATE_ASSOCIATED bit in the **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) property on folder objects.</span></span>
    
- <span data-ttu-id="153e6-113">Admite el indicador DEL_ASSOCIATED en el método [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="153e6-113">Support the DEL_ASSOCIATED flag in the [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md) method.</span></span> 
    
- <span data-ttu-id="153e6-114">Establecer el MSGFLAG_ASSOCIATED de bit en la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) para los mensajes en la tabla de contenido asociada.</span><span class="sxs-lookup"><span data-stu-id="153e6-114">Set the MSGFLAG_ASSOCIATED bit in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property for messages in the associated contents table.</span></span>
    
- <span data-ttu-id="153e6-115">Exponer y responder a la propiedad **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) en las carpetas.</span><span class="sxs-lookup"><span data-stu-id="153e6-115">Expose and respond to the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property on folders.</span></span>
    
- <span data-ttu-id="153e6-116">Mantener la propiedad **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) en las carpetas.</span><span class="sxs-lookup"><span data-stu-id="153e6-116">Maintain the **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) property on folders.</span></span>
    
<span data-ttu-id="153e6-117">No hay ningún bit en la propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) para indicar si el proveedor de almacén de mensajes es compatible con las tablas de contenido asociada.</span><span class="sxs-lookup"><span data-stu-id="153e6-117">There is no bit in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property to indicate whether your message store provider supports associated contents tables.</span></span> <span data-ttu-id="153e6-118">Si su proveedor de almacén de mensajes no es compatible con ellos, debe devolver MAPI_E_NO_SUPPORT cuando llama a aplicaciones cliente de cualquiera de los métodos anteriores con la marca MAPI_ASSOCIATED.</span><span class="sxs-lookup"><span data-stu-id="153e6-118">If your message store provider does not support them, it should return MAPI_E_NO_SUPPORT when client applications call any of the above methods with the MAPI_ASSOCIATED flag.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="153e6-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="153e6-119">See also</span></span>



[<span data-ttu-id="153e6-120">Caracter�sticas de almac�n de mensajes</span><span class="sxs-lookup"><span data-stu-id="153e6-120">Message Store Features</span></span>](message-store-features.md)

