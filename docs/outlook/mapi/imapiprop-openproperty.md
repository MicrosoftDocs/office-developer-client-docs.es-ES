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
ms.openlocfilehash: 656e5c5532edfc6c791ca30aa30f4c4d96847295
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817415"
---
# <a name="imapipropopenproperty"></a><span data-ttu-id="72f98-103">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="72f98-103">IMAPIProp::OpenProperty</span></span>

<span data-ttu-id="72f98-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="72f98-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="72f98-105">Devuelve un puntero a una interfaz que se puede usar para obtener acceso a una propiedad.</span><span class="sxs-lookup"><span data-stu-id="72f98-105">Returns a pointer to an interface that can be used to access a property.</span></span>
  
```cpp
HRESULT OpenProperty(
  ULONG ulPropTag,
  LPCIID lpiid,
  ULONG ulInterfaceOptions,
  ULONG ulFlags,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="72f98-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="72f98-106">Parameters</span></span>

 <span data-ttu-id="72f98-107">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="72f98-107">_ulPropTag_</span></span>
  
> <span data-ttu-id="72f98-108">[entrada] La etiqueta de propiedad tener acceso a la propiedad.</span><span class="sxs-lookup"><span data-stu-id="72f98-108">[in] The property tag for the property to be accessed.</span></span> <span data-ttu-id="72f98-109">El identificador y el tipo deben ser incluidos en la etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="72f98-109">Both the identifier and the type must be included in the property tag.</span></span>
    
 <span data-ttu-id="72f98-110">_lpiid_</span><span class="sxs-lookup"><span data-stu-id="72f98-110">_lpiid_</span></span>
  
> <span data-ttu-id="72f98-111">[entrada] Un puntero al identificador de la interfaz que se usará para tener acceso a la propiedad.</span><span class="sxs-lookup"><span data-stu-id="72f98-111">[in] A pointer to the identifier for the interface to be used to access the property.</span></span> <span data-ttu-id="72f98-112">El parámetro _lpiid_ no debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="72f98-112">The  _lpiid_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="72f98-113">_ulInterfaceOptions_</span><span class="sxs-lookup"><span data-stu-id="72f98-113">_ulInterfaceOptions_</span></span>
  
> <span data-ttu-id="72f98-114">[entrada] Datos que se relación con la interfaz identificada mediante el parámetro _lpiid_ .</span><span class="sxs-lookup"><span data-stu-id="72f98-114">[in] Data that relates to the interface identified by the  _lpiid_ parameter.</span></span> 
    
 <span data-ttu-id="72f98-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="72f98-115">_ulFlags_</span></span>
  
> <span data-ttu-id="72f98-116">[entrada] Una máscara de bits de indicadores que controla el acceso a la propiedad.</span><span class="sxs-lookup"><span data-stu-id="72f98-116">[in] A bitmask of flags that controls access to the property.</span></span> <span data-ttu-id="72f98-117">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="72f98-117">The following flags can be set:</span></span>
    
<span data-ttu-id="72f98-118">MAPI_CREATE</span><span class="sxs-lookup"><span data-stu-id="72f98-118">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="72f98-119">Si la propiedad no existe, se debe crear.</span><span class="sxs-lookup"><span data-stu-id="72f98-119">If the property does not exist, it should be created.</span></span> <span data-ttu-id="72f98-120">Si la propiedad existe, debe descartarse el valor actual de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="72f98-120">If the property does exist, the current value of the property should be discarded.</span></span> <span data-ttu-id="72f98-121">Cuando un autor de la llamada establece la marca MAPI_CREATE, también debe establecer la marca MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="72f98-121">When a caller sets the MAPI_CREATE flag, it should also set the MAPI_MODIFY flag.</span></span>
    
<span data-ttu-id="72f98-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="72f98-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="72f98-123">Permite **OpenProperty** devolver de correctamente, posiblemente antes de que el objeto está totalmente disponible para el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="72f98-123">Allows **OpenProperty** to return successfully, possibly before the object is fully available to the caller.</span></span> <span data-ttu-id="72f98-124">Si el objeto no está disponible, realizar una llamada de objeto posteriores puede provocar un error.</span><span class="sxs-lookup"><span data-stu-id="72f98-124">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="72f98-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="72f98-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="72f98-126">MAPI_MODIFY es necesaria en estas situaciones:</span><span class="sxs-lookup"><span data-stu-id="72f98-126">MAPI_MODIFY is required in these situations:</span></span>
    
  - <span data-ttu-id="72f98-127">Al abrir una propiedad de secuencia, como **IID_IStream**para modificarla.</span><span class="sxs-lookup"><span data-stu-id="72f98-127">When opening a stream property, such as **IID_IStream**, to modify it.</span></span>
    
  - <span data-ttu-id="72f98-128">Cuando abra un archivo adjunto de incrustación de mensajes, como [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) , se abre con **IID_IMessage**, que lo modifique.</span><span class="sxs-lookup"><span data-stu-id="72f98-128">When opening an embedded message attachment, such as [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) opened with **IID_IMessage**, to modify it.</span></span>
    
 <span data-ttu-id="72f98-129">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="72f98-129">_lppUnk_</span></span>
  
> <span data-ttu-id="72f98-130">[out] Un puntero a la interfaz que se usará para el acceso a la propiedad solicitada.</span><span class="sxs-lookup"><span data-stu-id="72f98-130">[out] A pointer to the requested interface to be used for property access.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="72f98-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="72f98-131">Return value</span></span>

<span data-ttu-id="72f98-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="72f98-132">S_OK</span></span> 
  
> <span data-ttu-id="72f98-133">El puntero de interfaz solicitada se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="72f98-133">The requested interface pointer was successfully returned.</span></span>
    
<span data-ttu-id="72f98-134">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="72f98-134">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="72f98-135">La interfaz solicitada no se admite para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="72f98-135">The requested interface is not supported for this property.</span></span>
    
<span data-ttu-id="72f98-136">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="72f98-136">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="72f98-137">El autor de la llamada no tiene permisos suficientes para tener acceso a la propiedad.</span><span class="sxs-lookup"><span data-stu-id="72f98-137">The caller has insufficient permissions to access the property.</span></span>
    
<span data-ttu-id="72f98-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="72f98-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="72f98-139">El objeto no puede proporcionar acceso a esta propiedad a través de la interfaz solicitada.</span><span class="sxs-lookup"><span data-stu-id="72f98-139">The object cannot provide access to this property through the requested interface.</span></span>
    
<span data-ttu-id="72f98-140">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="72f98-140">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="72f98-141">La propiedad solicitada no existe y no se ha establecido MAPI_CREATE en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="72f98-141">The requested property does not exist and MAPI_CREATE was not set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="72f98-142">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="72f98-142">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="72f98-143">El tipo de propiedad en la etiqueta se establece en PT_UNSPECIFIED.</span><span class="sxs-lookup"><span data-stu-id="72f98-143">The property type in the tag is set to PT_UNSPECIFIED.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="72f98-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="72f98-144">Remarks</span></span>

<span data-ttu-id="72f98-145">El método **IMAPIProp::OpenProperty** proporciona acceso a una propiedad a través de una interfaz determinada.</span><span class="sxs-lookup"><span data-stu-id="72f98-145">The **IMAPIProp::OpenProperty** method provides access to a property through a particular interface.</span></span> <span data-ttu-id="72f98-146">**OpenProperty** es una alternativa a los métodos [IMAPIProp::GetProps](imapiprop-getprops.md) y [IMAPIProp::SetProps](imapiprop-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="72f98-146">**OpenProperty** is an alternative to the [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::SetProps](imapiprop-setprops.md) methods.</span></span> <span data-ttu-id="72f98-147">Cuando se produce un error debido a que la propiedad es demasiado grande o demasiado compleja **GetProps** o **SetProps** , llamar **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="72f98-147">When either **GetProps** or **SetProps** fails because the property is too large or too complex, call **OpenProperty**.</span></span> <span data-ttu-id="72f98-148">**OpenProperty** normalmente se usa para tener acceso a las propiedades de tipo pt Object.</span><span class="sxs-lookup"><span data-stu-id="72f98-148">**OpenProperty** is typically used to access properties of type PT_OBJECT.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="72f98-149">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="72f98-149">Notes to callers</span></span>

<span data-ttu-id="72f98-150">Para obtener acceso a datos adjuntos de mensajes, abra la propiedad **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) con un identificador de interfaz diferente, según el tipo de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="72f98-150">To access message attachments, open the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property with a different interface identifier, depending on the type of attachment.</span></span> <span data-ttu-id="72f98-151">En la siguiente tabla se describe cómo llamar a **OpenProperty** para los diferentes tipos de datos adjuntos:</span><span class="sxs-lookup"><span data-stu-id="72f98-151">The following table describes how to call **OpenProperty** for the different types of attachments:</span></span> 
  
|<span data-ttu-id="72f98-152">**Tipo de datos adjuntos**</span><span class="sxs-lookup"><span data-stu-id="72f98-152">**Type of attachment**</span></span>|<span data-ttu-id="72f98-153">**Identificador de interfaz que se utiliza**</span><span class="sxs-lookup"><span data-stu-id="72f98-153">**Interface identifier to use**</span></span>|
|:-----|:-----|
|<span data-ttu-id="72f98-154">Binario</span><span class="sxs-lookup"><span data-stu-id="72f98-154">Binary</span></span>  <br/> |<span data-ttu-id="72f98-155">IID_IStream</span><span class="sxs-lookup"><span data-stu-id="72f98-155">IID_IStream</span></span>  <br/> |
|<span data-ttu-id="72f98-156">String</span><span class="sxs-lookup"><span data-stu-id="72f98-156">String</span></span>  <br/> |<span data-ttu-id="72f98-157">IID_IStream</span><span class="sxs-lookup"><span data-stu-id="72f98-157">IID_IStream</span></span>  <br/> |
|<span data-ttu-id="72f98-158">Message</span><span class="sxs-lookup"><span data-stu-id="72f98-158">Message</span></span>  <br/> |<span data-ttu-id="72f98-159">IID_IMessage</span><span class="sxs-lookup"><span data-stu-id="72f98-159">IID_IMessage</span></span>  <br/> |
|<span data-ttu-id="72f98-160">OLE 2.0</span><span class="sxs-lookup"><span data-stu-id="72f98-160">OLE 2.0</span></span>  <br/> |<span data-ttu-id="72f98-161">IID_IStreamDocfile</span><span class="sxs-lookup"><span data-stu-id="72f98-161">IID_IStreamDocfile</span></span>  <br/> |
   
<span data-ttu-id="72f98-162">**IStreamDocfile** es un derivado de la interfaz [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) que se basa en un archivo compuesto OLE 2.0.</span><span class="sxs-lookup"><span data-stu-id="72f98-162">**IStreamDocfile** is a derivative of the [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) interface that is based on an OLE 2.0 compound file.</span></span> <span data-ttu-id="72f98-163">**IStreamDocfile** es la mejor opción para obtener acceso a los datos adjuntos de OLE 2.0, ya que implica la menor cantidad de sobrecarga.</span><span class="sxs-lookup"><span data-stu-id="72f98-163">**IStreamDocfile** is the best choice for accessing OLE 2.0 attachments because it involves the least amount of overhead.</span></span> <span data-ttu-id="72f98-164">Puede usar IID_IStreamDocFile para las propiedades que contienen datos almacenados en almacenamiento estructurado disponible a través de la interfaz [IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="72f98-164">You can use IID_IStreamDocFile for those properties that contain data stored in structured storage available through the [IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx) interface.</span></span> 
  
<span data-ttu-id="72f98-165">Para obtener más información acerca de cómo usar **OpenProperty** con datos adjuntos, vea la propiedad **PR_ATTACH_DATA_OBJ** y [Abrir un archivo adjunto](opening-an-attachment.md).</span><span class="sxs-lookup"><span data-stu-id="72f98-165">For more information about how to use **OpenProperty** with attachments, see the **PR_ATTACH_DATA_OBJ** property and [Opening an Attachment](opening-an-attachment.md).</span></span>
  
<span data-ttu-id="72f98-166">No use el puntero **IStream** que reciben para llamar al método su [Seek](http://msdn.microsoft.com/en-us/library/aa380043%28v=VS.85%29.aspx) o [SetSize](http://msdn.microsoft.com/en-us/library/aa380044%28v=VS.85%29.aspx) a menos que utilice una cero variable de tamaño o posición.</span><span class="sxs-lookup"><span data-stu-id="72f98-166">Do not use the **IStream** pointer that you receive to call either its [Seek](http://msdn.microsoft.com/en-us/library/aa380043%28v=VS.85%29.aspx) or [SetSize](http://msdn.microsoft.com/en-us/library/aa380044%28v=VS.85%29.aspx) method unless you use a zero position or size variable.</span></span> <span data-ttu-id="72f98-167">Además, no se basan en el valor del parámetro de salida _plibNewPosition_ devuelto de la llamada **Seek** .</span><span class="sxs-lookup"><span data-stu-id="72f98-167">Also, do not rely on the value of the  _plibNewPosition_ output parameter returned from the **Seek** call.</span></span> 
  
<span data-ttu-id="72f98-168">Si se llama **OpenProperty** para tener acceso a una propiedad con la interfaz **IStream** , use sólo esa interfaz para realizar cambios en él.</span><span class="sxs-lookup"><span data-stu-id="72f98-168">If you call **OpenProperty** to access a property with the **IStream** interface, use only that interface to make changes to it.</span></span> <span data-ttu-id="72f98-169">No intente actualizar la propiedad con cualquiera de las otras [IMAPIProp: IUnknown](imapipropiunknown.md) métodos, como **SetProps** o [IMAPIProp::DeleteProps](imapiprop-deleteprops.md).</span><span class="sxs-lookup"><span data-stu-id="72f98-169">Do not attempt to update the property with any of the other [IMAPIProp : IUnknown](imapipropiunknown.md) methods, such as **SetProps** or [IMAPIProp::DeleteProps](imapiprop-deleteprops.md).</span></span> 
  
<span data-ttu-id="72f98-170">No intente abrir una propiedad con **OpenProperty** más de una vez.</span><span class="sxs-lookup"><span data-stu-id="72f98-170">Do not try to open a property with **OpenProperty** more than once.</span></span> <span data-ttu-id="72f98-171">Los resultados son undefined porque pueden variar de un proveedor a otro.</span><span class="sxs-lookup"><span data-stu-id="72f98-171">The results are undefined because they can vary from provider to provider.</span></span> 
  
<span data-ttu-id="72f98-172">Si necesita modificar la propiedad que se va a abrir, establecer la marca MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="72f98-172">If you need to modify the property to be opened, set the MAPI_MODIFY flag.</span></span> <span data-ttu-id="72f98-173">Si no está seguro de si el objeto es compatible con la propiedad pero cree que debería, establezca los indicadores MAPI_CREATE y MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="72f98-173">If you are not sure whether the object supports the property but you think it should, set the MAPI_CREATE and MAPI_MODIFY flags.</span></span> <span data-ttu-id="72f98-174">Siempre que se establezca MAPI_CREATE, también se debe establecer MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="72f98-174">Whenever MAPI_CREATE is set, MAPI_MODIFY must also be set.</span></span>
  
<span data-ttu-id="72f98-175">Usted es responsable de refundición el puntero de interfaz devuelto en el parámetro _lppUnk_ a uno que sea apropiado para la interfaz especificada en el parámetro _lpiid_ .</span><span class="sxs-lookup"><span data-stu-id="72f98-175">You are responsible for recasting the interface pointer returned in the  _lppUnk_ parameter to one that is appropriate for the interface specified in the  _lpiid_ parameter.</span></span> <span data-ttu-id="72f98-176">También debe usar el puntero devuelto para llamar al método [IUnknown:: Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) cuando haya terminado con él.</span><span class="sxs-lookup"><span data-stu-id="72f98-176">You must also use the returned pointer to call its [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method when you are finished with it.</span></span> 
  
<span data-ttu-id="72f98-177">En ocasiones, establecer los marcadores en el parámetro _ulFlags indicado_ no es suficiente para indicar el tipo de acceso a la propiedad que es necesario.</span><span class="sxs-lookup"><span data-stu-id="72f98-177">Sometimes setting the flags in the  _ulFlags_ parameter is not enough to indicate the type of access to the property that is required.</span></span> <span data-ttu-id="72f98-178">Puede colocar datos adicionales, como indicadores, en el parámetro _ulInterfaceOptions_ .</span><span class="sxs-lookup"><span data-stu-id="72f98-178">You can put additional data, such as flags, in the  _ulInterfaceOptions_ parameter.</span></span> <span data-ttu-id="72f98-179">Estos datos son dependientes de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="72f98-179">This data is interface dependent.</span></span> <span data-ttu-id="72f98-180">Algunas interfaces (como **IStream**) usarla y otros no lo hacen.</span><span class="sxs-lookup"><span data-stu-id="72f98-180">Some interfaces (such as **IStream**) use it, and others do not.</span></span> <span data-ttu-id="72f98-181">Por ejemplo, cuando se abre una propiedad que se debe modificar con **IStream**, establecer la marca STGM_WRITE en el parámetro _ulInterfaceOptions_ además de MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="72f98-181">For example, when you open a property to be modified with **IStream**, set the STGM_WRITE flag in the  _ulInterfaceOptions_ parameter in addition to MAPI_MODIFY.</span></span> <span data-ttu-id="72f98-182">Cuando se abre una tabla mediante la interfaz [IMAPITable](imapitableiunknown.md) , puede establecer _ulInterfaceOptions_ en MAPI_UNICODE para indicar si las columnas de la tabla que tienen propiedades de cadena deben estar en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="72f98-182">When you open a table by using the [IMAPITable](imapitableiunknown.md) interface, you can set  _ulInterfaceOptions_ to MAPI_UNICODE to indicate whether the columns in the table that hold string properties should be in Unicode format.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="72f98-183">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="72f98-183">MFCMAPI reference</span></span>

<span data-ttu-id="72f98-184">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="72f98-184">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="72f98-185">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="72f98-185">**File**</span></span>|<span data-ttu-id="72f98-186">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="72f98-186">**Function**</span></span>|<span data-ttu-id="72f98-187">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="72f98-187">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="72f98-188">StreamEditor.cpp</span><span class="sxs-lookup"><span data-stu-id="72f98-188">StreamEditor.cpp</span></span>  <br/> |<span data-ttu-id="72f98-189">CStreamEditor::ReadTextStreamFromProperty</span><span class="sxs-lookup"><span data-stu-id="72f98-189">CStreamEditor::ReadTextStreamFromProperty</span></span>  <br/> |<span data-ttu-id="72f98-190">MFCMAPI usa el método **IMAPIProp::OpenProperty** para recuperar una interfaz de secuencia de texto de gran tamaño y propiedades binarias.</span><span class="sxs-lookup"><span data-stu-id="72f98-190">MFCMAPI uses the **IMAPIProp::OpenProperty** method to retrieve a stream interface for large text and binary properties.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="72f98-191">Vea también</span><span class="sxs-lookup"><span data-stu-id="72f98-191">See also</span></span>

- [<span data-ttu-id="72f98-192">HrIStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="72f98-192">HrIStorageFromStream</span></span>](hristoragefromstream.md) 
- [<span data-ttu-id="72f98-193">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="72f98-193">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md) 
- [<span data-ttu-id="72f98-194">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="72f98-194">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
- [<span data-ttu-id="72f98-195">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="72f98-195">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
- [<span data-ttu-id="72f98-196">IMAPISupport::IStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="72f98-196">IMAPISupport::IStorageFromStream</span></span>](imapisupport-istoragefromstream.md)
- [<span data-ttu-id="72f98-197">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="72f98-197">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
- [<span data-ttu-id="72f98-198">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="72f98-198">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
- [<span data-ttu-id="72f98-199">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="72f98-199">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
- [<span data-ttu-id="72f98-200">Abrir datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="72f98-200">Opening an Attachment</span></span>](opening-an-attachment.md)

