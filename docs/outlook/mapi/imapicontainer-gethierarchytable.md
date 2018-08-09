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
ms.openlocfilehash: b30c6e9840ed5dddfd2d3a5f149a3f0f6e8da605
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817228"
---
# <a name="imapicontainergethierarchytable"></a><span data-ttu-id="bb9c4-103">IMAPIContainer::GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="bb9c4-103">IMAPIContainer::GetHierarchyTable</span></span>

  
  
<span data-ttu-id="bb9c4-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bb9c4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bb9c4-105">Devuelve un puntero a la tabla de jerarquía del contenedor.</span><span class="sxs-lookup"><span data-stu-id="bb9c4-105">Returns a pointer to the container's hierarchy table.</span></span>
  
```cpp
HRESULT GetHierarchyTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="bb9c4-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="bb9c4-106">Parameters</span></span>

 <span data-ttu-id="bb9c4-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bb9c4-107">_ulFlags_</span></span>
  
> <span data-ttu-id="bb9c4-108">[entrada] Una máscara de bits de indicadores que controla cómo se devuelve información de la tabla.</span><span class="sxs-lookup"><span data-stu-id="bb9c4-108">[in] A bitmask of flags that controls how information is returned in the table.</span></span> <span data-ttu-id="bb9c4-109">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="bb9c4-109">The following flags can be set:</span></span>
    
<span data-ttu-id="bb9c4-110">CONVENIENT_DEPTH</span><span class="sxs-lookup"><span data-stu-id="bb9c4-110">CONVENIENT_DEPTH</span></span> 
  
> <span data-ttu-id="bb9c4-111">Rellena la tabla de jerarquía con contenedores de varios niveles.</span><span class="sxs-lookup"><span data-stu-id="bb9c4-111">Fills the hierarchy table with containers from multiple levels.</span></span> <span data-ttu-id="bb9c4-112">Si no se establece CONVENIENT_DEPTH, en la tabla de jerarquía contiene sólo los contenedores de secundarios inmediatos del contenedor.</span><span class="sxs-lookup"><span data-stu-id="bb9c4-112">If CONVENIENT_DEPTH is not set, the hierarchy table contains only the container's immediate child containers.</span></span>
    
<span data-ttu-id="bb9c4-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="bb9c4-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="bb9c4-114">**GetHierarchyTable** puede devolver correctamente, posiblemente antes de que la tabla está disponible para el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="bb9c4-114">**GetHierarchyTable** can return successfully, possibly before the table is made available to the caller.</span></span> <span data-ttu-id="bb9c4-115">Si no está disponible en la tabla, realizar una llamada de tabla subsiguiente puede producir un error.</span><span class="sxs-lookup"><span data-stu-id="bb9c4-115">If the table is not available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="bb9c4-116">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="bb9c4-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="bb9c4-117">Solicitudes que se devuelven las columnas que contienen datos de cadena en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="bb9c4-117">Requests that the columns that contain string data be returned in Unicode format.</span></span> <span data-ttu-id="bb9c4-118">Si no está establecido el indicador MAPI_UNICODE., se deben devolver las cadenas en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="bb9c4-118">If the MAPI_UNICODE flag is not set, the strings should be returned in ANSI format.</span></span> 
    
<span data-ttu-id="bb9c4-119">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="bb9c4-119">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="bb9c4-120">Muestra los elementos que actualmente están marcados como suaves eliminan, es decir, se encuentran en la retención de elementos eliminados fase de tiempo.</span><span class="sxs-lookup"><span data-stu-id="bb9c4-120">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="bb9c4-121">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="bb9c4-121">_lppTable_</span></span>
  
> <span data-ttu-id="bb9c4-122">[out] Un puntero a un puntero a la tabla de jerarquía.</span><span class="sxs-lookup"><span data-stu-id="bb9c4-122">[out] A pointer to a pointer to the hierarchy table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bb9c4-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb9c4-123">Return value</span></span>

<span data-ttu-id="bb9c4-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="bb9c4-124">S_OK</span></span> 
  
> <span data-ttu-id="bb9c4-125">En la tabla de jerarquía se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="bb9c4-125">The hierarchy table was successfully retrieved.</span></span>
    
<span data-ttu-id="bb9c4-126">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="bb9c4-126">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="bb9c4-127">Se ha establecido el indicador MAPI_UNICODE y la implementación no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y la implementación admite sólo Unicode.</span><span class="sxs-lookup"><span data-stu-id="bb9c4-127">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="bb9c4-128">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="bb9c4-128">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="bb9c4-129">El contenedor tiene los contenedores secundarios y no puede proporcionar una tabla de jerarquía.</span><span class="sxs-lookup"><span data-stu-id="bb9c4-129">The container has no child containers and cannot provide a hierarchy table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bb9c4-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bb9c4-130">Remarks</span></span>

<span data-ttu-id="bb9c4-131">El método **IMAPIContainer::GetHierarchyTable** devuelve un puntero a la tabla de jerarquía de un contenedor.</span><span class="sxs-lookup"><span data-stu-id="bb9c4-131">The **IMAPIContainer::GetHierarchyTable** method returns a pointer to the hierarchy table of a container.</span></span> <span data-ttu-id="bb9c4-132">Una tabla de jerarquía contiene información de resumen acerca de los contenedores secundarios en el contenedor.</span><span class="sxs-lookup"><span data-stu-id="bb9c4-132">A hierarchy table holds summary information about the child containers in the container.</span></span> <span data-ttu-id="bb9c4-133">Tablas de jerarquía de carpeta almacenar información acerca de las subcarpetas; tablas de jerarquía de la libreta de direcciones contienen información acerca de secundarios contenedores de la libreta de direcciones y listas de distribución.</span><span class="sxs-lookup"><span data-stu-id="bb9c4-133">Folder hierarchy tables hold information about subfolders; address book hierarchy tables hold information about child address book containers and distribution lists.</span></span> 
  
<span data-ttu-id="bb9c4-134">Es posible que algunos contenedores tener ningún contenedores secundarios.</span><span class="sxs-lookup"><span data-stu-id="bb9c4-134">It is possible for some containers to have no child containers.</span></span> <span data-ttu-id="bb9c4-135">Estos contenedores devuelven MAPI_E_NO_SUPPORT de sus implementaciones de **GetHierarchyTable**.</span><span class="sxs-lookup"><span data-stu-id="bb9c4-135">These containers return MAPI_E_NO_SUPPORT from their implementations of **GetHierarchyTable**.</span></span>
  
<span data-ttu-id="bb9c4-136">Cuando se establece la marca CONVENIENT_DEPTH, cada fila de la tabla de jerarquía incluye también la propiedad **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) como una columna.</span><span class="sxs-lookup"><span data-stu-id="bb9c4-136">When the CONVENIENT_DEPTH flag is set, each row in the hierarchy table also includes the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property as a column.</span></span> <span data-ttu-id="bb9c4-137">**PR_DEPTH** indica el nivel de cada contenedor en relación con el contenedor que implementa la tabla.</span><span class="sxs-lookup"><span data-stu-id="bb9c4-137">**PR_DEPTH** indicates the level of each container relative to the container that implements the table.</span></span> <span data-ttu-id="bb9c4-138">Secundarios inmediatos del contenedor de implementación son contenedores en profundidad de cero, los contenedores secundarios de los contenedores de profundidad cero se encuentran en profundidad de uno y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="bb9c4-138">The implementing container's immediate child containers are at depth zero, child containers in the zero depth containers are at depth one, and so on.</span></span> <span data-ttu-id="bb9c4-139">Los valores de **PR_DEPTH** aumentan secuencialmente como profundiza la jerarquía de niveles.</span><span class="sxs-lookup"><span data-stu-id="bb9c4-139">The values of **PR_DEPTH** increase sequentially as the hierarchy of levels deepens.</span></span> 
  
<span data-ttu-id="bb9c4-140">Para obtener una lista completa de columnas opcionales y obligatorios en las tablas de jerarquía, vea [Las tablas de jerarquía](hierarchy-tables.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c4-140">For a complete list of required and optional columns in hierarchy tables, see [Hierarchy Tables](hierarchy-tables.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="bb9c4-141">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="bb9c4-141">Notes to implementers</span></span>

<span data-ttu-id="bb9c4-142">Si decide admitir una tabla de jerarquías de su contenedor, también debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="bb9c4-142">If you support a hierarchy table for your container, you must also do the following:</span></span>
  
- <span data-ttu-id="bb9c4-143">Admite una llamada al método de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del contenedor para abrir la propiedad **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="bb9c4-143">Support a call to the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="bb9c4-144">Devolver **PR_CONTAINER_HIERARCHY** de una llamada a los métodos [IMAPIProp::GetPropList](imapiprop-getproplist.md) o [IMAPIProp::GetProps](imapiprop-getprops.md) del contenedor.</span><span class="sxs-lookup"><span data-stu-id="bb9c4-144">Return **PR_CONTAINER_HIERARCHY** from a call to the container's [IMAPIProp::GetPropList](imapiprop-getproplist.md) or [IMAPIProp::GetProps](imapiprop-getprops.md) methods.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="bb9c4-145">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="bb9c4-145">Notes to callers</span></span>

<span data-ttu-id="bb9c4-146">Las columnas de tabla de contenido de cadena y binaria se pueden truncar.</span><span class="sxs-lookup"><span data-stu-id="bb9c4-146">String and binary contents table columns can be truncated.</span></span> <span data-ttu-id="bb9c4-147">Normalmente, los proveedores devuelven 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="bb9c4-147">Typically, providers return 255 characters.</span></span> <span data-ttu-id="bb9c4-148">Debido a que no se conoce de antemano si una tabla incluye columnas truncadas, supongamos que una columna se trunca si la longitud de la columna es de 255 o 510 bytes.</span><span class="sxs-lookup"><span data-stu-id="bb9c4-148">Because you cannot know beforehand whether a table includes truncated columns, assume that a column is truncated if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="bb9c4-149">Siempre puede recuperar el valor completo de una columna truncada, si es necesario, directamente desde el objeto mediante su identificador de entrada para abrirlo y, a continuación, llamar al método [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="bb9c4-149">You can always retrieve the full value of a truncated column, if necessary, directly from the object by using its entry identifier to open it and then calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
<span data-ttu-id="bb9c4-150">Dependiendo del proveedor en la implementación, las restricciones y las operaciones de ordenación pueden aplicar a toda la cadena o a la versión truncada de dicha cadena.</span><span class="sxs-lookup"><span data-stu-id="bb9c4-150">Depending on the provider's implementation, restrictions and sorting operations can apply to the whole string or to the truncated version of that string.</span></span> <span data-ttu-id="bb9c4-151">Además, no se garantiza que los proveedores de almacén para respetar el conjunto de criterio de ordenación [que ssortorderset](ssortorderset.md) especificado para tablas de jerarquía.</span><span class="sxs-lookup"><span data-stu-id="bb9c4-151">Moreover, store providers are not guaranteed to honor the sort order set [SSortOrderSet](ssortorderset.md) specified for hierarchy tables.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="bb9c4-152">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="bb9c4-152">MFCMAPI reference</span></span>

<span data-ttu-id="bb9c4-153">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="bb9c4-153">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bb9c4-154">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="bb9c4-154">**File**</span></span>|<span data-ttu-id="bb9c4-155">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="bb9c4-155">**Function**</span></span>|<span data-ttu-id="bb9c4-156">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="bb9c4-156">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bb9c4-157">HierarchyTableTreeCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="bb9c4-157">HierarchyTableTreeCtrl.cpp</span></span>  <br/> |<span data-ttu-id="bb9c4-158">CHierarchyTableTreeCtrl::GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="bb9c4-158">CHierarchyTableTreeCtrl::GetHierarchyTable</span></span>  <br/> |<span data-ttu-id="bb9c4-159">La clase CHierarchyTableTreeCtrl utiliza **GetHierarchyTable** para obtener las tablas de jerarquía para mostrar en un control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="bb9c4-159">The CHierarchyTableTreeCtrl class uses **GetHierarchyTable** to obtain hierarchy tables to display in a tree view control.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bb9c4-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb9c4-160">See also</span></span>



[<span data-ttu-id="bb9c4-161">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="bb9c4-161">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="bb9c4-162">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="bb9c4-162">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="bb9c4-163">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bb9c4-163">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="bb9c4-164">Propiedad canónica PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="bb9c4-164">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="bb9c4-165">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="bb9c4-165">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="bb9c4-166">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="bb9c4-166">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

