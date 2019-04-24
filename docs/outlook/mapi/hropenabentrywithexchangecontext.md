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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347792"
---
# <a name="hropenabentrywithexchangecontext"></a><span data-ttu-id="d0ccd-103">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="d0ccd-103">HrOpenABEntryWithExchangeContext</span></span>

  
  
<span data-ttu-id="d0ccd-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0ccd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0ccd-105">Abre el **entryID** mediante la libreta de direcciones de Exchange identificada por **pEmsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="d0ccd-105">Opens the **entryID** using the Exchange Address Book identified by **pEmsmdbUID**.</span></span> <span data-ttu-id="d0ccd-106">Esta función funciona de manera similar a [IAddrBook::D etails](iaddrbook-details.md) , excepto que el uso de esta función garantiza que [IAddrBook:: OpenEntry](iaddrbook-openentry.md) se abre usando el proveedor de libreta de direcciones de Exchange esperado.</span><span class="sxs-lookup"><span data-stu-id="d0ccd-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md) except that using this function ensures that the [IAddrBook::OpenEntry](iaddrbook-openentry.md) is opened by using the expected Exchange Address Book Provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d0ccd-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d0ccd-107">Header file:</span></span>  <br/> |<span data-ttu-id="d0ccd-108">abhelp. h</span><span class="sxs-lookup"><span data-stu-id="d0ccd-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="d0ccd-109">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="d0ccd-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="d0ccd-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="d0ccd-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="d0ccd-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="d0ccd-111">Called by:</span></span>  <br/> |<span data-ttu-id="d0ccd-112">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="d0ccd-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="d0ccd-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="d0ccd-113">Parameters</span></span>

 <span data-ttu-id="d0ccd-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="d0ccd-114">_pmsess_</span></span>
  
> <span data-ttu-id="d0ccd-115">a La sesión iniciada en **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="d0ccd-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="d0ccd-116">No puede ser nulo.</span><span class="sxs-lookup"><span data-stu-id="d0ccd-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="d0ccd-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="d0ccd-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="d0ccd-118">a Un puntero a una **emsmdbUID** que identifica el servicio de Exchange que contiene el proveedor de la libreta de direcciones de Exchange que esta función debe usar para mostrar detalles sobre el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="d0ccd-118">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="d0ccd-119">Si el identificador de entrada entrante no es un identificador de entrada de proveedor de libreta de direcciones de Exchange, se omite este parámetro y la llamada a la función se comporta como [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="d0ccd-119">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="d0ccd-120">Si este parámetro es NULL o un MAPIUID cero, esta función se comporta como [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="d0ccd-120">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="d0ccd-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="d0ccd-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="d0ccd-122">a La libreta de direcciones que se usa para abrir el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="d0ccd-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="d0ccd-123">No puede ser nulo.</span><span class="sxs-lookup"><span data-stu-id="d0ccd-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="d0ccd-124">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="d0ccd-124">_cbEntryID_</span></span>
  
> <span data-ttu-id="d0ccd-125">a El recuento de bytes del identificador de entrada especificado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="d0ccd-125">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="d0ccd-126">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="d0ccd-126">_lpEntryID_</span></span>
  
>  <span data-ttu-id="d0ccd-127">a Un puntero al identificador de entrada que representa la entrada de la libreta de direcciones que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="d0ccd-127">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="d0ccd-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d0ccd-128">_ulFlags_</span></span>
  
> <span data-ttu-id="d0ccd-129">a Máscara de máscara de marcadores que controla cómo se abre la entrada.</span><span class="sxs-lookup"><span data-stu-id="d0ccd-129">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="d0ccd-130">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="d0ccd-130">The following flags can be set:</span></span>
    
<span data-ttu-id="d0ccd-131">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="d0ccd-131">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="d0ccd-132">Solicita que se abra la entrada con los permisos de red y de cliente máximos permitidos.</span><span class="sxs-lookup"><span data-stu-id="d0ccd-132">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="d0ccd-133">Por ejemplo, si el cliente tiene permiso de lectura y escritura, el proveedor de la libreta de direcciones intenta abrir la entrada con permisos de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d0ccd-133">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="d0ccd-134">El cliente puede recuperar el nivel de acceso que se ha concedido al llamar al método [IMAPIProp:: GetProps](imapiprop-getprops.md) de la entrada abierta y recuperar la propiedad PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="d0ccd-134">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="d0ccd-135">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="d0ccd-135">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="d0ccd-136">Usa sólo la libreta de direcciones sin conexión para realizar la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="d0ccd-136">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="d0ccd-137">Por ejemplo, puede usar esta marca para permitir que una aplicación cliente Abra la lista global de direcciones (GAL) en el modo caché de Exchange y obtenga acceso a una entrada de la libreta de direcciones desde la memoria caché sin crear tráfico entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="d0ccd-137">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="d0ccd-138">Este indicador solo es compatible con el proveedor de libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d0ccd-138">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="d0ccd-139">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="d0ccd-139">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="d0ccd-140">Permite que la llamada se realice correctamente, potencialmente antes de que la entrada esté completamente abierta y disponible, lo que implica que las llamadas posteriores a la entrada puedan devolver un error.</span><span class="sxs-lookup"><span data-stu-id="d0ccd-140">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="d0ccd-141">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="d0ccd-141">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="d0ccd-142">Usa sólo la GAL para la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="d0ccd-142">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="d0ccd-143">Este indicador solo es compatible con el proveedor de libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d0ccd-143">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="d0ccd-144">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="d0ccd-144">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="d0ccd-145">Solicita que la entrada se abra con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d0ccd-145">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="d0ccd-146">Debido a que las entradas se abren con acceso de solo lectura de forma predeterminada, los clientes no deben dar por supuesto que el permiso de lectura y escritura se concedió independientemente de si se ha establecido MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="d0ccd-146">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="d0ccd-147">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="d0ccd-147">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="d0ccd-148">No usa la libreta de direcciones sin conexión para realizar la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="d0ccd-148">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="d0ccd-149">Este indicador solo es compatible con el proveedor de libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d0ccd-149">This flag is supported only by the Exchange Address Book Provider.</span></span>
    

