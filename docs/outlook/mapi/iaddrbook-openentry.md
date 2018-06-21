---
title: IAddrBookOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.OpenEntry
api_type:
- COM
ms.assetid: bd7746f4-8070-4cc5-8b8e-c527c5847545
description: 'Última modificación: 01 de febrero de 2013'
ms.openlocfilehash: fa279962043f6f7cb7a134b624000c9c7e65369f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/21/2018
ms.locfileid: "19817148"
---
# <a name="iaddrbookopenentry"></a><span data-ttu-id="fc538-103">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="fc538-103">IAddrBook::OpenEntry</span></span>

<span data-ttu-id="fc538-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fc538-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fc538-105">Se abre una entrada de la libreta de direcciones y devuelve un puntero a una interfaz que se puede usar para tener acceso a la entrada.</span><span class="sxs-lookup"><span data-stu-id="fc538-105">Opens an address book entry and returns a pointer to an interface that can be used to access the entry.</span></span>
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="fc538-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fc538-106">Parameters</span></span>

<span data-ttu-id="fc538-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="fc538-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="fc538-108">[entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="fc538-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="fc538-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="fc538-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="fc538-110">[entrada] Un puntero al identificador de entrada que representa la entrada de la libreta de direcciones para abrir.</span><span class="sxs-lookup"><span data-stu-id="fc538-110">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
<span data-ttu-id="fc538-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="fc538-111">_lpInterface_</span></span>
  
> <span data-ttu-id="fc538-112">[entrada] Un puntero al identificador de interfaz (IID) de la interfaz que se usará para tener acceso a la entrada open.</span><span class="sxs-lookup"><span data-stu-id="fc538-112">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="fc538-113">Pasando NULL, devuelve la interfaz del objeto estándar.</span><span class="sxs-lookup"><span data-stu-id="fc538-113">Passing NULL returns the object's standard interface.</span></span> <span data-ttu-id="fc538-114">Para los usuarios de mensajería, es la interfaz estándar de [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="fc538-114">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="fc538-115">Para las listas de distribución, es [IDistList: IMAPIContainer](idistlistimapicontainer.md) y para contenedores, es [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="fc538-115">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md) and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="fc538-116">Los autores de llamadas pueden establecer _lpInterface_ en la interfaz estándar adecuada o una interfaz en la jerarquía de herencia.</span><span class="sxs-lookup"><span data-stu-id="fc538-116">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
<span data-ttu-id="fc538-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fc538-117">_ulFlags_</span></span>
  
> <span data-ttu-id="fc538-118">[entrada] Una máscara de bits de indicadores que controla cómo se abre la entrada.</span><span class="sxs-lookup"><span data-stu-id="fc538-118">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="fc538-119">Se pueden establecer las siguientes marcas.</span><span class="sxs-lookup"><span data-stu-id="fc538-119">The following flags can be set.</span></span>
    
<span data-ttu-id="fc538-120">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="fc538-120">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="fc538-121">Solicitudes que se abra la entrada con los permisos de red y cliente permitidos máximos.</span><span class="sxs-lookup"><span data-stu-id="fc538-121">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="fc538-122">Por ejemplo, si el cliente no tiene permiso de lectura y escritura, el proveedor de la libreta de direcciones debe intentar abrir la entrada con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="fc538-122">For example, if the client has read/write permission, the address book provider should attempt to open the entry with read/write permission.</span></span> <span data-ttu-id="fc538-123">El cliente puede recuperar el nivel de acceso que se ha concedido por llamar al método open de la entrada [IMAPIProp::GetProps](imapiprop-getprops.md) y recuperación de la propiedad **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="fc538-123">The client can retrieve the access level that was granted by calling the open entry's [IMAPIProp::GetProps](imapiprop-getprops.md) method and retrieving the **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="fc538-124">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="fc538-124">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="fc538-125">Se abre una entrada de la libreta de direcciones y tiene acceso a él sólo desde la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="fc538-125">Opens an address book entry and accesses it only from the cache.</span></span> <span data-ttu-id="fc538-126">Por ejemplo, puede usar esta marca para permitir que una aplicación cliente para abrir la lista global de direcciones (GAL) en el modo de intercambio en caché y obtener acceso a una entrada en esa libreta de direcciones de la memoria caché sin crear el tráfico entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="fc538-126">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="fc538-127">Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="fc538-127">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="fc538-128">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="fc538-128">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="fc538-129">Permite que la llamada se realice correctamente, potencialmente antes de la entrada es totalmente abiertos y disponibles, lo que implica que las llamadas posteriores a la entrada devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="fc538-129">Allows the call to succeed, potentially before the entry is fully open and available, implying that later calls to the entry might return an error.</span></span>
    
<span data-ttu-id="fc538-130">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="fc538-130">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="fc538-131">Usar sólo la lista global de direcciones para llevar a cabo la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="fc538-131">Use only the GAL to perform name resolution.</span></span> <span data-ttu-id="fc538-132">Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="fc538-132">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="fc538-133">_UlFlags_ MAPI_GAL_ONLY no pueden definirse en el archivo de encabezado que se pueden descargar tiene actualmente, en cuyo caso se puede agregar a su código con el siguiente valor: >`#define MAPI_GAL_ONLY (0x00000080)`</span><span class="sxs-lookup"><span data-stu-id="fc538-133">The  _ulFlags_ MAPI_GAL_ONLY might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following value: >  `#define MAPI_GAL_ONLY (0x00000080)`</span></span>
  
<span data-ttu-id="fc538-134">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="fc538-134">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="fc538-135">Las solicitudes de que la entrada se abre con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="fc538-135">Requests that the entry be opened with read/write permission.</span></span> <span data-ttu-id="fc538-136">Debido a que las entradas se abren con acceso de solo lectura de forma predeterminada, los clientes no deben suponer que se ha concedido permiso de lectura y escritura, independientemente de si se ha establecido MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="fc538-136">Because entries are opened with read-only access by default, clients should not assume that read/write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="fc538-137">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="fc538-137">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="fc538-138">No use la libreta de direcciones sin conexión para llevar a cabo la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="fc538-138">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="fc538-139">Esta marca sólo es compatible con el proveedor de la libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="fc538-139">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="fc538-140">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="fc538-140">_lpulObjType_</span></span>
  
> <span data-ttu-id="fc538-141">[out] Un puntero al tipo de la entrada que se abrió.</span><span class="sxs-lookup"><span data-stu-id="fc538-141">[out] A pointer to the type of the opened entry.</span></span>
    
<span data-ttu-id="fc538-142">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="fc538-142">_lppUnk_</span></span>
  
> <span data-ttu-id="fc538-143">[out] Un puntero a un puntero a la entrada que se abrió.</span><span class="sxs-lookup"><span data-stu-id="fc538-143">[out] A pointer to a pointer to the opened entry.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fc538-144">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fc538-144">Return value</span></span>

<span data-ttu-id="fc538-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="fc538-145">S_OK</span></span> 
  
> <span data-ttu-id="fc538-146">La entrada se abrió correctamente.</span><span class="sxs-lookup"><span data-stu-id="fc538-146">The entry was successfully opened.</span></span>
    
<span data-ttu-id="fc538-147">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="fc538-147">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="fc538-148">Se ha intentado abrir una entrada para la que el usuario no tiene permisos suficientes.</span><span class="sxs-lookup"><span data-stu-id="fc538-148">An attempt was made to open an entry for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="fc538-149">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="fc538-149">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="fc538-150">La entrada representada por _lpEntryID_ no existe.</span><span class="sxs-lookup"><span data-stu-id="fc538-150">The entry represented by  _lpEntryID_ does not exist.</span></span> 
    
<span data-ttu-id="fc538-151">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="fc538-151">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="fc538-152">No se reconoce el identificador de entrada especificado en _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="fc538-152">The entry identifier specified in  _lpEntryID_ is not recognized.</span></span> <span data-ttu-id="fc538-153">Normalmente, este valor se devuelve si el responsable de la entrada correspondiente del proveedor de libreta de direcciones no está abierto.</span><span class="sxs-lookup"><span data-stu-id="fc538-153">This value is typically returned if the address book provider responsible for the corresponding entry is not open.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fc538-154">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fc538-154">Remarks</span></span>

<span data-ttu-id="fc538-155">Los clientes y proveedores de servicios de llamar al método **IAddrBook::OpenEntry** para abrir una entrada de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="fc538-155">Clients and service providers call the **IAddrBook::OpenEntry** method to open an address book entry.</span></span> <span data-ttu-id="fc538-156">MAPI reenvía la llamada a la libreta de direcciones adecuado, basándose en la estructura [MAPIUID](mapiuid.md) que se incluye en el identificador de entrada que se pasa en el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="fc538-156">MAPI forwards the call to the appropriate address book provider, based on the [MAPIUID](mapiuid.md) structure included in the entry identifier passed in the  _lpEntryID_ parameter.</span></span> <span data-ttu-id="fc538-157">El proveedor de la libreta de direcciones abre la entrada como de sólo lectura a menos que se establece la marca MAPI_MODIFY o MAPI_BEST_ACCESS en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="fc538-157">The address book provider opens the entry as read-only unless the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter is set.</span></span> <span data-ttu-id="fc538-158">Sin embargo, estos marcadores son sugerencias.</span><span class="sxs-lookup"><span data-stu-id="fc538-158">However, these flags are suggestions.</span></span> <span data-ttu-id="fc538-159">Si el proveedor de la libreta de direcciones no permitir la modificación de la entrada de solicitado, devuelve MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="fc538-159">If the address book provider does not allow modification for the entry requested, it returns MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="fc538-160">El parámetro _lpInterface_ indica qué interfaz se debe utilizar para tener acceso a la entrada que se abrió.</span><span class="sxs-lookup"><span data-stu-id="fc538-160">The  _lpInterface_ parameter indicates which interface should be used to access the opened entry.</span></span> <span data-ttu-id="fc538-161">Pasando NULL en _lpInterface_ indica que se debe usar la interfaz estándar de MAPI para ese tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="fc538-161">Passing NULL in  _lpInterface_ indicates the standard MAPI interface for that type of entry should be used.</span></span> <span data-ttu-id="fc538-162">Debido a que el proveedor de la libreta de direcciones podría devolver una interfaz diferente de aquél al que sugiere el parámetro _lpInterface_ , el llamador debe comprobar el valor devuelto en el parámetro _lpulObjType_ para determinar si el tipo de objeto devuelto es ¿Qué se esperaba.</span><span class="sxs-lookup"><span data-stu-id="fc538-162">Because the address book provider might return a different interface than the one suggested by the  _lpInterface_ parameter, the caller should check the value returned in the  _lpulObjType_ parameter to determine whether the object type returned is what was expected.</span></span> <span data-ttu-id="fc538-163">Si el tipo de objeto no es del tipo esperado, el autor de la llamada puede convertir el parámetro _lppUnk_ a un tipo que sea más adecuado.</span><span class="sxs-lookup"><span data-stu-id="fc538-163">If the object type is not of the type expected, the caller can cast the  _lppUnk_ parameter to a type that is more appropriate.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fc538-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc538-164">See also</span></span>

- [<span data-ttu-id="fc538-165">IAddrBook: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="fc538-165">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

