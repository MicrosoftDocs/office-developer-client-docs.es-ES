---
title: IMsgStoreOpenEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.OpenEntry
api_type:
- COM
ms.assetid: a63c42cf-36af-466b-b41e-d6b53ce1c9fb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 07667558a21a9110d684164d2e6c143d6a519368
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409338"
---
# <a name="imsgstoreopenentry"></a><span data-ttu-id="3472f-103">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="3472f-103">IMsgStore::OpenEntry</span></span>

  
  
<span data-ttu-id="3472f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3472f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3472f-105">Abre una carpeta o un mensaje y devuelve un puntero de interfaz para obtener más acceso.</span><span class="sxs-lookup"><span data-stu-id="3472f-105">Opens a folder or message and returns an interface pointer for further access.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="3472f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3472f-106">Parameters</span></span>

 <span data-ttu-id="3472f-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="3472f-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="3472f-108">[entrada] El recuento de bytes en el identificador de entrada al que apunta el  _parámetro lpEntryID_  _._</span><span class="sxs-lookup"><span data-stu-id="3472f-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter  _._</span></span>
    
 <span data-ttu-id="3472f-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="3472f-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="3472f-110">[entrada] Puntero al identificador de entrada del objeto que se debe abrir o NULL.</span><span class="sxs-lookup"><span data-stu-id="3472f-110">[in] A pointer to the entry identifier of the object to open, or NULL.</span></span> <span data-ttu-id="3472f-111">Si  _lpEntryID_ se establece en NULL, **OpenEntry** abre la carpeta raíz para el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="3472f-111">If  _lpEntryID_ is set to NULL, **OpenEntry** opens the root folder for the message store.</span></span> 
    
 <span data-ttu-id="3472f-112">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="3472f-112">_lpInterface_</span></span>
  
> <span data-ttu-id="3472f-113">[entrada] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso al objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="3472f-113">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the opened object.</span></span> <span data-ttu-id="3472f-114">Si se pasa NULL, se devuelve la interfaz estándar del objeto[(IMAPIFolder](imapifolderimapicontainer.md) para carpetas e [IMessage](imessageimapiprop.md) para mensajes).</span><span class="sxs-lookup"><span data-stu-id="3472f-114">Passing NULL results in the object's standard interface ([IMAPIFolder](imapifolderimapicontainer.md) for folders and [IMessage](imessageimapiprop.md) for messages) being returned.</span></span> 
    
 <span data-ttu-id="3472f-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3472f-115">_ulFlags_</span></span>
  
> <span data-ttu-id="3472f-116">[entrada] Máscara de bits de marcas que controla cómo se abre el objeto.</span><span class="sxs-lookup"><span data-stu-id="3472f-116">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="3472f-117">Se pueden usar las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="3472f-117">The following flags can be used:</span></span>
    
<span data-ttu-id="3472f-118">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="3472f-118">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="3472f-119">Solicita que el objeto se abra con los permisos de red máximos permitidos para el usuario y el acceso máximo a la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="3472f-119">Requests that the object be opened by using the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="3472f-120">Por ejemplo, si el cliente tiene permiso de lectura y escritura, el objeto debe abrirse mediante el permiso de lectura y escritura; si el cliente tiene permiso de solo lectura, el objeto debe abrirse mediante el permiso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3472f-120">For example, if the client has read/write permission, the object should be opened by using read/write permission; if the client has read-only permission, the object should be opened by using read-only permission.</span></span> 
    
<span data-ttu-id="3472f-121">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="3472f-121">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="3472f-122">Permite **que OpenEntry** vuelva correctamente, posiblemente antes de que el objeto esté totalmente disponible para el cliente que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="3472f-122">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="3472f-123">Si el objeto no está disponible, realizar una llamada a objeto posterior puede generar un error.</span><span class="sxs-lookup"><span data-stu-id="3472f-123">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="3472f-124">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="3472f-124">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="3472f-125">Solicita permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="3472f-125">Requests read/write permission.</span></span> <span data-ttu-id="3472f-126">De forma predeterminada, los objetos se abren con permiso de solo lectura y los clientes no deben trabajar en la suposición de que se concede permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="3472f-126">By default, objects are opened with read-only permission, and clients should not work on the assumption that read/write permission is granted.</span></span> 
    
 <span data-ttu-id="3472f-127">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="3472f-127">_lpulObjType_</span></span>
  
> <span data-ttu-id="3472f-128">[salida] Puntero al tipo del objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="3472f-128">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="3472f-129">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="3472f-129">_lppUnk_</span></span>
  
> <span data-ttu-id="3472f-130">[salida] Puntero a un puntero al objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="3472f-130">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3472f-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3472f-131">Return value</span></span>

<span data-ttu-id="3472f-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="3472f-132">S_OK</span></span> 
  
> <span data-ttu-id="3472f-133">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="3472f-133">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="3472f-134">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="3472f-134">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="3472f-135">Se intentó modificar un objeto de solo lectura o obtener acceso a un objeto para el que el usuario no tiene permisos suficientes.</span><span class="sxs-lookup"><span data-stu-id="3472f-135">An attempt was made to modify a read-only object or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="3472f-136">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="3472f-136">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="3472f-137">Cuando se abre un almacén en modo en caché, un cliente o proveedor de servicios puede llamar a **IMsgStore::OpenEntry**, estableciendo la marca MAPI_NO_CACHE para abrir un elemento o una carpeta en el almacén remoto.</span><span class="sxs-lookup"><span data-stu-id="3472f-137">When a store is opened in cached mode, a client or service provider can call **IMsgStore::OpenEntry**, setting the MAPI_NO_CACHE flag to open an item or a folder on the remote store.</span></span> <span data-ttu-id="3472f-138">Si abre el almacén de mensajes con la marca MDB_ONLINE en el servidor remoto, no es necesario usar la marca MAPI_NO_CACHE cliente.</span><span class="sxs-lookup"><span data-stu-id="3472f-138">If you open the message store with the MDB_ONLINE flag on the remote server, you do not have to use the MAPI_NO_CACHE flag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3472f-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3472f-139">Remarks</span></span>

<span data-ttu-id="3472f-140">El **método IMsgStore::OpenEntry** abre una carpeta o un mensaje y devuelve un puntero a una interfaz que se puede usar para obtener más acceso.</span><span class="sxs-lookup"><span data-stu-id="3472f-140">The **IMsgStore::OpenEntry** method opens a folder or message and returns a pointer to an interface that can be used for further access.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="3472f-141">Al abrir entradas de carpeta en un almacén público, como carpetas y mensajes, use **IMsgStore::OpenEntry** en lugar de [IMAPISession::OpenEntry](imapisession-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="3472f-141">When opening folder entries on a public store, such as folders and messages, use **IMsgStore::OpenEntry** instead of [IMAPISession::OpenEntry](imapisession-openentry.md).</span></span> <span data-ttu-id="3472f-142">Esto garantiza que las carpetas públicas funcionen correctamente cuando se definen varias cuentas de Exchange en un perfil.</span><span class="sxs-lookup"><span data-stu-id="3472f-142">This ensures that public folders function correctly when multiple Exchange accounts are defined in a profile.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3472f-143">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="3472f-143">Notes to callers</span></span>

<span data-ttu-id="3472f-144">Las carpetas y los mensajes se abren automáticamente con permiso de solo lectura, a menos que establezca la marca MAPI_MODIFY o MAPI_BEST_ACCESS en el _parámetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="3472f-144">Folders and messages are automatically opened with read-only permission, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="3472f-145">Establecer una de estas marcas no garantiza un tipo concreto de permiso; los permisos que se le conceden dependen del proveedor del almacén de mensajes, el nivel de acceso y el objeto.</span><span class="sxs-lookup"><span data-stu-id="3472f-145">Setting one of these flags does not guarantee a particular type of permission; the permissions that you are granted depend on the message store provider, your access level, and the object.</span></span> <span data-ttu-id="3472f-146">Para determinar el nivel de acceso del objeto abierto, recupere **su PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3472f-146">To determine the access level of the opened object, retrieve its **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="3472f-147">Aunque **IMsgStore::OpenEntry** se puede usar para abrir cualquier carpeta o mensaje, suele ser más rápido usar el método [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) si tiene acceso a la carpeta principal de la carpeta o mensaje que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="3472f-147">Although **IMsgStore::OpenEntry** can be used to open any folder or message, it is usually faster to use the [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) method if you have access to the parent folder of the folder or message to be opened.</span></span> 
  
<span data-ttu-id="3472f-148">Compruebe el valor devuelto en el  _parámetro lpulObjType para_ determinar si el tipo de objeto devuelto es el esperado.</span><span class="sxs-lookup"><span data-stu-id="3472f-148">Check the value returned in the  _lpulObjType_ parameter to determine whether the returned object type is what you expected.</span></span> <span data-ttu-id="3472f-149">Si el tipo de objeto no es el tipo esperado, convierte el puntero del parámetro  _lppUnk_ en un puntero del tipo adecuado.</span><span class="sxs-lookup"><span data-stu-id="3472f-149">If the object type is not the expected type, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type.</span></span> <span data-ttu-id="3472f-150">Por ejemplo, si va a abrir una carpeta, convertir  _lppUnk_ en un puntero de tipo **LPMAPIFOLDER**.</span><span class="sxs-lookup"><span data-stu-id="3472f-150">For example, if you are opening a folder, cast  _lppUnk_ to a pointer of type **LPMAPIFOLDER**.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3472f-151">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="3472f-151">MFCMAPI reference</span></span>

<span data-ttu-id="3472f-152">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="3472f-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3472f-153">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="3472f-153">**File**</span></span>|<span data-ttu-id="3472f-154">**Función**</span><span class="sxs-lookup"><span data-stu-id="3472f-154">**Function**</span></span>|<span data-ttu-id="3472f-155">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="3472f-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3472f-156">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="3472f-156">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="3472f-157">CallOpenEntry</span><span class="sxs-lookup"><span data-stu-id="3472f-157">CallOpenEntry</span></span>  <br/> |<span data-ttu-id="3472f-158">MFCMAPI usa el **método IMsgStore::OpenEntry** para abrir el objeto asociado con un identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="3472f-158">MFCMAPI uses the **IMsgStore::OpenEntry** method to open the object associated with an entry ID.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3472f-159">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3472f-159">See also</span></span>



[<span data-ttu-id="3472f-160">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="3472f-160">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
  
[<span data-ttu-id="3472f-161">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3472f-161">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="3472f-162">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="3472f-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

