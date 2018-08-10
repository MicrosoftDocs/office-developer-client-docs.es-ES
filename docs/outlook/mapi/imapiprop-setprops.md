---
title: IMAPIPropSetProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.SetProps
api_type:
- COM
ms.assetid: 49f007c9-42e5-4391-8b83-988c9b0ebdba
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 304295e3ac77fb67ec5875620a7a269377b542c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817412"
---
# <a name="imapipropsetprops"></a><span data-ttu-id="2219b-103">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="2219b-103">IMAPIProp::SetProps</span></span>

  
  
<span data-ttu-id="2219b-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2219b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2219b-105">Actualiza las propiedades de uno o más.</span><span class="sxs-lookup"><span data-stu-id="2219b-105">Updates one or more properties.</span></span>
  
```cpp
HRESULT SetProps(
  ULONG cValues,
  LPSPropValue lpPropArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="2219b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2219b-106">Parameters</span></span>

 <span data-ttu-id="2219b-107">_cValues_</span><span class="sxs-lookup"><span data-stu-id="2219b-107">_cValues_</span></span>
  
> <span data-ttu-id="2219b-108">[entrada] El recuento de valores de la propiedad indicada por el parámetro _lpPropArray_ .</span><span class="sxs-lookup"><span data-stu-id="2219b-108">[in] The count of property values pointed to by the  _lpPropArray_ parameter.</span></span> <span data-ttu-id="2219b-109">El parámetro _cValues_ no debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="2219b-109">The  _cValues_ parameter must not be 0.</span></span> 
    
 <span data-ttu-id="2219b-110">_lpPropArray_</span><span class="sxs-lookup"><span data-stu-id="2219b-110">_lpPropArray_</span></span>
  
> <span data-ttu-id="2219b-111">[entrada] Un puntero a una matriz de estructuras [SPropValue](spropvalue.md) que contienen valores de propiedad para actualizarse.</span><span class="sxs-lookup"><span data-stu-id="2219b-111">[in] A pointer to an array of [SPropValue](spropvalue.md) structures that contain property values to be updated.</span></span> 
    
 <span data-ttu-id="2219b-112">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="2219b-112">_lppProblems_</span></span>
  
> <span data-ttu-id="2219b-113">[entrada, salida] En la entrada, un puntero a un puntero a una estructura [SPropProblemArray](spropproblemarray.md) ; de lo contrario, NULL, que indica que no hay necesidad de información de error.</span><span class="sxs-lookup"><span data-stu-id="2219b-113">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, indicating no need for error information.</span></span> <span data-ttu-id="2219b-114">Si _lppProblems_ es un puntero válido en la entrada, **SetProps** devuelve información detallada acerca de los errores en la actualización de una o más propiedades.</span><span class="sxs-lookup"><span data-stu-id="2219b-114">If  _lppProblems_ is a valid pointer on input, **SetProps** returns detailed information about errors in updating one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2219b-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2219b-115">Return value</span></span>

<span data-ttu-id="2219b-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="2219b-116">S_OK</span></span> 
  
> <span data-ttu-id="2219b-117">Las propiedades se han actualizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="2219b-117">The properties were successfully updated.</span></span>
    
<span data-ttu-id="2219b-118">Los siguientes valores se pueden devolver en la estructura de **SPropProblemArray** , pero no como valores devueltos por **SetProps**:</span><span class="sxs-lookup"><span data-stu-id="2219b-118">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **SetProps**:</span></span>
  
<span data-ttu-id="2219b-119">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="2219b-119">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="2219b-120">Se ha establecido el indicador MAPI_UNICODE y la implementación no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y la implementación admite sólo Unicode.</span><span class="sxs-lookup"><span data-stu-id="2219b-120">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="2219b-121">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="2219b-121">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="2219b-122">La propiedad no se puede actualizar porque es de sólo lectura, calculada por el proveedor de servicios que es responsable del objeto.</span><span class="sxs-lookup"><span data-stu-id="2219b-122">The property cannot be updated because it is read-only, computed by the service provider that is responsible for the object.</span></span>
    
<span data-ttu-id="2219b-123">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="2219b-123">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="2219b-124">El tipo de propiedad no es válido.</span><span class="sxs-lookup"><span data-stu-id="2219b-124">The property type is invalid.</span></span>
    
<span data-ttu-id="2219b-125">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="2219b-125">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="2219b-126">Se ha intentado para modificar un objeto de sólo lectura o para obtener acceso a un objeto para el que el usuario no tiene permisos suficientes.</span><span class="sxs-lookup"><span data-stu-id="2219b-126">An attempt was made to modify a read-only object or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="2219b-127">MAPI_E_NOT_ENOUGH_MEMORY</span><span class="sxs-lookup"><span data-stu-id="2219b-127">MAPI_E_NOT_ENOUGH_MEMORY</span></span> 
  
> <span data-ttu-id="2219b-128">La propiedad no se puede actualizar porque es mayor que el tamaño de búfer de procedimiento remoto (RPC) de la llamada.</span><span class="sxs-lookup"><span data-stu-id="2219b-128">The property cannot be updated because it is larger than the remote procedure call (RPC) buffer size.</span></span>
    
<span data-ttu-id="2219b-129">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="2219b-129">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="2219b-130">El tipo de propiedad no es el tipo esperado por la implementación de la llamada.</span><span class="sxs-lookup"><span data-stu-id="2219b-130">The property type is not the type expected by the calling implementation.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="2219b-131">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="2219b-131">Notes to implementers</span></span>

<span data-ttu-id="2219b-132">Omitir la etiqueta de propiedad de **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) y todas las propiedades con un tipo de **PT_ERROR**.</span><span class="sxs-lookup"><span data-stu-id="2219b-132">Ignore the **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) property tag and all properties with a type of **PT_ERROR**.</span></span> <span data-ttu-id="2219b-133">No realice cambios o informar de los problemas en la estructura **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="2219b-133">Do not make changes or report problems in the **SPropProblemArray** structure.</span></span> 
  
<span data-ttu-id="2219b-134">Devolver MAPI_E_INVALID_PARAMETER si una propiedad de tipo **pt Object** está incluida en la matriz de valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="2219b-134">Return MAPI_E_INVALID_PARAMETER if a property of type **PT_OBJECT** is included in the property value array.</span></span> <span data-ttu-id="2219b-135">También se devuelven este error si se incluye una propiedad de varios valores en la matriz y sus miembros **cValues** se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="2219b-135">Also return this error if a multiple-value property is included in the array and its **cValues** member is set to 0.</span></span> 
  
<span data-ttu-id="2219b-136">Si la llamada se realiza correctamente en general, pero hay problemas con la configuración de algunas de las propiedades, devuelve S_OK y colocar la información acerca de los problemas en la entrada correspondiente de la estructura de **SPropProblemArray** que señala el parámetro _lppProblems_ .</span><span class="sxs-lookup"><span data-stu-id="2219b-136">If the call succeeds overall but there are problems with setting some of the properties, return S_OK and put information about the problems in the appropriate entry of the **SPropProblemArray** structure that the  _lppProblems_ parameter points to.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2219b-137">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="2219b-137">Notes to callers</span></span>

<span data-ttu-id="2219b-138">Según el proveedor de servicio, es posible que también podrá cambiar el tipo de propiedad, se pasa una etiqueta de propiedad que contiene un tipo diferente que se utilizó anteriormente con un identificador de la propiedad determinada.</span><span class="sxs-lookup"><span data-stu-id="2219b-138">Depending on the service provider, you might also be able to change the property type by passing a property tag that contains a different type than was previously used with a given property identifier.</span></span>
  
<span data-ttu-id="2219b-139">Si incluye una etiqueta de propiedad para una propiedad que no es compatible con el objeto y la implementación de **SetProps** permite la creación de nuevas propiedades, la propiedad se agrega al objeto.</span><span class="sxs-lookup"><span data-stu-id="2219b-139">If you include a property tag for a property that is unsupported by the object and the implementation of **SetProps** allows the creation of new properties, the property is added to the object.</span></span> <span data-ttu-id="2219b-140">Se descarta cualquier valor anterior almacenado con el identificador de la propiedad que se usó para la nueva propiedad.</span><span class="sxs-lookup"><span data-stu-id="2219b-140">Any previous value stored with the property identifier that was used for the new property is discarded.</span></span> 
  
<span data-ttu-id="2219b-141">Tenga en cuenta que el valor devuelto de S_OK no garantiza que todas las propiedades se han actualizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="2219b-141">Note that the S_OK return value does not guarantee that all of the properties were successfully updated.</span></span> <span data-ttu-id="2219b-142">Algunos proveedores de la memoria caché **SetProps** llamadas hasta que reciben una llamada que requiere la intervención del proveedor, como [IMAPIProp::SaveChanges](imapiprop-savechanges.md) o [IMAPIProp::GetProps](imapiprop-getprops.md).</span><span class="sxs-lookup"><span data-stu-id="2219b-142">Some providers cache **SetProps** calls until they receive a call that requires provider intervention, such as [IMAPIProp::SaveChanges](imapiprop-savechanges.md) or [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span> <span data-ttu-id="2219b-143">Por lo tanto, es posible recibir los valores de error que se relacionan con la llamada **SetProps** con las llamadas posteriores.</span><span class="sxs-lookup"><span data-stu-id="2219b-143">Therefore, it is possible to receive error values that relate to the **SetProps** call with the later calls.</span></span> 
  
<span data-ttu-id="2219b-144">Si **SetProps** devuelve S_OK, compruebe la estructura de **SPropProblemArray** que señala _lppProblems_ para problemas de actualización de las propiedades individuales.</span><span class="sxs-lookup"><span data-stu-id="2219b-144">If **SetProps** returns S_OK, check the **SPropProblemArray** structure pointed to by  _lppProblems_ for problems updating individual properties.</span></span> <span data-ttu-id="2219b-145">Si **SetProps** devuelve un error, no comprobar la matriz de problema (propiedad).</span><span class="sxs-lookup"><span data-stu-id="2219b-145">If **SetProps** returns an error, do not check the property problem array.</span></span> <span data-ttu-id="2219b-146">En su lugar, llame al método del objeto [IMAPIProp::GetLastError](imapiprop-getlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="2219b-146">Instead, call the object's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method.</span></span> 
  
<span data-ttu-id="2219b-147">Al actualizar las propiedades de gran tamaño, **SetProps** puede producir un error y devolver MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="2219b-147">When updating large properties, **SetProps** can fail and return MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="2219b-148">No hay ningún tamaño máximo para las propiedades y objetos diferentes pueden tener distintos límites.</span><span class="sxs-lookup"><span data-stu-id="2219b-148">There is no maximum size for properties, and different objects can have different limits.</span></span> <span data-ttu-id="2219b-149">Si se trabaja con las propiedades potencialmente grandes, estar preparado para llamar al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) con IID_IStream como el identificador de interfaz si **SetProps** devuelve este valor de error.</span><span class="sxs-lookup"><span data-stu-id="2219b-149">If you deal with potentially large properties, be prepared to call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with IID_IStream as the interface identifier if **SetProps** returns this error value.</span></span> 
  
<span data-ttu-id="2219b-150">Llame a la función [MAPIFreeBuffer](mapifreebuffer.md) para liberar la estructura **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="2219b-150">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the **SPropProblemArray** structure.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2219b-151">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="2219b-151">MFCMAPI reference</span></span>

<span data-ttu-id="2219b-152">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="2219b-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2219b-153">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="2219b-153">**File**</span></span>|<span data-ttu-id="2219b-154">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="2219b-154">**Function**</span></span>|<span data-ttu-id="2219b-155">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="2219b-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2219b-156">PropertyEditor.cpp</span><span class="sxs-lookup"><span data-stu-id="2219b-156">PropertyEditor.cpp</span></span>  <br/> |<span data-ttu-id="2219b-157">CPropertyEditor::WriteSPropValueToObject</span><span class="sxs-lookup"><span data-stu-id="2219b-157">CPropertyEditor::WriteSPropValueToObject</span></span>  <br/> |<span data-ttu-id="2219b-158">MFCMAPI usa el método **IMAPIProp::SetProps** volver a escribir una propiedad en un objeto después de que la propiedad se ha editado.</span><span class="sxs-lookup"><span data-stu-id="2219b-158">MFCMAPI uses the **IMAPIProp::SetProps** method to write a property back to an object after the property has been edited.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2219b-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="2219b-159">See also</span></span>



[<span data-ttu-id="2219b-160">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="2219b-160">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="2219b-161">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="2219b-161">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="2219b-162">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="2219b-162">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="2219b-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="2219b-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="2219b-164">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="2219b-164">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="2219b-165">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="2219b-165">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="2219b-166">SPropValue</span><span class="sxs-lookup"><span data-stu-id="2219b-166">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="2219b-167">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2219b-167">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)

