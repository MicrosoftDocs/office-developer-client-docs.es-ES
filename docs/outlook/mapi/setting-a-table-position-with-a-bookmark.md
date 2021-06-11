---
title: Establecer una posición de tabla con un marcador
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 56ab37f9-5aa6-4e9d-9dc8-b3d95aa19f35
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f0b041cecca92c0ced32631c67c72fcafdab2a16
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422463"
---
# <a name="setting-a-table-position-with-a-bookmark"></a><span data-ttu-id="2af27-103">Establecer una posición de tabla con un marcador</span><span class="sxs-lookup"><span data-stu-id="2af27-103">Setting a Table Position with a Bookmark</span></span>

  
  
<span data-ttu-id="2af27-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2af27-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2af27-105">Un marcador es un recurso que indica una ubicación determinada en una tabla.</span><span class="sxs-lookup"><span data-stu-id="2af27-105">A bookmark is a resource that indicates a particular location in a table.</span></span> <span data-ttu-id="2af27-106">Establecer un marcador permite volver a una posición más adelante, una característica que puede mejorar significativamente el rendimiento de las operaciones de tabla.</span><span class="sxs-lookup"><span data-stu-id="2af27-106">Setting a bookmark makes it possible to return to a position at a later time, a feature that can significantly improve the performance of table operations.</span></span> <span data-ttu-id="2af27-107">MAPI define tres marcadores estándar:</span><span class="sxs-lookup"><span data-stu-id="2af27-107">MAPI defines three standard bookmarks:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2af27-108">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="2af27-108">BOOKMARK_CURRENT</span></span>  <br/> |<span data-ttu-id="2af27-109">Apunta a la fila actual de una tabla.</span><span class="sxs-lookup"><span data-stu-id="2af27-109">Points to the current row in a table.</span></span>  <br/> |
|<span data-ttu-id="2af27-110">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="2af27-110">BOOKMARK_BEGINNING</span></span>  <br/> |<span data-ttu-id="2af27-111">Apunta a la primera fila de una tabla.</span><span class="sxs-lookup"><span data-stu-id="2af27-111">Points to the first row in a table.</span></span>  <br/> |
|<span data-ttu-id="2af27-112">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="2af27-112">BOOKMARK_END</span></span>  <br/> |<span data-ttu-id="2af27-113">Apunta a la última fila de una tabla.</span><span class="sxs-lookup"><span data-stu-id="2af27-113">Points to the last row in a table.</span></span>  <br/> |
   
<span data-ttu-id="2af27-114">Los implementadores de tablas son necesarios para admitir estos marcadores estándar y también pueden admitir otros.</span><span class="sxs-lookup"><span data-stu-id="2af27-114">Table implementers are required to support these standard bookmarks and can also support others.</span></span> <span data-ttu-id="2af27-115">Sin embargo, como los marcadores son recursos y los recursos son limitados, los usuarios de marcadores deben liberarlos tan pronto como sea posible.</span><span class="sxs-lookup"><span data-stu-id="2af27-115">However, because bookmarks are resources and resources are limited, bookmark users should free them as soon as possible.</span></span> 
  
 <span data-ttu-id="2af27-116">**Para establecer un marcador en la posición actual de la tabla**</span><span class="sxs-lookup"><span data-stu-id="2af27-116">**To set a bookmark at the current table position**</span></span>
  
- <span data-ttu-id="2af27-117">Llame [a IMAPITable::CreateBookmark](imapitable-createbookmark.md).</span><span class="sxs-lookup"><span data-stu-id="2af27-117">Call [IMAPITable::CreateBookmark](imapitable-createbookmark.md).</span></span> <span data-ttu-id="2af27-118">En ocasiones, no habrá suficiente memoria disponible para asignar el nuevo marcador, lo que hace que **CreateBookmark** devuelva el MAPI_E_UNABLE_TO_COMPLETE error.</span><span class="sxs-lookup"><span data-stu-id="2af27-118">Occasionally there will be insufficient memory available to allocate the new bookmark, causing **CreateBookmark** to return the MAPI_E_UNABLE_TO_COMPLETE error value.</span></span> 
    
 <span data-ttu-id="2af27-119">**Para liberar un marcador**</span><span class="sxs-lookup"><span data-stu-id="2af27-119">**To free a bookmark**</span></span>
  
- <span data-ttu-id="2af27-120">Llame [a IMAPITable::FreeBookmark](imapitable-freebookmark.md).</span><span class="sxs-lookup"><span data-stu-id="2af27-120">Call [IMAPITable::FreeBookmark](imapitable-freebookmark.md).</span></span>
    
 <span data-ttu-id="2af27-121">**Para mover el cursor a una posición marcada**</span><span class="sxs-lookup"><span data-stu-id="2af27-121">**To move the cursor to a bookmarked position**</span></span>
  
- <span data-ttu-id="2af27-122">Llame [a IMAPITable::SeekRow](imapitable-seekrow.md).</span><span class="sxs-lookup"><span data-stu-id="2af27-122">Call [IMAPITable::SeekRow](imapitable-seekrow.md).</span></span> <span data-ttu-id="2af27-123">**SeekRow** establece un nuevo valor para la BOOKMARK_CURRENT posición.</span><span class="sxs-lookup"><span data-stu-id="2af27-123">**SeekRow** establishes a new value for the BOOKMARK_CURRENT position.</span></span> <span data-ttu-id="2af27-124">**SeekRow** se puede usar, por ejemplo, para colocar una tabla de diez filas desde la posición actual o para empezar de nuevo al principio.</span><span class="sxs-lookup"><span data-stu-id="2af27-124">**SeekRow** can be used, for example, to position a table ten rows from the current position or to start over at the beginning.</span></span> <span data-ttu-id="2af27-125">Los clientes o proveedores de servicios pueden buscar el marcador actual, inicial o final de una tabla, o cualquier otra posición asociada a un marcador predefinido.</span><span class="sxs-lookup"><span data-stu-id="2af27-125">Clients or service providers can seek to the current, beginning, or end of a table, or any other position that is associated with a predefined bookmark.</span></span> <span data-ttu-id="2af27-126">Pueden moverse en una dirección hacia delante o hacia atrás y limitar la operación a un número especificado de filas.</span><span class="sxs-lookup"><span data-stu-id="2af27-126">They can move in either a forward or backward direction and limit the operation to a specified number of rows.</span></span> <span data-ttu-id="2af27-127">Como regla general, los autores de llamadas deben buscar a través de no más de 50 filas con **SeekRow**; [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) debe usarse con un número mayor de filas.</span><span class="sxs-lookup"><span data-stu-id="2af27-127">As a rule, callers should seek through no more than 50 rows with **SeekRow**; [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) should be used with larger numbers of rows.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="2af27-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="2af27-128">See also</span></span>



[<span data-ttu-id="2af27-129">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="2af27-129">MAPI Tables</span></span>](mapi-tables.md)

