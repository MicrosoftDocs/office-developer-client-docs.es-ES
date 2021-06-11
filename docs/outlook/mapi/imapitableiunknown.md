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
ms.openlocfilehash: d6a13799da4ef9315f9c23317fa18853d71c72f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420118"
---
# <a name="imapitable--iunknown"></a><span data-ttu-id="76211-103">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="76211-103">IMAPITable : IUnknown</span></span>

  
  
<span data-ttu-id="76211-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="76211-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="76211-105">Proporciona una vista de solo lectura de una tabla.</span><span class="sxs-lookup"><span data-stu-id="76211-105">Provides a read-only view of a table.</span></span> <span data-ttu-id="76211-106">Los clientes y proveedores de servicios usan **IMAPITable** para manipular la forma en que aparece una tabla.</span><span class="sxs-lookup"><span data-stu-id="76211-106">**IMAPITable** is used by clients and service providers to manipulate the way a table appears.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="76211-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="76211-107">Header file:</span></span>  <br/> |<span data-ttu-id="76211-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="76211-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="76211-109">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="76211-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="76211-110">Objetos Table</span><span class="sxs-lookup"><span data-stu-id="76211-110">Table objects</span></span>  <br/> |
|<span data-ttu-id="76211-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="76211-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="76211-112">Proveedores de servicios y MAPI</span><span class="sxs-lookup"><span data-stu-id="76211-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="76211-113">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="76211-113">Called by:</span></span>  <br/> |<span data-ttu-id="76211-114">Aplicaciones cliente, proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="76211-114">Client applications, service providers</span></span>  <br/> |
|<span data-ttu-id="76211-115">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="76211-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="76211-116">IID_IMAPITable</span><span class="sxs-lookup"><span data-stu-id="76211-116">IID_IMAPITable</span></span>  <br/> |
|<span data-ttu-id="76211-117">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="76211-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="76211-118">LPMAPITABLE</span><span class="sxs-lookup"><span data-stu-id="76211-118">LPMAPITABLE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="76211-119">Orden de Vtable</span><span class="sxs-lookup"><span data-stu-id="76211-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="76211-120">GetLastError</span><span class="sxs-lookup"><span data-stu-id="76211-120">GetLastError</span></span>](imapitable-getlasterror.md) <br/> |<span data-ttu-id="76211-121">Devuelve una [estructura MAPIERROR](mapierror.md) que contiene información sobre el error anterior en la tabla.</span><span class="sxs-lookup"><span data-stu-id="76211-121">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error on the table.</span></span>  <br/> |
|[<span data-ttu-id="76211-122">Aconsejar</span><span class="sxs-lookup"><span data-stu-id="76211-122">Advise</span></span>](imapitable-advise.md) <br/> |<span data-ttu-id="76211-123">Se registra para recibir una notificación de eventos especificados que afectan a la tabla.</span><span class="sxs-lookup"><span data-stu-id="76211-123">Registers to receive notification of specified events affecting the table.</span></span>  <br/> |
|[<span data-ttu-id="76211-124">Unadvise</span><span class="sxs-lookup"><span data-stu-id="76211-124">Unadvise</span></span>](imapitable-unadvise.md) <br/> |<span data-ttu-id="76211-125">Cancela el envío de notificaciones configuradas anteriormente con una llamada al **método IMAPITable::Advise.**</span><span class="sxs-lookup"><span data-stu-id="76211-125">Cancels the sending of notifications previously set up with a call to the **IMAPITable::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="76211-126">GetStatus</span><span class="sxs-lookup"><span data-stu-id="76211-126">GetStatus</span></span>](imapitable-getstatus.md) <br/> |<span data-ttu-id="76211-127">Devuelve el estado y el tipo de la tabla.</span><span class="sxs-lookup"><span data-stu-id="76211-127">Returns the table's status and type.</span></span>  <br/> |
|[<span data-ttu-id="76211-128">SetColumns</span><span class="sxs-lookup"><span data-stu-id="76211-128">SetColumns</span></span>](imapitable-setcolumns.md) <br/> |<span data-ttu-id="76211-129">Define las propiedades concretas y el orden de las propiedades que se mostrarán como columnas en la tabla.</span><span class="sxs-lookup"><span data-stu-id="76211-129">Defines the particular properties and order of properties to appear as columns in the table.</span></span>  <br/> |
|[<span data-ttu-id="76211-130">QueryColumns</span><span class="sxs-lookup"><span data-stu-id="76211-130">QueryColumns</span></span>](imapitable-querycolumns.md) <br/> |<span data-ttu-id="76211-131">Devuelve una lista de columnas para la tabla.</span><span class="sxs-lookup"><span data-stu-id="76211-131">Returns a list of columns for the table.</span></span>  <br/> |
|[<span data-ttu-id="76211-132">GetRowCount</span><span class="sxs-lookup"><span data-stu-id="76211-132">GetRowCount</span></span>](imapitable-getrowcount.md) <br/> |<span data-ttu-id="76211-133">Devuelve el número total de filas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="76211-133">Returns the total number of rows in the table.</span></span>  <br/> |
|[<span data-ttu-id="76211-134">SeekRow</span><span class="sxs-lookup"><span data-stu-id="76211-134">SeekRow</span></span>](imapitable-seekrow.md) <br/> |<span data-ttu-id="76211-135">Mueve el cursor a una posición específica de la tabla.</span><span class="sxs-lookup"><span data-stu-id="76211-135">Moves the cursor to a specific position in the table.</span></span>  <br/> |
|[<span data-ttu-id="76211-136">SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="76211-136">SeekRowApprox</span></span>](imapitable-seekrowapprox.md) <br/> |<span data-ttu-id="76211-137">Mueve el cursor a una posición fraccional aproximada de la tabla.</span><span class="sxs-lookup"><span data-stu-id="76211-137">Moves the cursor to an approximate fractional position in the table.</span></span>  <br/> |
|[<span data-ttu-id="76211-138">QueryPosition</span><span class="sxs-lookup"><span data-stu-id="76211-138">QueryPosition</span></span>](imapitable-queryposition.md) <br/> |<span data-ttu-id="76211-139">Recupera la posición actual de fila de tabla del cursor, basándose en un valor fraccional.</span><span class="sxs-lookup"><span data-stu-id="76211-139">Retrieves the current table row position of the cursor, based on a fractional value.</span></span>  <br/> |
|[<span data-ttu-id="76211-140">FindRow</span><span class="sxs-lookup"><span data-stu-id="76211-140">FindRow</span></span>](imapitable-findrow.md) <br/> |<span data-ttu-id="76211-141">Busca la siguiente fila de una tabla que coincida con criterios de búsqueda específicos.</span><span class="sxs-lookup"><span data-stu-id="76211-141">Finds the next row in a table that matches specific search criteria.</span></span>  <br/> |
|[<span data-ttu-id="76211-142">Restrict</span><span class="sxs-lookup"><span data-stu-id="76211-142">Restrict</span></span>](imapitable-restrict.md) <br/> |<span data-ttu-id="76211-143">Aplica un filtro a una tabla, lo que reduce el conjunto de filas a solo aquellas filas que coincidan con los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="76211-143">Applies a filter to a table, reducing the row set to only those rows matching the specified criteria.</span></span>  <br/> |
|[<span data-ttu-id="76211-144">CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="76211-144">CreateBookmark</span></span>](imapitable-createbookmark.md) <br/> |<span data-ttu-id="76211-145">Marca la posición actual de la tabla.</span><span class="sxs-lookup"><span data-stu-id="76211-145">Marks the table's current position.</span></span>  <br/> |
|[<span data-ttu-id="76211-146">FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="76211-146">FreeBookmark</span></span>](imapitable-freebookmark.md) <br/> |<span data-ttu-id="76211-147">Libera la memoria asociada a un marcador.</span><span class="sxs-lookup"><span data-stu-id="76211-147">Releases the memory associated with a bookmark.</span></span>  <br/> |
|[<span data-ttu-id="76211-148">SortTable</span><span class="sxs-lookup"><span data-stu-id="76211-148">SortTable</span></span>](imapitable-sorttable.md) <br/> |<span data-ttu-id="76211-149">Ordena las filas de la tabla según criterios de ordenación.</span><span class="sxs-lookup"><span data-stu-id="76211-149">Orders the rows of the table based on sort criteria.</span></span>  <br/> |
|[<span data-ttu-id="76211-150">QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="76211-150">QuerySortOrder</span></span>](imapitable-querysortorder.md) <br/> |<span data-ttu-id="76211-151">Recupera el criterio de ordenación actual de una tabla.</span><span class="sxs-lookup"><span data-stu-id="76211-151">Retrieves the current sort order for a table.</span></span>  <br/> |
|[<span data-ttu-id="76211-152">QueryRows</span><span class="sxs-lookup"><span data-stu-id="76211-152">QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="76211-153">Devuelve una o más filas de una tabla, comenzando en la posición actual del cursor.</span><span class="sxs-lookup"><span data-stu-id="76211-153">Returns one or more rows from a table, beginning at the current cursor position.</span></span>  <br/> |
|[<span data-ttu-id="76211-154">Anular</span><span class="sxs-lookup"><span data-stu-id="76211-154">Abort</span></span>](imapitable-abort.md) <br/> |<span data-ttu-id="76211-155">Detiene las operaciones asincrónicas actualmente en curso para la tabla.</span><span class="sxs-lookup"><span data-stu-id="76211-155">Stops any asynchronous operations currently in progress for the table.</span></span>  <br/> |
|[<span data-ttu-id="76211-156">ExpandRow</span><span class="sxs-lookup"><span data-stu-id="76211-156">ExpandRow</span></span>](imapitable-expandrow.md) <br/> |<span data-ttu-id="76211-157">Expande una categoría de tabla contrae y agrega las filas de hoja que pertenecen a la categoría a la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="76211-157">Expands a collapsed table category, adding the leaf rows belonging to the category to the table view.</span></span>  <br/> |
|[<span data-ttu-id="76211-158">CollapseRow</span><span class="sxs-lookup"><span data-stu-id="76211-158">CollapseRow</span></span>](imapitable-collapserow.md) <br/> |<span data-ttu-id="76211-159">Contrae una categoría de tabla expandida, quitando las filas hoja que pertenecen a la categoría de la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="76211-159">Collapses an expanded table category, removing the leaf rows belonging to the category from the table view.</span></span>  <br/> |
|[<span data-ttu-id="76211-160">WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="76211-160">WaitForCompletion</span></span>](imapitable-waitforcompletion.md) <br/> |<span data-ttu-id="76211-161">Suspende el procesamiento hasta que se hayan completado una o varias operaciones asincrónicas en curso en la tabla.</span><span class="sxs-lookup"><span data-stu-id="76211-161">Suspends processing until one or more asynchronous operations in progress on the table have completed.</span></span>  <br/> |
|[<span data-ttu-id="76211-162">GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="76211-162">GetCollapseState</span></span>](imapitable-getcollapsestate.md) <br/> |<span data-ttu-id="76211-163">Devuelve los datos necesarios para volver a generar el estado contraído o expandido actual de una tabla categorizada.</span><span class="sxs-lookup"><span data-stu-id="76211-163">Returns the data necessary to rebuild the current collapsed or expanded state of a categorized table.</span></span>  <br/> |
|[<span data-ttu-id="76211-164">SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="76211-164">SetCollapseState</span></span>](imapitable-setcollapsestate.md) <br/> |<span data-ttu-id="76211-165">Vuelve a generar el estado expandido o contraído actual de una tabla categorizada con datos guardados mediante una llamada anterior al método **IMAPITable::GetCollapseState.**</span><span class="sxs-lookup"><span data-stu-id="76211-165">Rebuilds the current expanded or collapsed state of a categorized table using data that was saved by a prior call to the **IMAPITable::GetCollapseState** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="76211-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="76211-166">See also</span></span>



[<span data-ttu-id="76211-167">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="76211-167">MAPI Interfaces</span></span>](mapi-interfaces.md)

