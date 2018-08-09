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
ms.openlocfilehash: a913f2f3a72a365ec7d5078eccf31c4212ca83a5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817976"
---
# <a name="itabledatahrgetview"></a><span data-ttu-id="ca945-103">ITableData::HrGetView</span><span class="sxs-lookup"><span data-stu-id="ca945-103">ITableData::HrGetView</span></span>

  
  
<span data-ttu-id="ca945-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ca945-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ca945-105">Crea una vista de tabla, la devolución de un puntero a una implementación [IMAPITable](imapitableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="ca945-105">Creates a table view, returning a pointer to an [IMAPITable](imapitableiunknown.md) implementation.</span></span> 
  
```cpp
HRESULT HrGetView(
  LPSSortOrderSet lpSSortOrderSet,
  CALLERRELEASE FAR * lpfCallerRelease,
  ULONG_PTR ulCallerData,
  LPMAPITABLE FAR * lppMAPITable
);
```

## <a name="parameters"></a><span data-ttu-id="ca945-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ca945-106">Parameters</span></span>

 <span data-ttu-id="ca945-107">_lpSSortOrderSet_</span><span class="sxs-lookup"><span data-stu-id="ca945-107">_lpSSortOrderSet_</span></span>
  
> <span data-ttu-id="ca945-108">[entrada] Un puntero a una estructura de criterio de ordenación que describe el criterio de ordenación para la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="ca945-108">[in] A pointer to a sort order structure that describes the sort order for the table view.</span></span> <span data-ttu-id="ca945-109">Si se pasa NULL en el parámetro _lpSSortOrderSet_ , no se ordena la vista.</span><span class="sxs-lookup"><span data-stu-id="ca945-109">If NULL is passed in the  _lpSSortOrderSet_ parameter, the view is not sorted.</span></span> 
    
 <span data-ttu-id="ca945-110">_lpfCallerRelease_</span><span class="sxs-lookup"><span data-stu-id="ca945-110">_lpfCallerRelease_</span></span>
  
> <span data-ttu-id="ca945-111">[entrada] Un puntero a una función de devolución de llamada según el prototipo [CALLERRELEASE](callerrelease.md) que llama MAPI cuando suelta la vista.</span><span class="sxs-lookup"><span data-stu-id="ca945-111">[in] A pointer to a callback function based on the [CALLERRELEASE](callerrelease.md) prototype that MAPI calls when it releases the view.</span></span> <span data-ttu-id="ca945-112">Si se pasa NULL en el parámetro _lpfCallerRelease_ , ninguna función se llama en la versión de la vista.</span><span class="sxs-lookup"><span data-stu-id="ca945-112">If NULL is passed in the  _lpfCallerRelease_ parameter, no function is called on release of the view.</span></span> 
    
 <span data-ttu-id="ca945-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="ca945-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="ca945-114">[entrada] Los datos que se deben guardar con la nueva vista y se pasan a la función de devolución de llamada que señala _lpfCallerRelease_.</span><span class="sxs-lookup"><span data-stu-id="ca945-114">[in] The data that must be saved with the new view and passed to the callback function pointed to by  _lpfCallerRelease_.</span></span>
    
 <span data-ttu-id="ca945-115">_lppMAPITable_</span><span class="sxs-lookup"><span data-stu-id="ca945-115">_lppMAPITable_</span></span>
  
> <span data-ttu-id="ca945-116">[out] Un puntero a un puntero a la vista recién creada.</span><span class="sxs-lookup"><span data-stu-id="ca945-116">[out] A pointer to a pointer to the newly created view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ca945-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ca945-117">Return value</span></span>

<span data-ttu-id="ca945-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="ca945-118">S_OK</span></span> 
  
> <span data-ttu-id="ca945-119">La vista se ha creado correctamente.</span><span class="sxs-lookup"><span data-stu-id="ca945-119">The view was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ca945-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ca945-120">Remarks</span></span>

<span data-ttu-id="ca945-121">El método **ITableData::HrGetView** crea una vista de solo lectura de los datos en la tabla, se ordenan en el orden que apunta el parámetro _lpSSortOrderSet_ .</span><span class="sxs-lookup"><span data-stu-id="ca945-121">The **ITableData::HrGetView** method creates a read-only view of the data in the table, sorted in the order pointed to by the  _lpSSortOrderSet_ parameter.</span></span> <span data-ttu-id="ca945-122">Se coloca el cursor al principio de la primera fila en la vista.</span><span class="sxs-lookup"><span data-stu-id="ca945-122">The cursor is placed at the beginning of the first row in the view.</span></span> <span data-ttu-id="ca945-123">Se devuelve una implementación de interfaz **IMAPITable** para obtener acceso a la vista.</span><span class="sxs-lookup"><span data-stu-id="ca945-123">An **IMAPITable** interface implementation for accessing the view is returned.</span></span> 
  
<span data-ttu-id="ca945-124">Proveedores de servicios de llamada **HrGetView** cuando sea necesario proporcionar un acceso de cliente a una tabla.</span><span class="sxs-lookup"><span data-stu-id="ca945-124">Service providers call **HrGetView** when they need to give a client access to a table.</span></span> <span data-ttu-id="ca945-125">**HrGetView** crea la vista y devuelve el puntero **IMAPITable** .</span><span class="sxs-lookup"><span data-stu-id="ca945-125">**HrGetView** creates the view and returns the **IMAPITable** pointer.</span></span> <span data-ttu-id="ca945-126">Proveedores de servicios a su vez pasan el puntero de la sesión en el cliente.</span><span class="sxs-lookup"><span data-stu-id="ca945-126">Service providers in turn pass the pointer on to the client.</span></span> <span data-ttu-id="ca945-127">Cuando el cliente haya terminado de usar la tabla y llama a su método [IUnknown:: Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) , **HrGetView** llama a la función de devolución de llamada indicada por el parámetro _lpfCallerRelease_ .</span><span class="sxs-lookup"><span data-stu-id="ca945-127">When the client is finished using the table and calls its [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method, **HrGetView** calls the callback function pointed to by the  _lpfCallerRelease_ parameter.</span></span> 
  
<span data-ttu-id="ca945-128">Si necesita un proveedor de servicios para volver a un cliente de una vista que tenga una columna personalizada o una restricción, el proveedor puede llamar a los métodos la vista [IMAPITable::SetColumns](imapitable-setcolumns.md) e [IMAPITable:: Restrict](imapitable-restrict.md) antes de permitir el acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="ca945-128">If a service provider needs to return to a client a view that has a customized column set or a restriction, the provider can call the view's [IMAPITable::SetColumns](imapitable-setcolumns.md) and [IMAPITable::Restrict](imapitable-restrict.md) methods before allowing the client access.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ca945-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="ca945-129">See also</span></span>



[<span data-ttu-id="ca945-130">CALLERRELEASE</span><span class="sxs-lookup"><span data-stu-id="ca945-130">CALLERRELEASE</span></span>](callerrelease.md)
  
[<span data-ttu-id="ca945-131">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ca945-131">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="ca945-132">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="ca945-132">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="ca945-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ca945-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

