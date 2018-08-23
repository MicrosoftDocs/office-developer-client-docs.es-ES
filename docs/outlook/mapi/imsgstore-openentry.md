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
ms.openlocfilehash: 611680db87c02b9370d6c1b3ac7a8d68b47f3050
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574030"
---
# <a name="imsgstoreopenentry"></a><span data-ttu-id="f3695-103">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="f3695-103">IMsgStore::OpenEntry</span></span>

  
  
<span data-ttu-id="f3695-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3695-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3695-105">Se abre una carpeta o un mensaje y devuelve un puntero de interfaz para aún más el acceso.</span><span class="sxs-lookup"><span data-stu-id="f3695-105">Opens a folder or message and returns an interface pointer for further access.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="f3695-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f3695-106">Parameters</span></span>

 <span data-ttu-id="f3695-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="f3695-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="f3695-108">[entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ _._</span><span class="sxs-lookup"><span data-stu-id="f3695-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter  _._</span></span>
    
 <span data-ttu-id="f3695-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="f3695-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="f3695-110">[entrada] Un puntero al identificador de entrada del objeto para abrir o NULL.</span><span class="sxs-lookup"><span data-stu-id="f3695-110">[in] A pointer to the entry identifier of the object to open, or NULL.</span></span> <span data-ttu-id="f3695-111">Si _lpEntryID_ se establece en NULL, **OpenEntry** abre la carpeta raíz para el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f3695-111">If  _lpEntryID_ is set to NULL, **OpenEntry** opens the root folder for the message store.</span></span> 
    
 <span data-ttu-id="f3695-112">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="f3695-112">_lpInterface_</span></span>
  
> <span data-ttu-id="f3695-113">[entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso al objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="f3695-113">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the opened object.</span></span> <span data-ttu-id="f3695-114">Si se pasa NULL da como resultado el objeto de la interfaz estándar ([IMAPIFolder](imapifolderimapicontainer.md) para las carpetas) y [IMessage](imessageimapiprop.md) para los mensajes que se devuelven.</span><span class="sxs-lookup"><span data-stu-id="f3695-114">Passing NULL results in the object's standard interface ([IMAPIFolder](imapifolderimapicontainer.md) for folders and [IMessage](imessageimapiprop.md) for messages) being returned.</span></span> 
    
 <span data-ttu-id="f3695-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f3695-115">_ulFlags_</span></span>
  
> <span data-ttu-id="f3695-116">[entrada] Una máscara de bits de indicadores que controla cómo se abre el objeto.</span><span class="sxs-lookup"><span data-stu-id="f3695-116">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="f3695-117">Se pueden usar los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="f3695-117">The following flags can be used:</span></span>
    
<span data-ttu-id="f3695-118">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="f3695-118">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="f3695-119">Solicita que se abre el objeto mediante el uso de los permisos de red máximo permitidos para el acceso de usuarios y el número máximo de clientes aplicación.</span><span class="sxs-lookup"><span data-stu-id="f3695-119">Requests that the object be opened by using the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="f3695-120">Por ejemplo, si el cliente no tiene permiso de lectura y escritura, se debe abrir el objeto mediante el uso de permisos de lectura y escritura; Si el cliente no tiene permiso de sólo lectura, se debe abrir el objeto mediante el uso de permisos de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="f3695-120">For example, if the client has read/write permission, the object should be opened by using read/write permission; if the client has read-only permission, the object should be opened by using read-only permission.</span></span> 
    
<span data-ttu-id="f3695-121">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="f3695-121">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="f3695-122">Permite **OpenEntry** devolver de correctamente, posiblemente antes de que el objeto está totalmente disponible para el cliente de la llamada.</span><span class="sxs-lookup"><span data-stu-id="f3695-122">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="f3695-123">Si el objeto no está disponible, realizar una llamada de objeto posteriores puede provocar un error.</span><span class="sxs-lookup"><span data-stu-id="f3695-123">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="f3695-124">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="f3695-124">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="f3695-125">Las solicitudes de permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="f3695-125">Requests read/write permission.</span></span> <span data-ttu-id="f3695-126">De forma predeterminada, los objetos se abren con permiso de sólo lectura y los clientes no deben trabajar en la suposición de que se concede el permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="f3695-126">By default, objects are opened with read-only permission, and clients should not work on the assumption that read/write permission is granted.</span></span> 
    
 <span data-ttu-id="f3695-127">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="f3695-127">_lpulObjType_</span></span>
  
> <span data-ttu-id="f3695-128">[out] Un puntero al tipo del objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="f3695-128">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="f3695-129">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="f3695-129">_lppUnk_</span></span>
  
> <span data-ttu-id="f3695-130">[out] Un puntero a un puntero al objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="f3695-130">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f3695-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f3695-131">Return value</span></span>

<span data-ttu-id="f3695-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3695-132">S_OK</span></span> 
  
> <span data-ttu-id="f3695-133">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="f3695-133">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="f3695-134">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="f3695-134">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="f3695-135">Se ha intentado para modificar un objeto de sólo lectura o para obtener acceso a un objeto para el que el usuario no tiene permisos suficientes.</span><span class="sxs-lookup"><span data-stu-id="f3695-135">An attempt was made to modify a read-only object or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="f3695-136">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="f3695-136">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="f3695-137">Cuando un almacén se abre en modo en caché, puede llamar a un proveedor de servicio o cliente **IMsgStore::OpenEntry**, establecer el indicador MAPI_NO_CACHE para abrir un elemento o una carpeta en el almacén remoto.</span><span class="sxs-lookup"><span data-stu-id="f3695-137">When a store is opened in cached mode, a client or service provider can call **IMsgStore::OpenEntry**, setting the MAPI_NO_CACHE flag to open an item or a folder on the remote store.</span></span> <span data-ttu-id="f3695-138">Si se abre el almacén de mensajes con el indicador MDB_ONLINE en el servidor remoto, no es necesario usar el indicador MAPI_NO_CACHE.</span><span class="sxs-lookup"><span data-stu-id="f3695-138">If you open the message store with the MDB_ONLINE flag on the remote server, you do not have to use the MAPI_NO_CACHE flag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f3695-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f3695-139">Remarks</span></span>

<span data-ttu-id="f3695-140">El método **IMsgStore::OpenEntry** abre una carpeta o un mensaje y devuelve un puntero a una interfaz que se puede usar para aún más el acceso.</span><span class="sxs-lookup"><span data-stu-id="f3695-140">The **IMsgStore::OpenEntry** method opens a folder or message and returns a pointer to an interface that can be used for further access.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="f3695-141">Al abrir entradas de la carpeta en un almacén público, como las carpetas y mensajes, use **IMsgStore::OpenEntry** en lugar de [IMAPISession::OpenEntry](imapisession-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="f3695-141">When opening folder entries on a public store, such as folders and messages, use **IMsgStore::OpenEntry** instead of [IMAPISession::OpenEntry](imapisession-openentry.md).</span></span> <span data-ttu-id="f3695-142">Esto garantiza que funcionan las carpetas públicas correctamente cuando se definen varias cuentas de Exchange en un perfil.</span><span class="sxs-lookup"><span data-stu-id="f3695-142">This ensures that public folders function correctly when multiple Exchange accounts are defined in a profile.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f3695-143">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="f3695-143">Notes to callers</span></span>

<span data-ttu-id="f3695-144">Las carpetas y los mensajes se abren automáticamente con permisos de sólo lectura, a menos que establezca el indicador MAPI_MODIFY o MAPI_BEST_ACCESS en el parámetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="f3695-144">Folders and messages are automatically opened with read-only permission, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="f3695-145">Establecer uno de estos marcadores no garantiza un tipo concreto de permiso; dependen de los permisos que se conceden en el proveedor de almacenamiento de mensajes, su nivel de acceso y el objeto.</span><span class="sxs-lookup"><span data-stu-id="f3695-145">Setting one of these flags does not guarantee a particular type of permission; the permissions that you are granted depend on the message store provider, your access level, and the object.</span></span> <span data-ttu-id="f3695-146">Para determinar el nivel de acceso del objeto abierto, recuperar su propiedad **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f3695-146">To determine the access level of the opened object, retrieve its **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="f3695-147">Aunque **IMsgStore::OpenEntry** puede utilizarse para abrir cualquier carpeta o mensaje, suele ser más rápido utilizar el método [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) si dispone de acceso a la carpeta principal de la carpeta o el mensaje que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="f3695-147">Although **IMsgStore::OpenEntry** can be used to open any folder or message, it is usually faster to use the [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) method if you have access to the parent folder of the folder or message to be opened.</span></span> 
  
<span data-ttu-id="f3695-148">Comprobar el valor devuelto en el parámetro _lpulObjType_ para determinar si el tipo de objeto devuelto es lo que esperaba.</span><span class="sxs-lookup"><span data-stu-id="f3695-148">Check the value returned in the  _lpulObjType_ parameter to determine whether the returned object type is what you expected.</span></span> <span data-ttu-id="f3695-149">Si el tipo de objeto no es del tipo esperado, convertir el puntero desde el parámetro _lppUnk_ a un puntero del tipo apropiado.</span><span class="sxs-lookup"><span data-stu-id="f3695-149">If the object type is not the expected type, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type.</span></span> <span data-ttu-id="f3695-150">Por ejemplo, si va a abrir una carpeta, convierta _lppUnk_ a un puntero de tipo **LPMAPIFOLDER**.</span><span class="sxs-lookup"><span data-stu-id="f3695-150">For example, if you are opening a folder, cast  _lppUnk_ to a pointer of type **LPMAPIFOLDER**.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f3695-151">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f3695-151">MFCMAPI reference</span></span>

<span data-ttu-id="f3695-152">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="f3695-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f3695-153">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="f3695-153">**File**</span></span>|<span data-ttu-id="f3695-154">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="f3695-154">**Function**</span></span>|<span data-ttu-id="f3695-155">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="f3695-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f3695-156">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="f3695-156">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="f3695-157">CallOpenEntry</span><span class="sxs-lookup"><span data-stu-id="f3695-157">CallOpenEntry</span></span>  <br/> |<span data-ttu-id="f3695-158">MFCMAPI utiliza el método **IMsgStore::OpenEntry** para abrir el objeto asociado con un identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="f3695-158">MFCMAPI uses the **IMsgStore::OpenEntry** method to open the object associated with an entry ID.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f3695-159">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="f3695-159">See also</span></span>



[<span data-ttu-id="f3695-160">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="f3695-160">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
  
[<span data-ttu-id="f3695-161">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f3695-161">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="f3695-162">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="f3695-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

