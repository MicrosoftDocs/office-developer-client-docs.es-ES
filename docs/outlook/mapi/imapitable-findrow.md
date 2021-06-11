---
title: IMAPITableFindRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.FindRow
api_type:
- COM
ms.assetid: 6511368c-9777-497e-9eea-cf390c04b92e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a5364af229721d101f38d2f054f528169b48c09e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429575"
---
# <a name="imapitablefindrow"></a><span data-ttu-id="e2363-103">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="e2363-103">IMAPITable::FindRow</span></span>

  
  
<span data-ttu-id="e2363-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2363-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2363-105">Busca la siguiente fila de una tabla que coincide con criterios de búsqueda específicos y mueve el cursor a esa fila.</span><span class="sxs-lookup"><span data-stu-id="e2363-105">Finds the next row in a table that matches specific search criteria and moves the cursor to that row.</span></span>
  
```cpp
HRESULT FindRow(
LPSRestriction lpRestriction,
BOOKMARK BkOrigin,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="e2363-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="e2363-106">Parameters</span></span>

 <span data-ttu-id="e2363-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="e2363-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="e2363-108">[in] Puntero a una [estructura SRestriction](srestriction.md) que describe los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="e2363-108">[in] A pointer to an [SRestriction](srestriction.md) structure that describes the search criteria.</span></span> 
    
 <span data-ttu-id="e2363-109">_BkOrigin_</span><span class="sxs-lookup"><span data-stu-id="e2363-109">_BkOrigin_</span></span>
  
> <span data-ttu-id="e2363-110">[in] Marcador que identifica la fila en la que **FindRow** debe comenzar su búsqueda.</span><span class="sxs-lookup"><span data-stu-id="e2363-110">[in] A bookmark identifying the row where **FindRow** should begin its search.</span></span> <span data-ttu-id="e2363-111">Se puede crear un marcador mediante el método [IMAPITable::CreateBookmark](imapitable-createbookmark.md) o se puede pasar uno de los siguientes valores predefinidos.</span><span class="sxs-lookup"><span data-stu-id="e2363-111">A bookmark can be created using the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method, or one of the following predefined values can be passed.</span></span> 
    
<span data-ttu-id="e2363-112">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="e2363-112">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="e2363-113">Busca desde el principio de la tabla.</span><span class="sxs-lookup"><span data-stu-id="e2363-113">Searches from the beginning of the table.</span></span> 
    
<span data-ttu-id="e2363-114">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="e2363-114">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="e2363-115">Busca en la fila de la tabla donde se encuentra el cursor.</span><span class="sxs-lookup"><span data-stu-id="e2363-115">Searches from the row in the table where the cursor is located.</span></span> 
    
<span data-ttu-id="e2363-116">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="e2363-116">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="e2363-117">Busca desde el final de la tabla.</span><span class="sxs-lookup"><span data-stu-id="e2363-117">Searches from the end of the table.</span></span> 
    
 <span data-ttu-id="e2363-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e2363-118">_ulFlags_</span></span>
  
> <span data-ttu-id="e2363-119">[in] Máscara de bits de marcas que controla la dirección de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="e2363-119">[in] A bitmask of flags that controls the direction of the search.</span></span> <span data-ttu-id="e2363-120">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="e2363-120">The following flag can be set:</span></span>
    
<span data-ttu-id="e2363-121">DIR_BACKWARD</span><span class="sxs-lookup"><span data-stu-id="e2363-121">DIR_BACKWARD</span></span> 
  
> <span data-ttu-id="e2363-122">Busca hacia atrás desde la fila identificada por el marcador.</span><span class="sxs-lookup"><span data-stu-id="e2363-122">Searches backward from the row identified by the bookmark.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e2363-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e2363-123">Return value</span></span>

<span data-ttu-id="e2363-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="e2363-124">S_OK</span></span> 
  
> <span data-ttu-id="e2363-125">La operación de búsqueda se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="e2363-125">The find operation was successful.</span></span>
    
<span data-ttu-id="e2363-126">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="e2363-126">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="e2363-127">El marcador del  _parámetro BkOrigin_ no es válido porque se ha quitado o porque está más allá de la última fila solicitada.</span><span class="sxs-lookup"><span data-stu-id="e2363-127">The bookmark in the  _BkOrigin_ parameter is invalid because it has been removed or because it is beyond the last row requested.</span></span> 
    
<span data-ttu-id="e2363-128">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="e2363-128">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="e2363-129">No se encontraron filas que coincidan con la restricción.</span><span class="sxs-lookup"><span data-stu-id="e2363-129">No rows were found that matched the restriction.</span></span>
    
<span data-ttu-id="e2363-130">MAPI_W_POSITION_CHANGED</span><span class="sxs-lookup"><span data-stu-id="e2363-130">MAPI_W_POSITION_CHANGED</span></span>
  
> <span data-ttu-id="e2363-131">La llamada se ha hecho correctamente, pero el marcador usado en la operación ya no se establece en la misma fila que cuando se usó por última vez; si no se ha usado el marcador, ya no está en la misma posición que cuando se creó.</span><span class="sxs-lookup"><span data-stu-id="e2363-131">The call succeeded, but the bookmark used in the operation is no longer set at the same row as when it was last used; if the bookmark has not been used, it is no longer in the same position as when it was created.</span></span> <span data-ttu-id="e2363-132">Cuando se devuelve esta advertencia, la llamada debe controlarse como correcta.</span><span class="sxs-lookup"><span data-stu-id="e2363-132">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="e2363-133">Para probar esta advertencia, use la **HR_FAILED** macro.</span><span class="sxs-lookup"><span data-stu-id="e2363-133">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="e2363-134">Consulte [Using Macros for Error Handling](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="e2363-134">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e2363-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e2363-135">Remarks</span></span>

<span data-ttu-id="e2363-136">El **método IMAPITable::FindRow** localiza la primera fila de la tabla para que coincida con un conjunto de criterios de búsqueda descritos en la estructura **SRestriction** a la que apunta el parámetro _lpRestriction._</span><span class="sxs-lookup"><span data-stu-id="e2363-136">The **IMAPITable::FindRow** method locates the first row in the table to match a set of search criteria described in the **SRestriction** structure pointed to by the  _lpRestriction_ parameter.</span></span> 
  
<span data-ttu-id="e2363-137">Por lo general, **FindRow** busca hacia delante desde el marcador especificado.</span><span class="sxs-lookup"><span data-stu-id="e2363-137">Usually, **FindRow** searches forward from the specified bookmark.</span></span> <span data-ttu-id="e2363-138">El autor de la llamada puede establecer la búsqueda para que se mueva hacia atrás desde el marcador estableciendo la marca DIR_BACKWARD en el _parámetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="e2363-138">The caller can set the search to move backward from the bookmark by setting the DIR_BACKWARD flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="e2363-139">La búsqueda hacia delante comienza desde el marcador actual; la búsqueda hacia atrás comienza desde la fila anterior al marcador.</span><span class="sxs-lookup"><span data-stu-id="e2363-139">Searching forward starts from the current bookmark; searching backward starts from the row prior to the bookmark.</span></span> <span data-ttu-id="e2363-140">La posición final de la búsqueda es justo antes de que se encontrara la primera fila que satisficía la restricción.</span><span class="sxs-lookup"><span data-stu-id="e2363-140">The end position of the search is just before the first row found that satisfied the restriction.</span></span> 
  
<span data-ttu-id="e2363-141">Si la fila señalada por el marcador en el parámetro  _BkOrigin_ ya no existe en la tabla y la tabla no puede establecer una nueva posición para el marcador, **FindRow** devuelve MAPI_E_INVALID_BOOKMARK.</span><span class="sxs-lookup"><span data-stu-id="e2363-141">If the row pointed to by the bookmark in the  _BkOrigin_ parameter no longer exists in the table and the table cannot establish a new position for the bookmark, **FindRow** returns MAPI_E_INVALID_BOOKMARK.</span></span> <span data-ttu-id="e2363-142">Si la fila señalada por  _BkOrigin_ ya no existe y la tabla puede establecer una nueva posición para el marcador, **FindRow** devuelve MAPI_W_POSITION_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="e2363-142">If the row pointed to by  _BkOrigin_ no longer exists and the table is able to establish a new position for the bookmark, **FindRow** returns MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="e2363-143">Si el marcador pasado en  _BkOrigin_ es BOOKMARK_BEGINNING o BOOKMARK_END, **FindRow** devuelve MAPI_E_NOT_FOUND si no se encuentra ninguna fila que coincida.</span><span class="sxs-lookup"><span data-stu-id="e2363-143">If the bookmark passed in  _BkOrigin_ is either BOOKMARK_BEGINNING or BOOKMARK_END, **FindRow** returns MAPI_E_NOT_FOUND if no matching row is found.</span></span> <span data-ttu-id="e2363-144">Si el marcador usado en  _BkOrigin_ es BOOKMARK_CURRENT, **FindRow** puede devolver MAPI_W_POSITION_CHANGED pero no MAPI_E_INVALID_BOOKMARK porque siempre hay una posición del cursor actual.</span><span class="sxs-lookup"><span data-stu-id="e2363-144">If the bookmark used in  _BkOrigin_ is BOOKMARK_CURRENT, **FindRow** can return MAPI_W_POSITION_CHANGED but not MAPI_E_INVALID_BOOKMARK because there is always a current cursor position.</span></span> 
  
<span data-ttu-id="e2363-145">La **columna de propiedad PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) es necesaria para todas las tablas y todas las implementaciones de **FindRow** son necesarias para admitir llamadas que buscan una fila basada en PR_INSTANCE_KEY.</span><span class="sxs-lookup"><span data-stu-id="e2363-145">The **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property column is required for all tables, and all implementations of **FindRow** are required to support calls seeking a row based on PR_INSTANCE_KEY.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e2363-146">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="e2363-146">Notes to implementers</span></span>

<span data-ttu-id="e2363-147">El tipo de búsqueda de prefijos realizada por **FindRow** solo es útil cuando la búsqueda sigue la misma dirección que la organización de la tabla.</span><span class="sxs-lookup"><span data-stu-id="e2363-147">The type of prefix searching performed by **FindRow** is only useful when the search follows the same direction as the table organization.</span></span> <span data-ttu-id="e2363-148">Para lograr el comportamiento necesario, la función de comparación implícita por el **RELOP_GE** pasado en la estructura de restricción de propiedades debe ser la misma función de comparación en la que se basa el criterio de ordenación de tabla.</span><span class="sxs-lookup"><span data-stu-id="e2363-148">In order to achieve the required behavior, the comparison function implied by the **RELOP_GE** passed in the property restriction structure should be the same comparison function on which the table sort order is based.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e2363-149">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="e2363-149">Notes to callers</span></span>

<span data-ttu-id="e2363-150">Puede usar **FindRow para** admitir el desplazamiento en función de las cadenas que escriba el usuario, especialmente en cuadros de lista dentro de cuadros de diálogo de direcciones.</span><span class="sxs-lookup"><span data-stu-id="e2363-150">You can use **FindRow** to support scrolling based on strings typed in by the user, especially in list boxes within address dialog boxes.</span></span> <span data-ttu-id="e2363-151">En este tipo de desplazamiento, los usuarios escriben prefijos progresivamente más largos de un valor de cadena deseado y puede emitir periódicamente una llamada **FindRow** para saltar a la primera fila que coincida con el prefijo.</span><span class="sxs-lookup"><span data-stu-id="e2363-151">In this type of scrolling, users enter progressively longer prefixes of a desired string value, and you can periodically issue a **FindRow** call to jump to the first row that matches the prefix.</span></span> <span data-ttu-id="e2363-152">La dirección en la que salta el cursor depende de la dirección en la que se establezca la búsqueda para ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="e2363-152">Which direction the cursor jumps depends on which direction the search is set to run.</span></span> 
  
<span data-ttu-id="e2363-153">Para usar **FindRow,** se debe establecer un marcador.</span><span class="sxs-lookup"><span data-stu-id="e2363-153">To use **FindRow**, a bookmark must be set.</span></span> <span data-ttu-id="e2363-154">La búsqueda de cadena puede originarse a partir de cualquier marcador, incluidos los marcadores preestablecidos que indican la posición actual y el principio y el final de la tabla.</span><span class="sxs-lookup"><span data-stu-id="e2363-154">The string search can originate from any bookmark, including from the preset bookmarks indicating the current position and the beginning and end of the table.</span></span> <span data-ttu-id="e2363-155">Si hay un gran número de filas en la tabla, la operación de búsqueda puede ser lenta.</span><span class="sxs-lookup"><span data-stu-id="e2363-155">If there are a large number of rows in the table, the search operation can be slow.</span></span>
  
<span data-ttu-id="e2363-156">Use una restricción para buscar un prefijo de cadena para desplazarse de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="e2363-156">Use a restriction to find a string prefix for scrolling as follows.</span></span> <span data-ttu-id="e2363-157">Para la búsqueda hacia delante en una columna ordenada en orden ascendente y para la búsqueda hacia atrás en una columna ordenada en orden descendente, pase una estructura  de restricción de propiedades en el parámetro _lpRestriction_ con la relación **RELOP_GE** y la etiqueta y el prefijo de propiedad adecuados, usando el prefijo **GE** de la etiqueta de formato _._</span><span class="sxs-lookup"><span data-stu-id="e2363-157">For forward searching on a column sorted in ascending order and for backward searching on a column sorted in descending order, pass a property restriction structure in the  _lpRestriction_ parameter with the relation **RELOP_GE** and the appropriate property tag and prefix, using the format  _tag_ **GE** _prefix_.</span></span> 
  
<span data-ttu-id="e2363-158">Para obtener más información acerca del uso de estructuras de restricción para especificar un filtro, vea [Acerca de las restricciones](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="e2363-158">For more information about using restriction structures to specify a filter, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e2363-159">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e2363-159">MFCMAPI reference</span></span>

<span data-ttu-id="e2363-160">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="e2363-160">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e2363-161">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="e2363-161">**File**</span></span>|<span data-ttu-id="e2363-162">**Función**</span><span class="sxs-lookup"><span data-stu-id="e2363-162">**Function**</span></span>|<span data-ttu-id="e2363-163">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="e2363-163">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e2363-164">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="e2363-164">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="e2363-165">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="e2363-165">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="e2363-166">MFCMAPI usa el **método IMAPITable::FindRow** para buscar filas que coincidan con una restricción.</span><span class="sxs-lookup"><span data-stu-id="e2363-166">MFCMAPI uses the **IMAPITable::FindRow** method to find rows which match a restriction.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e2363-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2363-167">See also</span></span>



[<span data-ttu-id="e2363-168">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="e2363-168">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="e2363-169">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="e2363-169">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="e2363-170">SRestriction</span><span class="sxs-lookup"><span data-stu-id="e2363-170">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="e2363-171">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e2363-171">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="e2363-172">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="e2363-172">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

