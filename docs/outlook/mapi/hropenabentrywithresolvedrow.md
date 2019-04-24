---
title: HrOpenABEntryWithResolvedRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ce3a583c-16a9-4268-9476-926d2780eae5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2eb643e0002e2159e3197d66e021aba0bb8c126f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347778"
---
# <a name="hropenabentrywithresolvedrow"></a><span data-ttu-id="d3631-103">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="d3631-103">HrOpenABEntryWithResolvedRow</span></span>

  
  
<span data-ttu-id="d3631-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3631-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3631-105">Realiza la misma función que [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) , con la diferencia de que obtiene automáticamente el **emsabpUID** de la fila resuelta y abre el **entryID**.</span><span class="sxs-lookup"><span data-stu-id="d3631-105">Performs the same function as [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) except that it automatically gets the **emsabpUID** from the resolved row and opens the **entryID**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d3631-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d3631-106">Header file:</span></span>  <br/> |<span data-ttu-id="d3631-107">abhelp. h</span><span class="sxs-lookup"><span data-stu-id="d3631-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="d3631-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="d3631-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d3631-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d3631-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d3631-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="d3631-110">Called by:</span></span>  <br/> |<span data-ttu-id="d3631-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="d3631-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithResolvedRow(
  LPSRow prwResolved,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="d3631-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="d3631-112">Parameters</span></span>

 <span data-ttu-id="d3631-113">_prwResolved_</span><span class="sxs-lookup"><span data-stu-id="d3631-113">_prwResolved_</span></span>
  
> <span data-ttu-id="d3631-114">a Un puntero a la fila resuelta que se usa para obtener la **emsabpUID** y abrir la **entryID**.</span><span class="sxs-lookup"><span data-stu-id="d3631-114">[in] A pointer to the resolved row that is used to get the **emsabpUID** and open the **entryID**.</span></span>
    
 <span data-ttu-id="d3631-115">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="d3631-115">_pAddrBook_</span></span>
  
> <span data-ttu-id="d3631-116">a La libreta de direcciones que se usa para abrir el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="d3631-116">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="d3631-117">No puede ser nulo.</span><span class="sxs-lookup"><span data-stu-id="d3631-117">It cannot be NULL.</span></span>
    
 <span data-ttu-id="d3631-118">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="d3631-118">_cbEntryID_</span></span>
  
> <span data-ttu-id="d3631-119">a El recuento de bytes del identificador de entrada especificado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="d3631-119">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="d3631-120">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="d3631-120">_lpEntryID_</span></span>
  
>  <span data-ttu-id="d3631-121">a Un puntero al identificador de entrada que representa la entrada de la libreta de direcciones que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="d3631-121">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="d3631-122">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="d3631-122">_lpInterface_</span></span>
  
> <span data-ttu-id="d3631-123">a Un puntero al identificador de interfaz (IID) de la interfaz que se usa para obtener acceso a la entrada abierta.</span><span class="sxs-lookup"><span data-stu-id="d3631-123">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="d3631-124">Al pasar NULL, se devuelve la interfaz estándar del objeto.</span><span class="sxs-lookup"><span data-stu-id="d3631-124">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="d3631-125">Para los usuarios de mensajería, la interfaz estándar es [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="d3631-125">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="d3631-126">Para las listas de distribución, es [IDistList: IMAPIContainer](idistlistimapicontainer.md)y para contenedores, es [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="d3631-126">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md)and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="d3631-127">Los autores de llamadas pueden establecer _lpInterface_ en la interfaz estándar adecuada o en una interfaz de la jerarquía de herencia.</span><span class="sxs-lookup"><span data-stu-id="d3631-127">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="d3631-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d3631-128">_ulFlags_</span></span>
  
> <span data-ttu-id="d3631-129">a Máscara de máscara de marcadores que controla cómo se abre la entrada.</span><span class="sxs-lookup"><span data-stu-id="d3631-129">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="d3631-130">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="d3631-130">The following flags can be set:</span></span>
    
<span data-ttu-id="d3631-131">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="d3631-131">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="d3631-132">Solicita que se abra la entrada con los permisos de red y de cliente máximos permitidos.</span><span class="sxs-lookup"><span data-stu-id="d3631-132">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="d3631-133">Por ejemplo, si el cliente tiene permiso de lectura y escritura, el proveedor de la libreta de direcciones intenta abrir la entrada con permisos de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d3631-133">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="d3631-134">El cliente puede recuperar el nivel de acceso que se ha concedido al llamar al método [IMAPIProp:: GetProps](imapiprop-getprops.md) de la entrada abierta y recuperar la propiedad PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="d3631-134">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="d3631-135">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="d3631-135">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="d3631-136">Usa sólo la libreta de direcciones sin conexión para realizar la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="d3631-136">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="d3631-137">Por ejemplo, puede usar esta marca para permitir que una aplicación cliente Abra la lista global de direcciones (GAL) en el modo caché de Exchange y obtenga acceso a una entrada de la libreta de direcciones desde la memoria caché sin crear tráfico entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="d3631-137">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="d3631-138">Este indicador solo es compatible con el proveedor de libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d3631-138">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="d3631-139">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="d3631-139">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="d3631-140">Permite que la llamada se realice correctamente, potencialmente antes de que la entrada esté completamente abierta y disponible, lo que implica que las llamadas posteriores a la entrada puedan devolver un error.</span><span class="sxs-lookup"><span data-stu-id="d3631-140">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="d3631-141">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="d3631-141">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="d3631-142">Usa sólo la GAL para la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="d3631-142">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="d3631-143">Este indicador solo es compatible con el proveedor de libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d3631-143">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="d3631-144">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="d3631-144">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="d3631-145">Solicita que la entrada se abra con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d3631-145">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="d3631-146">Debido a que las entradas se abren con acceso de solo lectura de forma predeterminada, los clientes no deben dar por supuesto que el permiso de lectura y escritura se concedió independientemente de si se ha establecido MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="d3631-146">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="d3631-147">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="d3631-147">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="d3631-148">No usa la libreta de direcciones sin conexión para realizar la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="d3631-148">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="d3631-149">Este indicador solo es compatible con el proveedor de libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d3631-149">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="d3631-150">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="d3631-150">_lpulObjType_</span></span>
  
> <span data-ttu-id="d3631-151">contempla Puntero al tipo de la entrada abierta.</span><span class="sxs-lookup"><span data-stu-id="d3631-151">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="d3631-152">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="d3631-152">_lppUnk_</span></span>
  
> <span data-ttu-id="d3631-153">contempla Un puntero a un puntero de la entrada abierta.</span><span class="sxs-lookup"><span data-stu-id="d3631-153">[out] A pointer to a pointer of the opened entry.</span></span>
    

