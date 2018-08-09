---
title: ITableDataHrInsertRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrInsertRow
api_type:
- COM
ms.assetid: e5ae37ea-81a5-49c7-9ad0-0bfac518426c
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 29fdbf060576ee9309473fddf8740b06229dae9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817965"
---
# <a name="itabledatahrinsertrow"></a><span data-ttu-id="3bef8-103">ITableData::HrInsertRow</span><span class="sxs-lookup"><span data-stu-id="3bef8-103">ITableData::HrInsertRow</span></span>

  
  
<span data-ttu-id="3bef8-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3bef8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3bef8-105">Inserta una fila de tabla.</span><span class="sxs-lookup"><span data-stu-id="3bef8-105">Inserts a table row.</span></span> 
  
```cpp
HRESULT HrInsertRow(
  ULONG uliRow,
  LPSRow lpSRow
);
```

## <a name="parameters"></a><span data-ttu-id="3bef8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3bef8-106">Parameters</span></span>

 <span data-ttu-id="3bef8-107">_uliRow_</span><span class="sxs-lookup"><span data-stu-id="3bef8-107">_uliRow_</span></span>
  
> <span data-ttu-id="3bef8-108">[entrada] Un número de fila secuencial que representa una fila concreta.</span><span class="sxs-lookup"><span data-stu-id="3bef8-108">[in] A sequential row number that represents a specific row.</span></span> <span data-ttu-id="3bef8-109">Después de la fila que indica el número se colocará la nueva fila.</span><span class="sxs-lookup"><span data-stu-id="3bef8-109">The new row will be placed after the row that the number indicates.</span></span> <span data-ttu-id="3bef8-110">El parámetro _uliRow_ puede contener los números de filas de n a 0, donde n es el número total de filas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="3bef8-110">The  _uliRow_ parameter can contains row numbers from 0 through n, where n is the total number of rows in the table.</span></span> <span data-ttu-id="3bef8-111">Pasando n _uliRow_ , la fila anexa al final de la tabla.</span><span class="sxs-lookup"><span data-stu-id="3bef8-111">Passing n in  _uliRow_ appends the row to the end of the table.</span></span> 
    
 <span data-ttu-id="3bef8-112">_lpSRow_</span><span class="sxs-lookup"><span data-stu-id="3bef8-112">_lpSRow_</span></span>
  
> <span data-ttu-id="3bef8-113">[entrada] Un puntero a una estructura [SRow](srow.md) que describe la fila que se va a insertar.</span><span class="sxs-lookup"><span data-stu-id="3bef8-113">[in] A pointer to an [SRow](srow.md) structure that describes the row to be inserted.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3bef8-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3bef8-114">Return value</span></span>

<span data-ttu-id="3bef8-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="3bef8-115">S_OK</span></span> 
  
> <span data-ttu-id="3bef8-116">La fila se insertó correctamente.</span><span class="sxs-lookup"><span data-stu-id="3bef8-116">The row was successfully inserted.</span></span>
    
<span data-ttu-id="3bef8-117">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3bef8-117">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="3bef8-118">Una fila que tiene el mismo valor para su columna de índice, como la fila que va a insertarse ya existe en la tabla.</span><span class="sxs-lookup"><span data-stu-id="3bef8-118">A row that has the same value for its index column as the row to be inserted already exists in the table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3bef8-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3bef8-119">Remarks</span></span>

<span data-ttu-id="3bef8-120">El método **ITableData::HrInsertRow** , inserta una fila en una tabla en una posición determinada.</span><span class="sxs-lookup"><span data-stu-id="3bef8-120">The **ITableData::HrInsertRow** method inserts a row into a table at a particular position.</span></span> <span data-ttu-id="3bef8-121">La nueva fila se inserta después de la fila que se encuentra en la posición especificada por el parámetro _uliRow_ .</span><span class="sxs-lookup"><span data-stu-id="3bef8-121">The new row is inserted after the row that is in the position specified by the  _uliRow_ parameter.</span></span> 
  
<span data-ttu-id="3bef8-122">Si _uliRow_ se establece en el número de filas en la tabla, la nueva fila se anexa al final de la tabla.</span><span class="sxs-lookup"><span data-stu-id="3bef8-122">If  _uliRow_ is set to the number of rows in the table, the new row is appended to the end of the table.</span></span> 
  
<span data-ttu-id="3bef8-123">La propiedad que actúa como la columna de índice para la tabla debe incluirse en el miembro **lpProps** de la estructura [SRow](srow.md) indicada por el parámetro _lpSRow_ .</span><span class="sxs-lookup"><span data-stu-id="3bef8-123">The property that acts as the index column for the table must be included in the **lpProps** member of the [SRow](srow.md) structure pointed to by the  _lpSRow_ parameter.</span></span> <span data-ttu-id="3bef8-124">Esta propiedad de índice, normalmente **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), se usa para identificar de forma exclusiva la fila de tareas de mantenimiento futuros.</span><span class="sxs-lookup"><span data-stu-id="3bef8-124">This index property, typically **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), is used to uniquely identify the row for future maintenance tasks.</span></span>
  
<span data-ttu-id="3bef8-125">Las columnas de propiedad de la estructura de **SRow** no es necesario estar en el mismo orden que las columnas de propiedad en la tabla.</span><span class="sxs-lookup"><span data-stu-id="3bef8-125">The property columns in the **SRow** structure do not have to be in the same order as the property columns in the table.</span></span> 
  
<span data-ttu-id="3bef8-126">Después de que se inserte la fila, se envían a todos los clientes o proveedores de servicios que tienen una vista de la tabla y que ha llamado [IMAPITable::Advise](imapitable-advise.md) (método) de la tabla para registrar para las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="3bef8-126">After the row is inserted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> <span data-ttu-id="3bef8-127">Si la fila insertada no está incluida en la vista debido a una restricción, se envía ninguna notificación.</span><span class="sxs-lookup"><span data-stu-id="3bef8-127">No notification is sent if the inserted row is not included in the view due to a restriction.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3bef8-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="3bef8-128">See also</span></span>



[<span data-ttu-id="3bef8-129">SRow</span><span class="sxs-lookup"><span data-stu-id="3bef8-129">SRow</span></span>](srow.md)
  
[<span data-ttu-id="3bef8-130">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="3bef8-130">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="3bef8-131">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3bef8-131">ITableData : IUnknown</span></span>](itabledataiunknown.md)

