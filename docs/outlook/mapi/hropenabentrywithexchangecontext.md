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
ms.openlocfilehash: e0b6718345588e79a8038f7cb409ef901d7c11f5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577159"
---
# <a name="hropenabentrywithexchangecontext"></a><span data-ttu-id="26317-103">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="26317-103">HrOpenABEntryWithExchangeContext</span></span>

  
  
<span data-ttu-id="26317-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="26317-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="26317-105">Se abre la **propiedad entryID** utilizando la libreta de direcciones de Exchange identificado por **pEmsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="26317-105">Opens the **entryID** using the Exchange Address Book identified by **pEmsmdbUID**.</span></span> <span data-ttu-id="26317-106">Esta función funciona de manera similar a [IAddrBook::Details](iaddrbook-details.md) excepto en que el uso de esta función garantiza que la [IAddrBook::OpenEntry](iaddrbook-openentry.md) se abre mediante el proveedor de la libreta de direcciones de Exchange esperado.</span><span class="sxs-lookup"><span data-stu-id="26317-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md) except that using this function ensures that the [IAddrBook::OpenEntry](iaddrbook-openentry.md) is opened by using the expected Exchange Address Book Provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="26317-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="26317-107">Header file:</span></span>  <br/> |<span data-ttu-id="26317-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="26317-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="26317-109">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="26317-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="26317-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="26317-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="26317-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="26317-111">Called by:</span></span>  <br/> |<span data-ttu-id="26317-112">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="26317-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="26317-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="26317-113">Parameters</span></span>

 <span data-ttu-id="26317-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="26317-114">_pmsess_</span></span>
  
> <span data-ttu-id="26317-115">[entrada] La ha iniciado la sesión **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="26317-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="26317-116">No puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="26317-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="26317-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="26317-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="26317-118">[entrada] Un puntero a un **emsmdbUID** que identifica el servicio de Exchange que contiene el proveedor de libreta de direcciones de Exchange que se debe usar esta función para mostrar los detalles en el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="26317-118">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="26317-119">Si el identificador de entrada entrante no es un identificador de entrada del proveedor de libreta de direcciones de Exchange, este parámetro se omite y la llamada a la función se comporta como [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="26317-119">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="26317-120">Si este parámetro es NULL o un cero MAPIUID, esta función se comporta como [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="26317-120">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="26317-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="26317-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="26317-122">[entrada] La libreta de direcciones que se usó para abrir el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="26317-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="26317-123">No puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="26317-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="26317-124">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="26317-124">_cbEntryID_</span></span>
  
> <span data-ttu-id="26317-125">[entrada] El número de bytes del identificador de entrada especificado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="26317-125">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="26317-126">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="26317-126">_lpEntryID_</span></span>
  
>  <span data-ttu-id="26317-127">[entrada] Un puntero al identificador de entrada que representa la entrada de la libreta de direcciones para abrir.</span><span class="sxs-lookup"><span data-stu-id="26317-127">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="26317-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="26317-128">_ulFlags_</span></span>
  
> <span data-ttu-id="26317-129">[entrada] Una máscara de bits de indicadores que controla cómo se abre la entrada.</span><span class="sxs-lookup"><span data-stu-id="26317-129">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="26317-130">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="26317-130">The following flags can be set:</span></span>
    
<span data-ttu-id="26317-131">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="26317-131">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="26317-132">Solicitudes que se abra la entrada con los permisos de red y cliente permitidos máximos.</span><span class="sxs-lookup"><span data-stu-id="26317-132">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="26317-133">Por ejemplo, si el cliente ha leído y permiso de escritura, el proveedor de la libreta de direcciones intenta abrir la entrada con la lectura y permiso de escritura.</span><span class="sxs-lookup"><span data-stu-id="26317-133">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="26317-134">El cliente puede recuperar el nivel de acceso que se ha concedido mediante una llamada al método [IMAPIProp::GetProps](imapiprop-getprops.md) de la entrada open y la recuperación de la propiedad PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="26317-134">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="26317-135">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="26317-135">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="26317-136">Utiliza sólo la libreta de direcciones sin conexión para llevar a cabo la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="26317-136">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="26317-137">Por ejemplo, puede usar esta marca para permitir que una aplicación cliente para abrir la lista global de direcciones (GAL) en el modo de intercambio en caché y obtener acceso a una entrada en esa libreta de direcciones de la memoria caché sin crear el tráfico entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="26317-137">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="26317-138">Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="26317-138">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="26317-139">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="26317-139">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="26317-140">Permite que la llamada se realice correctamente, potencialmente antes de la entrada es totalmente abiertos y disponibles, lo que implica que las llamadas posteriores a la entrada devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="26317-140">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="26317-141">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="26317-141">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="26317-142">Utiliza sólo la lista global de direcciones para llevar a cabo la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="26317-142">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="26317-143">Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="26317-143">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="26317-144">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="26317-144">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="26317-145">Las solicitudes que se abre la entrada con leer y permiso de escritura.</span><span class="sxs-lookup"><span data-stu-id="26317-145">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="26317-146">Debido a que las entradas se abren con acceso de solo lectura de forma predeterminada, los clientes no deben asumir que de lectura y escritura se ha concedido permiso, independientemente de si se ha establecido MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="26317-146">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="26317-147">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="26317-147">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="26317-148">No utiliza la libreta de direcciones sin conexión para llevar a cabo la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="26317-148">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="26317-149">Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="26317-149">This flag is supported only by the Exchange Address Book Provider.</span></span>
    

