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
ms.openlocfilehash: 61991972fdf8674a9ffd2b790e26c7fa669df357
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328864"
---
# <a name="imapitablequerysortorder"></a><span data-ttu-id="9cf02-103">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="9cf02-103">IMAPITable::QuerySortOrder</span></span>

  
  
<span data-ttu-id="9cf02-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9cf02-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9cf02-105">Recupera el criterio de ordenación actual de una tabla.</span><span class="sxs-lookup"><span data-stu-id="9cf02-105">Retrieves the current sort order for a table.</span></span>
  
```cpp
HRESULT QuerySortOrder(
LPSSortOrderSet FAR * lppSortCriteria
);
```

## <a name="parameters"></a><span data-ttu-id="9cf02-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="9cf02-106">Parameters</span></span>

 <span data-ttu-id="9cf02-107">_lppSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="9cf02-107">_lppSortCriteria_</span></span>
  
> <span data-ttu-id="9cf02-108">contempla Puntero a un puntero a la estructura [SSortOrderSet](ssortorderset.md) que contiene el criterio de ordenación actual.</span><span class="sxs-lookup"><span data-stu-id="9cf02-108">[out] Pointer to a pointer to the [SSortOrderSet](ssortorderset.md) structure holding the current sort order.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9cf02-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9cf02-109">Return value</span></span>

<span data-ttu-id="9cf02-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="9cf02-110">S_OK</span></span> 
  
> <span data-ttu-id="9cf02-111">El criterio de ordenación actual se ha devuelto correctamente.</span><span class="sxs-lookup"><span data-stu-id="9cf02-111">The current sort order was successfully returned.</span></span>
    
<span data-ttu-id="9cf02-112">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="9cf02-112">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="9cf02-113">Hay otra operación en curso que evita que se inicie la operación de recuperación del criterio de ordenación.</span><span class="sxs-lookup"><span data-stu-id="9cf02-113">Another operation is in progress that prevents the sort order retrieval operation from starting.</span></span> <span data-ttu-id="9cf02-114">Debe permitirse que la operación en curso se complete o que deba detenerse.</span><span class="sxs-lookup"><span data-stu-id="9cf02-114">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9cf02-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9cf02-115">Remarks</span></span>

<span data-ttu-id="9cf02-116">El método **IMAPITable:: QuerySortOrder** recupera el criterio de ordenación actual de una tabla.</span><span class="sxs-lookup"><span data-stu-id="9cf02-116">The **IMAPITable::QuerySortOrder** method retrieves the current sort order for a table.</span></span> <span data-ttu-id="9cf02-117">Los criterios de ordenación se describen con una estructura [SSortOrderSet](ssortorderset.md) .</span><span class="sxs-lookup"><span data-stu-id="9cf02-117">Sort orders are described with an [SSortOrderSet](ssortorderset.md) structure.</span></span> 
  
- <span data-ttu-id="9cf02-118">El miembro **cSorts** de la estructura **SSortOrderSet** se puede establecer en cero si:</span><span class="sxs-lookup"><span data-stu-id="9cf02-118">The **cSorts** member of the **SSortOrderSet** structure can be set to zero if:</span></span> 
    
- <span data-ttu-id="9cf02-119">La tabla no está ordenada.</span><span class="sxs-lookup"><span data-stu-id="9cf02-119">The table is unsorted.</span></span>
    
- <span data-ttu-id="9cf02-120">No hay información sobre cómo se ordena la tabla.</span><span class="sxs-lookup"><span data-stu-id="9cf02-120">There is no information about how the table is sorted.</span></span>
    
- <span data-ttu-id="9cf02-121">La estructura **SSortOrderSet** no es adecuada para describir el criterio de ordenación.</span><span class="sxs-lookup"><span data-stu-id="9cf02-121">The **SSortOrderSet** structure is not appropriate for describing the sort order.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="9cf02-122">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="9cf02-122">Notes to implementers</span></span>

<span data-ttu-id="9cf02-123">Si se realiza una llamada al método [IMAPITable:: SortTable](imapitable-sorttable.md) con una estructura **SSortOrderSet** que contiene cero columnas en el criterio de ordenación, quite el criterio de ordenación actual y aplique el orden predeterminado, si hay alguno.</span><span class="sxs-lookup"><span data-stu-id="9cf02-123">If a call is made to your [IMAPITable::SortTable](imapitable-sorttable.md) method with an **SSortOrderSet** structure containing zero columns in the sort key, remove the current sort order and apply the default order, if there is one.</span></span> <span data-ttu-id="9cf02-124">En llamadas posteriores a **QuerySortOrder**, puede elegir si desea devolver cero o más columnas para el criterio de ordenación.</span><span class="sxs-lookup"><span data-stu-id="9cf02-124">In subsequent calls to **QuerySortOrder**, you can choose whether to return zero or more columns for the sort key.</span></span> <span data-ttu-id="9cf02-125">Puede devolver más columnas que las que hay en la vista actual.</span><span class="sxs-lookup"><span data-stu-id="9cf02-125">You can return more columns than are in the present view.</span></span>
  
<span data-ttu-id="9cf02-126">Para obtener más información acerca de la ordenación, vea [ordenar y categorizar](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="9cf02-126">For more information about sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9cf02-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="9cf02-127">See also</span></span>



[<span data-ttu-id="9cf02-128">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="9cf02-128">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="9cf02-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="9cf02-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="9cf02-130">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="9cf02-130">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="9cf02-131">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9cf02-131">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

