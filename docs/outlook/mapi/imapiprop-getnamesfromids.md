---
title: IMAPIPropGetNamesFromIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetNamesFromIDs
api_type:
- COM
ms.assetid: 3efa4731-cf32-4a6c-9ba8-d059e58b0d98
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f6688afde9b36a7722eaaf768f091481c15b7308
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423576"
---
# <a name="imapipropgetnamesfromids"></a><span data-ttu-id="865a3-103">IMAPIProp::GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="865a3-103">IMAPIProp::GetNamesFromIDs</span></span>

  
  
<span data-ttu-id="865a3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="865a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="865a3-105">Proporciona los nombres de propiedad que corresponden a uno o más identificadores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="865a3-105">Provides the property names that correspond to one or more property identifiers.</span></span>
  
```cpp
HRESULT GetNamesFromIDs(
  LPSPropTagArray FAR * lppPropTags,
  LPGUID lpPropSetGuid,
  ULONG ulFlags,
  ULONG FAR * lpcPropNames,
  LPMAPINAMEID FAR * FAR * lpppPropNames
);
```

## <a name="parameters"></a><span data-ttu-id="865a3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="865a3-106">Parameters</span></span>

 <span data-ttu-id="865a3-107">_lppPropTags_</span><span class="sxs-lookup"><span data-stu-id="865a3-107">_lppPropTags_</span></span>
  
> <span data-ttu-id="865a3-108">[entrada, salida] En la entrada, un puntero a una [estructura SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas de propiedad; de lo contrario, NULL, que indica que se deben devolver todos los nombres.</span><span class="sxs-lookup"><span data-stu-id="865a3-108">[in, out] On input, a pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags; otherwise, NULL, indicating that all names should be returned.</span></span> <span data-ttu-id="865a3-109">El **miembro cValues** de la matriz de etiquetas de propiedades no puede ser 0.</span><span class="sxs-lookup"><span data-stu-id="865a3-109">The **cValues** member for the property tag array cannot be 0.</span></span> <span data-ttu-id="865a3-110">Si  _lppPropTags es_ un puntero válido en la entrada, **GetNamesFromIDs** devuelve nombres para cada identificador de propiedad incluido en la matriz.</span><span class="sxs-lookup"><span data-stu-id="865a3-110">If  _lppPropTags_ is a valid pointer on input, **GetNamesFromIDs** returns names for each property identifier included in the array.</span></span> 
    
 <span data-ttu-id="865a3-111">_lpPropSetGuid_</span><span class="sxs-lookup"><span data-stu-id="865a3-111">_lpPropSetGuid_</span></span>
  
> <span data-ttu-id="865a3-112">[entrada] Puntero a un GUID o estructura [GUID](guid.md) que identifica un conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="865a3-112">[in] A pointer to a GUID, or [GUID](guid.md) structure, that identifies a property set.</span></span> <span data-ttu-id="865a3-113">El  _parámetro lpPropSetGuid_ puede apuntar a un conjunto de propiedades válido o puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="865a3-113">The  _lpPropSetGuid_ parameter can point to a valid property set or can be NULL.</span></span> 
    
 <span data-ttu-id="865a3-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="865a3-114">_ulFlags_</span></span>
  
> <span data-ttu-id="865a3-115">[entrada] Máscara de bits de marcas que indica el tipo de nombres que se devolverán.</span><span class="sxs-lookup"><span data-stu-id="865a3-115">[in] A bitmask of flags that indicates the type of names to be returned.</span></span> <span data-ttu-id="865a3-116">Se pueden usar las siguientes marcas (si se establecen ambas marcas, no se devolverá ningún nombre):</span><span class="sxs-lookup"><span data-stu-id="865a3-116">The following flags can be used (if both flags are set, no names will be returned):</span></span>
    
<span data-ttu-id="865a3-117">MAPI_NO_IDS</span><span class="sxs-lookup"><span data-stu-id="865a3-117">MAPI_NO_IDS</span></span> 
  
> <span data-ttu-id="865a3-118">Solicita que solo se devuelvan los nombres almacenados como cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="865a3-118">Requests that only names stored as Unicode strings be returned.</span></span> 
    
<span data-ttu-id="865a3-119">MAPI_NO_STRINGS</span><span class="sxs-lookup"><span data-stu-id="865a3-119">MAPI_NO_STRINGS</span></span> 
  
> <span data-ttu-id="865a3-120">Solicita que solo se devuelvan los nombres almacenados como identificadores numéricos.</span><span class="sxs-lookup"><span data-stu-id="865a3-120">Requests that only names stored as numeric identifiers be returned.</span></span> 
    
 <span data-ttu-id="865a3-121">_lpcPropNames_</span><span class="sxs-lookup"><span data-stu-id="865a3-121">_lpcPropNames_</span></span>
  
> <span data-ttu-id="865a3-122">[salida] Puntero a un recuento de punteros de nombre de propiedad en la matriz a la que apunta el parámetro _lppPropNames._</span><span class="sxs-lookup"><span data-stu-id="865a3-122">[out] A pointer to a count of the property name pointers in the array pointed to by the  _lppPropNames_ parameter.</span></span> 
    
 <span data-ttu-id="865a3-123">_lpppPropNames_</span><span class="sxs-lookup"><span data-stu-id="865a3-123">_lpppPropNames_</span></span>
  
> <span data-ttu-id="865a3-124">[salida] Puntero a una matriz de punteros a estructuras [MAPINAMEID](mapinameid.md) que contienen nombres de propiedad.</span><span class="sxs-lookup"><span data-stu-id="865a3-124">[out] A pointer to an array of pointers to [MAPINAMEID](mapinameid.md) structures that contains property names.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="865a3-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="865a3-125">Return value</span></span>

<span data-ttu-id="865a3-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="865a3-126">S_OK</span></span> 
  
> <span data-ttu-id="865a3-127">Los nombres de las propiedades se devolvieron correctamente.</span><span class="sxs-lookup"><span data-stu-id="865a3-127">The property names were successfully returned.</span></span> 
    
<span data-ttu-id="865a3-128">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="865a3-128">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="865a3-129">El objeto no admite propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="865a3-129">The object does not support named properties.</span></span> 
    
<span data-ttu-id="865a3-130">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="865a3-130">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="865a3-131">La llamada se ha hecho correctamente en general, pero no se pudieron devolver los nombres de una o más propiedades.</span><span class="sxs-lookup"><span data-stu-id="865a3-131">The call succeeded overall, but names for one or more properties could not be returned.</span></span> <span data-ttu-id="865a3-132">Las etiquetas de propiedad de las propiedades con error tienen un tipo de propiedad **de PT_ERROR**.</span><span class="sxs-lookup"><span data-stu-id="865a3-132">The property tags for the failing properties have a property type of **PT_ERROR**.</span></span> <span data-ttu-id="865a3-133">Cuando se devuelve esta advertencia, la llamada debe tratarse como correcta.</span><span class="sxs-lookup"><span data-stu-id="865a3-133">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="865a3-134">Para probar esta advertencia, use la **macro HR_FAILED** datos.</span><span class="sxs-lookup"><span data-stu-id="865a3-134">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="865a3-135">Para obtener más información, vea [Usar macros para el control de errores.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="865a3-135">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span> 
    
<span data-ttu-id="865a3-136">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="865a3-136">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="865a3-137">El **miembro cValues** de una o varias de las entradas de la matriz de etiquetas de propiedades a las que  _apunta lppPropTags_ se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="865a3-137">The **cValues** member of one or more of the entries in the property tag array pointed to by  _lppPropTags_ is set to 0.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="865a3-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="865a3-138">Remarks</span></span>

<span data-ttu-id="865a3-139">Aunque el acceso a la mayoría de las propiedades es por identificador de propiedad, se puede tener acceso a algunas propiedades por nombre.</span><span class="sxs-lookup"><span data-stu-id="865a3-139">While access to most properties is by property identifier, some properties can be accessed by name.</span></span> <span data-ttu-id="865a3-140">Se puede llamar al método **IMAPIProp::GetNamesFromIDs** para hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="865a3-140">The **IMAPIProp::GetNamesFromIDs** method can be called to do the following:</span></span> 
  
- <span data-ttu-id="865a3-141">Recuperar nombres de identificadores de propiedad específicos en un conjunto de propiedades específico.</span><span class="sxs-lookup"><span data-stu-id="865a3-141">Retrieve names for specific property identifiers in a specific property set.</span></span>
    
- <span data-ttu-id="865a3-142">Recuperar nombres para identificadores de propiedad específicos en cualquier conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="865a3-142">Retrieve names for specific property identifiers in any property set.</span></span>
    
- <span data-ttu-id="865a3-143">Recupere los nombres de todas las propiedades con nombre que se incluyen en la asignación del objeto.</span><span class="sxs-lookup"><span data-stu-id="865a3-143">Retrieve names for all named properties that are included in the object's mapping.</span></span>
    
<span data-ttu-id="865a3-144">Si  _lppPropTags_ apunta a una matriz de etiquetas de propiedad válida con uno o más identificadores de propiedad y  _lpPropSetGuid_ apunta a un conjunto de propiedades válido, **GetNamesFromIDs** omite el conjunto de propiedades y los tipos de propiedad y devuelve todos los nombres que se asignan a los identificadores especificados.</span><span class="sxs-lookup"><span data-stu-id="865a3-144">If  _lppPropTags_ points to a valid property tag array with one or more property identifiers, and  _lpPropSetGuid_ points to a valid property set, **GetNamesFromIDs** ignores the property set and the property types and returns all of the names that map to the specified identifiers.</span></span> 
  
<span data-ttu-id="865a3-145">Si  _lppPropTags_ apunta a una matriz de etiquetas de propiedad válida con uno o más identificadores de propiedad y  _lpPropSetGuid_ es NULL, **GetNamesFromIDs** devuelve todos los nombres que se asignan a los identificadores especificados.</span><span class="sxs-lookup"><span data-stu-id="865a3-145">If  _lppPropTags_ points to a valid property tag array with one or more property identifiers and  _lpPropSetGuid_ is NULL, **GetNamesFromIDs** returns all of the names that map to the specified identifiers.</span></span> 
  
<span data-ttu-id="865a3-146">Si un identificador especificado no tiene un nombre, **GetNamesFromIDs** devuelve NULL en el lugar de ese identificador en la estructura devuelta en  _lpppPropNames_ y también devuelve MAPI_W_ERRORS_RETURNED.</span><span class="sxs-lookup"><span data-stu-id="865a3-146">If a specified identifier does not have a name, **GetNamesFromIDs** returns NULL in that identifier's place in the structure returned in  _lpppPropNames_ and also returns MAPI_W_ERRORS_RETURNED.</span></span> 
  
<span data-ttu-id="865a3-147">Si  _tanto lpPropSetGuid_ como  _lppPropTags_ son NULL, **GetNamesFromIDs** asigna una nueva matriz de etiquetas de propiedad y devuelve todos los nombres de todas las propiedades con nombre para el objeto.</span><span class="sxs-lookup"><span data-stu-id="865a3-147">If both  _lpPropSetGuid_ and  _lppPropTags_ are NULL, **GetNamesFromIDs** allocates a new property tag array and returns all of the names for all of the named properties for the object.</span></span> 
  
<span data-ttu-id="865a3-148">Cuando no hay nombres que devolver, quizás porque no hay propiedades en el conjunto de propiedades solicitadas o todas las propiedades son de un tipo excluido por las marcas, **GetNamesFromIDs** hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="865a3-148">When there are no names to be returned, perhaps because there are no properties in the requested property set or all of the properties are of a type excluded by the flags, **GetNamesFromIDs** does the following:</span></span> 
  
- <span data-ttu-id="865a3-149">Devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="865a3-149">Returns S_OK.</span></span>
    
- <span data-ttu-id="865a3-150">Asigna una nueva **estructura SPropTagArray,** estableciendo el **miembro cValues** en 0.</span><span class="sxs-lookup"><span data-stu-id="865a3-150">Allocates a new **SPropTagArray** structure, setting the **cValues** member to 0.</span></span> 
    
- <span data-ttu-id="865a3-151">Establece el contenido  _de lpcPropNames_ en 0.</span><span class="sxs-lookup"><span data-stu-id="865a3-151">Sets the contents of  _lpcPropNames_ to 0.</span></span> 
    
- <span data-ttu-id="865a3-152">Establece el contenido de  _lpppPropNames_ en NULL.</span><span class="sxs-lookup"><span data-stu-id="865a3-152">Sets the contents of  _lpppPropNames_ to NULL.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="865a3-153">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="865a3-153">Notes to implementers</span></span>

<span data-ttu-id="865a3-154">Si  _lpPropSetGuid_ apunta a un conjunto de propiedades válido y  _lppPropTags_ es NULL, el resultado es indefinido.</span><span class="sxs-lookup"><span data-stu-id="865a3-154">If  _lpPropSetGuid_ points to a valid property set and  _lppPropTags_ is NULL, the result is undefined.</span></span> <span data-ttu-id="865a3-155">Puede usar una de las siguientes estrategias:</span><span class="sxs-lookup"><span data-stu-id="865a3-155">You can use one of the following strategies:</span></span> 
  
- <span data-ttu-id="865a3-156">Ignore el conjunto de propiedades y devuelva los nombres de los identificadores de la matriz de etiquetas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="865a3-156">Ignore the property set and return the names for the identifiers in the property tag array.</span></span>
    
- <span data-ttu-id="865a3-157">Devuelve los nombres de solo los identificadores de la matriz de etiquetas de propiedades que pertenecen al conjunto de propiedades especificado.</span><span class="sxs-lookup"><span data-stu-id="865a3-157">Return the names for only the identifiers in the property tag array that belong to the specified property set.</span></span>
    
- <span data-ttu-id="865a3-158">Se producirá un error en la llamada, MAPI_E_INVALID_PARAMETER.</span><span class="sxs-lookup"><span data-stu-id="865a3-158">Fail the call, returning MAPI_E_INVALID_PARAMETER.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="865a3-159">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="865a3-159">Notes to callers</span></span>

<span data-ttu-id="865a3-160">Para recuperar todas las propiedades con nombre de un objeto, primero debe llamar al método [IMAPIProp::GetPropList](imapiprop-getproplist.md) del objeto y, a continuación, pasar los identificadores devueltos que están por encima del intervalo 0x8000 a **GetNamesFromIDs**.</span><span class="sxs-lookup"><span data-stu-id="865a3-160">To retrieve all of the named properties for an object, you must first call the object's [IMAPIProp::GetPropList](imapiprop-getproplist.md) method and then pass the returned identifiers that are above the 0x8000 range to **GetNamesFromIDs**.</span></span>
  
<span data-ttu-id="865a3-161">Si pasa un conjunto de propiedades válido pero no una matriz de etiquetas de propiedad válida, esté preparado para obtener resultados impredecibles.</span><span class="sxs-lookup"><span data-stu-id="865a3-161">If you pass a valid property set but not a valid property tag array, be prepared for unpredictable results.</span></span> <span data-ttu-id="865a3-162">Algunas implementaciones de **GetNamesFromIDs** omiten el conjunto de propiedades y devuelven los nombres de los identificadores de la matriz de etiquetas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="865a3-162">Some implementations of **GetNamesFromIDs** ignore the property set and return the names for the identifiers in the property tag array.</span></span> <span data-ttu-id="865a3-163">Algunas implementaciones devuelven MAPI_E_INVALID_PARAMETER.</span><span class="sxs-lookup"><span data-stu-id="865a3-163">Some implementations return MAPI_E_INVALID_PARAMETER.</span></span> <span data-ttu-id="865a3-164">Aún así, otras implementaciones devuelven nombres para identificadores de todas las propiedades del conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="865a3-164">Still other implementations return names for identifiers of all properties in the property set.</span></span> <span data-ttu-id="865a3-165">Si el conjunto de propiedades PS_PUBLIC_STRINGS, **GetNamesFromIDs** puede devolver todos los nombres que se crearon.</span><span class="sxs-lookup"><span data-stu-id="865a3-165">If the property set is PS_PUBLIC_STRINGS, **GetNamesFromIDs** can return all names that were ever created.</span></span> <span data-ttu-id="865a3-166">No importa si el proveedor de servicios almacena una propiedad en los identificadores asociados con las cadenas públicas.</span><span class="sxs-lookup"><span data-stu-id="865a3-166">Whether the service provider stores a property under the identifiers associated with the public strings is immaterial.</span></span> 
  
<span data-ttu-id="865a3-167">Cuando haya terminado con los nombres de propiedad, compruebe el contenido del parámetro  _lpcPropNames_ para determinar si se han devuelto nombres.</span><span class="sxs-lookup"><span data-stu-id="865a3-167">When you are finished with the property names, check the contents of the  _lpcPropNames_ parameter to determine whether any names were returned.</span></span> <span data-ttu-id="865a3-168">Si es así, llame a la función [MAPIFreeBuffer](mapifreebuffer.md) para liberar la memoria a la que  _apuntan lppPropTags_ y  _lpppPropNames_ cuando se devuelve un resultado correcto.</span><span class="sxs-lookup"><span data-stu-id="865a3-168">If so, call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the memory pointed to by  _lppPropTags_ and  _lpppPropNames_ when a successful result is returned.</span></span> <span data-ttu-id="865a3-169">Una llamada a **MAPIFreeBuffer** es suficiente para cada parámetro; No es necesario recorrer la matriz de punteros y liberar individualmente cada **estructura MAPINAMEID.**</span><span class="sxs-lookup"><span data-stu-id="865a3-169">One call to **MAPIFreeBuffer** is sufficient for each parameter; you do not have to traverse the array of pointers and free each **MAPINAMEID** structure individually.</span></span> 
  
<span data-ttu-id="865a3-170">Para obtener más información acerca de las propiedades con nombre, vea [propiedades con nombre MAPI](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="865a3-170">For more information about named properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="865a3-171">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="865a3-171">MFCMAPI reference</span></span>

<span data-ttu-id="865a3-172">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="865a3-172">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="865a3-173">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="865a3-173">**File**</span></span>|<span data-ttu-id="865a3-174">**Función**</span><span class="sxs-lookup"><span data-stu-id="865a3-174">**Function**</span></span>|<span data-ttu-id="865a3-175">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="865a3-175">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="865a3-176">SingleMAPIPropListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="865a3-176">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="865a3-177">CSingleMAPIPropListCtrl::FindAllNamedProps</span><span class="sxs-lookup"><span data-stu-id="865a3-177">CSingleMAPIPropListCtrl::FindAllNamedProps</span></span>  <br/> |<span data-ttu-id="865a3-178">MFCMAPI usa el **método IMAPIProp::GetNamesFromIDs** para buscar propiedades con nombre que se han asignado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="865a3-178">MFCMAPI uses the **IMAPIProp::GetNamesFromIDs** method to look up named properties that have previously been mapped.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="865a3-179">Consulte también</span><span class="sxs-lookup"><span data-stu-id="865a3-179">See also</span></span>



[<span data-ttu-id="865a3-180">GUID</span><span class="sxs-lookup"><span data-stu-id="865a3-180">GUID</span></span>](guid.md)
  
[<span data-ttu-id="865a3-181">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="865a3-181">IMAPIProp::GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md)
  
[<span data-ttu-id="865a3-182">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="865a3-182">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="865a3-183">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="865a3-183">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="865a3-184">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="865a3-184">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="865a3-185">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="865a3-185">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="865a3-186">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="865a3-186">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="865a3-187">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="865a3-187">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="865a3-188">Propiedades con nombre MAPI</span><span class="sxs-lookup"><span data-stu-id="865a3-188">MAPI Named Properties</span></span>](mapi-named-properties.md)
  
[<span data-ttu-id="865a3-189">Uso de macros para el control de errores</span><span class="sxs-lookup"><span data-stu-id="865a3-189">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

