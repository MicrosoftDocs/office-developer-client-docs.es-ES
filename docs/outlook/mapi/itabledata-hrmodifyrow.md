---
title: ITableDataHrModifyRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrModifyRow
api_type:
- COM
ms.assetid: 9e255b3e-dd17-4528-ba4e-c3a1aef32b04
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5ef210aedc884e5c09eca6335199e2ef284b901c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574835"
---
# <a name="itabledatahrmodifyrow"></a><span data-ttu-id="43d2a-103">ITableData::HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="43d2a-103">ITableData::HrModifyRow</span></span>

  
  
<span data-ttu-id="43d2a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43d2a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43d2a-105">Inserta una nueva fila de tabla, posiblemente reemplazando una fila existente.</span><span class="sxs-lookup"><span data-stu-id="43d2a-105">Inserts a new table row, possibly replacing an existing row.</span></span>
  
```cpp
HRESULT HrModifyRow(
  LPSRow lpSRow
);
```

## <a name="parameters"></a><span data-ttu-id="43d2a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="43d2a-106">Parameters</span></span>

 <span data-ttu-id="43d2a-107">_lpSRow_</span><span class="sxs-lookup"><span data-stu-id="43d2a-107">_lpSRow_</span></span>
  
> <span data-ttu-id="43d2a-108">[entrada] Un puntero a una estructura [SRow](srow.md) que describe la fila que se va a agregar o reemplazar una fila existente.</span><span class="sxs-lookup"><span data-stu-id="43d2a-108">[in] A pointer to an [SRow](srow.md) structure that describes the row to be added or to replace an existing row.</span></span> <span data-ttu-id="43d2a-109">Una de las estructuras de valor de la propiedad indicadas por el miembro **lpProps** de la estructura **SRow** debe contener la columna de índice, el mismo valor que se especificó en el parámetro _ulPropTagIndexColumn_ en la llamada a la [CreateTable ](createtable.md)(función).</span><span class="sxs-lookup"><span data-stu-id="43d2a-109">One of the property value structures pointed to by the **lpProps** member of the **SRow** structure should contain the index column, the same value that was specified in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="43d2a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="43d2a-110">Return value</span></span>

<span data-ttu-id="43d2a-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="43d2a-111">S_OK</span></span> 
  
> <span data-ttu-id="43d2a-112">La fila se inserta o se modificó correctamente.</span><span class="sxs-lookup"><span data-stu-id="43d2a-112">The row was successfully inserted or modified.</span></span>
    
<span data-ttu-id="43d2a-113">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="43d2a-113">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="43d2a-114">La fila se pasan en no tiene una columna de índice.</span><span class="sxs-lookup"><span data-stu-id="43d2a-114">The passed-in row does not have an index column.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="43d2a-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="43d2a-115">Remarks</span></span>

<span data-ttu-id="43d2a-116">El método **ITableData::HrModifyRow** inserta la fila descrita por la estructura de **SRow** indicada por el parámetro _lpSRow_ .</span><span class="sxs-lookup"><span data-stu-id="43d2a-116">The **ITableData::HrModifyRow** method inserts the row described by the **SRow** structure pointed to by the  _lpSRow_ parameter.</span></span> <span data-ttu-id="43d2a-117">Si una fila que tiene el mismo valor para su columna de índice que la fila que señala _lpSRow_ ya existe en la tabla, se reemplaza la fila existente.</span><span class="sxs-lookup"><span data-stu-id="43d2a-117">If a row that has the same value for its index column as the row that  _lpSRow_ points to already exists in the table, the existing row is replaced.</span></span> <span data-ttu-id="43d2a-118">Si no hay ninguna fila que coincida con el incluido en la estructura de **SRow** , **HrModifyRow** agrega la fila al final de la tabla.</span><span class="sxs-lookup"><span data-stu-id="43d2a-118">If no row exists that matches the one included in the **SRow** structure, **HrModifyRow** adds the row to the end of the table.</span></span> 
  
<span data-ttu-id="43d2a-119">Todas las vistas de la tabla se modifican para incluir la fila indicada por _lpSRow_.</span><span class="sxs-lookup"><span data-stu-id="43d2a-119">All views of the table are modified to include the row pointed to by  _lpSRow_.</span></span> <span data-ttu-id="43d2a-120">Sin embargo, si una vista tiene una restricción en el lugar que excluye la fila, pueden no ser visible para el usuario.</span><span class="sxs-lookup"><span data-stu-id="43d2a-120">However, if a view has a restriction in place that excludes the row, it may not be visible to the user.</span></span> 
  
<span data-ttu-id="43d2a-121">Las columnas de la fila que señala _lpSRow_ no es necesario estar en el mismo orden que las columnas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="43d2a-121">The columns in the row pointed to by  _lpSRow_ do not have to be in the same order as the columns in the table.</span></span> <span data-ttu-id="43d2a-122">También puede incluir el autor de la llamada como propiedades de las columnas que no están actualmente en la tabla.</span><span class="sxs-lookup"><span data-stu-id="43d2a-122">The caller can also include as columns properties that are not currently in the table.</span></span> <span data-ttu-id="43d2a-123">Para las vistas existentes, **HrModifyRow** realiza estas nuevas columnas disponibles, pero no se incluye en el conjunto actual de la columna.</span><span class="sxs-lookup"><span data-stu-id="43d2a-123">For existing views, **HrModifyRow** makes these new columns available but does not include them in the current column set.</span></span> <span data-ttu-id="43d2a-124">Para las futuras vistas, **HrModifyRow** incluye las nuevas columnas en el conjunto de columnas.</span><span class="sxs-lookup"><span data-stu-id="43d2a-124">For future views, **HrModifyRow** includes the new columns in the column set.</span></span> 
  
<span data-ttu-id="43d2a-125">Una vez que **HrModifyRow** se agrega la fila, se envían a todos los clientes o proveedores de servicios que tienen una vista de la tabla y que ha llamado [IMAPITable::Advise](imapitable-advise.md) (método) de la tabla para registrar para las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="43d2a-125">After **HrModifyRow** adds the row, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="43d2a-126">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="43d2a-126">See also</span></span>



[<span data-ttu-id="43d2a-127">SRow</span><span class="sxs-lookup"><span data-stu-id="43d2a-127">SRow</span></span>](srow.md)
  
[<span data-ttu-id="43d2a-128">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="43d2a-128">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="43d2a-129">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="43d2a-129">ITableData : IUnknown</span></span>](itabledataiunknown.md)

