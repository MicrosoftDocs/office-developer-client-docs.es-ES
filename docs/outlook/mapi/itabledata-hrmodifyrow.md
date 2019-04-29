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
ms.openlocfilehash: 44ecf095ad24dd266dc5f603ace9c7b9f21c1b41
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409002"
---
# <a name="itabledatahrmodifyrow"></a><span data-ttu-id="b2f99-103">ITableData::HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="b2f99-103">ITableData::HrModifyRow</span></span>

  
  
<span data-ttu-id="b2f99-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2f99-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2f99-105">Inserta una nueva fila de tabla, posiblemente reemplazando una fila existente.</span><span class="sxs-lookup"><span data-stu-id="b2f99-105">Inserts a new table row, possibly replacing an existing row.</span></span>
  
```cpp
HRESULT HrModifyRow(
  LPSRow lpSRow
);
```

## <a name="parameters"></a><span data-ttu-id="b2f99-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="b2f99-106">Parameters</span></span>

 <span data-ttu-id="b2f99-107">_lpSRow_</span><span class="sxs-lookup"><span data-stu-id="b2f99-107">_lpSRow_</span></span>
  
> <span data-ttu-id="b2f99-108">a Puntero a una estructura [SRow](srow.md) que describe la fila que se va a agregar o para reemplazar una fila existente.</span><span class="sxs-lookup"><span data-stu-id="b2f99-108">[in] A pointer to an [SRow](srow.md) structure that describes the row to be added or to replace an existing row.</span></span> <span data-ttu-id="b2f99-109">Una de las estructuras de valores de propiedad a la que apunta el miembro **lpProps** de la estructura **SRow** debe contener la columna index, el mismo valor que se especificó en el parámetro _UlPropTagIndexColumn_ en la llamada a [createTable ](createtable.md)función.</span><span class="sxs-lookup"><span data-stu-id="b2f99-109">One of the property value structures pointed to by the **lpProps** member of the **SRow** structure should contain the index column, the same value that was specified in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b2f99-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b2f99-110">Return value</span></span>

<span data-ttu-id="b2f99-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="b2f99-111">S_OK</span></span> 
  
> <span data-ttu-id="b2f99-112">La fila se insertó o modificó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b2f99-112">The row was successfully inserted or modified.</span></span>
    
<span data-ttu-id="b2f99-113">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b2f99-113">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="b2f99-114">La fila pasada no tiene una columna de índice.</span><span class="sxs-lookup"><span data-stu-id="b2f99-114">The passed-in row does not have an index column.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b2f99-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b2f99-115">Remarks</span></span>

<span data-ttu-id="b2f99-116">El método **ITableData:: HrModifyRow** inserta la fila descrita por la estructura **SRow** a la que apunta el parámetro _lpSRow_ .</span><span class="sxs-lookup"><span data-stu-id="b2f99-116">The **ITableData::HrModifyRow** method inserts the row described by the **SRow** structure pointed to by the  _lpSRow_ parameter.</span></span> <span data-ttu-id="b2f99-117">Si una fila que tiene el mismo valor para la columna de índice que la fila a la que apunta _lpSRow_ ya existe en la tabla, se reemplaza la fila existente.</span><span class="sxs-lookup"><span data-stu-id="b2f99-117">If a row that has the same value for its index column as the row that  _lpSRow_ points to already exists in the table, the existing row is replaced.</span></span> <span data-ttu-id="b2f99-118">Si no existe ninguna fila que coincida con la que se incluye en la estructura **SRow** , **HrModifyRow** agrega la fila al final de la tabla.</span><span class="sxs-lookup"><span data-stu-id="b2f99-118">If no row exists that matches the one included in the **SRow** structure, **HrModifyRow** adds the row to the end of the table.</span></span> 
  
<span data-ttu-id="b2f99-119">Se modifican todas las vistas de la tabla para que incluyan la fila a la que apunta _lpSRow_.</span><span class="sxs-lookup"><span data-stu-id="b2f99-119">All views of the table are modified to include the row pointed to by  _lpSRow_.</span></span> <span data-ttu-id="b2f99-120">Sin embargo, si una vista tiene una restricción que excluye la fila, es posible que no esté visible para el usuario.</span><span class="sxs-lookup"><span data-stu-id="b2f99-120">However, if a view has a restriction in place that excludes the row, it may not be visible to the user.</span></span> 
  
<span data-ttu-id="b2f99-121">Las columnas de la fila a las que apunta _lpSRow_ no tienen que estar en el mismo orden que las columnas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="b2f99-121">The columns in the row pointed to by  _lpSRow_ do not have to be in the same order as the columns in the table.</span></span> <span data-ttu-id="b2f99-122">El autor de la llamada también puede incluir como propiedades de columnas que no se encuentran actualmente en la tabla.</span><span class="sxs-lookup"><span data-stu-id="b2f99-122">The caller can also include as columns properties that are not currently in the table.</span></span> <span data-ttu-id="b2f99-123">Para las vistas existentes, **HrModifyRow** hace que estas nuevas columnas estén disponibles, pero no las incluye en el conjunto de columnas actual.</span><span class="sxs-lookup"><span data-stu-id="b2f99-123">For existing views, **HrModifyRow** makes these new columns available but does not include them in the current column set.</span></span> <span data-ttu-id="b2f99-124">Para vistas futuras, **HrModifyRow** incluye las nuevas columnas en el conjunto de columnas.</span><span class="sxs-lookup"><span data-stu-id="b2f99-124">For future views, **HrModifyRow** includes the new columns in the column set.</span></span> 
  
<span data-ttu-id="b2f99-125">Después de que **HrModifyRow** agrega la fila, se envían notificaciones a todos los clientes o proveedores de servicios que tienen una vista de la tabla y que han llamado al método [IMAPITable:: Advise](imapitable-advise.md) para registrarse para las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="b2f99-125">After **HrModifyRow** adds the row, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b2f99-126">Ver también</span><span class="sxs-lookup"><span data-stu-id="b2f99-126">See also</span></span>



[<span data-ttu-id="b2f99-127">SRow</span><span class="sxs-lookup"><span data-stu-id="b2f99-127">SRow</span></span>](srow.md)
  
[<span data-ttu-id="b2f99-128">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b2f99-128">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="b2f99-129">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b2f99-129">ITableData : IUnknown</span></span>](itabledataiunknown.md)

