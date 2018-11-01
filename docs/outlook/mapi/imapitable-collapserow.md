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
ms.openlocfilehash: b4dd7e9715c2d3c99eda44f7eed0b3360a2e33be
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595303"
---
# <a name="imapitablecollapserow"></a><span data-ttu-id="fba7a-103">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="fba7a-103">IMAPITable::CollapseRow</span></span>

  
  
<span data-ttu-id="fba7a-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fba7a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fba7a-105">Contrae una categoría de tabla expandida, quitar los encabezados de nivel inferior y filas de la hoja que pertenecen a la categoría de la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="fba7a-105">Collapses an expanded table category, removing any lower-level headings and leaf rows belonging to the category from the table view.</span></span>
  
```cpp
HRESULT CollapseRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulFlags,
ULONG FAR * lpulRowCount
);
```

## <a name="parameters"></a><span data-ttu-id="fba7a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fba7a-106">Parameters</span></span>

 <span data-ttu-id="fba7a-107">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="fba7a-107">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="fba7a-108">[entrada] El número de bytes de la propiedad PR_INSTANCE_KEY indicada por el parámetro _pbInstanceKey_ .</span><span class="sxs-lookup"><span data-stu-id="fba7a-108">[in] The count of bytes in the PR_INSTANCE_KEY property pointed to by the  _pbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="fba7a-109">_pbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="fba7a-109">_pbInstanceKey_</span></span>
  
> <span data-ttu-id="fba7a-110">[entrada] Un puntero a la propiedad **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) que identifica la fila de encabezado de la categoría.</span><span class="sxs-lookup"><span data-stu-id="fba7a-110">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property that identifies the heading row for the category.</span></span> 
    
 <span data-ttu-id="fba7a-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fba7a-111">_ulFlags_</span></span>
  
> <span data-ttu-id="fba7a-112">Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="fba7a-112">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="fba7a-113">_lpulRowCount_</span><span class="sxs-lookup"><span data-stu-id="fba7a-113">_lpulRowCount_</span></span>
  
> <span data-ttu-id="fba7a-114">[out] Un puntero al número total de filas que se va a quitar de la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="fba7a-114">[out] A pointer to the total number of rows that are being removed from the table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fba7a-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fba7a-115">Return value</span></span>

<span data-ttu-id="fba7a-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="fba7a-116">S_OK</span></span> 
  
> <span data-ttu-id="fba7a-117">Se ha realizado correctamente la operación de contraer.</span><span class="sxs-lookup"><span data-stu-id="fba7a-117">The collapse operation has succeeded.</span></span>
    
<span data-ttu-id="fba7a-118">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="fba7a-118">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="fba7a-119">La fila identificada por el parámetro _pbInstanceKey_ no existe.</span><span class="sxs-lookup"><span data-stu-id="fba7a-119">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> 
    
<span data-ttu-id="fba7a-120">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="fba7a-120">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="fba7a-121">La fila identificada por el parámetro _pbInstanceKey_ no existe.</span><span class="sxs-lookup"><span data-stu-id="fba7a-121">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> <span data-ttu-id="fba7a-122">Este error es una alternativa a MAPI_E_NOT_FOUND; proveedores de servicios pueden devolver cualquiera de ellas.</span><span class="sxs-lookup"><span data-stu-id="fba7a-122">This error is an alternative to MAPI_E_NOT_FOUND; service providers can return either one.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fba7a-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fba7a-123">Remarks</span></span>

<span data-ttu-id="fba7a-124">El método **IMAPITable::CollapseRow** contrae una categoría de tabla y lo quita de la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="fba7a-124">The **IMAPITable::CollapseRow** method collapses a table category and removes it from the table view.</span></span> <span data-ttu-id="fba7a-125">Las filas están contraídas empezando por la fila identificada por la propiedad **PR_INSTANCE_KEY** indicada por el parámetro _pbInstanceKey_ .</span><span class="sxs-lookup"><span data-stu-id="fba7a-125">The rows are collapsed starting at the row identified by the **PR_INSTANCE_KEY** property pointed to by the  _pbInstanceKey_ parameter.</span></span> <span data-ttu-id="fba7a-126">Se devuelve el número de filas que se han quitado de la vista en el contenido del parámetro _lpulRowCount_ .</span><span class="sxs-lookup"><span data-stu-id="fba7a-126">The number of rows that are removed from the view is returned in the contents of the  _lpulRowCount_ parameter.</span></span> 
  
<span data-ttu-id="fba7a-127">Nunca se generan notificaciones para las filas de tabla que se quitan de una vista como resultado de una operación de contracción.</span><span class="sxs-lookup"><span data-stu-id="fba7a-127">Notifications are never generated for table rows that are removed from a view as the result of a collapse operation.</span></span> 
  
<span data-ttu-id="fba7a-128">Cuando se contrae una fila que se define mediante un marcador fuera de la vista, el marcador se mueve para que apunte a la siguiente fila visible.</span><span class="sxs-lookup"><span data-stu-id="fba7a-128">When a row that is defined by a bookmark is collapsed out of view, the bookmark is moved to point to the next visible row.</span></span> 
  
<span data-ttu-id="fba7a-129">Para obtener más información acerca de las tablas ordenadas por categorías, vea [Ordenar y la categorización](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="fba7a-129">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="fba7a-130">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="fba7a-130">MFCMAPI reference</span></span>

<span data-ttu-id="fba7a-131">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="fba7a-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fba7a-132">**File**</span><span class="sxs-lookup"><span data-stu-id="fba7a-132">**File**</span></span>|<span data-ttu-id="fba7a-133">**Función**</span><span class="sxs-lookup"><span data-stu-id="fba7a-133">**Function**</span></span>|<span data-ttu-id="fba7a-134">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="fba7a-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fba7a-135">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="fba7a-135">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="fba7a-136">CContentsTableListCtrl::DoExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="fba7a-136">CContentsTableListCtrl::DoExpandCollapse</span></span>  <br/> |<span data-ttu-id="fba7a-137">MFCMAPI usa el método **IMAPITable::CollapseRow** para contraer una categoría de tabla.</span><span class="sxs-lookup"><span data-stu-id="fba7a-137">MFCMAPI uses the **IMAPITable::CollapseRow** method to collapse a table category.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fba7a-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="fba7a-138">See also</span></span>



[<span data-ttu-id="fba7a-139">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="fba7a-139">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
  
[<span data-ttu-id="fba7a-140">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="fba7a-140">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
  
[<span data-ttu-id="fba7a-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="fba7a-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="fba7a-142">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="fba7a-142">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
  
[<span data-ttu-id="fba7a-143">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="fba7a-143">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="fba7a-144">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="fba7a-144">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="fba7a-145">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fba7a-145">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="fba7a-146">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="fba7a-146">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

