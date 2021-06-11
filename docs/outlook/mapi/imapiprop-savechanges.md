---
title: IMAPIPropSaveChanges
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.SaveChanges
api_type:
- COM
ms.assetid: 864dbc3e-2039-435a-a279-385d79d1d13f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2c8244180a5cafedc887fa72f36f233fb5084f79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316635"
---
# <a name="imapipropsavechanges"></a><span data-ttu-id="288b3-103">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="288b3-103">IMAPIProp::SaveChanges</span></span>

  
  
<span data-ttu-id="288b3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="288b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="288b3-105">Realiza de forma permanente los cambios realizados en un objeto desde la última operación de guardado.</span><span class="sxs-lookup"><span data-stu-id="288b3-105">Makes permanent any changes that were made to an object since the last save operation.</span></span> 
  
```cpp
HRESULT SaveChanges(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="288b3-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="288b3-106">Parameters</span></span>

 <span data-ttu-id="288b3-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="288b3-107">_ulFlags_</span></span>
  
> <span data-ttu-id="288b3-108">[in] Máscara de bits de marcas que controla lo que sucede con el objeto cuando se llama al método **IMAPIProp::SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="288b3-108">[in] A bitmask of flags that controls what happens to the object when the **IMAPIProp::SaveChanges** method is called.</span></span> <span data-ttu-id="288b3-109">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="288b3-109">The following flags can be set:</span></span> 
    
<span data-ttu-id="288b3-110">NON_EMS_XP_SAVE</span><span class="sxs-lookup"><span data-stu-id="288b3-110">NON_EMS_XP_SAVE</span></span>
  
> <span data-ttu-id="288b3-111">Indica que el mensaje no se ha entregado desde un Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="288b3-111">Indicates that the message has not been delivered from a Microsoft Exchange Server.</span></span> <span data-ttu-id="288b3-112">Esta marca debe usarse en combinación con el método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) y la marca ITEMPROC_FORCE para indicar a un almacén PST que el mensaje es apto para el procesamiento de reglas antes de que el almacén de archivos de carpetas personales (PST) notije a cualquier cliente de escucha que el mensaje ha llegado.</span><span class="sxs-lookup"><span data-stu-id="288b3-112">This flag should be used in combination with the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method and the ITEMPROC_FORCE flag to indicate to a PST store that the message is eligible for rules processing before the Personal Folders file (PST) store notifies any listening client that the message has arrived.</span></span> <span data-ttu-id="288b3-113">Este procesamiento de reglas solo se aplica a los nuevos mensajes que se crean con [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) en un servidor que no es un Exchange Server, en cuyo caso el Exchange Server ya habría procesado reglas en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="288b3-113">This rules processing only applies to new messages that are created with [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) on a server that is not an Exchange Server, in which case the Exchange Server would have already processed rules on the message.</span></span> 
    
<span data-ttu-id="288b3-114">FORCE_SAVE</span><span class="sxs-lookup"><span data-stu-id="288b3-114">FORCE_SAVE</span></span> 
  
> <span data-ttu-id="288b3-115">Los cambios deben escribirse en el objeto, reemplazando los cambios anteriores realizados en el objeto y el objeto debe cerrarse.</span><span class="sxs-lookup"><span data-stu-id="288b3-115">Changes should be written to the object, overriding any previous changes that were made to the object, and the object should be closed.</span></span> <span data-ttu-id="288b3-116">Se debe establecer el permiso de lectura y escritura para que la operación se pueda realizar correctamente.</span><span class="sxs-lookup"><span data-stu-id="288b3-116">Read/write permission must be set for the operation to succeed.</span></span> <span data-ttu-id="288b3-117">La FORCE_SAVE se usa después de que una llamada anterior a **SaveChanges** devolvía MAPI_E_OBJECT_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="288b3-117">The FORCE_SAVE flag is used after a previous call to **SaveChanges** returned MAPI_E_OBJECT_CHANGED.</span></span> 
    
<span data-ttu-id="288b3-118">KEEP_OPEN_READONLY</span><span class="sxs-lookup"><span data-stu-id="288b3-118">KEEP_OPEN_READONLY</span></span> 
  
> <span data-ttu-id="288b3-119">Los cambios deben ser confirmados y el objeto debe mantenerse abierto para su lectura.</span><span class="sxs-lookup"><span data-stu-id="288b3-119">Changes should be committed and the object should be kept open for reading.</span></span> <span data-ttu-id="288b3-120">No se realizarán cambios adicionales.</span><span class="sxs-lookup"><span data-stu-id="288b3-120">No additional changes will be made.</span></span> 
    
<span data-ttu-id="288b3-121">KEEP_OPEN_READWRITE</span><span class="sxs-lookup"><span data-stu-id="288b3-121">KEEP_OPEN_READWRITE</span></span> 
  
> <span data-ttu-id="288b3-122">Los cambios deben ser confirmados y el objeto debe mantenerse abierto para el permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="288b3-122">Changes should be committed and the object should be kept open for read/write permission.</span></span> <span data-ttu-id="288b3-123">Esta marca suele establecerse cuando el objeto se abrió por primera vez para el permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="288b3-123">This flag is usually set when the object was first opened for read/write permission.</span></span> <span data-ttu-id="288b3-124">Se permiten los cambios posteriores en el objeto.</span><span class="sxs-lookup"><span data-stu-id="288b3-124">Subsequent changes to the object are allowed.</span></span> 
    
<span data-ttu-id="288b3-125">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="288b3-125">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="288b3-126">Permite **que SaveChanges** vuelva correctamente, posiblemente antes de que los cambios se hayan confirmado completamente.</span><span class="sxs-lookup"><span data-stu-id="288b3-126">Allows **SaveChanges** to return successfully, possibly before the changes have been fully committed.</span></span> 
    
<span data-ttu-id="288b3-127">SPAMFILTER_ONSAVE</span><span class="sxs-lookup"><span data-stu-id="288b3-127">SPAMFILTER_ONSAVE</span></span>
  
> <span data-ttu-id="288b3-128">Habilita el filtrado de correo no deseado en un mensaje que se está guardando.</span><span class="sxs-lookup"><span data-stu-id="288b3-128">Enables spam filtering on a message that is being saved.</span></span> <span data-ttu-id="288b3-129">El soporte de filtrado de spam solo está disponible si el tipo de dirección de correo electrónico del remitente es Protocolo simple de transferencia de correo (SMTP) y el mensaje se está guardando en un almacén de un archivo de carpetas personales (PST).</span><span class="sxs-lookup"><span data-stu-id="288b3-129">Spam filtering support is available only if the sender's email address type is Simple Mail Transfer Protocol (SMTP), and the message is being saved to a store for a Personal Folders file (PST).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="288b3-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="288b3-130">Return value</span></span>

<span data-ttu-id="288b3-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="288b3-131">S_OK</span></span> 
  
> <span data-ttu-id="288b3-132">El compromiso de los cambios se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="288b3-132">The commitment of changes was successful.</span></span>
    
<span data-ttu-id="288b3-133">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="288b3-133">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="288b3-134">**SaveChanges** no puede mantener el objeto abierto para el permiso de solo lectura si KEEP_OPEN_READONLY está establecido, o permiso de lectura y escritura si KEEP_OPEN_READWRITE está establecido.</span><span class="sxs-lookup"><span data-stu-id="288b3-134">**SaveChanges** cannot keep the object open for read-only permission if KEEP_OPEN_READONLY is set, or read/write permission if KEEP_OPEN_READWRITE is set.</span></span> <span data-ttu-id="288b3-135">No se confirma ningún cambio.</span><span class="sxs-lookup"><span data-stu-id="288b3-135">No changes are committed.</span></span> 
    
<span data-ttu-id="288b3-136">MAPI_E_OBJECT_CHANGED</span><span class="sxs-lookup"><span data-stu-id="288b3-136">MAPI_E_OBJECT_CHANGED</span></span> 
  
> <span data-ttu-id="288b3-137">El objeto ha cambiado desde que se abrió.</span><span class="sxs-lookup"><span data-stu-id="288b3-137">The object has changed since it was opened.</span></span>
    
<span data-ttu-id="288b3-138">MAPI_E_OBJECT_DELETED</span><span class="sxs-lookup"><span data-stu-id="288b3-138">MAPI_E_OBJECT_DELETED</span></span> 
  
> <span data-ttu-id="288b3-139">El objeto se ha eliminado desde que se abrió.</span><span class="sxs-lookup"><span data-stu-id="288b3-139">The object has been deleted since it was opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="288b3-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="288b3-140">Remarks</span></span>

<span data-ttu-id="288b3-141">El **método IMAPIProp::SaveChanges** hace que los cambios de propiedad sea permanente para los objetos que admiten el modelo de transacciones de procesamiento, como mensajes, datos adjuntos, contenedores de libreta de direcciones y objetos de usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="288b3-141">The **IMAPIProp::SaveChanges** method makes property changes permanent for objects that support the transaction model of processing, such as messages, attachments, address book containers, and messaging user objects.</span></span> <span data-ttu-id="288b3-142">Los objetos que no admiten transacciones, como carpetas, almacenes de mensajes y secciones de perfil, hacen cambios permanentes inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="288b3-142">Objects that do not support transactions, such as folders, message stores, and profile sections, make changes permanent immediately.</span></span> <span data-ttu-id="288b3-143">No se requiere **ninguna llamada a SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="288b3-143">No call to **SaveChanges** is required.</span></span> 
  
<span data-ttu-id="288b3-144">Dado que los proveedores de servicios no tienen que generar un identificador de entrada para sus objetos hasta que se hayan guardado todas las propiedades, es posible que la propiedad **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) de un objeto no esté disponible hasta después de llamar a su **método SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="288b3-144">Because service providers do not have to generate an entry identifier for their objects until all properties have been saved, an object's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property might not be available until after its **SaveChanges** method has been called.</span></span> <span data-ttu-id="288b3-145">Algunos proveedores esperan hasta que se KEEP_OPEN_READONLY marca en la **llamada SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="288b3-145">Some providers wait until the KEEP_OPEN_READONLY flag is set on the **SaveChanges** call.</span></span> <span data-ttu-id="288b3-146">KEEP_OPEN_READONLY indica que los cambios que se guardarán en la llamada actual serán los últimos cambios que se realizarán en el objeto.</span><span class="sxs-lookup"><span data-stu-id="288b3-146">KEEP_OPEN_READONLY indicates that the changes to be saved in the current call will be the last changes that will be made on the object.</span></span> 
  
<span data-ttu-id="288b3-147">Algunas implementaciones de almacén de mensajes no muestran mensajes recién creados en una carpeta hasta que un cliente guarda los cambios de mensaje mediante **SaveChanges** y libera los objetos de mensaje mediante el método [IUnknown::Release.](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="288b3-147">Some message store implementations do not show newly created messages in a folder until a client saves the message changes by using **SaveChanges** and releases the message objects by using the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="288b3-148">Además, algunas implementaciones de objetos no pueden generar una propiedad **PR_ENTRYID** para un objeto recién creado hasta después de llamar a **SaveChanges** y otras solo pueden hacerlo después de llamar a **SaveChanges** mediante KEEP_OPEN_READONLY establecido en  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="288b3-148">In addition, some object implementations cannot generate a **PR_ENTRYID** property for a newly created object until after **SaveChanges** has been called, and some can do so only after **SaveChanges** has been called by using KEEP_OPEN_READONLY set in  _ulFlags_.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="288b3-149">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="288b3-149">Notes to implementers</span></span>

<span data-ttu-id="288b3-150">Si recibe la marca KEEP_OPEN_READONLY, tiene la opción de dejar el acceso del objeto como lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="288b3-150">If you receive the KEEP_OPEN_READONLY flag, you have the option of leaving the object's access as read/write.</span></span> <span data-ttu-id="288b3-151">Sin embargo, un proveedor nunca puede dejar un objeto en un estado de solo lectura cuando se pasa KEEP_OPEN_READWRITE marca.</span><span class="sxs-lookup"><span data-stu-id="288b3-151">However, a provider can never leave an object in a read-only state when the KEEP_OPEN_READWRITE flag is passed.</span></span>
  
<span data-ttu-id="288b3-152">Cuando un cliente guarda varios datos adjuntos en varios mensajes, llama al **método SaveChanges** para cada dato adjunto y cada mensaje.</span><span class="sxs-lookup"><span data-stu-id="288b3-152">When a client saves multiple attachments to multiple messages, it calls the **SaveChanges** method for every attachment and every message.</span></span> <span data-ttu-id="288b3-153">A menudo, los clientes MAPI_DEFERRED_ERRORS para cada una de estas llamadas excepto para la última.</span><span class="sxs-lookup"><span data-stu-id="288b3-153">Often clients will set MAPI_DEFERRED_ERRORS for each of these calls except for the last one.</span></span> <span data-ttu-id="288b3-154">Puede devolver errores con la última llamada o con llamadas anteriores.</span><span class="sxs-lookup"><span data-stu-id="288b3-154">You can return errors either with the last call or earlier calls.</span></span> <span data-ttu-id="288b3-155">Incluso puede omitir la marca.</span><span class="sxs-lookup"><span data-stu-id="288b3-155">You can even ignore the flag.</span></span> 
  
<span data-ttu-id="288b3-156">Si KEEP_OPEN_READWRITE o KEEP_OPEN_READONLY se establece junto con MAPI_DEFERRED_ERRORS, puede omitir la solicitud de aplazamiento de error.</span><span class="sxs-lookup"><span data-stu-id="288b3-156">If either KEEP_OPEN_READWRITE or KEEP_OPEN_READONLY is set together with MAPI_DEFERRED_ERRORS, you can ignore the error deferment request.</span></span> <span data-ttu-id="288b3-157">Si MAPI_DEFERRED_ERRORS está establecido en _ulFlags_, se puede devolver uno de los errores diferidos anteriormente para la **llamada SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="288b3-157">If MAPI_DEFERRED_ERRORS is not set in  _ulFlags_, one of the previously deferred errors can be returned for the **SaveChanges** call.</span></span> 
  
<span data-ttu-id="288b3-158">Si un proveedor de transporte remoto proporciona una implementación funcional de este método es opcional y depende de otras opciones de diseño en la implementación.</span><span class="sxs-lookup"><span data-stu-id="288b3-158">Whether a remote transport provider provides a functional implementation of this method is optional and depends on other design choices in your implementation.</span></span> <span data-ttu-id="288b3-159">Si implementa este método, hacerlo de acuerdo con la documentación aquí.</span><span class="sxs-lookup"><span data-stu-id="288b3-159">If you implement this method, do so according to the documentation here.</span></span> <span data-ttu-id="288b3-160">Dado que los objetos de carpeta y los objetos de estado no se realizan transacciones, como mínimo, la implementación de **SaveChanges** por parte de un proveedor de transporte remoto debe devolver S_OK sin realizar ningún trabajo.</span><span class="sxs-lookup"><span data-stu-id="288b3-160">Because folder objects and status objects are not transacted, at a minimum a remote transport provider's implementation of **SaveChanges** must return S_OK without actually doing any work.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="288b3-161">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="288b3-161">Notes to callers</span></span>

<span data-ttu-id="288b3-162">Si un cliente pasa KEEP_OPEN_READONLY, llama al método [IMAPIProp::SetProps](imapiprop-setprops.md) y, a continuación, vuelve a llamar a **SaveChanges,** puede producirse un error en la misma implementación.</span><span class="sxs-lookup"><span data-stu-id="288b3-162">If a client passes KEEP_OPEN_READONLY, calls the [IMAPIProp::SetProps](imapiprop-setprops.md) method, and then calls **SaveChanges** again, the same implementation might fail.</span></span> 
  
<span data-ttu-id="288b3-163">Después de recibir MAPI_E_NO_ACCESS de una llamada en la que KEEP_OPEN_READWRITE, seguirá teniendo permiso de lectura y escritura en el objeto.</span><span class="sxs-lookup"><span data-stu-id="288b3-163">After receiving MAPI_E_NO_ACCESS from a call in which you set KEEP_OPEN_READWRITE, you will continue to have read/write permission to the object.</span></span> <span data-ttu-id="288b3-164">Puede volver a **llamar a SaveChanges,** pasando la marca KEEP_OPEN_READONLY o ninguna marca con KEEP_OPEN_SUFFIX.</span><span class="sxs-lookup"><span data-stu-id="288b3-164">You can call **SaveChanges** again, passing either the KEEP_OPEN_READONLY flag or no flags with KEEP_OPEN_SUFFIX.</span></span> 
  
<span data-ttu-id="288b3-165">Si un proveedor admite la marca KEEP_OPEN_READWRITE depende de la implementación del proveedor.</span><span class="sxs-lookup"><span data-stu-id="288b3-165">Whether a provider supports the KEEP_OPEN_READWRITE flag depends on the provider's implementation.</span></span> 
  
<span data-ttu-id="288b3-166">Para indicar que la única llamada que se realiza en el objeto después de **SaveChanges** es **IUnknown::Release**, no establezca ninguna marca para el _parámetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="288b3-166">To indicate that the only call to be made on the object after **SaveChanges** is **IUnknown::Release**, set no flags for the  _ulFlags_ parameter.</span></span> <span data-ttu-id="288b3-167">Un error de **SaveChanges** indica que no se pudieron hacer los cambios pendientes permanentes.</span><span class="sxs-lookup"><span data-stu-id="288b3-167">An error from **SaveChanges** indicates that it could not make the pending changes permanent.</span></span> <span data-ttu-id="288b3-168">Diferentes proveedores controlan la ausencia de marcas en la **llamada SaveChanges** de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="288b3-168">Different providers handle the absence of flags on the **SaveChanges** call differently.</span></span> <span data-ttu-id="288b3-169">Algunos proveedores tratan este estado del mismo modo que KEEP_OPEN_READONLY; otros proveedores lo interpretan igual que KEEP_OPEN_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="288b3-169">Some providers treat this state the same as KEEP_OPEN_READONLY; other providers interpret it the same as KEEP_OPEN_READWRITE.</span></span> <span data-ttu-id="288b3-170">Aún así, otros proveedores cierran el objeto cuando no reciben marcas en la **llamada SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="288b3-170">Still other providers shut down the object when they do not receive flags on the **SaveChanges** call.</span></span> 
  
<span data-ttu-id="288b3-171">Algunas propiedades, normalmente las propiedades calculadas, no se pueden procesar hasta que se llama a **SaveChanges** y, en algunos casos, **a Release**.</span><span class="sxs-lookup"><span data-stu-id="288b3-171">Some properties, typically computed properties, cannot be processed until you call **SaveChanges** and, in some cases, **Release**.</span></span>
  
<span data-ttu-id="288b3-172">Al realizar cambios masivos, como guardar datos adjuntos en varios mensajes, aplazar el procesamiento de errores estableciendo la marca MAPI_DEFERRED_ERRORS en  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="288b3-172">When you make bulk changes, such as saving attachments to multiple messages, defer error processing by setting the MAPI_DEFERRED_ERRORS flag in  _ulFlags_.</span></span> <span data-ttu-id="288b3-173">Si guarda varios datos adjuntos en varios mensajes, realice una llamada **a SaveChanges** a cada dato adjunto y una llamada **a SaveChanges** a cada mensaje.</span><span class="sxs-lookup"><span data-stu-id="288b3-173">If you save multiple attachments to multiple messages, make one **SaveChanges** call to each attachment and one **SaveChanges** call to each message.</span></span> <span data-ttu-id="288b3-174">Establezca la MAPI_DEFERRED_ERRORS para cada llamada de datos adjuntos y para todos los mensajes excepto para la última.</span><span class="sxs-lookup"><span data-stu-id="288b3-174">Set the MAPI_DEFERRED_ERRORS flag for each attachment call and for all messages except for the last one.</span></span> 
  
<span data-ttu-id="288b3-175">Si **SaveChanges** devuelve MAPI_E_OBJECT_CHANGED, compruebe si el objeto original se ha modificado.</span><span class="sxs-lookup"><span data-stu-id="288b3-175">If **SaveChanges** returns MAPI_E_OBJECT_CHANGED, check whether the original object has been modified.</span></span> <span data-ttu-id="288b3-176">Si es así, advierte al usuario, que puede solicitar que los cambios sobrescriban los cambios anteriores o guarde el objeto en otro lugar.</span><span class="sxs-lookup"><span data-stu-id="288b3-176">If so, warn the user, who can either request that the changes overwrite the previous changes or save the object elsewhere.</span></span> <span data-ttu-id="288b3-177">Si el objeto original se ha eliminado, advierte al usuario que le dé la oportunidad de guardar el objeto en otra ubicación.</span><span class="sxs-lookup"><span data-stu-id="288b3-177">If the original object has been deleted, warn the user to give them the opportunity to save the object in another location.</span></span> 
  
<span data-ttu-id="288b3-178">No puede llamar a **SaveChanges** con la FORCE_SAVE en un objeto abierto que se ha eliminado.</span><span class="sxs-lookup"><span data-stu-id="288b3-178">You cannot call **SaveChanges** with the FORCE_SAVE flag on an open object that has been deleted.</span></span> 
  
<span data-ttu-id="288b3-179">Si **SaveChanges** devuelve un error, el objeto cuyos cambios se iban a guardar permanece abierto, independientemente de las marcas establecidas en el _parámetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="288b3-179">If **SaveChanges** returns an error, the object whose changes were to be saved remains open, regardless of the flags set in the  _ulFlags_ parameter.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="288b3-180">Es posible que NON_EMS_XP_SAVE y SPAMFILTER_ONSAVE  _ulFlags_ no se definan en el archivo de encabezado descargable que tiene actualmente, en cuyo caso puede agregarlo al código con los siguientes valores: >  `#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`</span><span class="sxs-lookup"><span data-stu-id="288b3-180">The  _ulFlags_ NON_EMS_XP_SAVE and SPAMFILTER_ONSAVE might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following values: >  `#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`</span></span>
  
<span data-ttu-id="288b3-181">Para obtener más información, vea [Saving MAPI Properties](saving-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="288b3-181">For more information, see [Saving MAPI Properties](saving-mapi-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="288b3-182">Vea también</span><span class="sxs-lookup"><span data-stu-id="288b3-182">See also</span></span>



[<span data-ttu-id="288b3-183">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="288b3-183">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="288b3-184">Propiedad canónica PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="288b3-184">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="288b3-185">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="288b3-185">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="288b3-186">Guardar propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="288b3-186">Saving MAPI Properties</span></span>](saving-mapi-properties.md)

