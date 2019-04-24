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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351236"
---
# <a name="setting-a-table-position-with-a-bookmark"></a><span data-ttu-id="8eeb9-103">Establecer una posición de tabla con un marcador</span><span class="sxs-lookup"><span data-stu-id="8eeb9-103">Setting a Table Position with a Bookmark</span></span>

  
  
<span data-ttu-id="8eeb9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8eeb9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8eeb9-105">Un marcador es un recurso que indica una ubicación determinada de una tabla.</span><span class="sxs-lookup"><span data-stu-id="8eeb9-105">A bookmark is a resource that indicates a particular location in a table.</span></span> <span data-ttu-id="8eeb9-106">Establecer un marcador permite volver a una posición posterior, una característica que puede mejorar significativamente el rendimiento de las operaciones de tabla.</span><span class="sxs-lookup"><span data-stu-id="8eeb9-106">Setting a bookmark makes it possible to return to a position at a later time, a feature that can significantly improve the performance of table operations.</span></span> <span data-ttu-id="8eeb9-107">MAPI define tres marcadores estándar:</span><span class="sxs-lookup"><span data-stu-id="8eeb9-107">MAPI defines three standard bookmarks:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8eeb9-108">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="8eeb9-108">BOOKMARK_CURRENT</span></span>  <br/> |<span data-ttu-id="8eeb9-109">Apunta a la fila actual de una tabla.</span><span class="sxs-lookup"><span data-stu-id="8eeb9-109">Points to the current row in a table.</span></span>  <br/> |
|<span data-ttu-id="8eeb9-110">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="8eeb9-110">BOOKMARK_BEGINNING</span></span>  <br/> |<span data-ttu-id="8eeb9-111">Apunta a la primera fila de una tabla.</span><span class="sxs-lookup"><span data-stu-id="8eeb9-111">Points to the first row in a table.</span></span>  <br/> |
|<span data-ttu-id="8eeb9-112">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="8eeb9-112">BOOKMARK_END</span></span>  <br/> |<span data-ttu-id="8eeb9-113">Apunta a la última fila de una tabla.</span><span class="sxs-lookup"><span data-stu-id="8eeb9-113">Points to the last row in a table.</span></span>  <br/> |
   
<span data-ttu-id="8eeb9-114">Los implementadores de tablas son necesarios para admitir estos marcadores estándar y también pueden admitir otros.</span><span class="sxs-lookup"><span data-stu-id="8eeb9-114">Table implementers are required to support these standard bookmarks and can also support others.</span></span> <span data-ttu-id="8eeb9-115">Sin embargo, dado que los marcadores son recursos y los recursos son limitados, los usuarios de marcadores deben liberarlos tan pronto como sea posible.</span><span class="sxs-lookup"><span data-stu-id="8eeb9-115">However, because bookmarks are resources and resources are limited, bookmark users should free them as soon as possible.</span></span> 
  
 <span data-ttu-id="8eeb9-116">**Para establecer un marcador en la posición de la tabla actual**</span><span class="sxs-lookup"><span data-stu-id="8eeb9-116">**To set a bookmark at the current table position**</span></span>
  
- <span data-ttu-id="8eeb9-117">Llame al [IMAPITable:: CreateBookmark](imapitable-createbookmark.md).</span><span class="sxs-lookup"><span data-stu-id="8eeb9-117">Call [IMAPITable::CreateBookmark](imapitable-createbookmark.md).</span></span> <span data-ttu-id="8eeb9-118">De vez en cuando no habrá suficiente memoria disponible para asignar el nuevo marcador, lo que hará que **CreateBookmark** devuelva el valor de error MAPI_E_UNABLE_TO_COMPLETE.</span><span class="sxs-lookup"><span data-stu-id="8eeb9-118">Occasionally there will be insufficient memory available to allocate the new bookmark, causing **CreateBookmark** to return the MAPI_E_UNABLE_TO_COMPLETE error value.</span></span> 
    
 <span data-ttu-id="8eeb9-119">**Para liberar un marcador**</span><span class="sxs-lookup"><span data-stu-id="8eeb9-119">**To free a bookmark**</span></span>
  
- <span data-ttu-id="8eeb9-120">Llame al [IMAPITable:: FreeBookmark](imapitable-freebookmark.md).</span><span class="sxs-lookup"><span data-stu-id="8eeb9-120">Call [IMAPITable::FreeBookmark](imapitable-freebookmark.md).</span></span>
    
 <span data-ttu-id="8eeb9-121">**Para mover el cursor a una posición con marcador**</span><span class="sxs-lookup"><span data-stu-id="8eeb9-121">**To move the cursor to a bookmarked position**</span></span>
  
- <span data-ttu-id="8eeb9-122">Llame al [IMAPITable:: SeekRow](imapitable-seekrow.md).</span><span class="sxs-lookup"><span data-stu-id="8eeb9-122">Call [IMAPITable::SeekRow](imapitable-seekrow.md).</span></span> <span data-ttu-id="8eeb9-123">**SeekRow** establece un nuevo valor para la posición BOOKMARK_CURRENT.</span><span class="sxs-lookup"><span data-stu-id="8eeb9-123">**SeekRow** establishes a new value for the BOOKMARK_CURRENT position.</span></span> <span data-ttu-id="8eeb9-124">**SeekRow** puede usarse, por ejemplo, para colocar una tabla diez filas a partir de la posición actual o para volver a empezar desde el principio.</span><span class="sxs-lookup"><span data-stu-id="8eeb9-124">**SeekRow** can be used, for example, to position a table ten rows from the current position or to start over at the beginning.</span></span> <span data-ttu-id="8eeb9-125">Los clientes o proveedores de servicios pueden buscar el actual, el principio o el final de una tabla, o cualquier otra posición asociada con un marcador predefinido.</span><span class="sxs-lookup"><span data-stu-id="8eeb9-125">Clients or service providers can seek to the current, beginning, or end of a table, or any other position that is associated with a predefined bookmark.</span></span> <span data-ttu-id="8eeb9-126">Se pueden mover en una dirección hacia delante o hacia atrás, y limitar la operación a un número especificado de filas.</span><span class="sxs-lookup"><span data-stu-id="8eeb9-126">They can move in either a forward or backward direction and limit the operation to a specified number of rows.</span></span> <span data-ttu-id="8eeb9-127">Como regla, los autores de la llamada deben buscar en más de 50 filas con **SeekRow**; El [IMAPITable:: SeekRowApprox](imapitable-seekrowapprox.md) debe usarse con un número mayor de filas.</span><span class="sxs-lookup"><span data-stu-id="8eeb9-127">As a rule, callers should seek through no more than 50 rows with **SeekRow**; [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) should be used with larger numbers of rows.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="8eeb9-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="8eeb9-128">See also</span></span>



[<span data-ttu-id="8eeb9-129">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="8eeb9-129">MAPI Tables</span></span>](mapi-tables.md)

