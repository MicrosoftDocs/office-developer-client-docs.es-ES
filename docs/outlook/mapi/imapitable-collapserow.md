---
title: IMAPITableCollapseRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.CollapseRow
api_type:
- COM
ms.assetid: 1a23e555-be26-43fb-a715-cfc4ffa623cd
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e6a180ceb325a705ebf226bb728c52cce7396490
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416177"
---
# <a name="imapitablecollapserow"></a><span data-ttu-id="d6466-103">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="d6466-103">IMAPITable::CollapseRow</span></span>

  
  
<span data-ttu-id="d6466-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6466-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6466-105">Contrae una categoría de tabla expandida, quitando los encabezados de nivel inferior y las filas hoja que pertenecen a la categoría de la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="d6466-105">Collapses an expanded table category, removing any lower-level headings and leaf rows belonging to the category from the table view.</span></span>
  
```cpp
HRESULT CollapseRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulFlags,
ULONG FAR * lpulRowCount
);
```

## <a name="parameters"></a><span data-ttu-id="d6466-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d6466-106">Parameters</span></span>

 <span data-ttu-id="d6466-107">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="d6466-107">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="d6466-108">[entrada] El recuento de bytes en la PR_INSTANCE_KEY propiedad que apunta el _parámetro pbInstanceKey._</span><span class="sxs-lookup"><span data-stu-id="d6466-108">[in] The count of bytes in the PR_INSTANCE_KEY property pointed to by the  _pbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="d6466-109">_pbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="d6466-109">_pbInstanceKey_</span></span>
  
> <span data-ttu-id="d6466-110">[entrada] Puntero a la propiedad **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) que identifica la fila de título de la categoría.</span><span class="sxs-lookup"><span data-stu-id="d6466-110">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property that identifies the heading row for the category.</span></span> 
    
 <span data-ttu-id="d6466-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d6466-111">_ulFlags_</span></span>
  
> <span data-ttu-id="d6466-112">Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="d6466-112">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="d6466-113">_lpulRowCount_</span><span class="sxs-lookup"><span data-stu-id="d6466-113">_lpulRowCount_</span></span>
  
> <span data-ttu-id="d6466-114">[salida] Puntero al número total de filas que se están quitando de la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="d6466-114">[out] A pointer to the total number of rows that are being removed from the table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d6466-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d6466-115">Return value</span></span>

<span data-ttu-id="d6466-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="d6466-116">S_OK</span></span> 
  
> <span data-ttu-id="d6466-117">La operación de con contraer se ha hecho correctamente.</span><span class="sxs-lookup"><span data-stu-id="d6466-117">The collapse operation has succeeded.</span></span>
    
<span data-ttu-id="d6466-118">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="d6466-118">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="d6466-119">La fila identificada por el  _parámetro pbInstanceKey_ no existe.</span><span class="sxs-lookup"><span data-stu-id="d6466-119">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> 
    
<span data-ttu-id="d6466-120">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="d6466-120">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="d6466-121">La fila identificada por el  _parámetro pbInstanceKey_ no existe.</span><span class="sxs-lookup"><span data-stu-id="d6466-121">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> <span data-ttu-id="d6466-122">Este error es una alternativa a MAPI_E_NOT_FOUND; los proveedores de servicios pueden devolver cualquiera de los dos.</span><span class="sxs-lookup"><span data-stu-id="d6466-122">This error is an alternative to MAPI_E_NOT_FOUND; service providers can return either one.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d6466-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d6466-123">Remarks</span></span>

<span data-ttu-id="d6466-124">El **método IMAPITable::CollapseRow** contrae una categoría de tabla y la quita de la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="d6466-124">The **IMAPITable::CollapseRow** method collapses a table category and removes it from the table view.</span></span> <span data-ttu-id="d6466-125">Las filas se contraen empezando por la fila identificada por **la PR_INSTANCE_KEY** que apunta el _parámetro pbInstanceKey._</span><span class="sxs-lookup"><span data-stu-id="d6466-125">The rows are collapsed starting at the row identified by the **PR_INSTANCE_KEY** property pointed to by the  _pbInstanceKey_ parameter.</span></span> <span data-ttu-id="d6466-126">El número de filas que se quitan de la vista se devuelve en el contenido del parámetro _lpulRowCount._</span><span class="sxs-lookup"><span data-stu-id="d6466-126">The number of rows that are removed from the view is returned in the contents of the  _lpulRowCount_ parameter.</span></span> 
  
<span data-ttu-id="d6466-127">Las notificaciones nunca se generan para las filas de tabla que se quitan de una vista como resultado de una operación de con contraer.</span><span class="sxs-lookup"><span data-stu-id="d6466-127">Notifications are never generated for table rows that are removed from a view as the result of a collapse operation.</span></span> 
  
<span data-ttu-id="d6466-128">Cuando una fila definida por un marcador se contrae fuera de la vista, el marcador se mueve para apuntar a la siguiente fila visible.</span><span class="sxs-lookup"><span data-stu-id="d6466-128">When a row that is defined by a bookmark is collapsed out of view, the bookmark is moved to point to the next visible row.</span></span> 
  
<span data-ttu-id="d6466-129">Para obtener más información acerca de las tablas categorizadas, vea [Ordenar y categorizar.](sorting-and-categorization.md)</span><span class="sxs-lookup"><span data-stu-id="d6466-129">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d6466-130">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d6466-130">MFCMAPI reference</span></span>

<span data-ttu-id="d6466-131">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="d6466-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d6466-132">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="d6466-132">**File**</span></span>|<span data-ttu-id="d6466-133">**Función**</span><span class="sxs-lookup"><span data-stu-id="d6466-133">**Function**</span></span>|<span data-ttu-id="d6466-134">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="d6466-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d6466-135">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="d6466-135">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="d6466-136">CContentsTableListCtrl::D oExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="d6466-136">CContentsTableListCtrl::DoExpandCollapse</span></span>  <br/> |<span data-ttu-id="d6466-137">MFCMAPI usa el **método IMAPITable::CollapseRow** para contraer una categoría de tabla.</span><span class="sxs-lookup"><span data-stu-id="d6466-137">MFCMAPI uses the **IMAPITable::CollapseRow** method to collapse a table category.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d6466-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d6466-138">See also</span></span>



[<span data-ttu-id="d6466-139">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="d6466-139">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
  
[<span data-ttu-id="d6466-140">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="d6466-140">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
  
[<span data-ttu-id="d6466-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="d6466-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="d6466-142">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="d6466-142">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
  
[<span data-ttu-id="d6466-143">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="d6466-143">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="d6466-144">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="d6466-144">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="d6466-145">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d6466-145">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="d6466-146">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="d6466-146">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

