---
title: ITableDataHrDeleteRows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrDeleteRows
api_type:
- COM
ms.assetid: 7b351eec-9624-4b38-9978-5d0b67b64687
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 00662d7a5bf1c2addc5c4e0b39d657abd7073753
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817966"
---
# <a name="itabledatahrdeleterows"></a><span data-ttu-id="4fe1f-103">ITableData::HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="4fe1f-103">ITableData::HrDeleteRows</span></span>

  
  
<span data-ttu-id="4fe1f-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4fe1f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4fe1f-105">Elimina varias filas de tabla.</span><span class="sxs-lookup"><span data-stu-id="4fe1f-105">Deletes multiple table rows.</span></span>
  
```cpp
HRESULT HrDeleteRows(
  ULONG ulFlags,
  LPSRowSet lprowsetToDelete,
  ULONG FAR * cRowsDeleted
);
```

## <a name="parameters"></a><span data-ttu-id="4fe1f-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="4fe1f-106">Parameters</span></span>

 <span data-ttu-id="4fe1f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4fe1f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="4fe1f-108">[entrada] Una máscara de bits de indicadores que controla la eliminación.</span><span class="sxs-lookup"><span data-stu-id="4fe1f-108">[in] A bitmask of flags that controls the deletion.</span></span> <span data-ttu-id="4fe1f-109">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="4fe1f-109">The following flag can be set:</span></span>
    
<span data-ttu-id="4fe1f-110">TAD_ALL_ROWS</span><span class="sxs-lookup"><span data-stu-id="4fe1f-110">TAD_ALL_ROWS</span></span> 
  
> <span data-ttu-id="4fe1f-111">Elimina todas las filas de la tabla y todas las vistas correspondientes, enviar una notificación de TABLE_RELOAD único.</span><span class="sxs-lookup"><span data-stu-id="4fe1f-111">Deletes all rows from the table and all corresponding views, sending a single TABLE_RELOAD notification.</span></span>
    
 <span data-ttu-id="4fe1f-112">_lprowsetToDelete_</span><span class="sxs-lookup"><span data-stu-id="4fe1f-112">_lprowsetToDelete_</span></span>
  
> <span data-ttu-id="4fe1f-113">[entrada] Un puntero a un conjunto de filas que se describe las filas que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="4fe1f-113">[in] A pointer to a row set that describes the rows to be deleted.</span></span> <span data-ttu-id="4fe1f-114">El parámetro _lprowsetToDelete_ puede ser NULL si la marca TAD_ALL_ROWS se establece en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="4fe1f-114">The  _lprowsetToDelete_ parameter can be NULL if the TAD_ALL_ROWS flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="4fe1f-115">_cRowsDeleted_</span><span class="sxs-lookup"><span data-stu-id="4fe1f-115">_cRowsDeleted_</span></span>
  
> <span data-ttu-id="4fe1f-116">[out] El recuento de las filas eliminadas.</span><span class="sxs-lookup"><span data-stu-id="4fe1f-116">[out] The count of the deleted rows.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4fe1f-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4fe1f-117">Return value</span></span>

<span data-ttu-id="4fe1f-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="4fe1f-118">S_OK</span></span> 
  
> <span data-ttu-id="4fe1f-119">Las filas de tabla se eliminaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="4fe1f-119">The table rows were successfully deleted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4fe1f-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4fe1f-120">Remarks</span></span>

<span data-ttu-id="4fe1f-121">El método **ITableData::HrDeleteRows** busca y quita las filas de tabla que contienen las columnas que coinciden con la propiedad apuntada establece el miembro **lpProps** de cada entrada de **aRow** en la fila.</span><span class="sxs-lookup"><span data-stu-id="4fe1f-121">The **ITableData::HrDeleteRows** method locates and removes the table rows that contain the columns that match the property pointed to by the **lpProps** member of each **aRow** entry in the row set.</span></span> <span data-ttu-id="4fe1f-122">Una columna de índice se usa para identificar cada fila; Esta columna debe tener la misma etiqueta de propiedad, como la etiqueta de propiedad que se pasa en el parámetro _ulPropTagIndexColumn_ en la llamada a la función [CreateTable](createtable.md) .</span><span class="sxs-lookup"><span data-stu-id="4fe1f-122">An index column is used to identify each row; this column must have the same property tag as the property tag passed in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
  
<span data-ttu-id="4fe1f-123">Se devuelve el número de filas que realmente se eliminaron en _cRowsDeleted_.</span><span class="sxs-lookup"><span data-stu-id="4fe1f-123">The number of rows that were actually deleted is returned in  _cRowsDeleted_.</span></span> <span data-ttu-id="4fe1f-124">Se devuelve ningún error si no se podrían encontrar una o varias filas.</span><span class="sxs-lookup"><span data-stu-id="4fe1f-124">No error is returned if one or more rows could not be found.</span></span> 
  
<span data-ttu-id="4fe1f-125">Después de que se eliminan las filas, las notificaciones se envían a todos los clientes o proveedores de servicios que tienen una vista de la tabla y que ha llamado [IMAPITable::Advise](imapitable-advise.md) (método) de la tabla para registrar para las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="4fe1f-125">After the rows are deleted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
<span data-ttu-id="4fe1f-126">Eliminación de filas no reduce las columnas disponibles para las vistas de tabla existentes o vuelven a abrir vistas de tabla, incluso si las filas eliminadas son la última que tienen los valores de una columna específica.</span><span class="sxs-lookup"><span data-stu-id="4fe1f-126">Deleting rows does not reduce the columns available to existing table views or subsequently opened table views, even if the deleted rows are the last that have values for a specific column.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4fe1f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="4fe1f-127">See also</span></span>



[<span data-ttu-id="4fe1f-128">CreateTable</span><span class="sxs-lookup"><span data-stu-id="4fe1f-128">CreateTable</span></span>](createtable.md)
  
[<span data-ttu-id="4fe1f-129">ITableData::HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="4fe1f-129">ITableData::HrDeleteRow</span></span>](itabledata-hrdeleterow.md)
  
[<span data-ttu-id="4fe1f-130">ITableData::HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="4fe1f-130">ITableData::HrModifyRows</span></span>](itabledata-hrmodifyrows.md)
  
[<span data-ttu-id="4fe1f-131">SRowSet</span><span class="sxs-lookup"><span data-stu-id="4fe1f-131">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="4fe1f-132">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="4fe1f-132">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="4fe1f-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4fe1f-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)
