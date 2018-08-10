---
title: IMAPITable IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable
api_type:
- COM
ms.assetid: f25be2b1-0f94-4a0c-b29d-d2201dc70ab7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0ffaf5909c978059343067c93a2b30f5969327e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817606"
---
# <a name="imapitable--iunknown"></a><span data-ttu-id="63c7f-103">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="63c7f-103">IMAPITable : IUnknown</span></span>

  
  
<span data-ttu-id="63c7f-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="63c7f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="63c7f-105">Proporciona una vista de sólo lectura de una tabla.</span><span class="sxs-lookup"><span data-stu-id="63c7f-105">Provides a read-only view of a table.</span></span> <span data-ttu-id="63c7f-106">**IMAPITable** se usa en los clientes y proveedores de servicios para manipular la apariencia de una tabla.</span><span class="sxs-lookup"><span data-stu-id="63c7f-106">**IMAPITable** is used by clients and service providers to manipulate the way a table appears.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="63c7f-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="63c7f-107">Header file:</span></span>  <br/> |<span data-ttu-id="63c7f-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="63c7f-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="63c7f-109">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="63c7f-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="63c7f-110">Objetos de la tabla</span><span class="sxs-lookup"><span data-stu-id="63c7f-110">Table objects</span></span>  <br/> |
|<span data-ttu-id="63c7f-111">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="63c7f-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="63c7f-112">Proveedores de servicios y MAPI</span><span class="sxs-lookup"><span data-stu-id="63c7f-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="63c7f-113">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="63c7f-113">Called by:</span></span>  <br/> |<span data-ttu-id="63c7f-114">Aplicaciones cliente, los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="63c7f-114">Client applications, service providers</span></span>  <br/> |
|<span data-ttu-id="63c7f-115">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="63c7f-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="63c7f-116">IID_IMAPITable</span><span class="sxs-lookup"><span data-stu-id="63c7f-116">IID_IMAPITable</span></span>  <br/> |
|<span data-ttu-id="63c7f-117">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="63c7f-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="63c7f-118">LPMAPITABLE</span><span class="sxs-lookup"><span data-stu-id="63c7f-118">LPMAPITABLE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="63c7f-119">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="63c7f-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="63c7f-120">GetLastError</span><span class="sxs-lookup"><span data-stu-id="63c7f-120">GetLastError</span></span>](imapitable-getlasterror.md) <br/> |<span data-ttu-id="63c7f-121">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior en la tabla.</span><span class="sxs-lookup"><span data-stu-id="63c7f-121">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error on the table.</span></span>  <br/> |
|[<span data-ttu-id="63c7f-122">Aviso</span><span class="sxs-lookup"><span data-stu-id="63c7f-122">Advise</span></span>](imapitable-advise.md) <br/> |<span data-ttu-id="63c7f-123">Se registra para recibir notificaciones de los eventos que afectan a la tabla.</span><span class="sxs-lookup"><span data-stu-id="63c7f-123">Registers to receive notification of specified events affecting the table.</span></span>  <br/> |
|[<span data-ttu-id="63c7f-124">Desaconsejar</span><span class="sxs-lookup"><span data-stu-id="63c7f-124">Unadvise</span></span>](imapitable-unadvise.md) <br/> |<span data-ttu-id="63c7f-125">Cancela el envío de notificaciones configuradas previamente con una llamada al método **IMAPITable::Advise** .</span><span class="sxs-lookup"><span data-stu-id="63c7f-125">Cancels the sending of notifications previously set up with a call to the **IMAPITable::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="63c7f-126">GetStatus</span><span class="sxs-lookup"><span data-stu-id="63c7f-126">GetStatus</span></span>](imapitable-getstatus.md) <br/> |<span data-ttu-id="63c7f-127">Devuelve el estado y el tipo de la tabla.</span><span class="sxs-lookup"><span data-stu-id="63c7f-127">Returns the table's status and type.</span></span>  <br/> |
|[<span data-ttu-id="63c7f-128">SetColumns</span><span class="sxs-lookup"><span data-stu-id="63c7f-128">SetColumns</span></span>](imapitable-setcolumns.md) <br/> |<span data-ttu-id="63c7f-129">Define las propiedades concretas y el orden de las propiedades que aparecen como columnas en la tabla.</span><span class="sxs-lookup"><span data-stu-id="63c7f-129">Defines the particular properties and order of properties to appear as columns in the table.</span></span>  <br/> |
|[<span data-ttu-id="63c7f-130">QueryColumns</span><span class="sxs-lookup"><span data-stu-id="63c7f-130">QueryColumns</span></span>](imapitable-querycolumns.md) <br/> |<span data-ttu-id="63c7f-131">Devuelve una lista de columnas para la tabla.</span><span class="sxs-lookup"><span data-stu-id="63c7f-131">Returns a list of columns for the table.</span></span>  <br/> |
|[<span data-ttu-id="63c7f-132">GetRowCount</span><span class="sxs-lookup"><span data-stu-id="63c7f-132">GetRowCount</span></span>](imapitable-getrowcount.md) <br/> |<span data-ttu-id="63c7f-133">Devuelve el número total de filas en la tabla.</span><span class="sxs-lookup"><span data-stu-id="63c7f-133">Returns the total number of rows in the table.</span></span>  <br/> |
|[<span data-ttu-id="63c7f-134">SeekRow</span><span class="sxs-lookup"><span data-stu-id="63c7f-134">SeekRow</span></span>](imapitable-seekrow.md) <br/> |<span data-ttu-id="63c7f-135">Mueve el cursor a una posición específica en la tabla.</span><span class="sxs-lookup"><span data-stu-id="63c7f-135">Moves the cursor to a specific position in the table.</span></span>  <br/> |
|[<span data-ttu-id="63c7f-136">SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="63c7f-136">SeekRowApprox</span></span>](imapitable-seekrowapprox.md) <br/> |<span data-ttu-id="63c7f-137">Mueve el cursor a una posición aproximada fraccionaria en la tabla.</span><span class="sxs-lookup"><span data-stu-id="63c7f-137">Moves the cursor to an approximate fractional position in the table.</span></span>  <br/> |
|[<span data-ttu-id="63c7f-138">QueryPosition</span><span class="sxs-lookup"><span data-stu-id="63c7f-138">QueryPosition</span></span>](imapitable-queryposition.md) <br/> |<span data-ttu-id="63c7f-139">Recupera la posición de fila de tabla actual del cursor, basándose en un valor decimal.</span><span class="sxs-lookup"><span data-stu-id="63c7f-139">Retrieves the current table row position of the cursor, based on a fractional value.</span></span>  <br/> |
|[<span data-ttu-id="63c7f-140">FindRow</span><span class="sxs-lookup"><span data-stu-id="63c7f-140">FindRow</span></span>](imapitable-findrow.md) <br/> |<span data-ttu-id="63c7f-141">Busca la siguiente fila en una tabla que coincida con los criterios de búsqueda específicos.</span><span class="sxs-lookup"><span data-stu-id="63c7f-141">Finds the next row in a table that matches specific search criteria.</span></span>  <br/> |
|[<span data-ttu-id="63c7f-142">Restringir</span><span class="sxs-lookup"><span data-stu-id="63c7f-142">Restrict</span></span>](imapitable-restrict.md) <br/> |<span data-ttu-id="63c7f-143">Se aplica un filtro a una tabla, reducción de la fila que se establece en sólo las filas que coincidan con los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="63c7f-143">Applies a filter to a table, reducing the row set to only those rows matching the specified criteria.</span></span>  <br/> |
|[<span data-ttu-id="63c7f-144">CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="63c7f-144">CreateBookmark</span></span>](imapitable-createbookmark.md) <br/> |<span data-ttu-id="63c7f-145">Marca la posición actual de la tabla.</span><span class="sxs-lookup"><span data-stu-id="63c7f-145">Marks the table's current position.</span></span>  <br/> |
|[<span data-ttu-id="63c7f-146">FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="63c7f-146">FreeBookmark</span></span>](imapitable-freebookmark.md) <br/> |<span data-ttu-id="63c7f-147">Libera la memoria asociada con un marcador.</span><span class="sxs-lookup"><span data-stu-id="63c7f-147">Releases the memory associated with a bookmark.</span></span>  <br/> |
|[<span data-ttu-id="63c7f-148">SortTable</span><span class="sxs-lookup"><span data-stu-id="63c7f-148">SortTable</span></span>](imapitable-sorttable.md) <br/> |<span data-ttu-id="63c7f-149">Ordena las filas de la tabla en función de los criterios de ordenación.</span><span class="sxs-lookup"><span data-stu-id="63c7f-149">Orders the rows of the table based on sort criteria.</span></span>  <br/> |
|[<span data-ttu-id="63c7f-150">QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="63c7f-150">QuerySortOrder</span></span>](imapitable-querysortorder.md) <br/> |<span data-ttu-id="63c7f-151">Recupera el criterio de ordenación actual para una tabla.</span><span class="sxs-lookup"><span data-stu-id="63c7f-151">Retrieves the current sort order for a table.</span></span>  <br/> |
|[<span data-ttu-id="63c7f-152">QueryRows</span><span class="sxs-lookup"><span data-stu-id="63c7f-152">QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="63c7f-153">Devuelve una o varias filas de una tabla, que comienza en la posición actual del cursor.</span><span class="sxs-lookup"><span data-stu-id="63c7f-153">Returns one or more rows from a table, beginning at the current cursor position.</span></span>  <br/> |
|[<span data-ttu-id="63c7f-154">Anular</span><span class="sxs-lookup"><span data-stu-id="63c7f-154">Abort</span></span>](imapitable-abort.md) <br/> |<span data-ttu-id="63c7f-155">Detiene cualquier operación asincrónica actualmente en curso para la tabla.</span><span class="sxs-lookup"><span data-stu-id="63c7f-155">Stops any asynchronous operations currently in progress for the table.</span></span>  <br/> |
|[<span data-ttu-id="63c7f-156">ExpandRow</span><span class="sxs-lookup"><span data-stu-id="63c7f-156">ExpandRow</span></span>](imapitable-expandrow.md) <br/> |<span data-ttu-id="63c7f-157">Expande una categoría de tabla contraído, adición de las filas de la hoja que pertenecen a la categoría a la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="63c7f-157">Expands a collapsed table category, adding the leaf rows belonging to the category to the table view.</span></span>  <br/> |
|[<span data-ttu-id="63c7f-158">CollapseRow</span><span class="sxs-lookup"><span data-stu-id="63c7f-158">CollapseRow</span></span>](imapitable-collapserow.md) <br/> |<span data-ttu-id="63c7f-159">Contrae una categoría de tabla expandida, quitar las filas de la hoja que pertenecen a la categoría de la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="63c7f-159">Collapses an expanded table category, removing the leaf rows belonging to the category from the table view.</span></span>  <br/> |
|[<span data-ttu-id="63c7f-160">WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="63c7f-160">WaitForCompletion</span></span>](imapitable-waitforcompletion.md) <br/> |<span data-ttu-id="63c7f-161">Suspende el procesamiento hasta que han completado una o varias operaciones asincrónicas en curso en la tabla.</span><span class="sxs-lookup"><span data-stu-id="63c7f-161">Suspends processing until one or more asynchronous operations in progress on the table have completed.</span></span>  <br/> |
|[<span data-ttu-id="63c7f-162">GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="63c7f-162">GetCollapseState</span></span>](imapitable-getcollapsestate.md) <br/> |<span data-ttu-id="63c7f-163">Devuelve los datos necesarios para volver a generar la actual contraído o expandido el estado de una tabla con categorías.</span><span class="sxs-lookup"><span data-stu-id="63c7f-163">Returns the data necessary to rebuild the current collapsed or expanded state of a categorized table.</span></span>  <br/> |
|[<span data-ttu-id="63c7f-164">SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="63c7f-164">SetCollapseState</span></span>](imapitable-setcollapsestate.md) <br/> |<span data-ttu-id="63c7f-165">Vuelve a crear el estado actual de expandidos o contraído de una tabla con categorías utilizando los datos que se guardan por una llamada anterior al método **IMAPITable::GetCollapseState** .</span><span class="sxs-lookup"><span data-stu-id="63c7f-165">Rebuilds the current expanded or collapsed state of a categorized table using data that was saved by a prior call to the **IMAPITable::GetCollapseState** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="63c7f-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="63c7f-166">See also</span></span>



[<span data-ttu-id="63c7f-167">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="63c7f-167">MAPI Interfaces</span></span>](mapi-interfaces.md)

