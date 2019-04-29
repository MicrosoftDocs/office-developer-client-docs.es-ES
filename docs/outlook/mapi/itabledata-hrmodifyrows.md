---
title: ITableDataHrModifyRows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrModifyRows
api_type:
- COM
ms.assetid: d295c896-9882-4d6f-9689-5cf40db208c0
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d0074dd006fda6d44252011d0b979169e0c3d4cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405362"
---
# <a name="itabledatahrmodifyrows"></a><span data-ttu-id="124e0-103">ITableData::HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="124e0-103">ITableData::HrModifyRows</span></span>

  
  
<span data-ttu-id="124e0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="124e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="124e0-105">Inserta varias filas de tabla, posiblemente reemplazando las filas existentes.</span><span class="sxs-lookup"><span data-stu-id="124e0-105">Inserts multiple table rows, possibly replacing existing rows.</span></span>
  
```cpp
HRESULT HrModifyRows(
  ULONG ulFlags,
  LPSRowSet lpSRowSet
);
```

## <a name="parameters"></a><span data-ttu-id="124e0-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="124e0-106">Parameters</span></span>

 <span data-ttu-id="124e0-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="124e0-107">_ulFlags_</span></span>
  
> <span data-ttu-id="124e0-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="124e0-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="124e0-109">_lpSRowSet_</span><span class="sxs-lookup"><span data-stu-id="124e0-109">_lpSRowSet_</span></span>
  
> <span data-ttu-id="124e0-110">a Un puntero a una estructura [SRowSet](srowset.md) que contiene el conjunto de filas que se va a agregar, reemplazando las filas existentes si es necesario.</span><span class="sxs-lookup"><span data-stu-id="124e0-110">[in] A pointer to an [SRowSet](srowset.md) structure that contains the set of rows to be added, replacing existing rows if necessary.</span></span> <span data-ttu-id="124e0-111">Una de las estructuras de valores de propiedad a la que apunta el miembro **lpProps** de cada estructura [SRow](srow.md) en el conjunto de filas debe contener la columna de índice, el mismo valor que se especificó en el parámetro _ulPropTagIndexColumn_ en la llamada al [método Función CreateTable](createtable.md) .</span><span class="sxs-lookup"><span data-stu-id="124e0-111">One of the property value structures pointed to by the **lpProps** member of each [SRow](srow.md) structure in the row set should contain the index column, the same value that was specified in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="124e0-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="124e0-112">Return value</span></span>

<span data-ttu-id="124e0-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="124e0-113">S_OK</span></span> 
  
> <span data-ttu-id="124e0-114">Las filas se insertaron o modificaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="124e0-114">The rows were successfully inserted or modified.</span></span>
    
<span data-ttu-id="124e0-115">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="124e0-115">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="124e0-116">Una o varias de las filas que se han pasado no tienen una columna de índice.</span><span class="sxs-lookup"><span data-stu-id="124e0-116">One or more of the passed-in rows does not have an index column.</span></span> <span data-ttu-id="124e0-117">Si se devuelve este error, no se cambia ninguna fila.</span><span class="sxs-lookup"><span data-stu-id="124e0-117">If this error is returned, no rows are changed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="124e0-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="124e0-118">Remarks</span></span>

<span data-ttu-id="124e0-119">El método **ITableData:: HrModifyRows** inserta las filas descritas por la estructura [SRowSet](srowset.md) a la que apunta el parámetro _lpSRowSet_ .</span><span class="sxs-lookup"><span data-stu-id="124e0-119">The **ITableData::HrModifyRows** method inserts the rows described by the [SRowSet](srowset.md) structure pointed to by the  _lpSRowSet_ parameter.</span></span> <span data-ttu-id="124e0-120">Si el valor de la columna de índice de una fila en el conjunto de filas coincide con el valor de una fila existente en la tabla, se reemplaza la fila existente.</span><span class="sxs-lookup"><span data-stu-id="124e0-120">If the index column value of a row in the row set matches the value for an existing row in the table, the existing row is replaced.</span></span> <span data-ttu-id="124e0-121">Si no existe ninguna fila que coincida con la que se incluye en la estructura **SRowSet** , **HrModifyRows** agrega la fila al final de la tabla.</span><span class="sxs-lookup"><span data-stu-id="124e0-121">If no row exists that matches the one included in the **SRowSet** structure, **HrModifyRows** adds the row to the end of the table.</span></span> 
  
<span data-ttu-id="124e0-122">Se modifican todas las vistas de la tabla para que incluyan las filas a las que apunta _lpSRowSet_.</span><span class="sxs-lookup"><span data-stu-id="124e0-122">All views of the table are modified to include the rows pointed to by  _lpSRowSet_.</span></span> <span data-ttu-id="124e0-123">Sin embargo, si una vista tiene una restricción que excluye una fila, es posible que no esté visible para el usuario.</span><span class="sxs-lookup"><span data-stu-id="124e0-123">However, if a view has a restriction in place that excludes a row, it may not be visible to the user.</span></span> 
  
<span data-ttu-id="124e0-124">Las columnas de las filas a las que apunta _lpSRowSet_ no tienen que estar en el mismo orden que las columnas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="124e0-124">The columns in the rows pointed to by  _lpSRowSet_ do not have to be in the same order as the columns in the table.</span></span> <span data-ttu-id="124e0-125">El autor de la llamada también puede incluir como propiedades de columnas que no se encuentran actualmente en la tabla.</span><span class="sxs-lookup"><span data-stu-id="124e0-125">The caller can also include as columns properties that are not currently in the table.</span></span> <span data-ttu-id="124e0-126">Para las vistas existentes, **HrModifyRows** hace que estas nuevas columnas estén disponibles, pero no las incluye en el conjunto de columnas actual.</span><span class="sxs-lookup"><span data-stu-id="124e0-126">For existing views, **HrModifyRows** makes these new columns available but does not include them in the current column set.</span></span> <span data-ttu-id="124e0-127">Para vistas futuras, **HrModifyRows** incluye las nuevas columnas en el conjunto de columnas.</span><span class="sxs-lookup"><span data-stu-id="124e0-127">For future views, **HrModifyRows** includes the new columns in the column set.</span></span> 
  
<span data-ttu-id="124e0-128">Después de que **HrModifyRows** haya agregado las filas, las notificaciones se envían a todos los clientes o proveedores de servicios que tienen una vista de la tabla y que han llamado al método [IMAPITable:: Advise](imapitable-advise.md) para registrarse para las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="124e0-128">After **HrModifyRows** has added the rows, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> <span data-ttu-id="124e0-129">MAPI envía notificaciones TABLE_ROW_ADDED o TABLE_ROW_MODIFIED para cada fila, hasta ocho filas.</span><span class="sxs-lookup"><span data-stu-id="124e0-129">MAPI sends TABLE_ROW_ADDED or TABLE_ROW_MODIFIED notifications for each row, up to eight rows.</span></span> <span data-ttu-id="124e0-130">Si más de ocho filas se ven afectadas por la llamada **HrModifyRows** , MAPI envía una sola notificación de TABLE_CHANGED en su lugar.</span><span class="sxs-lookup"><span data-stu-id="124e0-130">If more than eight rows are affected by the **HrModifyRows** call, MAPI sends a single TABLE_CHANGED notification instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="124e0-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="124e0-131">See also</span></span>



[<span data-ttu-id="124e0-132">SRowSet</span><span class="sxs-lookup"><span data-stu-id="124e0-132">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="124e0-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="124e0-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

