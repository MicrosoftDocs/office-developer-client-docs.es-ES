---
title: IMAPIPropOpenProperty
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.OpenProperty
api_type:
- COM
ms.assetid: e400e6cc-4e36-43fc-9304-b688a0a7fd77
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7bf1d6912e44319c36e288cd3870218e8c4e45ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319813"
---
# <a name="imapipropopenproperty"></a><span data-ttu-id="55712-103">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="55712-103">IMAPIProp::OpenProperty</span></span>

<span data-ttu-id="55712-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55712-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55712-105">Devuelve un puntero a una interfaz que se puede usar para obtener acceso a una propiedad.</span><span class="sxs-lookup"><span data-stu-id="55712-105">Returns a pointer to an interface that can be used to access a property.</span></span>
  
```cpp
HRESULT OpenProperty(
  ULONG ulPropTag,
  LPCIID lpiid,
  ULONG ulInterfaceOptions,
  ULONG ulFlags,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="55712-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="55712-106">Parameters</span></span>

 <span data-ttu-id="55712-107">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="55712-107">_ulPropTag_</span></span>
  
> <span data-ttu-id="55712-108">a Etiqueta de propiedad de la propiedad a la que se va a tener acceso.</span><span class="sxs-lookup"><span data-stu-id="55712-108">[in] The property tag for the property to be accessed.</span></span> <span data-ttu-id="55712-109">El identificador y el tipo deben incluirse en la etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="55712-109">Both the identifier and the type must be included in the property tag.</span></span>
    
 <span data-ttu-id="55712-110">_lpiid_</span><span class="sxs-lookup"><span data-stu-id="55712-110">_lpiid_</span></span>
  
> <span data-ttu-id="55712-111">a Puntero al identificador de la interfaz que se va a usar para obtener acceso a la propiedad.</span><span class="sxs-lookup"><span data-stu-id="55712-111">[in] A pointer to the identifier for the interface to be used to access the property.</span></span> <span data-ttu-id="55712-112">El parámetro _lpiid_ no debe ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="55712-112">The  _lpiid_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="55712-113">_ulInterfaceOptions_</span><span class="sxs-lookup"><span data-stu-id="55712-113">_ulInterfaceOptions_</span></span>
  
> <span data-ttu-id="55712-114">a Datos relacionados con la interfaz identificada por el parámetro _lpiid_ .</span><span class="sxs-lookup"><span data-stu-id="55712-114">[in] Data that relates to the interface identified by the  _lpiid_ parameter.</span></span> 
    
 <span data-ttu-id="55712-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="55712-115">_ulFlags_</span></span>
  
> <span data-ttu-id="55712-116">a Máscara de máscara de marcadores que controla el acceso a la propiedad.</span><span class="sxs-lookup"><span data-stu-id="55712-116">[in] A bitmask of flags that controls access to the property.</span></span> <span data-ttu-id="55712-117">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="55712-117">The following flags can be set:</span></span>
    
<span data-ttu-id="55712-118">MAPI_CREATE</span><span class="sxs-lookup"><span data-stu-id="55712-118">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="55712-119">Si la propiedad no existe, se debe crear.</span><span class="sxs-lookup"><span data-stu-id="55712-119">If the property does not exist, it should be created.</span></span> <span data-ttu-id="55712-120">Si la propiedad existe, se debe descartar el valor actual de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="55712-120">If the property does exist, the current value of the property should be discarded.</span></span> <span data-ttu-id="55712-121">Cuando un autor de llamada establece la marca MAPI_CREATE, también debe establecer la marca MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="55712-121">When a caller sets the MAPI_CREATE flag, it should also set the MAPI_MODIFY flag.</span></span>
    
<span data-ttu-id="55712-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="55712-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="55712-123">Permite que **OpenProperty** vuelva correctamente, posiblemente antes de que el objeto esté completamente disponible para el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="55712-123">Allows **OpenProperty** to return successfully, possibly before the object is fully available to the caller.</span></span> <span data-ttu-id="55712-124">Si el objeto no está disponible, la realización de una llamada de objeto subsiguiente puede generar un error.</span><span class="sxs-lookup"><span data-stu-id="55712-124">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="55712-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="55712-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="55712-126">MAPI_MODIFY es necesario en estas situaciones:</span><span class="sxs-lookup"><span data-stu-id="55712-126">MAPI_MODIFY is required in these situations:</span></span>
    
  - <span data-ttu-id="55712-127">Al abrir una propiedad de flujo, como **IID_IStream**, para modificarla.</span><span class="sxs-lookup"><span data-stu-id="55712-127">When opening a stream property, such as **IID_IStream**, to modify it.</span></span>
    
  - <span data-ttu-id="55712-128">Al abrir datos adjuntos de un mensaje incrustado, como [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) abierto con **IID_IMessage**, para modificarlo.</span><span class="sxs-lookup"><span data-stu-id="55712-128">When opening an embedded message attachment, such as [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) opened with **IID_IMessage**, to modify it.</span></span>
    
 <span data-ttu-id="55712-129">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="55712-129">_lppUnk_</span></span>
  
> <span data-ttu-id="55712-130">contempla Puntero a la interfaz solicitada que se va a utilizar para el acceso a la propiedad.</span><span class="sxs-lookup"><span data-stu-id="55712-130">[out] A pointer to the requested interface to be used for property access.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="55712-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="55712-131">Return value</span></span>

<span data-ttu-id="55712-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="55712-132">S_OK</span></span> 
  
> <span data-ttu-id="55712-133">El puntero de interfaz solicitado se ha devuelto correctamente.</span><span class="sxs-lookup"><span data-stu-id="55712-133">The requested interface pointer was successfully returned.</span></span>
    
<span data-ttu-id="55712-134">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="55712-134">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="55712-135">La interfaz solicitada no es compatible con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="55712-135">The requested interface is not supported for this property.</span></span>
    
<span data-ttu-id="55712-136">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="55712-136">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="55712-137">El autor de la llamada no tiene suficientes permisos para obtener acceso a la propiedad.</span><span class="sxs-lookup"><span data-stu-id="55712-137">The caller has insufficient permissions to access the property.</span></span>
    
<span data-ttu-id="55712-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="55712-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="55712-139">El objeto no puede proporcionar acceso a esta propiedad a través de la interfaz solicitada.</span><span class="sxs-lookup"><span data-stu-id="55712-139">The object cannot provide access to this property through the requested interface.</span></span>
    
<span data-ttu-id="55712-140">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="55712-140">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="55712-141">La propiedad solicitada no existe y MAPI_CREATE no se estableció en el parámetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="55712-141">The requested property does not exist and MAPI_CREATE was not set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="55712-142">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="55712-142">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="55712-143">El tipo de propiedad de la etiqueta se establece en PT_UNSPECIFIED.</span><span class="sxs-lookup"><span data-stu-id="55712-143">The property type in the tag is set to PT_UNSPECIFIED.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="55712-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="55712-144">Remarks</span></span>

<span data-ttu-id="55712-145">El método **IMAPIProp:: OpenProperty** proporciona acceso a una propiedad a través de una interfaz determinada.</span><span class="sxs-lookup"><span data-stu-id="55712-145">The **IMAPIProp::OpenProperty** method provides access to a property through a particular interface.</span></span> <span data-ttu-id="55712-146">**OpenProperty** es una alternativa a los métodos [IMAPIProp:: GetProps](imapiprop-getprops.md) y [IMAPIProp:: SetProps](imapiprop-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="55712-146">**OpenProperty** is an alternative to the [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::SetProps](imapiprop-setprops.md) methods.</span></span> <span data-ttu-id="55712-147">Cuando se produce un error en **GetProps** o **SetProps** porque la propiedad es demasiado grande o demasiado compleja, llame a **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="55712-147">When either **GetProps** or **SetProps** fails because the property is too large or too complex, call **OpenProperty**.</span></span> <span data-ttu-id="55712-148">**OpenProperty** se usa normalmente para obtener acceso a las propiedades de tipo PT Object.</span><span class="sxs-lookup"><span data-stu-id="55712-148">**OpenProperty** is typically used to access properties of type PT_OBJECT.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="55712-149">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="55712-149">Notes to callers</span></span>

<span data-ttu-id="55712-150">Para tener acceso a los datos adjuntos de los mensajes, abra la propiedad **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) con un identificador de interfaz diferente, según el tipo de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="55712-150">To access message attachments, open the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property with a different interface identifier, depending on the type of attachment.</span></span> <span data-ttu-id="55712-151">En la tabla siguiente se describe cómo llamar a **OpenProperty** para los distintos tipos de datos adjuntos:</span><span class="sxs-lookup"><span data-stu-id="55712-151">The following table describes how to call **OpenProperty** for the different types of attachments:</span></span> 
  
|<span data-ttu-id="55712-152">**Tipo de datos adjuntos**</span><span class="sxs-lookup"><span data-stu-id="55712-152">**Type of attachment**</span></span>|<span data-ttu-id="55712-153">**Identificador de interfaz que se va a usar**</span><span class="sxs-lookup"><span data-stu-id="55712-153">**Interface identifier to use**</span></span>|
|:-----|:-----|
|<span data-ttu-id="55712-154">Binary</span><span class="sxs-lookup"><span data-stu-id="55712-154">Binary</span></span>  <br/> |<span data-ttu-id="55712-155">IID_IStream</span><span class="sxs-lookup"><span data-stu-id="55712-155">IID_IStream</span></span>  <br/> |
|<span data-ttu-id="55712-156">String</span><span class="sxs-lookup"><span data-stu-id="55712-156">String</span></span>  <br/> |<span data-ttu-id="55712-157">IID_IStream</span><span class="sxs-lookup"><span data-stu-id="55712-157">IID_IStream</span></span>  <br/> |
|<span data-ttu-id="55712-158">Mensaje</span><span class="sxs-lookup"><span data-stu-id="55712-158">Message</span></span>  <br/> |<span data-ttu-id="55712-159">IID_IMessage</span><span class="sxs-lookup"><span data-stu-id="55712-159">IID_IMessage</span></span>  <br/> |
|<span data-ttu-id="55712-160">OLE 2,0</span><span class="sxs-lookup"><span data-stu-id="55712-160">OLE 2.0</span></span>  <br/> |<span data-ttu-id="55712-161">IID_IStreamDocfile</span><span class="sxs-lookup"><span data-stu-id="55712-161">IID_IStreamDocfile</span></span>  <br/> |
   
<span data-ttu-id="55712-162">**IStreamDocfile** es un derivado de la interfaz [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) que se basa en un archivo compuesto OLE 2,0.</span><span class="sxs-lookup"><span data-stu-id="55712-162">**IStreamDocfile** is a derivative of the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface that is based on an OLE 2.0 compound file.</span></span> <span data-ttu-id="55712-163">**IStreamDocfile** es la mejor opción para obtener acceso a los datos adjuntos de OLE 2,0 porque implica la menor cantidad de sobrecarga.</span><span class="sxs-lookup"><span data-stu-id="55712-163">**IStreamDocfile** is the best choice for accessing OLE 2.0 attachments because it involves the least amount of overhead.</span></span> <span data-ttu-id="55712-164">Puede usar IID_IStreamDocFile para las propiedades que contienen datos almacenados en el almacenamiento estructurado disponible a través de la interfaz [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="55712-164">You can use IID_IStreamDocFile for those properties that contain data stored in structured storage available through the [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) interface.</span></span> 
  
<span data-ttu-id="55712-165">Para obtener más información acerca de cómo usar **OpenProperty** con datos adjuntos, vea la propiedad **PR_ATTACH_DATA_OBJ** y [abrir datos](opening-an-attachment.md)adjuntos.</span><span class="sxs-lookup"><span data-stu-id="55712-165">For more information about how to use **OpenProperty** with attachments, see the **PR_ATTACH_DATA_OBJ** property and [Opening an Attachment](opening-an-attachment.md).</span></span>
  
<span data-ttu-id="55712-166">No use el puntero **IStream** que reciba para llamar a su método [Seek](https://msdn.microsoft.com/library/aa380043%28v=VS.85%29.aspx) o [setSize](https://msdn.microsoft.com/library/aa380044%28v=VS.85%29.aspx) a menos que use una variable de tamaño o de posición cero.</span><span class="sxs-lookup"><span data-stu-id="55712-166">Do not use the **IStream** pointer that you receive to call either its [Seek](https://msdn.microsoft.com/library/aa380043%28v=VS.85%29.aspx) or [SetSize](https://msdn.microsoft.com/library/aa380044%28v=VS.85%29.aspx) method unless you use a zero position or size variable.</span></span> <span data-ttu-id="55712-167">Además, no confíe en el valor del parámetro de salida _plibNewPosition_ devuelto desde la llamada a **Seek** .</span><span class="sxs-lookup"><span data-stu-id="55712-167">Also, do not rely on the value of the  _plibNewPosition_ output parameter returned from the **Seek** call.</span></span> 
  
<span data-ttu-id="55712-168">Si llama a **OpenProperty** para tener acceso a una propiedad con la interfaz **IStream** , use sólo esa interfaz para realizar cambios.</span><span class="sxs-lookup"><span data-stu-id="55712-168">If you call **OpenProperty** to access a property with the **IStream** interface, use only that interface to make changes to it.</span></span> <span data-ttu-id="55712-169">No intente actualizar la propiedad con ninguno de los otros métodos [IMAPIProp: IUnknown](imapipropiunknown.md) , como **SetProps** o [IMAPIProp::D eleteprops](imapiprop-deleteprops.md).</span><span class="sxs-lookup"><span data-stu-id="55712-169">Do not attempt to update the property with any of the other [IMAPIProp : IUnknown](imapipropiunknown.md) methods, such as **SetProps** or [IMAPIProp::DeleteProps](imapiprop-deleteprops.md).</span></span> 
  
<span data-ttu-id="55712-170">No intente abrir una propiedad con **OpenProperty** más de una vez.</span><span class="sxs-lookup"><span data-stu-id="55712-170">Do not try to open a property with **OpenProperty** more than once.</span></span> <span data-ttu-id="55712-171">Los resultados no están definidos porque pueden variar de un proveedor a un proveedor.</span><span class="sxs-lookup"><span data-stu-id="55712-171">The results are undefined because they can vary from provider to provider.</span></span> 
  
<span data-ttu-id="55712-172">Si necesita modificar la propiedad que se va a abrir, establezca la marca MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="55712-172">If you need to modify the property to be opened, set the MAPI_MODIFY flag.</span></span> <span data-ttu-id="55712-173">Si no está seguro de si el objeto admite la propiedad pero cree que debería, establezca las marcas MAPI_CREATE y MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="55712-173">If you are not sure whether the object supports the property but you think it should, set the MAPI_CREATE and MAPI_MODIFY flags.</span></span> <span data-ttu-id="55712-174">Siempre que se establece MAPI_CREATE, se debe establecer MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="55712-174">Whenever MAPI_CREATE is set, MAPI_MODIFY must also be set.</span></span>
  
<span data-ttu-id="55712-175">Usted es responsable de reconvertir el puntero de interfaz devuelto en el parámetro _lppUnk_ en uno que sea adecuado para la interfaz especificada en el parámetro _lpiid_ .</span><span class="sxs-lookup"><span data-stu-id="55712-175">You are responsible for recasting the interface pointer returned in the  _lppUnk_ parameter to one that is appropriate for the interface specified in the  _lpiid_ parameter.</span></span> <span data-ttu-id="55712-176">También debe usar el puntero devuelto para llamar a su método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) cuando haya terminado.</span><span class="sxs-lookup"><span data-stu-id="55712-176">You must also use the returned pointer to call its [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method when you are finished with it.</span></span> 
  
<span data-ttu-id="55712-177">A veces, la configuración de las marcas en el parámetro _ulFlags_ no es suficiente para indicar el tipo de acceso a la propiedad que se requiere.</span><span class="sxs-lookup"><span data-stu-id="55712-177">Sometimes setting the flags in the  _ulFlags_ parameter is not enough to indicate the type of access to the property that is required.</span></span> <span data-ttu-id="55712-178">Puede colocar datos adicionales, como indicadores, en el parámetro _ulInterfaceOptions_ .</span><span class="sxs-lookup"><span data-stu-id="55712-178">You can put additional data, such as flags, in the  _ulInterfaceOptions_ parameter.</span></span> <span data-ttu-id="55712-179">Estos datos dependen de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="55712-179">This data is interface dependent.</span></span> <span data-ttu-id="55712-180">Algunas interfaces (como **IStream**) la usan y otras no.</span><span class="sxs-lookup"><span data-stu-id="55712-180">Some interfaces (such as **IStream**) use it, and others do not.</span></span> <span data-ttu-id="55712-181">Por ejemplo, al abrir una propiedad que se va a modificar con **IStream**, establezca la marca STGM_WRITE en el parámetro _ULINTERFACEOPTIONS_ además de MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="55712-181">For example, when you open a property to be modified with **IStream**, set the STGM_WRITE flag in the  _ulInterfaceOptions_ parameter in addition to MAPI_MODIFY.</span></span> <span data-ttu-id="55712-182">Al abrir una tabla mediante la interfaz [IMAPITable](imapitableiunknown.md) , puede establecer _ulInterfaceOptions_ en MAPI_UNICODE para indicar si las columnas de la tabla que contienen propiedades de cadena deben estar en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="55712-182">When you open a table by using the [IMAPITable](imapitableiunknown.md) interface, you can set  _ulInterfaceOptions_ to MAPI_UNICODE to indicate whether the columns in the table that hold string properties should be in Unicode format.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="55712-183">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="55712-183">MFCMAPI reference</span></span>

<span data-ttu-id="55712-184">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="55712-184">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="55712-185">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="55712-185">**File**</span></span>|<span data-ttu-id="55712-186">**Función**</span><span class="sxs-lookup"><span data-stu-id="55712-186">**Function**</span></span>|<span data-ttu-id="55712-187">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="55712-187">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="55712-188">StreamEditor. cpp</span><span class="sxs-lookup"><span data-stu-id="55712-188">StreamEditor.cpp</span></span>  <br/> |<span data-ttu-id="55712-189">CStreamEditor:: ReadTextStreamFromProperty</span><span class="sxs-lookup"><span data-stu-id="55712-189">CStreamEditor::ReadTextStreamFromProperty</span></span>  <br/> |<span data-ttu-id="55712-190">MFCMAPI usa el método **IMAPIProp:: OpenProperty** para recuperar una interfaz de secuencia para las propiedades binarias y de texto de gran tamaño.</span><span class="sxs-lookup"><span data-stu-id="55712-190">MFCMAPI uses the **IMAPIProp::OpenProperty** method to retrieve a stream interface for large text and binary properties.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="55712-191">Vea también</span><span class="sxs-lookup"><span data-stu-id="55712-191">See also</span></span>

- [<span data-ttu-id="55712-192">HrIStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="55712-192">HrIStorageFromStream</span></span>](hristoragefromstream.md) 
- [<span data-ttu-id="55712-193">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="55712-193">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md) 
- [<span data-ttu-id="55712-194">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="55712-194">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
- [<span data-ttu-id="55712-195">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="55712-195">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
- [<span data-ttu-id="55712-196">IMAPISupport::IStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="55712-196">IMAPISupport::IStorageFromStream</span></span>](imapisupport-istoragefromstream.md)
- [<span data-ttu-id="55712-197">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="55712-197">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
- [<span data-ttu-id="55712-198">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="55712-198">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
- [<span data-ttu-id="55712-199">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="55712-199">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
- [<span data-ttu-id="55712-200">Apertura de datos adJuntos</span><span class="sxs-lookup"><span data-stu-id="55712-200">Opening an Attachment</span></span>](opening-an-attachment.md)

