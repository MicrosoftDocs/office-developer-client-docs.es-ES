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
# <a name="imapitablegetcollapsestate"></a><span data-ttu-id="58ce8-103">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="58ce8-103">IMAPITable::GetCollapseState</span></span>

  
  
<span data-ttu-id="58ce8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58ce8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58ce8-105">Devuelve los datos necesarios para volver a generar el estado contraído o expandido actual de una tabla categorizada.</span><span class="sxs-lookup"><span data-stu-id="58ce8-105">Returns the data that is needed to rebuild the current collapsed or expanded state of a categorized table.</span></span>
  
```cpp
HRESULT GetCollapseState(
ULONG ulFlags,
ULONG cbInstanceKey,
LPBYTE lpbInstanceKey,
ULONG FAR * lpcbCollapseState,
LPBYTE FAR * lppbCollapseState
);
```

## <a name="parameters"></a><span data-ttu-id="58ce8-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="58ce8-106">Parameters</span></span>

 <span data-ttu-id="58ce8-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="58ce8-107">_ulFlags_</span></span>
  
> <span data-ttu-id="58ce8-108">Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="58ce8-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="58ce8-109">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="58ce8-109">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="58ce8-110">[in] Recuento de bytes en la clave de instancia a la que apunta el _parámetro lpbInstanceKey._</span><span class="sxs-lookup"><span data-stu-id="58ce8-110">[in] The count of bytes in the instance key pointed to by the  _lpbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="58ce8-111">_lpbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="58ce8-111">_lpbInstanceKey_</span></span>
  
> <span data-ttu-id="58ce8-112">[in] Puntero a la **propiedad PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) de la fila en la que se debe volver a generar el estado contraído o expandido actual.</span><span class="sxs-lookup"><span data-stu-id="58ce8-112">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property of the row at which the current collapsed or expanded state should be rebuilt.</span></span> <span data-ttu-id="58ce8-113">El  _parámetro lpbInstanceKey_ no puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="58ce8-113">The  _lpbInstanceKey_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="58ce8-114">_lpcbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="58ce8-114">_lpcbCollapseState_</span></span>
  
> <span data-ttu-id="58ce8-115">[salida] Puntero al recuento de estructuras apuntadas por el _parámetro lppbCollapseState._</span><span class="sxs-lookup"><span data-stu-id="58ce8-115">[out] A pointer to the count of structures pointed to by the  _lppbCollapseState_ parameter.</span></span> 
    
 <span data-ttu-id="58ce8-116">_lppbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="58ce8-116">_lppbCollapseState_</span></span>
  
> <span data-ttu-id="58ce8-117">[salida] Puntero a un puntero a estructuras que contienen datos que describen la vista de tabla actual.</span><span class="sxs-lookup"><span data-stu-id="58ce8-117">[out] A pointer to a pointer to structures that contain data that describes the current table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="58ce8-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="58ce8-118">Return value</span></span>

<span data-ttu-id="58ce8-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="58ce8-119">S_OK</span></span> 
  
> <span data-ttu-id="58ce8-120">El estado de la tabla categorizada se guardó correctamente.</span><span class="sxs-lookup"><span data-stu-id="58ce8-120">The state for the categorized table was successfully saved.</span></span>
    
<span data-ttu-id="58ce8-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="58ce8-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="58ce8-122">Hay otra operación en curso que impide que se inicie la operación.</span><span class="sxs-lookup"><span data-stu-id="58ce8-122">Another operation is in progress that prevents the operation from starting.</span></span> <span data-ttu-id="58ce8-123">Debe permitirse completar la operación en curso o detenerse.</span><span class="sxs-lookup"><span data-stu-id="58ce8-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="58ce8-124">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="58ce8-124">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="58ce8-125">La tabla no admite categorización y vistas expandida y contraida.</span><span class="sxs-lookup"><span data-stu-id="58ce8-125">The table does not support categorization and expanded and collapsed views.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="58ce8-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="58ce8-126">Remarks</span></span>

<span data-ttu-id="58ce8-127">El **método IMAPITable::GetCollapseState** funciona con el método [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md) para cambiar la vista del usuario de una tabla categorizada.</span><span class="sxs-lookup"><span data-stu-id="58ce8-127">The **IMAPITable::GetCollapseState** method works with the [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md) method to change the user's view of a categorized table.</span></span> <span data-ttu-id="58ce8-128">**GetCollapseState** guarda los datos necesarios para que **SetCollapseState** lo use para volver a generar las vistas adecuadas de las categorías de una tabla categorizada.</span><span class="sxs-lookup"><span data-stu-id="58ce8-128">**GetCollapseState** saves the data that is needed for **SetCollapseState** to use to rebuild the appropriate views of the categories of a categorized table.</span></span> <span data-ttu-id="58ce8-129">Los proveedores de servicios determinan los datos que se guardarán.</span><span class="sxs-lookup"><span data-stu-id="58ce8-129">Service providers determine the data to be saved.</span></span> <span data-ttu-id="58ce8-130">Sin embargo, la mayoría de los proveedores de servicios que **implementan GetCollapseState** guarda lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="58ce8-130">However, most service providers implementing **GetCollapseState** save the following:</span></span> 
  
- <span data-ttu-id="58ce8-131">Las claves de ordenación (columnas estándar y columnas de categoría).</span><span class="sxs-lookup"><span data-stu-id="58ce8-131">The sort keys (standard columns and category columns).</span></span>
    
- <span data-ttu-id="58ce8-132">Información sobre la fila que representa la clave de instancia.</span><span class="sxs-lookup"><span data-stu-id="58ce8-132">Information about the row that the instance key represents.</span></span>
    
- <span data-ttu-id="58ce8-133">Información para restaurar las categorías contraídos y expandido de la tabla.</span><span class="sxs-lookup"><span data-stu-id="58ce8-133">Information to restore the collapsed and expanded categories of the table.</span></span>
    
<span data-ttu-id="58ce8-134">Para obtener más información acerca de las tablas categorizadas, vea [Sorting and Categorization](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="58ce8-134">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="58ce8-135">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="58ce8-135">Notes to implementers</span></span>

<span data-ttu-id="58ce8-136">Almacene el estado actual de todos los nodos de una tabla en el _parámetro lppbCollapseState._</span><span class="sxs-lookup"><span data-stu-id="58ce8-136">Store the current state of all nodes of a table in the  _lppbCollapseState_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="58ce8-137">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="58ce8-137">Notes to callers</span></span>

<span data-ttu-id="58ce8-138">Llame siempre **a GetCollapseState antes** de llamar a **SetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="58ce8-138">Always call **GetCollapseState** before you call **SetCollapseState**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="58ce8-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="58ce8-139">See also</span></span>



[<span data-ttu-id="58ce8-140">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="58ce8-140">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
  
[<span data-ttu-id="58ce8-141">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="58ce8-141">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

