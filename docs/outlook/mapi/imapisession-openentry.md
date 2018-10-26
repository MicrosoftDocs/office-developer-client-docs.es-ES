---
title: IMAPISessionOpenEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenEntry
api_type:
- COM
ms.assetid: a4df4860-cf4f-4e97-97c4-fcd89b7f1f91
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6234fc737857a7e35f562703802f81ff154b3ee6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591019"
---
# <a name="imapisessionopenentry"></a><span data-ttu-id="5c338-103">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="5c338-103">IMAPISession::OpenEntry</span></span>

  
  
<span data-ttu-id="5c338-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c338-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c338-105">Se abre un objeto y devuelve un puntero de interfaz de acceso adicional.</span><span class="sxs-lookup"><span data-stu-id="5c338-105">Opens an object and returns an interface pointer for additional access.</span></span>
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="5c338-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5c338-106">Parameters</span></span>

 <span data-ttu-id="5c338-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="5c338-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="5c338-108">[entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="5c338-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="5c338-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="5c338-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="5c338-110">[entrada] Un puntero al identificador de entrada del objeto que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="5c338-110">[in] A pointer to the entry identifier of the object to open.</span></span>
    
 <span data-ttu-id="5c338-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="5c338-111">_lpInterface_</span></span>
  
> <span data-ttu-id="5c338-112">[entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso al objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="5c338-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the opened object.</span></span> <span data-ttu-id="5c338-113">Pasando NULL, devuelve la interfaz del objeto estándar.</span><span class="sxs-lookup"><span data-stu-id="5c338-113">Passing NULL returns the object's standard interface.</span></span> <span data-ttu-id="5c338-114">Por ejemplo, si el objeto que se va a abrir es un mensaje, la interfaz estándar es [IMessage](imessageimapiprop.md); para las carpetas, es [IMAPIFolder](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="5c338-114">For example, if the object to be opened is a message, the standard interface is [IMessage](imessageimapiprop.md); for folders, it is [IMAPIFolder](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="5c338-115">Las interfaces estándares para objetos de la libreta de direcciones son [IDistList](idistlistimapicontainer.md) para una lista de distribución y [IMailUser](imailuserimapiprop.md) para un usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="5c338-115">The standard interfaces for address book objects are [IDistList](idistlistimapicontainer.md) for a distribution list and [IMailUser](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="5c338-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5c338-116">_ulFlags_</span></span>
  
> <span data-ttu-id="5c338-117">[entrada] Una máscara de bits de indicadores que controla cómo se abre el objeto.</span><span class="sxs-lookup"><span data-stu-id="5c338-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="5c338-118">Se pueden usar los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="5c338-118">The following flags can be used:</span></span>
    
<span data-ttu-id="5c338-119">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="5c338-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="5c338-120">Solicita que se abre el objeto mediante el uso de los permisos de red máximo permitidos para el acceso de usuarios y el número máximo de clientes aplicación.</span><span class="sxs-lookup"><span data-stu-id="5c338-120">Requests that the object be opened by using the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="5c338-121">Por ejemplo, si el cliente no tiene permiso de lectura y escritura, se debe abrir el objeto con permisos de lectura y escritura; Si el cliente no tiene permiso de sólo lectura, se debe abrir el objeto con permiso de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="5c338-121">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only permission, the object should be opened with read-only permission.</span></span> 
    
<span data-ttu-id="5c338-122">MAPI_CACHE_OK</span><span class="sxs-lookup"><span data-stu-id="5c338-122">MAPI_CACHE_OK</span></span>
  
> <span data-ttu-id="5c338-123">Usar todos los medios, incluidos libretas de direcciones sin conexión, para llevar a cabo la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="5c338-123">Use all means, including offline address books, to perform name resolution.</span></span>
    
<span data-ttu-id="5c338-124">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="5c338-124">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="5c338-125">Usar sólo la libreta de direcciones sin conexión para llevar a cabo la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="5c338-125">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="5c338-126">Por ejemplo, puede usar esta marca para permitir que una aplicación cliente para abrir la lista global de direcciones (GAL) en el modo de intercambio en caché y obtener acceso a una entrada en esa libreta de direcciones de la memoria caché sin crear el tráfico entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="5c338-126">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="5c338-127">Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5c338-127">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="5c338-128">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="5c338-128">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="5c338-129">Permite **OpenEntry** devolver de correctamente, posiblemente antes de que el objeto está totalmente disponible para el cliente de la llamada.</span><span class="sxs-lookup"><span data-stu-id="5c338-129">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="5c338-130">Si el objeto no está disponible, realizar una llamada de objeto posteriores puede provocar un error.</span><span class="sxs-lookup"><span data-stu-id="5c338-130">If the object is not available, making a subsequent object call can cause an error.</span></span> 
    
<span data-ttu-id="5c338-131">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="5c338-131">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="5c338-132">Las solicitudes de permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="5c338-132">Requests read/write permission.</span></span> <span data-ttu-id="5c338-133">De forma predeterminada, los objetos se abren con permiso de sólo lectura y los clientes no deben trabajar en la suposición de que se concede el permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="5c338-133">By default, objects are opened with read-only permission, and clients should not work on the assumption that read/write permission is granted.</span></span> 
    
<span data-ttu-id="5c338-134">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="5c338-134">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="5c338-135">No use la libreta de direcciones sin conexión para llevar a cabo la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="5c338-135">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="5c338-136">Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5c338-136">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="5c338-137">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="5c338-137">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="5c338-138">Mostrar los elementos que actualmente están marcados como suaves eliminan (es decir, se encuentran en la retención de elementos eliminados fase de tiempo).</span><span class="sxs-lookup"><span data-stu-id="5c338-138">Show items that are currently marked as soft deleted (that is, they are in the deleted item retention time phase).</span></span>
    
 <span data-ttu-id="5c338-139">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="5c338-139">_lpulObjType_</span></span>
  
> <span data-ttu-id="5c338-140">[out] Un puntero al tipo del objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="5c338-140">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="5c338-141">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="5c338-141">_lppUnk_</span></span>
  
> <span data-ttu-id="5c338-142">[out] Un puntero a un puntero al objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="5c338-142">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5c338-143">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5c338-143">Return value</span></span>

<span data-ttu-id="5c338-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="5c338-144">S_OK</span></span> 
  
> <span data-ttu-id="5c338-145">El objeto se ha abierto correctamente.</span><span class="sxs-lookup"><span data-stu-id="5c338-145">The object was opened successfully.</span></span>
    
<span data-ttu-id="5c338-146">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="5c338-146">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="5c338-147">Se ha intentado modificar un objeto de sólo lectura o se ha intentado tener acceso a un objeto para el que el usuario no tiene permisos suficientes.</span><span class="sxs-lookup"><span data-stu-id="5c338-147">An attempt was made to modify a read-only object or an attempt was made to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="5c338-148">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="5c338-148">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="5c338-149">No es un objeto asociado con el identificador de entrada que se pasa en el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="5c338-149">There is not an object associated with the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="5c338-150">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="5c338-150">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="5c338-151">El identificador de entrada que se pasa en el parámetro _lpEntryID_ está en un formato no reconoce.</span><span class="sxs-lookup"><span data-stu-id="5c338-151">The entry identifier passed in the  _lpEntryID_ parameter is in an unrecognizable format.</span></span> <span data-ttu-id="5c338-152">Normalmente, este valor se devuelve si el proveedor de servicio que contiene el objeto no está abierto.</span><span class="sxs-lookup"><span data-stu-id="5c338-152">This value is typically returned if the service provider that contains the object is not open.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5c338-153">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5c338-153">Remarks</span></span>

<span data-ttu-id="5c338-154">Abre el método de **IMAPISession::OpenEntry** un mensaje almacenar o direcciones de objeto de libro, devuelve un puntero a una interfaz que puede utilizarse para tener acceso al objeto.</span><span class="sxs-lookup"><span data-stu-id="5c338-154">The **IMAPISession::OpenEntry** method opens a message store or address book object, returning a pointer to an interface that can be used to access the object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5c338-155">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="5c338-155">Notes to callers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5c338-156">Al abrir entradas de la carpeta en un almacén público, como las carpetas y mensajes, use [IMsgStore::OpenEntry](imsgstore-openentry.md) en lugar de **IMAPISession::OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="5c338-156">When opening folder entries on a public store, such as folders and messages, use [IMsgStore::OpenEntry](imsgstore-openentry.md) instead of **IMAPISession::OpenEntry**.</span></span> <span data-ttu-id="5c338-157">Esto garantiza que funcionan las carpetas públicas correctamente cuando se definen varias cuentas de Exchange en un perfil.</span><span class="sxs-lookup"><span data-stu-id="5c338-157">This ensures that public folders function correctly when multiple Exchange accounts are defined in a profile.</span></span> 
  
<span data-ttu-id="5c338-158">Llame a **IMAPISession::OpenEntry** sólo cuando no sabe qué tipo de objeto que va a abrir.</span><span class="sxs-lookup"><span data-stu-id="5c338-158">Call **IMAPISession::OpenEntry** only when you do not know what kind of object that you are opening.</span></span> <span data-ttu-id="5c338-159">Si sabe que va a abrir una carpeta o un mensaje, llame a [IMsgStore::OpenEntry](imsgstore-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="5c338-159">If you know that you are opening a folder or a message, call [IMsgStore::OpenEntry](imsgstore-openentry.md).</span></span> <span data-ttu-id="5c338-160">Si sabe que va a abrir un contenedor de la libreta de direcciones, un usuario de mensajería, o una lista de distribución, llame a [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="5c338-160">If you know that you are opening an address book container, a messaging user, or a distribution list, call [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="5c338-161">Estos métodos más específicos son más rápidos que **IMAPISession::OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="5c338-161">These more specific methods are faster than **IMAPISession::OpenEntry**.</span></span> 
  
<span data-ttu-id="5c338-162">MAPI abre todos los objetos con permisos de sólo lectura, a menos que establezca el indicador MAPI_MODIFY o MAPI_BEST_ACCESS en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="5c338-162">MAPI opens all objects with read-only permission, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="5c338-163">Establecer uno de estos marcadores no garantiza un tipo concreto de acceso; los permisos que se conceden dependen del proveedor de servicios, el nivel de acceso y el objeto.</span><span class="sxs-lookup"><span data-stu-id="5c338-163">Setting one of these flags does not guarantee a particular type of access; the permissions that are granted depend on the service provider, the access level, and the object.</span></span> <span data-ttu-id="5c338-164">Para determinar el nivel de acceso del objeto abierto, recuperar su propiedad **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5c338-164">To determine the access level of the opened object, retrieve its **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="5c338-165">Al llamar a **IMAPISession::OpenEntry** y configuración _lpEntryID_ para que apunte al identificador de entrada de un almacén de mensajes es el mismo que llamar al método [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) con la marca MDB_NO_DIALOG establecer.</span><span class="sxs-lookup"><span data-stu-id="5c338-165">Calling **IMAPISession::OpenEntry** and setting  _lpEntryID_ to point to the entry identifier of a message store is the same as calling the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method with the MDB_NO_DIALOG flag set.</span></span> <span data-ttu-id="5c338-166">La configuración del indicador también es equivalente, excepto en que se va a solicitar el permiso de lectura y escritura con **OpenMsgStore**, debe establecer la marca MDB_WRITE en lugar de MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="5c338-166">The flag settings are also equivalent, except that to request read/write permission with **OpenMsgStore**, you must set the MDB_WRITE flag instead of MAPI_MODIFY.</span></span> 
  
<span data-ttu-id="5c338-167">Comprobar el valor devuelto en el parámetro _lpulObjType_ para determinar si el tipo de objeto devuelto es lo que esperaba.</span><span class="sxs-lookup"><span data-stu-id="5c338-167">Check the value returned in the  _lpulObjType_ parameter to determine whether the object type returned is what you expected.</span></span> <span data-ttu-id="5c338-168">Si el tipo de objeto no es del tipo que esperaba, convertir el puntero desde el parámetro _lppUnk_ a un puntero del tipo apropiado.</span><span class="sxs-lookup"><span data-stu-id="5c338-168">If the object type is not the type that you expected, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type.</span></span> <span data-ttu-id="5c338-169">Por ejemplo, si va a abrir una carpeta, convierta _lppUnk_ a un puntero de tipo LPMAPIFOLDER.</span><span class="sxs-lookup"><span data-stu-id="5c338-169">For example, if you are opening a folder, cast  _lppUnk_ to a pointer of type LPMAPIFOLDER.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5c338-170">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="5c338-170">MFCMAPI reference</span></span>

<span data-ttu-id="5c338-171">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="5c338-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5c338-172">**File**</span><span class="sxs-lookup"><span data-stu-id="5c338-172">**File**</span></span>|<span data-ttu-id="5c338-173">**Función**</span><span class="sxs-lookup"><span data-stu-id="5c338-173">**Function**</span></span>|<span data-ttu-id="5c338-174">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="5c338-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5c338-175">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="5c338-175">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="5c338-176">CallOpenEntry</span><span class="sxs-lookup"><span data-stu-id="5c338-176">CallOpenEntry</span></span>  <br/> |<span data-ttu-id="5c338-177">MFCMAPI utiliza el método **IMAPISession::OpenEntry** para abrir un objeto.</span><span class="sxs-lookup"><span data-stu-id="5c338-177">MFCMAPI uses the **IMAPISession::OpenEntry** method to open an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5c338-178">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c338-178">See also</span></span>



[<span data-ttu-id="5c338-179">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="5c338-179">IAddrBook::OpenEntry</span></span>](iaddrbook-openentry.md)
  
[<span data-ttu-id="5c338-180">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="5c338-180">IDistList : IMAPIContainer</span></span>](idistlistimapicontainer.md)
  
[<span data-ttu-id="5c338-181">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5c338-181">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md)
  
[<span data-ttu-id="5c338-182">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="5c338-182">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="5c338-183">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="5c338-183">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="5c338-184">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5c338-184">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
  
[<span data-ttu-id="5c338-185">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="5c338-185">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
  
[<span data-ttu-id="5c338-186">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="5c338-186">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="5c338-187">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="5c338-187">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

