---
title: ITableData IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData
api_type:
- COM
ms.assetid: ac7ae09f-ce19-45cf-8963-fad5bba75452
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 968768fe75286b93bf12e349a4845fdfaa1923e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817986"
---
# <a name="itabledata--iunknown"></a><span data-ttu-id="f4dbe-103">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f4dbe-103">ITableData : IUnknown</span></span>

  
  
<span data-ttu-id="f4dbe-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f4dbe-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f4dbe-105">Proporciona métodos de utilidad para trabajar con tablas.</span><span class="sxs-lookup"><span data-stu-id="f4dbe-105">Provides utility methods for working with tables.</span></span> <span data-ttu-id="f4dbe-106">MAPI proporciona objetos de datos de tabla u objetos que implementan **ITableData** para ayudar a los proveedores de servicios de realizar el mantenimiento de la tabla.</span><span class="sxs-lookup"><span data-stu-id="f4dbe-106">MAPI provides table data objects or objects that implement **ITableData** to help service providers perform table maintenance.</span></span> <span data-ttu-id="f4dbe-107">Para obtener un objeto de datos de tabla, proveedores de servicios de llamar a la función [CreateTable](createtable.md) .</span><span class="sxs-lookup"><span data-stu-id="f4dbe-107">To obtain a table data object, service providers call the [CreateTable](createtable.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f4dbe-108">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="f4dbe-108">Header file:</span></span>  <br/> |<span data-ttu-id="f4dbe-109">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="f4dbe-109">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f4dbe-110">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="f4dbe-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="f4dbe-111">Objetos de datos de tabla</span><span class="sxs-lookup"><span data-stu-id="f4dbe-111">Table data objects</span></span>  <br/> |
|<span data-ttu-id="f4dbe-112">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="f4dbe-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="f4dbe-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="f4dbe-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="f4dbe-114">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="f4dbe-114">Called by:</span></span>  <br/> |<span data-ttu-id="f4dbe-115">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="f4dbe-115">Service providers</span></span>  <br/> |
|<span data-ttu-id="f4dbe-116">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="f4dbe-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="f4dbe-117">IID_IMAPITableData</span><span class="sxs-lookup"><span data-stu-id="f4dbe-117">IID_IMAPITableData</span></span>  <br/> |
|<span data-ttu-id="f4dbe-118">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="f4dbe-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="f4dbe-119">LPTABLEDATA</span><span class="sxs-lookup"><span data-stu-id="f4dbe-119">LPTABLEDATA</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="f4dbe-120">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="f4dbe-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="f4dbe-121">HrGetView</span><span class="sxs-lookup"><span data-stu-id="f4dbe-121">HrGetView</span></span>](itabledata-hrgetview.md) <br/> |<span data-ttu-id="f4dbe-122">Crea una vista de tabla, la devolución de un puntero a una implementación [IMAPITable](imapitableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="f4dbe-122">Creates a table view, returning a pointer to an [IMAPITable](imapitableiunknown.md) implementation.</span></span>  <br/> |
|[<span data-ttu-id="f4dbe-123">HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="f4dbe-123">HrModifyRow</span></span>](itabledata-hrmodifyrow.md) <br/> |<span data-ttu-id="f4dbe-124">Inserta una nueva fila de tabla, posiblemente reemplazando una fila existente.</span><span class="sxs-lookup"><span data-stu-id="f4dbe-124">Inserts a new table row, possibly replacing an existing row.</span></span>  <br/> |
|[<span data-ttu-id="f4dbe-125">HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="f4dbe-125">HrDeleteRow</span></span>](itabledata-hrdeleterow.md) <br/> |<span data-ttu-id="f4dbe-126">Elimina una fila de tabla.</span><span class="sxs-lookup"><span data-stu-id="f4dbe-126">Deletes a table row.</span></span>  <br/> |
|[<span data-ttu-id="f4dbe-127">HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="f4dbe-127">HrQueryRow</span></span>](itabledata-hrqueryrow.md) <br/> |<span data-ttu-id="f4dbe-128">Recupera una fila de tabla.</span><span class="sxs-lookup"><span data-stu-id="f4dbe-128">Retrieves a table row.</span></span>  <br/> |
|[<span data-ttu-id="f4dbe-129">HrEnumRow</span><span class="sxs-lookup"><span data-stu-id="f4dbe-129">HrEnumRow</span></span>](itabledata-hrenumrow.md) <br/> |<span data-ttu-id="f4dbe-130">Recupera una fila en función de su posición en la tabla.</span><span class="sxs-lookup"><span data-stu-id="f4dbe-130">Retrieves a row based on its position in the table.</span></span>  <br/> |
|[<span data-ttu-id="f4dbe-131">HrNotify</span><span class="sxs-lookup"><span data-stu-id="f4dbe-131">HrNotify</span></span>](itabledata-hrnotify.md) <br/> |<span data-ttu-id="f4dbe-132">Envía una notificación para una fila de tabla.</span><span class="sxs-lookup"><span data-stu-id="f4dbe-132">Sends a notification for a table row.</span></span>  <br/> |
|[<span data-ttu-id="f4dbe-133">HrInsertRow</span><span class="sxs-lookup"><span data-stu-id="f4dbe-133">HrInsertRow</span></span>](itabledata-hrinsertrow.md) <br/> |<span data-ttu-id="f4dbe-134">Inserta una fila de tabla.</span><span class="sxs-lookup"><span data-stu-id="f4dbe-134">Inserts a table row.</span></span>  <br/> |
|[<span data-ttu-id="f4dbe-135">HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="f4dbe-135">HrModifyRows</span></span>](itabledata-hrmodifyrows.md) <br/> |<span data-ttu-id="f4dbe-136">Inserta varias filas de tabla, posiblemente reemplazando las filas existentes.</span><span class="sxs-lookup"><span data-stu-id="f4dbe-136">Inserts multiple table rows, possibly replacing existing rows.</span></span>  <br/> |
|[<span data-ttu-id="f4dbe-137">HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="f4dbe-137">HrDeleteRows</span></span>](itabledata-hrdeleterows.md) <br/> |<span data-ttu-id="f4dbe-138">Elimina varias filas de tabla.</span><span class="sxs-lookup"><span data-stu-id="f4dbe-138">Deletes multiple table rows.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4dbe-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f4dbe-139">Remarks</span></span>

<span data-ttu-id="f4dbe-140">La implementación de MAPI de **ITableData** funciona con tablas manteniendo todos los datos y las restricciones asociadas en la memoria, lo que apropiadas para su uso con tablas muy grandes.</span><span class="sxs-lookup"><span data-stu-id="f4dbe-140">The MAPI implementation of **ITableData** works with tables by holding all of the data and any associated restrictions in memory, making it unsuitable for use with very large tables.</span></span> <span data-ttu-id="f4dbe-141">No se admiten las restricciones de gran tamaño y operaciones complejas, como la categorización.</span><span class="sxs-lookup"><span data-stu-id="f4dbe-141">Large restrictions and complex operations such as categorization are not supported.</span></span> 
  
<span data-ttu-id="f4dbe-142">Objetos de datos de tabla identifican filas mediante el uso de una columna de índice, una propiedad que se garantiza que tiene un valor único para cada fila.</span><span class="sxs-lookup"><span data-stu-id="f4dbe-142">Table data objects identify rows by using an index column, a property that is guaranteed to have a unique value for each row.</span></span> <span data-ttu-id="f4dbe-143">La mayoría de los proveedores de servicios use la propiedad **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) como la columna de índice.</span><span class="sxs-lookup"><span data-stu-id="f4dbe-143">Most service providers use the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property as the index column.</span></span> <span data-ttu-id="f4dbe-144">Las propiedades que tienen varios valores no se puede usar como una columna de índice.</span><span class="sxs-lookup"><span data-stu-id="f4dbe-144">Properties that have multiple values cannot be used as an index column.</span></span>
  
<span data-ttu-id="f4dbe-145">Objetos de datos de tabla generan una única notificación independientemente del número de filas afectadas por un cambio o la eliminación.</span><span class="sxs-lookup"><span data-stu-id="f4dbe-145">Table data objects generate a single notification regardless of the number of rows affected by a change or deletion.</span></span> <span data-ttu-id="f4dbe-146">Si no existe una fila de destino de una operación, se agrega una fila.</span><span class="sxs-lookup"><span data-stu-id="f4dbe-146">If a target row in an operation does not exist, a row is added.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f4dbe-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4dbe-147">See also</span></span>



[<span data-ttu-id="f4dbe-148">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="f4dbe-148">MAPI Interfaces</span></span>](mapi-interfaces.md)

