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
# <a name="folder-associated-information-tables"></a><span data-ttu-id="60cda-103">Folder-Associated de información</span><span class="sxs-lookup"><span data-stu-id="60cda-103">Folder-Associated Information Tables</span></span>

  
  
<span data-ttu-id="60cda-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="60cda-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="60cda-105">MAPI define la marca MAPI_ASSOCIATED para varios componentes MAPI que se deben usar al tratar con tablas de información asociadas.</span><span class="sxs-lookup"><span data-stu-id="60cda-105">MAPI defines the MAPI_ASSOCIATED flag for various MAPI components to use when dealing with associated information tables.</span></span> <span data-ttu-id="60cda-106">Cada carpeta de un almacén de mensajes debe tener una tabla de contenido asociada junto con su tabla de contenido estándar.</span><span class="sxs-lookup"><span data-stu-id="60cda-106">Each folder in a message store should have an associated contents table along with its standard contents table.</span></span> <span data-ttu-id="60cda-107">Las aplicaciones cliente almacenan mensajes especiales en la tabla de contenido asociada de una carpeta para contener formularios y vistas.</span><span class="sxs-lookup"><span data-stu-id="60cda-107">Client applications store special messages in a folder's associated contents table to hold forms and views.</span></span> <span data-ttu-id="60cda-108">De hecho, para admitir formularios y vistas, el proveedor del almacén de mensajes debe implementar tablas de contenido asociadas.</span><span class="sxs-lookup"><span data-stu-id="60cda-108">In fact, to support forms and views, your message store provider must implement associated contents tables.</span></span>
  
<span data-ttu-id="60cda-109">Para implementar tablas de contenido asociadas, el proveedor de la tienda debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="60cda-109">To implement associated contents tables, your store provider must do the following:</span></span>
  
- <span data-ttu-id="60cda-110">Admite la marca MAPI_ASSOCIATED en el método [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) para que las aplicaciones cliente puedan obtener la tabla de contenido asociada de la carpeta en lugar de la tabla de contenido estándar.</span><span class="sxs-lookup"><span data-stu-id="60cda-110">Support the MAPI_ASSOCIATED flag in the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method so client applications can get the folder's associated contents table instead of the standard contents table.</span></span> 
    
- <span data-ttu-id="60cda-111">Admite la MAPI_ASSOCIATED en el método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) para que las aplicaciones cliente puedan agregar mensajes a la tabla de contenido asociada a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="60cda-111">Support the MAPI_ASSOCIATED flag in the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method so client applications can add messages to a folder's associated contents table.</span></span> 
    
- <span data-ttu-id="60cda-112">Establezca el MAPI_ACCESS_CREATE_ASSOCIATED en la **propiedad PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) en objetos de carpeta.</span><span class="sxs-lookup"><span data-stu-id="60cda-112">Set the MAPI_ACCESS_CREATE_ASSOCIATED bit in the **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) property on folder objects.</span></span>
    
- <span data-ttu-id="60cda-113">Admite la DEL_ASSOCIATED en el [método IMAPIFolder::EmptyFolder.](imapifolder-emptyfolder.md)</span><span class="sxs-lookup"><span data-stu-id="60cda-113">Support the DEL_ASSOCIATED flag in the [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md) method.</span></span> 
    
- <span data-ttu-id="60cda-114">Establezca el MSGFLAG_ASSOCIATED en la **propiedad PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) para los mensajes de la tabla de contenido asociada.</span><span class="sxs-lookup"><span data-stu-id="60cda-114">Set the MSGFLAG_ASSOCIATED bit in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property for messages in the associated contents table.</span></span>
    
- <span data-ttu-id="60cda-115">Exponer y responder a la **propiedad PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) en las carpetas.</span><span class="sxs-lookup"><span data-stu-id="60cda-115">Expose and respond to the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property on folders.</span></span>
    
- <span data-ttu-id="60cda-116">Mantenga la **propiedad PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) en las carpetas.</span><span class="sxs-lookup"><span data-stu-id="60cda-116">Maintain the **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) property on folders.</span></span>
    
<span data-ttu-id="60cda-117">No hay ningún bit en la **propiedad PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) para indicar si el proveedor del almacén de mensajes admite tablas de contenido asociadas.</span><span class="sxs-lookup"><span data-stu-id="60cda-117">There is no bit in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property to indicate whether your message store provider supports associated contents tables.</span></span> <span data-ttu-id="60cda-118">Si el proveedor del almacén de mensajes no los admite, debe devolver MAPI_E_NO_SUPPORT cuando las aplicaciones cliente llamen a cualquiera de los métodos anteriores con la MAPI_ASSOCIATED marca.</span><span class="sxs-lookup"><span data-stu-id="60cda-118">If your message store provider does not support them, it should return MAPI_E_NO_SUPPORT when client applications call any of the above methods with the MAPI_ASSOCIATED flag.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="60cda-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="60cda-119">See also</span></span>



[<span data-ttu-id="60cda-120">Caracter�sticas de almac�n de mensajes</span><span class="sxs-lookup"><span data-stu-id="60cda-120">Message Store Features</span></span>](message-store-features.md)

