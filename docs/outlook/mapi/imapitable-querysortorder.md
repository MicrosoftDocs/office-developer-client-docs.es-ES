---
title: IMAPITableQuerySortOrder
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QuerySortOrder
api_type:
- COM
ms.assetid: 7b4ca523-0703-417c-8586-c4324c200020
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 48ca692779fb53cab386d8a18b5f0a50e11d531c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569438"
---
# <a name="imapitablequerysortorder"></a><span data-ttu-id="c6aca-103">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="c6aca-103">IMAPITable::QuerySortOrder</span></span>

  
  
<span data-ttu-id="c6aca-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c6aca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c6aca-105">Recupera el criterio de ordenación actual para una tabla.</span><span class="sxs-lookup"><span data-stu-id="c6aca-105">Retrieves the current sort order for a table.</span></span>
  
```cpp
HRESULT QuerySortOrder(
LPSSortOrderSet FAR * lppSortCriteria
);
```

## <a name="parameters"></a><span data-ttu-id="c6aca-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c6aca-106">Parameters</span></span>

 <span data-ttu-id="c6aca-107">_lppSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="c6aca-107">_lppSortCriteria_</span></span>
  
> <span data-ttu-id="c6aca-108">[out] Puntero a un puntero a la estructura de [SSortOrderSet](ssortorderset.md) que contiene el criterio de ordenación actual.</span><span class="sxs-lookup"><span data-stu-id="c6aca-108">[out] Pointer to a pointer to the [SSortOrderSet](ssortorderset.md) structure holding the current sort order.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c6aca-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c6aca-109">Return value</span></span>

<span data-ttu-id="c6aca-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="c6aca-110">S_OK</span></span> 
  
> <span data-ttu-id="c6aca-111">El criterio de ordenación actual se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="c6aca-111">The current sort order was successfully returned.</span></span>
    
<span data-ttu-id="c6aca-112">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="c6aca-112">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="c6aca-113">Otra operación está en curso que impide que la operación de recuperación de ordenación orden de inicio.</span><span class="sxs-lookup"><span data-stu-id="c6aca-113">Another operation is in progress that prevents the sort order retrieval operation from starting.</span></span> <span data-ttu-id="c6aca-114">Debe ser permite la operación en curso para llevar a cabo o se debe detener.</span><span class="sxs-lookup"><span data-stu-id="c6aca-114">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c6aca-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c6aca-115">Remarks</span></span>

<span data-ttu-id="c6aca-116">El método **IMAPITable::QuerySortOrder** recupera el criterio de ordenación actual para una tabla.</span><span class="sxs-lookup"><span data-stu-id="c6aca-116">The **IMAPITable::QuerySortOrder** method retrieves the current sort order for a table.</span></span> <span data-ttu-id="c6aca-117">Criterios de ordenación se describen con una estructura [SSortOrderSet](ssortorderset.md) .</span><span class="sxs-lookup"><span data-stu-id="c6aca-117">Sort orders are described with an [SSortOrderSet](ssortorderset.md) structure.</span></span> 
  
- <span data-ttu-id="c6aca-118">El miembro **cSorts** de la estructura **SSortOrderSet** se puede establecer en cero si:</span><span class="sxs-lookup"><span data-stu-id="c6aca-118">The **cSorts** member of the **SSortOrderSet** structure can be set to zero if:</span></span> 
    
- <span data-ttu-id="c6aca-119">La tabla no está ordenada.</span><span class="sxs-lookup"><span data-stu-id="c6aca-119">The table is unsorted.</span></span>
    
- <span data-ttu-id="c6aca-120">No hay ninguna información acerca de cómo se ordena la tabla.</span><span class="sxs-lookup"><span data-stu-id="c6aca-120">There is no information about how the table is sorted.</span></span>
    
- <span data-ttu-id="c6aca-121">La estructura de **SSortOrderSet** no es adecuada para describir el criterio de ordenación.</span><span class="sxs-lookup"><span data-stu-id="c6aca-121">The **SSortOrderSet** structure is not appropriate for describing the sort order.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="c6aca-122">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="c6aca-122">Notes to implementers</span></span>

<span data-ttu-id="c6aca-123">Si se realiza una llamada al método [SortTable](imapitable-sorttable.md) con una estructura **SSortOrderSet** que contiene cero columnas en el criterio de ordenación, quite el criterio de ordenación actual y aplicar el orden de forma predeterminada, si hay alguno.</span><span class="sxs-lookup"><span data-stu-id="c6aca-123">If a call is made to your [IMAPITable::SortTable](imapitable-sorttable.md) method with an **SSortOrderSet** structure containing zero columns in the sort key, remove the current sort order and apply the default order, if there is one.</span></span> <span data-ttu-id="c6aca-124">En llamadas posteriores a **QuerySortOrder**, puede elegir si se debe devolver cero o más columnas de la clave de ordenación.</span><span class="sxs-lookup"><span data-stu-id="c6aca-124">In subsequent calls to **QuerySortOrder**, you can choose whether to return zero or more columns for the sort key.</span></span> <span data-ttu-id="c6aca-125">Puede devolver más columnas que se encuentran en la vista actual.</span><span class="sxs-lookup"><span data-stu-id="c6aca-125">You can return more columns than are in the present view.</span></span>
  
<span data-ttu-id="c6aca-126">Para obtener más información acerca de la ordenación, vea [Ordenar y la categorización](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="c6aca-126">For more information about sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c6aca-127">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="c6aca-127">See also</span></span>



[<span data-ttu-id="c6aca-128">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="c6aca-128">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="c6aca-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="c6aca-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="c6aca-130">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="c6aca-130">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="c6aca-131">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c6aca-131">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

