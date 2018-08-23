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
ms.openlocfilehash: f43e3a7e3376cb437620204a29aed9fb732d3427
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564097"
---
# <a name="setting-a-table-position-with-a-bookmark"></a><span data-ttu-id="3ccd7-103">Establecer una posición de tabla con un marcador</span><span class="sxs-lookup"><span data-stu-id="3ccd7-103">Setting a Table Position with a Bookmark</span></span>

  
  
<span data-ttu-id="3ccd7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ccd7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ccd7-105">Un marcador es un recurso que indica una ubicación determinada en una tabla.</span><span class="sxs-lookup"><span data-stu-id="3ccd7-105">A bookmark is a resource that indicates a particular location in a table.</span></span> <span data-ttu-id="3ccd7-106">Establecer un marcador hace posible volver a una posición en un momento posterior, una característica que puede mejorar significativamente el rendimiento de las operaciones de la tabla.</span><span class="sxs-lookup"><span data-stu-id="3ccd7-106">Setting a bookmark makes it possible to return to a position at a later time, a feature that can significantly improve the performance of table operations.</span></span> <span data-ttu-id="3ccd7-107">MAPI define tres marcadores estándares:</span><span class="sxs-lookup"><span data-stu-id="3ccd7-107">MAPI defines three standard bookmarks:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3ccd7-108">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="3ccd7-108">BOOKMARK_CURRENT</span></span>  <br/> |<span data-ttu-id="3ccd7-109">Puntos a la fila actual de una tabla.</span><span class="sxs-lookup"><span data-stu-id="3ccd7-109">Points to the current row in a table.</span></span>  <br/> |
|<span data-ttu-id="3ccd7-110">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="3ccd7-110">BOOKMARK_BEGINNING</span></span>  <br/> |<span data-ttu-id="3ccd7-111">Puntos a la primera fila de una tabla.</span><span class="sxs-lookup"><span data-stu-id="3ccd7-111">Points to the first row in a table.</span></span>  <br/> |
|<span data-ttu-id="3ccd7-112">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="3ccd7-112">BOOKMARK_END</span></span>  <br/> |<span data-ttu-id="3ccd7-113">Apunta a la última fila de una tabla.</span><span class="sxs-lookup"><span data-stu-id="3ccd7-113">Points to the last row in a table.</span></span>  <br/> |
   
<span data-ttu-id="3ccd7-114">Los implementadores de tabla son necesarios para admitir estos marcadores estándares y también pueden admitir otros usuarios.</span><span class="sxs-lookup"><span data-stu-id="3ccd7-114">Table implementers are required to support these standard bookmarks and can also support others.</span></span> <span data-ttu-id="3ccd7-115">Sin embargo, debido a que los marcadores son recursos y los recursos se limitan, los usuarios de marcador deben liberarlos tan pronto como sea posible.</span><span class="sxs-lookup"><span data-stu-id="3ccd7-115">However, because bookmarks are resources and resources are limited, bookmark users should free them as soon as possible.</span></span> 
  
 <span data-ttu-id="3ccd7-116">**Para establecer un marcador en la posición actual de la tabla**</span><span class="sxs-lookup"><span data-stu-id="3ccd7-116">**To set a bookmark at the current table position**</span></span>
  
- <span data-ttu-id="3ccd7-117">Llame a [IMAPITable::CreateBookmark](imapitable-createbookmark.md).</span><span class="sxs-lookup"><span data-stu-id="3ccd7-117">Call [IMAPITable::CreateBookmark](imapitable-createbookmark.md).</span></span> <span data-ttu-id="3ccd7-118">En ocasiones será suficiente memoria disponible para asignar el nuevo marcador, lo que provoca que **CreateBookmark** devolver el valor de error MAPI_E_UNABLE_TO_COMPLETE.</span><span class="sxs-lookup"><span data-stu-id="3ccd7-118">Occasionally there will be insufficient memory available to allocate the new bookmark, causing **CreateBookmark** to return the MAPI_E_UNABLE_TO_COMPLETE error value.</span></span> 
    
 <span data-ttu-id="3ccd7-119">**Para liberar un marcador**</span><span class="sxs-lookup"><span data-stu-id="3ccd7-119">**To free a bookmark**</span></span>
  
- <span data-ttu-id="3ccd7-120">Llame a [IMAPITable::FreeBookmark](imapitable-freebookmark.md).</span><span class="sxs-lookup"><span data-stu-id="3ccd7-120">Call [IMAPITable::FreeBookmark](imapitable-freebookmark.md).</span></span>
    
 <span data-ttu-id="3ccd7-121">**Para mover el cursor a una posición con marcador**</span><span class="sxs-lookup"><span data-stu-id="3ccd7-121">**To move the cursor to a bookmarked position**</span></span>
  
- <span data-ttu-id="3ccd7-122">Llame a [IMAPITable::SeekRow](imapitable-seekrow.md).</span><span class="sxs-lookup"><span data-stu-id="3ccd7-122">Call [IMAPITable::SeekRow](imapitable-seekrow.md).</span></span> <span data-ttu-id="3ccd7-123">**SeekRow** establece un nuevo valor para la posición de BOOKMARK_CURRENT.</span><span class="sxs-lookup"><span data-stu-id="3ccd7-123">**SeekRow** establishes a new value for the BOOKMARK_CURRENT position.</span></span> <span data-ttu-id="3ccd7-124">**SeekRow** puede utilizarse, por ejemplo, para colocar un filas de tabla diez desde la posición actual o para empezar de nuevo al principio.</span><span class="sxs-lookup"><span data-stu-id="3ccd7-124">**SeekRow** can be used, for example, to position a table ten rows from the current position or to start over at the beginning.</span></span> <span data-ttu-id="3ccd7-125">Los clientes o proveedores de servicios pueden buscar a la actual, a partir de, o finalizar de una tabla o cualquier otra posición en la que está asociada con un marcador predefinido.</span><span class="sxs-lookup"><span data-stu-id="3ccd7-125">Clients or service providers can seek to the current, beginning, or end of a table, or any other position that is associated with a predefined bookmark.</span></span> <span data-ttu-id="3ccd7-126">En una dirección hacia delante o hacia atrás y el límite de la operación puede mover a un número especificado de filas.</span><span class="sxs-lookup"><span data-stu-id="3ccd7-126">They can move in either a forward or backward direction and limit the operation to a specified number of rows.</span></span> <span data-ttu-id="3ccd7-127">Como regla general, deben tratar de los autores de llamadas a través de no más de 50 filas con **SeekRow**; Debe usarse [IMAPITable:: SeekRowApprox](imapitable-seekrowapprox.md) con un gran número de filas.</span><span class="sxs-lookup"><span data-stu-id="3ccd7-127">As a rule, callers should seek through no more than 50 rows with **SeekRow**; [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) should be used with larger numbers of rows.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="3ccd7-128">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="3ccd7-128">See also</span></span>



[<span data-ttu-id="3ccd7-129">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="3ccd7-129">MAPI Tables</span></span>](mapi-tables.md)

