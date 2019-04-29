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
ms.openlocfilehash: 87709f8a77471637d7652982669bcba93ca2e1dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412621"
---
# <a name="imapipropsetprops"></a><span data-ttu-id="49fac-103">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="49fac-103">IMAPIProp::SetProps</span></span>

  
  
<span data-ttu-id="49fac-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="49fac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="49fac-105">Actualiza una o más propiedades.</span><span class="sxs-lookup"><span data-stu-id="49fac-105">Updates one or more properties.</span></span>
  
```cpp
HRESULT SetProps(
  ULONG cValues,
  LPSPropValue lpPropArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="49fac-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="49fac-106">Parameters</span></span>

 <span data-ttu-id="49fac-107">_cValues_</span><span class="sxs-lookup"><span data-stu-id="49fac-107">_cValues_</span></span>
  
> <span data-ttu-id="49fac-108">a El número de valores de propiedad a los que apunta el parámetro _lpPropArray_ .</span><span class="sxs-lookup"><span data-stu-id="49fac-108">[in] The count of property values pointed to by the  _lpPropArray_ parameter.</span></span> <span data-ttu-id="49fac-109">El parámetro _cValues_ no debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="49fac-109">The  _cValues_ parameter must not be 0.</span></span> 
    
 <span data-ttu-id="49fac-110">_lpPropArray_</span><span class="sxs-lookup"><span data-stu-id="49fac-110">_lpPropArray_</span></span>
  
> <span data-ttu-id="49fac-111">a Un puntero a una matriz de estructuras [SPropValue](spropvalue.md) que contiene los valores de propiedad que se van a actualizar.</span><span class="sxs-lookup"><span data-stu-id="49fac-111">[in] A pointer to an array of [SPropValue](spropvalue.md) structures that contain property values to be updated.</span></span> 
    
 <span data-ttu-id="49fac-112">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="49fac-112">_lppProblems_</span></span>
  
> <span data-ttu-id="49fac-113">[in, out] En la entrada, un puntero a un puntero a una estructura [SPropProblemArray](spropproblemarray.md) ; de lo contrario, NULL, que indica que no es necesaria información de error.</span><span class="sxs-lookup"><span data-stu-id="49fac-113">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, indicating no need for error information.</span></span> <span data-ttu-id="49fac-114">Si _lppProblems_ es un puntero válido en la entrada, **SetProps** devuelve información detallada sobre los errores de actualización de una o varias propiedades.</span><span class="sxs-lookup"><span data-stu-id="49fac-114">If  _lppProblems_ is a valid pointer on input, **SetProps** returns detailed information about errors in updating one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="49fac-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="49fac-115">Return value</span></span>

<span data-ttu-id="49fac-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="49fac-116">S_OK</span></span> 
  
> <span data-ttu-id="49fac-117">Las propiedades se actualizaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="49fac-117">The properties were successfully updated.</span></span>
    
<span data-ttu-id="49fac-118">Los valores siguientes se pueden devolver en la estructura **SPropProblemArray** , pero no como valores devueltos para **SetProps**:</span><span class="sxs-lookup"><span data-stu-id="49fac-118">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **SetProps**:</span></span>
  
<span data-ttu-id="49fac-119">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="49fac-119">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="49fac-120">Se estableció la marca MAPI_UNICODE y la implementación no admite Unicode, o no se estableció MAPI_UNICODE y la implementación solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="49fac-120">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="49fac-121">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="49fac-121">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="49fac-122">La propiedad no se puede actualizar porque es de solo lectura, calculada por el proveedor de servicios responsable del objeto.</span><span class="sxs-lookup"><span data-stu-id="49fac-122">The property cannot be updated because it is read-only, computed by the service provider that is responsible for the object.</span></span>
    
<span data-ttu-id="49fac-123">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="49fac-123">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="49fac-124">El tipo de propiedad no es válido.</span><span class="sxs-lookup"><span data-stu-id="49fac-124">The property type is invalid.</span></span>
    
<span data-ttu-id="49fac-125">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="49fac-125">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="49fac-126">Se ha intentado modificar un objeto de solo lectura o tener acceso a un objeto para el que el usuario no tiene permisos suficientes.</span><span class="sxs-lookup"><span data-stu-id="49fac-126">An attempt was made to modify a read-only object or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="49fac-127">MAPI_E_NOT_ENOUGH_MEMORY</span><span class="sxs-lookup"><span data-stu-id="49fac-127">MAPI_E_NOT_ENOUGH_MEMORY</span></span> 
  
> <span data-ttu-id="49fac-128">La propiedad no se puede actualizar porque es mayor que el tamaño del búfer de la llamada a procedimiento remoto (RPC).</span><span class="sxs-lookup"><span data-stu-id="49fac-128">The property cannot be updated because it is larger than the remote procedure call (RPC) buffer size.</span></span>
    
<span data-ttu-id="49fac-129">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="49fac-129">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="49fac-130">El tipo de propiedad no es el tipo esperado por la implementación que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="49fac-130">The property type is not the type expected by the calling implementation.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="49fac-131">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="49fac-131">Notes to implementers</span></span>

<span data-ttu-id="49fac-132">Ignore la etiqueta de propiedad **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) y todas las propiedades con un tipo de **PT_ERROR**.</span><span class="sxs-lookup"><span data-stu-id="49fac-132">Ignore the **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) property tag and all properties with a type of **PT_ERROR**.</span></span> <span data-ttu-id="49fac-133">No realice cambios ni informe de problemas en la estructura **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="49fac-133">Do not make changes or report problems in the **SPropProblemArray** structure.</span></span> 
  
<span data-ttu-id="49fac-134">Devuelve MAPI_E_INVALID_PARAMETER si una propiedad de tipo **PT Object** se incluye en la matriz de valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="49fac-134">Return MAPI_E_INVALID_PARAMETER if a property of type **PT_OBJECT** is included in the property value array.</span></span> <span data-ttu-id="49fac-135">También devuelve este error si se incluye una propiedad de varios valores en la matriz y su miembro **cValues** se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="49fac-135">Also return this error if a multiple-value property is included in the array and its **cValues** member is set to 0.</span></span> 
  
<span data-ttu-id="49fac-136">Si la llamada se realiza correctamente, pero hay problemas para establecer algunas de las propiedades, devuelva S_OK y coloque la información sobre los problemas en la entrada correspondiente a la estructura **SPropProblemArray** a la que apunta el parámetro _lppProblems_ .</span><span class="sxs-lookup"><span data-stu-id="49fac-136">If the call succeeds overall but there are problems with setting some of the properties, return S_OK and put information about the problems in the appropriate entry of the **SPropProblemArray** structure that the  _lppProblems_ parameter points to.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="49fac-137">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="49fac-137">Notes to callers</span></span>

<span data-ttu-id="49fac-138">Dependiendo del proveedor de servicios, es posible que también pueda cambiar el tipo de propiedad pasando una etiqueta de propiedad que contenga un tipo diferente de la utilizada anteriormente con un identificador de propiedad determinado.</span><span class="sxs-lookup"><span data-stu-id="49fac-138">Depending on the service provider, you might also be able to change the property type by passing a property tag that contains a different type than was previously used with a given property identifier.</span></span>
  
<span data-ttu-id="49fac-139">Si incluye una etiqueta de propiedad para una propiedad que no es compatible con el objeto y la implementación de **SetProps** permite la creación de nuevas propiedades, la propiedad se agrega al objeto.</span><span class="sxs-lookup"><span data-stu-id="49fac-139">If you include a property tag for a property that is unsupported by the object and the implementation of **SetProps** allows the creation of new properties, the property is added to the object.</span></span> <span data-ttu-id="49fac-140">Se descarta cualquier valor anterior almacenado con el identificador de propiedad usado para la nueva propiedad.</span><span class="sxs-lookup"><span data-stu-id="49fac-140">Any previous value stored with the property identifier that was used for the new property is discarded.</span></span> 
  
<span data-ttu-id="49fac-141">Tenga en cuenta que el valor devuelto S_OK no garantiza que todas las propiedades se actualicen correctamente.</span><span class="sxs-lookup"><span data-stu-id="49fac-141">Note that the S_OK return value does not guarantee that all of the properties were successfully updated.</span></span> <span data-ttu-id="49fac-142">Algunos proveedores llaman a **SetProps** de caché hasta que reciben una llamada que requiere la intervención del proveedor, como [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) o [IMAPIProp:: GetProps](imapiprop-getprops.md).</span><span class="sxs-lookup"><span data-stu-id="49fac-142">Some providers cache **SetProps** calls until they receive a call that requires provider intervention, such as [IMAPIProp::SaveChanges](imapiprop-savechanges.md) or [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span> <span data-ttu-id="49fac-143">Por lo tanto, es posible recibir valores de error relacionados con la llamada de **SetProps** con las llamadas posteriores.</span><span class="sxs-lookup"><span data-stu-id="49fac-143">Therefore, it is possible to receive error values that relate to the **SetProps** call with the later calls.</span></span> 
  
<span data-ttu-id="49fac-144">Si **SetProps** Devuelve S_OK, Compruebe la estructura **SPropProblemArray** apuntado por _lppProblems_ para ver si hay problemas al actualizar propiedades individuales.</span><span class="sxs-lookup"><span data-stu-id="49fac-144">If **SetProps** returns S_OK, check the **SPropProblemArray** structure pointed to by  _lppProblems_ for problems updating individual properties.</span></span> <span data-ttu-id="49fac-145">Si **SetProps** devuelve un error, no Compruebe la matriz de problemas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="49fac-145">If **SetProps** returns an error, do not check the property problem array.</span></span> <span data-ttu-id="49fac-146">En su lugar, llame al método [IMAPIProp:: GetLastError](imapiprop-getlasterror.md) del objeto.</span><span class="sxs-lookup"><span data-stu-id="49fac-146">Instead, call the object's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method.</span></span> 
  
<span data-ttu-id="49fac-147">Cuando se actualizan propiedades de gran tamaño, **SetProps** puede producir un error y devolver MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="49fac-147">When updating large properties, **SetProps** can fail and return MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="49fac-148">No hay ningún tamaño máximo para las propiedades y los distintos objetos pueden tener distintos límites.</span><span class="sxs-lookup"><span data-stu-id="49fac-148">There is no maximum size for properties, and different objects can have different limits.</span></span> <span data-ttu-id="49fac-149">Si trabaja con propiedades potencialmente grandes, prepárese para llamar al método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) con IID_IStream como identificador de interfaz si **SetProps** devuelve este valor de error.</span><span class="sxs-lookup"><span data-stu-id="49fac-149">If you deal with potentially large properties, be prepared to call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with IID_IStream as the interface identifier if **SetProps** returns this error value.</span></span> 
  
<span data-ttu-id="49fac-150">Llame a la función [MAPIFreeBuffer](mapifreebuffer.md) para liberar la estructura **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="49fac-150">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the **SPropProblemArray** structure.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="49fac-151">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="49fac-151">MFCMAPI reference</span></span>

<span data-ttu-id="49fac-152">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="49fac-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="49fac-153">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="49fac-153">**File**</span></span>|<span data-ttu-id="49fac-154">**Función**</span><span class="sxs-lookup"><span data-stu-id="49fac-154">**Function**</span></span>|<span data-ttu-id="49fac-155">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="49fac-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="49fac-156">Editor. cpp</span><span class="sxs-lookup"><span data-stu-id="49fac-156">PropertyEditor.cpp</span></span>  <br/> |<span data-ttu-id="49fac-157">CPropertyEditor:: WriteSPropValueToObject</span><span class="sxs-lookup"><span data-stu-id="49fac-157">CPropertyEditor::WriteSPropValueToObject</span></span>  <br/> |<span data-ttu-id="49fac-158">MFCMAPI usa el método **IMAPIProp:: SetProps** para volver a escribir una propiedad en un objeto después de que se haya editado la propiedad.</span><span class="sxs-lookup"><span data-stu-id="49fac-158">MFCMAPI uses the **IMAPIProp::SetProps** method to write a property back to an object after the property has been edited.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="49fac-159">Ver también</span><span class="sxs-lookup"><span data-stu-id="49fac-159">See also</span></span>



[<span data-ttu-id="49fac-160">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="49fac-160">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="49fac-161">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="49fac-161">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="49fac-162">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="49fac-162">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="49fac-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="49fac-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="49fac-164">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="49fac-164">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="49fac-165">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="49fac-165">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="49fac-166">SPropValue</span><span class="sxs-lookup"><span data-stu-id="49fac-166">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="49fac-167">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="49fac-167">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)

