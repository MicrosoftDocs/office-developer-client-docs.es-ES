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
# <a name="imapitable--iunknown"></a><span data-ttu-id="ced8e-103">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ced8e-103">IMAPITable : IUnknown</span></span>

  
  
<span data-ttu-id="ced8e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ced8e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ced8e-105">Proporciona una vista de solo lectura de una tabla.</span><span class="sxs-lookup"><span data-stu-id="ced8e-105">Provides a read-only view of a table.</span></span> <span data-ttu-id="ced8e-106">Los clientes y proveedores de servicios usan **IMAPITable** para manipular la forma en que aparece una tabla.</span><span class="sxs-lookup"><span data-stu-id="ced8e-106">**IMAPITable** is used by clients and service providers to manipulate the way a table appears.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ced8e-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="ced8e-107">Header file:</span></span>  <br/> |<span data-ttu-id="ced8e-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ced8e-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ced8e-109">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="ced8e-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="ced8e-110">Objetos Table</span><span class="sxs-lookup"><span data-stu-id="ced8e-110">Table objects</span></span>  <br/> |
|<span data-ttu-id="ced8e-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="ced8e-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="ced8e-112">Proveedores de servicios y MAPI</span><span class="sxs-lookup"><span data-stu-id="ced8e-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="ced8e-113">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="ced8e-113">Called by:</span></span>  <br/> |<span data-ttu-id="ced8e-114">Aplicaciones cliente, proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="ced8e-114">Client applications, service providers</span></span>  <br/> |
|<span data-ttu-id="ced8e-115">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="ced8e-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="ced8e-116">IID_IMAPITable</span><span class="sxs-lookup"><span data-stu-id="ced8e-116">IID_IMAPITable</span></span>  <br/> |
|<span data-ttu-id="ced8e-117">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="ced8e-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="ced8e-118">LPMAPITABLE</span><span class="sxs-lookup"><span data-stu-id="ced8e-118">LPMAPITABLE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="ced8e-119">Orden de tabla virtual</span><span class="sxs-lookup"><span data-stu-id="ced8e-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="ced8e-120">GetLastError</span><span class="sxs-lookup"><span data-stu-id="ced8e-120">GetLastError</span></span>](imapitable-getlasterror.md) <br/> |<span data-ttu-id="ced8e-121">Devuelve una [estructura MAPIERROR](mapierror.md) que contiene información sobre el error anterior de la tabla.</span><span class="sxs-lookup"><span data-stu-id="ced8e-121">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error on the table.</span></span>  <br/> |
|[<span data-ttu-id="ced8e-122">Aconsejar</span><span class="sxs-lookup"><span data-stu-id="ced8e-122">Advise</span></span>](imapitable-advise.md) <br/> |<span data-ttu-id="ced8e-123">Se registra para recibir una notificación de eventos especificados que afectan a la tabla.</span><span class="sxs-lookup"><span data-stu-id="ced8e-123">Registers to receive notification of specified events affecting the table.</span></span>  <br/> |
|[<span data-ttu-id="ced8e-124">Unadvise</span><span class="sxs-lookup"><span data-stu-id="ced8e-124">Unadvise</span></span>](imapitable-unadvise.md) <br/> |<span data-ttu-id="ced8e-125">Cancela el envío de notificaciones previamente configuradas con una llamada al método **IMAPITable::Advise.**</span><span class="sxs-lookup"><span data-stu-id="ced8e-125">Cancels the sending of notifications previously set up with a call to the **IMAPITable::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="ced8e-126">GetStatus</span><span class="sxs-lookup"><span data-stu-id="ced8e-126">GetStatus</span></span>](imapitable-getstatus.md) <br/> |<span data-ttu-id="ced8e-127">Devuelve el estado y el tipo de la tabla.</span><span class="sxs-lookup"><span data-stu-id="ced8e-127">Returns the table's status and type.</span></span>  <br/> |
|[<span data-ttu-id="ced8e-128">SetColumns</span><span class="sxs-lookup"><span data-stu-id="ced8e-128">SetColumns</span></span>](imapitable-setcolumns.md) <br/> |<span data-ttu-id="ced8e-129">Define las propiedades concretas y el orden de las propiedades que aparecen como columnas en la tabla.</span><span class="sxs-lookup"><span data-stu-id="ced8e-129">Defines the particular properties and order of properties to appear as columns in the table.</span></span>  <br/> |
|[<span data-ttu-id="ced8e-130">QueryColumns</span><span class="sxs-lookup"><span data-stu-id="ced8e-130">QueryColumns</span></span>](imapitable-querycolumns.md) <br/> |<span data-ttu-id="ced8e-131">Devuelve una lista de columnas para la tabla.</span><span class="sxs-lookup"><span data-stu-id="ced8e-131">Returns a list of columns for the table.</span></span>  <br/> |
|[<span data-ttu-id="ced8e-132">GetRowCount</span><span class="sxs-lookup"><span data-stu-id="ced8e-132">GetRowCount</span></span>](imapitable-getrowcount.md) <br/> |<span data-ttu-id="ced8e-133">Devuelve el número total de filas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="ced8e-133">Returns the total number of rows in the table.</span></span>  <br/> |
|[<span data-ttu-id="ced8e-134">SeekRow</span><span class="sxs-lookup"><span data-stu-id="ced8e-134">SeekRow</span></span>](imapitable-seekrow.md) <br/> |<span data-ttu-id="ced8e-135">Mueve el cursor a una posición específica de la tabla.</span><span class="sxs-lookup"><span data-stu-id="ced8e-135">Moves the cursor to a specific position in the table.</span></span>  <br/> |
|[<span data-ttu-id="ced8e-136">SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="ced8e-136">SeekRowApprox</span></span>](imapitable-seekrowapprox.md) <br/> |<span data-ttu-id="ced8e-137">Mueve el cursor a una posición fraccional aproximada en la tabla.</span><span class="sxs-lookup"><span data-stu-id="ced8e-137">Moves the cursor to an approximate fractional position in the table.</span></span>  <br/> |
|[<span data-ttu-id="ced8e-138">QueryPosition</span><span class="sxs-lookup"><span data-stu-id="ced8e-138">QueryPosition</span></span>](imapitable-queryposition.md) <br/> |<span data-ttu-id="ced8e-139">Recupera la posición actual de fila de tabla del cursor, basándose en un valor fraccionrio.</span><span class="sxs-lookup"><span data-stu-id="ced8e-139">Retrieves the current table row position of the cursor, based on a fractional value.</span></span>  <br/> |
|[<span data-ttu-id="ced8e-140">FindRow</span><span class="sxs-lookup"><span data-stu-id="ced8e-140">FindRow</span></span>](imapitable-findrow.md) <br/> |<span data-ttu-id="ced8e-141">Busca la siguiente fila de una tabla que coincide con criterios de búsqueda específicos.</span><span class="sxs-lookup"><span data-stu-id="ced8e-141">Finds the next row in a table that matches specific search criteria.</span></span>  <br/> |
|[<span data-ttu-id="ced8e-142">Restrict</span><span class="sxs-lookup"><span data-stu-id="ced8e-142">Restrict</span></span>](imapitable-restrict.md) <br/> |<span data-ttu-id="ced8e-143">Aplica un filtro a una tabla, lo que reduce el conjunto de filas a solo aquellas filas que coincidan con los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="ced8e-143">Applies a filter to a table, reducing the row set to only those rows matching the specified criteria.</span></span>  <br/> |
|[<span data-ttu-id="ced8e-144">CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="ced8e-144">CreateBookmark</span></span>](imapitable-createbookmark.md) <br/> |<span data-ttu-id="ced8e-145">Marca la posición actual de la tabla.</span><span class="sxs-lookup"><span data-stu-id="ced8e-145">Marks the table's current position.</span></span>  <br/> |
|[<span data-ttu-id="ced8e-146">FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="ced8e-146">FreeBookmark</span></span>](imapitable-freebookmark.md) <br/> |<span data-ttu-id="ced8e-147">Libera la memoria asociada a un marcador.</span><span class="sxs-lookup"><span data-stu-id="ced8e-147">Releases the memory associated with a bookmark.</span></span>  <br/> |
|[<span data-ttu-id="ced8e-148">SortTable</span><span class="sxs-lookup"><span data-stu-id="ced8e-148">SortTable</span></span>](imapitable-sorttable.md) <br/> |<span data-ttu-id="ced8e-149">Ordena las filas de la tabla según criterios de ordenación.</span><span class="sxs-lookup"><span data-stu-id="ced8e-149">Orders the rows of the table based on sort criteria.</span></span>  <br/> |
|[<span data-ttu-id="ced8e-150">QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="ced8e-150">QuerySortOrder</span></span>](imapitable-querysortorder.md) <br/> |<span data-ttu-id="ced8e-151">Recupera el criterio de ordenación actual de una tabla.</span><span class="sxs-lookup"><span data-stu-id="ced8e-151">Retrieves the current sort order for a table.</span></span>  <br/> |
|[<span data-ttu-id="ced8e-152">QueryRows</span><span class="sxs-lookup"><span data-stu-id="ced8e-152">QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="ced8e-153">Devuelve una o más filas de una tabla, comenzando en la posición actual del cursor.</span><span class="sxs-lookup"><span data-stu-id="ced8e-153">Returns one or more rows from a table, beginning at the current cursor position.</span></span>  <br/> |
|[<span data-ttu-id="ced8e-154">Anular</span><span class="sxs-lookup"><span data-stu-id="ced8e-154">Abort</span></span>](imapitable-abort.md) <br/> |<span data-ttu-id="ced8e-155">Detiene las operaciones asincrónicas actualmente en curso para la tabla.</span><span class="sxs-lookup"><span data-stu-id="ced8e-155">Stops any asynchronous operations currently in progress for the table.</span></span>  <br/> |
|[<span data-ttu-id="ced8e-156">ExpandRow</span><span class="sxs-lookup"><span data-stu-id="ced8e-156">ExpandRow</span></span>](imapitable-expandrow.md) <br/> |<span data-ttu-id="ced8e-157">Expande una categoría de tabla contrayendo y agrega las filas hoja pertenecientes a la categoría a la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="ced8e-157">Expands a collapsed table category, adding the leaf rows belonging to the category to the table view.</span></span>  <br/> |
|[<span data-ttu-id="ced8e-158">CollapseRow</span><span class="sxs-lookup"><span data-stu-id="ced8e-158">CollapseRow</span></span>](imapitable-collapserow.md) <br/> |<span data-ttu-id="ced8e-159">Contrae una categoría de tabla expandida, quitando las filas hoja pertenecientes a la categoría de la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="ced8e-159">Collapses an expanded table category, removing the leaf rows belonging to the category from the table view.</span></span>  <br/> |
|[<span data-ttu-id="ced8e-160">WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="ced8e-160">WaitForCompletion</span></span>](imapitable-waitforcompletion.md) <br/> |<span data-ttu-id="ced8e-161">Suspende el procesamiento hasta que se hayan completado una o varias operaciones asincrónicas en curso en la tabla.</span><span class="sxs-lookup"><span data-stu-id="ced8e-161">Suspends processing until one or more asynchronous operations in progress on the table have completed.</span></span>  <br/> |
|[<span data-ttu-id="ced8e-162">GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="ced8e-162">GetCollapseState</span></span>](imapitable-getcollapsestate.md) <br/> |<span data-ttu-id="ced8e-163">Devuelve los datos necesarios para volver a generar el estado contraído o expandido actual de una tabla categorizada.</span><span class="sxs-lookup"><span data-stu-id="ced8e-163">Returns the data necessary to rebuild the current collapsed or expanded state of a categorized table.</span></span>  <br/> |
|[<span data-ttu-id="ced8e-164">SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="ced8e-164">SetCollapseState</span></span>](imapitable-setcollapsestate.md) <br/> |<span data-ttu-id="ced8e-165">Vuelve a generar el estado expandido o contraído actual de una tabla categorizada con datos guardados por una llamada anterior al método **IMAPITable::GetCollapseState.**</span><span class="sxs-lookup"><span data-stu-id="ced8e-165">Rebuilds the current expanded or collapsed state of a categorized table using data that was saved by a prior call to the **IMAPITable::GetCollapseState** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ced8e-166">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ced8e-166">See also</span></span>



[<span data-ttu-id="ced8e-167">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="ced8e-167">MAPI Interfaces</span></span>](mapi-interfaces.md)

