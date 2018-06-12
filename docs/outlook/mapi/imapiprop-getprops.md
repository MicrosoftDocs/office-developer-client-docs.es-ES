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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 33351235db2a9a3f9d9b67f59e8356a0fa8abfa8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817410"
---
# <a name="imapipropgetprops"></a><span data-ttu-id="66cd3-103">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="66cd3-103">IMAPIProp::GetProps</span></span>

  
  
<span data-ttu-id="66cd3-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="66cd3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="66cd3-105">Recupera el valor de la propiedad de una o varias propiedades de un objeto.</span><span class="sxs-lookup"><span data-stu-id="66cd3-105">Retrieves the property value of one or more properties of an object.</span></span>
  
```cpp
HRESULT GetProps(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="66cd3-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="66cd3-106">Parameters</span></span>

 <span data-ttu-id="66cd3-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="66cd3-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="66cd3-108">[entrada] Un puntero a una matriz de etiquetas (propiedad) que identifican las propiedades cuyos valores se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="66cd3-108">[in] A pointer to an array of property tags that identify the properties whose values are to be retrieved.</span></span> <span data-ttu-id="66cd3-109">El parámetro _lpPropTagArray_ debe ser NULL, que indica que se deben devolver los valores de todas las propiedades del objeto, o señalar a una estructura de [elemento SPropTagArray](sproptagarray.md) que contiene una o más etiquetas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="66cd3-109">The  _lpPropTagArray_ parameter must be either NULL, indicating that values for all properties of the object should be returned, or point to an [SPropTagArray](sproptagarray.md) structure that contains one or more property tags.</span></span> 
    
 <span data-ttu-id="66cd3-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="66cd3-110">_ulFlags_</span></span>
  
> <span data-ttu-id="66cd3-111">[entrada] Una máscara de bits de marcadores que indica el formato para las propiedades que tengan el tipo de PT_UNSPECIFIED.</span><span class="sxs-lookup"><span data-stu-id="66cd3-111">[in] A bitmask of flags that indicates the format for properties that have the type PT_UNSPECIFIED.</span></span> <span data-ttu-id="66cd3-112">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="66cd3-112">The following flag can be set:</span></span>
    
<span data-ttu-id="66cd3-113">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="66cd3-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="66cd3-114">Los valores de cadena para estas propiedades se deben devolver en el formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="66cd3-114">The string values for these properties should be returned in the Unicode format.</span></span> <span data-ttu-id="66cd3-115">Si no está establecido el indicador MAPI_UNICODE., se deben devolver los valores de cadena en el formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="66cd3-115">If the MAPI_UNICODE flag is not set, the string values should be returned in the ANSI format.</span></span>
    
 <span data-ttu-id="66cd3-116">_lpcValues_</span><span class="sxs-lookup"><span data-stu-id="66cd3-116">_lpcValues_</span></span>
  
> <span data-ttu-id="66cd3-117">[out] Un puntero a un recuento de valores de la propiedad indicada por el parámetro _lppPropArray_ .</span><span class="sxs-lookup"><span data-stu-id="66cd3-117">[out] A pointer to a count of property values pointed to by the  _lppPropArray_ parameter.</span></span> <span data-ttu-id="66cd3-118">Si _lppPropArray_ es NULL, el contenido del parámetro _lpcValues_ es cero.</span><span class="sxs-lookup"><span data-stu-id="66cd3-118">If  _lppPropArray_ is NULL, the content of the  _lpcValues_ parameter is zero.</span></span> 
    
 <span data-ttu-id="66cd3-119">_lppPropArray_</span><span class="sxs-lookup"><span data-stu-id="66cd3-119">_lppPropArray_</span></span>
  
> <span data-ttu-id="66cd3-120">[out] Un puntero a un puntero a los valores de propiedad recuperado.</span><span class="sxs-lookup"><span data-stu-id="66cd3-120">[out] A pointer to a pointer to the retrieved property values.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="66cd3-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="66cd3-121">Return value</span></span>

<span data-ttu-id="66cd3-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="66cd3-122">S_OK</span></span> 
  
> <span data-ttu-id="66cd3-123">Los valores de propiedad se recuperaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="66cd3-123">The property values were successfully retrieved.</span></span>
    
<span data-ttu-id="66cd3-124">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="66cd3-124">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="66cd3-125">La llamada satisfactoria, pero no se podrían tener acceso a una o más propiedades.</span><span class="sxs-lookup"><span data-stu-id="66cd3-125">The call succeeded overall, but one or more properties could not be accessed.</span></span> <span data-ttu-id="66cd3-126">El miembro **aulPropTag** de para cada propiedad no está disponible el valor de la propiedad tiene un tipo de propiedad de PT_ERROR y un identificador de cero.</span><span class="sxs-lookup"><span data-stu-id="66cd3-126">The **aulPropTag** member of the property value for each unavailable property has a property type of PT_ERROR and an identifier of zero.</span></span> <span data-ttu-id="66cd3-127">Cuando se devuelve esta advertencia, la llamada se debe controlarse como correcta.</span><span class="sxs-lookup"><span data-stu-id="66cd3-127">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="66cd3-128">Para probar esta advertencia, utilice la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="66cd3-128">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="66cd3-129">Para obtener más información, vea [Uso de Macros para el control de errores](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="66cd3-129">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
<span data-ttu-id="66cd3-130">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="66cd3-130">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="66cd3-131">Cero se pasó en el miembro **cValues** de la estructura del **elemento SPropTagArray** que señala _lpPropTagArray_.</span><span class="sxs-lookup"><span data-stu-id="66cd3-131">Zero was passed in the **cValues** member of the **SPropTagArray** structure pointed to by  _lpPropTagArray_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="66cd3-132">Notas</span><span class="sxs-lookup"><span data-stu-id="66cd3-132">Remarks</span></span>

<span data-ttu-id="66cd3-133">El método **IMAPIProp::GetProps** obtiene los valores de propiedad de una o varias propiedades de un objeto.</span><span class="sxs-lookup"><span data-stu-id="66cd3-133">The **IMAPIProp::GetProps** method obtains the property values of one or more properties of an object.</span></span> 
  
<span data-ttu-id="66cd3-134">Se devuelven los valores de propiedad en el mismo orden medida que se solicitan (es decir, el orden de las propiedades de la matriz de la etiqueta de propiedad que señala _lpPropTagArray_ coincidencias del orden de la matriz de estructuras de valor de propiedad que señala _lppPropArray _).</span><span class="sxs-lookup"><span data-stu-id="66cd3-134">The property values are returned in the same order as they were requested (that is, the order of properties in the property tag array pointed to by  _lpPropTagArray_ matches the order in the array of property value structures pointed to by  _lppPropArray_).</span></span> 
  
<span data-ttu-id="66cd3-135">Los tipos de propiedad especificados en los miembros de **aulPropTag** de la matriz de la etiqueta de propiedad indican el tipo de valor que se debe devolver en el miembro de **valor** de cada estructura de valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="66cd3-135">The property types specified in the **aulPropTag** members of the property tag array indicate the type of value that should be returned in the **Value** member of each property value structure.</span></span> <span data-ttu-id="66cd3-136">Sin embargo, si el autor de la llamada no conoce el tipo de una propiedad, el tipo en el miembro **aulPropTag** se puede establecer en su lugar en PT_UNSPECIFIED.</span><span class="sxs-lookup"><span data-stu-id="66cd3-136">However, if the caller does not know the type of a property, the type in the **aulPropTag** member can be set instead to PT_UNSPECIFIED.</span></span> <span data-ttu-id="66cd3-137">Al recuperar el valor, **GetProps** establece el tipo correcto en el miembro **aulPropTag** de la estructura del valor de propiedad para la propiedad.</span><span class="sxs-lookup"><span data-stu-id="66cd3-137">In retrieving the value, **GetProps** sets the correct type in the **aulPropTag** member of the property value structure for the property.</span></span> 
  
<span data-ttu-id="66cd3-138">Si se especifican los tipos de propiedad en el **elemento SPropTagArray** en _lpPropTagArray_, los valores de propiedad en la **SPropValue** devuelta en _lppPropArray_ tienen tipos que coincidan exactamente con los tipos solicitados, a menos que se devuelve un valor de error en su lugar.</span><span class="sxs-lookup"><span data-stu-id="66cd3-138">If property types are specified in the **SPropTagArray** in  _lpPropTagArray_, the property values in the **SPropValue** returned in  _lppPropArray_ have types that exactly match the requested types, unless an error value is returned instead.</span></span> 
  
<span data-ttu-id="66cd3-139">Propiedades de cadena pueden tener uno de los dos tipos de propiedad: PT_UNICODE para representar el formato Unicode y PT_STRING8 para representar el formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="66cd3-139">String properties can have one of two property types: PT_UNICODE to represent the Unicode format and PT_STRING8 to represent the ANSI format.</span></span> <span data-ttu-id="66cd3-140">Si se establece el indicador MAPI_UNICODE en el parámetro _ulFlags_ , siempre que **GetProps** no puede determinar el formato adecuado para una propiedad de cadena, devuelve su valor en el formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="66cd3-140">If the MAPI_UNICODE flag is set in the  _ulFlags_ parameter, whenever **GetProps** cannot determine the appropriate format for a string property, it returns its value in the Unicode format.</span></span> <span data-ttu-id="66cd3-141">**GetProps** no puede determinar un tipo de propiedad de cadena exacta en las situaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="66cd3-141">**GetProps** cannot determine an exact string property type in the following situations:</span></span> 
  
- <span data-ttu-id="66cd3-142">El parámetro _lpPropTagArray_ se establece en NULL para solicitar todas las propiedades.</span><span class="sxs-lookup"><span data-stu-id="66cd3-142">The  _lpPropTagArray_ parameter is set to NULL to request all properties.</span></span> 
    
- <span data-ttu-id="66cd3-143">El miembro **aulPropTag** incluye el valor de PT_UNSPECIFIED como su tipo de propiedad en la matriz de la etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="66cd3-143">The **aulPropTag** member includes the value PT_UNSPECIFIED as its property type in the property tag array.</span></span> 
    
<span data-ttu-id="66cd3-144">Si el parámetro _lpPropTagArray_ se establece en NULL para recuperar todas las propiedades del objeto y no existen propiedades, **GetProps** hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="66cd3-144">If the  _lpPropTagArray_ parameter is set to NULL to retrieve all of the properties of the object and no properties exist, **GetProps** does the following:</span></span> 
  
- <span data-ttu-id="66cd3-145">Devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="66cd3-145">Returns S_OK.</span></span>
    
- <span data-ttu-id="66cd3-146">Establece el valor de recuento en el miembro **cValues** de la estructura del valor de propiedad en 0.</span><span class="sxs-lookup"><span data-stu-id="66cd3-146">Sets the count value in the **cValues** member of the property value structure to 0.</span></span> 
    
- <span data-ttu-id="66cd3-147">Establece el contenido de _lpcValues_ en 0.</span><span class="sxs-lookup"><span data-stu-id="66cd3-147">Sets the contents of  _lpcValues_ to 0.</span></span> 
    
- <span data-ttu-id="66cd3-148">_LppPropArray_ se establece en NULL.</span><span class="sxs-lookup"><span data-stu-id="66cd3-148">Sets  _lppPropArray_ to NULL.</span></span> 
    
 <span data-ttu-id="66cd3-149">**GetProps** no debe devolver las propiedades de varios valores con **cValues** se establecen en 0.</span><span class="sxs-lookup"><span data-stu-id="66cd3-149">**GetProps** must not return multiple-value properties with **cValues** set to 0.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="66cd3-150">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="66cd3-150">Notes to implementers</span></span>

<span data-ttu-id="66cd3-151">Llame a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) para asignar memoria inicialmente para la estructura de [SPropValue](spropvalue.md) que señala _lpPropTagArray_; Llame a [MAPIAllocateMore](mapiallocatemore.md) para asignar cualquier memoria adicional necesaria para los miembros de estructura.</span><span class="sxs-lookup"><span data-stu-id="66cd3-151">Call the [MAPIAllocateBuffer](mapiallocatebuffer.md) function to allocate memory initially for the [SPropValue](spropvalue.md) structure pointed to by  _lpPropTagArray_; call [MAPIAllocateMore](mapiallocatemore.md) to allocate any additional memory needed for the structure's members.</span></span> 
  
<span data-ttu-id="66cd3-152">Devolver MAPI_W_ERRORS_RETURNED si no se puede recuperar el valor de una o varias de las propiedades solicitadas.</span><span class="sxs-lookup"><span data-stu-id="66cd3-152">Return MAPI_W_ERRORS_RETURNED if you cannot retrieve the value for one or more of the requested properties.</span></span> <span data-ttu-id="66cd3-153">En la estructura del valor de propiedad, establezca el tipo en el miembro **aulPropTag** para PT_ERROR y el miembro de **valor** a un código de estado que describe el error.</span><span class="sxs-lookup"><span data-stu-id="66cd3-153">In the property value structure, set the type in the **aulPropTag** member to PT_ERROR and the **Value** member to a status code that describes the error.</span></span> <span data-ttu-id="66cd3-154">Por ejemplo, si tiene que convertir una cadena en Unicode y no admiten Unicode, establezca al miembro de **valor** a MAPI_E_BAD_CHARWIDTH.</span><span class="sxs-lookup"><span data-stu-id="66cd3-154">For example, if you have to convert a string to Unicode and do not support Unicode, set the **Value** member to MAPI_E_BAD_CHARWIDTH.</span></span> <span data-ttu-id="66cd3-155">Si la propiedad es demasiado grande, establézcalo en MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="66cd3-155">If the property is too large, set it to MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="66cd3-156">Si el objeto no admite la propiedad, establézcalo en MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="66cd3-156">If the object does not support the property, set it to MAPI_E_NOT_FOUND.</span></span> 
  
<span data-ttu-id="66cd3-157">Implementación del proveedor de transporte remoto del método **GetProps** debe devolver los valores de propiedades de la carpeta de propiedades solicitados por el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="66cd3-157">A remote transport provider's implementation of the **GetProps** method must return the folder's property values for properties requested by the caller.</span></span> <span data-ttu-id="66cd3-158">Su implementación debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="66cd3-158">Your implementation must do the following:</span></span> 
  
- <span data-ttu-id="66cd3-159">Asignar una matriz de valores de propiedad para volver al autor de la llamada y almacenar su dirección en el parámetro de puntero de valor de propiedad que se pasó para ese propósito.</span><span class="sxs-lookup"><span data-stu-id="66cd3-159">Allocate a property value array to return to the caller and store its address in the property value pointer parameter passed in for that purpose.</span></span>
    
- <span data-ttu-id="66cd3-160">Copie las etiquetas de propiedad de las propiedades de la carpeta en las etiquetas de propiedad en la matriz de valores de propiedad según la matriz de etiquetas (propiedad) se pasan a **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="66cd3-160">Copy the property tags from the folder's properties into the property tags in the property value array according to the array of property tags passed to **GetProps**.</span></span>
    
- <span data-ttu-id="66cd3-161">Asegúrese de que el tipo de propiedad se establece para todas las etiquetas de propiedad que se pasan a **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="66cd3-161">Ensure that the property type is set for all property tags passed to **GetProps**.</span></span> <span data-ttu-id="66cd3-162">El autor de la llamada puede pasar en un tipo de propiedad de PT_UNSPECIFIED, en el que caso **GetProps** debe establecer el tipo de propiedad correcto para esa etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="66cd3-162">The caller can pass in a property type of PT_UNSPECIFIED, in which case **GetProps** must set the correct property type for that property tag.</span></span> 
    
- <span data-ttu-id="66cd3-163">Establezca el valor de cada propiedad de la matriz de valores de propiedad según su etiqueta.</span><span class="sxs-lookup"><span data-stu-id="66cd3-163">Set the value of each property in the property value array according to its tag.</span></span> <span data-ttu-id="66cd3-164">Por ejemplo, si la etiqueta de la propiedad solicitada por el autor de la llamada es **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)), **GetProps** puede establecer el valor en MAPI_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="66cd3-164">For example, if the property tag requested by the caller is **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)), **GetProps** can set the value to MAPI_FOLDER.</span></span> 
    
- <span data-ttu-id="66cd3-165">Si el autor de la llamada pasa las etiquetas de propiedad que no controla su implementación, puede establecer la etiqueta de propiedad en PT_ERROR para esas propiedades y establezca el valor de propiedad en MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="66cd3-165">If the caller passes in any property tags that your implementation does not handle, you can set the property tag to PT_ERROR for those properties, and set the property value to MAPI_E_NOT_FOUND.</span></span>
    
- <span data-ttu-id="66cd3-166">Devuelve S_OK si se ha producido ningún error ni MAPI_W_ERRORS_RETURNED si se han producido errores.</span><span class="sxs-lookup"><span data-stu-id="66cd3-166">Return S_OK if no errors occurred or MAPI_W_ERRORS_RETURNED if there were errors.</span></span>
    
<span data-ttu-id="66cd3-167">Implementación del proveedor de transporte remoto del método **GetProps** debe admitir las siguientes propiedades como mínimo:</span><span class="sxs-lookup"><span data-stu-id="66cd3-167">A remote transport provider's implementation of the **GetProps** method must support the following properties at a minimum:</span></span> 
  
- <span data-ttu-id="66cd3-168">**PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="66cd3-168">**PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md))</span></span>
    
- <span data-ttu-id="66cd3-169">**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="66cd3-169">**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))</span></span>
    
- <span data-ttu-id="66cd3-170">**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="66cd3-170">**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="66cd3-171">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="66cd3-171">**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))</span></span>
    
- <span data-ttu-id="66cd3-172">**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="66cd3-172">**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="66cd3-173">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="66cd3-173">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="66cd3-174">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="66cd3-174">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
- <span data-ttu-id="66cd3-175">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="66cd3-175">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span></span>
    
- <span data-ttu-id="66cd3-176">**PR_OBJECT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="66cd3-176">**PR_OBJECT_TYPE**</span></span>
    
- <span data-ttu-id="66cd3-177">**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="66cd3-177">**PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="66cd3-178">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="66cd3-178">Notes to callers</span></span>

<span data-ttu-id="66cd3-179">Para las propiedades de tipo pt Object, llame al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) en lugar de **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="66cd3-179">For properties of type PT_OBJECT, call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method instead of **GetProps**.</span></span> 
  
<span data-ttu-id="66cd3-180">Para las propiedades seguras, no se espera recuperar al llamar a **GetProps** con el parámetro _lppPropTagArray_ establecido en NULL.</span><span class="sxs-lookup"><span data-stu-id="66cd3-180">For secure properties, do not expect to retrieve them by calling **GetProps** with the  _lppPropTagArray_ parameter set to NULL.</span></span> <span data-ttu-id="66cd3-181">Debe establecer explícitamente el identificador de la propiedad segura en el miembro **aulPropTag** de su matriz de etiqueta de propiedad cuando se llama a **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="66cd3-181">You must explicitly set a secure property's identifier in the **aulPropTag** member of its property tag array when you call **GetProps**.</span></span> <span data-ttu-id="66cd3-182">Cómo y cuándo está disponible una propiedad segura es hasta el proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="66cd3-182">When and how a secure property is available is up to the service provider.</span></span> 
  
<span data-ttu-id="66cd3-183">Libere la estructura **SPropValue** devuelta por una llamada a la función [MAPIFreeBuffer](mapifreebuffer.md) sólo si **GetProps** devuelve S_OK o MAPI_W_ERRORS_RETURNED.</span><span class="sxs-lookup"><span data-stu-id="66cd3-183">Free the returned **SPropValue** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function only if **GetProps** returns S_OK or MAPI_W_ERRORS_RETURNED.</span></span> 
  
<span data-ttu-id="66cd3-184">Si **GetProps** devuelve MAPI_W_ERRORS_RETURNED porque no se pudo tener acceso una o más propiedades, compruebe las etiquetas de propiedad de las propiedades devueltas.</span><span class="sxs-lookup"><span data-stu-id="66cd3-184">If **GetProps** returns MAPI_W_ERRORS_RETURNED because it could not access one or more properties, check the property tags of the returned properties.</span></span> <span data-ttu-id="66cd3-185">Las propiedades con errores tendrá los siguientes valores establecidos en su estructura de valor de propiedad:</span><span class="sxs-lookup"><span data-stu-id="66cd3-185">The failed properties will have the following values set in their property value structure:</span></span> 
  
- <span data-ttu-id="66cd3-186">El tipo de propiedad en el miembro **aulPropTag** establecido en PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="66cd3-186">The property type in the **aulPropTag** member set to PT_ERROR.</span></span> 
    
- <span data-ttu-id="66cd3-187">El valor de la propiedad en el **valor de** conjunto de miembros a un código de estado para el error, como MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="66cd3-187">The property value in the **Value** member set to a status code for the error, such as MAPI_E_NOT_FOUND.</span></span> 
    
<span data-ttu-id="66cd3-188">Las propiedades que se producirá un error porque son demasiado grandes para cómodamente se devuelven en la estructura de valor de propiedad tienen sus miembros **valor** establecido en MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="66cd3-188">Properties that fail because they are too large to conveniently be returned in the property value structure have their **Value** member set to MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="66cd3-189">Normalmente, este problema ocurre con las propiedades de tipo de cadena o binario PT_STRING8, PT_UNICODE o PT_BINARY cuando el valor de la propiedad es de 4 KB o más grande.</span><span class="sxs-lookup"><span data-stu-id="66cd3-189">Typically, this occurs with string or binary properties of type PT_STRING8, PT_UNICODE, or PT_BINARY when the value of the property is 4 KB or larger.</span></span> <span data-ttu-id="66cd3-190">Llame a **IMAPIProp::OpenProperty** para recuperar propiedades de gran tamaño.</span><span class="sxs-lookup"><span data-stu-id="66cd3-190">Call **IMAPIProp::OpenProperty** to retrieve large properties.</span></span> 
  
<span data-ttu-id="66cd3-191">No todas las implementaciones de **GetProps** admiten formatos Unicode y ANSI para cadenas de caracteres.</span><span class="sxs-lookup"><span data-stu-id="66cd3-191">Not all implementations of **GetProps** support both the Unicode and ANSI formats for character strings.</span></span> <span data-ttu-id="66cd3-192">Cuando una propiedad concreta requiere la conversión de formato de cadena y **GetProps** no lo admiten, el miembro de **valor** de la propiedad se establece en MAPI_E_BAD_CHARWIDTH.</span><span class="sxs-lookup"><span data-stu-id="66cd3-192">When a particular property requires string format conversion and **GetProps** cannot support it, the **Value** member for the property is set to MAPI_E_BAD_CHARWIDTH.</span></span> 
  
<span data-ttu-id="66cd3-193">Para comprobar si un archivo PST es un archivo PST de SharePoint, monte el PST utilizando [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md), a continuación, se llame **GetProps** en el objeto de almacén de mensaje que solicita esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="66cd3-193">To check if a PST is a SharePoint PST, mount the PST using [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md), then call **GetProps** on the message store object requesting this property.</span></span> <span data-ttu-id="66cd3-194">Si existe, se puede suponer que se ha configurado el PST de SharePoint; Si no es así, el archivo PST no se ha configurado como un archivo PST de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="66cd3-194">If it exists, you can assume the PST has been configured for SharePoint; if not, the PST has not been configured as a SharePoint PST.</span></span> 
  
<span data-ttu-id="66cd3-195">Para obtener más información acerca de cómo usar **GetProps** para tener acceso a las propiedades, vea [Recuperar propiedades de MAPI](retrieving-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="66cd3-195">For more information about how to use **GetProps** to access properties, see [Retrieving MAPI Properties](retrieving-mapi-properties.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="66cd3-196">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="66cd3-196">MFCMAPI reference</span></span>

<span data-ttu-id="66cd3-197">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="66cd3-197">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="66cd3-198">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="66cd3-198">**File**</span></span>|<span data-ttu-id="66cd3-199">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="66cd3-199">**Function**</span></span>|<span data-ttu-id="66cd3-200">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="66cd3-200">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="66cd3-201">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="66cd3-201">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="66cd3-202">GetPropsNULL</span><span class="sxs-lookup"><span data-stu-id="66cd3-202">GetPropsNULL</span></span>  <br/> |<span data-ttu-id="66cd3-203">MFCMAPI utiliza el método **IMAPIProp::GetProps** para obtener todas las propiedades de un objeto pasando NULL o la matriz devuelta por el método [IMAPIProp::GetPropList](imapiprop-getproplist.md) en el parámetro _lpPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="66cd3-203">MFCMAPI uses the **IMAPIProp::GetProps** method to obtain all properties for an object by passing either NULL or the array returned by the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method in the  _lpPropTagArray_ parameter.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="66cd3-204">Ver también</span><span class="sxs-lookup"><span data-stu-id="66cd3-204">See also</span></span>



[<span data-ttu-id="66cd3-205">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="66cd3-205">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="66cd3-206">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="66cd3-206">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="66cd3-207">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="66cd3-207">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="66cd3-208">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="66cd3-208">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="66cd3-209">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="66cd3-209">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="66cd3-210">Elemento SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="66cd3-210">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="66cd3-211">SPropValue</span><span class="sxs-lookup"><span data-stu-id="66cd3-211">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="66cd3-212">IMAPIProp: IUnknown</span><span class="sxs-lookup"><span data-stu-id="66cd3-212">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="66cd3-213">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="66cd3-213">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="66cd3-214">Recuperación de propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="66cd3-214">Retrieving MAPI Properties</span></span>](retrieving-mapi-properties.md)
  
[<span data-ttu-id="66cd3-215">Usar Macros para el tratamiento de errores</span><span class="sxs-lookup"><span data-stu-id="66cd3-215">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

