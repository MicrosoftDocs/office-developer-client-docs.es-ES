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
# <a name="hropenabentrywithprovideruid"></a><span data-ttu-id="d8205-103">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="d8205-103">HrOpenABEntryWithProviderUID</span></span>

  
  
<span data-ttu-id="d8205-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8205-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8205-105">Abre el **entryID** mediante la libreta de direcciones de Exchange identificada por _pEmsabpUID_.</span><span class="sxs-lookup"><span data-stu-id="d8205-105">Opens the **entryID** using the Exchange Address Book identified by  _pEmsabpUID_.</span></span> <span data-ttu-id="d8205-106">Esta función funciona de manera similar a [IAddrBook:: OpenEntry](iaddrbook-openentry.md) , excepto en que el uso de esta función garantiza que [IAddrBook:: OpenEntry](iaddrbook-openentry.md) se abre usando el proveedor de libreta de direcciones de Exchange esperado.</span><span class="sxs-lookup"><span data-stu-id="d8205-106">This function works similarly to [IAddrBook::OpenEntry](iaddrbook-openentry.md) except that using this function ensures that [IAddrBook::OpenEntry](iaddrbook-openentry.md) is opened by using the expected Exchange Address Book provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d8205-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d8205-107">Header file:</span></span>  <br/> |<span data-ttu-id="d8205-108">abhelp. h</span><span class="sxs-lookup"><span data-stu-id="d8205-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="d8205-109">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="d8205-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="d8205-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="d8205-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="d8205-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="d8205-111">Called by:</span></span>  <br/> |<span data-ttu-id="d8205-112">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="d8205-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="d8205-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="d8205-113">Parameters</span></span>

 <span data-ttu-id="d8205-114">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="d8205-114">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="d8205-115">a Un puntero a una **emsmdbUID** que identifica el servicio de Exchange que contiene el proveedor de la libreta de direcciones de Exchange que esta función debe usar para mostrar detalles sobre el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="d8205-115">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="d8205-116">Si el identificador de entrada entrante no es un identificador de entrada de proveedor de libreta de direcciones de Exchange, se omite este parámetro y la llamada a la función se comporta como [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="d8205-116">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="d8205-117">Si este parámetro es NULL o un MAPIUID cero, esta función se comporta como [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="d8205-117">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="d8205-118">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="d8205-118">_pAddrBook_</span></span>
  
> <span data-ttu-id="d8205-119">a La libreta de direcciones que se usa para abrir el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="d8205-119">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="d8205-120">No puede ser nulo.</span><span class="sxs-lookup"><span data-stu-id="d8205-120">It cannot be NULL.</span></span>
    
 <span data-ttu-id="d8205-121">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="d8205-121">_cbEntryID_</span></span>
  
> <span data-ttu-id="d8205-122">a El recuento de bytes del identificador de entrada especificado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="d8205-122">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="d8205-123">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="d8205-123">_lpEntryID_</span></span>
  
>  <span data-ttu-id="d8205-124">a Un puntero al identificador de entrada que representa la entrada de la libreta de direcciones que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="d8205-124">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="d8205-125">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="d8205-125">_lpInterface_</span></span>
  
> <span data-ttu-id="d8205-126">a Un puntero al identificador de interfaz (IID) de la interfaz que se usa para obtener acceso a la entrada abierta.</span><span class="sxs-lookup"><span data-stu-id="d8205-126">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="d8205-127">Al pasar NULL, se devuelve la interfaz estándar del objeto.</span><span class="sxs-lookup"><span data-stu-id="d8205-127">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="d8205-128">Para los usuarios de mensajería, la interfaz estándar es [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="d8205-128">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="d8205-129">Para las listas de distribución, es [IDistList: IMAPIContainer](idistlistimapicontainer.md)y para contenedores, es [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="d8205-129">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md)and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="d8205-130">Los autores de llamadas pueden establecer _lpInterface_ en la interfaz estándar adecuada o en una interfaz de la jerarquía de herencia.</span><span class="sxs-lookup"><span data-stu-id="d8205-130">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="d8205-131">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d8205-131">_ulFlags_</span></span>
  
> <span data-ttu-id="d8205-132">a Una máscara de máscara de marcadores que controla cómo se abre la entrada, se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="d8205-132">[in] A bitmask of flags that controls the how the entry is opened, The following flags can be set:</span></span>
    
<span data-ttu-id="d8205-133">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="d8205-133">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="d8205-134">Solicita que se abra la entrada con los permisos de red y de cliente máximos permitidos.</span><span class="sxs-lookup"><span data-stu-id="d8205-134">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="d8205-135">Por ejemplo, si el cliente tiene permiso de lectura y escritura, el proveedor de la libreta de direcciones intenta abrir la entrada con permisos de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d8205-135">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="d8205-136">El cliente puede recuperar el nivel de acceso que se ha concedido al llamar al método [IMAPIProp:: GetProps](imapiprop-getprops.md) de la entrada abierta y recuperar la propiedad PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="d8205-136">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="d8205-137">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="d8205-137">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="d8205-138">Use solo la libreta de direcciones sin conexión para realizar la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="d8205-138">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="d8205-139">Por ejemplo, puede usar esta marca para permitir que una aplicación cliente Abra la lista global de direcciones (GAL) en el modo caché de Exchange y obtenga acceso a una entrada de la libreta de direcciones desde la memoria caché sin crear tráfico entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="d8205-139">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="d8205-140">Este indicador solo es compatible con el proveedor de libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d8205-140">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="d8205-141">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="d8205-141">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="d8205-142">Permite que la llamada se realice correctamente, potencialmente antes de que la entrada esté completamente abierta y disponible, lo que implica que las llamadas posteriores a la entrada puedan devolver un error.</span><span class="sxs-lookup"><span data-stu-id="d8205-142">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="d8205-143">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="d8205-143">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="d8205-144">Use solamente la GAL para la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="d8205-144">Use only the GAL to perform name resolution.</span></span> <span data-ttu-id="d8205-145">Este indicador solo es compatible con el proveedor de libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d8205-145">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="d8205-146">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="d8205-146">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="d8205-147">Solicita que la entrada se abra con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d8205-147">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="d8205-148">Debido a que las entradas se abren con acceso de solo lectura de forma predeterminada, los clientes no deben dar por supuesto que el permiso de lectura y escritura se concedió independientemente de si se ha establecido MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="d8205-148">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="d8205-149">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="d8205-149">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="d8205-150">No use la libreta de direcciones sin conexión para realizar la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="d8205-150">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="d8205-151">Este indicador solo es compatible con el proveedor de libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d8205-151">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="d8205-152">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="d8205-152">_lpulObjType_</span></span>
  
> <span data-ttu-id="d8205-153">contempla Puntero al tipo de la entrada abierta.</span><span class="sxs-lookup"><span data-stu-id="d8205-153">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="d8205-154">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="d8205-154">_lppUnk_</span></span>
  
> <span data-ttu-id="d8205-155">contempla Un puntero a un puntero de la entrada abierta.</span><span class="sxs-lookup"><span data-stu-id="d8205-155">[out] A pointer to a pointer of the opened entry.</span></span>
    

