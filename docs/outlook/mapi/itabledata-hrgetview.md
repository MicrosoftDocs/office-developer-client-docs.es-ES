---
title: ITableDataHrGetView
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrGetView
api_type:
- COM
ms.assetid: 0e2a47be-497b-4031-87ce-60b2635e25f7
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 375a0f1d39b09b7ad453120f20752e00ffda0e15
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278718"
---
# <a name="itabledatahrgetview"></a><span data-ttu-id="a8d9d-103">ITableData::HrGetView</span><span class="sxs-lookup"><span data-stu-id="a8d9d-103">ITableData::HrGetView</span></span>

  
  
<span data-ttu-id="a8d9d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8d9d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8d9d-105">Crea una vista de tabla y devuelve un puntero a una [implementación imapitable.](imapitableiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="a8d9d-105">Creates a table view, returning a pointer to an [IMAPITable](imapitableiunknown.md) implementation.</span></span> 
  
```cpp
HRESULT HrGetView(
  LPSSortOrderSet lpSSortOrderSet,
  CALLERRELEASE FAR * lpfCallerRelease,
  ULONG_PTR ulCallerData,
  LPMAPITABLE FAR * lppMAPITable
);
```

## <a name="parameters"></a><span data-ttu-id="a8d9d-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="a8d9d-106">Parameters</span></span>

 <span data-ttu-id="a8d9d-107">_lpSSortOrderSet_</span><span class="sxs-lookup"><span data-stu-id="a8d9d-107">_lpSSortOrderSet_</span></span>
  
> <span data-ttu-id="a8d9d-108">[in] Puntero a una estructura de criterio de ordenación que describe el criterio de ordenación de la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="a8d9d-108">[in] A pointer to a sort order structure that describes the sort order for the table view.</span></span> <span data-ttu-id="a8d9d-109">Si se pasa NULL en el  _parámetro lpSSortOrderSet,_ la vista no se ordena.</span><span class="sxs-lookup"><span data-stu-id="a8d9d-109">If NULL is passed in the  _lpSSortOrderSet_ parameter, the view is not sorted.</span></span> 
    
 <span data-ttu-id="a8d9d-110">_lpfCallerRelease_</span><span class="sxs-lookup"><span data-stu-id="a8d9d-110">_lpfCallerRelease_</span></span>
  
> <span data-ttu-id="a8d9d-111">[in] Puntero a una función de devolución de llamada basada en el prototipo [CALLERRELEASE](callerrelease.md) al que LLAMA MAPI cuando libera la vista.</span><span class="sxs-lookup"><span data-stu-id="a8d9d-111">[in] A pointer to a callback function based on the [CALLERRELEASE](callerrelease.md) prototype that MAPI calls when it releases the view.</span></span> <span data-ttu-id="a8d9d-112">Si se pasa NULL en el  _parámetro lpfCallerRelease,_ no se llama a ninguna función al liberar la vista.</span><span class="sxs-lookup"><span data-stu-id="a8d9d-112">If NULL is passed in the  _lpfCallerRelease_ parameter, no function is called on release of the view.</span></span> 
    
 <span data-ttu-id="a8d9d-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="a8d9d-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="a8d9d-114">[in] Los datos que se deben guardar con la nueva vista y pasar a la función de devolución de llamada a la que  _apunta lpfCallerRelease_.</span><span class="sxs-lookup"><span data-stu-id="a8d9d-114">[in] The data that must be saved with the new view and passed to the callback function pointed to by  _lpfCallerRelease_.</span></span>
    
 <span data-ttu-id="a8d9d-115">_lppMAPITable_</span><span class="sxs-lookup"><span data-stu-id="a8d9d-115">_lppMAPITable_</span></span>
  
> <span data-ttu-id="a8d9d-116">[salida] Puntero a un puntero a la vista recién creada.</span><span class="sxs-lookup"><span data-stu-id="a8d9d-116">[out] A pointer to a pointer to the newly created view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a8d9d-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8d9d-117">Return value</span></span>

<span data-ttu-id="a8d9d-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="a8d9d-118">S_OK</span></span> 
  
> <span data-ttu-id="a8d9d-119">La vista se creó correctamente.</span><span class="sxs-lookup"><span data-stu-id="a8d9d-119">The view was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a8d9d-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a8d9d-120">Remarks</span></span>

<span data-ttu-id="a8d9d-121">El **método ITableData::HrGetView** crea una vista de solo lectura de los datos de la tabla, ordenada en el orden indicado por el parámetro _lpSSortOrderSet._</span><span class="sxs-lookup"><span data-stu-id="a8d9d-121">The **ITableData::HrGetView** method creates a read-only view of the data in the table, sorted in the order pointed to by the  _lpSSortOrderSet_ parameter.</span></span> <span data-ttu-id="a8d9d-122">El cursor se coloca al principio de la primera fila de la vista.</span><span class="sxs-lookup"><span data-stu-id="a8d9d-122">The cursor is placed at the beginning of the first row in the view.</span></span> <span data-ttu-id="a8d9d-123">Se devuelve una implementación de interfaz **IMAPITable** para obtener acceso a la vista.</span><span class="sxs-lookup"><span data-stu-id="a8d9d-123">An **IMAPITable** interface implementation for accessing the view is returned.</span></span> 
  
<span data-ttu-id="a8d9d-124">Los proveedores de servicios **llaman a HrGetView** cuando necesitan dar a un cliente acceso a una tabla.</span><span class="sxs-lookup"><span data-stu-id="a8d9d-124">Service providers call **HrGetView** when they need to give a client access to a table.</span></span> <span data-ttu-id="a8d9d-125">**HrGetView crea** la vista y devuelve el **puntero IMAPITable.**</span><span class="sxs-lookup"><span data-stu-id="a8d9d-125">**HrGetView** creates the view and returns the **IMAPITable** pointer.</span></span> <span data-ttu-id="a8d9d-126">A su vez, los proveedores de servicios pasan el puntero al cliente.</span><span class="sxs-lookup"><span data-stu-id="a8d9d-126">Service providers in turn pass the pointer on to the client.</span></span> <span data-ttu-id="a8d9d-127">Cuando el cliente termina de usar la tabla y llama a su método [IUnknown::Release,](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) **HrGetView** llama a la función de devolución de llamada señalada por el parámetro _lpfCallerRelease._</span><span class="sxs-lookup"><span data-stu-id="a8d9d-127">When the client is finished using the table and calls its [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method, **HrGetView** calls the callback function pointed to by the  _lpfCallerRelease_ parameter.</span></span> 
  
<span data-ttu-id="a8d9d-128">Si un proveedor de servicios necesita devolver a un cliente una vista que tenga un conjunto de columnas personalizado o una restricción, el proveedor puede llamar a los métodos [IMAPITable::SetColumns](imapitable-setcolumns.md) e [IMAPITable::Restrict](imapitable-restrict.md) de la vista antes de permitir el acceso del cliente.</span><span class="sxs-lookup"><span data-stu-id="a8d9d-128">If a service provider needs to return to a client a view that has a customized column set or a restriction, the provider can call the view's [IMAPITable::SetColumns](imapitable-setcolumns.md) and [IMAPITable::Restrict](imapitable-restrict.md) methods before allowing the client access.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a8d9d-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8d9d-129">See also</span></span>



[<span data-ttu-id="a8d9d-130">CALLERRELEASE</span><span class="sxs-lookup"><span data-stu-id="a8d9d-130">CALLERRELEASE</span></span>](callerrelease.md)
  
[<span data-ttu-id="a8d9d-131">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a8d9d-131">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="a8d9d-132">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="a8d9d-132">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="a8d9d-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a8d9d-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

