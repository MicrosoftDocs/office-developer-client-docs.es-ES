---
title: Abrir un descriptor de vista
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1940feb0-9e0f-4d96-9fb9-b9a35a0aa661
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ce53e5a91f6fa340728872457eae7f6514e287aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413041"
---
# <a name="opening-a-view-descriptor"></a><span data-ttu-id="762e4-103">Abrir un descriptor de vista</span><span class="sxs-lookup"><span data-stu-id="762e4-103">Opening a view descriptor</span></span>
  
<span data-ttu-id="762e4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="762e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="762e4-105">Muchas carpetas se pueden abrir con una vista normal, una vista predeterminada o cualquier número de vistas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="762e4-105">Many folders can be opened with a normal view, a default view, or any number of personalized views.</span></span> <span data-ttu-id="762e4-106">Una vista describe cómo mostrar el contenido de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="762e4-106">A view describes how to display the contents of a folder.</span></span> <span data-ttu-id="762e4-107">La vista normal se usa cuando no hay ninguna vista alternativa y cuando se abre la carpeta por primera vez.</span><span class="sxs-lookup"><span data-stu-id="762e4-107">The normal view is used when there is no alternative view and when you are opening the folder for the first time.</span></span> <span data-ttu-id="762e4-108">Cuando existe una vista alternativa, debe usarla para abrir la carpeta.</span><span class="sxs-lookup"><span data-stu-id="762e4-108">When an alternative view does exist, you must use it to open the folder.</span></span>
  
<span data-ttu-id="762e4-109">Una vista se describe en un mensaje conocido como descriptor de vista.</span><span class="sxs-lookup"><span data-stu-id="762e4-109">A view is described in a message known as a view descriptor.</span></span> <span data-ttu-id="762e4-110">Los descriptores de vista normalmente se crean como mensajes asociados y pueden aparecer en las carpetas de vista comunes o personales o en cualquier carpeta IPM.</span><span class="sxs-lookup"><span data-stu-id="762e4-110">View descriptors are typically created as associated messages and can appear in either the common or personal view folders or in any IPM folder.</span></span>
  
### <a name="to-open-a-view-descriptor"></a><span data-ttu-id="762e4-111">Para abrir un descriptor de vista</span><span class="sxs-lookup"><span data-stu-id="762e4-111">To open a view descriptor</span></span>
  
1. <span data-ttu-id="762e4-112">Llama [a IMAPIContainer::GetContentsTable para](imapicontainer-getcontentstable.md) recuperar la tabla de contenido asociada para la carpeta.</span><span class="sxs-lookup"><span data-stu-id="762e4-112">Call [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) to retrieve the associated contents table for the folder.</span></span> 
    
2. <span data-ttu-id="762e4-113">Cree una restricción que busque solo mensajes con la clase de mensaje reservada para descriptores de vista y llame a [IMAPITable::Restrict](imapitable-restrict.md) para limitar la tabla y [IMAPITable::QueryRows](imapitable-queryrows.md) para recuperar las filas adecuadas o...</span><span class="sxs-lookup"><span data-stu-id="762e4-113">Create a restriction that locates only messages with the message class reserved for view descriptors and call [IMAPITable::Restrict](imapitable-restrict.md) to limit the table and [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the appropriate rows, or...</span></span>
    
   <span data-ttu-id="762e4-114">Llame al método [IMAPIProp::GetProps](imapiprop-getprops.md) de la carpeta para recuperar su **propiedad PR_DEFAULT_VIEW_ENTRYID** ([PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="762e4-114">Call the folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_DEFAULT_VIEW_ENTRYID** ([PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="762e4-115">**PR_DEFAULT_VIEW_ENTRYID** contiene el identificador de entrada del mensaje que contiene el descriptor de vista predeterminado para una carpeta.</span><span class="sxs-lookup"><span data-stu-id="762e4-115">**PR_DEFAULT_VIEW_ENTRYID** contains the entry identifier for the message containing the default view descriptor for a folder.</span></span> <span data-ttu-id="762e4-116">Esta llamada se realizará correctamente si la carpeta admite el uso de la marca MAPI_ASSOCIATED en las llamadas a [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) e [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).</span><span class="sxs-lookup"><span data-stu-id="762e4-116">This call will succeed if the folder supports the use of the MAPI_ASSOCIATED flag on calls to [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) and [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).</span></span>
    
3. <span data-ttu-id="762e4-117">Llama [a IMsgStore::OpenEntry con](imsgstore-openentry.md) el identificador de entrada del descriptor de vista para abrirlo.</span><span class="sxs-lookup"><span data-stu-id="762e4-117">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with the entry identifier of the view descriptor to open it.</span></span> 
    

