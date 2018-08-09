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
ms.openlocfilehash: 0e39f4edc871b49675f1ffcc1bc541345c8829d5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817087"
---
# <a name="hropenabentrywithresolvedrow"></a><span data-ttu-id="38b09-103">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="38b09-103">HrOpenABEntryWithResolvedRow</span></span>

  
  
<span data-ttu-id="38b09-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="38b09-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="38b09-105">Realiza la misma función que [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) excepto en que obtiene el **emsabpUID** de la fila resuelta automáticamente y se abre la **propiedad entryID**.</span><span class="sxs-lookup"><span data-stu-id="38b09-105">Performs the same function as [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) except that it automatically gets the **emsabpUID** from the resolved row and opens the **entryID**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="38b09-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="38b09-106">Header file:</span></span>  <br/> |<span data-ttu-id="38b09-107">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="38b09-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="38b09-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="38b09-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="38b09-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="38b09-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="38b09-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="38b09-110">Called by:</span></span>  <br/> |<span data-ttu-id="38b09-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="38b09-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="38b09-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="38b09-112">Parameters</span></span>

 <span data-ttu-id="38b09-113">_prwResolved_</span><span class="sxs-lookup"><span data-stu-id="38b09-113">_prwResolved_</span></span>
  
> <span data-ttu-id="38b09-114">[entrada] Un puntero a la fila resuelta que se usa para obtener la **emsabpUID** y abra el **entryID**.</span><span class="sxs-lookup"><span data-stu-id="38b09-114">[in] A pointer to the resolved row that is used to get the **emsabpUID** and open the **entryID**.</span></span>
    
 <span data-ttu-id="38b09-115">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="38b09-115">_pAddrBook_</span></span>
  
> <span data-ttu-id="38b09-116">[entrada] La libreta de direcciones que se usó para abrir el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="38b09-116">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="38b09-117">No puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="38b09-117">It cannot be NULL.</span></span>
    
 <span data-ttu-id="38b09-118">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="38b09-118">_cbEntryID_</span></span>
  
> <span data-ttu-id="38b09-119">[entrada] El número de bytes del identificador de entrada especificado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="38b09-119">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="38b09-120">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="38b09-120">_lpEntryID_</span></span>
  
>  <span data-ttu-id="38b09-121">[entrada] Un puntero al identificador de entrada que representa la entrada de la libreta de direcciones para abrir.</span><span class="sxs-lookup"><span data-stu-id="38b09-121">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="38b09-122">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="38b09-122">_lpInterface_</span></span>
  
> <span data-ttu-id="38b09-123">[entrada] Un puntero al identificador de interfaz (IID) de la interfaz que se usa para tener acceso a la entrada open.</span><span class="sxs-lookup"><span data-stu-id="38b09-123">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="38b09-124">Pasando NULL, devuelve la interfaz estándar del objeto.</span><span class="sxs-lookup"><span data-stu-id="38b09-124">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="38b09-125">Para los usuarios de mensajería, es la interfaz estándar de [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="38b09-125">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="38b09-126">Para las listas de distribución, es [IDistList: IMAPIContainer](idistlistimapicontainer.md)y para contenedores, es [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="38b09-126">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md)and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="38b09-127">Los autores de llamadas pueden establecer _lpInterface_ en la interfaz estándar adecuada o una interfaz en la jerarquía de herencia.</span><span class="sxs-lookup"><span data-stu-id="38b09-127">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="38b09-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="38b09-128">_ulFlags_</span></span>
  
> <span data-ttu-id="38b09-129">[entrada] Una máscara de bits de indicadores que controla cómo se abre la entrada.</span><span class="sxs-lookup"><span data-stu-id="38b09-129">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="38b09-130">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="38b09-130">The following flags can be set:</span></span>
    
<span data-ttu-id="38b09-131">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="38b09-131">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="38b09-132">Solicitudes que se abra la entrada con los permisos de red y cliente permitidos máximos.</span><span class="sxs-lookup"><span data-stu-id="38b09-132">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="38b09-133">Por ejemplo, si el cliente ha leído y permiso de escritura, el proveedor de la libreta de direcciones intenta abrir la entrada con la lectura y permiso de escritura.</span><span class="sxs-lookup"><span data-stu-id="38b09-133">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="38b09-134">El cliente puede recuperar el nivel de acceso que se ha concedido mediante una llamada al método [IMAPIProp::GetProps](imapiprop-getprops.md) de la entrada open y la recuperación de la propiedad PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="38b09-134">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="38b09-135">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="38b09-135">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="38b09-136">Utiliza sólo la libreta de direcciones sin conexión para llevar a cabo la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="38b09-136">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="38b09-137">Por ejemplo, puede usar esta marca para permitir que una aplicación cliente para abrir la lista global de direcciones (GAL) en el modo de intercambio en caché y obtener acceso a una entrada en esa libreta de direcciones de la memoria caché sin crear el tráfico entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="38b09-137">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="38b09-138">Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="38b09-138">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="38b09-139">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="38b09-139">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="38b09-140">Permite que la llamada se realice correctamente, potencialmente antes de la entrada es totalmente abiertos y disponibles, lo que implica que las llamadas posteriores a la entrada devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="38b09-140">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="38b09-141">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="38b09-141">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="38b09-142">Utiliza sólo la lista global de direcciones para llevar a cabo la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="38b09-142">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="38b09-143">Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="38b09-143">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="38b09-144">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="38b09-144">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="38b09-145">Las solicitudes que se abre la entrada con leer y permiso de escritura.</span><span class="sxs-lookup"><span data-stu-id="38b09-145">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="38b09-146">Debido a que las entradas se abren con acceso de solo lectura de forma predeterminada, los clientes no deben asumir que de lectura y escritura se ha concedido permiso, independientemente de si se ha establecido MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="38b09-146">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="38b09-147">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="38b09-147">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="38b09-148">No utiliza la libreta de direcciones sin conexión para llevar a cabo la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="38b09-148">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="38b09-149">Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="38b09-149">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="38b09-150">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="38b09-150">_lpulObjType_</span></span>
  
> <span data-ttu-id="38b09-151">[out] Un puntero al tipo de la entrada que se abrió.</span><span class="sxs-lookup"><span data-stu-id="38b09-151">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="38b09-152">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="38b09-152">_lppUnk_</span></span>
  
> <span data-ttu-id="38b09-153">[out] Un puntero a un puntero de la entrada que se abrió.</span><span class="sxs-lookup"><span data-stu-id="38b09-153">[out] A pointer to a pointer of the opened entry.</span></span>
    

