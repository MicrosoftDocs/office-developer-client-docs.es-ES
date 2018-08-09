---
title: IMAPITableSetCollapseState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SetCollapseState
api_type:
- COM
ms.assetid: 31325e8f-1cf9-49b2-8118-953996b0037f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 252b6d6c7ff74acd5f0b288af48ff2901c2330ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817618"
---
# <a name="imapitablesetcollapsestate"></a><span data-ttu-id="b2986-103">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="b2986-103">IMAPITable::SetCollapseState</span></span>

  
  
<span data-ttu-id="b2986-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b2986-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b2986-105">Vuelve a crear el estado actual de expandidos o contraído de una tabla con categorías utilizando los datos que se guardan por una llamada anterior al método [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) .</span><span class="sxs-lookup"><span data-stu-id="b2986-105">Rebuilds the current expanded or collapsed state of a categorized table using data that was saved by a prior call to the [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) method.</span></span> 
  
```cpp
HRESULT SetCollapseState(
ULONG ulFlags,
ULONG cbCollapseState,
LPBYTE pbCollapseState,
BOOKMARK FAR * lpbkLocation
);
```

## <a name="parameters"></a><span data-ttu-id="b2986-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="b2986-106">Parameters</span></span>

 <span data-ttu-id="b2986-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b2986-107">_ulFlags_</span></span>
  
> <span data-ttu-id="b2986-108">Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b2986-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="b2986-109">_cbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="b2986-109">_cbCollapseState_</span></span>
  
> <span data-ttu-id="b2986-110">[entrada] Recuento de bytes de la estructura que señala el parámetro _pbCollapseState_ .</span><span class="sxs-lookup"><span data-stu-id="b2986-110">[in] Count of bytes in the structure pointed to by the  _pbCollapseState_ parameter.</span></span> 
    
 <span data-ttu-id="b2986-111">_pbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="b2986-111">_pbCollapseState_</span></span>
  
> <span data-ttu-id="b2986-112">[entrada] Puntero a las estructuras que contiene los datos necesarios para volver a generar la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="b2986-112">[in] Pointer to the structures containing the data needed to rebuild the table view.</span></span>
    
 <span data-ttu-id="b2986-113">_lpbkLocation_</span><span class="sxs-lookup"><span data-stu-id="b2986-113">_lpbkLocation_</span></span>
  
> <span data-ttu-id="b2986-114">[out] Puntero a un marcador que identifica la fila de la tabla a la que debe recompilar el estado contraído o expandido.</span><span class="sxs-lookup"><span data-stu-id="b2986-114">[out] Pointer to a bookmark identifying the row in the table at which the collapsed or expanded state should be rebuilt.</span></span> <span data-ttu-id="b2986-115">Este marcador y la clave de instancia que se pasa en el parámetro _lpbInstanceKey_ en la llamada a [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) identifican la misma fila.</span><span class="sxs-lookup"><span data-stu-id="b2986-115">This bookmark and the instance key passed in the  _lpbInstanceKey_ parameter in the call to [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) identify the same row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b2986-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b2986-116">Return value</span></span>

<span data-ttu-id="b2986-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="b2986-117">S_OK</span></span> 
  
> <span data-ttu-id="b2986-118">El estado de la tabla con categorías volvió a generar correctamente.</span><span class="sxs-lookup"><span data-stu-id="b2986-118">The state of the categorized table was successfully rebuilt.</span></span>
    
<span data-ttu-id="b2986-119">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="b2986-119">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="b2986-120">Otra operación está en curso que impide que la operación de inicio.</span><span class="sxs-lookup"><span data-stu-id="b2986-120">Another operation is in progress that prevents the operation from starting.</span></span> <span data-ttu-id="b2986-121">Debe ser permite la operación en curso para llevar a cabo o se debe detener.</span><span class="sxs-lookup"><span data-stu-id="b2986-121">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="b2986-122">MAPI_E_UNABLE_TO_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="b2986-122">MAPI_E_UNABLE_TO_COMPLETE</span></span> 
  
> <span data-ttu-id="b2986-123">La tabla no puede terminar de volver a generar la vista contraída o expandida.</span><span class="sxs-lookup"><span data-stu-id="b2986-123">The table could not finish rebuilding the collapsed or expanded view.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b2986-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b2986-124">Remarks</span></span>

<span data-ttu-id="b2986-125">El método **IMAPITable::SetCollapseState** restablece el estado expandido o contraído de la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="b2986-125">The **IMAPITable::SetCollapseState** method reestablishes the expanded or collapsed state of the table view.</span></span> <span data-ttu-id="b2986-126">**SetCollapseState** y **GetCollapseState** trabajan juntos como sigue:</span><span class="sxs-lookup"><span data-stu-id="b2986-126">**SetCollapseState** and **GetCollapseState** work together as follows:</span></span> 
  
1. <span data-ttu-id="b2986-127">Cuando el estado de una tabla con categorías se va a cambiar, [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) se llama para guardar todos los datos relacionados con el estado antes de realizar el cambio.</span><span class="sxs-lookup"><span data-stu-id="b2986-127">When the state of a categorized table is about to change, [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) is called to save all of the data pertaining to the state prior to the change.</span></span> 
    
2. <span data-ttu-id="b2986-128">Para restaurar la vista de la tabla a su estado guardado, se denomina **SetCollapseState** .</span><span class="sxs-lookup"><span data-stu-id="b2986-128">To restore the view of the table to its saved state, **SetCollapseState** is called.</span></span> <span data-ttu-id="b2986-129">Los datos guardados por **GetCollapseState** se pasan al **SetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="b2986-129">The data saved by **GetCollapseState** is passed to **SetCollapseState**.</span></span> <span data-ttu-id="b2986-130">**SetCollapseState** es capaz de utilizar esos datos para restaurar el estado.</span><span class="sxs-lookup"><span data-stu-id="b2986-130">**SetCollapseState** is able to use that data to restore the state.</span></span> 
    
3. <span data-ttu-id="b2986-131">**SetCollapseState** devuelve como un parámetro de salida de un marcador que identifica la misma fila que la clave de la instancia que se pasa como entrada en **GetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="b2986-131">**SetCollapseState** returns as an output parameter a bookmark that identifies the same row as the instance key passed as input to **GetCollapseState**.</span></span>
    
<span data-ttu-id="b2986-132">Para obtener más información acerca de las tablas ordenadas por categorías, vea [Ordenar y la categorización](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="b2986-132">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b2986-133">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="b2986-133">Notes to implementers</span></span>

<span data-ttu-id="b2986-134">Usted es responsable de comprobar que el criterio de ordenación y restricciones son exactamente los mismos tal como se administraban en el momento de la llamada **GetCollapseState** .</span><span class="sxs-lookup"><span data-stu-id="b2986-134">You are responsible for verifying that the sort order and restrictions are exactly the same as they were at the time of the **GetCollapseState** call.</span></span> <span data-ttu-id="b2986-135">Si se ha realizado un cambio, no debe llamarse **SetCollapseState** debido a que los resultados pueden ser impredecibles.</span><span class="sxs-lookup"><span data-stu-id="b2986-135">If a change has been made, **SetCollapseState** should not be called because the results can be unpredictable.</span></span> <span data-ttu-id="b2986-136">Esto puede ocurrir si, por ejemplo, un cliente llama a **GetCollapseState** y, a continuación, **SortTable** para cambiar el criterio de ordenación antes de llamar a **SetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="b2986-136">This can happen if, for example, a client calls **GetCollapseState** and then **SortTable** to change the sort key before calling **SetCollapseState**.</span></span> <span data-ttu-id="b2986-137">Para estar seguro, compruebe que los datos guardados todavía están válidos antes de continuar con la restauración.</span><span class="sxs-lookup"><span data-stu-id="b2986-137">To be safe, check that the saved data is still valid before proceeding with the restoration.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b2986-138">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="b2986-138">Notes to callers</span></span>

<span data-ttu-id="b2986-139">Para llamar a **SetCollapseState**, debe haber llamado anteriormente **GetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="b2986-139">To call **SetCollapseState**, you must have previously called **GetCollapseState**.</span></span> <span data-ttu-id="b2986-140">El establecimiento de las categorías de criterio de ordenación debe ser el mismo para ambos métodos.</span><span class="sxs-lookup"><span data-stu-id="b2986-140">The sort order establishing the categories should be the same for both methods.</span></span> <span data-ttu-id="b2986-141">Si difieren de los criterios de ordenación, los resultados de la operación de **SetCollapseState** son imprevisibles.</span><span class="sxs-lookup"><span data-stu-id="b2986-141">If the sort orders differ, the results of the **SetCollapseState** operation are unpredictable.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b2986-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="b2986-142">See also</span></span>



[<span data-ttu-id="b2986-143">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="b2986-143">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="b2986-144">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="b2986-144">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="b2986-145">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="b2986-145">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
  
[<span data-ttu-id="b2986-146">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b2986-146">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

