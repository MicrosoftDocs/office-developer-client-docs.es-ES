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
ms.openlocfilehash: 2709ac612fc9e2edaa57b280d52c0a5229ee9978
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435442"
---
# <a name="itabledatahrinsertrow"></a><span data-ttu-id="e0ec1-103">ITableData::HrInsertRow</span><span class="sxs-lookup"><span data-stu-id="e0ec1-103">ITableData::HrInsertRow</span></span>

  
  
<span data-ttu-id="e0ec1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0ec1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0ec1-105">Inserta una fila de tabla.</span><span class="sxs-lookup"><span data-stu-id="e0ec1-105">Inserts a table row.</span></span> 
  
```cpp
HRESULT HrInsertRow(
  ULONG uliRow,
  LPSRow lpSRow
);
```

## <a name="parameters"></a><span data-ttu-id="e0ec1-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="e0ec1-106">Parameters</span></span>

 <span data-ttu-id="e0ec1-107">_uliRow_</span><span class="sxs-lookup"><span data-stu-id="e0ec1-107">_uliRow_</span></span>
  
> <span data-ttu-id="e0ec1-108">[in] Número de fila secuencial que representa una fila específica.</span><span class="sxs-lookup"><span data-stu-id="e0ec1-108">[in] A sequential row number that represents a specific row.</span></span> <span data-ttu-id="e0ec1-109">La nueva fila se colocará después de la fila que indica el número.</span><span class="sxs-lookup"><span data-stu-id="e0ec1-109">The new row will be placed after the row that the number indicates.</span></span> <span data-ttu-id="e0ec1-110">El  _parámetro uliRow_ puede contiene números de fila de 0 a n, donde n es el número total de filas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="e0ec1-110">The  _uliRow_ parameter can contains row numbers from 0 through n, where n is the total number of rows in the table.</span></span> <span data-ttu-id="e0ec1-111">Al pasar n en  _uliRow_ se anexa la fila al final de la tabla.</span><span class="sxs-lookup"><span data-stu-id="e0ec1-111">Passing n in  _uliRow_ appends the row to the end of the table.</span></span> 
    
 <span data-ttu-id="e0ec1-112">_lpSRow_</span><span class="sxs-lookup"><span data-stu-id="e0ec1-112">_lpSRow_</span></span>
  
> <span data-ttu-id="e0ec1-113">[in] Puntero a una [estructura SRow](srow.md) que describe la fila que se va a insertar.</span><span class="sxs-lookup"><span data-stu-id="e0ec1-113">[in] A pointer to an [SRow](srow.md) structure that describes the row to be inserted.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e0ec1-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e0ec1-114">Return value</span></span>

<span data-ttu-id="e0ec1-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="e0ec1-115">S_OK</span></span> 
  
> <span data-ttu-id="e0ec1-116">La fila se insertó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e0ec1-116">The row was successfully inserted.</span></span>
    
<span data-ttu-id="e0ec1-117">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e0ec1-117">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="e0ec1-118">Una fila que tiene el mismo valor para su columna de índice que la fila que se va a insertar ya existe en la tabla.</span><span class="sxs-lookup"><span data-stu-id="e0ec1-118">A row that has the same value for its index column as the row to be inserted already exists in the table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e0ec1-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e0ec1-119">Remarks</span></span>

<span data-ttu-id="e0ec1-120">El **método ITableData::HrInsertRow** inserta una fila en una tabla en una posición determinada.</span><span class="sxs-lookup"><span data-stu-id="e0ec1-120">The **ITableData::HrInsertRow** method inserts a row into a table at a particular position.</span></span> <span data-ttu-id="e0ec1-121">La nueva fila se inserta después de la fila que se encuentra en la posición especificada por el _parámetro uliRow._</span><span class="sxs-lookup"><span data-stu-id="e0ec1-121">The new row is inserted after the row that is in the position specified by the  _uliRow_ parameter.</span></span> 
  
<span data-ttu-id="e0ec1-122">Si  _uliRow_ se establece en el número de filas de la tabla, la nueva fila se anexa al final de la tabla.</span><span class="sxs-lookup"><span data-stu-id="e0ec1-122">If  _uliRow_ is set to the number of rows in the table, the new row is appended to the end of the table.</span></span> 
  
<span data-ttu-id="e0ec1-123">La propiedad que actúa como columna de índice para la tabla debe incluirse en el **miembro lpProps** de la [estructura SRow](srow.md) a la que apunta el _parámetro lpSRow._</span><span class="sxs-lookup"><span data-stu-id="e0ec1-123">The property that acts as the index column for the table must be included in the **lpProps** member of the [SRow](srow.md) structure pointed to by the  _lpSRow_ parameter.</span></span> <span data-ttu-id="e0ec1-124">Esta propiedad index, normalmente **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), se usa para identificar de forma única la fila para tareas de mantenimiento futuras.</span><span class="sxs-lookup"><span data-stu-id="e0ec1-124">This index property, typically **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), is used to uniquely identify the row for future maintenance tasks.</span></span>
  
<span data-ttu-id="e0ec1-125">Las columnas de propiedad de **la estructura SRow** no tienen que estar en el mismo orden que las columnas de propiedad de la tabla.</span><span class="sxs-lookup"><span data-stu-id="e0ec1-125">The property columns in the **SRow** structure do not have to be in the same order as the property columns in the table.</span></span> 
  
<span data-ttu-id="e0ec1-126">Una vez insertada la fila, se envían notificaciones a todos los clientes o proveedores de servicios que tienen una vista de la tabla y que han llamado al método [IMAPITable::Advise](imapitable-advise.md) de la tabla para registrarse en las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="e0ec1-126">After the row is inserted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> <span data-ttu-id="e0ec1-127">No se envía ninguna notificación si la fila insertada no se incluye en la vista debido a una restricción.</span><span class="sxs-lookup"><span data-stu-id="e0ec1-127">No notification is sent if the inserted row is not included in the view due to a restriction.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e0ec1-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0ec1-128">See also</span></span>



[<span data-ttu-id="e0ec1-129">SRow</span><span class="sxs-lookup"><span data-stu-id="e0ec1-129">SRow</span></span>](srow.md)
  
[<span data-ttu-id="e0ec1-130">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="e0ec1-130">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="e0ec1-131">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e0ec1-131">ITableData : IUnknown</span></span>](itabledataiunknown.md)

