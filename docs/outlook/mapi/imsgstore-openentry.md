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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309698"
---
# <a name="imsgstoreopenentry"></a><span data-ttu-id="21fe6-103">IMsgStore::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="21fe6-103">IMsgStore::OpenEntry</span></span>

  
  
<span data-ttu-id="21fe6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21fe6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="21fe6-105">Abre una carpeta o un mensaje y devuelve un puntero de interfaz para obtener más acceso.</span><span class="sxs-lookup"><span data-stu-id="21fe6-105">Opens a folder or message and returns an interface pointer for further access.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="21fe6-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="21fe6-106">Parameters</span></span>

 <span data-ttu-id="21fe6-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="21fe6-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="21fe6-108">a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEntryID_ _._</span><span class="sxs-lookup"><span data-stu-id="21fe6-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter  _._</span></span>
    
 <span data-ttu-id="21fe6-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="21fe6-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="21fe6-110">a Un puntero al identificador de entrada del objeto que se va a abrir o NULL.</span><span class="sxs-lookup"><span data-stu-id="21fe6-110">[in] A pointer to the entry identifier of the object to open, or NULL.</span></span> <span data-ttu-id="21fe6-111">Si _lpEntryID_ se establece en null, **OpenEntry** abre la carpeta raíz del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="21fe6-111">If  _lpEntryID_ is set to NULL, **OpenEntry** opens the root folder for the message store.</span></span> 
    
 <span data-ttu-id="21fe6-112">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="21fe6-112">_lpInterface_</span></span>
  
> <span data-ttu-id="21fe6-113">a Puntero al identificador de interfaz (IID) que representa la interfaz que se va a utilizar para tener acceso al objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="21fe6-113">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the opened object.</span></span> <span data-ttu-id="21fe6-114">El paso de resultados NULOs en la interfaz estándar del objeto ([IMAPIFolder](imapifolderimapicontainer.md) para las carpetas y [IMessage](imessageimapiprop.md) para los mensajes) se devuelven.</span><span class="sxs-lookup"><span data-stu-id="21fe6-114">Passing NULL results in the object's standard interface ([IMAPIFolder](imapifolderimapicontainer.md) for folders and [IMessage](imessageimapiprop.md) for messages) being returned.</span></span> 
    
 <span data-ttu-id="21fe6-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="21fe6-115">_ulFlags_</span></span>
  
> <span data-ttu-id="21fe6-116">a Máscara de máscara de marcadores que controla cómo se abre el objeto.</span><span class="sxs-lookup"><span data-stu-id="21fe6-116">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="21fe6-117">Se pueden usar los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="21fe6-117">The following flags can be used:</span></span>
    
<span data-ttu-id="21fe6-118">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="21fe6-118">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="21fe6-119">Solicita que el objeto se abra mediante el número máximo de permisos de red permitidos para el usuario y el máximo acceso a la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="21fe6-119">Requests that the object be opened by using the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="21fe6-120">Por ejemplo, si el cliente tiene permiso de lectura y escritura, el objeto debe abrirse con el permiso de lectura y escritura; Si el cliente tiene permiso de solo lectura, el objeto debe abrirse utilizando el permiso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="21fe6-120">For example, if the client has read/write permission, the object should be opened by using read/write permission; if the client has read-only permission, the object should be opened by using read-only permission.</span></span> 
    
<span data-ttu-id="21fe6-121">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="21fe6-121">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="21fe6-122">Permite que **OpenEntry** se devuelva correctamente, posiblemente antes de que el objeto esté completamente disponible para el cliente que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="21fe6-122">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="21fe6-123">Si el objeto no está disponible, la realización de una llamada de objeto subsiguiente puede generar un error.</span><span class="sxs-lookup"><span data-stu-id="21fe6-123">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="21fe6-124">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="21fe6-124">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="21fe6-125">Solicita el permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="21fe6-125">Requests read/write permission.</span></span> <span data-ttu-id="21fe6-126">De forma predeterminada, los objetos se abren con permiso de solo lectura y los clientes no deben trabajar en el supuesto de que se conceda permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="21fe6-126">By default, objects are opened with read-only permission, and clients should not work on the assumption that read/write permission is granted.</span></span> 
    
 <span data-ttu-id="21fe6-127">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="21fe6-127">_lpulObjType_</span></span>
  
> <span data-ttu-id="21fe6-128">contempla Un puntero al tipo del objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="21fe6-128">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="21fe6-129">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="21fe6-129">_lppUnk_</span></span>
  
> <span data-ttu-id="21fe6-130">contempla Un puntero a un puntero al objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="21fe6-130">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="21fe6-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="21fe6-131">Return value</span></span>

<span data-ttu-id="21fe6-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="21fe6-132">S_OK</span></span> 
  
> <span data-ttu-id="21fe6-133">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="21fe6-133">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="21fe6-134">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="21fe6-134">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="21fe6-135">Se ha intentado modificar un objeto de solo lectura o tener acceso a un objeto para el que el usuario no tiene permisos suficientes.</span><span class="sxs-lookup"><span data-stu-id="21fe6-135">An attempt was made to modify a read-only object or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="21fe6-136">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="21fe6-136">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="21fe6-137">Cuando un almacén se abre en el modo en caché, un cliente o un proveedor de servicios puede llamar a **IMsgStore:: OpenEntry**, estableciendo la marca MAPI_NO_CACHE para abrir un elemento o una carpeta en el almacén remoto.</span><span class="sxs-lookup"><span data-stu-id="21fe6-137">When a store is opened in cached mode, a client or service provider can call **IMsgStore::OpenEntry**, setting the MAPI_NO_CACHE flag to open an item or a folder on the remote store.</span></span> <span data-ttu-id="21fe6-138">Si abre el almacén de mensajes con la marca MDB_ONLINE en el servidor remoto, no es necesario que use la marca MAPI_NO_CACHE.</span><span class="sxs-lookup"><span data-stu-id="21fe6-138">If you open the message store with the MDB_ONLINE flag on the remote server, you do not have to use the MAPI_NO_CACHE flag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="21fe6-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="21fe6-139">Remarks</span></span>

<span data-ttu-id="21fe6-140">El método **IMsgStore:: OpenEntry** abre una carpeta o un mensaje y devuelve un puntero a una interfaz que se puede usar para obtener más acceso.</span><span class="sxs-lookup"><span data-stu-id="21fe6-140">The **IMsgStore::OpenEntry** method opens a folder or message and returns a pointer to an interface that can be used for further access.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="21fe6-141">Al abrir las entradas de carpeta en un almacén público, como carpetas y mensajes, use **IMsgStore:: OpenEntry** en lugar de [IMAPISession:: OpenEntry](imapisession-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="21fe6-141">When opening folder entries on a public store, such as folders and messages, use **IMsgStore::OpenEntry** instead of [IMAPISession::OpenEntry](imapisession-openentry.md).</span></span> <span data-ttu-id="21fe6-142">Esto garantiza que las carpetas públicas funcionen correctamente cuando se definen varias cuentas de Exchange en un perfil.</span><span class="sxs-lookup"><span data-stu-id="21fe6-142">This ensures that public folders function correctly when multiple Exchange accounts are defined in a profile.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="21fe6-143">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="21fe6-143">Notes to callers</span></span>

<span data-ttu-id="21fe6-144">Las carpetas y los mensajes se abren automáticamente con permiso de solo lectura, a menos que establezca el indicador MAPI_MODIFY o MAPI_BEST_ACCESS en el parámetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="21fe6-144">Folders and messages are automatically opened with read-only permission, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="21fe6-145">La configuración de uno de estos marcadores no garantiza un tipo concreto de permiso; los permisos que se concedan dependen del proveedor de almacenamiento de mensajes, el nivel de acceso y el objeto.</span><span class="sxs-lookup"><span data-stu-id="21fe6-145">Setting one of these flags does not guarantee a particular type of permission; the permissions that you are granted depend on the message store provider, your access level, and the object.</span></span> <span data-ttu-id="21fe6-146">Para determinar el nivel de acceso del objeto abierto, recupere su propiedad **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="21fe6-146">To determine the access level of the opened object, retrieve its **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="21fe6-147">Aunque **IMsgStore:: OpenEntry** se puede usar para abrir cualquier carpeta o mensaje, suele ser más rápido usar el método [IMAPIContainer:: OpenEntry](imapicontainer-openentry.md) si tiene acceso a la carpeta principal de la carpeta o del mensaje que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="21fe6-147">Although **IMsgStore::OpenEntry** can be used to open any folder or message, it is usually faster to use the [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) method if you have access to the parent folder of the folder or message to be opened.</span></span> 
  
<span data-ttu-id="21fe6-148">Compruebe el valor devuelto en el parámetro _lpulObjType_ para determinar si el tipo de objeto devuelto es el que esperaba.</span><span class="sxs-lookup"><span data-stu-id="21fe6-148">Check the value returned in the  _lpulObjType_ parameter to determine whether the returned object type is what you expected.</span></span> <span data-ttu-id="21fe6-149">Si el tipo de objeto no es el esperado, convierta el puntero del parámetro _lppUnk_ en un puntero del tipo apropiado.</span><span class="sxs-lookup"><span data-stu-id="21fe6-149">If the object type is not the expected type, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type.</span></span> <span data-ttu-id="21fe6-150">Por ejemplo, si abre una carpeta, convierta _lppUnk_ en un puntero de tipo **LPMAPIFOLDER**.</span><span class="sxs-lookup"><span data-stu-id="21fe6-150">For example, if you are opening a folder, cast  _lppUnk_ to a pointer of type **LPMAPIFOLDER**.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="21fe6-151">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="21fe6-151">MFCMAPI reference</span></span>

<span data-ttu-id="21fe6-152">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="21fe6-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="21fe6-153">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="21fe6-153">**File**</span></span>|<span data-ttu-id="21fe6-154">**Función**</span><span class="sxs-lookup"><span data-stu-id="21fe6-154">**Function**</span></span>|<span data-ttu-id="21fe6-155">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="21fe6-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="21fe6-156">MAPIFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="21fe6-156">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="21fe6-157">CallOpenEntry</span><span class="sxs-lookup"><span data-stu-id="21fe6-157">CallOpenEntry</span></span>  <br/> |<span data-ttu-id="21fe6-158">MFCMAPI usa el método **IMsgStore:: OpenEntry** para abrir el objeto asociado con un identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="21fe6-158">MFCMAPI uses the **IMsgStore::OpenEntry** method to open the object associated with an entry ID.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="21fe6-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="21fe6-159">See also</span></span>



[<span data-ttu-id="21fe6-160">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="21fe6-160">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
  
[<span data-ttu-id="21fe6-161">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="21fe6-161">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="21fe6-162">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="21fe6-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

