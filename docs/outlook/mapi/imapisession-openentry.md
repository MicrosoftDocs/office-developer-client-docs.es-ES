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
ms.openlocfilehash: 10992fdf53c416c473b90b5748b9c5fa4f65cffc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426390"
---
# <a name="imapisessionopenentry"></a><span data-ttu-id="b6695-103">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="b6695-103">IMAPISession::OpenEntry</span></span>

  
  
<span data-ttu-id="b6695-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6695-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6695-105">Abre un objeto y devuelve un puntero de interfaz para obtener acceso adicional.</span><span class="sxs-lookup"><span data-stu-id="b6695-105">Opens an object and returns an interface pointer for additional access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="b6695-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="b6695-106">Parameters</span></span>

 <span data-ttu-id="b6695-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="b6695-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="b6695-108">a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="b6695-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="b6695-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="b6695-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="b6695-110">a Un puntero al identificador de entrada del objeto que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="b6695-110">[in] A pointer to the entry identifier of the object to open.</span></span>
    
 <span data-ttu-id="b6695-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="b6695-111">_lpInterface_</span></span>
  
> <span data-ttu-id="b6695-112">a Puntero al identificador de interfaz (IID) que representa la interfaz que se va a utilizar para tener acceso al objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="b6695-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the opened object.</span></span> <span data-ttu-id="b6695-113">Al pasar NULL, se devuelve la interfaz estándar del objeto.</span><span class="sxs-lookup"><span data-stu-id="b6695-113">Passing NULL returns the object's standard interface.</span></span> <span data-ttu-id="b6695-114">Por ejemplo, si el objeto que se va a abrir es un mensaje, la interfaz estándar es [IMessage](imessageimapiprop.md); para las carpetas, es [IMAPIFolder](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="b6695-114">For example, if the object to be opened is a message, the standard interface is [IMessage](imessageimapiprop.md); for folders, it is [IMAPIFolder](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="b6695-115">Las interfaces estándar para los objetos de la libreta de direcciones son [IDistList](idistlistimapicontainer.md) para una lista de distribución y [IMailUser](imailuserimapiprop.md) para un usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="b6695-115">The standard interfaces for address book objects are [IDistList](idistlistimapicontainer.md) for a distribution list and [IMailUser](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="b6695-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b6695-116">_ulFlags_</span></span>
  
> <span data-ttu-id="b6695-117">a Máscara de máscara de marcadores que controla cómo se abre el objeto.</span><span class="sxs-lookup"><span data-stu-id="b6695-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="b6695-118">Se pueden usar los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="b6695-118">The following flags can be used:</span></span>
    
<span data-ttu-id="b6695-119">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="b6695-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="b6695-120">Solicita que el objeto se abra mediante el número máximo de permisos de red permitidos para el usuario y el máximo acceso a la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="b6695-120">Requests that the object be opened by using the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="b6695-121">Por ejemplo, si el cliente tiene permiso de lectura y escritura, el objeto debe abrirse con permiso de lectura y escritura; Si el cliente tiene permiso de solo lectura, el objeto debe abrirse con permiso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b6695-121">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only permission, the object should be opened with read-only permission.</span></span> 
    
<span data-ttu-id="b6695-122">MAPI_CACHE_OK</span><span class="sxs-lookup"><span data-stu-id="b6695-122">MAPI_CACHE_OK</span></span>
  
> <span data-ttu-id="b6695-123">Use todos los medios, incluidas las libretas de direcciones sin conexión, para realizar la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="b6695-123">Use all means, including offline address books, to perform name resolution.</span></span>
    
<span data-ttu-id="b6695-124">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="b6695-124">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="b6695-125">Use solo la libreta de direcciones sin conexión para realizar la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="b6695-125">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="b6695-126">Por ejemplo, puede usar esta marca para permitir que una aplicación cliente Abra la lista global de direcciones (GAL) en el modo caché de Exchange y obtenga acceso a una entrada de la libreta de direcciones desde la memoria caché sin crear tráfico entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="b6695-126">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="b6695-127">Este indicador solo es compatible con el proveedor de libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b6695-127">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="b6695-128">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="b6695-128">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="b6695-129">Permite que **OpenEntry** se devuelva correctamente, posiblemente antes de que el objeto esté completamente disponible para el cliente que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="b6695-129">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="b6695-130">Si el objeto no está disponible, realizar una llamada subsiguiente a un objeto puede provocar un error.</span><span class="sxs-lookup"><span data-stu-id="b6695-130">If the object is not available, making a subsequent object call can cause an error.</span></span> 
    
<span data-ttu-id="b6695-131">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="b6695-131">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="b6695-132">Solicita el permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="b6695-132">Requests read/write permission.</span></span> <span data-ttu-id="b6695-133">De forma predeterminada, los objetos se abren con permiso de solo lectura y los clientes no deben trabajar en el supuesto de que se conceda permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="b6695-133">By default, objects are opened with read-only permission, and clients should not work on the assumption that read/write permission is granted.</span></span> 
    
<span data-ttu-id="b6695-134">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="b6695-134">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="b6695-135">No use la libreta de direcciones sin conexión para realizar la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="b6695-135">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="b6695-136">Este indicador solo es compatible con el proveedor de libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b6695-136">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="b6695-137">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="b6695-137">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="b6695-138">Muestra los elementos que están marcados actualmente como eliminados temporalmente (es decir, se encuentran en la fase de tiempo de retención de elementos eliminados).</span><span class="sxs-lookup"><span data-stu-id="b6695-138">Show items that are currently marked as soft deleted (that is, they are in the deleted item retention time phase).</span></span>
    
 <span data-ttu-id="b6695-139">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="b6695-139">_lpulObjType_</span></span>
  
> <span data-ttu-id="b6695-140">contempla Un puntero al tipo del objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="b6695-140">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="b6695-141">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="b6695-141">_lppUnk_</span></span>
  
> <span data-ttu-id="b6695-142">contempla Un puntero a un puntero al objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="b6695-142">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b6695-143">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b6695-143">Return value</span></span>

<span data-ttu-id="b6695-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="b6695-144">S_OK</span></span> 
  
> <span data-ttu-id="b6695-145">El objeto se ha abierto correctamente.</span><span class="sxs-lookup"><span data-stu-id="b6695-145">The object was opened successfully.</span></span>
    
<span data-ttu-id="b6695-146">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="b6695-146">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="b6695-147">Se ha intentado modificar un objeto de solo lectura o se ha intentado obtener acceso a un objeto para el que el usuario no tiene permisos suficientes.</span><span class="sxs-lookup"><span data-stu-id="b6695-147">An attempt was made to modify a read-only object or an attempt was made to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="b6695-148">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="b6695-148">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="b6695-149">No hay un objeto asociado con el identificador de entrada pasado en el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="b6695-149">There is not an object associated with the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="b6695-150">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="b6695-150">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="b6695-151">El identificador de entrada pasado en el parámetro _lpEntryID_ tiene un formato irreconocible.</span><span class="sxs-lookup"><span data-stu-id="b6695-151">The entry identifier passed in the  _lpEntryID_ parameter is in an unrecognizable format.</span></span> <span data-ttu-id="b6695-152">Normalmente, este valor se devuelve si el proveedor de servicios que contiene el objeto no está abierto.</span><span class="sxs-lookup"><span data-stu-id="b6695-152">This value is typically returned if the service provider that contains the object is not open.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b6695-153">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b6695-153">Remarks</span></span>

<span data-ttu-id="b6695-154">El método **IMAPISession:: OpenEntry** abre un objeto de la libreta de direcciones o un almacén de mensajes, que devuelve un puntero a una interfaz que se puede usar para tener acceso al objeto.</span><span class="sxs-lookup"><span data-stu-id="b6695-154">The **IMAPISession::OpenEntry** method opens a message store or address book object, returning a pointer to an interface that can be used to access the object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b6695-155">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="b6695-155">Notes to callers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b6695-156">Al abrir las entradas de carpeta en un almacén público, como carpetas y mensajes, use [IMsgStore:: OpenEntry](imsgstore-openentry.md) en lugar de **IMAPISession:: OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="b6695-156">When opening folder entries on a public store, such as folders and messages, use [IMsgStore::OpenEntry](imsgstore-openentry.md) instead of **IMAPISession::OpenEntry**.</span></span> <span data-ttu-id="b6695-157">Esto garantiza que las carpetas públicas funcionen correctamente cuando se definen varias cuentas de Exchange en un perfil.</span><span class="sxs-lookup"><span data-stu-id="b6695-157">This ensures that public folders function correctly when multiple Exchange accounts are defined in a profile.</span></span> 
  
<span data-ttu-id="b6695-158">Llame a **IMAPISession:: OpenEntry** solo cuando no sepa qué tipo de objeto está abriendo.</span><span class="sxs-lookup"><span data-stu-id="b6695-158">Call **IMAPISession::OpenEntry** only when you do not know what kind of object that you are opening.</span></span> <span data-ttu-id="b6695-159">Si sabe que va a abrir una carpeta o un mensaje, llame a [IMsgStore:: OpenEntry](imsgstore-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="b6695-159">If you know that you are opening a folder or a message, call [IMsgStore::OpenEntry](imsgstore-openentry.md).</span></span> <span data-ttu-id="b6695-160">Si sabe que va a abrir un contenedor de libreta de direcciones, un usuario de mensajería o una lista de distribución, llame a [IAddrBook:: OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="b6695-160">If you know that you are opening an address book container, a messaging user, or a distribution list, call [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="b6695-161">Estos métodos más específicos son más rápidos que **IMAPISession:: OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="b6695-161">These more specific methods are faster than **IMAPISession::OpenEntry**.</span></span> 
  
<span data-ttu-id="b6695-162">MAPI abre todos los objetos con permiso de solo lectura, a menos que establezca el indicador MAPI_MODIFY o MAPI_BEST_ACCESS en el parámetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="b6695-162">MAPI opens all objects with read-only permission, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="b6695-163">La configuración de uno de estos marcadores no garantiza un tipo concreto de acceso; los permisos que se conceden dependen del proveedor de servicios, el nivel de acceso y el objeto.</span><span class="sxs-lookup"><span data-stu-id="b6695-163">Setting one of these flags does not guarantee a particular type of access; the permissions that are granted depend on the service provider, the access level, and the object.</span></span> <span data-ttu-id="b6695-164">Para determinar el nivel de acceso del objeto abierto, recupere su propiedad **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b6695-164">To determine the access level of the opened object, retrieve its **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="b6695-165">Llamar a **IMAPISession:: OpenEntry** y establecer _lpEntryID_ para que apunten al identificador de entrada de un almacén de mensajes es el mismo que llamar al método [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) con la marca MDB_NO_DIALOG establecida.</span><span class="sxs-lookup"><span data-stu-id="b6695-165">Calling **IMAPISession::OpenEntry** and setting  _lpEntryID_ to point to the entry identifier of a message store is the same as calling the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method with the MDB_NO_DIALOG flag set.</span></span> <span data-ttu-id="b6695-166">La configuración de la marca también es equivalente, excepto en que para solicitar el permiso de lectura/escritura con **OpenMsgStore**, debe establecer la marca MDB_WRITE en lugar de MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="b6695-166">The flag settings are also equivalent, except that to request read/write permission with **OpenMsgStore**, you must set the MDB_WRITE flag instead of MAPI_MODIFY.</span></span> 
  
<span data-ttu-id="b6695-167">Compruebe el valor devuelto en el parámetro _lpulObjType_ para determinar si el tipo de objeto devuelto es el esperado.</span><span class="sxs-lookup"><span data-stu-id="b6695-167">Check the value returned in the  _lpulObjType_ parameter to determine whether the object type returned is what you expected.</span></span> <span data-ttu-id="b6695-168">Si el tipo de objeto no es el tipo que esperaba, convierta el puntero del parámetro _lppUnk_ en un puntero del tipo apropiado.</span><span class="sxs-lookup"><span data-stu-id="b6695-168">If the object type is not the type that you expected, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type.</span></span> <span data-ttu-id="b6695-169">Por ejemplo, si abre una carpeta, convierta _lppUnk_ en un puntero de tipo LPMAPIFOLDER.</span><span class="sxs-lookup"><span data-stu-id="b6695-169">For example, if you are opening a folder, cast  _lppUnk_ to a pointer of type LPMAPIFOLDER.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b6695-170">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b6695-170">MFCMAPI reference</span></span>

<span data-ttu-id="b6695-171">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="b6695-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b6695-172">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="b6695-172">**File**</span></span>|<span data-ttu-id="b6695-173">**Función**</span><span class="sxs-lookup"><span data-stu-id="b6695-173">**Function**</span></span>|<span data-ttu-id="b6695-174">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="b6695-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b6695-175">MAPIFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="b6695-175">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="b6695-176">CallOpenEntry</span><span class="sxs-lookup"><span data-stu-id="b6695-176">CallOpenEntry</span></span>  <br/> |<span data-ttu-id="b6695-177">MFCMAPI usa el método **IMAPISession:: OpenEntry** para abrir un objeto.</span><span class="sxs-lookup"><span data-stu-id="b6695-177">MFCMAPI uses the **IMAPISession::OpenEntry** method to open an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b6695-178">Ver también</span><span class="sxs-lookup"><span data-stu-id="b6695-178">See also</span></span>



[<span data-ttu-id="b6695-179">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="b6695-179">IAddrBook::OpenEntry</span></span>](iaddrbook-openentry.md)
  
[<span data-ttu-id="b6695-180">IDistList : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="b6695-180">IDistList : IMAPIContainer</span></span>](idistlistimapicontainer.md)
  
[<span data-ttu-id="b6695-181">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b6695-181">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md)
  
[<span data-ttu-id="b6695-182">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="b6695-182">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="b6695-183">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="b6695-183">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="b6695-184">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b6695-184">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
  
[<span data-ttu-id="b6695-185">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="b6695-185">IMsgStore::OpenEntry</span></span>](imsgstore-openentry.md)
  
[<span data-ttu-id="b6695-186">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b6695-186">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="b6695-187">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="b6695-187">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

