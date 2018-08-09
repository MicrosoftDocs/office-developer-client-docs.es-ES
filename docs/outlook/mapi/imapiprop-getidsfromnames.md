---
title: IMAPIPropGetIDsFromNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetIDsFromNames
api_type:
- COM
ms.assetid: e3f501a4-a8ee-43d7-bd83-c94e7980c398
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5247ca71c88b9c0f8591a732746a17204265741c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817414"
---
# <a name="imapipropgetidsfromnames"></a><span data-ttu-id="95d49-103">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="95d49-103">IMAPIProp::GetIDsFromNames</span></span>

  
  
<span data-ttu-id="95d49-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="95d49-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="95d49-105">Proporciona los identificadores de propiedad que se corresponden con uno o varios nombres de propiedad.</span><span class="sxs-lookup"><span data-stu-id="95d49-105">Provides the property identifiers that correspond to one or more property names.</span></span>
  
```cpp
HRESULT GetIDsFromNames(
  ULONG cPropNames,
  LPMAPINAMEID FAR * lppPropNames,
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTags
);
```

## <a name="parameters"></a><span data-ttu-id="95d49-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="95d49-106">Parameters</span></span>

 <span data-ttu-id="95d49-107">_cPropNames_</span><span class="sxs-lookup"><span data-stu-id="95d49-107">_cPropNames_</span></span>
  
> <span data-ttu-id="95d49-108">[entrada] El recuento de nombres de propiedad que señala el parámetro _lppPropNames_ .</span><span class="sxs-lookup"><span data-stu-id="95d49-108">[in] The count of property names pointed to by the  _lppPropNames_ parameter.</span></span> <span data-ttu-id="95d49-109">Si _lppPropNames_ es NULL, el parámetro _cPropNames_ debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="95d49-109">If  _lppPropNames_ is NULL, the  _cPropNames_ parameter must be 0.</span></span> 
    
 <span data-ttu-id="95d49-110">_lppPropNames_</span><span class="sxs-lookup"><span data-stu-id="95d49-110">_lppPropNames_</span></span>
  
> <span data-ttu-id="95d49-111">[entrada] Un puntero a una matriz de nombres de propiedad o NULL.</span><span class="sxs-lookup"><span data-stu-id="95d49-111">[in] A pointer to an array of property names, or NULL.</span></span> <span data-ttu-id="95d49-112">Si se pasa NULL solicita identificadores de propiedad para todos los nombres de propiedad en todos los conjuntos de propiedades acerca de que el objeto tiene información.</span><span class="sxs-lookup"><span data-stu-id="95d49-112">Passing NULL requests property identifiers for all property names in all property sets about which the object has information.</span></span> <span data-ttu-id="95d49-113">El parámetro _lppPropNames_ no debe ser NULL si la marca MAPI_CREATE se establece en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="95d49-113">The  _lppPropNames_ parameter must not be NULL if the MAPI_CREATE flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="95d49-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="95d49-114">_ulFlags_</span></span>
  
> <span data-ttu-id="95d49-115">[entrada] Una máscara de bits de marcadores que indica cómo se deben devolver los identificadores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="95d49-115">[in] A bitmask of flags that indicates how the property identifiers should be returned.</span></span> <span data-ttu-id="95d49-116">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="95d49-116">The following flag can be set:</span></span>
    
<span data-ttu-id="95d49-117">MAPI_CREATE</span><span class="sxs-lookup"><span data-stu-id="95d49-117">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="95d49-118">Asigna un identificador de la propiedad, si uno aún no se ha asignado, a uno o varios de los nombres incluidos en la matriz de nombre de propiedad que señala _lppPropNames_.</span><span class="sxs-lookup"><span data-stu-id="95d49-118">Assigns a property identifier, if one has not yet been assigned, to one or more of the names included in the property name array pointed to by  _lppPropNames_.</span></span> <span data-ttu-id="95d49-119">Esta marca internamente registra el identificador en la tabla de asignación de nombre a identificador.</span><span class="sxs-lookup"><span data-stu-id="95d49-119">This flag internally registers the identifier in the name-to-identifier mapping table.</span></span>
    
 <span data-ttu-id="95d49-120">_lppPropTags_</span><span class="sxs-lookup"><span data-stu-id="95d49-120">_lppPropTags_</span></span>
  
> <span data-ttu-id="95d49-121">[out] Un puntero a un puntero a una matriz de etiquetas (propiedad) que contiene los identificadores de propiedad existente o recién asignados.</span><span class="sxs-lookup"><span data-stu-id="95d49-121">[out] A pointer to a pointer to an array of property tags that contains existing or newly assigned property identifiers.</span></span> <span data-ttu-id="95d49-122">Los tipos de propiedad para las etiquetas de propiedad de esta matriz se establecen en **PT_UNSPECIFIED**.</span><span class="sxs-lookup"><span data-stu-id="95d49-122">The property types for the property tags in this array are set to **PT_UNSPECIFIED**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="95d49-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="95d49-123">Return value</span></span>

<span data-ttu-id="95d49-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="95d49-124">S_OK</span></span> 
  
> <span data-ttu-id="95d49-125">Los identificadores de los nombres de propiedad especificado correctamente se han devuelto.</span><span class="sxs-lookup"><span data-stu-id="95d49-125">The identifiers for the specified property names were successfully returned.</span></span>
    
<span data-ttu-id="95d49-126">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="95d49-126">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="95d49-127">El objeto no admite propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="95d49-127">The object does not support named properties.</span></span>
    
<span data-ttu-id="95d49-128">MAPI_E_NOT_ENOUGH_MEMORY</span><span class="sxs-lookup"><span data-stu-id="95d49-128">MAPI_E_NOT_ENOUGH_MEMORY</span></span> 
  
> <span data-ttu-id="95d49-129">Memoria insuficiente estaba disponible para recuperar los identificadores.</span><span class="sxs-lookup"><span data-stu-id="95d49-129">Insufficient memory was available to retrieve the identifiers.</span></span>
    
<span data-ttu-id="95d49-130">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="95d49-130">MAPI_E_TOO_BIG</span></span> 
  
> <span data-ttu-id="95d49-131">No se puede realizar la operación, ya que requiere demasiadas etiquetas de propiedad que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="95d49-131">The operation cannot be performed because it requires too many property tags to be returned.</span></span>
    
<span data-ttu-id="95d49-132">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="95d49-132">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="95d49-133">La llamada satisfactoria, pero no se podrían devolver uno o varios identificadores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="95d49-133">The call succeeded overall, but one or more property identifiers could not be returned.</span></span> <span data-ttu-id="95d49-134">El tipo de propiedad correspondiente para cada propiedad no está disponible se establece en **PT_ERROR** y su identificador en cero.</span><span class="sxs-lookup"><span data-stu-id="95d49-134">The corresponding property type for each unavailable property is set to **PT_ERROR** and its identifier to zero.</span></span> <span data-ttu-id="95d49-135">Cuando se devuelve esta advertencia, controlar la llamada como correcta.</span><span class="sxs-lookup"><span data-stu-id="95d49-135">When this warning is returned, handle the call as successful.</span></span> <span data-ttu-id="95d49-136">Para probar esta advertencia, utilice la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="95d49-136">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="95d49-137">Vea [uso de Macros para el tratamiento de errores](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="95d49-137">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="95d49-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="95d49-138">Remarks</span></span>

<span data-ttu-id="95d49-139">El método **IMAPIProp::GetIDsFromNames** recupera una matriz de etiquetas de propiedad que mantenga los identificadores de propiedad para una o varias propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="95d49-139">The **IMAPIProp::GetIDsFromNames** method retrieves an array of property tags that hold the property identifiers for one or more named properties.</span></span> <span data-ttu-id="95d49-140">Puede llamar a **IMAPIProp::GetIDsFromNames** para hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="95d49-140">**IMAPIProp::GetIDsFromNames** can be called to do the following:</span></span> 
  
- <span data-ttu-id="95d49-141">Crear identificadores para nombres nuevos.</span><span class="sxs-lookup"><span data-stu-id="95d49-141">Create identifiers for new names.</span></span>
    
- <span data-ttu-id="95d49-142">Recuperar identificadores de nombres específicos.</span><span class="sxs-lookup"><span data-stu-id="95d49-142">Retrieve identifiers for specific names.</span></span>
    
- <span data-ttu-id="95d49-143">Recuperar los identificadores de todas las propiedades con nombre que se incluyen en la asignación del objeto.</span><span class="sxs-lookup"><span data-stu-id="95d49-143">Retrieve identifiers for all named properties that are included in the object's mapping.</span></span>
    
<span data-ttu-id="95d49-144">Propiedades con nombre se usan normalmente por los proveedores de almacén de mensajes para las carpetas y mensajes.</span><span class="sxs-lookup"><span data-stu-id="95d49-144">Named properties are typically used by message store providers for folders and messages.</span></span> <span data-ttu-id="95d49-145">Otros objetos, como la mensajería de los usuarios y las secciones de perfil, puede que no admita la asociación de los nombres de los identificadores de propiedades y podrían devolver MAPI_E_NO_SUPPORT de **a GetIDsFromNames**.</span><span class="sxs-lookup"><span data-stu-id="95d49-145">Other objects, such as messaging users and profile sections, might not support the association of names to property identifiers and might return MAPI_E_NO_SUPPORT from **GetIDsFromNames**.</span></span>
  
<span data-ttu-id="95d49-146">Si se ha producido un error que devuelve un identificador para un nombre en particular, **a GetIDsFromNames** devuelve MAPI_W_ERRORS_RETURNED y establece el tipo de propiedad en la entrada de matriz de etiqueta de propiedad que se corresponde con el nombre **PT_ERROR** y el identificador a cero.</span><span class="sxs-lookup"><span data-stu-id="95d49-146">If there is an error that returns an identifier for a particular name, **GetIDsFromNames** returns MAPI_W_ERRORS_RETURNED and sets the property type in the property tag array entry that corresponds to the name to **PT_ERROR** and the identifier to zero.</span></span> 
  
<span data-ttu-id="95d49-147">Asignación de nombre a identificador está representado por una propiedad del objeto **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="95d49-147">Name-to-identifier mapping is represented by an object's **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) property.</span></span> <span data-ttu-id="95d49-148">**PR_MAPPING_SIGNATURE** contiene una estructura [MAPIUID](mapiuid.md) que indica el proveedor de servicio responsable del objeto.</span><span class="sxs-lookup"><span data-stu-id="95d49-148">**PR_MAPPING_SIGNATURE** contains a [MAPIUID](mapiuid.md) structure that indicates the service provider responsible for the object.</span></span> <span data-ttu-id="95d49-149">Si la propiedad **PR_MAPPING_SIGNATURE** es el mismo para dos objetos, se supone que estos objetos utilizan la misma asignación de nombre a identificador.</span><span class="sxs-lookup"><span data-stu-id="95d49-149">If the **PR_MAPPING_SIGNATURE** property is the same for two objects, assume that these objects use the same name-to-identifier mapping.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="95d49-150">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="95d49-150">Notes to implementers</span></span>

<span data-ttu-id="95d49-151">Los identificadores que se pasan en la matriz de etiqueta de la propiedad indicada por el parámetro _lppPropNames_ deben estar en el intervalo de 0 x 8000 a 0xFFFE.</span><span class="sxs-lookup"><span data-stu-id="95d49-151">The identifiers that you pass back in the property tag array pointed to by the  _lppPropNames_ parameter must be in the 0x8000 to 0xFFFE range.</span></span> <span data-ttu-id="95d49-152">Las entradas de esta matriz deben estar en el mismo orden que los nombres pasados en la matriz de nombre de la propiedad indicadas por _lppPropNames_.</span><span class="sxs-lookup"><span data-stu-id="95d49-152">The entries in this array must be in the same order as the names passed in the property name array pointed to by  _lppPropNames_.</span></span> 
  
<span data-ttu-id="95d49-153">Si decide admitir propiedades con nombre en un contenedor, utilice la misma asignación de nombre a identificador para todos los objetos en el contenedor (es decir, no use una asignación distinta para cada carpeta en el almacén de mensajes o cada mensaje en la carpeta).</span><span class="sxs-lookup"><span data-stu-id="95d49-153">If you support named properties on a container, use the same name-to-identifier mapping for all objects in your container (that is, do not use a different mapping for each folder in your message store or each message in your folder).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="95d49-154">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="95d49-154">Notes to callers</span></span>

<span data-ttu-id="95d49-155">Debido a que los tipos de propiedad para los identificadores devueltos en la matriz de etiqueta de propiedad que señala _lppPropTags_ se establecen en **PT_UNSPECIFIED**, debe llamar al método [IMAPIProp::SetProps](imapiprop-setprops.md) para recuperar los tipos precisos.</span><span class="sxs-lookup"><span data-stu-id="95d49-155">Because the property types for the returned identifiers in the property tag array pointed to by  _lppPropTags_ are set to **PT_UNSPECIFIED**, you will have to call the [IMAPIProp::SetProps](imapiprop-setprops.md) method to retrieve the accurate types.</span></span> 
  
<span data-ttu-id="95d49-156">Si mover o copiar objetos con propiedades con nombre y los objetos de origen y de destino tienen firmas de asignación distinta indicada por los valores de sus propiedades **PR_MAPPING_SIGNATURE** , debe conservar los nombres durante estas operaciones.</span><span class="sxs-lookup"><span data-stu-id="95d49-156">If you move or copy objects with named properties, and the source and destination objects have different mapping signatures as indicated by the values of their **PR_MAPPING_SIGNATURE** properties, you must preserve the names during these operations.</span></span> <span data-ttu-id="95d49-157">Para conservar los nombres de propiedad, ajustar los identificadores de propiedad correspondientes para que coincidan con la asignación del identificador del nombre del objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="95d49-157">To preserve property names, adjust the corresponding property identifiers to match the name-to-identifier mapping of the destination object.</span></span> 
  
<span data-ttu-id="95d49-158">Algunos objetos tienen un límite en el número de identificadores de propiedad que se puede asignar el nombre.</span><span class="sxs-lookup"><span data-stu-id="95d49-158">Some objects have a limit as to the number of property identifiers they can name.</span></span> <span data-ttu-id="95d49-159">Si una llamada a **GetIDsFromNames** hace que se supere este límite, el método devuelve MAPI_E_TOO_BIG.</span><span class="sxs-lookup"><span data-stu-id="95d49-159">If a call to **GetIDsFromNames** causes this limit to be exceeded, the method returns MAPI_E_TOO_BIG.</span></span> <span data-ttu-id="95d49-160">En este caso, la consulta por identificador.</span><span class="sxs-lookup"><span data-stu-id="95d49-160">In this case, query by identifier.</span></span> 
  
<span data-ttu-id="95d49-161">Para obtener más información, vea [Propiedades de nombre de MAPI](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="95d49-161">For more information, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="95d49-162">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="95d49-162">MFCMAPI reference</span></span>

<span data-ttu-id="95d49-163">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="95d49-163">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="95d49-164">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="95d49-164">**File**</span></span>|<span data-ttu-id="95d49-165">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="95d49-165">**Function**</span></span>|<span data-ttu-id="95d49-166">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="95d49-166">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="95d49-167">SingleMAPIPropListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="95d49-167">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="95d49-168">CSingleMAPIPropListCtrl::FindAllNamedPropsUsed</span><span class="sxs-lookup"><span data-stu-id="95d49-168">CSingleMAPIPropListCtrl::FindAllNamedPropsUsed</span></span>  <br/> |<span data-ttu-id="95d49-169">MFCMAPI utiliza el método **IMAPIProp::GetIDsFromNames** para obtener las etiquetas de propiedad para todas las propiedades con nombre que se han asignado.</span><span class="sxs-lookup"><span data-stu-id="95d49-169">MFCMAPI uses the **IMAPIProp::GetIDsFromNames** method to obtain property tags for all named properties that have been mapped.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="95d49-170">Vea también</span><span class="sxs-lookup"><span data-stu-id="95d49-170">See also</span></span>



[<span data-ttu-id="95d49-171">IMAPIProp::GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="95d49-171">IMAPIProp::GetNamesFromIDs</span></span>](imapiprop-getnamesfromids.md)
  
[<span data-ttu-id="95d49-172">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="95d49-172">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="95d49-173">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="95d49-173">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="95d49-174">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="95d49-174">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="95d49-175">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="95d49-175">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="95d49-176">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="95d49-176">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="95d49-177">Con el nombre de las propiedades de MAPI</span><span class="sxs-lookup"><span data-stu-id="95d49-177">MAPI Named Properties</span></span>](mapi-named-properties.md)
  
[<span data-ttu-id="95d49-178">Uso de macros para el control de errores</span><span class="sxs-lookup"><span data-stu-id="95d49-178">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

