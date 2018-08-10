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
ms.openlocfilehash: 1fd711683ff476ef5d381bca2f9db6bc25b07c68
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817587"
---
# <a name="imapitablecollapserow"></a><span data-ttu-id="a5af8-103">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="a5af8-103">IMAPITable::CollapseRow</span></span>

  
  
<span data-ttu-id="a5af8-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a5af8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a5af8-105">Contrae una categoría de tabla expandida, quitar los encabezados de nivel inferior y filas de la hoja que pertenecen a la categoría de la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="a5af8-105">Collapses an expanded table category, removing any lower-level headings and leaf rows belonging to the category from the table view.</span></span>
  
```cpp
HRESULT CollapseRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulFlags,
ULONG FAR * lpulRowCount
);
```

## <a name="parameters"></a><span data-ttu-id="a5af8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a5af8-106">Parameters</span></span>

 <span data-ttu-id="a5af8-107">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="a5af8-107">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="a5af8-108">[entrada] El número de bytes de la propiedad PR_INSTANCE_KEY indicada por el parámetro _pbInstanceKey_ .</span><span class="sxs-lookup"><span data-stu-id="a5af8-108">[in] The count of bytes in the PR_INSTANCE_KEY property pointed to by the  _pbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="a5af8-109">_pbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="a5af8-109">_pbInstanceKey_</span></span>
  
> <span data-ttu-id="a5af8-110">[entrada] Un puntero a la propiedad **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) que identifica la fila de encabezado de la categoría.</span><span class="sxs-lookup"><span data-stu-id="a5af8-110">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property that identifies the heading row for the category.</span></span> 
    
 <span data-ttu-id="a5af8-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a5af8-111">_ulFlags_</span></span>
  
> <span data-ttu-id="a5af8-112">Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="a5af8-112">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="a5af8-113">_lpulRowCount_</span><span class="sxs-lookup"><span data-stu-id="a5af8-113">_lpulRowCount_</span></span>
  
> <span data-ttu-id="a5af8-114">[out] Un puntero al número total de filas que se va a quitar de la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="a5af8-114">[out] A pointer to the total number of rows that are being removed from the table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a5af8-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a5af8-115">Return value</span></span>

<span data-ttu-id="a5af8-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="a5af8-116">S_OK</span></span> 
  
> <span data-ttu-id="a5af8-117">Se ha realizado correctamente la operación de contraer.</span><span class="sxs-lookup"><span data-stu-id="a5af8-117">The collapse operation has succeeded.</span></span>
    
<span data-ttu-id="a5af8-118">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="a5af8-118">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="a5af8-119">La fila identificada por el parámetro _pbInstanceKey_ no existe.</span><span class="sxs-lookup"><span data-stu-id="a5af8-119">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> 
    
<span data-ttu-id="a5af8-120">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="a5af8-120">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="a5af8-121">La fila identificada por el parámetro _pbInstanceKey_ no existe.</span><span class="sxs-lookup"><span data-stu-id="a5af8-121">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> <span data-ttu-id="a5af8-122">Este error es una alternativa a MAPI_E_NOT_FOUND; proveedores de servicios pueden devolver cualquiera de ellas.</span><span class="sxs-lookup"><span data-stu-id="a5af8-122">This error is an alternative to MAPI_E_NOT_FOUND; service providers can return either one.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a5af8-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a5af8-123">Remarks</span></span>

<span data-ttu-id="a5af8-124">El método **IMAPITable::CollapseRow** contrae una categoría de tabla y lo quita de la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="a5af8-124">The **IMAPITable::CollapseRow** method collapses a table category and removes it from the table view.</span></span> <span data-ttu-id="a5af8-125">Las filas están contraídas empezando por la fila identificada por la propiedad **PR_INSTANCE_KEY** indicada por el parámetro _pbInstanceKey_ .</span><span class="sxs-lookup"><span data-stu-id="a5af8-125">The rows are collapsed starting at the row identified by the **PR_INSTANCE_KEY** property pointed to by the  _pbInstanceKey_ parameter.</span></span> <span data-ttu-id="a5af8-126">Se devuelve el número de filas que se han quitado de la vista en el contenido del parámetro _lpulRowCount_ .</span><span class="sxs-lookup"><span data-stu-id="a5af8-126">The number of rows that are removed from the view is returned in the contents of the  _lpulRowCount_ parameter.</span></span> 
  
<span data-ttu-id="a5af8-127">Nunca se generan notificaciones para las filas de tabla que se quitan de una vista como resultado de una operación de contracción.</span><span class="sxs-lookup"><span data-stu-id="a5af8-127">Notifications are never generated for table rows that are removed from a view as the result of a collapse operation.</span></span> 
  
<span data-ttu-id="a5af8-128">Cuando se contrae una fila que se define mediante un marcador fuera de la vista, el marcador se mueve para que apunte a la siguiente fila visible.</span><span class="sxs-lookup"><span data-stu-id="a5af8-128">When a row that is defined by a bookmark is collapsed out of view, the bookmark is moved to point to the next visible row.</span></span> 
  
<span data-ttu-id="a5af8-129">Para obtener más información acerca de las tablas ordenadas por categorías, vea [Ordenar y la categorización](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="a5af8-129">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a5af8-130">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a5af8-130">MFCMAPI reference</span></span>

<span data-ttu-id="a5af8-131">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="a5af8-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a5af8-132">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="a5af8-132">**File**</span></span>|<span data-ttu-id="a5af8-133">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="a5af8-133">**Function**</span></span>|<span data-ttu-id="a5af8-134">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="a5af8-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a5af8-135">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="a5af8-135">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="a5af8-136">CContentsTableListCtrl::DoExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="a5af8-136">CContentsTableListCtrl::DoExpandCollapse</span></span>  <br/> |<span data-ttu-id="a5af8-137">MFCMAPI usa el método **IMAPITable::CollapseRow** para contraer una categoría de tabla.</span><span class="sxs-lookup"><span data-stu-id="a5af8-137">MFCMAPI uses the **IMAPITable::CollapseRow** method to collapse a table category.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a5af8-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="a5af8-138">See also</span></span>



[<span data-ttu-id="a5af8-139">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="a5af8-139">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
  
[<span data-ttu-id="a5af8-140">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="a5af8-140">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
  
[<span data-ttu-id="a5af8-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="a5af8-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="a5af8-142">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="a5af8-142">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
  
[<span data-ttu-id="a5af8-143">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="a5af8-143">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="a5af8-144">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="a5af8-144">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="a5af8-145">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a5af8-145">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="a5af8-146">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="a5af8-146">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

