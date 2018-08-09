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
ms.openlocfilehash: 37d0ce65e125b2420af775d61ead51db189758ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817970"
---
# <a name="itabledatahrdeleterow"></a><span data-ttu-id="daa3f-103">ITableData::HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="daa3f-103">ITableData::HrDeleteRow</span></span>

  
  
<span data-ttu-id="daa3f-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="daa3f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="daa3f-105">Elimina una fila de tabla.</span><span class="sxs-lookup"><span data-stu-id="daa3f-105">Deletes a table row.</span></span>
  
```cpp
HRESULT HrDeleteRow(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="daa3f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="daa3f-106">Parameters</span></span>

 <span data-ttu-id="daa3f-107">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="daa3f-107">_lpSPropValue_</span></span>
  
> <span data-ttu-id="daa3f-108">[entrada] Un puntero a una estructura de valor de propiedad que describe la columna de índice de la fila que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="daa3f-108">[in] A pointer to a property value structure that describes the index column for the row to be deleted.</span></span> <span data-ttu-id="daa3f-109">El miembro **ulPropTag** de la estructura del valor de propiedad debe contener la misma etiqueta de propiedad como el parámetro _ulPropTagIndexColumn_ de la llamada a la función [CreateTable](createtable.md) .</span><span class="sxs-lookup"><span data-stu-id="daa3f-109">The **ulPropTag** member of the property value structure should contain the same property tag as the  _ulPropTagIndexColumn_ parameter from the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="daa3f-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="daa3f-110">Return value</span></span>

<span data-ttu-id="daa3f-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="daa3f-111">S_OK</span></span> 
  
> <span data-ttu-id="daa3f-112">La fila se eliminó correctamente.</span><span class="sxs-lookup"><span data-stu-id="daa3f-112">The row was successfully deleted.</span></span>
    
<span data-ttu-id="daa3f-113">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="daa3f-113">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="daa3f-114">La propiedad indicada por el parámetro _lpSPropValue_ no identifica una fila en la tabla.</span><span class="sxs-lookup"><span data-stu-id="daa3f-114">The property pointed to by the  _lpSPropValue_ parameter does not identify a row in the table.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="daa3f-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="daa3f-115">Remarks</span></span>

<span data-ttu-id="daa3f-116">El método **ITableData::HrDeleteRow** quita la fila de tabla que contiene la columna que coincide con la propiedad indicada por el parámetro _lpSPropValue_ .</span><span class="sxs-lookup"><span data-stu-id="daa3f-116">The **ITableData::HrDeleteRow** method removes the table row that contains the column that matches the property pointed to by the  _lpSPropValue_ parameter.</span></span> <span data-ttu-id="daa3f-117">Se eliminan los datos de la fila y la fila se quita de todas las vistas abiertas.</span><span class="sxs-lookup"><span data-stu-id="daa3f-117">The data for the row is deleted and the row is removed from all open views.</span></span> 
  
<span data-ttu-id="daa3f-118">Después de que se elimina la fila, se envían a todos los clientes o proveedores de servicios que tienen una vista de la tabla y que ha llamado [IMAPITable::Advise](imapitable-advise.md) (método) de la tabla para registrar para las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="daa3f-118">After the row is deleted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
<span data-ttu-id="daa3f-119">Eliminación de una fila no reduce el conjunto de columna que está disponible para las vistas existentes o vuelven a abrir vistas, incluso si la fila eliminada es la última fila que tenga un valor para una columna específica.</span><span class="sxs-lookup"><span data-stu-id="daa3f-119">Deleting a row does not reduce the column set that is available to existing views or subsequently opened views, even if the deleted row is the last row that has a value for a specific column.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="daa3f-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="daa3f-120">See also</span></span>



[<span data-ttu-id="daa3f-121">CreateTable</span><span class="sxs-lookup"><span data-stu-id="daa3f-121">CreateTable</span></span>](createtable.md)
  
[<span data-ttu-id="daa3f-122">ITableData::HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="daa3f-122">ITableData::HrDeleteRows</span></span>](itabledata-hrdeleterows.md)
  
[<span data-ttu-id="daa3f-123">ITableData::HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="daa3f-123">ITableData::HrModifyRow</span></span>](itabledata-hrmodifyrow.md)
  
[<span data-ttu-id="daa3f-124">SPropValue</span><span class="sxs-lookup"><span data-stu-id="daa3f-124">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="daa3f-125">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="daa3f-125">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="daa3f-126">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="daa3f-126">ITableData : IUnknown</span></span>](itabledataiunknown.md)

