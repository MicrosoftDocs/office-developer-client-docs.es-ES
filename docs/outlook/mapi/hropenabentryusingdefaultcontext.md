---
title: HrOpenABEntryUsingDefaultContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17cba69b-2b25-4b99-99d9-ec68fb8a35b5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f60c4d3761694439d10b073fda5bc36443c13e43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434343"
---
# <a name="hropenabentryusingdefaultcontext"></a><span data-ttu-id="27aca-103">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="27aca-103">HrOpenABEntryUsingDefaultContext</span></span>

  
  
<span data-ttu-id="27aca-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27aca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27aca-105">Realiza la misma función que [HrOpenABEntryWithExchangeContext,](hropenabentrywithexchangecontext.md) excepto que usa **el emsmdbUID** heredado como el _parámetro pEmsmdbUID._</span><span class="sxs-lookup"><span data-stu-id="27aca-105">Performs the same function as [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) except that it uses the legacy **emsmdbUID** as the  _pEmsmdbUID_ parameter.</span></span> <span data-ttu-id="27aca-106">No use esta función a menos que no pueda obtener el **emsmdbUID** correcto para la llamada a [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md).</span><span class="sxs-lookup"><span data-stu-id="27aca-106">Do not use this function unless you cannot obtain the correct **emsmdbUID** for the call to [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="27aca-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="27aca-107">Header file:</span></span>  <br/> |<span data-ttu-id="27aca-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="27aca-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="27aca-109">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="27aca-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="27aca-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="27aca-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="27aca-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="27aca-111">Called by:</span></span>  <br/> |<span data-ttu-id="27aca-112">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="27aca-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryUsingDefaultContext(
  LPMAPISESSION pmsess,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="27aca-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="27aca-113">Parameters</span></span>

 <span data-ttu-id="27aca-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="27aca-114">_pmsess_</span></span>
  
> <span data-ttu-id="27aca-115">[in] La sesión iniciada **en IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="27aca-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="27aca-116">No puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="27aca-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="27aca-117">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="27aca-117">_pAddrBook_</span></span>
  
> <span data-ttu-id="27aca-118">[in] La libreta de direcciones usada para abrir el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="27aca-118">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="27aca-119">No puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="27aca-119">It cannot be NULL.</span></span>
    
 <span data-ttu-id="27aca-120">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="27aca-120">_cbEntryID_</span></span>
  
> <span data-ttu-id="27aca-121">[in] Recuento de bytes del identificador de entrada especificado por el _parámetro lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="27aca-121">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="27aca-122">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="27aca-122">_lpEntryID_</span></span>
  
>  <span data-ttu-id="27aca-123">[in] Puntero al identificador de entrada que representa la entrada de la libreta de direcciones que se debe abrir.</span><span class="sxs-lookup"><span data-stu-id="27aca-123">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="27aca-124">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="27aca-124">_lpInterface_</span></span>
  
> <span data-ttu-id="27aca-125">[in] Puntero al identificador de interfaz (IID) de la interfaz que se usa para obtener acceso a la entrada abierta.</span><span class="sxs-lookup"><span data-stu-id="27aca-125">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="27aca-126">Si se pasa NULL, se devuelve la interfaz estándar del objeto.</span><span class="sxs-lookup"><span data-stu-id="27aca-126">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="27aca-127">Para los usuarios de mensajería, la interfaz estándar es [IMailUser : IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="27aca-127">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="27aca-128">Para las listas de distribución es [IDistList : IMAPIContainer](idistlistimapicontainer.md)y para los contenedores es [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="27aca-128">For distribution lists it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="27aca-129">Los autores de llamadas pueden  _establecer lpInterface_ en la interfaz estándar adecuada o en una interfaz de la jerarquía de herencia.</span><span class="sxs-lookup"><span data-stu-id="27aca-129">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="27aca-130">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="27aca-130">_ulFlags_</span></span>
  
> <span data-ttu-id="27aca-131">[in] Máscara de bits de marcas que controla cómo se abre la entrada.</span><span class="sxs-lookup"><span data-stu-id="27aca-131">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="27aca-132">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="27aca-132">The following flags can be set:</span></span>
    
<span data-ttu-id="27aca-133">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="27aca-133">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="27aca-134">Solicita que la entrada se abra con los permisos máximos permitidos de red y cliente.</span><span class="sxs-lookup"><span data-stu-id="27aca-134">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="27aca-135">Por ejemplo, si el cliente tiene permiso de lectura y escritura, el proveedor de libreta de direcciones intenta abrir la entrada con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="27aca-135">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="27aca-136">El cliente puede recuperar el nivel de acceso concedido llamando al método [IMAPIProp::GetProps](imapiprop-getprops.md) de la entrada abierta y recuperando la propiedad PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="27aca-136">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="27aca-137">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="27aca-137">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="27aca-138">Usa solo la libreta de direcciones sin conexión para realizar la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="27aca-138">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="27aca-139">Por ejemplo, puede usar esta marca para permitir que una aplicación cliente abra la lista global de direcciones (GAL) en modo de intercambio en caché y acceda a una entrada de esa libreta de direcciones desde la memoria caché sin crear tráfico entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="27aca-139">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="27aca-140">Esta marca solo es compatible con el Exchange libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="27aca-140">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="27aca-141">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="27aca-141">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="27aca-142">Permite que la llamada se haga correctamente, posiblemente antes de que la entrada esté totalmente abierta y disponible, lo que implica que las llamadas posteriores a la entrada podrían devolver un error.</span><span class="sxs-lookup"><span data-stu-id="27aca-142">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="27aca-143">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="27aca-143">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="27aca-144">Usa solo la GAL para realizar la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="27aca-144">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="27aca-145">Esta marca solo es compatible con el Exchange libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="27aca-145">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="27aca-146">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="27aca-146">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="27aca-147">Solicita que la entrada se abra con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="27aca-147">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="27aca-148">Dado que las entradas se abren con acceso de solo lectura de forma predeterminada, los clientes no deben asumir que se haya concedido permiso de lectura y escritura independientemente de si MAPI_MODIFY está establecido.</span><span class="sxs-lookup"><span data-stu-id="27aca-148">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="27aca-149">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="27aca-149">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="27aca-150">No usa la libreta de direcciones sin conexión para realizar la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="27aca-150">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="27aca-151">Esta marca solo es compatible con el Exchange libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="27aca-151">This flag is supported only by the Exchange address book provider.</span></span>
    
 <span data-ttu-id="27aca-152">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="27aca-152">_lpulObjType_</span></span>
  
> <span data-ttu-id="27aca-153">[salida] Puntero al tipo de entrada abierta.</span><span class="sxs-lookup"><span data-stu-id="27aca-153">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="27aca-154">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="27aca-154">_lppUnk_</span></span>
  
> <span data-ttu-id="27aca-155">[salida] Puntero a un puntero de la entrada abierta.</span><span class="sxs-lookup"><span data-stu-id="27aca-155">[out] A pointer to a pointer of the opened entry.</span></span>
    

