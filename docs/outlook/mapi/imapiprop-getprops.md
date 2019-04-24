---
title: IMAPIPropGetProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetProps
api_type:
- COM
ms.assetid: 1c7a9cd2-d765-4218-9aee-52df1a2aae6c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9b03775d495f7d1f51142eb0ed06fc9ecdf6d1a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316614"
---
# <a name="imapipropgetprops"></a><span data-ttu-id="5b7de-103">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="5b7de-103">IMAPIProp::GetProps</span></span>

  
  
<span data-ttu-id="5b7de-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b7de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b7de-105">Recupera el valor de la propiedad de una o varias propiedades de un objeto.</span><span class="sxs-lookup"><span data-stu-id="5b7de-105">Retrieves the property value of one or more properties of an object.</span></span>
  
```cpp
HRESULT GetProps(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="5b7de-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="5b7de-106">Parameters</span></span>

 <span data-ttu-id="5b7de-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="5b7de-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="5b7de-108">a Un puntero a una matriz de etiquetas de propiedad que identifican las propiedades cuyos valores se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="5b7de-108">[in] A pointer to an array of property tags that identify the properties whose values are to be retrieved.</span></span> <span data-ttu-id="5b7de-109">El parámetro _lpPropTagArray_ debe ser null, que indica que deben devolverse los valores de todas las propiedades del objeto, o bien, apuntar a una estructura [SPropTagArray](sproptagarray.md) que contenga una o más etiquetas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="5b7de-109">The  _lpPropTagArray_ parameter must be either NULL, indicating that values for all properties of the object should be returned, or point to an [SPropTagArray](sproptagarray.md) structure that contains one or more property tags.</span></span> 
    
 <span data-ttu-id="5b7de-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5b7de-110">_ulFlags_</span></span>
  
> <span data-ttu-id="5b7de-111">a Máscara de máscara de marcadores que indica el formato de las propiedades que tienen el tipo PT_UNSPECIFIED.</span><span class="sxs-lookup"><span data-stu-id="5b7de-111">[in] A bitmask of flags that indicates the format for properties that have the type PT_UNSPECIFIED.</span></span> <span data-ttu-id="5b7de-112">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="5b7de-112">The following flag can be set:</span></span>
    
<span data-ttu-id="5b7de-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5b7de-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="5b7de-114">Los valores de cadena para estas propiedades deben devolverse en el formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="5b7de-114">The string values for these properties should be returned in the Unicode format.</span></span> <span data-ttu-id="5b7de-115">Si no se establece la marca MAPI_UNICODE, los valores de cadena deben devolverse en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="5b7de-115">If the MAPI_UNICODE flag is not set, the string values should be returned in the ANSI format.</span></span>
    
 <span data-ttu-id="5b7de-116">_lpcValues_</span><span class="sxs-lookup"><span data-stu-id="5b7de-116">_lpcValues_</span></span>
  
> <span data-ttu-id="5b7de-117">contempla Un puntero a un recuento de valores de propiedad apuntado por el parámetro _lppPropArray_ .</span><span class="sxs-lookup"><span data-stu-id="5b7de-117">[out] A pointer to a count of property values pointed to by the  _lppPropArray_ parameter.</span></span> <span data-ttu-id="5b7de-118">Si _lppPropArray_ es null, el contenido del parámetro _lpcValues_ es cero.</span><span class="sxs-lookup"><span data-stu-id="5b7de-118">If  _lppPropArray_ is NULL, the content of the  _lpcValues_ parameter is zero.</span></span> 
    
 <span data-ttu-id="5b7de-119">_lppPropArray_</span><span class="sxs-lookup"><span data-stu-id="5b7de-119">_lppPropArray_</span></span>
  
> <span data-ttu-id="5b7de-120">contempla Un puntero a un puntero a los valores de propiedad recuperados.</span><span class="sxs-lookup"><span data-stu-id="5b7de-120">[out] A pointer to a pointer to the retrieved property values.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5b7de-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5b7de-121">Return value</span></span>

<span data-ttu-id="5b7de-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="5b7de-122">S_OK</span></span> 
  
> <span data-ttu-id="5b7de-123">Los valores de la propiedad se recuperaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="5b7de-123">The property values were successfully retrieved.</span></span>
    
<span data-ttu-id="5b7de-124">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="5b7de-124">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="5b7de-125">La llamada se realizó en general, pero no se pudo tener acceso a una o más propiedades.</span><span class="sxs-lookup"><span data-stu-id="5b7de-125">The call succeeded overall, but one or more properties could not be accessed.</span></span> <span data-ttu-id="5b7de-126">El miembro **aulPropTag** del valor de la propiedad para cada propiedad no disponible tiene un tipo de propiedad de PT_ERROR y un identificador de cero.</span><span class="sxs-lookup"><span data-stu-id="5b7de-126">The **aulPropTag** member of the property value for each unavailable property has a property type of PT_ERROR and an identifier of zero.</span></span> <span data-ttu-id="5b7de-127">Cuando se devuelve esta advertencia, la llamada se debe administrar como correcta.</span><span class="sxs-lookup"><span data-stu-id="5b7de-127">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="5b7de-128">Para probar esta advertencia, use la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="5b7de-128">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="5b7de-129">Para obtener más información, consulte [usar macros para el control de errores](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="5b7de-129">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
<span data-ttu-id="5b7de-130">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5b7de-130">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="5b7de-131">Se pasó cero en el miembro **cValues** de la estructura **SPropTagArray** a la que apunta _lpPropTagArray_.</span><span class="sxs-lookup"><span data-stu-id="5b7de-131">Zero was passed in the **cValues** member of the **SPropTagArray** structure pointed to by  _lpPropTagArray_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5b7de-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5b7de-132">Remarks</span></span>

<span data-ttu-id="5b7de-133">El método **IMAPIProp:: GetProps** obtiene los valores de propiedad de una o varias propiedades de un objeto.</span><span class="sxs-lookup"><span data-stu-id="5b7de-133">The **IMAPIProp::GetProps** method obtains the property values of one or more properties of an object.</span></span> 
  
<span data-ttu-id="5b7de-134">Los valores de propiedad se devuelven en el mismo orden en que se solicitaron (es decir, el orden de propiedades en la matriz de etiquetas de propiedad a la que apunta _lpPropTagArray_ coincide con el orden de la matriz de estructuras de valores de propiedad apuntado por _lppPropArray _).</span><span class="sxs-lookup"><span data-stu-id="5b7de-134">The property values are returned in the same order as they were requested (that is, the order of properties in the property tag array pointed to by  _lpPropTagArray_ matches the order in the array of property value structures pointed to by  _lppPropArray_).</span></span> 
  
<span data-ttu-id="5b7de-135">Los tipos de propiedad especificados en los miembros **aulPropTag** de la matriz de etiquetas de propiedad indican el tipo de valor que se debe devolver en el miembro de **valor** de cada estructura de valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="5b7de-135">The property types specified in the **aulPropTag** members of the property tag array indicate the type of value that should be returned in the **Value** member of each property value structure.</span></span> <span data-ttu-id="5b7de-136">Sin embargo, si el autor de la llamada no conoce el tipo de una propiedad, el tipo del miembro **aulPropTag** se puede establecer en su lugar para PT_UNSPECIFIED.</span><span class="sxs-lookup"><span data-stu-id="5b7de-136">However, if the caller does not know the type of a property, the type in the **aulPropTag** member can be set instead to PT_UNSPECIFIED.</span></span> <span data-ttu-id="5b7de-137">Al recuperar el valor, **GetProps** establece el tipo correcto en el miembro **aulPropTag** de la estructura del valor de la propiedad para la propiedad.</span><span class="sxs-lookup"><span data-stu-id="5b7de-137">In retrieving the value, **GetProps** sets the correct type in the **aulPropTag** member of the property value structure for the property.</span></span> 
  
<span data-ttu-id="5b7de-138">Si los tipos de propiedad se especifican en **SPropTagArray** en _lpPropTagArray_, los valores de propiedad de **SPropValue** devueltos en _lppPropArray_ tienen tipos que coinciden exactamente con los tipos solicitados, a menos que se devuelva un valor de error. en lugar.</span><span class="sxs-lookup"><span data-stu-id="5b7de-138">If property types are specified in the **SPropTagArray** in  _lpPropTagArray_, the property values in the **SPropValue** returned in  _lppPropArray_ have types that exactly match the requested types, unless an error value is returned instead.</span></span> 
  
<span data-ttu-id="5b7de-139">Las propiedades de cadena pueden tener uno de los dos tipos de propiedades: PT_UNICODE para representar el formato Unicode y PT_STRING8 para representar el formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="5b7de-139">String properties can have one of two property types: PT_UNICODE to represent the Unicode format and PT_STRING8 to represent the ANSI format.</span></span> <span data-ttu-id="5b7de-140">Si la marca MAPI_UNICODE se establece en el parámetro _ulFlags_ , siempre que **GetProps** no pueda determinar el formato adecuado para una propiedad de cadena, devolverá su valor en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="5b7de-140">If the MAPI_UNICODE flag is set in the  _ulFlags_ parameter, whenever **GetProps** cannot determine the appropriate format for a string property, it returns its value in the Unicode format.</span></span> <span data-ttu-id="5b7de-141">**GetProps** no puede determinar un tipo de propiedad de cadena exacta en las siguientes situaciones:</span><span class="sxs-lookup"><span data-stu-id="5b7de-141">**GetProps** cannot determine an exact string property type in the following situations:</span></span> 
  
- <span data-ttu-id="5b7de-142">El parámetro _lpPropTagArray_ se establece en null para solicitar todas las propiedades.</span><span class="sxs-lookup"><span data-stu-id="5b7de-142">The  _lpPropTagArray_ parameter is set to NULL to request all properties.</span></span> 
    
- <span data-ttu-id="5b7de-143">El miembro **aulPropTag** incluye el valor PT_UNSPECIFIED como su tipo de propiedad en la matriz de etiquetas de propiedades.</span><span class="sxs-lookup"><span data-stu-id="5b7de-143">The **aulPropTag** member includes the value PT_UNSPECIFIED as its property type in the property tag array.</span></span> 
    
<span data-ttu-id="5b7de-144">Si el parámetro _lpPropTagArray_ se establece en null para recuperar todas las propiedades del objeto y no existen propiedades, **GetProps** hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="5b7de-144">If the  _lpPropTagArray_ parameter is set to NULL to retrieve all of the properties of the object and no properties exist, **GetProps** does the following:</span></span> 
  
- <span data-ttu-id="5b7de-145">Devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="5b7de-145">Returns S_OK.</span></span>
    
- <span data-ttu-id="5b7de-146">Establece en 0 el valor de recuento del miembro **cValues** de la estructura del valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="5b7de-146">Sets the count value in the **cValues** member of the property value structure to 0.</span></span> 
    
- <span data-ttu-id="5b7de-147">Establece el contenido de _lpcValues_ en 0.</span><span class="sxs-lookup"><span data-stu-id="5b7de-147">Sets the contents of  _lpcValues_ to 0.</span></span> 
    
- <span data-ttu-id="5b7de-148">Establece _lppPropArray_ en NULL.</span><span class="sxs-lookup"><span data-stu-id="5b7de-148">Sets  _lppPropArray_ to NULL.</span></span> 
    
 <span data-ttu-id="5b7de-149">**GetProps** no debe devolver propiedades de varios valores con **cValues** establecido en 0.</span><span class="sxs-lookup"><span data-stu-id="5b7de-149">**GetProps** must not return multiple-value properties with **cValues** set to 0.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="5b7de-150">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="5b7de-150">Notes to implementers</span></span>

<span data-ttu-id="5b7de-151">Llame a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) para asignar memoria al principio para la estructura [SPropValue](spropvalue.md) a la que apunta _lpPropTagArray_; llamar a [MAPIAllocateMore](mapiallocatemore.md) para asignar la memoria adicional necesaria para los miembros de la estructura.</span><span class="sxs-lookup"><span data-stu-id="5b7de-151">Call the [MAPIAllocateBuffer](mapiallocatebuffer.md) function to allocate memory initially for the [SPropValue](spropvalue.md) structure pointed to by  _lpPropTagArray_; call [MAPIAllocateMore](mapiallocatemore.md) to allocate any additional memory needed for the structure's members.</span></span> 
  
<span data-ttu-id="5b7de-152">Devuelve MAPI_W_ERRORS_RETURNED si no puede recuperar el valor de una o varias de las propiedades solicitadas.</span><span class="sxs-lookup"><span data-stu-id="5b7de-152">Return MAPI_W_ERRORS_RETURNED if you cannot retrieve the value for one or more of the requested properties.</span></span> <span data-ttu-id="5b7de-153">En la estructura del valor de la propiedad, establezca el tipo del miembro **aulPropTag** en PT_ERROR y el miembro **Value** en un código de estado que describe el error.</span><span class="sxs-lookup"><span data-stu-id="5b7de-153">In the property value structure, set the type in the **aulPropTag** member to PT_ERROR and the **Value** member to a status code that describes the error.</span></span> <span data-ttu-id="5b7de-154">Por ejemplo, si tiene que convertir una cadena en Unicode y no admite Unicode, establezca el **valor** de Member en MAPI_E_BAD_CHARWIDTH.</span><span class="sxs-lookup"><span data-stu-id="5b7de-154">For example, if you have to convert a string to Unicode and do not support Unicode, set the **Value** member to MAPI_E_BAD_CHARWIDTH.</span></span> <span data-ttu-id="5b7de-155">Si la propiedad es demasiado grande, establézcalo en MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="5b7de-155">If the property is too large, set it to MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="5b7de-156">Si el objeto no admite la propiedad, establézcalo en MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="5b7de-156">If the object does not support the property, set it to MAPI_E_NOT_FOUND.</span></span> 
  
<span data-ttu-id="5b7de-157">La implementación de un proveedor de transporte remoto del método **GetProps** debe devolver los valores de propiedad de la carpeta para las propiedades solicitadas por el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="5b7de-157">A remote transport provider's implementation of the **GetProps** method must return the folder's property values for properties requested by the caller.</span></span> <span data-ttu-id="5b7de-158">La implementación debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="5b7de-158">Your implementation must do the following:</span></span> 
  
- <span data-ttu-id="5b7de-159">Asigne una matriz de valores de propiedad para volver a la persona que llama y almacenar su dirección en el parámetro de puntero de valor de propiedad que se pasa para ese propósito.</span><span class="sxs-lookup"><span data-stu-id="5b7de-159">Allocate a property value array to return to the caller and store its address in the property value pointer parameter passed in for that purpose.</span></span>
    
- <span data-ttu-id="5b7de-160">Copie las etiquetas de propiedad de las propiedades de la carpeta en las etiquetas de propiedad de la matriz de valores de propiedad de acuerdo con la matriz de etiquetas de propiedad pasadas a **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="5b7de-160">Copy the property tags from the folder's properties into the property tags in the property value array according to the array of property tags passed to **GetProps**.</span></span>
    
- <span data-ttu-id="5b7de-161">Asegúrese de que el tipo de propiedad está establecido para todas las etiquetas de propiedad pasadas a **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="5b7de-161">Ensure that the property type is set for all property tags passed to **GetProps**.</span></span> <span data-ttu-id="5b7de-162">El autor de la llamada puede pasar un tipo de propiedad de PT_UNSPECIFIED, en cuyo caso **GetProps** debe establecer el tipo de propiedad correcto para esa etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="5b7de-162">The caller can pass in a property type of PT_UNSPECIFIED, in which case **GetProps** must set the correct property type for that property tag.</span></span> 
    
- <span data-ttu-id="5b7de-163">Establezca el valor de cada propiedad en la matriz de valores de propiedad según su etiqueta.</span><span class="sxs-lookup"><span data-stu-id="5b7de-163">Set the value of each property in the property value array according to its tag.</span></span> <span data-ttu-id="5b7de-164">Por ejemplo, si la etiqueta de propiedad solicitada por el autor de la llamada es **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)), **GetProps** puede establecer el valor en MAPI_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="5b7de-164">For example, if the property tag requested by the caller is **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)), **GetProps** can set the value to MAPI_FOLDER.</span></span> 
    
- <span data-ttu-id="5b7de-165">Si el autor de la llamada pasa cualquier etiqueta de propiedad que su implementación no controla, puede establecer la etiqueta de propiedad en PT_ERROR para esas propiedades y establecer el valor de la propiedad en MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="5b7de-165">If the caller passes in any property tags that your implementation does not handle, you can set the property tag to PT_ERROR for those properties, and set the property value to MAPI_E_NOT_FOUND.</span></span>
    
- <span data-ttu-id="5b7de-166">Devuelve S_OK si no se han producido errores o MAPI_W_ERRORS_RETURNED si hay errores.</span><span class="sxs-lookup"><span data-stu-id="5b7de-166">Return S_OK if no errors occurred or MAPI_W_ERRORS_RETURNED if there were errors.</span></span>
    
<span data-ttu-id="5b7de-167">La implementación de un proveedor de transporte remoto del método **GetProps** debe admitir las siguientes propiedades como mínimo:</span><span class="sxs-lookup"><span data-stu-id="5b7de-167">A remote transport provider's implementation of the **GetProps** method must support the following properties at a minimum:</span></span> 
  
- <span data-ttu-id="5b7de-168">**PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5b7de-168">**PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md))</span></span>
    
- <span data-ttu-id="5b7de-169">**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5b7de-169">**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))</span></span>
    
- <span data-ttu-id="5b7de-170">**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5b7de-170">**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="5b7de-171">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5b7de-171">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="5b7de-172">**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5b7de-172">**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="5b7de-173">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5b7de-173">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="5b7de-174">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5b7de-174">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
- <span data-ttu-id="5b7de-175">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5b7de-175">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span></span>
    
- <span data-ttu-id="5b7de-176">**PR_OBJECT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="5b7de-176">**PR_OBJECT_TYPE**</span></span>
    
- <span data-ttu-id="5b7de-177">**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5b7de-177">**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="5b7de-178">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="5b7de-178">Notes to callers</span></span>

<span data-ttu-id="5b7de-179">Para propiedades de tipo PT Object, llame al método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) en lugar de a **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="5b7de-179">For properties of type PT_OBJECT, call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method instead of **GetProps**.</span></span> 
  
<span data-ttu-id="5b7de-180">Para las propiedades seguras, no espere recuperarlas llamando a **GetProps** con el parámetro _LPPPROPTAGARRAY_ establecido en NULL.</span><span class="sxs-lookup"><span data-stu-id="5b7de-180">For secure properties, do not expect to retrieve them by calling **GetProps** with the  _lppPropTagArray_ parameter set to NULL.</span></span> <span data-ttu-id="5b7de-181">Debe establecer explícitamente un identificador de propiedad segura en el miembro **aulPropTag** de su matriz de etiquetas de propiedad cuando llame a **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="5b7de-181">You must explicitly set a secure property's identifier in the **aulPropTag** member of its property tag array when you call **GetProps**.</span></span> <span data-ttu-id="5b7de-182">Cuándo y cómo una propiedad segura está disponible en el proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="5b7de-182">When and how a secure property is available is up to the service provider.</span></span> 
  
<span data-ttu-id="5b7de-183">Libere la estructura **SPropValue** devuelta llamando a la función [MAPIFreeBuffer](mapifreebuffer.md) solo si **GetProps** Devuelve S_OK o MAPI_W_ERRORS_RETURNED.</span><span class="sxs-lookup"><span data-stu-id="5b7de-183">Free the returned **SPropValue** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function only if **GetProps** returns S_OK or MAPI_W_ERRORS_RETURNED.</span></span> 
  
<span data-ttu-id="5b7de-184">Si **GetProps** devuelve MAPI_W_ERRORS_RETURNED porque no pudo obtener acceso a una o más propiedades, compruebe las etiquetas de propiedad de las propiedades devueltas.</span><span class="sxs-lookup"><span data-stu-id="5b7de-184">If **GetProps** returns MAPI_W_ERRORS_RETURNED because it could not access one or more properties, check the property tags of the returned properties.</span></span> <span data-ttu-id="5b7de-185">Las propiedades con error tendrán los siguientes valores establecidos en su estructura de valores de propiedad:</span><span class="sxs-lookup"><span data-stu-id="5b7de-185">The failed properties will have the following values set in their property value structure:</span></span> 
  
- <span data-ttu-id="5b7de-186">El tipo de propiedad en el miembro **aulPropTag** se establece en PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="5b7de-186">The property type in the **aulPropTag** member set to PT_ERROR.</span></span> 
    
- <span data-ttu-id="5b7de-187">El valor de la propiedad en el **valor** miembro establecido en un código de estado para el error, como MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="5b7de-187">The property value in the **Value** member set to a status code for the error, such as MAPI_E_NOT_FOUND.</span></span> 
    
<span data-ttu-id="5b7de-188">Propiedades que dan error porque son demasiado grandes como para que se devuelvan convenientemente en la estructura del valor de la propiedad, establezca el valor del miembro **Value** en MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="5b7de-188">Properties that fail because they are too large to conveniently be returned in the property value structure have their **Value** member set to MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="5b7de-189">Normalmente, esto ocurre con las propiedades String o Binary de tipo PT_STRING8, PT_UNICODE o PT_BINARY cuando el valor de la propiedad es 4 KB o superior.</span><span class="sxs-lookup"><span data-stu-id="5b7de-189">Typically, this occurs with string or binary properties of type PT_STRING8, PT_UNICODE, or PT_BINARY when the value of the property is 4 KB or larger.</span></span> <span data-ttu-id="5b7de-190">Llamar a **IMAPIProp:: OpenProperty** para recuperar propiedades grandes.</span><span class="sxs-lookup"><span data-stu-id="5b7de-190">Call **IMAPIProp::OpenProperty** to retrieve large properties.</span></span> 
  
<span data-ttu-id="5b7de-191">No todas las implementaciones de **GetProps** admiten los formatos Unicode y ANSI para las cadenas de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5b7de-191">Not all implementations of **GetProps** support both the Unicode and ANSI formats for character strings.</span></span> <span data-ttu-id="5b7de-192">Cuando una propiedad determinada requiere la conversión de formato de cadena y **GetProps** no la admite, el valor del miembro **Value** de la propiedad se establece en MAPI_E_BAD_CHARWIDTH.</span><span class="sxs-lookup"><span data-stu-id="5b7de-192">When a particular property requires string format conversion and **GetProps** cannot support it, the **Value** member for the property is set to MAPI_E_BAD_CHARWIDTH.</span></span> 
  
<span data-ttu-id="5b7de-193">Para comprobar si un PST es un archivo PST de SharePoint, Monte el archivo PST con [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md)y, a continuación, llame a **GetProps** en el objeto de almacén de mensajes que solicita esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="5b7de-193">To check if a PST is a SharePoint PST, mount the PST using [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md), then call **GetProps** on the message store object requesting this property.</span></span> <span data-ttu-id="5b7de-194">Si existe, puede suponer que el archivo PST se ha configurado para SharePoint; de lo contrario, el archivo PST no se ha configurado como un archivo PST de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="5b7de-194">If it exists, you can assume the PST has been configured for SharePoint; if not, the PST has not been configured as a SharePoint PST.</span></span> 
  
<span data-ttu-id="5b7de-195">Para obtener más información acerca de cómo usar **GetProps** para obtener acceso a las propiedades, vea [recuperar propiedades de MAPI](retrieving-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="5b7de-195">For more information about how to use **GetProps** to access properties, see [Retrieving MAPI Properties](retrieving-mapi-properties.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5b7de-196">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="5b7de-196">MFCMAPI reference</span></span>

<span data-ttu-id="5b7de-197">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="5b7de-197">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5b7de-198">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="5b7de-198">**File**</span></span>|<span data-ttu-id="5b7de-199">**Función**</span><span class="sxs-lookup"><span data-stu-id="5b7de-199">**Function**</span></span>|<span data-ttu-id="5b7de-200">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="5b7de-200">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5b7de-201">MAPIFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="5b7de-201">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="5b7de-202">GetPropsNULL</span><span class="sxs-lookup"><span data-stu-id="5b7de-202">GetPropsNULL</span></span>  <br/> |<span data-ttu-id="5b7de-203">MFCMAPI usa el método **IMAPIProp:: GetProps** para obtener todas las propiedades de un objeto pasando un valor null o la matriz devuelta por el método [IMAPIProp:: GetPropList](imapiprop-getproplist.md) en el parámetro _lpPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="5b7de-203">MFCMAPI uses the **IMAPIProp::GetProps** method to obtain all properties for an object by passing either NULL or the array returned by the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method in the  _lpPropTagArray_ parameter.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5b7de-204">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b7de-204">See also</span></span>



[<span data-ttu-id="5b7de-205">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="5b7de-205">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="5b7de-206">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="5b7de-206">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="5b7de-207">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="5b7de-207">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="5b7de-208">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="5b7de-208">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="5b7de-209">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="5b7de-209">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="5b7de-210">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="5b7de-210">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="5b7de-211">SPropValue</span><span class="sxs-lookup"><span data-stu-id="5b7de-211">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="5b7de-212">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5b7de-212">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="5b7de-213">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="5b7de-213">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="5b7de-214">Recuperación de propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5b7de-214">Retrieving MAPI Properties</span></span>](retrieving-mapi-properties.md)
  
[<span data-ttu-id="5b7de-215">Uso de macros para el control de errores</span><span class="sxs-lookup"><span data-stu-id="5b7de-215">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

