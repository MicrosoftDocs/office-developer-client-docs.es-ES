---
title: OpenIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OpenIMsgOnIStg
api_type:
- HeaderDef
ms.assetid: a98b0b26-9b19-44ca-9b4e-0ad4d1c54325
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 27a5978d85cf06a31f583b82cd39d0001852876b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818439"
---
# <a name="openimsgonistg"></a><span data-ttu-id="1b145-103">OpenIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="1b145-103">OpenIMsgOnIStg</span></span>

<span data-ttu-id="1b145-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1b145-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1b145-105">Crea un nuevo objeto [IMessage](imessageimapiprop.md) encima de un objeto OLE **IStorage** existente, para usarse dentro de una sesión de mensajería.</span><span class="sxs-lookup"><span data-stu-id="1b145-105">Builds a new [IMessage](imessageimapiprop.md) object on top of an existing OLE **IStorage** object, to be used within a message session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1b145-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="1b145-106">Header file:</span></span>  <br/> |<span data-ttu-id="1b145-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="1b145-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="1b145-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="1b145-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1b145-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1b145-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1b145-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="1b145-110">Called by:</span></span>  <br/> |<span data-ttu-id="1b145-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="1b145-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE OpenIMsgOnIStg(
  LPMSGSESS lpMsgSess,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  LPMALLOC lpmalloc,
  LPVOID lpMapiSup,
  LPSTORAGE lpStg,
  MSGCALLRELEASE FAR * lpfMsgCallRelease,
  ULONG ulCallerData,
  ULONG ulFlags,
  LPMESSAGE FAR * lppMsg
);
```

## <a name="parameters"></a><span data-ttu-id="1b145-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1b145-112">Parameters</span></span>

<span data-ttu-id="1b145-113">_lpMsgSess_</span><span class="sxs-lookup"><span data-stu-id="1b145-113">_lpMsgSess_</span></span>
  
> <span data-ttu-id="1b145-114">[entrada] Puntero a un objeto de sesión de mensaje dentro del cual el nuevo **IMessage**- en - objeto **IStorage** es que se creará.</span><span class="sxs-lookup"><span data-stu-id="1b145-114">[in] Pointer to a message session object within which the new **IMessage**-on- **IStorage** object is to be created.</span></span> 
    
<span data-ttu-id="1b145-115">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="1b145-115">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="1b145-116">[entrada] Puntero a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) , que se usará para asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="1b145-116">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
<span data-ttu-id="1b145-117">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="1b145-117">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="1b145-118">[entrada] Puntero a la función [MAPIAllocateMore](mapiallocatemore.md) , que se usará para asignar memoria adicional.</span><span class="sxs-lookup"><span data-stu-id="1b145-118">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
<span data-ttu-id="1b145-119">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="1b145-119">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="1b145-120">[entrada] Puntero a la función [MAPIFreeBuffer](mapifreebuffer.md) , que se usará para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="1b145-120">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
<span data-ttu-id="1b145-121">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="1b145-121">_lpMalloc_</span></span>
  
> <span data-ttu-id="1b145-122">[entrada] Puntero a un objeto del asignador de memoria exposición de la interfaz de OLE **IMalloc** .</span><span class="sxs-lookup"><span data-stu-id="1b145-122">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="1b145-123">**La interfaz** debe usar este método de asignación al trabajar con interfaces como **IStorage** y **IStream**.</span><span class="sxs-lookup"><span data-stu-id="1b145-123">The **IMessage** interface needs to use this allocation method when working with interfaces such as **IStorage** and **IStream**.</span></span> 
    
<span data-ttu-id="1b145-124">_lpMapiSup_</span><span class="sxs-lookup"><span data-stu-id="1b145-124">_lpMapiSup_</span></span>
  
> <span data-ttu-id="1b145-125">[entrada] Puntero opcional a un objeto de soporte técnico MAPI que puede usar un proveedor de servicios para llamar a los métodos de la [IMAPISupport: IUnknown](imapisupportiunknown.md) interfaz.</span><span class="sxs-lookup"><span data-stu-id="1b145-125">[in] Optional pointer to a MAPI support object that a service provider can use to call the methods of the [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> 
    
<span data-ttu-id="1b145-126">_lpStg_</span><span class="sxs-lookup"><span data-stu-id="1b145-126">_lpStg_</span></span>
  
> <span data-ttu-id="1b145-127">[entrada, salida] Puntero a un objeto OLE **IStorage** que está abierto y tiene como de solo lectura o permisos de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="1b145-127">[in, out] Pointer to an OLE **IStorage** object that is open and has read-only or read/write permission.</span></span> <span data-ttu-id="1b145-128">Debido a que **IMessage** no admite el acceso de sólo escritura, **OpenIMsgOnIStg** no acepta un objeto de almacenamiento abierto en modo de sólo escritura.</span><span class="sxs-lookup"><span data-stu-id="1b145-128">Because **IMessage** does not support write-only access, **OpenIMsgOnIStg** does not accept a storage object opened in write-only mode.</span></span> 
    
<span data-ttu-id="1b145-129">_lpfMsgCallRelease_</span><span class="sxs-lookup"><span data-stu-id="1b145-129">_lpfMsgCallRelease_</span></span>
  
> <span data-ttu-id="1b145-130">[entrada] Puntero opcional a una función de devolución de llamada según el prototipo [MSGCALLRELEASE](msgcallrelease.md) es MAPI para llamar a después de la última versión en el **IMessage**- en - objeto **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="1b145-130">[in] Optional pointer to a callback function based on the [MSGCALLRELEASE](msgcallrelease.md) prototype that MAPI is to call following the last release on the **IMessage**-on- **IStorage** object.</span></span> 
    
<span data-ttu-id="1b145-131">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="1b145-131">_ulCallerData_</span></span>
  
> <span data-ttu-id="1b145-132">[entrada] Datos del autor de la llamada guarda por MAPI con el objeto de **IStorage** **IMessage**- en - y se pasan a la **MSGCALLRELEASE** en función de función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="1b145-132">[in] Caller data saved by MAPI with the **IMessage**-on- **IStorage** object and passed to the **MSGCALLRELEASE** based callback function.</span></span> <span data-ttu-id="1b145-133">Los datos proporcionan contexto sobre el objeto **IMessage** que se publica y el objeto de **IStorage** en la parte superior que se generó.</span><span class="sxs-lookup"><span data-stu-id="1b145-133">The data provides context about the **IMessage** object being released and the **IStorage** object on top of which it was built.</span></span> 
    
<span data-ttu-id="1b145-134">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1b145-134">_ulFlags_</span></span>
  
> <span data-ttu-id="1b145-135">[entrada] Máscara de bits de indicadores que se utilizan para controlar si se llama al método OLE **IStorage::Commit** cuando la aplicación de cliente o el proveedor de servicios llama al método **IMessage::SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="1b145-135">[in] Bitmask of flags used to control whether the OLE **IStorage::Commit** method is called when the client application or service provider calls the **IMessage::SaveChanges** method.</span></span> <span data-ttu-id="1b145-136">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="1b145-136">The following flags can be set:</span></span> 
    
<span data-ttu-id="1b145-137">IMSG_NO_ISTG_COMMIT</span><span class="sxs-lookup"><span data-stu-id="1b145-137">IMSG_NO_ISTG_COMMIT</span></span> 
  
> <span data-ttu-id="1b145-138">El método OLE **IStorage::Commit** no es se llama cuando el cliente o el proveedor llama a [SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="1b145-138">The OLE method **IStorage::Commit** is not to be called when the client or provider calls [SaveChanges](imapiprop-savechanges.md).</span></span> 
    
<span data-ttu-id="1b145-139">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="1b145-139">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="1b145-140">Habilita la creación de archivos .msg de Unicode.</span><span class="sxs-lookup"><span data-stu-id="1b145-140">Enables creation of Unicode .msg files.</span></span> <span data-ttu-id="1b145-141">El archivo [IMessage](imessageimapiprop.md) resultante muestra STORE_UNICODE_OK en su [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) y es compatible con propiedades de Unicode.</span><span class="sxs-lookup"><span data-stu-id="1b145-141">The resulting [IMessage](imessageimapiprop.md) file shows STORE_UNICODE_OK in its [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) and supports Unicode properties.</span></span> 
    
  > [!NOTE]
  > <span data-ttu-id="1b145-142">El indicador MAPI_UNICODE sólo se admite en esta función en Outlook 2003 o superior.</span><span class="sxs-lookup"><span data-stu-id="1b145-142">The MAPI_UNICODE flag is only supported in this function on Outlook 2003 or higher.</span></span> 
  
<span data-ttu-id="1b145-143">_lppMsg_</span><span class="sxs-lookup"><span data-stu-id="1b145-143">_lppMsg_</span></span>
  
> <span data-ttu-id="1b145-144">[out] Puntero a un puntero al objeto **IMessage** abierto.</span><span class="sxs-lookup"><span data-stu-id="1b145-144">[out] Pointer to a pointer to the opened **IMessage** object.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1b145-145">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1b145-145">Return value</span></span>

<span data-ttu-id="1b145-146">S_OK</span><span class="sxs-lookup"><span data-stu-id="1b145-146">S_OK</span></span> 
  
> <span data-ttu-id="1b145-147">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="1b145-147">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1b145-148">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1b145-148">Remarks</span></span>

<span data-ttu-id="1b145-149">Sólo se pueden tener acceso a atributos de la propiedad en objetos property, es decir, objetos que implementan la [IMAPIProp: IUnknown](imapipropiunknown.md) interfaz.</span><span class="sxs-lookup"><span data-stu-id="1b145-149">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="1b145-150">Para hacer que las propiedades MAPI esté disponible en un objeto de almacenamiento estructurado OLE, se basa **OpenIMsgOnIStg** un [IMessage: IMAPIProp](imessageimapiprop.md) objeto en la parte superior del objeto OLE **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="1b145-150">To make MAPI properties available on an OLE structured storage object, **OpenIMsgOnIStg** builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="1b145-151">Pueden establecer los atributos de propiedad en dichos objetos o modifica con [SetAttribIMsgOnIStg](setattribimsgonistg.md) y recuperar con [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span><span class="sxs-lookup"><span data-stu-id="1b145-151">The property attributes on such objects can be set or altered with [SetAttribIMsgOnIStg](setattribimsgonistg.md) and retrieved with [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1b145-152">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="1b145-152">Notes to callers</span></span>

<span data-ttu-id="1b145-153">Una sesión de mensajería se debe abrir con [OpenIMsgSession](openimsgsession.md) antes de llamar a **OpenIMsgOnIStg** .</span><span class="sxs-lookup"><span data-stu-id="1b145-153">A message session should be opened with [OpenIMsgSession](openimsgsession.md) before **OpenIMsgOnIStg** is called.</span></span> <span data-ttu-id="1b145-154">Proporcionar un parámetro válido _lpMsgSess_ realizar sures que se crea el nuevo mensaje dentro de una sesión de mensajería para que se cierra cuando se cierra la sesión.</span><span class="sxs-lookup"><span data-stu-id="1b145-154">Supplying a valid  _lpMsgSess_ parameter make sures that the new message is created within a message session so that it is closed when the session is closed.</span></span> <span data-ttu-id="1b145-155">Si _lpMsgSess_ es NULL, el mensaje se crea independientemente de cualquier sesión de mensajería.</span><span class="sxs-lookup"><span data-stu-id="1b145-155">If  _lpMsgSess_ is NULL, the message is created independently of any message session.</span></span> <span data-ttu-id="1b145-156">Si la aplicación de cliente o el proveedor de servicio que creó el mensaje de la versión, así como todos sus datos adjuntos no y abrir tablas, memoria se pierde y puede provocar que se cierre la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1b145-156">If the client application or service provider that created the message does not release it, as well as all its attachments and open tables, memory is leaked and may cause the application to terminate.</span></span> 
  
<span data-ttu-id="1b145-157">MAPI utiliza las funciones que señala _lpAllocateBuffer_, _lpAllocateMore_y _lpFreeBuffer_ para la mayoría de asignación de memoria y cancelación de asignación, en particular para asignar la memoria para su uso por las aplicaciones cliente al llamar a las interfaces de objeto Por ejemplo, [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="1b145-157">MAPI uses the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="1b145-158">Los punteros _lpAllocateBuffer_, _lpAllocateMore_y _lpFreeBuffer_ son opcionales cuando se llama a la función **OpenIMsgOnIStg** con un parámetro válido _lpMapiSup_ .</span><span class="sxs-lookup"><span data-stu-id="1b145-158">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ pointers are optional when the **OpenIMsgOnIStg** function is called with a valid  _lpMapiSup_ parameter.</span></span> 
  
<span data-ttu-id="1b145-159">Debido a que se trata de un objeto OLE subyacente, MAPI también debe usar la asignación de memoria OLE.</span><span class="sxs-lookup"><span data-stu-id="1b145-159">Because it is dealing with an underlying OLE object, MAPI also needs to use OLE memory allocation.</span></span> <span data-ttu-id="1b145-160">Para obtener más información acerca de los objetos de almacenamiento estructurado OLE y asignación de memoria OLE, vea la _referencia del programador de OLE_.</span><span class="sxs-lookup"><span data-stu-id="1b145-160">For more information about OLE structured storage objects and OLE memory allocation, see the  _OLE Programmer's Reference_.</span></span> 
  
<span data-ttu-id="1b145-161">Si se proporciona un valor válido para _lpMapiSup_, **IMessage** es compatible con los indicadores MAPI_DIALOG y ATTACH_DIALOG llamando al método [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) para proporcionar una interfaz de usuario de progreso para el [IMAPIProp::CopyTo](imapiprop-copyto.md) y los métodos de [IMessage::DeleteAttach](imessage-deleteattach.md) .</span><span class="sxs-lookup"><span data-stu-id="1b145-161">If a valid value is supplied for  _lpMapiSup_, **IMessage** supports the MAPI_DIALOG and ATTACH_DIALOG flags by calling the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to supply a progress user interface for the [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMessage::DeleteAttach](imessage-deleteattach.md) methods.</span></span> <span data-ttu-id="1b145-162">Además, el método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) intenta convertir los identificadores de entrada a corto plazo a los identificadores de entrada a largo plazo por una llamada al método [IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md) y realizar llamadas en el objeto resultante de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="1b145-162">Also, the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method attempts to convert short-term entry identifiers to long-term entry identifiers by calling the [IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md) method and making calls on the resulting address book object.</span></span> <span data-ttu-id="1b145-163">Si se pasa NULL para _lpMapiSup_, **IMessage** omite MAPI_DIALOG y ATTACH_DIALOG y almacena los identificadores de entrada a corto plazo sin conversión.</span><span class="sxs-lookup"><span data-stu-id="1b145-163">If NULL is passed for  _lpMapiSup_, **IMessage** ignores MAPI_DIALOG and ATTACH_DIALOG and stores short-term entry identifiers without conversion.</span></span> 
  
<span data-ttu-id="1b145-164">El objeto **IStorage** indicado por el parámetro _lpStg_ debe abrirse en modo STGM_READ o de STGM_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="1b145-164">The **IStorage** object pointed to by the  _lpStg_ parameter must be opened in either the STGM_READ or STGM_READWRITE mode.</span></span> <span data-ttu-id="1b145-165">Si se usa el modo de STGM_READWRITE, también se debe establecer el modo de STGM_TRANSACTED.</span><span class="sxs-lookup"><span data-stu-id="1b145-165">If the STGM_READWRITE mode is used, the STGM_TRANSACTED mode must also be set.</span></span> 
  
<span data-ttu-id="1b145-166">La función de devolución de llamada indicada por el parámetro _lpfMsgCallRelease_ es opcional; Si se proporciona, se debe basar en el prototipo de función [MSGCALLRELEASE](msgcallrelease.md) .</span><span class="sxs-lookup"><span data-stu-id="1b145-166">The callback function pointed to by the  _lpfMsgCallRelease_ parameter is optional; if provided, it should be based on the [MSGCALLRELEASE](msgcallrelease.md) function prototype.</span></span> <span data-ttu-id="1b145-167">**La interfaz** llama cuando el recuento de referencia del objeto **IStorage** **IMessage**- en - se establece en cero por la última llamada a su método de **versión** .</span><span class="sxs-lookup"><span data-stu-id="1b145-167">The **IMessage** interface calls it when the reference count of the **IMessage**-on- **IStorage** object is set to zero by the last call to its **Release** method.</span></span> <span data-ttu-id="1b145-168">La función de devolución de llamada se usa con frecuencia para liberar la interfaz **IStorage** subyacente.</span><span class="sxs-lookup"><span data-stu-id="1b145-168">The callback function is commonly used to free the underlying **IStorage** interface.</span></span> <span data-ttu-id="1b145-169">**IMessage** no intentará tener acceso al objeto **IStorage** indicado por el parámetro _lpStg_ después de realizar la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="1b145-169">**IMessage** will not attempt to access the **IStorage** object pointed to by the  _lpStg_ parameter after making the callback.</span></span> 
  
<span data-ttu-id="1b145-170">Algunos clientes o proveedores podrían escribir datos adicionales para el objeto **IStorage** más allá de qué **IMessage** propio escribe cuando se llama a su método [SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="1b145-170">Some clients or providers might write additional data to the **IStorage** object beyond what **IMessage** itself writes when its [SaveChanges](imapiprop-savechanges.md) method is called.</span></span> <span data-ttu-id="1b145-171">El cliente o el proveedor puede usar la marca IMSG_NO_ISTG_COMMIT para impedir que una llamada al método OLE **IStorage::Commit** durante el procesamiento de una llamada **SaveChanges** ; **IMessage** en este caso el cliente o el proveedor debe propio confirmar el objeto **IStorage** cuando se escriben los datos adicionales.</span><span class="sxs-lookup"><span data-stu-id="1b145-171">The client or provider can use the IMSG_NO_ISTG_COMMIT flag to prevent **IMessage** from calling the OLE **IStorage::Commit** method while processing a **SaveChanges** call; in this case the client or provider must itself commit the **IStorage** object when the additional data is written.</span></span> <span data-ttu-id="1b145-172">Para facilitar esto, la implementación **IMessage** garantías para el nombre de todos los substorages que crea en el objeto de **IStorage** comienzan con la cadena "__", es decir, con dos caracteres de subrayado.</span><span class="sxs-lookup"><span data-stu-id="1b145-172">To aid in this, the **IMessage** implementation guarantees to name all substorages it creates in the **IStorage** object starting with the string "__", that is, with two underscores.</span></span> <span data-ttu-id="1b145-173">El cliente o el proveedor para evitar conflictos de nombres, mantener sus nombres subalmacenamiento fuera de este espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="1b145-173">The client or provider can avoid name collisions by keeping its substorage names out of this namespace.</span></span> 
  
<span data-ttu-id="1b145-174">MAPI no define el comportamiento de varias operaciones open realizadas en un subobjetos de un mensaje, como un archivo adjunto, una secuencia o un mensaje incrustado.</span><span class="sxs-lookup"><span data-stu-id="1b145-174">MAPI does not define the behavior of multiple open operations performed on a subobject of a message, such as an attachment, a stream, or an embedded message.</span></span> <span data-ttu-id="1b145-175">MAPI permite actualmente una subobjetos que ya está abierto para abrirse una vez más, pero MAPI se lleva a cabo la operación de apertura por incrementar el recuento de referencia para el objeto abierto existente y devolución para el cliente o el proveedor que llama la [IMessage::OpenAttach ](imessage-openattach.md)o [IMAPIProp::OpenProperty](imapiprop-openproperty.md) (método).</span><span class="sxs-lookup"><span data-stu-id="1b145-175">MAPI currently allows a subobject that is already open to be opened once more, but MAPI performs the open operation by incrementing the reference count for the existing open object and returning it to the client or provider that called the [IMessage::OpenAttach](imessage-openattach.md) or [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span></span> <span data-ttu-id="1b145-176">Esto significa que el acceso solicitado para la primera operación de apertura en un subobjetos el acceso proporcionado para todas las operaciones de open subsiguientes, independientemente de la solicitada por las operaciones de access.</span><span class="sxs-lookup"><span data-stu-id="1b145-176">This means the access requested for the first open operation on a subobject is the access provided for all subsequent open operations, regardless of the access requested by the operations.</span></span> 
  
<span data-ttu-id="1b145-177">El procedimiento correcto para colocar un mensaje en un archivo adjunto es llamar al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) con un identificador de interfaz de IID_IMessage.</span><span class="sxs-lookup"><span data-stu-id="1b145-177">The correct procedure for placing a message into an attachment is to call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with an interface identifier of IID_IMessage.</span></span> <span data-ttu-id="1b145-178">**OpenProperty** actualmente también admite la creación de datos adjuntos de mensajes disponibles directamente en la interfaz OLE **IStorage** , es decir, utilizando el identificador de la interfaz IID_IStorage.</span><span class="sxs-lookup"><span data-stu-id="1b145-178">**OpenProperty** currently also supports creation of message attachments available directly on the OLE **IStorage** interface, that is, using the IID_IStorage interface identifier.</span></span> <span data-ttu-id="1b145-179">Se admite el acceso de **IStorage** para permitir que una forma sencilla de poner un documento de Microsoft Word en un archivo adjunto sin convertirlo a o desde la interfaz **IStream** OLE.</span><span class="sxs-lookup"><span data-stu-id="1b145-179">**IStorage** access is supported to allow an easy way to put a Microsoft Word document into an attachment without converting it to or from the OLE **IStream** interface.</span></span> <span data-ttu-id="1b145-180">Sin embargo, **IMessage** es posible que no se comportan de forma predecible si **OpenIMsgOnIStg** se pasa un puntero **IStorage** para los datos adjuntos y, a continuación, se liberan los objetos en el orden incorrecto.</span><span class="sxs-lookup"><span data-stu-id="1b145-180">However, **IMessage** may not behave predictably if **OpenIMsgOnIStg** is passed an **IStorage** pointer to the attachment data and then the objects are released in the wrong order.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1b145-181">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1b145-181">MFCMAPI reference</span></span>

<span data-ttu-id="1b145-182">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="1b145-182">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1b145-183">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="1b145-183">**File**</span></span>|<span data-ttu-id="1b145-184">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="1b145-184">**Function**</span></span>|<span data-ttu-id="1b145-185">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="1b145-185">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1b145-186">File.cpp</span><span class="sxs-lookup"><span data-stu-id="1b145-186">File.cpp</span></span>  <br/> |<span data-ttu-id="1b145-187">LoadMSGToMessage</span><span class="sxs-lookup"><span data-stu-id="1b145-187">LoadMSGToMessage</span></span>  <br/> |<span data-ttu-id="1b145-188">MFCMAPI utiliza el método **OpenIMsgOnIStg** para abrir una interfaz en la parte superior de la. MSG de archivos para que el archivo se puede manipular con MAPI.</span><span class="sxs-lookup"><span data-stu-id="1b145-188">MFCMAPI uses the **OpenIMsgOnIStg** method to open an IMessage interface on top of the .MSG file so that the file may be manipulated with MAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1b145-189">Vea también</span><span class="sxs-lookup"><span data-stu-id="1b145-189">See also</span></span>

- [<span data-ttu-id="1b145-190">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="1b145-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

