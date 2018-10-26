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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398846"
---
# <a name="imapipropsavechanges"></a><span data-ttu-id="5234f-103">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="5234f-103">IMAPIProp::SaveChanges</span></span>

  
  
<span data-ttu-id="5234f-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5234f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5234f-105">Hace permanentes los cambios realizados a un objeto desde la última operación de guardar.</span><span class="sxs-lookup"><span data-stu-id="5234f-105">Makes permanent any changes that were made to an object since the last save operation.</span></span> 
  
```cpp
HRESULT SaveChanges(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="5234f-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="5234f-106">Parameters</span></span>

 <span data-ttu-id="5234f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5234f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="5234f-108">[entrada] Una máscara de bits de indicadores que controla lo que ocurre con el objeto cuando se llama al método **IMAPIProp::SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="5234f-108">[in] A bitmask of flags that controls what happens to the object when the **IMAPIProp::SaveChanges** method is called.</span></span> <span data-ttu-id="5234f-109">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="5234f-109">The following flags can be set:</span></span> 
    
<span data-ttu-id="5234f-110">NON_EMS_XP_SAVE</span><span class="sxs-lookup"><span data-stu-id="5234f-110">NON_EMS_XP_SAVE</span></span>
  
> <span data-ttu-id="5234f-111">Indica que no se ha entregado el mensaje de un servidor de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="5234f-111">Indicates that the message has not been delivered from a Microsoft Exchange Server.</span></span> <span data-ttu-id="5234f-112">Este indicador se debe usar en combinación con el método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) y la marca ITEMPROC_FORCE para indicar a un almacén de archivos PST que el mensaje tiene derecho para reglas de procesamiento antes de que el almacén de carpetas personales (PST) de archivo se lo comunica cualquiera cliente de escucha que ha llegado el mensaje.</span><span class="sxs-lookup"><span data-stu-id="5234f-112">This flag should be used in combination with the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method and the ITEMPROC_FORCE flag to indicate to a PST store that the message is eligible for rules processing before the Personal Folders file (PST) store notifies any listening client that the message has arrived.</span></span> <span data-ttu-id="5234f-113">Esta reglas de procesamiento sólo se aplica a los nuevos mensajes que se crean con [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) en un servidor que no es un servidor de Exchange, en cuyo caso el servidor de Exchange ya habría procesado reglas en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="5234f-113">This rules processing only applies to new messages that are created with [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) on a server that is not an Exchange Server, in which case the Exchange Server would have already processed rules on the message.</span></span> 
    
<span data-ttu-id="5234f-114">FORCE_SAVE</span><span class="sxs-lookup"><span data-stu-id="5234f-114">FORCE_SAVE</span></span> 
  
> <span data-ttu-id="5234f-115">Los cambios se deben escribirse en el objeto, reemplazar los cambios anteriores que se han realizado en el objeto, y se debe cerrar el objeto.</span><span class="sxs-lookup"><span data-stu-id="5234f-115">Changes should be written to the object, overriding any previous changes that were made to the object, and the object should be closed.</span></span> <span data-ttu-id="5234f-116">Permiso de lectura y escritura se debe establecer para que la operación se realice correctamente.</span><span class="sxs-lookup"><span data-stu-id="5234f-116">Read/write permission must be set for the operation to succeed.</span></span> <span data-ttu-id="5234f-117">El indicador FORCE_SAVE se utiliza después de una llamada anterior a **SaveChanges** devolvió MAPI_E_OBJECT_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="5234f-117">The FORCE_SAVE flag is used after a previous call to **SaveChanges** returned MAPI_E_OBJECT_CHANGED.</span></span> 
    
<span data-ttu-id="5234f-118">KEEP_OPEN_READONLY</span><span class="sxs-lookup"><span data-stu-id="5234f-118">KEEP_OPEN_READONLY</span></span> 
  
> <span data-ttu-id="5234f-119">Se deberían confirmar los cambios y el objeto se debe mantener abierto para lectura.</span><span class="sxs-lookup"><span data-stu-id="5234f-119">Changes should be committed and the object should be kept open for reading.</span></span> <span data-ttu-id="5234f-120">No se realizarán cambios adicionales.</span><span class="sxs-lookup"><span data-stu-id="5234f-120">No additional changes will be made.</span></span> 
    
<span data-ttu-id="5234f-121">KEEP_OPEN_READWRITE</span><span class="sxs-lookup"><span data-stu-id="5234f-121">KEEP_OPEN_READWRITE</span></span> 
  
> <span data-ttu-id="5234f-122">Se deberían confirmar los cambios y el objeto se debe mantener abierto para el permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="5234f-122">Changes should be committed and the object should be kept open for read/write permission.</span></span> <span data-ttu-id="5234f-123">Este indicador normalmente se establece cuando se abre por primera vez el objeto de permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="5234f-123">This flag is usually set when the object was first opened for read/write permission.</span></span> <span data-ttu-id="5234f-124">Se permiten los cambios posteriores en el objeto.</span><span class="sxs-lookup"><span data-stu-id="5234f-124">Subsequent changes to the object are allowed.</span></span> 
    
<span data-ttu-id="5234f-125">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="5234f-125">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="5234f-126">Permite **SaveChanges** devolver de correctamente, posiblemente antes de que los cambios se han guardado por completo.</span><span class="sxs-lookup"><span data-stu-id="5234f-126">Allows **SaveChanges** to return successfully, possibly before the changes have been fully committed.</span></span> 
    
<span data-ttu-id="5234f-127">SPAMFILTER_ONSAVE</span><span class="sxs-lookup"><span data-stu-id="5234f-127">SPAMFILTER_ONSAVE</span></span>
  
> <span data-ttu-id="5234f-128">Permite contra correo no deseado filtrado en un mensaje que se va a guardar.</span><span class="sxs-lookup"><span data-stu-id="5234f-128">Enables spam filtering on a message that is being saved.</span></span> <span data-ttu-id="5234f-129">El soporte de filtrado de spam solo está disponible si el tipo de dirección de correo electrónico del remitente es Protocolo simple de transferencia de correo (SMTP) y el mensaje se está guardando en un almacén de un archivo de carpetas personales (PST).</span><span class="sxs-lookup"><span data-stu-id="5234f-129">Spam filtering support is available only if the sender's email address type is Simple Mail Transfer Protocol (SMTP), and the message is being saved to a store for a Personal Folders file (PST).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5234f-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5234f-130">Return value</span></span>

<span data-ttu-id="5234f-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="5234f-131">S_OK</span></span> 
  
> <span data-ttu-id="5234f-132">El compromiso de cambios fue correcto.</span><span class="sxs-lookup"><span data-stu-id="5234f-132">The commitment of changes was successful.</span></span>
    
<span data-ttu-id="5234f-133">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="5234f-133">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="5234f-134">**SaveChanges** no se puede mantener el objeto abierto para el permiso de sólo lectura si KEEP_OPEN_READONLY está establecido, o el permiso de lectura y escritura si se establece KEEP_OPEN_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="5234f-134">**SaveChanges** cannot keep the object open for read-only permission if KEEP_OPEN_READONLY is set, or read/write permission if KEEP_OPEN_READWRITE is set.</span></span> <span data-ttu-id="5234f-135">No hay cambios se confirman.</span><span class="sxs-lookup"><span data-stu-id="5234f-135">No changes are committed.</span></span> 
    
<span data-ttu-id="5234f-136">MAPI_E_OBJECT_CHANGED</span><span class="sxs-lookup"><span data-stu-id="5234f-136">MAPI_E_OBJECT_CHANGED</span></span> 
  
> <span data-ttu-id="5234f-137">El objeto ha cambiado desde que se abrió.</span><span class="sxs-lookup"><span data-stu-id="5234f-137">The object has changed since it was opened.</span></span>
    
<span data-ttu-id="5234f-138">MAPI_E_OBJECT_DELETED</span><span class="sxs-lookup"><span data-stu-id="5234f-138">MAPI_E_OBJECT_DELETED</span></span> 
  
> <span data-ttu-id="5234f-139">El objeto se ha eliminado desde que se abrió.</span><span class="sxs-lookup"><span data-stu-id="5234f-139">The object has been deleted since it was opened.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5234f-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5234f-140">Remarks</span></span>

<span data-ttu-id="5234f-141">El método **IMAPIProp::SaveChanges** realiza los cambios de propiedad permanente para los objetos que admiten el modelo de transacción de procesamiento, como mensajes, datos adjuntos, contenedores de libretas de direcciones y los objetos de usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="5234f-141">The **IMAPIProp::SaveChanges** method makes property changes permanent for objects that support the transaction model of processing, such as messages, attachments, address book containers, and messaging user objects.</span></span> <span data-ttu-id="5234f-142">Objetos que no admiten transacciones, como las carpetas, los almacenes de mensajes y las secciones de perfil, realice cambios permanentes inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="5234f-142">Objects that do not support transactions, such as folders, message stores, and profile sections, make changes permanent immediately.</span></span> <span data-ttu-id="5234f-143">Ninguna llamada a **SaveChanges** es necesaria.</span><span class="sxs-lookup"><span data-stu-id="5234f-143">No call to **SaveChanges** is required.</span></span> 
  
<span data-ttu-id="5234f-144">Debido a que no es necesario generar un identificador de entrada para sus objetos hasta que se han guardado todas las propiedades de los proveedores de servicios, la propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) de un objeto no esté disponible hasta después de su método **SaveChanges** se ha llamado.</span><span class="sxs-lookup"><span data-stu-id="5234f-144">Because service providers do not have to generate an entry identifier for their objects until all properties have been saved, an object's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property might not be available until after its **SaveChanges** method has been called.</span></span> <span data-ttu-id="5234f-145">Algunos proveedores de esperar hasta que se establezca el indicador KEEP_OPEN_READONLY en la llamada de **SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="5234f-145">Some providers wait until the KEEP_OPEN_READONLY flag is set on the **SaveChanges** call.</span></span> <span data-ttu-id="5234f-146">KEEP_OPEN_READONLY indica que los cambios se guarden en la llamada actual serán los últimos cambios que se realizarán en el objeto.</span><span class="sxs-lookup"><span data-stu-id="5234f-146">KEEP_OPEN_READONLY indicates that the changes to be saved in the current call will be the last changes that will be made on the object.</span></span> 
  
<span data-ttu-id="5234f-147">Algunas implementaciones de almacén de mensajes no mostrar recién creado mensajes hacer en una carpeta hasta que un cliente guarda el mensaje cambia mediante el uso de **SaveChanges** y libera los objetos de mensaje con el método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="5234f-147">Some message store implementations do not show newly created messages in a folder until a client saves the message changes by using **SaveChanges** and releases the message objects by using the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="5234f-148">Además, algunas implementaciones de objeto no pueden generar una propiedad de **entrada del objeto** para un objeto recién creado hasta que después se ha llamado al **SaveChanges** y algunas pueden hacerlo sólo una vez que se ha llamado al **SaveChanges** mediante el uso de KEEP_OPEN_READONLY establecer en _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="5234f-148">In addition, some object implementations cannot generate a **PR_ENTRYID** property for a newly created object until after **SaveChanges** has been called, and some can do so only after **SaveChanges** has been called by using KEEP_OPEN_READONLY set in  _ulFlags_.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="5234f-149">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="5234f-149">Notes to implementers</span></span>

<span data-ttu-id="5234f-150">Si recibe la marca KEEP_OPEN_READONLY, tendrá la opción de salir de access del objeto como de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="5234f-150">If you receive the KEEP_OPEN_READONLY flag, you have the option of leaving the object's access as read/write.</span></span> <span data-ttu-id="5234f-151">Sin embargo, un proveedor de nunca puede dejar un objeto en un estado de sólo lectura cuando se pasa el indicador KEEP_OPEN_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="5234f-151">However, a provider can never leave an object in a read-only state when the KEEP_OPEN_READWRITE flag is passed.</span></span>
  
<span data-ttu-id="5234f-152">Cuando un cliente guarda los datos adjuntos de varios a varios mensajes, se llama al método **SaveChanges** para todos los datos adjuntos y todos los mensajes.</span><span class="sxs-lookup"><span data-stu-id="5234f-152">When a client saves multiple attachments to multiple messages, it calls the **SaveChanges** method for every attachment and every message.</span></span> <span data-ttu-id="5234f-153">A menudo los clientes establecerá MAPI_DEFERRED_ERRORS para cada una de estas llamadas excepto el último.</span><span class="sxs-lookup"><span data-stu-id="5234f-153">Often clients will set MAPI_DEFERRED_ERRORS for each of these calls except for the last one.</span></span> <span data-ttu-id="5234f-154">Puede devolver los errores con la última llamada o llamadas anteriores.</span><span class="sxs-lookup"><span data-stu-id="5234f-154">You can return errors either with the last call or earlier calls.</span></span> <span data-ttu-id="5234f-155">Incluso puede pasar por alto la marca.</span><span class="sxs-lookup"><span data-stu-id="5234f-155">You can even ignore the flag.</span></span> 
  
<span data-ttu-id="5234f-156">Si se establece KEEP_OPEN_READWRITE o KEEP_OPEN_READONLY junto con MAPI_DEFERRED_ERRORS, puede omitir la petición de aplazamiento de error.</span><span class="sxs-lookup"><span data-stu-id="5234f-156">If either KEEP_OPEN_READWRITE or KEEP_OPEN_READONLY is set together with MAPI_DEFERRED_ERRORS, you can ignore the error deferment request.</span></span> <span data-ttu-id="5234f-157">Si MAPI_DEFERRED_ERRORS no está establecido en _ulFlags_, uno de los errores anteriormente diferidos puede devolver para la llamada de **SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="5234f-157">If MAPI_DEFERRED_ERRORS is not set in  _ulFlags_, one of the previously deferred errors can be returned for the **SaveChanges** call.</span></span> 
  
<span data-ttu-id="5234f-158">Si un proveedor de transporte remoto proporciona una implementación funcional de este método es opcional y depende de otras opciones de diseño en su implementación.</span><span class="sxs-lookup"><span data-stu-id="5234f-158">Whether a remote transport provider provides a functional implementation of this method is optional and depends on other design choices in your implementation.</span></span> <span data-ttu-id="5234f-159">Si implementa este método, hacerlo de acuerdo con la documentación de aquí.</span><span class="sxs-lookup"><span data-stu-id="5234f-159">If you implement this method, do so according to the documentation here.</span></span> <span data-ttu-id="5234f-160">Debido a que no se negocian objetos folder y objetos de estado, como mínimo implementación del proveedor de transporte remoto de **SaveChanges** debe devolver S_OK sin realmente realizar cualquier trabajo.</span><span class="sxs-lookup"><span data-stu-id="5234f-160">Because folder objects and status objects are not transacted, at a minimum a remote transport provider's implementation of **SaveChanges** must return S_OK without actually doing any work.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5234f-161">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="5234f-161">Notes to callers</span></span>

<span data-ttu-id="5234f-162">Si un cliente pasa KEEP_OPEN_READONLY, llama al método [IMAPIProp::SetProps](imapiprop-setprops.md) y, a continuación, llama a **SaveChanges** de nuevo, puede producirse un error en la misma implementación.</span><span class="sxs-lookup"><span data-stu-id="5234f-162">If a client passes KEEP_OPEN_READONLY, calls the [IMAPIProp::SetProps](imapiprop-setprops.md) method, and then calls **SaveChanges** again, the same implementation might fail.</span></span> 
  
<span data-ttu-id="5234f-163">Después de recibir una llamada MAPI_E_NO_ACCESS en el que establecer KEEP_OPEN_READWRITE, continuará tienen permiso de lectura y escritura para el objeto.</span><span class="sxs-lookup"><span data-stu-id="5234f-163">After receiving MAPI_E_NO_ACCESS from a call in which you set KEEP_OPEN_READWRITE, you will continue to have read/write permission to the object.</span></span> <span data-ttu-id="5234f-164">Puede llamar a **SaveChanges** nuevo, pasando el indicador KEEP_OPEN_READONLY o sin marcadores con KEEP_OPEN_SUFFIX.</span><span class="sxs-lookup"><span data-stu-id="5234f-164">You can call **SaveChanges** again, passing either the KEEP_OPEN_READONLY flag or no flags with KEEP_OPEN_SUFFIX.</span></span> 
  
<span data-ttu-id="5234f-165">Si un proveedor admite la marca KEEP_OPEN_READWRITE depende de la implementación del proveedor.</span><span class="sxs-lookup"><span data-stu-id="5234f-165">Whether a provider supports the KEEP_OPEN_READWRITE flag depends on the provider's implementation.</span></span> 
  
<span data-ttu-id="5234f-166">Para indicar que la llamada sólo deben realizar en el objeto después de **SaveChanges** es **IUnknown:: Release**, no establezca marcadores para el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="5234f-166">To indicate that the only call to be made on the object after **SaveChanges** is **IUnknown::Release**, set no flags for the  _ulFlags_ parameter.</span></span> <span data-ttu-id="5234f-167">Un error de **SaveChanges** indica que podrían no realizar los cambios pendientes permanente.</span><span class="sxs-lookup"><span data-stu-id="5234f-167">An error from **SaveChanges** indicates that it could not make the pending changes permanent.</span></span> <span data-ttu-id="5234f-168">Distintos proveedores de tratar la ausencia de indicadores en la llamada **SaveChanges** de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="5234f-168">Different providers handle the absence of flags on the **SaveChanges** call differently.</span></span> <span data-ttu-id="5234f-169">Algunos proveedores de tratan este estado igual que KEEP_OPEN_READONLY; otros proveedores de interpretan el mismo que KEEP_OPEN_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="5234f-169">Some providers treat this state the same as KEEP_OPEN_READONLY; other providers interpret it the same as KEEP_OPEN_READWRITE.</span></span> <span data-ttu-id="5234f-170">Aún otros proveedores apague el objeto cuando no reciben marcas en la llamada de **SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="5234f-170">Still other providers shut down the object when they do not receive flags on the **SaveChanges** call.</span></span> 
  
<span data-ttu-id="5234f-171">Algunas propiedades, propiedades calculadas por lo general, no se puede procesar hasta que se llame **SaveChanges** y, en algunos casos, la **versión**.</span><span class="sxs-lookup"><span data-stu-id="5234f-171">Some properties, typically computed properties, cannot be processed until you call **SaveChanges** and, in some cases, **Release**.</span></span>
  
<span data-ttu-id="5234f-172">Cuando se realizan cambios de forma masiva, como guardar los datos adjuntos a varios mensajes, aplazar error al procesar estableciendo el indicador MAPI_DEFERRED_ERRORS en _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="5234f-172">When you make bulk changes, such as saving attachments to multiple messages, defer error processing by setting the MAPI_DEFERRED_ERRORS flag in  _ulFlags_.</span></span> <span data-ttu-id="5234f-173">Si guarda los datos adjuntos de varios a varios mensajes, realizar una **SaveChanges** llamar a cada dato adjunto y uno **SaveChanges** llamar a cada mensaje.</span><span class="sxs-lookup"><span data-stu-id="5234f-173">If you save multiple attachments to multiple messages, make one **SaveChanges** call to each attachment and one **SaveChanges** call to each message.</span></span> <span data-ttu-id="5234f-174">Establecer la marca MAPI_DEFERRED_ERRORS para cada llamada de datos adjuntos y para todos los mensajes excepto el último.</span><span class="sxs-lookup"><span data-stu-id="5234f-174">Set the MAPI_DEFERRED_ERRORS flag for each attachment call and for all messages except for the last one.</span></span> 
  
<span data-ttu-id="5234f-175">Si **SaveChanges** devuelve MAPI_E_OBJECT_CHANGED, compruebe si se ha modificado el objeto original.</span><span class="sxs-lookup"><span data-stu-id="5234f-175">If **SaveChanges** returns MAPI_E_OBJECT_CHANGED, check whether the original object has been modified.</span></span> <span data-ttu-id="5234f-176">Si es así, avisar al usuario, que ya sea puede solicitar que los cambios de sobrescribirán los cambios anteriores o guardar el objeto en otra ubicación.</span><span class="sxs-lookup"><span data-stu-id="5234f-176">If so, warn the user, who can either request that the changes overwrite the previous changes or save the object elsewhere.</span></span> <span data-ttu-id="5234f-177">Si se ha eliminado el objeto original, advertir al usuario que conceda la oportunidad de guardar el objeto en otra ubicación.</span><span class="sxs-lookup"><span data-stu-id="5234f-177">If the original object has been deleted, warn the user to give them the opportunity to save the object in another location.</span></span> 
  
<span data-ttu-id="5234f-178">No se puede llamar a **SaveChanges** con la marca FORCE_SAVE en un objeto abierto que se ha eliminado.</span><span class="sxs-lookup"><span data-stu-id="5234f-178">You cannot call **SaveChanges** with the FORCE_SAVE flag on an open object that has been deleted.</span></span> 
  
<span data-ttu-id="5234f-179">Si **SaveChanges** devuelve un error, abra el objeto cuyos cambios tenían que guardarse permanece, independientemente de los indicadores establecidos en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="5234f-179">If **SaveChanges** returns an error, the object whose changes were to be saved remains open, regardless of the flags set in the  _ulFlags_ parameter.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="5234f-180">El _ulFlags_ NON_EMS_XP_SAVE y SPAMFILTER_ONSAVE no pueden definirse en el archivo de encabezado que se pueden descargar tiene actualmente, en cuyo caso se puede agregar a su código con los siguientes valores: >`#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`</span><span class="sxs-lookup"><span data-stu-id="5234f-180">The  _ulFlags_ NON_EMS_XP_SAVE and SPAMFILTER_ONSAVE might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following values: >  `#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`</span></span>
  
<span data-ttu-id="5234f-181">Para obtener más información, vea [Guardar las propiedades de MAPI](saving-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="5234f-181">For more information, see [Saving MAPI Properties](saving-mapi-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5234f-182">Vea también</span><span class="sxs-lookup"><span data-stu-id="5234f-182">See also</span></span>



[<span data-ttu-id="5234f-183">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="5234f-183">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="5234f-184">Propiedad canónico PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="5234f-184">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="5234f-185">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5234f-185">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="5234f-186">Guardar las propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5234f-186">Saving MAPI Properties</span></span>](saving-mapi-properties.md)

