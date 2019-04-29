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
ms.openlocfilehash: 28880b818bc80e31cae0c695d4aac92eb9555cac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433587"
---
# <a name="imapipropgetidsfromnames"></a><span data-ttu-id="2add4-103">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="2add4-103">IMAPIProp::GetIDsFromNames</span></span>

  
  
<span data-ttu-id="2add4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2add4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2add4-105">Proporciona los identificadores de propiedad que corresponden a uno o más nombres de propiedad.</span><span class="sxs-lookup"><span data-stu-id="2add4-105">Provides the property identifiers that correspond to one or more property names.</span></span>
  
```cpp
HRESULT GetIDsFromNames(
  ULONG cPropNames,
  LPMAPINAMEID FAR * lppPropNames,
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTags
);
```

## <a name="parameters"></a><span data-ttu-id="2add4-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="2add4-106">Parameters</span></span>

 <span data-ttu-id="2add4-107">_cPropNames_</span><span class="sxs-lookup"><span data-stu-id="2add4-107">_cPropNames_</span></span>
  
> <span data-ttu-id="2add4-108">a El número de nombres de propiedad a los que apunta el parámetro _lppPropNames_ .</span><span class="sxs-lookup"><span data-stu-id="2add4-108">[in] The count of property names pointed to by the  _lppPropNames_ parameter.</span></span> <span data-ttu-id="2add4-109">Si _lppPropNames_ es null, el parámetro _cPropNames_ debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="2add4-109">If  _lppPropNames_ is NULL, the  _cPropNames_ parameter must be 0.</span></span> 
    
 <span data-ttu-id="2add4-110">_lppPropNames_</span><span class="sxs-lookup"><span data-stu-id="2add4-110">_lppPropNames_</span></span>
  
> <span data-ttu-id="2add4-111">a Un puntero a una matriz de nombres de propiedad o NULL.</span><span class="sxs-lookup"><span data-stu-id="2add4-111">[in] A pointer to an array of property names, or NULL.</span></span> <span data-ttu-id="2add4-112">Pasar identificadores de propiedad de solicitudes NULL para todos los nombres de propiedad en todos los conjuntos de propiedades sobre los que el objeto tiene información.</span><span class="sxs-lookup"><span data-stu-id="2add4-112">Passing NULL requests property identifiers for all property names in all property sets about which the object has information.</span></span> <span data-ttu-id="2add4-113">El parámetro _lppPropNames_ no debe ser null si el indicador MAPI_CREATE está establecido en el parámetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="2add4-113">The  _lppPropNames_ parameter must not be NULL if the MAPI_CREATE flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="2add4-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2add4-114">_ulFlags_</span></span>
  
> <span data-ttu-id="2add4-115">a Máscara de máscara de marcadores que indica cómo se deben devolver los identificadores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="2add4-115">[in] A bitmask of flags that indicates how the property identifiers should be returned.</span></span> <span data-ttu-id="2add4-116">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="2add4-116">The following flag can be set:</span></span>
    
<span data-ttu-id="2add4-117">MAPI_CREATE</span><span class="sxs-lookup"><span data-stu-id="2add4-117">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="2add4-118">Asigna un identificador de propiedad, si aún no se ha asignado ninguno, a uno o varios de los nombres incluidos en la matriz de nombres de propiedad a la que apunta _lppPropNames_.</span><span class="sxs-lookup"><span data-stu-id="2add4-118">Assigns a property identifier, if one has not yet been assigned, to one or more of the names included in the property name array pointed to by  _lppPropNames_.</span></span> <span data-ttu-id="2add4-119">Esta marca registra internamente el identificador en la tabla de asignación de nombre a identificador.</span><span class="sxs-lookup"><span data-stu-id="2add4-119">This flag internally registers the identifier in the name-to-identifier mapping table.</span></span>
    
 <span data-ttu-id="2add4-120">_lppPropTags_</span><span class="sxs-lookup"><span data-stu-id="2add4-120">_lppPropTags_</span></span>
  
> <span data-ttu-id="2add4-121">contempla Un puntero a un puntero a una matriz de etiquetas de propiedad que contiene los identificadores de propiedad existentes o recién asignados.</span><span class="sxs-lookup"><span data-stu-id="2add4-121">[out] A pointer to a pointer to an array of property tags that contains existing or newly assigned property identifiers.</span></span> <span data-ttu-id="2add4-122">Los tipos de propiedad de las etiquetas de propiedad de esta matriz se establecen en **PT_UNSPECIFIED**.</span><span class="sxs-lookup"><span data-stu-id="2add4-122">The property types for the property tags in this array are set to **PT_UNSPECIFIED**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2add4-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2add4-123">Return value</span></span>

<span data-ttu-id="2add4-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="2add4-124">S_OK</span></span> 
  
> <span data-ttu-id="2add4-125">Los identificadores de los nombres de propiedad especificados se han devuelto correctamente.</span><span class="sxs-lookup"><span data-stu-id="2add4-125">The identifiers for the specified property names were successfully returned.</span></span>
    
<span data-ttu-id="2add4-126">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="2add4-126">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="2add4-127">El objeto no admite propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="2add4-127">The object does not support named properties.</span></span>
    
<span data-ttu-id="2add4-128">MAPI_E_NOT_ENOUGH_MEMORY</span><span class="sxs-lookup"><span data-stu-id="2add4-128">MAPI_E_NOT_ENOUGH_MEMORY</span></span> 
  
> <span data-ttu-id="2add4-129">Memoria inSuficiente para recuperar los identificadores.</span><span class="sxs-lookup"><span data-stu-id="2add4-129">Insufficient memory was available to retrieve the identifiers.</span></span>
    
<span data-ttu-id="2add4-130">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="2add4-130">MAPI_E_TOO_BIG</span></span> 
  
> <span data-ttu-id="2add4-131">No se puede realizar la operación porque requiere que se devuelvan demasiadas etiquetas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="2add4-131">The operation cannot be performed because it requires too many property tags to be returned.</span></span>
    
<span data-ttu-id="2add4-132">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="2add4-132">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="2add4-133">La llamada se realizó en general, pero no se pudieron devolver uno o más identificadores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="2add4-133">The call succeeded overall, but one or more property identifiers could not be returned.</span></span> <span data-ttu-id="2add4-134">El tipo de propiedad correspondiente para cada propiedad no disponible se establece en **PT_ERROR** y su identificador en cero.</span><span class="sxs-lookup"><span data-stu-id="2add4-134">The corresponding property type for each unavailable property is set to **PT_ERROR** and its identifier to zero.</span></span> <span data-ttu-id="2add4-135">Cuando se devuelve esta advertencia, controlar la llamada correctamente.</span><span class="sxs-lookup"><span data-stu-id="2add4-135">When this warning is returned, handle the call as successful.</span></span> <span data-ttu-id="2add4-136">Para probar esta advertencia, use la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="2add4-136">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="2add4-137">Consulte [uso de macros para el control de errores](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="2add4-137">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2add4-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2add4-138">Remarks</span></span>

<span data-ttu-id="2add4-139">El método **IMAPIProp:: GetIDsFromNames** recupera una matriz de etiquetas de propiedad que contiene los identificadores de propiedad para una o más propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="2add4-139">The **IMAPIProp::GetIDsFromNames** method retrieves an array of property tags that hold the property identifiers for one or more named properties.</span></span> <span data-ttu-id="2add4-140">Se puede llamar a **IMAPIProp:: GetIDsFromNames** para hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2add4-140">**IMAPIProp::GetIDsFromNames** can be called to do the following:</span></span> 
  
- <span data-ttu-id="2add4-141">Crear identificadores para los nombres nuevos.</span><span class="sxs-lookup"><span data-stu-id="2add4-141">Create identifiers for new names.</span></span>
    
- <span data-ttu-id="2add4-142">Recuperar identificadores para nombres específicos.</span><span class="sxs-lookup"><span data-stu-id="2add4-142">Retrieve identifiers for specific names.</span></span>
    
- <span data-ttu-id="2add4-143">Recupere los identificadores de todas las propiedades con nombre que se incluyen en la asignación del objeto.</span><span class="sxs-lookup"><span data-stu-id="2add4-143">Retrieve identifiers for all named properties that are included in the object's mapping.</span></span>
    
<span data-ttu-id="2add4-144">Los proveedores de almacenamiento de mensajes suelen usar las propiedades con nombre para las carpetas y los mensajes.</span><span class="sxs-lookup"><span data-stu-id="2add4-144">Named properties are typically used by message store providers for folders and messages.</span></span> <span data-ttu-id="2add4-145">Es posible que otros objetos, como usuarios de mensajería y secciones de perfil, no admitan la Asociación de nombres con los identificadores de propiedad y puedan devolver MAPI_E_NO_SUPPORT de **GetIDsFromNames**.</span><span class="sxs-lookup"><span data-stu-id="2add4-145">Other objects, such as messaging users and profile sections, might not support the association of names to property identifiers and might return MAPI_E_NO_SUPPORT from **GetIDsFromNames**.</span></span>
  
<span data-ttu-id="2add4-146">Si hay un error que devuelve un identificador para un nombre en particular, **GetIDsFromNames** devuelve MAPI_W_ERRORS_RETURNED y establece el tipo de propiedad en la entrada de matriz de etiquetas de propiedad que corresponde al nombre a **PT_ERROR** y el identificador a cero.</span><span class="sxs-lookup"><span data-stu-id="2add4-146">If there is an error that returns an identifier for a particular name, **GetIDsFromNames** returns MAPI_W_ERRORS_RETURNED and sets the property type in the property tag array entry that corresponds to the name to **PT_ERROR** and the identifier to zero.</span></span> 
  
<span data-ttu-id="2add4-147">La asignación de nombre a identificador se representa mediante la propiedad **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) de un objeto.</span><span class="sxs-lookup"><span data-stu-id="2add4-147">Name-to-identifier mapping is represented by an object's **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) property.</span></span> <span data-ttu-id="2add4-148">**PR_MAPPING_SIGNATURE** contiene una estructura [MAPIUID](mapiuid.md) que indica el proveedor de servicios responsable del objeto.</span><span class="sxs-lookup"><span data-stu-id="2add4-148">**PR_MAPPING_SIGNATURE** contains a [MAPIUID](mapiuid.md) structure that indicates the service provider responsible for the object.</span></span> <span data-ttu-id="2add4-149">Si la propiedad **PR_MAPPING_SIGNATURE** es la misma para dos objetos, supongamos que estos objetos usan la misma asignación de nombre a identificador.</span><span class="sxs-lookup"><span data-stu-id="2add4-149">If the **PR_MAPPING_SIGNATURE** property is the same for two objects, assume that these objects use the same name-to-identifier mapping.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="2add4-150">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="2add4-150">Notes to implementers</span></span>

<span data-ttu-id="2add4-151">Los identificadores que se devuelven en la matriz de etiquetas de propiedad a la que señala el parámetro _lppPropNames_ deben estar en el intervalo de 0X8000 a 0xFFFE.</span><span class="sxs-lookup"><span data-stu-id="2add4-151">The identifiers that you pass back in the property tag array pointed to by the  _lppPropNames_ parameter must be in the 0x8000 to 0xFFFE range.</span></span> <span data-ttu-id="2add4-152">Las entradas de esta matriz deben estar en el mismo orden que los nombres pasados en la matriz de nombres de propiedad a la que señala _lppPropNames_.</span><span class="sxs-lookup"><span data-stu-id="2add4-152">The entries in this array must be in the same order as the names passed in the property name array pointed to by  _lppPropNames_.</span></span> 
  
<span data-ttu-id="2add4-153">Si admite propiedades con nombre en un contenedor, use la misma asignación de nombre a identificador para todos los objetos del contenedor (es decir, no use una asignación diferente para cada carpeta del almacén de mensajes o cada mensaje de la carpeta).</span><span class="sxs-lookup"><span data-stu-id="2add4-153">If you support named properties on a container, use the same name-to-identifier mapping for all objects in your container (that is, do not use a different mapping for each folder in your message store or each message in your folder).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="2add4-154">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="2add4-154">Notes to callers</span></span>

<span data-ttu-id="2add4-155">Debido a que los tipos de propiedad de los identificadores devueltos en la matriz de etiquetas de propiedad a la que apunta _lppPropTags_ se establecen en **PT_UNSPECIFIED**, deberá llamar al método [IMAPIProp:: SetProps](imapiprop-setprops.md) para recuperar los tipos precisos.</span><span class="sxs-lookup"><span data-stu-id="2add4-155">Because the property types for the returned identifiers in the property tag array pointed to by  _lppPropTags_ are set to **PT_UNSPECIFIED**, you will have to call the [IMAPIProp::SetProps](imapiprop-setprops.md) method to retrieve the accurate types.</span></span> 
  
<span data-ttu-id="2add4-156">Si mueve o copia objetos con propiedades con nombre y los objetos de origen y de destino tienen distintas firmas de asignación, tal y como indican los valores de sus propiedades **PR_MAPPING_SIGNATURE** , debe conservar los nombres durante estas operaciones.</span><span class="sxs-lookup"><span data-stu-id="2add4-156">If you move or copy objects with named properties, and the source and destination objects have different mapping signatures as indicated by the values of their **PR_MAPPING_SIGNATURE** properties, you must preserve the names during these operations.</span></span> <span data-ttu-id="2add4-157">Para conservar los nombres de propiedad, ajuste los identificadores de propiedad correspondientes para que correspondan a la asignación de nombre a identificador del objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="2add4-157">To preserve property names, adjust the corresponding property identifiers to match the name-to-identifier mapping of the destination object.</span></span> 
  
<span data-ttu-id="2add4-158">Algunos objetos tienen un límite en cuanto al número de identificadores de propiedad a los que se puede asignar nombre.</span><span class="sxs-lookup"><span data-stu-id="2add4-158">Some objects have a limit as to the number of property identifiers they can name.</span></span> <span data-ttu-id="2add4-159">Si una llamada a **GetIDsFromNames** hace que se supere este límite, el método devuelve MAPI_E_TOO_BIG.</span><span class="sxs-lookup"><span data-stu-id="2add4-159">If a call to **GetIDsFromNames** causes this limit to be exceeded, the method returns MAPI_E_TOO_BIG.</span></span> <span data-ttu-id="2add4-160">En este caso, consulte por identificador.</span><span class="sxs-lookup"><span data-stu-id="2add4-160">In this case, query by identifier.</span></span> 
  
<span data-ttu-id="2add4-161">Para obtener más información, consulte [MAPI con nombre de propiedades](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="2add4-161">For more information, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2add4-162">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="2add4-162">MFCMAPI reference</span></span>

<span data-ttu-id="2add4-163">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="2add4-163">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2add4-164">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="2add4-164">**File**</span></span>|<span data-ttu-id="2add4-165">**Función**</span><span class="sxs-lookup"><span data-stu-id="2add4-165">**Function**</span></span>|<span data-ttu-id="2add4-166">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="2add4-166">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2add4-167">SingleMAPIPropListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="2add4-167">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="2add4-168">CSingleMAPIPropListCtrl:: FindAllNamedPropsUsed</span><span class="sxs-lookup"><span data-stu-id="2add4-168">CSingleMAPIPropListCtrl::FindAllNamedPropsUsed</span></span>  <br/> |<span data-ttu-id="2add4-169">MFCMAPI usa el método **IMAPIProp:: GetIDsFromNames** para obtener etiquetas de propiedad para todas las propiedades con nombre que se han asignado.</span><span class="sxs-lookup"><span data-stu-id="2add4-169">MFCMAPI uses the **IMAPIProp::GetIDsFromNames** method to obtain property tags for all named properties that have been mapped.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2add4-170">Ver también</span><span class="sxs-lookup"><span data-stu-id="2add4-170">See also</span></span>



[<span data-ttu-id="2add4-171">IMAPIProp::GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="2add4-171">IMAPIProp::GetNamesFromIDs</span></span>](imapiprop-getnamesfromids.md)
  
[<span data-ttu-id="2add4-172">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="2add4-172">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="2add4-173">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="2add4-173">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="2add4-174">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="2add4-174">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="2add4-175">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2add4-175">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="2add4-176">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="2add4-176">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="2add4-177">Propiedades con nombre MAPI</span><span class="sxs-lookup"><span data-stu-id="2add4-177">MAPI Named Properties</span></span>](mapi-named-properties.md)
  
[<span data-ttu-id="2add4-178">Uso de macros para el control de errores</span><span class="sxs-lookup"><span data-stu-id="2add4-178">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

