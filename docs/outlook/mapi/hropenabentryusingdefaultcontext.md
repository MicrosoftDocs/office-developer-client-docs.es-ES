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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347827"
---
# <a name="hropenabentryusingdefaultcontext"></a><span data-ttu-id="5c1ca-103">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="5c1ca-103">HrOpenABEntryUsingDefaultContext</span></span>

  
  
<span data-ttu-id="5c1ca-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c1ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c1ca-105">Realiza la misma función que [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) , excepto que usa la **emsmdbUID** heredada como el parámetro _pEmsmdbUID_ .</span><span class="sxs-lookup"><span data-stu-id="5c1ca-105">Performs the same function as [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) except that it uses the legacy **emsmdbUID** as the  _pEmsmdbUID_ parameter.</span></span> <span data-ttu-id="5c1ca-106">No use esta función a menos que no pueda obtener el **emsmdbUID** correcto para la llamada a [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md).</span><span class="sxs-lookup"><span data-stu-id="5c1ca-106">Do not use this function unless you cannot obtain the correct **emsmdbUID** for the call to [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5c1ca-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="5c1ca-107">Header file:</span></span>  <br/> |<span data-ttu-id="5c1ca-108">abhelp. h</span><span class="sxs-lookup"><span data-stu-id="5c1ca-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="5c1ca-109">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="5c1ca-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="5c1ca-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="5c1ca-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="5c1ca-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="5c1ca-111">Called by:</span></span>  <br/> |<span data-ttu-id="5c1ca-112">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="5c1ca-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="5c1ca-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="5c1ca-113">Parameters</span></span>

 <span data-ttu-id="5c1ca-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="5c1ca-114">_pmsess_</span></span>
  
> <span data-ttu-id="5c1ca-115">a La sesión iniciada en **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="5c1ca-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="5c1ca-116">No puede ser nulo.</span><span class="sxs-lookup"><span data-stu-id="5c1ca-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="5c1ca-117">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="5c1ca-117">_pAddrBook_</span></span>
  
> <span data-ttu-id="5c1ca-118">a La libreta de direcciones que se usa para abrir el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="5c1ca-118">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="5c1ca-119">No puede ser nulo.</span><span class="sxs-lookup"><span data-stu-id="5c1ca-119">It cannot be NULL.</span></span>
    
 <span data-ttu-id="5c1ca-120">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="5c1ca-120">_cbEntryID_</span></span>
  
> <span data-ttu-id="5c1ca-121">a El recuento de bytes del identificador de entrada especificado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="5c1ca-121">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="5c1ca-122">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="5c1ca-122">_lpEntryID_</span></span>
  
>  <span data-ttu-id="5c1ca-123">a Un puntero al identificador de entrada que representa la entrada de la libreta de direcciones que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="5c1ca-123">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="5c1ca-124">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="5c1ca-124">_lpInterface_</span></span>
  
> <span data-ttu-id="5c1ca-125">a Un puntero al identificador de interfaz (IID) de la interfaz que se usa para obtener acceso a la entrada abierta.</span><span class="sxs-lookup"><span data-stu-id="5c1ca-125">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="5c1ca-126">Al pasar NULL, se devuelve la interfaz estándar del objeto.</span><span class="sxs-lookup"><span data-stu-id="5c1ca-126">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="5c1ca-127">Para los usuarios de mensajería, la interfaz estándar es [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="5c1ca-127">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="5c1ca-128">Para las listas de distribución es [IDistList: IMAPIContainer](idistlistimapicontainer.md)y, para los contenedores, es [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="5c1ca-128">For distribution lists it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="5c1ca-129">Los autores de llamadas pueden establecer _lpInterface_ en la interfaz estándar adecuada o en una interfaz de la jerarquía de herencia.</span><span class="sxs-lookup"><span data-stu-id="5c1ca-129">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="5c1ca-130">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5c1ca-130">_ulFlags_</span></span>
  
> <span data-ttu-id="5c1ca-131">a Máscara de máscara de marcadores que controla cómo se abre la entrada.</span><span class="sxs-lookup"><span data-stu-id="5c1ca-131">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="5c1ca-132">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="5c1ca-132">The following flags can be set:</span></span>
    
<span data-ttu-id="5c1ca-133">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="5c1ca-133">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="5c1ca-134">Solicita que se abra la entrada con los permisos de red y de cliente máximos permitidos.</span><span class="sxs-lookup"><span data-stu-id="5c1ca-134">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="5c1ca-135">Por ejemplo, si el cliente tiene permiso de lectura y escritura, el proveedor de la libreta de direcciones intenta abrir la entrada con permisos de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="5c1ca-135">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="5c1ca-136">El cliente puede recuperar el nivel de acceso que se ha concedido al llamar al método [IMAPIProp:: GetProps](imapiprop-getprops.md) de la entrada abierta y recuperar la propiedad PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="5c1ca-136">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="5c1ca-137">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="5c1ca-137">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="5c1ca-138">Usa sólo la libreta de direcciones sin conexión para realizar la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="5c1ca-138">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="5c1ca-139">Por ejemplo, puede usar esta marca para permitir que una aplicación cliente Abra la lista global de direcciones (GAL) en el modo caché de Exchange y obtenga acceso a una entrada de la libreta de direcciones desde la memoria caché sin crear tráfico entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="5c1ca-139">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="5c1ca-140">Este indicador solo es compatible con el proveedor de libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5c1ca-140">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="5c1ca-141">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="5c1ca-141">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="5c1ca-142">Permite que la llamada se realice correctamente, potencialmente antes de que la entrada esté completamente abierta y disponible, lo que implica que las llamadas posteriores a la entrada puedan devolver un error.</span><span class="sxs-lookup"><span data-stu-id="5c1ca-142">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="5c1ca-143">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="5c1ca-143">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="5c1ca-144">Usa sólo la GAL para la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="5c1ca-144">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="5c1ca-145">Este indicador solo es compatible con el proveedor de libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5c1ca-145">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="5c1ca-146">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="5c1ca-146">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="5c1ca-147">Solicita que la entrada se abra con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="5c1ca-147">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="5c1ca-148">Debido a que las entradas se abren con acceso de solo lectura de forma predeterminada, los clientes no deben dar por supuesto que el permiso de lectura y escritura se concedió independientemente de si se ha establecido MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="5c1ca-148">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="5c1ca-149">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="5c1ca-149">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="5c1ca-150">No usa la libreta de direcciones sin conexión para realizar la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="5c1ca-150">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="5c1ca-151">Este indicador solo es compatible con el proveedor de libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5c1ca-151">This flag is supported only by the Exchange address book provider.</span></span>
    
 <span data-ttu-id="5c1ca-152">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="5c1ca-152">_lpulObjType_</span></span>
  
> <span data-ttu-id="5c1ca-153">contempla Puntero al tipo de la entrada abierta.</span><span class="sxs-lookup"><span data-stu-id="5c1ca-153">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="5c1ca-154">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="5c1ca-154">_lppUnk_</span></span>
  
> <span data-ttu-id="5c1ca-155">contempla Un puntero a un puntero de la entrada abierta.</span><span class="sxs-lookup"><span data-stu-id="5c1ca-155">[out] A pointer to a pointer of the opened entry.</span></span>
    

