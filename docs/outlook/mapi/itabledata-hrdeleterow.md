---
title: ITableDataHrDeleteRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrDeleteRow
api_type:
- COM
ms.assetid: 670c2291-d5b6-4dcf-9046-9125272dd8f8
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b187cccc4505256b7ab4d580c30eeb2e15ebf574
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421679"
---
# <a name="itabledatahrdeleterow"></a><span data-ttu-id="4967e-103">ITableData::HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="4967e-103">ITableData::HrDeleteRow</span></span>

  
  
<span data-ttu-id="4967e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4967e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4967e-105">Elimina una fila de tabla.</span><span class="sxs-lookup"><span data-stu-id="4967e-105">Deletes a table row.</span></span>
  
```cpp
HRESULT HrDeleteRow(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="4967e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4967e-106">Parameters</span></span>

 <span data-ttu-id="4967e-107">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="4967e-107">_lpSPropValue_</span></span>
  
> <span data-ttu-id="4967e-108">[entrada] Puntero a una estructura de valores de propiedad que describe la columna de índice de la fila que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="4967e-108">[in] A pointer to a property value structure that describes the index column for the row to be deleted.</span></span> <span data-ttu-id="4967e-109">El **miembro ulPropTag** de la estructura de valores de propiedad debe contener la misma etiqueta de propiedad que el parámetro _ulPropTagIndexColumn_ de la llamada a la [función CreateTable.](createtable.md)</span><span class="sxs-lookup"><span data-stu-id="4967e-109">The **ulPropTag** member of the property value structure should contain the same property tag as the  _ulPropTagIndexColumn_ parameter from the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4967e-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4967e-110">Return value</span></span>

<span data-ttu-id="4967e-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="4967e-111">S_OK</span></span> 
  
> <span data-ttu-id="4967e-112">La fila se eliminó correctamente.</span><span class="sxs-lookup"><span data-stu-id="4967e-112">The row was successfully deleted.</span></span>
    
<span data-ttu-id="4967e-113">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="4967e-113">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="4967e-114">La propiedad a la que apunta el  _parámetro lpSPropValue_ no identifica una fila de la tabla.</span><span class="sxs-lookup"><span data-stu-id="4967e-114">The property pointed to by the  _lpSPropValue_ parameter does not identify a row in the table.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4967e-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4967e-115">Remarks</span></span>

<span data-ttu-id="4967e-116">El **método ITableData::HrDeleteRow** quita la fila de tabla que contiene la columna que coincide con la propiedad a la que apunta el parámetro _lpSPropValue._</span><span class="sxs-lookup"><span data-stu-id="4967e-116">The **ITableData::HrDeleteRow** method removes the table row that contains the column that matches the property pointed to by the  _lpSPropValue_ parameter.</span></span> <span data-ttu-id="4967e-117">Los datos de la fila se eliminan y la fila se quita de todas las vistas abiertas.</span><span class="sxs-lookup"><span data-stu-id="4967e-117">The data for the row is deleted and the row is removed from all open views.</span></span> 
  
<span data-ttu-id="4967e-118">Después de eliminar la fila, se envían notificaciones a todos los clientes o proveedores de servicios que tienen una vista de la tabla y que han llamado al método [IMAPITable::Advise](imapitable-advise.md) de la tabla para registrarse para recibir notificaciones.</span><span class="sxs-lookup"><span data-stu-id="4967e-118">After the row is deleted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
<span data-ttu-id="4967e-119">La eliminación de una fila no reduce el conjunto de columnas que está disponible para las vistas existentes o las vistas abiertas posteriormente, incluso si la fila eliminada es la última fila que tiene un valor para una columna específica.</span><span class="sxs-lookup"><span data-stu-id="4967e-119">Deleting a row does not reduce the column set that is available to existing views or subsequently opened views, even if the deleted row is the last row that has a value for a specific column.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4967e-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4967e-120">See also</span></span>



[<span data-ttu-id="4967e-121">CreateTable</span><span class="sxs-lookup"><span data-stu-id="4967e-121">CreateTable</span></span>](createtable.md)
  
[<span data-ttu-id="4967e-122">ITableData::HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="4967e-122">ITableData::HrDeleteRows</span></span>](itabledata-hrdeleterows.md)
  
[<span data-ttu-id="4967e-123">ITableData::HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="4967e-123">ITableData::HrModifyRow</span></span>](itabledata-hrmodifyrow.md)
  
[<span data-ttu-id="4967e-124">SPropValue</span><span class="sxs-lookup"><span data-stu-id="4967e-124">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="4967e-125">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4967e-125">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="4967e-126">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4967e-126">ITableData : IUnknown</span></span>](itabledataiunknown.md)

