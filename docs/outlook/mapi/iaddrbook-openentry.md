---
title: IAddrBookOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.OpenEntry
api_type:
- COM
ms.assetid: bd7746f4-8070-4cc5-8b8e-c527c5847545
description: 'Última modificación: 1 de febrero de 2013'
ms.openlocfilehash: 293fe5a65c760f61ab0073e0eafc1a606c69050f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434168"
---
# <a name="iaddrbookopenentry"></a><span data-ttu-id="4f816-103">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="4f816-103">IAddrBook::OpenEntry</span></span>

<span data-ttu-id="4f816-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f816-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f816-105">Abre una entrada de libreta de direcciones y devuelve un puntero a una interfaz que se puede usar para obtener acceso a la entrada.</span><span class="sxs-lookup"><span data-stu-id="4f816-105">Opens an address book entry and returns a pointer to an interface that can be used to access the entry.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="4f816-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="4f816-106">Parameters</span></span>

<span data-ttu-id="4f816-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="4f816-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="4f816-108">[in] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="4f816-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="4f816-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="4f816-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="4f816-110">[in] Puntero al identificador de entrada que representa la entrada de la libreta de direcciones que se debe abrir.</span><span class="sxs-lookup"><span data-stu-id="4f816-110">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
<span data-ttu-id="4f816-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="4f816-111">_lpInterface_</span></span>
  
> <span data-ttu-id="4f816-112">[in] Puntero al identificador de interfaz (IID) de la interfaz que se usará para tener acceso a la entrada abierta.</span><span class="sxs-lookup"><span data-stu-id="4f816-112">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="4f816-113">Si se pasa NULL, se devuelve la interfaz estándar del objeto.</span><span class="sxs-lookup"><span data-stu-id="4f816-113">Passing NULL returns the object's standard interface.</span></span> <span data-ttu-id="4f816-114">Para los usuarios de mensajería, la interfaz estándar es [IMailUser : IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="4f816-114">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="4f816-115">Para las listas de distribución, es [IDistList : IMAPIContainer](idistlistimapicontainer.md) y para contenedores, es [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="4f816-115">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md) and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="4f816-116">Los autores de llamadas pueden  _establecer lpInterface_ en la interfaz estándar adecuada o en una interfaz de la jerarquía de herencia.</span><span class="sxs-lookup"><span data-stu-id="4f816-116">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
<span data-ttu-id="4f816-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4f816-117">_ulFlags_</span></span>
  
> <span data-ttu-id="4f816-118">[in] Máscara de bits de marcas que controla cómo se abre la entrada.</span><span class="sxs-lookup"><span data-stu-id="4f816-118">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="4f816-119">Se pueden establecer las siguientes marcas.</span><span class="sxs-lookup"><span data-stu-id="4f816-119">The following flags can be set.</span></span>
    
<span data-ttu-id="4f816-120">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="4f816-120">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="4f816-121">Solicita que la entrada se abra con los permisos máximos permitidos de red y cliente.</span><span class="sxs-lookup"><span data-stu-id="4f816-121">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="4f816-122">Por ejemplo, si el cliente tiene permiso de lectura y escritura, el proveedor de la libreta de direcciones debe intentar abrir la entrada con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="4f816-122">For example, if the client has read/write permission, the address book provider should attempt to open the entry with read/write permission.</span></span> <span data-ttu-id="4f816-123">El cliente puede recuperar el nivel de acceso concedido llamando al método [IMAPIProp::GetProps](imapiprop-getprops.md) de la entrada abierta y recuperando la propiedad **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4f816-123">The client can retrieve the access level that was granted by calling the open entry's [IMAPIProp::GetProps](imapiprop-getprops.md) method and retrieving the **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="4f816-124">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="4f816-124">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="4f816-125">Abre una entrada de libreta de direcciones y solo tiene acceso a ella desde la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="4f816-125">Opens an address book entry and accesses it only from the cache.</span></span> <span data-ttu-id="4f816-126">Por ejemplo, puede usar esta marca para permitir que una aplicación cliente abra la lista global de direcciones (GAL) en modo de intercambio en caché y acceda a una entrada de esa libreta de direcciones desde la memoria caché sin crear tráfico entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="4f816-126">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="4f816-127">Esta marca solo es compatible con el Exchange libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="4f816-127">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="4f816-128">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="4f816-128">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="4f816-129">Permite que la llamada se haga correctamente, posiblemente antes de que la entrada esté totalmente abierta y disponible, lo que implica que las llamadas posteriores a la entrada podrían devolver un error.</span><span class="sxs-lookup"><span data-stu-id="4f816-129">Allows the call to succeed, potentially before the entry is fully open and available, implying that later calls to the entry might return an error.</span></span>
    
<span data-ttu-id="4f816-130">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="4f816-130">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="4f816-131">Use solo la GAL para realizar la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="4f816-131">Use only the GAL to perform name resolution.</span></span> <span data-ttu-id="4f816-132">Esta marca solo es compatible con el Exchange libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="4f816-132">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="4f816-133">Es posible que MAPI_GAL_ONLY  _ulFlags_ no se defina en el archivo de encabezado descargable que tiene actualmente, en cuyo caso puede agregarlo al código con el siguiente valor: >  `#define MAPI_GAL_ONLY (0x00000080)`</span><span class="sxs-lookup"><span data-stu-id="4f816-133">The  _ulFlags_ MAPI_GAL_ONLY might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following value: >  `#define MAPI_GAL_ONLY (0x00000080)`</span></span>
  
<span data-ttu-id="4f816-134">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="4f816-134">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="4f816-135">Solicita que la entrada se abra con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="4f816-135">Requests that the entry be opened with read/write permission.</span></span> <span data-ttu-id="4f816-136">Dado que las entradas se abren con acceso de solo lectura de forma predeterminada, los clientes no deben asumir que se haya concedido permiso de lectura y escritura independientemente de si MAPI_MODIFY está establecido.</span><span class="sxs-lookup"><span data-stu-id="4f816-136">Because entries are opened with read-only access by default, clients should not assume that read/write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="4f816-137">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="4f816-137">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="4f816-138">No use la libreta de direcciones sin conexión para realizar la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="4f816-138">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="4f816-139">Esta marca solo es compatible con el Exchange libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="4f816-139">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="4f816-140">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="4f816-140">_lpulObjType_</span></span>
  
> <span data-ttu-id="4f816-141">[salida] Puntero al tipo de entrada abierta.</span><span class="sxs-lookup"><span data-stu-id="4f816-141">[out] A pointer to the type of the opened entry.</span></span>
    
<span data-ttu-id="4f816-142">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="4f816-142">_lppUnk_</span></span>
  
> <span data-ttu-id="4f816-143">[salida] Puntero a un puntero a la entrada abierta.</span><span class="sxs-lookup"><span data-stu-id="4f816-143">[out] A pointer to a pointer to the opened entry.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4f816-144">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4f816-144">Return value</span></span>

<span data-ttu-id="4f816-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="4f816-145">S_OK</span></span> 
  
> <span data-ttu-id="4f816-146">La entrada se abrió correctamente.</span><span class="sxs-lookup"><span data-stu-id="4f816-146">The entry was successfully opened.</span></span>
    
<span data-ttu-id="4f816-147">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="4f816-147">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="4f816-148">Se intentó abrir una entrada para la que el usuario no tiene permisos suficientes.</span><span class="sxs-lookup"><span data-stu-id="4f816-148">An attempt was made to open an entry for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="4f816-149">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="4f816-149">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="4f816-150">La entrada representada por  _lpEntryID_ no existe.</span><span class="sxs-lookup"><span data-stu-id="4f816-150">The entry represented by  _lpEntryID_ does not exist.</span></span> 
    
<span data-ttu-id="4f816-151">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="4f816-151">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="4f816-152">No se reconoce el identificador de entrada especificado _en lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="4f816-152">The entry identifier specified in  _lpEntryID_ is not recognized.</span></span> <span data-ttu-id="4f816-153">Este valor normalmente se devuelve si el proveedor de libreta de direcciones responsable de la entrada correspondiente no está abierto.</span><span class="sxs-lookup"><span data-stu-id="4f816-153">This value is typically returned if the address book provider responsible for the corresponding entry is not open.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4f816-154">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4f816-154">Remarks</span></span>

<span data-ttu-id="4f816-155">Los clientes y proveedores de servicios llaman al **método IAddrBook::OpenEntry** para abrir una entrada de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="4f816-155">Clients and service providers call the **IAddrBook::OpenEntry** method to open an address book entry.</span></span> <span data-ttu-id="4f816-156">MAPI reenvía la llamada al proveedor de libreta de direcciones adecuado, en función de la estructura [MAPIUID](mapiuid.md) incluida en el identificador de entrada pasado en el _parámetro lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="4f816-156">MAPI forwards the call to the appropriate address book provider, based on the [MAPIUID](mapiuid.md) structure included in the entry identifier passed in the  _lpEntryID_ parameter.</span></span> <span data-ttu-id="4f816-157">El proveedor de libreta de direcciones abre la entrada como de solo lectura a menos que se establezca MAPI_MODIFY o MAPI_BEST_ACCESS marca del parámetro _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="4f816-157">The address book provider opens the entry as read-only unless the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter is set.</span></span> <span data-ttu-id="4f816-158">Sin embargo, estas marcas son sugerencias.</span><span class="sxs-lookup"><span data-stu-id="4f816-158">However, these flags are suggestions.</span></span> <span data-ttu-id="4f816-159">Si el proveedor de libreta de direcciones no permite la modificación de la entrada solicitada, devuelve MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="4f816-159">If the address book provider does not allow modification for the entry requested, it returns MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="4f816-160">El  _parámetro lpInterface_ indica qué interfaz debe usarse para tener acceso a la entrada abierta.</span><span class="sxs-lookup"><span data-stu-id="4f816-160">The  _lpInterface_ parameter indicates which interface should be used to access the opened entry.</span></span> <span data-ttu-id="4f816-161">Si se pasa NULL en  _lpInterface,_ se debe usar la interfaz MAPI estándar para ese tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="4f816-161">Passing NULL in  _lpInterface_ indicates the standard MAPI interface for that type of entry should be used.</span></span> <span data-ttu-id="4f816-162">Dado que el proveedor de libreta de direcciones puede devolver una interfaz diferente a la sugerida por el parámetro  _lpInterface,_ el autor de la llamada debe comprobar el valor devuelto en el parámetro  _lpulObjType_ para determinar si el tipo de objeto devuelto es el esperado.</span><span class="sxs-lookup"><span data-stu-id="4f816-162">Because the address book provider might return a different interface than the one suggested by the  _lpInterface_ parameter, the caller should check the value returned in the  _lpulObjType_ parameter to determine whether the object type returned is what was expected.</span></span> <span data-ttu-id="4f816-163">Si el tipo de objeto no es del tipo esperado, el autor de la llamada puede convertir el parámetro  _lppUnk_ en un tipo que sea más adecuado.</span><span class="sxs-lookup"><span data-stu-id="4f816-163">If the object type is not of the type expected, the caller can cast the  _lppUnk_ parameter to a type that is more appropriate.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4f816-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f816-164">See also</span></span>

- [<span data-ttu-id="4f816-165">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4f816-165">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

