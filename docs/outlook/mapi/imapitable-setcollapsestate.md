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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328836"
---
# <a name="imapitablesetcollapsestate"></a><span data-ttu-id="6aa4e-103">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="6aa4e-103">IMAPITable::SetCollapseState</span></span>

  
  
<span data-ttu-id="6aa4e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6aa4e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6aa4e-105">Vuelve a compilar el estado expandido o contraído actual de una tabla clasificada con datos que se guardaron mediante una llamada anterior al método [IMAPITable:: GetCollapseState](imapitable-getcollapsestate.md) .</span><span class="sxs-lookup"><span data-stu-id="6aa4e-105">Rebuilds the current expanded or collapsed state of a categorized table using data that was saved by a prior call to the [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) method.</span></span> 
  
```cpp
HRESULT SetCollapseState(
ULONG ulFlags,
ULONG cbCollapseState,
LPBYTE pbCollapseState,
BOOKMARK FAR * lpbkLocation
);
```

## <a name="parameters"></a><span data-ttu-id="6aa4e-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="6aa4e-106">Parameters</span></span>

 <span data-ttu-id="6aa4e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6aa4e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="6aa4e-108">Reserve debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="6aa4e-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="6aa4e-109">_cbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="6aa4e-109">_cbCollapseState_</span></span>
  
> <span data-ttu-id="6aa4e-110">a Número de bytes en la estructura a la que apunta el parámetro _pbCollapseState_ .</span><span class="sxs-lookup"><span data-stu-id="6aa4e-110">[in] Count of bytes in the structure pointed to by the  _pbCollapseState_ parameter.</span></span> 
    
 <span data-ttu-id="6aa4e-111">_pbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="6aa4e-111">_pbCollapseState_</span></span>
  
> <span data-ttu-id="6aa4e-112">a Puntero a las estructuras que contienen los datos necesarios para volver a crear la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="6aa4e-112">[in] Pointer to the structures containing the data needed to rebuild the table view.</span></span>
    
 <span data-ttu-id="6aa4e-113">_lpbkLocation_</span><span class="sxs-lookup"><span data-stu-id="6aa4e-113">_lpbkLocation_</span></span>
  
> <span data-ttu-id="6aa4e-114">contempla Puntero a un marcador que identifica la fila de la tabla en la que se debe recompilar el estado contraído o expandido.</span><span class="sxs-lookup"><span data-stu-id="6aa4e-114">[out] Pointer to a bookmark identifying the row in the table at which the collapsed or expanded state should be rebuilt.</span></span> <span data-ttu-id="6aa4e-115">Este marcador y la clave de instancia pasada en el parámetro _lpbInstanceKey_ en la llamada a [IMAPITable:: GetCollapseState](imapitable-getcollapsestate.md) identifican la misma fila.</span><span class="sxs-lookup"><span data-stu-id="6aa4e-115">This bookmark and the instance key passed in the  _lpbInstanceKey_ parameter in the call to [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) identify the same row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6aa4e-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6aa4e-116">Return value</span></span>

<span data-ttu-id="6aa4e-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="6aa4e-117">S_OK</span></span> 
  
> <span data-ttu-id="6aa4e-118">El estado de la tabla clasificada se reconstruyó correctamente.</span><span class="sxs-lookup"><span data-stu-id="6aa4e-118">The state of the categorized table was successfully rebuilt.</span></span>
    
<span data-ttu-id="6aa4e-119">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="6aa4e-119">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="6aa4e-120">Hay otra operación en curso que impide que la operación se inicie.</span><span class="sxs-lookup"><span data-stu-id="6aa4e-120">Another operation is in progress that prevents the operation from starting.</span></span> <span data-ttu-id="6aa4e-121">Debe permitirse que la operación en curso se complete o que deba detenerse.</span><span class="sxs-lookup"><span data-stu-id="6aa4e-121">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="6aa4e-122">MAPI_E_UNABLE_TO_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="6aa4e-122">MAPI_E_UNABLE_TO_COMPLETE</span></span> 
  
> <span data-ttu-id="6aa4e-123">La tabla no pudo terminar de volver a crear la vista contraída o expandida.</span><span class="sxs-lookup"><span data-stu-id="6aa4e-123">The table could not finish rebuilding the collapsed or expanded view.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6aa4e-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6aa4e-124">Remarks</span></span>

<span data-ttu-id="6aa4e-125">El método **IMAPITable:: SetCollapseState** restablece el estado expandido o contraído de la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="6aa4e-125">The **IMAPITable::SetCollapseState** method reestablishes the expanded or collapsed state of the table view.</span></span> <span data-ttu-id="6aa4e-126">**SetCollapseState** y **GetCollapseState** trabajan juntos de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="6aa4e-126">**SetCollapseState** and **GetCollapseState** work together as follows:</span></span> 
  
1. <span data-ttu-id="6aa4e-127">Cuando se va a cambiar el estado de una tabla clasificada, se llama a [IMAPITable:: GetCollapseState](imapitable-getcollapsestate.md) para guardar todos los datos pertenecientes al estado antes del cambio.</span><span class="sxs-lookup"><span data-stu-id="6aa4e-127">When the state of a categorized table is about to change, [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) is called to save all of the data pertaining to the state prior to the change.</span></span> 
    
2. <span data-ttu-id="6aa4e-128">Para restaurar la vista de la tabla a su estado guardado, se llama a **SetCollapseState** .</span><span class="sxs-lookup"><span data-stu-id="6aa4e-128">To restore the view of the table to its saved state, **SetCollapseState** is called.</span></span> <span data-ttu-id="6aa4e-129">Los datos guardados por **GetCollapseState** se pasan a **SetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="6aa4e-129">The data saved by **GetCollapseState** is passed to **SetCollapseState**.</span></span> <span data-ttu-id="6aa4e-130">**SetCollapseState** puede usar esos datos para restaurar el estado.</span><span class="sxs-lookup"><span data-stu-id="6aa4e-130">**SetCollapseState** is able to use that data to restore the state.</span></span> 
    
3. <span data-ttu-id="6aa4e-131">**SetCollapseState** devuelve como parámetro de salida un marcador que identifica la misma fila que la clave de instancia pasada como entrada a **GetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="6aa4e-131">**SetCollapseState** returns as an output parameter a bookmark that identifies the same row as the instance key passed as input to **GetCollapseState**.</span></span>
    
<span data-ttu-id="6aa4e-132">Para obtener más información acerca de las tablas clasificadas por categorías, vea [ordenar y categorización](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="6aa4e-132">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="6aa4e-133">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="6aa4e-133">Notes to implementers</span></span>

<span data-ttu-id="6aa4e-134">Usted es responsable de comprobar que el criterio de ordenación y las restricciones son exactamente iguales a los que estaban en el momento de la llamada **GetCollapseState** .</span><span class="sxs-lookup"><span data-stu-id="6aa4e-134">You are responsible for verifying that the sort order and restrictions are exactly the same as they were at the time of the **GetCollapseState** call.</span></span> <span data-ttu-id="6aa4e-135">Si se ha realizado un cambio, no se debe llamar a **SetCollapseState** porque los resultados pueden ser imprevisibles.</span><span class="sxs-lookup"><span data-stu-id="6aa4e-135">If a change has been made, **SetCollapseState** should not be called because the results can be unpredictable.</span></span> <span data-ttu-id="6aa4e-136">Esto puede ocurrir si, por ejemplo, un cliente llama a **GetCollapseState** y, a continuación, **SortTable** cambiar la clave de ordenación antes de llamar a **SetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="6aa4e-136">This can happen if, for example, a client calls **GetCollapseState** and then **SortTable** to change the sort key before calling **SetCollapseState**.</span></span> <span data-ttu-id="6aa4e-137">Para ser seguro, compruebe que los datos guardados siguen siendo válidos antes de continuar con la restauración.</span><span class="sxs-lookup"><span data-stu-id="6aa4e-137">To be safe, check that the saved data is still valid before proceeding with the restoration.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6aa4e-138">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="6aa4e-138">Notes to callers</span></span>

<span data-ttu-id="6aa4e-139">Para llamar a **SetCollapseState**, debe haber llamado previamente a **GetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="6aa4e-139">To call **SetCollapseState**, you must have previously called **GetCollapseState**.</span></span> <span data-ttu-id="6aa4e-140">El criterio de ordenación que establece las categorías debe ser el mismo para ambos métodos.</span><span class="sxs-lookup"><span data-stu-id="6aa4e-140">The sort order establishing the categories should be the same for both methods.</span></span> <span data-ttu-id="6aa4e-141">Si los criterios de ordenación son distintos, los resultados de la operación **SetCollapseState** son imprevisibles.</span><span class="sxs-lookup"><span data-stu-id="6aa4e-141">If the sort orders differ, the results of the **SetCollapseState** operation are unpredictable.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6aa4e-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="6aa4e-142">See also</span></span>



[<span data-ttu-id="6aa4e-143">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="6aa4e-143">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="6aa4e-144">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="6aa4e-144">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="6aa4e-145">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="6aa4e-145">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
  
[<span data-ttu-id="6aa4e-146">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6aa4e-146">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

