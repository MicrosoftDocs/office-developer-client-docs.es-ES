---
title: IMAPIContainerGetHierarchyTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetHierarchyTable
api_type:
- COM
ms.assetid: d0c54092-86a3-47e0-8133-72e119e74b65
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: efc7f7a2fa703004afe361d766e0209ba40ffe46
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426201"
---
# <a name="imapicontainergethierarchytable"></a><span data-ttu-id="609d5-103">IMAPIContainer::GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="609d5-103">IMAPIContainer::GetHierarchyTable</span></span>

  
  
<span data-ttu-id="609d5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="609d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="609d5-105">Devuelve un puntero a la tabla de jerarquías del contenedor.</span><span class="sxs-lookup"><span data-stu-id="609d5-105">Returns a pointer to the container's hierarchy table.</span></span>
  
```cpp
HRESULT GetHierarchyTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="609d5-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="609d5-106">Parameters</span></span>

 <span data-ttu-id="609d5-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="609d5-107">_ulFlags_</span></span>
  
> <span data-ttu-id="609d5-108">a Máscara de máscara de marcadores que controla cómo se devuelve la información en la tabla.</span><span class="sxs-lookup"><span data-stu-id="609d5-108">[in] A bitmask of flags that controls how information is returned in the table.</span></span> <span data-ttu-id="609d5-109">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="609d5-109">The following flags can be set:</span></span>
    
<span data-ttu-id="609d5-110">CONVENIENT_DEPTH</span><span class="sxs-lookup"><span data-stu-id="609d5-110">CONVENIENT_DEPTH</span></span> 
  
> <span data-ttu-id="609d5-111">Rellena la tabla de jerarquía con contenedores de varios niveles.</span><span class="sxs-lookup"><span data-stu-id="609d5-111">Fills the hierarchy table with containers from multiple levels.</span></span> <span data-ttu-id="609d5-112">Si no se establece CONVENIENT_DEPTH, la tabla de jerarquías contiene sólo los contenedores secundarios inmediatos del contenedor.</span><span class="sxs-lookup"><span data-stu-id="609d5-112">If CONVENIENT_DEPTH is not set, the hierarchy table contains only the container's immediate child containers.</span></span>
    
<span data-ttu-id="609d5-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="609d5-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="609d5-114">**GetHierarchyTable** puede volver correctamente, posiblemente antes de que el autor de la llamada haya disponible la tabla.</span><span class="sxs-lookup"><span data-stu-id="609d5-114">**GetHierarchyTable** can return successfully, possibly before the table is made available to the caller.</span></span> <span data-ttu-id="609d5-115">Si la tabla no está disponible, realizar una llamada subsiguiente a la tabla puede generar un error.</span><span class="sxs-lookup"><span data-stu-id="609d5-115">If the table is not available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="609d5-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="609d5-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="609d5-117">Solicita que las columnas que contienen datos de cadena se devuelvan en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="609d5-117">Requests that the columns that contain string data be returned in Unicode format.</span></span> <span data-ttu-id="609d5-118">Si no se establece la marca MAPI_UNICODE, las cadenas deben devolverse en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="609d5-118">If the MAPI_UNICODE flag is not set, the strings should be returned in ANSI format.</span></span> 
    
<span data-ttu-id="609d5-119">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="609d5-119">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="609d5-120">Muestra los elementos que están marcados actualmente como eliminados temporalmente, es decir, se encuentran en la fase de retención de elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="609d5-120">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="609d5-121">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="609d5-121">_lppTable_</span></span>
  
> <span data-ttu-id="609d5-122">contempla Un puntero a un puntero a la tabla de jerarquía.</span><span class="sxs-lookup"><span data-stu-id="609d5-122">[out] A pointer to a pointer to the hierarchy table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="609d5-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="609d5-123">Return value</span></span>

<span data-ttu-id="609d5-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="609d5-124">S_OK</span></span> 
  
> <span data-ttu-id="609d5-125">La tabla de jerarquías se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="609d5-125">The hierarchy table was successfully retrieved.</span></span>
    
<span data-ttu-id="609d5-126">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="609d5-126">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="609d5-127">Se estableció la marca MAPI_UNICODE y la implementación no admite Unicode, o no se estableció MAPI_UNICODE y la implementación solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="609d5-127">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="609d5-128">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="609d5-128">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="609d5-129">El contenedor no tiene contenedores secundarios y no puede proporcionar una tabla de jerarquía.</span><span class="sxs-lookup"><span data-stu-id="609d5-129">The container has no child containers and cannot provide a hierarchy table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="609d5-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="609d5-130">Remarks</span></span>

<span data-ttu-id="609d5-131">El método **IMAPIContainer:: GetHierarchyTable** devuelve un puntero a la tabla de jerarquías de un contenedor.</span><span class="sxs-lookup"><span data-stu-id="609d5-131">The **IMAPIContainer::GetHierarchyTable** method returns a pointer to the hierarchy table of a container.</span></span> <span data-ttu-id="609d5-132">Una tabla de jerarquía contiene información de resumen sobre los contenedores secundarios del contenedor.</span><span class="sxs-lookup"><span data-stu-id="609d5-132">A hierarchy table holds summary information about the child containers in the container.</span></span> <span data-ttu-id="609d5-133">Las tablas de jerarquía de carpetas contienen información acerca de las subcarpetas; las tablas de jerarquías de la libreta de direcciones contienen información sobre contenedores de libretas de direcciones secundarios y listas de distribución.</span><span class="sxs-lookup"><span data-stu-id="609d5-133">Folder hierarchy tables hold information about subfolders; address book hierarchy tables hold information about child address book containers and distribution lists.</span></span> 
  
<span data-ttu-id="609d5-134">Es posible que algunos contenedores no tengan contenedores secundarios.</span><span class="sxs-lookup"><span data-stu-id="609d5-134">It is possible for some containers to have no child containers.</span></span> <span data-ttu-id="609d5-135">Estos contenedores devuelven MAPI_E_NO_SUPPORT de sus implementaciones de **GetHierarchyTable**.</span><span class="sxs-lookup"><span data-stu-id="609d5-135">These containers return MAPI_E_NO_SUPPORT from their implementations of **GetHierarchyTable**.</span></span>
  
<span data-ttu-id="609d5-136">Cuando se establece la marca CONVENIENT_DEPTH, cada fila de la tabla de jerarquía también incluye la propiedad **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) como una columna.</span><span class="sxs-lookup"><span data-stu-id="609d5-136">When the CONVENIENT_DEPTH flag is set, each row in the hierarchy table also includes the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property as a column.</span></span> <span data-ttu-id="609d5-137">**PR_DEPTH** indica el nivel de cada contenedor en relación con el contenedor que implementa la tabla.</span><span class="sxs-lookup"><span data-stu-id="609d5-137">**PR_DEPTH** indicates the level of each container relative to the container that implements the table.</span></span> <span data-ttu-id="609d5-138">Los contenedores secundarios inmediatos del contenedor que se implementan están en cero de profundidad, los contenedores secundarios de los contenedores de profundidad cero están a la profundidad uno y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="609d5-138">The implementing container's immediate child containers are at depth zero, child containers in the zero depth containers are at depth one, and so on.</span></span> <span data-ttu-id="609d5-139">Los valores de **PR_DEPTH** aumentan secuencialmente a medida que se profundiza en la jerarquía de niveles.</span><span class="sxs-lookup"><span data-stu-id="609d5-139">The values of **PR_DEPTH** increase sequentially as the hierarchy of levels deepens.</span></span> 
  
<span data-ttu-id="609d5-140">Para obtener una lista completa de las columnas requeridas y opcionales de las tablas de jerarquía, consulte [Hierarchy tables](hierarchy-tables.md).</span><span class="sxs-lookup"><span data-stu-id="609d5-140">For a complete list of required and optional columns in hierarchy tables, see [Hierarchy Tables](hierarchy-tables.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="609d5-141">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="609d5-141">Notes to implementers</span></span>

<span data-ttu-id="609d5-142">Si admite una tabla de jerarquías para el contenedor, también debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="609d5-142">If you support a hierarchy table for your container, you must also do the following:</span></span>
  
- <span data-ttu-id="609d5-143">Admitir una llamada al método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) del contenedor para abrir la propiedad **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="609d5-143">Support a call to the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="609d5-144">Devuelve **PR_CONTAINER_HIERARCHY** de una llamada a los métodos [IMAPIProp:: GetPropList](imapiprop-getproplist.md) o [IMAPIProp:: GetProps](imapiprop-getprops.md) del contenedor.</span><span class="sxs-lookup"><span data-stu-id="609d5-144">Return **PR_CONTAINER_HIERARCHY** from a call to the container's [IMAPIProp::GetPropList](imapiprop-getproplist.md) or [IMAPIProp::GetProps](imapiprop-getprops.md) methods.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="609d5-145">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="609d5-145">Notes to callers</span></span>

<span data-ttu-id="609d5-146">Las columnas de la tabla de contenido binario y de cadena pueden truncarse.</span><span class="sxs-lookup"><span data-stu-id="609d5-146">String and binary contents table columns can be truncated.</span></span> <span data-ttu-id="609d5-147">Normalmente, los proveedores devuelven 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="609d5-147">Typically, providers return 255 characters.</span></span> <span data-ttu-id="609d5-148">Como no se puede saber de antemano si una tabla incluye columnas truncadas, se supone que una columna está truncada si la longitud de la columna es de 255 o de 510 bytes.</span><span class="sxs-lookup"><span data-stu-id="609d5-148">Because you cannot know beforehand whether a table includes truncated columns, assume that a column is truncated if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="609d5-149">Siempre puede recuperar el valor completo de una columna truncada, si es necesario, directamente desde el objeto mediante su identificador de entrada para abrirla y, a continuación, llamar al método [IMAPIProp:: GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="609d5-149">You can always retrieve the full value of a truncated column, if necessary, directly from the object by using its entry identifier to open it and then calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
<span data-ttu-id="609d5-150">Según la implementación del proveedor, las restricciones y las operaciones de ordenación pueden aplicarse a toda la cadena o a la versión truncada de esa cadena.</span><span class="sxs-lookup"><span data-stu-id="609d5-150">Depending on the provider's implementation, restrictions and sorting operations can apply to the whole string or to the truncated version of that string.</span></span> <span data-ttu-id="609d5-151">Además, no se garantiza que los proveedores de almacenamiento respeten el criterio de ordenación especificado en [SSortOrderSet](ssortorderset.md) para las tablas de jerarquía.</span><span class="sxs-lookup"><span data-stu-id="609d5-151">Moreover, store providers are not guaranteed to honor the sort order set [SSortOrderSet](ssortorderset.md) specified for hierarchy tables.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="609d5-152">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="609d5-152">MFCMAPI reference</span></span>

<span data-ttu-id="609d5-153">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="609d5-153">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="609d5-154">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="609d5-154">**File**</span></span>|<span data-ttu-id="609d5-155">**Función**</span><span class="sxs-lookup"><span data-stu-id="609d5-155">**Function**</span></span>|<span data-ttu-id="609d5-156">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="609d5-156">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="609d5-157">HierarchyTableTreeCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="609d5-157">HierarchyTableTreeCtrl.cpp</span></span>  <br/> |<span data-ttu-id="609d5-158">CHierarchyTableTreeCtrl:: GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="609d5-158">CHierarchyTableTreeCtrl::GetHierarchyTable</span></span>  <br/> |<span data-ttu-id="609d5-159">La clase CHierarchyTableTreeCtrl usa **GetHierarchyTable** para obtener las tablas de jerarquía que se mostrarán en un control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="609d5-159">The CHierarchyTableTreeCtrl class uses **GetHierarchyTable** to obtain hierarchy tables to display in a tree view control.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="609d5-160">Ver también</span><span class="sxs-lookup"><span data-stu-id="609d5-160">See also</span></span>



[<span data-ttu-id="609d5-161">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="609d5-161">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="609d5-162">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="609d5-162">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="609d5-163">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="609d5-163">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="609d5-164">Propiedad canónica PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="609d5-164">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="609d5-165">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="609d5-165">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="609d5-166">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="609d5-166">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

