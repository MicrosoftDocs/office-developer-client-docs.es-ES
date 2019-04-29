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
ms.openlocfilehash: 97575a65cd6825e07d6f11c813beec539f99f53a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436079"
---
# <a name="imapitablegetcollapsestate"></a><span data-ttu-id="9baa3-103">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="9baa3-103">IMAPITable::GetCollapseState</span></span>

  
  
<span data-ttu-id="9baa3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9baa3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9baa3-105">Devuelve los datos necesarios para volver a generar el estado expandido o contraído actual de una tabla clasificada.</span><span class="sxs-lookup"><span data-stu-id="9baa3-105">Returns the data that is needed to rebuild the current collapsed or expanded state of a categorized table.</span></span>
  
```cpp
HRESULT GetCollapseState(
ULONG ulFlags,
ULONG cbInstanceKey,
LPBYTE lpbInstanceKey,
ULONG FAR * lpcbCollapseState,
LPBYTE FAR * lppbCollapseState
);
```

## <a name="parameters"></a><span data-ttu-id="9baa3-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="9baa3-106">Parameters</span></span>

 <span data-ttu-id="9baa3-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9baa3-107">_ulFlags_</span></span>
  
> <span data-ttu-id="9baa3-108">Reserve debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="9baa3-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="9baa3-109">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="9baa3-109">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="9baa3-110">a El recuento de bytes de la clave de instancia apuntado por el parámetro _lpbInstanceKey_ .</span><span class="sxs-lookup"><span data-stu-id="9baa3-110">[in] The count of bytes in the instance key pointed to by the  _lpbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="9baa3-111">_lpbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="9baa3-111">_lpbInstanceKey_</span></span>
  
> <span data-ttu-id="9baa3-112">a Un puntero a la propiedad **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) de la fila en la que se debe recompilar el estado expandido o contraído actual.</span><span class="sxs-lookup"><span data-stu-id="9baa3-112">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property of the row at which the current collapsed or expanded state should be rebuilt.</span></span> <span data-ttu-id="9baa3-113">El parámetro _lpbInstanceKey_ no puede ser nulo.</span><span class="sxs-lookup"><span data-stu-id="9baa3-113">The  _lpbInstanceKey_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="9baa3-114">_lpcbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="9baa3-114">_lpcbCollapseState_</span></span>
  
> <span data-ttu-id="9baa3-115">contempla Un puntero al número de estructuras señalado por el parámetro _lppbCollapseState_ .</span><span class="sxs-lookup"><span data-stu-id="9baa3-115">[out] A pointer to the count of structures pointed to by the  _lppbCollapseState_ parameter.</span></span> 
    
 <span data-ttu-id="9baa3-116">_lppbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="9baa3-116">_lppbCollapseState_</span></span>
  
> <span data-ttu-id="9baa3-117">contempla Un puntero a un puntero a estructuras que contienen datos que describen la vista de tabla actual.</span><span class="sxs-lookup"><span data-stu-id="9baa3-117">[out] A pointer to a pointer to structures that contain data that describes the current table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9baa3-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9baa3-118">Return value</span></span>

<span data-ttu-id="9baa3-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="9baa3-119">S_OK</span></span> 
  
> <span data-ttu-id="9baa3-120">El estado de la tabla clasificada se ha guardado correctamente.</span><span class="sxs-lookup"><span data-stu-id="9baa3-120">The state for the categorized table was successfully saved.</span></span>
    
<span data-ttu-id="9baa3-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="9baa3-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="9baa3-122">Hay otra operación en curso que impide que la operación se inicie.</span><span class="sxs-lookup"><span data-stu-id="9baa3-122">Another operation is in progress that prevents the operation from starting.</span></span> <span data-ttu-id="9baa3-123">Debe permitirse que la operación en curso se complete o que deba detenerse.</span><span class="sxs-lookup"><span data-stu-id="9baa3-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="9baa3-124">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="9baa3-124">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="9baa3-125">La tabla no admite la categorización y las vistas expandidas y contraídas.</span><span class="sxs-lookup"><span data-stu-id="9baa3-125">The table does not support categorization and expanded and collapsed views.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9baa3-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9baa3-126">Remarks</span></span>

<span data-ttu-id="9baa3-127">El método **IMAPITable:: GetCollapseState** funciona con el método [IMAPITable:: SetCollapseState](imapitable-setcollapsestate.md) para cambiar la vista del usuario de una tabla clasificada.</span><span class="sxs-lookup"><span data-stu-id="9baa3-127">The **IMAPITable::GetCollapseState** method works with the [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md) method to change the user's view of a categorized table.</span></span> <span data-ttu-id="9baa3-128">**GetCollapseState** guarda los datos necesarios para que **SetCollapseState** use para volver a crear las vistas adecuadas de las categorías de una tabla clasificada.</span><span class="sxs-lookup"><span data-stu-id="9baa3-128">**GetCollapseState** saves the data that is needed for **SetCollapseState** to use to rebuild the appropriate views of the categories of a categorized table.</span></span> <span data-ttu-id="9baa3-129">Los proveedores de servicios determinan los datos que se van a guardar.</span><span class="sxs-lookup"><span data-stu-id="9baa3-129">Service providers determine the data to be saved.</span></span> <span data-ttu-id="9baa3-130">Sin embargo, la mayoría de los proveedores de servicios que implementan **GetCollapseState** guardan lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9baa3-130">However, most service providers implementing **GetCollapseState** save the following:</span></span> 
  
- <span data-ttu-id="9baa3-131">Claves de ordenación (columnas estándar y columnas de categoría).</span><span class="sxs-lookup"><span data-stu-id="9baa3-131">The sort keys (standard columns and category columns).</span></span>
    
- <span data-ttu-id="9baa3-132">Información sobre la fila representada por la clave de instancia.</span><span class="sxs-lookup"><span data-stu-id="9baa3-132">Information about the row that the instance key represents.</span></span>
    
- <span data-ttu-id="9baa3-133">Información para restaurar las categorías contraídas y expandidas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="9baa3-133">Information to restore the collapsed and expanded categories of the table.</span></span>
    
<span data-ttu-id="9baa3-134">Para obtener más información acerca de las tablas clasificadas por categorías, vea [ordenar y categorización](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="9baa3-134">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="9baa3-135">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="9baa3-135">Notes to implementers</span></span>

<span data-ttu-id="9baa3-136">Almacene el estado actual de todos los nodos de una tabla en el parámetro _lppbCollapseState_ .</span><span class="sxs-lookup"><span data-stu-id="9baa3-136">Store the current state of all nodes of a table in the  _lppbCollapseState_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9baa3-137">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="9baa3-137">Notes to callers</span></span>

<span data-ttu-id="9baa3-138">Llame siempre a **GetCollapseState** antes de llamar a **SetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="9baa3-138">Always call **GetCollapseState** before you call **SetCollapseState**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9baa3-139">Ver también</span><span class="sxs-lookup"><span data-stu-id="9baa3-139">See also</span></span>



[<span data-ttu-id="9baa3-140">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="9baa3-140">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
  
[<span data-ttu-id="9baa3-141">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9baa3-141">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

