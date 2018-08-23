---
title: IMAPITableExpandRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.ExpandRow
api_type:
- COM
ms.assetid: b96dd8f6-e648-4014-8a1d-ae1da771c439
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ce78c6873f3a1dc034ae33f3c9e965ef8f2f1815
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563782"
---
# <a name="imapitableexpandrow"></a><span data-ttu-id="60d16-103">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="60d16-103">IMAPITable::ExpandRow</span></span>

  
  
<span data-ttu-id="60d16-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="60d16-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="60d16-105">Expande una categoría de tabla contraído, adición de la hoja o las filas de encabezado de nivel inferior que pertenecen a la categoría a la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="60d16-105">Expands a collapsed table category, adding the leaf or lower-level heading rows belonging to the category to the table view.</span></span>
  
```cpp
HRESULT ExpandRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows,
ULONG FAR * lpulMoreRows
);
```

## <a name="parameters"></a><span data-ttu-id="60d16-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="60d16-106">Parameters</span></span>

 <span data-ttu-id="60d16-107">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="60d16-107">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="60d16-108">[entrada] El número de bytes de la propiedad PR_INSTANCE_KEY indicada por el parámetro _pbInstanceKey_ .</span><span class="sxs-lookup"><span data-stu-id="60d16-108">[in] The count of bytes in the PR_INSTANCE_KEY property pointed to by the  _pbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="60d16-109">_pbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="60d16-109">_pbInstanceKey_</span></span>
  
> <span data-ttu-id="60d16-110">[entrada] Un puntero a la propiedad **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) que identifica la fila de encabezado de la categoría.</span><span class="sxs-lookup"><span data-stu-id="60d16-110">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property that identifies the heading row for the category.</span></span> 
    
 <span data-ttu-id="60d16-111">_ulRowCount_</span><span class="sxs-lookup"><span data-stu-id="60d16-111">_ulRowCount_</span></span>
  
> <span data-ttu-id="60d16-112">[entrada] El número máximo de filas que se devuelven en el parámetro _lppRows_ .</span><span class="sxs-lookup"><span data-stu-id="60d16-112">[in] The maximum number of rows to return in the  _lppRows_ parameter.</span></span> 
    
 <span data-ttu-id="60d16-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="60d16-113">_ulFlags_</span></span>
  
> <span data-ttu-id="60d16-114">Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="60d16-114">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="60d16-115">_lppRows_</span><span class="sxs-lookup"><span data-stu-id="60d16-115">_lppRows_</span></span>
  
> <span data-ttu-id="60d16-116">[out] Un puntero a una estructura [SRowSet](srowset.md) recibir las filas primeros (hasta _ulRowCount_) que se han insertado en la vista de tabla como resultado de la expansión.</span><span class="sxs-lookup"><span data-stu-id="60d16-116">[out] A pointer to an [SRowSet](srowset.md) structure receiving the first (up to  _ulRowCount_) rows that have been inserted into the table view as a result of the expansion.</span></span> <span data-ttu-id="60d16-117">Estas filas se insertan después de la fila de encabezado identificada mediante el parámetro _pbInstanceKey_ .</span><span class="sxs-lookup"><span data-stu-id="60d16-117">These rows are inserted after the heading row identified by the  _pbInstanceKey_ parameter.</span></span> <span data-ttu-id="60d16-118">El parámetro _lppRows_ puede ser NULL si el parámetro _ulRowCount_ es cero.</span><span class="sxs-lookup"><span data-stu-id="60d16-118">The  _lppRows_ parameter can be NULL if the  _ulRowCount_ parameter is zero.</span></span> 
    
 <span data-ttu-id="60d16-119">_lpulMoreRows_</span><span class="sxs-lookup"><span data-stu-id="60d16-119">_lpulMoreRows_</span></span>
  
> <span data-ttu-id="60d16-120">[out] Un puntero al número total de filas que se han agregado a la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="60d16-120">[out] A pointer to the total number of rows that were added to the table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="60d16-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="60d16-121">Return value</span></span>

<span data-ttu-id="60d16-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="60d16-122">S_OK</span></span> 
  
> <span data-ttu-id="60d16-123">La categoría se expandió correctamente.</span><span class="sxs-lookup"><span data-stu-id="60d16-123">The category was expanded successfully.</span></span>
    
<span data-ttu-id="60d16-124">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="60d16-124">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="60d16-125">La fila identificada por el parámetro _pbInstanceKey_ no existe.</span><span class="sxs-lookup"><span data-stu-id="60d16-125">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="60d16-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="60d16-126">Remarks</span></span>

<span data-ttu-id="60d16-127">El método **IMAPITable::ExpandRow** expande una categoría de tabla contraído, adición de la hoja o las filas de encabezado de nivel inferior que pertenecen a la categoría a la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="60d16-127">The **IMAPITable::ExpandRow** method expands a collapsed table category, adding the leaf or lower-level heading rows that belong to the category to the table view.</span></span> <span data-ttu-id="60d16-128">En el parámetro _ulRowCount_ se puede especificar un límite para el número de filas que se devuelven en el parámetro _lppRows_ .</span><span class="sxs-lookup"><span data-stu-id="60d16-128">A limit to the number of rows to be returned in the  _lppRows_ parameter can be specified in the  _ulRowCount_ parameter.</span></span> <span data-ttu-id="60d16-129">Cuando _ulRowCount_ se establece en un valor mayor que cero y se devuelven una o varias filas en el conjunto de filas que señala _lppRows_, se establece la posición del marcador que bookmark_current se mueve a la fila inmediatamente después de la última fila de la fila.</span><span class="sxs-lookup"><span data-stu-id="60d16-129">When  _ulRowCount_ is set to a value greater than zero and one or more rows are returned in the row set pointed to by  _lppRows_, the position of the bookmark BOOKMARK_CURRENT is moved to the row immediately following the last row in the row set.</span></span>
  
<span data-ttu-id="60d16-130">Cuando _ulRowCount_ se establece en cero, que solicita que cero hoja o filas de título de nivel inferior se agrega a la categoría o, se devuelven cero filas porque no hay ninguna hoja o las filas de encabezado de nivel inferior de la categoría, se establece la posición de BOOKMARK_CURRENT en la fila Después de la fila identificada por _pbInstanceKey_.</span><span class="sxs-lookup"><span data-stu-id="60d16-130">When  _ulRowCount_ is set to zero, requesting that zero leaf or lower-level heading rows be added to the category, or zero rows are returned because there are no leaf or lower-level heading rows in the category, the position of BOOKMARK_CURRENT is set to the row following the row identified by  _pbInstanceKey_.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="60d16-131">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="60d16-131">Notes to implementers</span></span>

<span data-ttu-id="60d16-132">No generan notificaciones en las filas que se agregan a una vista de tabla debido a la expansión de la categoría.</span><span class="sxs-lookup"><span data-stu-id="60d16-132">Do not generate notifications on rows that are added to a table view due to category expansion.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="60d16-133">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="60d16-133">Notes to callers</span></span>

<span data-ttu-id="60d16-134">El número de filas en el conjunto de filas que apunta el parámetro _lppRows_ no podría ser igual al número de filas que realmente se han agregado a la tabla, todo el conjunto de hoja o heading filas para la categoría de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="60d16-134">The number of rows in the row set pointed to by the  _lppRows_ parameter might not equal the number of rows that were actually added to the table, the entire set of leaf or lower-level heading rows for the category.</span></span> <span data-ttu-id="60d16-135">Pueden producirse errores, como memoria insuficiente o el número de filas en la categoría si se excede el número especificado en el parámetro _ulRowCount_ .</span><span class="sxs-lookup"><span data-stu-id="60d16-135">Errors can occur, such as insufficient memory, or the number of rows in the category exceeding the number specified in  _ulRowCount_ parameter.</span></span> <span data-ttu-id="60d16-136">En cualquier caso, BOOKMARK_CURRENT se colocará en la última fila devuelta.</span><span class="sxs-lookup"><span data-stu-id="60d16-136">In either case, BOOKMARK_CURRENT will be positioned at the last row returned.</span></span> <span data-ttu-id="60d16-137">Para recuperar inmediatamente el resto de las filas de la categoría, llame [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="60d16-137">To immediately retrieve the rest of the rows in the category, call [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span>
  
<span data-ttu-id="60d16-138">No se debe esperar recibir una notificación de tabla cuando una categoría cambia su estado.</span><span class="sxs-lookup"><span data-stu-id="60d16-138">Do not expect to receive a table notification when a category changes its state.</span></span> <span data-ttu-id="60d16-139">Puede mantener una memoria caché local de filas que se pueden actualizar con cada llamada **ExpandRow** o **CollapseRow** .</span><span class="sxs-lookup"><span data-stu-id="60d16-139">You can maintain a local cache of rows that can be updated with every **ExpandRow** or **CollapseRow** call.</span></span> 
  
<span data-ttu-id="60d16-140">Para obtener más información acerca de las tablas ordenadas por categorías, vea [Ordenar y la categorización](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="60d16-140">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="60d16-141">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="60d16-141">MFCMAPI reference</span></span>

<span data-ttu-id="60d16-142">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="60d16-142">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="60d16-143">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="60d16-143">**File**</span></span>|<span data-ttu-id="60d16-144">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="60d16-144">**Function**</span></span>|<span data-ttu-id="60d16-145">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="60d16-145">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="60d16-146">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="60d16-146">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="60d16-147">CContentsTableListCtrl::DoExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="60d16-147">CContentsTableListCtrl::DoExpandCollapse</span></span>  <br/> |<span data-ttu-id="60d16-148">MFCMAPI usa el método **IMAPITable::ExpandRow** para expandir una categoría de tabla contraídos.</span><span class="sxs-lookup"><span data-stu-id="60d16-148">MFCMAPI uses the **IMAPITable::ExpandRow** method to expand a collapsed table category.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="60d16-149">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="60d16-149">See also</span></span>



[<span data-ttu-id="60d16-150">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="60d16-150">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)
  
[<span data-ttu-id="60d16-151">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="60d16-151">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="60d16-152">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="60d16-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

