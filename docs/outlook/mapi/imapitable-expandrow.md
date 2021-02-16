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
ms.openlocfilehash: 5e2ce756baaefef7bd0028e746b1dbe10756365e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415169"
---
# <a name="imapitableexpandrow"></a><span data-ttu-id="5bb36-103">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="5bb36-103">IMAPITable::ExpandRow</span></span>

  
  
<span data-ttu-id="5bb36-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5bb36-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5bb36-105">Expande una categoría de tabla contrayendo, agregando las filas de título hoja o de nivel inferior que pertenecen a la categoría a la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="5bb36-105">Expands a collapsed table category, adding the leaf or lower-level heading rows belonging to the category to the table view.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="5bb36-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5bb36-106">Parameters</span></span>

 <span data-ttu-id="5bb36-107">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="5bb36-107">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="5bb36-108">[entrada] El recuento de bytes de la PR_INSTANCE_KEY que apunta el _parámetro pbInstanceKey._</span><span class="sxs-lookup"><span data-stu-id="5bb36-108">[in] The count of bytes in the PR_INSTANCE_KEY property pointed to by the  _pbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="5bb36-109">_pbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="5bb36-109">_pbInstanceKey_</span></span>
  
> <span data-ttu-id="5bb36-110">[entrada] Puntero a la propiedad **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) que identifica la fila de título de la categoría.</span><span class="sxs-lookup"><span data-stu-id="5bb36-110">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property that identifies the heading row for the category.</span></span> 
    
 <span data-ttu-id="5bb36-111">_ulRowCount_</span><span class="sxs-lookup"><span data-stu-id="5bb36-111">_ulRowCount_</span></span>
  
> <span data-ttu-id="5bb36-112">[entrada] Número máximo de filas que se devolverán en el _parámetro lppRows._</span><span class="sxs-lookup"><span data-stu-id="5bb36-112">[in] The maximum number of rows to return in the  _lppRows_ parameter.</span></span> 
    
 <span data-ttu-id="5bb36-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5bb36-113">_ulFlags_</span></span>
  
> <span data-ttu-id="5bb36-114">Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5bb36-114">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="5bb36-115">_lppRows_</span><span class="sxs-lookup"><span data-stu-id="5bb36-115">_lppRows_</span></span>
  
> <span data-ttu-id="5bb36-116">[salida] Puntero a una estructura [SRowSet](srowset.md) que recibe las primeras filas (hasta  _ulRowCount_) que se han insertado en la vista de tabla como resultado de la expansión.</span><span class="sxs-lookup"><span data-stu-id="5bb36-116">[out] A pointer to an [SRowSet](srowset.md) structure receiving the first (up to  _ulRowCount_) rows that have been inserted into the table view as a result of the expansion.</span></span> <span data-ttu-id="5bb36-117">Estas filas se insertan después de la fila de título identificada por el _parámetro pbInstanceKey._</span><span class="sxs-lookup"><span data-stu-id="5bb36-117">These rows are inserted after the heading row identified by the  _pbInstanceKey_ parameter.</span></span> <span data-ttu-id="5bb36-118">El  _parámetro lppRows_ puede ser NULL si  _el parámetro ulRowCount_ es cero.</span><span class="sxs-lookup"><span data-stu-id="5bb36-118">The  _lppRows_ parameter can be NULL if the  _ulRowCount_ parameter is zero.</span></span> 
    
 <span data-ttu-id="5bb36-119">_lpulMoreRows_</span><span class="sxs-lookup"><span data-stu-id="5bb36-119">_lpulMoreRows_</span></span>
  
> <span data-ttu-id="5bb36-120">[salida] Puntero al número total de filas que se agregaron a la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="5bb36-120">[out] A pointer to the total number of rows that were added to the table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5bb36-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5bb36-121">Return value</span></span>

<span data-ttu-id="5bb36-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="5bb36-122">S_OK</span></span> 
  
> <span data-ttu-id="5bb36-123">La categoría se expandió correctamente.</span><span class="sxs-lookup"><span data-stu-id="5bb36-123">The category was expanded successfully.</span></span>
    
<span data-ttu-id="5bb36-124">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="5bb36-124">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="5bb36-125">La fila identificada por el  _parámetro pbInstanceKey_ no existe.</span><span class="sxs-lookup"><span data-stu-id="5bb36-125">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5bb36-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5bb36-126">Remarks</span></span>

<span data-ttu-id="5bb36-127">El **método IMAPITable::ExpandRow** expande una categoría de tabla contrae, agregando las filas de título hoja o de nivel inferior que pertenecen a la categoría a la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="5bb36-127">The **IMAPITable::ExpandRow** method expands a collapsed table category, adding the leaf or lower-level heading rows that belong to the category to the table view.</span></span> <span data-ttu-id="5bb36-128">Se puede especificar un límite en el número de filas que se devolverán en el parámetro _lppRows_ en el _parámetro ulRowCount._</span><span class="sxs-lookup"><span data-stu-id="5bb36-128">A limit to the number of rows to be returned in the  _lppRows_ parameter can be specified in the  _ulRowCount_ parameter.</span></span> <span data-ttu-id="5bb36-129">Cuando  _ulRowCount_ se establece en un valor mayor que cero y se devuelve una o más filas en el conjunto de filas señalado por  _lppRows_, la posición del marcador BOOKMARK_CURRENT se mueve a la fila inmediatamente posterior a la última fila del conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="5bb36-129">When  _ulRowCount_ is set to a value greater than zero and one or more rows are returned in the row set pointed to by  _lppRows_, the position of the bookmark BOOKMARK_CURRENT is moved to the row immediately following the last row in the row set.</span></span>
  
<span data-ttu-id="5bb36-130">Cuando  _ulRowCount_ se establece en cero, solicitando que las filas de título de hoja cero o de nivel inferior se agregan a la categoría, o se devuelven cero filas porque no hay filas de encabezado de hoja o de nivel inferior en la categoría, la posición de BOOKMARK_CURRENT se establece en la fila que sigue a la fila identificada por  _pbInstanceKey_.</span><span class="sxs-lookup"><span data-stu-id="5bb36-130">When  _ulRowCount_ is set to zero, requesting that zero leaf or lower-level heading rows be added to the category, or zero rows are returned because there are no leaf or lower-level heading rows in the category, the position of BOOKMARK_CURRENT is set to the row following the row identified by  _pbInstanceKey_.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="5bb36-131">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="5bb36-131">Notes to implementers</span></span>

<span data-ttu-id="5bb36-132">No genere notificaciones en filas que se agregan a una vista de tabla debido a la expansión de categorías.</span><span class="sxs-lookup"><span data-stu-id="5bb36-132">Do not generate notifications on rows that are added to a table view due to category expansion.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="5bb36-133">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="5bb36-133">Notes to callers</span></span>

<span data-ttu-id="5bb36-134">Es posible que el número de filas del conjunto de filas al que apunta el parámetro  _lppRows_ no sea igual al número de filas que se agregaron realmente a la tabla, todo el conjunto de filas de título hoja o de nivel inferior de la categoría.</span><span class="sxs-lookup"><span data-stu-id="5bb36-134">The number of rows in the row set pointed to by the  _lppRows_ parameter might not equal the number of rows that were actually added to the table, the entire set of leaf or lower-level heading rows for the category.</span></span> <span data-ttu-id="5bb36-135">Pueden producirse errores, como memoria insuficiente o el número de filas de la categoría que supera el número especificado en el _parámetro ulRowCount._</span><span class="sxs-lookup"><span data-stu-id="5bb36-135">Errors can occur, such as insufficient memory, or the number of rows in the category exceeding the number specified in  _ulRowCount_ parameter.</span></span> <span data-ttu-id="5bb36-136">En cualquier caso, BOOKMARK_CURRENT se colocará en la última fila devuelta.</span><span class="sxs-lookup"><span data-stu-id="5bb36-136">In either case, BOOKMARK_CURRENT will be positioned at the last row returned.</span></span> <span data-ttu-id="5bb36-137">Para recuperar inmediatamente el resto de las filas de la categoría, llame a [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="5bb36-137">To immediately retrieve the rest of the rows in the category, call [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span>
  
<span data-ttu-id="5bb36-138">No espere recibir una notificación de tabla cuando una categoría cambie su estado.</span><span class="sxs-lookup"><span data-stu-id="5bb36-138">Do not expect to receive a table notification when a category changes its state.</span></span> <span data-ttu-id="5bb36-139">Puede mantener una caché local de filas que se pueden actualizar con cada **llamada ExpandRow** o **CollapseRow.**</span><span class="sxs-lookup"><span data-stu-id="5bb36-139">You can maintain a local cache of rows that can be updated with every **ExpandRow** or **CollapseRow** call.</span></span> 
  
<span data-ttu-id="5bb36-140">Para obtener más información acerca de las tablas categorizadas, vea [Ordenar y categorizar.](sorting-and-categorization.md)</span><span class="sxs-lookup"><span data-stu-id="5bb36-140">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5bb36-141">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="5bb36-141">MFCMAPI reference</span></span>

<span data-ttu-id="5bb36-142">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="5bb36-142">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5bb36-143">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="5bb36-143">**File**</span></span>|<span data-ttu-id="5bb36-144">**Función**</span><span class="sxs-lookup"><span data-stu-id="5bb36-144">**Function**</span></span>|<span data-ttu-id="5bb36-145">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="5bb36-145">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5bb36-146">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="5bb36-146">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="5bb36-147">CContentsTableListCtrl::D oExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="5bb36-147">CContentsTableListCtrl::DoExpandCollapse</span></span>  <br/> |<span data-ttu-id="5bb36-148">MFCMAPI usa el **método IMAPITable::ExpandRow** para expandir una categoría de tabla contrae.</span><span class="sxs-lookup"><span data-stu-id="5bb36-148">MFCMAPI uses the **IMAPITable::ExpandRow** method to expand a collapsed table category.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5bb36-149">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5bb36-149">See also</span></span>



[<span data-ttu-id="5bb36-150">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="5bb36-150">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)
  
[<span data-ttu-id="5bb36-151">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5bb36-151">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="5bb36-152">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="5bb36-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

