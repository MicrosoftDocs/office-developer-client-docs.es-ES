---
title: HrOpenABEntryWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b640a5aa-4e36-4983-bf11-9428809e830b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 415d108f7fd9e84ba2a9090658bc0923550390f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434056"
---
# <a name="hropenabentrywithexchangecontext"></a><span data-ttu-id="5968a-103">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="5968a-103">HrOpenABEntryWithExchangeContext</span></span>

  
  
<span data-ttu-id="5968a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5968a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5968a-105">Abre el **entryID** mediante la libreta de direcciones de Exchange identificada **por pEmsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="5968a-105">Opens the **entryID** using the Exchange Address Book identified by **pEmsmdbUID**.</span></span> <span data-ttu-id="5968a-106">Esta función funciona de forma similar a [IAddrBook::D etails,](iaddrbook-details.md) excepto que el uso de esta función garantiza que [IAddrBook::OpenEntry](iaddrbook-openentry.md) se abre mediante el proveedor de libretas de direcciones de Exchange esperado.</span><span class="sxs-lookup"><span data-stu-id="5968a-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md) except that using this function ensures that the [IAddrBook::OpenEntry](iaddrbook-openentry.md) is opened by using the expected Exchange Address Book Provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5968a-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="5968a-107">Header file:</span></span>  <br/> |<span data-ttu-id="5968a-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="5968a-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="5968a-109">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="5968a-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="5968a-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="5968a-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="5968a-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="5968a-111">Called by:</span></span>  <br/> |<span data-ttu-id="5968a-112">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="5968a-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrDoABDetailsWithExchangeContext(
  LPMAPISESSION pmsess,
  const MAPIUID *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="5968a-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5968a-113">Parameters</span></span>

 <span data-ttu-id="5968a-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="5968a-114">_pmsess_</span></span>
  
> <span data-ttu-id="5968a-115">[entrada] La sesión iniciada **en IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="5968a-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="5968a-116">No puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="5968a-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="5968a-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="5968a-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="5968a-118">[entrada] Puntero a **un emsmdbUID** que identifica el servicio de Exchange que contiene el proveedor de libreta de direcciones de Exchange que esta función debe usar para mostrar detalles en el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="5968a-118">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="5968a-119">Si el identificador de entrada entrante no es un identificador de entrada del proveedor de libreta de direcciones de Exchange, este parámetro se omite y la llamada de función se comporta como [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="5968a-119">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="5968a-120">Si este parámetro es NULL o un MAPIUID cero, esta función se comporta como [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="5968a-120">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="5968a-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="5968a-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="5968a-122">[entrada] La libreta de direcciones usada para abrir el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="5968a-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="5968a-123">No puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="5968a-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="5968a-124">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="5968a-124">_cbEntryID_</span></span>
  
> <span data-ttu-id="5968a-125">[entrada] Recuento de bytes del identificador de entrada especificado por el _parámetro lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="5968a-125">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="5968a-126">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="5968a-126">_lpEntryID_</span></span>
  
>  <span data-ttu-id="5968a-127">[entrada] Puntero al identificador de entrada que representa la entrada de la libreta de direcciones que se debe abrir.</span><span class="sxs-lookup"><span data-stu-id="5968a-127">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="5968a-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5968a-128">_ulFlags_</span></span>
  
> <span data-ttu-id="5968a-129">[entrada] Máscara de bits de marcas que controla cómo se abre la entrada.</span><span class="sxs-lookup"><span data-stu-id="5968a-129">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="5968a-130">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="5968a-130">The following flags can be set:</span></span>
    
<span data-ttu-id="5968a-131">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="5968a-131">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="5968a-132">Solicita que la entrada se abra con los permisos máximos permitidos de red y cliente.</span><span class="sxs-lookup"><span data-stu-id="5968a-132">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="5968a-133">Por ejemplo, si el cliente tiene permisos de lectura y escritura, el proveedor de libreta de direcciones intenta abrir la entrada con permisos de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="5968a-133">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="5968a-134">El cliente puede recuperar el nivel de acceso concedido llamando al método [IMAPIProp::GetProps](imapiprop-getprops.md) de la entrada abierta y recuperando la propiedad PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="5968a-134">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="5968a-135">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="5968a-135">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="5968a-136">Usa solo la libreta de direcciones sin conexión para realizar la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="5968a-136">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="5968a-137">Por ejemplo, puede usar esta marca para permitir que una aplicación cliente abra la lista global de direcciones (GAL) en modo caché de Exchange y obtenga acceso a una entrada de esa libreta de direcciones desde la memoria caché sin crear tráfico entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="5968a-137">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="5968a-138">Esta marca solo es compatible con el proveedor de libretas de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5968a-138">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="5968a-139">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="5968a-139">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="5968a-140">Permite que la llamada se haga correctamente, posiblemente antes de que la entrada esté totalmente abierta y disponible, lo que implica que las llamadas posteriores a la entrada podrían devolver un error.</span><span class="sxs-lookup"><span data-stu-id="5968a-140">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="5968a-141">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="5968a-141">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="5968a-142">Usa solo la GAL para realizar la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="5968a-142">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="5968a-143">Esta marca solo es compatible con el proveedor de libretas de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5968a-143">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="5968a-144">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="5968a-144">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="5968a-145">Solicita que la entrada se abra con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="5968a-145">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="5968a-146">Dado que las entradas se abren con acceso de solo lectura de forma predeterminada, los clientes no deben suponer que se ha concedido permiso de lectura y escritura independientemente de si MAPI_MODIFY está establecido.</span><span class="sxs-lookup"><span data-stu-id="5968a-146">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="5968a-147">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="5968a-147">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="5968a-148">No usa la libreta de direcciones sin conexión para realizar la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="5968a-148">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="5968a-149">Esta marca solo es compatible con el proveedor de libretas de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5968a-149">This flag is supported only by the Exchange Address Book Provider.</span></span>
    

