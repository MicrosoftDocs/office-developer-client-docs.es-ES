---
title: IMAPITableGetCollapseState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetCollapseState
api_type:
- COM
ms.assetid: fd4ea496-4c83-49cd-854e-f373cc1ed2af
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 46d993060d03b8c22c2d6c083c05f023648e6642
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589668"
---
# <a name="imapitablegetcollapsestate"></a><span data-ttu-id="76fd0-103">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="76fd0-103">IMAPITable::GetCollapseState</span></span>

  
  
<span data-ttu-id="76fd0-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="76fd0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="76fd0-105">Devuelve los datos que es necesario volver a generar la actual contraído o expandido el estado de una tabla con categorías.</span><span class="sxs-lookup"><span data-stu-id="76fd0-105">Returns the data that is needed to rebuild the current collapsed or expanded state of a categorized table.</span></span>
  
```cpp
HRESULT GetCollapseState(
ULONG ulFlags,
ULONG cbInstanceKey,
LPBYTE lpbInstanceKey,
ULONG FAR * lpcbCollapseState,
LPBYTE FAR * lppbCollapseState
);
```

## <a name="parameters"></a><span data-ttu-id="76fd0-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="76fd0-106">Parameters</span></span>

 <span data-ttu-id="76fd0-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="76fd0-107">_ulFlags_</span></span>
  
> <span data-ttu-id="76fd0-108">Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="76fd0-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="76fd0-109">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="76fd0-109">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="76fd0-110">[entrada] El número de bytes de la clave de la instancia indicada por el parámetro _lpbInstanceKey_ .</span><span class="sxs-lookup"><span data-stu-id="76fd0-110">[in] The count of bytes in the instance key pointed to by the  _lpbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="76fd0-111">_lpbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="76fd0-111">_lpbInstanceKey_</span></span>
  
> <span data-ttu-id="76fd0-112">[entrada] Debe recompilar un puntero a la propiedad **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) de la fila en la que la actual, contrae o expande el estado.</span><span class="sxs-lookup"><span data-stu-id="76fd0-112">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property of the row at which the current collapsed or expanded state should be rebuilt.</span></span> <span data-ttu-id="76fd0-113">El parámetro _lpbInstanceKey_ no puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="76fd0-113">The  _lpbInstanceKey_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="76fd0-114">_lpcbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="76fd0-114">_lpcbCollapseState_</span></span>
  
> <span data-ttu-id="76fd0-115">[out] Un puntero para el recuento de estructuras indicada por el parámetro _lppbCollapseState_ .</span><span class="sxs-lookup"><span data-stu-id="76fd0-115">[out] A pointer to the count of structures pointed to by the  _lppbCollapseState_ parameter.</span></span> 
    
 <span data-ttu-id="76fd0-116">_lppbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="76fd0-116">_lppbCollapseState_</span></span>
  
> <span data-ttu-id="76fd0-117">[out] Un puntero a un puntero a estructuras que contienen datos que se describen la vista de tabla actual.</span><span class="sxs-lookup"><span data-stu-id="76fd0-117">[out] A pointer to a pointer to structures that contain data that describes the current table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="76fd0-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="76fd0-118">Return value</span></span>

<span data-ttu-id="76fd0-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="76fd0-119">S_OK</span></span> 
  
> <span data-ttu-id="76fd0-120">El estado de la tabla con categorías se guardó correctamente.</span><span class="sxs-lookup"><span data-stu-id="76fd0-120">The state for the categorized table was successfully saved.</span></span>
    
<span data-ttu-id="76fd0-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="76fd0-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="76fd0-122">Otra operación está en curso que impide que la operación de inicio.</span><span class="sxs-lookup"><span data-stu-id="76fd0-122">Another operation is in progress that prevents the operation from starting.</span></span> <span data-ttu-id="76fd0-123">Debe ser permite la operación en curso para llevar a cabo o se debe detener.</span><span class="sxs-lookup"><span data-stu-id="76fd0-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="76fd0-124">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="76fd0-124">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="76fd0-125">La tabla no admite la categorización y vistas expandida y contraída.</span><span class="sxs-lookup"><span data-stu-id="76fd0-125">The table does not support categorization and expanded and collapsed views.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="76fd0-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="76fd0-126">Remarks</span></span>

<span data-ttu-id="76fd0-127">El método **IMAPITable::GetCollapseState** funciona con el método [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md) para cambiar la vista del usuario de una tabla con categorías.</span><span class="sxs-lookup"><span data-stu-id="76fd0-127">The **IMAPITable::GetCollapseState** method works with the [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md) method to change the user's view of a categorized table.</span></span> <span data-ttu-id="76fd0-128">**GetCollapseState** guarda los datos que se necesitan para que **SetCollapseState** a usar para volver a generar las vistas de las categorías de una tabla con categorías adecuadas.</span><span class="sxs-lookup"><span data-stu-id="76fd0-128">**GetCollapseState** saves the data that is needed for **SetCollapseState** to use to rebuild the appropriate views of the categories of a categorized table.</span></span> <span data-ttu-id="76fd0-129">Proveedores de servicios de determinan los datos que se guarde.</span><span class="sxs-lookup"><span data-stu-id="76fd0-129">Service providers determine the data to be saved.</span></span> <span data-ttu-id="76fd0-130">Sin embargo, la mayoría de los proveedores de servicio implementar **GetCollapseState** guarda lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="76fd0-130">However, most service providers implementing **GetCollapseState** save the following:</span></span> 
  
- <span data-ttu-id="76fd0-131">Las claves de ordenación (estándares columnas y columnas de categoría).</span><span class="sxs-lookup"><span data-stu-id="76fd0-131">The sort keys (standard columns and category columns).</span></span>
    
- <span data-ttu-id="76fd0-132">Información acerca de la fila que representa la clave de instancia.</span><span class="sxs-lookup"><span data-stu-id="76fd0-132">Information about the row that the instance key represents.</span></span>
    
- <span data-ttu-id="76fd0-133">Información para restaurar las categorías contraídas y expandidas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="76fd0-133">Information to restore the collapsed and expanded categories of the table.</span></span>
    
<span data-ttu-id="76fd0-134">Para obtener más información acerca de las tablas ordenadas por categorías, vea [Ordenar y la categorización](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="76fd0-134">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="76fd0-135">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="76fd0-135">Notes to implementers</span></span>

<span data-ttu-id="76fd0-136">Almacenar el estado actual de todos los nodos de una tabla en el parámetro _lppbCollapseState_ .</span><span class="sxs-lookup"><span data-stu-id="76fd0-136">Store the current state of all nodes of a table in the  _lppbCollapseState_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="76fd0-137">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="76fd0-137">Notes to callers</span></span>

<span data-ttu-id="76fd0-138">Llame siempre a **GetCollapseState** antes de llamar a **SetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="76fd0-138">Always call **GetCollapseState** before you call **SetCollapseState**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="76fd0-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="76fd0-139">See also</span></span>



[<span data-ttu-id="76fd0-140">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="76fd0-140">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
  
[<span data-ttu-id="76fd0-141">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="76fd0-141">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

