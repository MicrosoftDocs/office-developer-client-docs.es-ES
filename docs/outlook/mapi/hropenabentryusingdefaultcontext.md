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
ms.openlocfilehash: 879ba4afe85e1f6db31bd829411689b2dad58ed9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565469"
---
# <a name="hropenabentryusingdefaultcontext"></a><span data-ttu-id="40a36-103">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="40a36-103">HrOpenABEntryUsingDefaultContext</span></span>

  
  
<span data-ttu-id="40a36-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40a36-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40a36-105">Realiza la misma función que [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) excepto en que utiliza el heredado **emsmdbUID** como el parámetro _pEmsmdbUID_ .</span><span class="sxs-lookup"><span data-stu-id="40a36-105">Performs the same function as [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) except that it uses the legacy **emsmdbUID** as the  _pEmsmdbUID_ parameter.</span></span> <span data-ttu-id="40a36-106">No utilice esta función, a menos que no se puede obtener la correcta **emsmdbUID** para la llamada a [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md).</span><span class="sxs-lookup"><span data-stu-id="40a36-106">Do not use this function unless you cannot obtain the correct **emsmdbUID** for the call to [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="40a36-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="40a36-107">Header file:</span></span>  <br/> |<span data-ttu-id="40a36-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="40a36-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="40a36-109">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="40a36-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="40a36-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="40a36-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="40a36-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="40a36-111">Called by:</span></span>  <br/> |<span data-ttu-id="40a36-112">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="40a36-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="40a36-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="40a36-113">Parameters</span></span>

 <span data-ttu-id="40a36-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="40a36-114">_pmsess_</span></span>
  
> <span data-ttu-id="40a36-115">[entrada] La ha iniciado la sesión **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="40a36-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="40a36-116">No puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="40a36-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="40a36-117">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="40a36-117">_pAddrBook_</span></span>
  
> <span data-ttu-id="40a36-118">[entrada] La libreta de direcciones que se usó para abrir el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="40a36-118">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="40a36-119">No puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="40a36-119">It cannot be NULL.</span></span>
    
 <span data-ttu-id="40a36-120">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="40a36-120">_cbEntryID_</span></span>
  
> <span data-ttu-id="40a36-121">[entrada] El número de bytes del identificador de entrada especificado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="40a36-121">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="40a36-122">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="40a36-122">_lpEntryID_</span></span>
  
>  <span data-ttu-id="40a36-123">[entrada] Un puntero al identificador de entrada que representa la entrada de la libreta de direcciones para abrir.</span><span class="sxs-lookup"><span data-stu-id="40a36-123">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="40a36-124">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="40a36-124">_lpInterface_</span></span>
  
> <span data-ttu-id="40a36-125">[entrada] Un puntero al identificador de interfaz (IID) de la interfaz que se usa para tener acceso a la entrada open.</span><span class="sxs-lookup"><span data-stu-id="40a36-125">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="40a36-126">Pasando NULL, devuelve la interfaz estándar del objeto.</span><span class="sxs-lookup"><span data-stu-id="40a36-126">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="40a36-127">Para los usuarios de mensajería, es la interfaz estándar de [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="40a36-127">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="40a36-128">Para las listas de distribución es [IDistList: IMAPIContainer](idistlistimapicontainer.md)y de los contenedores es [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="40a36-128">For distribution lists it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="40a36-129">Los autores de llamadas pueden establecer _lpInterface_ en la interfaz estándar adecuada o una interfaz en la jerarquía de herencia.</span><span class="sxs-lookup"><span data-stu-id="40a36-129">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="40a36-130">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="40a36-130">_ulFlags_</span></span>
  
> <span data-ttu-id="40a36-131">[entrada] Una máscara de bits de indicadores que controla cómo se abre la entrada.</span><span class="sxs-lookup"><span data-stu-id="40a36-131">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="40a36-132">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="40a36-132">The following flags can be set:</span></span>
    
<span data-ttu-id="40a36-133">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="40a36-133">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="40a36-134">Solicitudes que se abra la entrada con los permisos de red y cliente permitidos máximos.</span><span class="sxs-lookup"><span data-stu-id="40a36-134">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="40a36-135">Por ejemplo, si el cliente ha leído y permiso de escritura, el proveedor de la libreta de direcciones intenta abrir la entrada con la lectura y permiso de escritura.</span><span class="sxs-lookup"><span data-stu-id="40a36-135">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="40a36-136">El cliente puede recuperar el nivel de acceso que se ha concedido mediante una llamada al método [IMAPIProp::GetProps](imapiprop-getprops.md) de la entrada open y la recuperación de la propiedad PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="40a36-136">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="40a36-137">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="40a36-137">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="40a36-138">Utiliza sólo la libreta de direcciones sin conexión para llevar a cabo la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="40a36-138">Uses only the offline address book to perform name resolution.</span></span> <span data-ttu-id="40a36-139">Por ejemplo, puede usar esta marca para permitir que una aplicación cliente para abrir la lista global de direcciones (GAL) en el modo de intercambio en caché y obtener acceso a una entrada en esa libreta de direcciones de la memoria caché sin crear el tráfico entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="40a36-139">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="40a36-140">Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="40a36-140">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="40a36-141">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="40a36-141">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="40a36-142">Permite que la llamada se realice correctamente, potencialmente antes de la entrada es totalmente abiertos y disponibles, lo que implica que las llamadas posteriores a la entrada devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="40a36-142">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="40a36-143">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="40a36-143">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="40a36-144">Utiliza sólo la lista global de direcciones para llevar a cabo la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="40a36-144">Uses only the GAL to perform name resolution.</span></span> <span data-ttu-id="40a36-145">Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="40a36-145">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="40a36-146">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="40a36-146">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="40a36-147">Las solicitudes que se abre la entrada con leer y permiso de escritura.</span><span class="sxs-lookup"><span data-stu-id="40a36-147">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="40a36-148">Debido a que las entradas se abren con acceso de solo lectura de forma predeterminada, los clientes no deben asumir que de lectura y escritura se ha concedido permiso, independientemente de si se ha establecido MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="40a36-148">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="40a36-149">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="40a36-149">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="40a36-150">No utiliza la libreta de direcciones sin conexión para llevar a cabo la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="40a36-150">Does not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="40a36-151">Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="40a36-151">This flag is supported only by the Exchange address book provider.</span></span>
    
 <span data-ttu-id="40a36-152">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="40a36-152">_lpulObjType_</span></span>
  
> <span data-ttu-id="40a36-153">[out] Un puntero al tipo de la entrada que se abrió.</span><span class="sxs-lookup"><span data-stu-id="40a36-153">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="40a36-154">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="40a36-154">_lppUnk_</span></span>
  
> <span data-ttu-id="40a36-155">[out] Un puntero a un puntero de la entrada que se abrió.</span><span class="sxs-lookup"><span data-stu-id="40a36-155">[out] A pointer to a pointer of the opened entry.</span></span>
    

