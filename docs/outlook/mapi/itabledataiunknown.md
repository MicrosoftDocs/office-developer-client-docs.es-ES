---
title: IUnknown ITableData
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
ms.openlocfilehash: 3992bea899239ee5975505dec366490d6bbe1698
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430598"
---
# <a name="itabledata--iunknown"></a><span data-ttu-id="cca59-103">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cca59-103">ITableData : IUnknown</span></span>

  
  
<span data-ttu-id="cca59-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cca59-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cca59-105">Proporciona métodos de utilidades para trabajar con tablas.</span><span class="sxs-lookup"><span data-stu-id="cca59-105">Provides utility methods for working with tables.</span></span> <span data-ttu-id="cca59-106">MAPI proporciona objetos de datos de tabla u objetos que implementan **ITableData** para ayudar a los proveedores de servicios a realizar el mantenimiento de tablas.</span><span class="sxs-lookup"><span data-stu-id="cca59-106">MAPI provides table data objects or objects that implement **ITableData** to help service providers perform table maintenance.</span></span> <span data-ttu-id="cca59-107">Para obtener un objeto de datos de tabla, los proveedores de servicios llaman a la función [createTable](createtable.md) .</span><span class="sxs-lookup"><span data-stu-id="cca59-107">To obtain a table data object, service providers call the [CreateTable](createtable.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cca59-108">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="cca59-108">Header file:</span></span>  <br/> |<span data-ttu-id="cca59-109">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="cca59-109">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="cca59-110">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="cca59-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="cca59-111">Objetos de datos de tabla</span><span class="sxs-lookup"><span data-stu-id="cca59-111">Table data objects</span></span>  <br/> |
|<span data-ttu-id="cca59-112">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="cca59-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="cca59-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="cca59-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="cca59-114">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="cca59-114">Called by:</span></span>  <br/> |<span data-ttu-id="cca59-115">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="cca59-115">Service providers</span></span>  <br/> |
|<span data-ttu-id="cca59-116">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="cca59-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="cca59-117">IID_IMAPITableData</span><span class="sxs-lookup"><span data-stu-id="cca59-117">IID_IMAPITableData</span></span>  <br/> |
|<span data-ttu-id="cca59-118">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="cca59-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="cca59-119">LPTABLEDATA</span><span class="sxs-lookup"><span data-stu-id="cca59-119">LPTABLEDATA</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="cca59-120">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="cca59-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="cca59-121">HrGetView</span><span class="sxs-lookup"><span data-stu-id="cca59-121">HrGetView</span></span>](itabledata-hrgetview.md) <br/> |<span data-ttu-id="cca59-122">Crea una vista de tabla y devuelve un puntero a una implementación de [IMAPITable](imapitableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="cca59-122">Creates a table view, returning a pointer to an [IMAPITable](imapitableiunknown.md) implementation.</span></span>  <br/> |
|[<span data-ttu-id="cca59-123">HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="cca59-123">HrModifyRow</span></span>](itabledata-hrmodifyrow.md) <br/> |<span data-ttu-id="cca59-124">Inserta una nueva fila de tabla, posiblemente reemplazando una fila existente.</span><span class="sxs-lookup"><span data-stu-id="cca59-124">Inserts a new table row, possibly replacing an existing row.</span></span>  <br/> |
|[<span data-ttu-id="cca59-125">HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="cca59-125">HrDeleteRow</span></span>](itabledata-hrdeleterow.md) <br/> |<span data-ttu-id="cca59-126">Elimina una fila de tabla.</span><span class="sxs-lookup"><span data-stu-id="cca59-126">Deletes a table row.</span></span>  <br/> |
|[<span data-ttu-id="cca59-127">HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="cca59-127">HrQueryRow</span></span>](itabledata-hrqueryrow.md) <br/> |<span data-ttu-id="cca59-128">Recupera una fila de tabla.</span><span class="sxs-lookup"><span data-stu-id="cca59-128">Retrieves a table row.</span></span>  <br/> |
|[<span data-ttu-id="cca59-129">HrEnumRow</span><span class="sxs-lookup"><span data-stu-id="cca59-129">HrEnumRow</span></span>](itabledata-hrenumrow.md) <br/> |<span data-ttu-id="cca59-130">Recupera una fila basada en su posición en la tabla.</span><span class="sxs-lookup"><span data-stu-id="cca59-130">Retrieves a row based on its position in the table.</span></span>  <br/> |
|[<span data-ttu-id="cca59-131">HrNotify</span><span class="sxs-lookup"><span data-stu-id="cca59-131">HrNotify</span></span>](itabledata-hrnotify.md) <br/> |<span data-ttu-id="cca59-132">Envía una notificación para una fila de tabla.</span><span class="sxs-lookup"><span data-stu-id="cca59-132">Sends a notification for a table row.</span></span>  <br/> |
|[<span data-ttu-id="cca59-133">HrInsertRow</span><span class="sxs-lookup"><span data-stu-id="cca59-133">HrInsertRow</span></span>](itabledata-hrinsertrow.md) <br/> |<span data-ttu-id="cca59-134">Inserta una fila de tabla.</span><span class="sxs-lookup"><span data-stu-id="cca59-134">Inserts a table row.</span></span>  <br/> |
|[<span data-ttu-id="cca59-135">HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="cca59-135">HrModifyRows</span></span>](itabledata-hrmodifyrows.md) <br/> |<span data-ttu-id="cca59-136">Inserta varias filas de tabla, posiblemente reemplazando las filas existentes.</span><span class="sxs-lookup"><span data-stu-id="cca59-136">Inserts multiple table rows, possibly replacing existing rows.</span></span>  <br/> |
|[<span data-ttu-id="cca59-137">HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="cca59-137">HrDeleteRows</span></span>](itabledata-hrdeleterows.md) <br/> |<span data-ttu-id="cca59-138">Elimina varias filas de tabla.</span><span class="sxs-lookup"><span data-stu-id="cca59-138">Deletes multiple table rows.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cca59-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cca59-139">Remarks</span></span>

<span data-ttu-id="cca59-140">La implementación de MAPI de **ITableData** trabaja con tablas mediante la retención de todos los datos y las restricciones asociadas en la memoria, lo que hace que no sea adecuado para su uso con tablas de gran tamaño.</span><span class="sxs-lookup"><span data-stu-id="cca59-140">The MAPI implementation of **ITableData** works with tables by holding all of the data and any associated restrictions in memory, making it unsuitable for use with very large tables.</span></span> <span data-ttu-id="cca59-141">No se admiten restricciones y operaciones complejas de gran tamaño, como la categorización.</span><span class="sxs-lookup"><span data-stu-id="cca59-141">Large restrictions and complex operations such as categorization are not supported.</span></span> 
  
<span data-ttu-id="cca59-142">Los objetos de datos de tabla identifican las filas mediante una columna de índice, una propiedad que se garantiza que tendrá un valor único para cada fila.</span><span class="sxs-lookup"><span data-stu-id="cca59-142">Table data objects identify rows by using an index column, a property that is guaranteed to have a unique value for each row.</span></span> <span data-ttu-id="cca59-143">La mayoría de los proveedores de servicios usan la propiedad **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) como columna de índice.</span><span class="sxs-lookup"><span data-stu-id="cca59-143">Most service providers use the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property as the index column.</span></span> <span data-ttu-id="cca59-144">Las propiedades que tienen varios valores no se pueden usar como columna de índice.</span><span class="sxs-lookup"><span data-stu-id="cca59-144">Properties that have multiple values cannot be used as an index column.</span></span>
  
<span data-ttu-id="cca59-145">Los objetos de datos de tabla generan una sola notificación independientemente del número de filas afectadas por un cambio o la eliminación.</span><span class="sxs-lookup"><span data-stu-id="cca59-145">Table data objects generate a single notification regardless of the number of rows affected by a change or deletion.</span></span> <span data-ttu-id="cca59-146">Si no existe una fila de destino en una operación, se agrega una fila.</span><span class="sxs-lookup"><span data-stu-id="cca59-146">If a target row in an operation does not exist, a row is added.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cca59-147">Ver también</span><span class="sxs-lookup"><span data-stu-id="cca59-147">See also</span></span>



[<span data-ttu-id="cca59-148">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="cca59-148">MAPI Interfaces</span></span>](mapi-interfaces.md)

