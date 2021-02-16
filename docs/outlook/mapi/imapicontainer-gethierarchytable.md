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
# <a name="imapicontainergethierarchytable"></a><span data-ttu-id="d9c11-103">IMAPIContainer::GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="d9c11-103">IMAPIContainer::GetHierarchyTable</span></span>

  
  
<span data-ttu-id="d9c11-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9c11-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9c11-105">Devuelve un puntero a la tabla de jerarquía del contenedor.</span><span class="sxs-lookup"><span data-stu-id="d9c11-105">Returns a pointer to the container's hierarchy table.</span></span>
  
```cpp
HRESULT GetHierarchyTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="d9c11-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d9c11-106">Parameters</span></span>

 <span data-ttu-id="d9c11-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d9c11-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d9c11-108">[entrada] Máscara de bits de marcas que controla cómo se devuelve la información en la tabla.</span><span class="sxs-lookup"><span data-stu-id="d9c11-108">[in] A bitmask of flags that controls how information is returned in the table.</span></span> <span data-ttu-id="d9c11-109">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="d9c11-109">The following flags can be set:</span></span>
    
<span data-ttu-id="d9c11-110">CONVENIENT_DEPTH</span><span class="sxs-lookup"><span data-stu-id="d9c11-110">CONVENIENT_DEPTH</span></span> 
  
> <span data-ttu-id="d9c11-111">Rellena la tabla de jerarquía con contenedores de varios niveles.</span><span class="sxs-lookup"><span data-stu-id="d9c11-111">Fills the hierarchy table with containers from multiple levels.</span></span> <span data-ttu-id="d9c11-112">Si CONVENIENT_DEPTH no se establece, la tabla de jerarquía contiene solo los contenedores secundarios inmediatos del contenedor.</span><span class="sxs-lookup"><span data-stu-id="d9c11-112">If CONVENIENT_DEPTH is not set, the hierarchy table contains only the container's immediate child containers.</span></span>
    
<span data-ttu-id="d9c11-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="d9c11-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="d9c11-114">**GetHierarchyTable** puede devolverse correctamente, posiblemente antes de que la tabla esté disponible para el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="d9c11-114">**GetHierarchyTable** can return successfully, possibly before the table is made available to the caller.</span></span> <span data-ttu-id="d9c11-115">Si la tabla no está disponible, realizar una llamada de tabla posterior puede generar un error.</span><span class="sxs-lookup"><span data-stu-id="d9c11-115">If the table is not available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="d9c11-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d9c11-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d9c11-117">Solicita que las columnas que contienen datos de cadena se devuelvan en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="d9c11-117">Requests that the columns that contain string data be returned in Unicode format.</span></span> <span data-ttu-id="d9c11-118">Si no MAPI_UNICODE marca, las cadenas deben devolverse en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="d9c11-118">If the MAPI_UNICODE flag is not set, the strings should be returned in ANSI format.</span></span> 
    
<span data-ttu-id="d9c11-119">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="d9c11-119">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="d9c11-120">Muestra los elementos que están marcados actualmente como eliminados temporalmente, es decir, están en la fase de tiempo de retención de elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="d9c11-120">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="d9c11-121">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="d9c11-121">_lppTable_</span></span>
  
> <span data-ttu-id="d9c11-122">[salida] Puntero a un puntero a la tabla de jerarquía.</span><span class="sxs-lookup"><span data-stu-id="d9c11-122">[out] A pointer to a pointer to the hierarchy table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d9c11-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d9c11-123">Return value</span></span>

<span data-ttu-id="d9c11-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="d9c11-124">S_OK</span></span> 
  
> <span data-ttu-id="d9c11-125">La tabla de jerarquía se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="d9c11-125">The hierarchy table was successfully retrieved.</span></span>
    
<span data-ttu-id="d9c11-126">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="d9c11-126">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="d9c11-127">Se estableció MAPI_UNICODE marca y la implementación no admite Unicode, o MAPI_UNICODE no se estableció y la implementación solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="d9c11-127">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="d9c11-128">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="d9c11-128">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="d9c11-129">El contenedor no tiene contenedores secundarios y no puede proporcionar una tabla de jerarquía.</span><span class="sxs-lookup"><span data-stu-id="d9c11-129">The container has no child containers and cannot provide a hierarchy table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d9c11-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d9c11-130">Remarks</span></span>

<span data-ttu-id="d9c11-131">El **método IMAPIContainer::GetHierarchyTable** devuelve un puntero a la tabla de jerarquía de un contenedor.</span><span class="sxs-lookup"><span data-stu-id="d9c11-131">The **IMAPIContainer::GetHierarchyTable** method returns a pointer to the hierarchy table of a container.</span></span> <span data-ttu-id="d9c11-132">Una tabla de jerarquía contiene información de resumen sobre los contenedores secundarios del contenedor.</span><span class="sxs-lookup"><span data-stu-id="d9c11-132">A hierarchy table holds summary information about the child containers in the container.</span></span> <span data-ttu-id="d9c11-133">Las tablas de jerarquía de carpetas tienen información sobre subcarpetas; Las tablas de jerarquía de libretas de direcciones incluyen información sobre los contenedores de libretas de direcciones secundarios y las listas de distribución.</span><span class="sxs-lookup"><span data-stu-id="d9c11-133">Folder hierarchy tables hold information about subfolders; address book hierarchy tables hold information about child address book containers and distribution lists.</span></span> 
  
<span data-ttu-id="d9c11-134">Es posible que algunos contenedores no tengan contenedores secundarios.</span><span class="sxs-lookup"><span data-stu-id="d9c11-134">It is possible for some containers to have no child containers.</span></span> <span data-ttu-id="d9c11-135">Estos contenedores devuelven MAPI_E_NO_SUPPORT de sus implementaciones **de GetHierarchyTable**.</span><span class="sxs-lookup"><span data-stu-id="d9c11-135">These containers return MAPI_E_NO_SUPPORT from their implementations of **GetHierarchyTable**.</span></span>
  
<span data-ttu-id="d9c11-136">Cuando se CONVENIENT_DEPTH marca, cada fila de la tabla de jerarquía también incluye la propiedad **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) como una columna.</span><span class="sxs-lookup"><span data-stu-id="d9c11-136">When the CONVENIENT_DEPTH flag is set, each row in the hierarchy table also includes the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property as a column.</span></span> <span data-ttu-id="d9c11-137">**PR_DEPTH** indica el nivel de cada contenedor en relación con el contenedor que implementa la tabla.</span><span class="sxs-lookup"><span data-stu-id="d9c11-137">**PR_DEPTH** indicates the level of each container relative to the container that implements the table.</span></span> <span data-ttu-id="d9c11-138">Los contenedores secundarios inmediatos del contenedor de implementación están en profundidad cero, los contenedores secundarios en los contenedores de profundidad cero están en profundidad uno, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="d9c11-138">The implementing container's immediate child containers are at depth zero, child containers in the zero depth containers are at depth one, and so on.</span></span> <span data-ttu-id="d9c11-139">Los valores de **PR_DEPTH** aumentan secuencialmente a medida que aumenta la jerarquía de niveles.</span><span class="sxs-lookup"><span data-stu-id="d9c11-139">The values of **PR_DEPTH** increase sequentially as the hierarchy of levels deepens.</span></span> 
  
<span data-ttu-id="d9c11-140">Para obtener una lista completa de las columnas obligatorias y opcionales de las tablas de jerarquía, vea [Tablas de jerarquía.](hierarchy-tables.md)</span><span class="sxs-lookup"><span data-stu-id="d9c11-140">For a complete list of required and optional columns in hierarchy tables, see [Hierarchy Tables](hierarchy-tables.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d9c11-141">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="d9c11-141">Notes to implementers</span></span>

<span data-ttu-id="d9c11-142">Si admite una tabla de jerarquía para el contenedor, también debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d9c11-142">If you support a hierarchy table for your container, you must also do the following:</span></span>
  
- <span data-ttu-id="d9c11-143">Admite una llamada al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del contenedor para abrir la **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d9c11-143">Support a call to the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="d9c11-144">Devuelve **PR_CONTAINER_HIERARCHY** de una llamada a los métodos [IMAPIProp::GetPropList](imapiprop-getproplist.md) o [IMAPIProp::GetProps del](imapiprop-getprops.md) contenedor.</span><span class="sxs-lookup"><span data-stu-id="d9c11-144">Return **PR_CONTAINER_HIERARCHY** from a call to the container's [IMAPIProp::GetPropList](imapiprop-getproplist.md) or [IMAPIProp::GetProps](imapiprop-getprops.md) methods.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="d9c11-145">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="d9c11-145">Notes to callers</span></span>

<span data-ttu-id="d9c11-146">Las columnas de tabla de contenido binario y de cadena se pueden truncar.</span><span class="sxs-lookup"><span data-stu-id="d9c11-146">String and binary contents table columns can be truncated.</span></span> <span data-ttu-id="d9c11-147">Normalmente, los proveedores devuelven 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="d9c11-147">Typically, providers return 255 characters.</span></span> <span data-ttu-id="d9c11-148">Como no puede saber de antemano si una tabla incluye columnas truncadas, suponga que una columna se trunca si la longitud de la columna es de 255 o 510 bytes.</span><span class="sxs-lookup"><span data-stu-id="d9c11-148">Because you cannot know beforehand whether a table includes truncated columns, assume that a column is truncated if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="d9c11-149">Siempre puede recuperar el valor completo de una columna truncada, si es necesario, directamente desde el objeto usando su identificador de entrada para abrirlo y, a continuación, llamando al método [IMAPIProp::GetProps.](imapiprop-getprops.md)</span><span class="sxs-lookup"><span data-stu-id="d9c11-149">You can always retrieve the full value of a truncated column, if necessary, directly from the object by using its entry identifier to open it and then calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
<span data-ttu-id="d9c11-150">Según la implementación del proveedor, las restricciones y las operaciones de ordenación pueden aplicarse a toda la cadena o a la versión truncada de esa cadena.</span><span class="sxs-lookup"><span data-stu-id="d9c11-150">Depending on the provider's implementation, restrictions and sorting operations can apply to the whole string or to the truncated version of that string.</span></span> <span data-ttu-id="d9c11-151">Además, no se garantiza que los proveedores de almacén respetarán el conjunto de criterios de ordenación [especificado](ssortorderset.md) para las tablas de jerarquía.</span><span class="sxs-lookup"><span data-stu-id="d9c11-151">Moreover, store providers are not guaranteed to honor the sort order set [SSortOrderSet](ssortorderset.md) specified for hierarchy tables.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d9c11-152">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d9c11-152">MFCMAPI reference</span></span>

<span data-ttu-id="d9c11-153">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="d9c11-153">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d9c11-154">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="d9c11-154">**File**</span></span>|<span data-ttu-id="d9c11-155">**Función**</span><span class="sxs-lookup"><span data-stu-id="d9c11-155">**Function**</span></span>|<span data-ttu-id="d9c11-156">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="d9c11-156">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d9c11-157">HierarchyTableTreeCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="d9c11-157">HierarchyTableTreeCtrl.cpp</span></span>  <br/> |<span data-ttu-id="d9c11-158">CHierarchyTableTreeCtrl::GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="d9c11-158">CHierarchyTableTreeCtrl::GetHierarchyTable</span></span>  <br/> |<span data-ttu-id="d9c11-159">La clase CHierarchyTableTreeCtrl usa **GetHierarchyTable** para obtener tablas de jerarquía para mostrar en un control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="d9c11-159">The CHierarchyTableTreeCtrl class uses **GetHierarchyTable** to obtain hierarchy tables to display in a tree view control.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d9c11-160">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d9c11-160">See also</span></span>



[<span data-ttu-id="d9c11-161">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="d9c11-161">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="d9c11-162">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="d9c11-162">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="d9c11-163">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d9c11-163">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="d9c11-164">Propiedad canónica PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="d9c11-164">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="d9c11-165">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d9c11-165">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="d9c11-166">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="d9c11-166">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

