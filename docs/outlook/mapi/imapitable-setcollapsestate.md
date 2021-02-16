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
ms.openlocfilehash: 7351457dc5b72cfc4a7ef9f91e9d33a80ca98c39
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414070"
---
# <a name="imapitablesetcollapsestate"></a><span data-ttu-id="3bd56-103">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="3bd56-103">IMAPITable::SetCollapseState</span></span>

  
  
<span data-ttu-id="3bd56-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3bd56-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3bd56-105">Vuelve a generar el estado expandido o contraído actual de una tabla categorizada mediante datos guardados por una llamada anterior al método [IMAPITable::GetCollapseState.](imapitable-getcollapsestate.md)</span><span class="sxs-lookup"><span data-stu-id="3bd56-105">Rebuilds the current expanded or collapsed state of a categorized table using data that was saved by a prior call to the [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) method.</span></span> 
  
```cpp
HRESULT SetCollapseState(
ULONG ulFlags,
ULONG cbCollapseState,
LPBYTE pbCollapseState,
BOOKMARK FAR * lpbkLocation
);
```

## <a name="parameters"></a><span data-ttu-id="3bd56-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3bd56-106">Parameters</span></span>

 <span data-ttu-id="3bd56-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3bd56-107">_ulFlags_</span></span>
  
> <span data-ttu-id="3bd56-108">Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="3bd56-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="3bd56-109">_cbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="3bd56-109">_cbCollapseState_</span></span>
  
> <span data-ttu-id="3bd56-110">[entrada] Número de bytes en la estructura a la que apunta el _parámetro pbCollapseState._</span><span class="sxs-lookup"><span data-stu-id="3bd56-110">[in] Count of bytes in the structure pointed to by the  _pbCollapseState_ parameter.</span></span> 
    
 <span data-ttu-id="3bd56-111">_pbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="3bd56-111">_pbCollapseState_</span></span>
  
> <span data-ttu-id="3bd56-112">[entrada] Puntero a las estructuras que contienen los datos necesarios para volver a generar la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="3bd56-112">[in] Pointer to the structures containing the data needed to rebuild the table view.</span></span>
    
 <span data-ttu-id="3bd56-113">_lpbkLocation_</span><span class="sxs-lookup"><span data-stu-id="3bd56-113">_lpbkLocation_</span></span>
  
> <span data-ttu-id="3bd56-114">[salida] Puntero a un marcador que identifica la fila de la tabla en la que se debe volver a generar el estado contraído o expandido.</span><span class="sxs-lookup"><span data-stu-id="3bd56-114">[out] Pointer to a bookmark identifying the row in the table at which the collapsed or expanded state should be rebuilt.</span></span> <span data-ttu-id="3bd56-115">Este marcador y la clave de instancia pasados en el parámetro  _lpbInstanceKey_ en la llamada a [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) identifican la misma fila.</span><span class="sxs-lookup"><span data-stu-id="3bd56-115">This bookmark and the instance key passed in the  _lpbInstanceKey_ parameter in the call to [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) identify the same row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3bd56-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3bd56-116">Return value</span></span>

<span data-ttu-id="3bd56-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="3bd56-117">S_OK</span></span> 
  
> <span data-ttu-id="3bd56-118">El estado de la tabla categorizada se recompiló correctamente.</span><span class="sxs-lookup"><span data-stu-id="3bd56-118">The state of the categorized table was successfully rebuilt.</span></span>
    
<span data-ttu-id="3bd56-119">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="3bd56-119">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="3bd56-120">Hay otra operación en curso que impide que se inicie la operación.</span><span class="sxs-lookup"><span data-stu-id="3bd56-120">Another operation is in progress that prevents the operation from starting.</span></span> <span data-ttu-id="3bd56-121">La operación en curso debe poder completarse o debe detenerse.</span><span class="sxs-lookup"><span data-stu-id="3bd56-121">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="3bd56-122">MAPI_E_UNABLE_TO_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="3bd56-122">MAPI_E_UNABLE_TO_COMPLETE</span></span> 
  
> <span data-ttu-id="3bd56-123">La tabla no pudo terminar de recompilar la vista contraida o expandida.</span><span class="sxs-lookup"><span data-stu-id="3bd56-123">The table could not finish rebuilding the collapsed or expanded view.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3bd56-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3bd56-124">Remarks</span></span>

<span data-ttu-id="3bd56-125">El **método IMAPITable::SetCollapseState** restablece el estado expandido o contraído de la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="3bd56-125">The **IMAPITable::SetCollapseState** method reestablishes the expanded or collapsed state of the table view.</span></span> <span data-ttu-id="3bd56-126">**SetCollapseState** y **GetCollapseState** funcionan juntos de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="3bd56-126">**SetCollapseState** and **GetCollapseState** work together as follows:</span></span> 
  
1. <span data-ttu-id="3bd56-127">Cuando el estado de una tabla categorizada está a punto de cambiar, se llama a [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) para guardar todos los datos relacionados con el estado anterior al cambio.</span><span class="sxs-lookup"><span data-stu-id="3bd56-127">When the state of a categorized table is about to change, [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) is called to save all of the data pertaining to the state prior to the change.</span></span> 
    
2. <span data-ttu-id="3bd56-128">Para restaurar la vista de la tabla a su estado guardado, se llama **a SetCollapseState.**</span><span class="sxs-lookup"><span data-stu-id="3bd56-128">To restore the view of the table to its saved state, **SetCollapseState** is called.</span></span> <span data-ttu-id="3bd56-129">Los datos guardados **por GetCollapseState** se pasan **a SetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="3bd56-129">The data saved by **GetCollapseState** is passed to **SetCollapseState**.</span></span> <span data-ttu-id="3bd56-130">**SetCollapseState** es capaz de usar estos datos para restaurar el estado.</span><span class="sxs-lookup"><span data-stu-id="3bd56-130">**SetCollapseState** is able to use that data to restore the state.</span></span> 
    
3. <span data-ttu-id="3bd56-131">**SetCollapseState devuelve** como parámetro de salida un marcador que identifica la misma fila que la clave de instancia pasada como entrada a **GetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="3bd56-131">**SetCollapseState** returns as an output parameter a bookmark that identifies the same row as the instance key passed as input to **GetCollapseState**.</span></span>
    
<span data-ttu-id="3bd56-132">Para obtener más información acerca de las tablas categorizadas, vea [Ordenar y categorizar.](sorting-and-categorization.md)</span><span class="sxs-lookup"><span data-stu-id="3bd56-132">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3bd56-133">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="3bd56-133">Notes to implementers</span></span>

<span data-ttu-id="3bd56-134">Usted es responsable de comprobar que el criterio de ordenación y las restricciones son exactamente iguales que en el momento de la llamada **GetCollapseState.**</span><span class="sxs-lookup"><span data-stu-id="3bd56-134">You are responsible for verifying that the sort order and restrictions are exactly the same as they were at the time of the **GetCollapseState** call.</span></span> <span data-ttu-id="3bd56-135">Si se ha realizado un cambio, no se debe llamar a **SetCollapseState** porque los resultados pueden ser impredecibles.</span><span class="sxs-lookup"><span data-stu-id="3bd56-135">If a change has been made, **SetCollapseState** should not be called because the results can be unpredictable.</span></span> <span data-ttu-id="3bd56-136">Esto puede suceder si, por ejemplo, un cliente llama a **GetCollapseState** y, a continuación, **a SortTable** para cambiar la clave de ordenación antes de llamar a **SetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="3bd56-136">This can happen if, for example, a client calls **GetCollapseState** and then **SortTable** to change the sort key before calling **SetCollapseState**.</span></span> <span data-ttu-id="3bd56-137">Para que sea seguro, compruebe que los datos guardados siguen siendo válidos antes de continuar con la restauración.</span><span class="sxs-lookup"><span data-stu-id="3bd56-137">To be safe, check that the saved data is still valid before proceeding with the restoration.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3bd56-138">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="3bd56-138">Notes to callers</span></span>

<span data-ttu-id="3bd56-139">Para llamar **a SetCollapseState**, debe haber llamado previamente **a GetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="3bd56-139">To call **SetCollapseState**, you must have previously called **GetCollapseState**.</span></span> <span data-ttu-id="3bd56-140">El criterio de ordenación que establece las categorías debe ser el mismo para ambos métodos.</span><span class="sxs-lookup"><span data-stu-id="3bd56-140">The sort order establishing the categories should be the same for both methods.</span></span> <span data-ttu-id="3bd56-141">Si el criterio de ordenación difiere, los resultados de **la operación SetCollapseState** son impredecibles.</span><span class="sxs-lookup"><span data-stu-id="3bd56-141">If the sort orders differ, the results of the **SetCollapseState** operation are unpredictable.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3bd56-142">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3bd56-142">See also</span></span>



[<span data-ttu-id="3bd56-143">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="3bd56-143">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="3bd56-144">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="3bd56-144">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="3bd56-145">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="3bd56-145">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
  
[<span data-ttu-id="3bd56-146">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3bd56-146">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

