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
ms.openlocfilehash: e33e656e70802437ab8b8717c5e175e2a13e384e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817057"
---
# <a name="hropenabentrywithprovideruid"></a><span data-ttu-id="9d744-103">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="9d744-103">HrOpenABEntryWithProviderUID</span></span>

  
  
<span data-ttu-id="9d744-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9d744-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9d744-105">Se abre la **propiedad entryID** utilizando la libreta de direcciones de Exchange identificado por _pEmsabpUID_.</span><span class="sxs-lookup"><span data-stu-id="9d744-105">Opens the **entryID** using the Exchange Address Book identified by  _pEmsabpUID_.</span></span> <span data-ttu-id="9d744-106">Esta función funciona de manera similar a [IAddrBook::OpenEntry](iaddrbook-openentry.md) excepto en que el uso de esta función garantiza que [IAddrBook::OpenEntry](iaddrbook-openentry.md) se abre mediante el proveedor de la libreta de direcciones de Exchange esperado.</span><span class="sxs-lookup"><span data-stu-id="9d744-106">This function works similarly to [IAddrBook::OpenEntry](iaddrbook-openentry.md) except that using this function ensures that [IAddrBook::OpenEntry](iaddrbook-openentry.md) is opened by using the expected Exchange Address Book provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9d744-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="9d744-107">Header file:</span></span>  <br/> |<span data-ttu-id="9d744-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="9d744-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="9d744-109">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="9d744-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="9d744-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="9d744-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="9d744-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="9d744-111">Called by:</span></span>  <br/> |<span data-ttu-id="9d744-112">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="9d744-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="9d744-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9d744-113">Parameters</span></span>

 <span data-ttu-id="9d744-114">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="9d744-114">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="9d744-115">[entrada] Un puntero a un **emsmdbUID** que identifica el servicio de Exchange que contiene el proveedor de libreta de direcciones de Exchange que se debe usar esta función para mostrar los detalles en el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="9d744-115">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="9d744-116">Si el identificador de entrada entrante no es un identificador de entrada del proveedor de libreta de direcciones de Exchange, este parámetro se omite y la llamada a la función se comporta como [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="9d744-116">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="9d744-117">Si este parámetro es NULL o un cero MAPIUID, esta función se comporta como [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="9d744-117">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="9d744-118">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="9d744-118">_pAddrBook_</span></span>
  
> <span data-ttu-id="9d744-119">[entrada] La libreta de direcciones que se usó para abrir el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="9d744-119">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="9d744-120">No puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="9d744-120">It cannot be NULL.</span></span>
    
 <span data-ttu-id="9d744-121">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="9d744-121">_cbEntryID_</span></span>
  
> <span data-ttu-id="9d744-122">[entrada] El número de bytes del identificador de entrada especificado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="9d744-122">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="9d744-123">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="9d744-123">_lpEntryID_</span></span>
  
>  <span data-ttu-id="9d744-124">[entrada] Un puntero al identificador de entrada que representa la entrada de la libreta de direcciones para abrir.</span><span class="sxs-lookup"><span data-stu-id="9d744-124">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span> 
    
 <span data-ttu-id="9d744-125">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="9d744-125">_lpInterface_</span></span>
  
> <span data-ttu-id="9d744-126">[entrada] Un puntero al identificador de interfaz (IID) de la interfaz que se usa para tener acceso a la entrada open.</span><span class="sxs-lookup"><span data-stu-id="9d744-126">[in] A pointer to the interface identifier (IID) of the interface that is used to access the open entry.</span></span> <span data-ttu-id="9d744-127">Pasando NULL, devuelve la interfaz estándar del objeto.</span><span class="sxs-lookup"><span data-stu-id="9d744-127">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="9d744-128">Para los usuarios de mensajería, es la interfaz estándar de [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="9d744-128">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="9d744-129">Para las listas de distribución, es [IDistList: IMAPIContainer](idistlistimapicontainer.md)y para contenedores, es [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="9d744-129">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md)and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="9d744-130">Los autores de llamadas pueden establecer _lpInterface_ en la interfaz estándar adecuada o una interfaz en la jerarquía de herencia.</span><span class="sxs-lookup"><span data-stu-id="9d744-130">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="9d744-131">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9d744-131">_ulFlags_</span></span>
  
> <span data-ttu-id="9d744-132">[entrada] Una máscara de bits de indicadores que controla cómo se abre la entrada, se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="9d744-132">[in] A bitmask of flags that controls the how the entry is opened, The following flags can be set:</span></span>
    
<span data-ttu-id="9d744-133">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="9d744-133">MAPI_BEST_ACCESS</span></span>
  
> <span data-ttu-id="9d744-134">Solicitudes que se abra la entrada con los permisos de red y cliente permitidos máximos.</span><span class="sxs-lookup"><span data-stu-id="9d744-134">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="9d744-135">Por ejemplo, si el cliente ha leído y permiso de escritura, el proveedor de la libreta de direcciones intenta abrir la entrada con la lectura y permiso de escritura.</span><span class="sxs-lookup"><span data-stu-id="9d744-135">For example, if the client has read and write permission, the address book provider attempts to open the entry with read and write permission.</span></span> <span data-ttu-id="9d744-136">El cliente puede recuperar el nivel de acceso que se ha concedido mediante una llamada al método [IMAPIProp::GetProps](imapiprop-getprops.md) de la entrada open y la recuperación de la propiedad PR_ACCESS_LEVEL (PidTagAccessLevel).</span><span class="sxs-lookup"><span data-stu-id="9d744-136">The client can retrieve the access level that was granted by calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method of the open entry and retrieving the PR_ACCESS_LEVEL (PidTagAccessLevel) property.</span></span> 
    
<span data-ttu-id="9d744-137">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="9d744-137">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="9d744-138">Usar sólo la libreta de direcciones sin conexión para llevar a cabo la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="9d744-138">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="9d744-139">Por ejemplo, puede usar esta marca para permitir que una aplicación cliente para abrir la lista global de direcciones (GAL) en el modo de intercambio en caché y obtener acceso a una entrada en esa libreta de direcciones de la memoria caché sin crear el tráfico entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="9d744-139">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="9d744-140">Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="9d744-140">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="9d744-141">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="9d744-141">MAPI_DEFERRED_ERRORS</span></span>
  
> <span data-ttu-id="9d744-142">Permite que la llamada se realice correctamente, potencialmente antes de la entrada es totalmente abiertos y disponibles, lo que implica que las llamadas posteriores a la entrada devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="9d744-142">Allows the call to succeed, potentially before the entry is fully open and available, implying that subsequent calls to the entry might return an error.</span></span>
    
<span data-ttu-id="9d744-143">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="9d744-143">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="9d744-144">Usar sólo la lista global de direcciones para llevar a cabo la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="9d744-144">Use only the GAL to perform name resolution.</span></span> <span data-ttu-id="9d744-145">Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="9d744-145">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="9d744-146">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="9d744-146">MAPI_MODIFY</span></span>
  
> <span data-ttu-id="9d744-147">Las solicitudes que se abre la entrada con leer y permiso de escritura.</span><span class="sxs-lookup"><span data-stu-id="9d744-147">Requests that the entry be opened with read and write permission.</span></span> <span data-ttu-id="9d744-148">Debido a que las entradas se abren con acceso de solo lectura de forma predeterminada, los clientes no deben asumir que de lectura y escritura se ha concedido permiso, independientemente de si se ha establecido MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="9d744-148">Because entries are opened with read-only access by default, clients should not assume that read and write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="9d744-149">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="9d744-149">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="9d744-150">No use la libreta de direcciones sin conexión para llevar a cabo la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="9d744-150">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="9d744-151">Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="9d744-151">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
 <span data-ttu-id="9d744-152">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="9d744-152">_lpulObjType_</span></span>
  
> <span data-ttu-id="9d744-153">[out] Un puntero al tipo de la entrada que se abrió.</span><span class="sxs-lookup"><span data-stu-id="9d744-153">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="9d744-154">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="9d744-154">_lppUnk_</span></span>
  
> <span data-ttu-id="9d744-155">[out] Un puntero a un puntero de la entrada que se abrió.</span><span class="sxs-lookup"><span data-stu-id="9d744-155">[out] A pointer to a pointer of the opened entry.</span></span>
    

