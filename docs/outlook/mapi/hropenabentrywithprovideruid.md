---
title: HrOpenABEntryWithProviderUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83821a86-abff-460c-bb8e-9fd9d232dc6b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 20344185ffcbd90017fa3c3493218bd9b3ddfd74
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408897"
---
# <a name="hropenabentrywithprovideruid"></a><span data-ttu-id="9101c-103">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="9101c-103">HrOpenABEntryWithProviderUID</span></span>

  
  
<span data-ttu-id="9101c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9101c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9101c-105">Abre el **entryID** mediante la libreta de direcciones de Exchange identificada  _por pEmsabpUID_.</span><span class="sxs-lookup"><span data-stu-id="9101c-105">Opens the **entryID** using the Exchange Address Book identified by  _pEmsabpUID_.</span></span> <span data-ttu-id="9101c-106">Esta función funciona de forma similar a [IAddrBook::OpenEntry,](iaddrbook-openentry.md) excepto que el uso de esta función garantiza que [IAddrBook::OpenEntry](iaddrbook-openentry.md) se abra mediante el proveedor de libreta de direcciones de Exchange esperado.</span><span class="sxs-lookup"><span data-stu-id="9101c-106">This function works similarly to [IAddrBook::OpenEntry](iaddrbook-openentry.md) except that using this function ensures that [IAddrBook::OpenEntry](iaddrbook-openentry.md) is opened by using the expected Exchange Address Book provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9101c-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="9101c-107">Header file:</span></span>  <br/> |<span data-ttu-id="9101c-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="9101c-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="9101c-109">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="9101c-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="9101c-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="9101c-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="9101c-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="9101c-111">Called by:</span></span>  <br/> |<span data-ttu-id="9101c-112">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="9101c-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithProviderUID(
  const MAPIUID *pEmsabpUID,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="9101c-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9101c-113">Parameters</span></span>

 <span data-ttu-id="9101c-114">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="9101c-114">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="9101c-115">[entrada] Puntero a **un emsmdbUID** que identifica el servicio de Exchange que contiene el proveedor de libreta de direcciones de Exchange que esta función debe usar para mostrar detalles en el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="9101c-115">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="9101c-116">Si el identificador de entrada entrante no es un identificador de entrada del proveedor de libreta de direcciones de Exchange, este parámetro se omite y la llamada de función se comporta como [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="9101c-116">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="9101c-117">Si este parámetro es NULL o un MAPIUID cero, esta función se comporta como [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="9101c-117">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="9101c-118">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="9101c-118">_pAddrBook_</span></span>
  
> <span data-ttu-id="9101c-119">[entrada] La libreta de direcciones usada para abrir el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="9101c-119">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="9101c-120">No puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="9101c-120">It cannot be NULL.</span></span>
    
 <span data-ttu-id="9101c-121">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="9101c-121">_cbEntryID_</span></span>
  
> <span data-ttu-id="9101c-122">[entrada] Recuento de bytes del identificador de entrada especificado por el _parámetro lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="9101c-122">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="9101c-123">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="9101c-123">_lpEntryID_</span></span>
  
>  <span data-ttu-id="9101c-124">[entrada] Puntero al identificador de entrada que representa la entrada de la libreta de direcciones que se debe abrir.</span><span class="sxs-lookup"><span data-stu-id="9101c-124">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="9101c-125">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="9101c-125">_lpInterface_</span></span>
  
> <span data-ttu-id="9101c-126">[entrada] Puntero al identificador de interfaz (IID) de la interfaz que se usa para tener acceso a la entrada abierta.</span><span class="sxs-lookup"><span data-stu-id="9101c-126">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="9101c-127">Si se pasa NULL, se devuelve la interfaz estándar del objeto.</span><span class="sxs-lookup"><span data-stu-id="9101c-127">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="9101c-128">Para los usuarios de mensajería, la interfaz estándar [es IMailUser : IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="9101c-128">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="9101c-129">Para las listas de distribución, es [IDistList : IMAPIContainer](idistlistimapicontainer.md)y para contenedores, es [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="9101c-129">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md)and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="9101c-130">Los autores de llamadas pueden  _establecer lpInterface_ en la interfaz estándar adecuada o una interfaz en la jerarquía de herencia.</span><span class="sxs-lookup"><span data-stu-id="9101c-130">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="9101c-131">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9101c-131">_ulFlags_</span></span>
  
> <span data-ttu-id="9101c-132">[entrada] Máscara de bits de marcas que controla cómo se abre la entrada, se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="9101c-132">[in] A bitmask of flags that controls the how the entry is opened, The following flags can be set:</span></span>
    
<span data-ttu-id="9101c-133">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="9101c-133">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="9101c-134">Solicita que la entrada se abra con los permisos máximos permitidos de red y cliente.</span><span class="sxs-lookup"><span data-stu-id="9101c-134">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="9101c-135">Por ejemplo, si el cliente tiene permisos de lectura y escritura, el proveedor de libreta de direcciones intenta abrir la entrada con permisos de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="9101c-135">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="9101c-136">El cliente puede recuperar el nivel de acceso concedido llamando al método [IMAPIProp::GetProps](imapiprop-getprops.md) de la entrada abierta y recuperando la propiedad PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="9101c-136">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="9101c-137">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="9101c-137">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="9101c-138">Use solo la libreta de direcciones sin conexión para realizar la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="9101c-138">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="9101c-139">Por ejemplo, puede usar esta marca para permitir que una aplicación cliente abra la lista global de direcciones (GAL) en modo caché de Exchange y obtenga acceso a una entrada de esa libreta de direcciones desde la memoria caché sin crear tráfico entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="9101c-139">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="9101c-140">Esta marca solo es compatible con el proveedor de libretas de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="9101c-140">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="9101c-141">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="9101c-141">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="9101c-142">Permite que la llamada se haga correctamente, posiblemente antes de que la entrada esté totalmente abierta y disponible, lo que implica que las llamadas posteriores a la entrada podrían devolver un error.</span><span class="sxs-lookup"><span data-stu-id="9101c-142">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="9101c-143">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="9101c-143">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="9101c-144">Use solo la GAL para realizar la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="9101c-144">Use only the GAL to perform name resolution.</span></span> <span data-ttu-id="9101c-145">Esta marca solo es compatible con el proveedor de libretas de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="9101c-145">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="9101c-146">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="9101c-146">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="9101c-147">Solicita que la entrada se abra con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="9101c-147">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="9101c-148">Dado que las entradas se abren con acceso de solo lectura de forma predeterminada, los clientes no deben suponer que se ha concedido permiso de lectura y escritura independientemente de si MAPI_MODIFY está establecido.</span><span class="sxs-lookup"><span data-stu-id="9101c-148">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="9101c-149">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="9101c-149">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="9101c-150">No use la libreta de direcciones sin conexión para realizar la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="9101c-150">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="9101c-151">Esta marca solo es compatible con el proveedor de libretas de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="9101c-151">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="9101c-152">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="9101c-152">_lpulObjType_</span></span>
  
> <span data-ttu-id="9101c-153">[salida] Puntero al tipo de la entrada abierta.</span><span class="sxs-lookup"><span data-stu-id="9101c-153">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="9101c-154">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="9101c-154">_lppUnk_</span></span>
  
> <span data-ttu-id="9101c-155">[salida] Puntero a un puntero de la entrada abierta.</span><span class="sxs-lookup"><span data-stu-id="9101c-155">[out] A pointer to a pointer of the opened entry.</span></span>
    

