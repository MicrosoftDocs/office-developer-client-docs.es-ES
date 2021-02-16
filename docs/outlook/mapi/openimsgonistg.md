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
ms.openlocfilehash: 6d5ed20e532f0893757cc46d9ea478c7b65acc86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406524"
---
# <a name="openimsgonistg"></a><span data-ttu-id="48c38-103">OpenIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="48c38-103">OpenIMsgOnIStg</span></span>

<span data-ttu-id="48c38-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48c38-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48c38-105">Crea un nuevo [objeto IMessage](imessageimapiprop.md) sobre un objeto OLE **IStorage** existente, que se usará dentro de una sesión de mensaje.</span><span class="sxs-lookup"><span data-stu-id="48c38-105">Builds a new [IMessage](imessageimapiprop.md) object on top of an existing OLE **IStorage** object, to be used within a message session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="48c38-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="48c38-106">Header file:</span></span>  <br/> |<span data-ttu-id="48c38-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="48c38-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="48c38-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="48c38-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="48c38-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="48c38-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="48c38-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="48c38-110">Called by:</span></span>  <br/> |<span data-ttu-id="48c38-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="48c38-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="48c38-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="48c38-112">Parameters</span></span>

<span data-ttu-id="48c38-113">_lpMsgSess_</span><span class="sxs-lookup"><span data-stu-id="48c38-113">_lpMsgSess_</span></span>
  
> <span data-ttu-id="48c38-114">[entrada] Puntero a un objeto de sesión de mensaje en el que se va a crear el nuevo objeto **IMessage**-on- **IStorage.**</span><span class="sxs-lookup"><span data-stu-id="48c38-114">[in] Pointer to a message session object within which the new **IMessage**-on- **IStorage** object is to be created.</span></span> 
    
<span data-ttu-id="48c38-115">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="48c38-115">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="48c38-116">[entrada] Puntero a la [función MAPIAllocateBuffer,](mapiallocatebuffer.md) que se usará para asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="48c38-116">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
<span data-ttu-id="48c38-117">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="48c38-117">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="48c38-118">[entrada] Puntero a la [función MAPIAllocateMore,](mapiallocatemore.md) que se usará para asignar memoria adicional.</span><span class="sxs-lookup"><span data-stu-id="48c38-118">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
<span data-ttu-id="48c38-119">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="48c38-119">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="48c38-120">[entrada] Puntero a la [función MAPIFreeBuffer,](mapifreebuffer.md) que se usará para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="48c38-120">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
<span data-ttu-id="48c38-121">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="48c38-121">_lpMalloc_</span></span>
  
> <span data-ttu-id="48c38-122">[entrada] Puntero a un objeto de asignador de memoria que expone la interfaz OLE **IMalloc.**</span><span class="sxs-lookup"><span data-stu-id="48c38-122">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="48c38-123">La **interfaz IMessage** debe usar este método de asignación al trabajar con interfaces como **IStorage** **e IStream**.</span><span class="sxs-lookup"><span data-stu-id="48c38-123">The **IMessage** interface needs to use this allocation method when working with interfaces such as **IStorage** and **IStream**.</span></span> 
    
<span data-ttu-id="48c38-124">_lpMapiSup_</span><span class="sxs-lookup"><span data-stu-id="48c38-124">_lpMapiSup_</span></span>
  
> <span data-ttu-id="48c38-125">[entrada] Puntero opcional a un objeto de compatibilidad MAPI que un proveedor de servicios puede usar para llamar a los métodos de la [interfaz IMAPISupport : IUnknown.](imapisupportiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="48c38-125">[in] Optional pointer to a MAPI support object that a service provider can use to call the methods of the [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> 
    
<span data-ttu-id="48c38-126">_lpStg_</span><span class="sxs-lookup"><span data-stu-id="48c38-126">_lpStg_</span></span>
  
> <span data-ttu-id="48c38-127">[entrada, salida] Puntero a un objeto OLE **IStorage** que está abierto y tiene permiso de solo lectura o de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="48c38-127">[in, out] Pointer to an OLE **IStorage** object that is open and has read-only or read/write permission.</span></span> <span data-ttu-id="48c38-128">Dado **que IMessage** no admite el acceso de solo escritura, **OpenIMsgOnIStg** no acepta un objeto de almacenamiento abierto en modo de solo escritura.</span><span class="sxs-lookup"><span data-stu-id="48c38-128">Because **IMessage** does not support write-only access, **OpenIMsgOnIStg** does not accept a storage object opened in write-only mode.</span></span> 
    
<span data-ttu-id="48c38-129">_lpfMsgCallRelease_</span><span class="sxs-lookup"><span data-stu-id="48c38-129">_lpfMsgCallRelease_</span></span>
  
> <span data-ttu-id="48c38-130">[entrada] Puntero opcional a una función de devolución de llamada basada en el prototipo [MSGCALLRELEASE](msgcallrelease.md) al que MAPI llamará después de la última versión del objeto **IMessage**-on- **IStorage.**</span><span class="sxs-lookup"><span data-stu-id="48c38-130">[in] Optional pointer to a callback function based on the [MSGCALLRELEASE](msgcallrelease.md) prototype that MAPI is to call following the last release on the **IMessage**-on- **IStorage** object.</span></span> 
    
<span data-ttu-id="48c38-131">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="48c38-131">_ulCallerData_</span></span>
  
> <span data-ttu-id="48c38-132">[entrada] Datos del autor de la llamada guardados por MAPI con el objeto **IMessage**-on- **IStorage** y pasados a la función de devolución de llamada basada en **MSGCALLRELEASE.**</span><span class="sxs-lookup"><span data-stu-id="48c38-132">[in] Caller data saved by MAPI with the **IMessage**-on- **IStorage** object and passed to the **MSGCALLRELEASE** based callback function.</span></span> <span data-ttu-id="48c38-133">Los datos proporcionan contexto sobre el **objeto IMessage** que se está liberando y el objeto **IStorage** en la parte superior del cual se creó.</span><span class="sxs-lookup"><span data-stu-id="48c38-133">The data provides context about the **IMessage** object being released and the **IStorage** object on top of which it was built.</span></span> 
    
<span data-ttu-id="48c38-134">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="48c38-134">_ulFlags_</span></span>
  
> <span data-ttu-id="48c38-135">[entrada] Máscara de bits de marcas usadas para controlar si se llama al método OLE **IStorage::Commit** cuando la aplicación cliente o el proveedor de servicios llama al método **IMessage::SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="48c38-135">[in] Bitmask of flags used to control whether the OLE **IStorage::Commit** method is called when the client application or service provider calls the **IMessage::SaveChanges** method.</span></span> <span data-ttu-id="48c38-136">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="48c38-136">The following flags can be set:</span></span> 
    
<span data-ttu-id="48c38-137">IMSG_NO_ISTG_COMMIT</span><span class="sxs-lookup"><span data-stu-id="48c38-137">IMSG_NO_ISTG_COMMIT</span></span> 
  
> <span data-ttu-id="48c38-138">No se debe llamar al método OLE **IStorage::Commit** cuando el cliente o el proveedor llama [a SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="48c38-138">The OLE method **IStorage::Commit** is not to be called when the client or provider calls [SaveChanges](imapiprop-savechanges.md).</span></span> 
    
<span data-ttu-id="48c38-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="48c38-139">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="48c38-140">Permite la creación de archivos .msg Unicode.</span><span class="sxs-lookup"><span data-stu-id="48c38-140">Enables creation of Unicode .msg files.</span></span> <span data-ttu-id="48c38-141">El archivo [IMessage](imessageimapiprop.md) resultante muestra STORE_UNICODE_OK en [su PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) admite propiedades Unicode.</span><span class="sxs-lookup"><span data-stu-id="48c38-141">The resulting [IMessage](imessageimapiprop.md) file shows STORE_UNICODE_OK in its [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) and supports Unicode properties.</span></span> 
    
  > [!NOTE]
  > <span data-ttu-id="48c38-142">La MAPI_UNICODE solo se admite en esta función en Outlook 2003 o versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="48c38-142">The MAPI_UNICODE flag is only supported in this function on Outlook 2003 or higher.</span></span> 
  
<span data-ttu-id="48c38-143">_lppMsg_</span><span class="sxs-lookup"><span data-stu-id="48c38-143">_lppMsg_</span></span>
  
> <span data-ttu-id="48c38-144">[salida] Puntero a un puntero al objeto **IMessage** abierto.</span><span class="sxs-lookup"><span data-stu-id="48c38-144">[out] Pointer to a pointer to the opened **IMessage** object.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="48c38-145">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="48c38-145">Return value</span></span>

<span data-ttu-id="48c38-146">S_OK</span><span class="sxs-lookup"><span data-stu-id="48c38-146">S_OK</span></span> 
  
> <span data-ttu-id="48c38-147">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="48c38-147">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="48c38-148">Comentarios</span><span class="sxs-lookup"><span data-stu-id="48c38-148">Remarks</span></span>

<span data-ttu-id="48c38-149">Sólo se puede tener acceso a los atributos de propiedad en objetos de propiedad, es decir, objetos que implementan la [interfaz IMAPIProp : IUnknown.](imapipropiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="48c38-149">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="48c38-150">Para que las propiedades MAPI estén disponibles en un objeto de almacenamiento estructurado OLE, **OpenIMsgOnIStg** genera un [objeto IMessage : IMAPIProp](imessageimapiprop.md) sobre el objeto OLE **IStorage.**</span><span class="sxs-lookup"><span data-stu-id="48c38-150">To make MAPI properties available on an OLE structured storage object, **OpenIMsgOnIStg** builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="48c38-151">Los atributos de propiedad de estos objetos se pueden establecer o modificar [con SetAttribIMsgOnIStg](setattribimsgonistg.md) y recuperarse con [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span><span class="sxs-lookup"><span data-stu-id="48c38-151">The property attributes on such objects can be set or altered with [SetAttribIMsgOnIStg](setattribimsgonistg.md) and retrieved with [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="48c38-152">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="48c38-152">Notes to callers</span></span>

<span data-ttu-id="48c38-153">Se debe abrir una sesión de mensaje con [OpenIMsgSession antes](openimsgsession.md) de llamar a **OpenIMsgOnIStg.**</span><span class="sxs-lookup"><span data-stu-id="48c38-153">A message session should be opened with [OpenIMsgSession](openimsgsession.md) before **OpenIMsgOnIStg** is called.</span></span> <span data-ttu-id="48c38-154">Al proporcionar un parámetro  _lpMsgSess_ válido, se asegura de que el nuevo mensaje se crea dentro de una sesión de mensaje para que se cierre cuando se cierre la sesión.</span><span class="sxs-lookup"><span data-stu-id="48c38-154">Supplying a valid  _lpMsgSess_ parameter make sures that the new message is created within a message session so that it is closed when the session is closed.</span></span> <span data-ttu-id="48c38-155">Si  _lpMsgSess_ es NULL, el mensaje se crea independientemente de cualquier sesión de mensaje.</span><span class="sxs-lookup"><span data-stu-id="48c38-155">If  _lpMsgSess_ is NULL, the message is created independently of any message session.</span></span> <span data-ttu-id="48c38-156">Si la aplicación cliente o el proveedor de servicios que creó el mensaje no lo libera, así como todos sus datos adjuntos y tablas abiertas, la memoria se pierde y puede hacer que la aplicación finalice.</span><span class="sxs-lookup"><span data-stu-id="48c38-156">If the client application or service provider that created the message does not release it, as well as all its attachments and open tables, memory is leaked and may cause the application to terminate.</span></span> 
  
<span data-ttu-id="48c38-157">MAPI usa las funciones a las que  _apuntan lpAllocateBuffer_,  _lpAllocateMore_ y  _lpFreeBuffer_ para la mayor parte de la asignación y desasignación de memoria, en particular para asignar memoria para que la usen las aplicaciones cliente al llamar a interfaces de objetos como [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="48c38-157">MAPI uses the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="48c38-158">Los punteros _lpAllocateBuffer_, _lpAllocateMore_ y _lpFreeBuffer_ son opcionales cuando se llama a la función **OpenIMsgOnIStg** con un parámetro _lpMapiSup válido._</span><span class="sxs-lookup"><span data-stu-id="48c38-158">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ pointers are optional when the **OpenIMsgOnIStg** function is called with a valid  _lpMapiSup_ parameter.</span></span> 
  
<span data-ttu-id="48c38-159">Dado que se trata de un objeto OLE subyacente, MAPI también necesita usar la asignación de memoria OLE.</span><span class="sxs-lookup"><span data-stu-id="48c38-159">Because it is dealing with an underlying OLE object, MAPI also needs to use OLE memory allocation.</span></span> <span data-ttu-id="48c38-160">Para obtener más información acerca de los objetos de almacenamiento estructurado OLE y la asignación de memoria OLE, vea la  _referencia del programador de OLE_.</span><span class="sxs-lookup"><span data-stu-id="48c38-160">For more information about OLE structured storage objects and OLE memory allocation, see the  _OLE Programmer's Reference_.</span></span> 
  
<span data-ttu-id="48c38-161">Si se proporciona un valor válido para _lpMapiSup_, **IMessage** admite las marcas MAPI_DIALOG y ATTACH_DIALOG llamando al método [IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md) para proporcionar una interfaz de usuario de progreso para los métodos [IMAPIProp::CopyTo](imapiprop-copyto.md) e [IMessage::D eleteAttach.](imessage-deleteattach.md)</span><span class="sxs-lookup"><span data-stu-id="48c38-161">If a valid value is supplied for  _lpMapiSup_, **IMessage** supports the MAPI_DIALOG and ATTACH_DIALOG flags by calling the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to supply a progress user interface for the [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMessage::DeleteAttach](imessage-deleteattach.md) methods.</span></span> <span data-ttu-id="48c38-162">Además, el método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) intenta convertir identificadores de entrada a corto plazo en identificadores de entrada a largo plazo llamando al método [IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md) y realizando llamadas en el objeto de libreta de direcciones resultante.</span><span class="sxs-lookup"><span data-stu-id="48c38-162">Also, the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method attempts to convert short-term entry identifiers to long-term entry identifiers by calling the [IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md) method and making calls on the resulting address book object.</span></span> <span data-ttu-id="48c38-163">Si se pasa NULL para  _lpMapiSup_, **IMessage** omite MAPI_DIALOG y ATTACH_DIALOG y almacena identificadores de entrada a corto plazo sin conversión.</span><span class="sxs-lookup"><span data-stu-id="48c38-163">If NULL is passed for  _lpMapiSup_, **IMessage** ignores MAPI_DIALOG and ATTACH_DIALOG and stores short-term entry identifiers without conversion.</span></span> 
  
<span data-ttu-id="48c38-164">El **objeto IStorage** al que apunta el parámetro  _lpStg_ debe abrirse en el STGM_READ o STGM_READWRITE búsqueda.</span><span class="sxs-lookup"><span data-stu-id="48c38-164">The **IStorage** object pointed to by the  _lpStg_ parameter must be opened in either the STGM_READ or STGM_READWRITE mode.</span></span> <span data-ttu-id="48c38-165">Si se STGM_READWRITE el modo de STGM_TRANSACTED, también se debe establecer el modo de configuración.</span><span class="sxs-lookup"><span data-stu-id="48c38-165">If the STGM_READWRITE mode is used, the STGM_TRANSACTED mode must also be set.</span></span> 
  
<span data-ttu-id="48c38-166">La función de devolución de llamada a la que apunta _el parámetro lpfMsgCallRelease_ es opcional; si se proporciona, debe basarse en el prototipo de función [MSGCALLRELEASE.](msgcallrelease.md)</span><span class="sxs-lookup"><span data-stu-id="48c38-166">The callback function pointed to by the  _lpfMsgCallRelease_ parameter is optional; if provided, it should be based on the [MSGCALLRELEASE](msgcallrelease.md) function prototype.</span></span> <span data-ttu-id="48c38-167">La **interfaz IMessage** lo llama cuando el recuento de referencias del objeto **IMessage**-on- **IStorage** se establece en cero en la última llamada a su **método Release.**</span><span class="sxs-lookup"><span data-stu-id="48c38-167">The **IMessage** interface calls it when the reference count of the **IMessage**-on- **IStorage** object is set to zero by the last call to its **Release** method.</span></span> <span data-ttu-id="48c38-168">La función de devolución de llamada se usa normalmente para liberar la interfaz **subyacente IStorage.**</span><span class="sxs-lookup"><span data-stu-id="48c38-168">The callback function is commonly used to free the underlying **IStorage** interface.</span></span> <span data-ttu-id="48c38-169">**IMessage** no intentará obtener acceso al **objeto IStorage** al que apunta el parámetro  _lpStg_ después de realizar la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="48c38-169">**IMessage** will not attempt to access the **IStorage** object pointed to by the  _lpStg_ parameter after making the callback.</span></span> 
  
<span data-ttu-id="48c38-170">Algunos clientes o proveedores pueden escribir datos adicionales en el objeto **IStorage** más allá de lo que escribe el propio **IMessage** cuando se llama a su [método SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="48c38-170">Some clients or providers might write additional data to the **IStorage** object beyond what **IMessage** itself writes when its [SaveChanges](imapiprop-savechanges.md) method is called.</span></span> <span data-ttu-id="48c38-171">El cliente o proveedor puede usar la marca IMSG_NO_ISTG_COMMIT para evitar **que IMessage** llame al método OLE **IStorage::Commit** mientras se procesa una **llamada SaveChanges;** en este caso, el cliente o el proveedor debe confirmar el objeto **IStorage** cuando se escriben los datos adicionales.</span><span class="sxs-lookup"><span data-stu-id="48c38-171">The client or provider can use the IMSG_NO_ISTG_COMMIT flag to prevent **IMessage** from calling the OLE **IStorage::Commit** method while processing a **SaveChanges** call; in this case the client or provider must itself commit the **IStorage** object when the additional data is written.</span></span> <span data-ttu-id="48c38-172">Para ayudar en esto, la implementación de **IMessage** garantiza el nombre de todos los substorages que crea en el objeto **IStorage** a partir de la cadena "__", es decir, con dos caracteres de subrayado.</span><span class="sxs-lookup"><span data-stu-id="48c38-172">To aid in this, the **IMessage** implementation guarantees to name all substorages it creates in the **IStorage** object starting with the string "__", that is, with two underscores.</span></span> <span data-ttu-id="48c38-173">El cliente o el proveedor puede evitar conflictos de nombres manteniendo sus nombres de subesmacenamiento fuera de este espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="48c38-173">The client or provider can avoid name collisions by keeping its substorage names out of this namespace.</span></span> 
  
<span data-ttu-id="48c38-174">MAPI no define el comportamiento de varias operaciones abiertas realizadas en un subobjeto de un mensaje, como datos adjuntos, una secuencia o un mensaje incrustado.</span><span class="sxs-lookup"><span data-stu-id="48c38-174">MAPI does not define the behavior of multiple open operations performed on a subobject of a message, such as an attachment, a stream, or an embedded message.</span></span> <span data-ttu-id="48c38-175">MAPI actualmente permite que un subobjeto que ya está abierto se abra una vez más, pero MAPI realiza la operación de apertura incrementando el recuento de referencias para el objeto abierto existente y devolviendolo al cliente o proveedor que llamó al método [IMessage::OpenAttach](imessage-openattach.md) o [IMAPIProp::OpenProperty.](imapiprop-openproperty.md)</span><span class="sxs-lookup"><span data-stu-id="48c38-175">MAPI currently allows a subobject that is already open to be opened once more, but MAPI performs the open operation by incrementing the reference count for the existing open object and returning it to the client or provider that called the [IMessage::OpenAttach](imessage-openattach.md) or [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span></span> <span data-ttu-id="48c38-176">Esto significa que el acceso solicitado para la primera operación de apertura en un subobjeto es el acceso proporcionado para todas las operaciones de apertura posteriores, independientemente del acceso solicitado por las operaciones.</span><span class="sxs-lookup"><span data-stu-id="48c38-176">This means the access requested for the first open operation on a subobject is the access provided for all subsequent open operations, regardless of the access requested by the operations.</span></span> 
  
<span data-ttu-id="48c38-177">El procedimiento correcto para colocar un mensaje en un archivo adjunto es llamar al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) con un identificador de interfaz de IID_IMessage.</span><span class="sxs-lookup"><span data-stu-id="48c38-177">The correct procedure for placing a message into an attachment is to call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with an interface identifier of IID_IMessage.</span></span> <span data-ttu-id="48c38-178">**OpenProperty** actualmente también admite la creación de datos adjuntos de mensajes disponibles directamente en la interfaz OLE **IStorage,** es decir, mediante el uso del identificador IID_IStorage interfaz.</span><span class="sxs-lookup"><span data-stu-id="48c38-178">**OpenProperty** currently also supports creation of message attachments available directly on the OLE **IStorage** interface, that is, using the IID_IStorage interface identifier.</span></span> <span data-ttu-id="48c38-179">**El acceso** a IStorage es compatible para permitir una forma sencilla de colocar un documento de Microsoft Word en datos adjuntos sin convertirlo a o desde la interfaz **OLE IStream.**</span><span class="sxs-lookup"><span data-stu-id="48c38-179">**IStorage** access is supported to allow an easy way to put a Microsoft Word document into an attachment without converting it to or from the OLE **IStream** interface.</span></span> <span data-ttu-id="48c38-180">Sin embargo, es posible que **IMessage** no se comporte de forma predecible si **se** pasa un puntero **IStorage** a los datos adjuntos y, a continuación, los objetos se liberan en el orden incorrecto.</span><span class="sxs-lookup"><span data-stu-id="48c38-180">However, **IMessage** may not behave predictably if **OpenIMsgOnIStg** is passed an **IStorage** pointer to the attachment data and then the objects are released in the wrong order.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="48c38-181">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="48c38-181">MFCMAPI reference</span></span>

<span data-ttu-id="48c38-182">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="48c38-182">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="48c38-183">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="48c38-183">**File**</span></span>|<span data-ttu-id="48c38-184">**Función**</span><span class="sxs-lookup"><span data-stu-id="48c38-184">**Function**</span></span>|<span data-ttu-id="48c38-185">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="48c38-185">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="48c38-186">File.cpp</span><span class="sxs-lookup"><span data-stu-id="48c38-186">File.cpp</span></span>  <br/> |<span data-ttu-id="48c38-187">LoadMSGToMessage</span><span class="sxs-lookup"><span data-stu-id="48c38-187">LoadMSGToMessage</span></span>  <br/> |<span data-ttu-id="48c38-188">MFCMAPI usa el **método OpenIMsgOnIStg** para abrir una interfaz IMessage encima de . MSG para que el archivo se pueda manipular con MAPI.</span><span class="sxs-lookup"><span data-stu-id="48c38-188">MFCMAPI uses the **OpenIMsgOnIStg** method to open an IMessage interface on top of the .MSG file so that the file may be manipulated with MAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="48c38-189">Consulte también</span><span class="sxs-lookup"><span data-stu-id="48c38-189">See also</span></span>

- [<span data-ttu-id="48c38-190">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="48c38-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

