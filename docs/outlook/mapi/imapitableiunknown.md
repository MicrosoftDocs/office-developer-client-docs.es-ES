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
# <a name="imapitable--iunknown"></a><span data-ttu-id="e7204-103">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e7204-103">IMAPITable : IUnknown</span></span>

  
  
<span data-ttu-id="e7204-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7204-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7204-105">Proporciona una vista de sólo lectura de una tabla.</span><span class="sxs-lookup"><span data-stu-id="e7204-105">Provides a read-only view of a table.</span></span> <span data-ttu-id="e7204-106">Los clientes y los proveedores de servicios usan el **IMAPITable** para manipular la apariencia de una tabla.</span><span class="sxs-lookup"><span data-stu-id="e7204-106">**IMAPITable** is used by clients and service providers to manipulate the way a table appears.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e7204-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="e7204-107">Header file:</span></span>  <br/> |<span data-ttu-id="e7204-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e7204-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e7204-109">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="e7204-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="e7204-110">Objetos Table</span><span class="sxs-lookup"><span data-stu-id="e7204-110">Table objects</span></span>  <br/> |
|<span data-ttu-id="e7204-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="e7204-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="e7204-112">Proveedores de servicios y MAPI</span><span class="sxs-lookup"><span data-stu-id="e7204-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="e7204-113">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="e7204-113">Called by:</span></span>  <br/> |<span data-ttu-id="e7204-114">Aplicaciones cliente, proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="e7204-114">Client applications, service providers</span></span>  <br/> |
|<span data-ttu-id="e7204-115">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="e7204-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e7204-116">IID_IMAPITable</span><span class="sxs-lookup"><span data-stu-id="e7204-116">IID_IMAPITable</span></span>  <br/> |
|<span data-ttu-id="e7204-117">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="e7204-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="e7204-118">LPMAPITABLE</span><span class="sxs-lookup"><span data-stu-id="e7204-118">LPMAPITABLE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e7204-119">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="e7204-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="e7204-120">Volvió</span><span class="sxs-lookup"><span data-stu-id="e7204-120">GetLastError</span></span>](imapitable-getlasterror.md) <br/> |<span data-ttu-id="e7204-121">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior de la tabla.</span><span class="sxs-lookup"><span data-stu-id="e7204-121">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error on the table.</span></span>  <br/> |
|[<span data-ttu-id="e7204-122">Aconsej</span><span class="sxs-lookup"><span data-stu-id="e7204-122">Advise</span></span>](imapitable-advise.md) <br/> |<span data-ttu-id="e7204-123">Se registra para recibir una notificación de los eventos especificados que afectan a la tabla.</span><span class="sxs-lookup"><span data-stu-id="e7204-123">Registers to receive notification of specified events affecting the table.</span></span>  <br/> |
|[<span data-ttu-id="e7204-124">Unadvise</span><span class="sxs-lookup"><span data-stu-id="e7204-124">Unadvise</span></span>](imapitable-unadvise.md) <br/> |<span data-ttu-id="e7204-125">Cancela el envío de notificaciones previamente configurado con una llamada al método **IMAPITable:: Advise** .</span><span class="sxs-lookup"><span data-stu-id="e7204-125">Cancels the sending of notifications previously set up with a call to the **IMAPITable::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="e7204-126">GetStatus</span><span class="sxs-lookup"><span data-stu-id="e7204-126">GetStatus</span></span>](imapitable-getstatus.md) <br/> |<span data-ttu-id="e7204-127">Devuelve el tipo y el estado de la tabla.</span><span class="sxs-lookup"><span data-stu-id="e7204-127">Returns the table's status and type.</span></span>  <br/> |
|[<span data-ttu-id="e7204-128">SetColumns</span><span class="sxs-lookup"><span data-stu-id="e7204-128">SetColumns</span></span>](imapitable-setcolumns.md) <br/> |<span data-ttu-id="e7204-129">Define las propiedades y el orden de las propiedades específicas que aparecerán como columnas en la tabla.</span><span class="sxs-lookup"><span data-stu-id="e7204-129">Defines the particular properties and order of properties to appear as columns in the table.</span></span>  <br/> |
|[<span data-ttu-id="e7204-130">QueryColumns</span><span class="sxs-lookup"><span data-stu-id="e7204-130">QueryColumns</span></span>](imapitable-querycolumns.md) <br/> |<span data-ttu-id="e7204-131">Devuelve una lista de las columnas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="e7204-131">Returns a list of columns for the table.</span></span>  <br/> |
|[<span data-ttu-id="e7204-132">GetRowCount</span><span class="sxs-lookup"><span data-stu-id="e7204-132">GetRowCount</span></span>](imapitable-getrowcount.md) <br/> |<span data-ttu-id="e7204-133">Devuelve el número total de filas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="e7204-133">Returns the total number of rows in the table.</span></span>  <br/> |
|[<span data-ttu-id="e7204-134">SeekRow</span><span class="sxs-lookup"><span data-stu-id="e7204-134">SeekRow</span></span>](imapitable-seekrow.md) <br/> |<span data-ttu-id="e7204-135">Mueve el cursor a una posición específica de la tabla.</span><span class="sxs-lookup"><span data-stu-id="e7204-135">Moves the cursor to a specific position in the table.</span></span>  <br/> |
|[<span data-ttu-id="e7204-136">SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="e7204-136">SeekRowApprox</span></span>](imapitable-seekrowapprox.md) <br/> |<span data-ttu-id="e7204-137">Mueve el cursor a una posición fraccional aproximada en la tabla.</span><span class="sxs-lookup"><span data-stu-id="e7204-137">Moves the cursor to an approximate fractional position in the table.</span></span>  <br/> |
|[<span data-ttu-id="e7204-138">QueryPosition</span><span class="sxs-lookup"><span data-stu-id="e7204-138">QueryPosition</span></span>](imapitable-queryposition.md) <br/> |<span data-ttu-id="e7204-139">Recupera la posición de fila de la tabla actual del cursor, en función de un valor fraccionario.</span><span class="sxs-lookup"><span data-stu-id="e7204-139">Retrieves the current table row position of the cursor, based on a fractional value.</span></span>  <br/> |
|[<span data-ttu-id="e7204-140">FindRow</span><span class="sxs-lookup"><span data-stu-id="e7204-140">FindRow</span></span>](imapitable-findrow.md) <br/> |<span data-ttu-id="e7204-141">Busca la siguiente fila de una tabla que coincida con los criterios de búsqueda específicos.</span><span class="sxs-lookup"><span data-stu-id="e7204-141">Finds the next row in a table that matches specific search criteria.</span></span>  <br/> |
|[<span data-ttu-id="e7204-142">Restrict</span><span class="sxs-lookup"><span data-stu-id="e7204-142">Restrict</span></span>](imapitable-restrict.md) <br/> |<span data-ttu-id="e7204-143">Aplica un filtro a una tabla, lo que reduce el conjunto de filas a solo aquellas filas que coinciden con los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="e7204-143">Applies a filter to a table, reducing the row set to only those rows matching the specified criteria.</span></span>  <br/> |
|[<span data-ttu-id="e7204-144">CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="e7204-144">CreateBookmark</span></span>](imapitable-createbookmark.md) <br/> |<span data-ttu-id="e7204-145">Marca la posición actual de la tabla.</span><span class="sxs-lookup"><span data-stu-id="e7204-145">Marks the table's current position.</span></span>  <br/> |
|[<span data-ttu-id="e7204-146">FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="e7204-146">FreeBookmark</span></span>](imapitable-freebookmark.md) <br/> |<span data-ttu-id="e7204-147">Libera la memoria asociada a un marcador.</span><span class="sxs-lookup"><span data-stu-id="e7204-147">Releases the memory associated with a bookmark.</span></span>  <br/> |
|[<span data-ttu-id="e7204-148">SortTable</span><span class="sxs-lookup"><span data-stu-id="e7204-148">SortTable</span></span>](imapitable-sorttable.md) <br/> |<span data-ttu-id="e7204-149">Ordena las filas de la tabla según los criterios de ordenación.</span><span class="sxs-lookup"><span data-stu-id="e7204-149">Orders the rows of the table based on sort criteria.</span></span>  <br/> |
|[<span data-ttu-id="e7204-150">QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="e7204-150">QuerySortOrder</span></span>](imapitable-querysortorder.md) <br/> |<span data-ttu-id="e7204-151">Recupera el criterio de ordenación actual de una tabla.</span><span class="sxs-lookup"><span data-stu-id="e7204-151">Retrieves the current sort order for a table.</span></span>  <br/> |
|[<span data-ttu-id="e7204-152">QueryRows</span><span class="sxs-lookup"><span data-stu-id="e7204-152">QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="e7204-153">Devuelve una o más filas de una tabla, comenzando en la posición actual del cursor.</span><span class="sxs-lookup"><span data-stu-id="e7204-153">Returns one or more rows from a table, beginning at the current cursor position.</span></span>  <br/> |
|[<span data-ttu-id="e7204-154">Anular</span><span class="sxs-lookup"><span data-stu-id="e7204-154">Abort</span></span>](imapitable-abort.md) <br/> |<span data-ttu-id="e7204-155">Detiene todas las operaciones asincrónicas que se encuentran en curso para la tabla.</span><span class="sxs-lookup"><span data-stu-id="e7204-155">Stops any asynchronous operations currently in progress for the table.</span></span>  <br/> |
|[<span data-ttu-id="e7204-156">ExpandRow</span><span class="sxs-lookup"><span data-stu-id="e7204-156">ExpandRow</span></span>](imapitable-expandrow.md) <br/> |<span data-ttu-id="e7204-157">Expande una categoría de tabla contraída, agregando las filas hoja que pertenecen a la categoría a la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="e7204-157">Expands a collapsed table category, adding the leaf rows belonging to the category to the table view.</span></span>  <br/> |
|[<span data-ttu-id="e7204-158">CollapseRow</span><span class="sxs-lookup"><span data-stu-id="e7204-158">CollapseRow</span></span>](imapitable-collapserow.md) <br/> |<span data-ttu-id="e7204-159">Contrae una categoría de tabla expandida, quitando las filas hoja que pertenecen a la categoría de la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="e7204-159">Collapses an expanded table category, removing the leaf rows belonging to the category from the table view.</span></span>  <br/> |
|[<span data-ttu-id="e7204-160">WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="e7204-160">WaitForCompletion</span></span>](imapitable-waitforcompletion.md) <br/> |<span data-ttu-id="e7204-161">Suspende el procesamiento hasta que se completen una o más operaciones asincrónicas en curso en la tabla.</span><span class="sxs-lookup"><span data-stu-id="e7204-161">Suspends processing until one or more asynchronous operations in progress on the table have completed.</span></span>  <br/> |
|[<span data-ttu-id="e7204-162">GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="e7204-162">GetCollapseState</span></span>](imapitable-getcollapsestate.md) <br/> |<span data-ttu-id="e7204-163">Devuelve los datos necesarios para volver a generar el estado de contraído o expandido actual de una tabla clasificada.</span><span class="sxs-lookup"><span data-stu-id="e7204-163">Returns the data necessary to rebuild the current collapsed or expanded state of a categorized table.</span></span>  <br/> |
|[<span data-ttu-id="e7204-164">SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="e7204-164">SetCollapseState</span></span>](imapitable-setcollapsestate.md) <br/> |<span data-ttu-id="e7204-165">Vuelve a compilar el estado expandido o contraído actual de una tabla clasificada con datos que se guardaron mediante una llamada anterior al método **IMAPITable:: GetCollapseState** .</span><span class="sxs-lookup"><span data-stu-id="e7204-165">Rebuilds the current expanded or collapsed state of a categorized table using data that was saved by a prior call to the **IMAPITable::GetCollapseState** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e7204-166">Ver también</span><span class="sxs-lookup"><span data-stu-id="e7204-166">See also</span></span>



[<span data-ttu-id="e7204-167">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="e7204-167">MAPI Interfaces</span></span>](mapi-interfaces.md)

