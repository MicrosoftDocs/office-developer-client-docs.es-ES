---
title: Abrir un descriptor de vista
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1940feb0-9e0f-4d96-9fb9-b9a35a0aa661
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 525c817cfc3bdcf96455d35025e85486ec8b5b42
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818436"
---
# <a name="opening-a-view-descriptor"></a><span data-ttu-id="aae7d-103">Abrir un descriptor de vista</span><span class="sxs-lookup"><span data-stu-id="aae7d-103">Opening a view descriptor</span></span>
  
<span data-ttu-id="aae7d-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aae7d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aae7d-105">Muchas carpetas se pueden abrir con una vista normal, una vista predeterminada o cualquier número de vistas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="aae7d-105">Many folders can be opened with a normal view, a default view, or any number of personalized views.</span></span> <span data-ttu-id="aae7d-106">Una vista describe cómo mostrar el contenido de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="aae7d-106">A view describes how to display the contents of a folder.</span></span> <span data-ttu-id="aae7d-107">Cuando no hay ninguna vista alternativa y cuando se está abriendo la carpeta por primera vez, se usa la vista normal.</span><span class="sxs-lookup"><span data-stu-id="aae7d-107">The normal view is used when there is no alternative view and when you are opening the folder for the first time.</span></span> <span data-ttu-id="aae7d-108">Cuando existe una vista alternativa, debe usar para abrir la carpeta.</span><span class="sxs-lookup"><span data-stu-id="aae7d-108">When an alternative view does exist, you must use it to open the folder.</span></span>
  
<span data-ttu-id="aae7d-109">Una vista se describe en un mensaje que se conoce como un descriptor de vista.</span><span class="sxs-lookup"><span data-stu-id="aae7d-109">A view is described in a message known as a view descriptor.</span></span> <span data-ttu-id="aae7d-110">Descriptores de vista se crean normalmente como mensajes asociados y pueden aparecer en las carpetas de la vista personal o común o en cualquier carpeta IPM.</span><span class="sxs-lookup"><span data-stu-id="aae7d-110">View descriptors are typically created as associated messages and can appear in either the common or personal view folders or in any IPM folder.</span></span>
  
### <a name="to-open-a-view-descriptor"></a><span data-ttu-id="aae7d-111">Para abrir un descriptor de vista</span><span class="sxs-lookup"><span data-stu-id="aae7d-111">To open a view descriptor</span></span>
  
1. <span data-ttu-id="aae7d-112">Llame a [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) para recuperar la tabla de contenido asociada para la carpeta.</span><span class="sxs-lookup"><span data-stu-id="aae7d-112">Call [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) to retrieve the associated contents table for the folder.</span></span> 
    
2. <span data-ttu-id="aae7d-113">Crear una restricción que localiza sólo los mensajes con la clase de mensaje que se reserva para los descriptores de vista y llamar a [IMAPITable:: Restrict](imapitable-restrict.md) para limitar la tabla y [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar las filas apropiadas, o...</span><span class="sxs-lookup"><span data-stu-id="aae7d-113">Create a restriction that locates only messages with the message class reserved for view descriptors and call [IMAPITable::Restrict](imapitable-restrict.md) to limit the table and [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the appropriate rows, or...</span></span>
    
   <span data-ttu-id="aae7d-114">Llamar al método [IMAPIProp::GetProps](imapiprop-getprops.md) de la carpeta para recuperar su propiedad **PR_DEFAULT_VIEW_ENTRYID** ([PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="aae7d-114">Call the folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_DEFAULT_VIEW_ENTRYID** ([PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="aae7d-115">**PR_DEFAULT_VIEW_ENTRYID** contiene el identificador de entrada para el mensaje que contiene el descriptor de la vista predeterminada de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="aae7d-115">**PR_DEFAULT_VIEW_ENTRYID** contains the entry identifier for the message containing the default view descriptor for a folder.</span></span> <span data-ttu-id="aae7d-116">Esta llamada funcionará correctamente si la carpeta admite el uso de la marca MAPI_ASSOCIATED en las llamadas a [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) y [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).</span><span class="sxs-lookup"><span data-stu-id="aae7d-116">This call will succeed if the folder supports the use of the MAPI_ASSOCIATED flag on calls to [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) and [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).</span></span>
    
3. <span data-ttu-id="aae7d-117">Llame al método [IMsgStore::OpenEntry](imsgstore-openentry.md) con el identificador de entrada del descriptor de vista para abrirlo.</span><span class="sxs-lookup"><span data-stu-id="aae7d-117">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with the entry identifier of the view descriptor to open it.</span></span> 
    

