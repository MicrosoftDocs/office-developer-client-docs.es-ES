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
description: 'Última modificación: 1 de febrero de 2013'
ms.openlocfilehash: 293fe5a65c760f61ab0073e0eafc1a606c69050f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434168"
---
# <a name="iaddrbookopenentry"></a><span data-ttu-id="fa587-103">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="fa587-103">IAddrBook::OpenEntry</span></span>

<span data-ttu-id="fa587-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa587-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa587-105">Abre una entrada de la libreta de direcciones y devuelve un puntero a una interfaz que puede usarse para tener acceso a la entrada.</span><span class="sxs-lookup"><span data-stu-id="fa587-105">Opens an address book entry and returns a pointer to an interface that can be used to access the entry.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="fa587-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="fa587-106">Parameters</span></span>

<span data-ttu-id="fa587-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="fa587-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="fa587-108">a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="fa587-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="fa587-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="fa587-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="fa587-110">a Un puntero al identificador de entrada que representa la entrada de la libreta de direcciones que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="fa587-110">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
<span data-ttu-id="fa587-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="fa587-111">_lpInterface_</span></span>
  
> <span data-ttu-id="fa587-112">a Puntero al identificador de interfaz (IID) de la interfaz que se va a usar para obtener acceso a la entrada abierta.</span><span class="sxs-lookup"><span data-stu-id="fa587-112">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="fa587-113">Al pasar NULL, se devuelve la interfaz estándar del objeto.</span><span class="sxs-lookup"><span data-stu-id="fa587-113">Passing NULL returns the object's standard interface.</span></span> <span data-ttu-id="fa587-114">Para los usuarios de mensajería, la interfaz estándar es [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="fa587-114">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="fa587-115">Para las listas de distribución, es [IDistList: IMAPIContainer](idistlistimapicontainer.md) y para contenedores, es [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="fa587-115">For distribution lists, it is [IDistList : IMAPIContainer](idistlistimapicontainer.md) and for containers, it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="fa587-116">Los autores de llamadas pueden establecer _lpInterface_ en la interfaz estándar adecuada o en una interfaz de la jerarquía de herencia.</span><span class="sxs-lookup"><span data-stu-id="fa587-116">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
<span data-ttu-id="fa587-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fa587-117">_ulFlags_</span></span>
  
> <span data-ttu-id="fa587-118">a Máscara de máscara de marcadores que controla cómo se abre la entrada.</span><span class="sxs-lookup"><span data-stu-id="fa587-118">[in] A bitmask of flags that controls how the entry is opened.</span></span> <span data-ttu-id="fa587-119">Se pueden establecer los siguientes indicadores.</span><span class="sxs-lookup"><span data-stu-id="fa587-119">The following flags can be set.</span></span>
    
<span data-ttu-id="fa587-120">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="fa587-120">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="fa587-121">Solicita que se abra la entrada con los permisos de red y de cliente máximos permitidos.</span><span class="sxs-lookup"><span data-stu-id="fa587-121">Requests that the entry be opened with the maximum allowed network and client permissions.</span></span> <span data-ttu-id="fa587-122">Por ejemplo, si el cliente tiene permiso de lectura y escritura, el proveedor de la libreta de direcciones debe intentar abrir la entrada con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="fa587-122">For example, if the client has read/write permission, the address book provider should attempt to open the entry with read/write permission.</span></span> <span data-ttu-id="fa587-123">El cliente puede recuperar el nivel de acceso que se ha concedido al llamar al método [IMAPIProp:: GetProps](imapiprop-getprops.md) del elemento abierto y recuperar la propiedad **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="fa587-123">The client can retrieve the access level that was granted by calling the open entry's [IMAPIProp::GetProps](imapiprop-getprops.md) method and retrieving the **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="fa587-124">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="fa587-124">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="fa587-125">Abre una entrada de la libreta de direcciones y solo obtiene acceso a ella desde la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="fa587-125">Opens an address book entry and accesses it only from the cache.</span></span> <span data-ttu-id="fa587-126">Por ejemplo, puede usar esta marca para permitir que una aplicación cliente Abra la lista global de direcciones (GAL) en el modo caché de Exchange y obtenga acceso a una entrada de la libreta de direcciones desde la memoria caché sin crear tráfico entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="fa587-126">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="fa587-127">Este indicador solo es compatible con el proveedor de libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="fa587-127">This flag is supported only by the Exchange address book provider.</span></span>
    
<span data-ttu-id="fa587-128">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="fa587-128">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="fa587-129">Permite que la llamada se realice correctamente, posiblemente antes de que la entrada esté completamente abierta y disponible, lo que implica que las llamadas posteriores a la entrada podrían devolver un error.</span><span class="sxs-lookup"><span data-stu-id="fa587-129">Allows the call to succeed, potentially before the entry is fully open and available, implying that later calls to the entry might return an error.</span></span>
    
<span data-ttu-id="fa587-130">MAPI_GAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="fa587-130">MAPI_GAL_ONLY</span></span>
  
> <span data-ttu-id="fa587-131">Use solamente la GAL para la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="fa587-131">Use only the GAL to perform name resolution.</span></span> <span data-ttu-id="fa587-132">Este indicador solo es compatible con el proveedor de libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="fa587-132">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="fa587-133">Es posible que el MAPI_GAL_ONLY _ulFlags_ no esté definido en el archivo de encabezado descargable que tiene actualmente, en cuyo caso puede agregarlo al código con el siguiente valor: >`#define MAPI_GAL_ONLY (0x00000080)`</span><span class="sxs-lookup"><span data-stu-id="fa587-133">The  _ulFlags_ MAPI_GAL_ONLY might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following value: >  `#define MAPI_GAL_ONLY (0x00000080)`</span></span>
  
<span data-ttu-id="fa587-134">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="fa587-134">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="fa587-135">Solicita que la entrada se abra con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="fa587-135">Requests that the entry be opened with read/write permission.</span></span> <span data-ttu-id="fa587-136">Debido a que las entradas se abren con acceso de solo lectura de forma predeterminada, los clientes no deben dar por supuesto que el permiso de lectura y escritura se concedió independientemente de si se ha establecido MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="fa587-136">Because entries are opened with read-only access by default, clients should not assume that read/write permission was granted regardless of whether MAPI_MODIFY is set.</span></span>
    
<span data-ttu-id="fa587-137">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="fa587-137">MAPI_NO_CACHE</span></span>
  
> <span data-ttu-id="fa587-138">No use la libreta de direcciones sin conexión para realizar la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="fa587-138">Do not use the offline address book to perform name resolution.</span></span> <span data-ttu-id="fa587-139">Este indicador solo es compatible con el proveedor de libreta de direcciones de Exchange.</span><span class="sxs-lookup"><span data-stu-id="fa587-139">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="fa587-140">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="fa587-140">_lpulObjType_</span></span>
  
> <span data-ttu-id="fa587-141">contempla Puntero al tipo de la entrada abierta.</span><span class="sxs-lookup"><span data-stu-id="fa587-141">[out] A pointer to the type of the opened entry.</span></span>
    
<span data-ttu-id="fa587-142">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="fa587-142">_lppUnk_</span></span>
  
> <span data-ttu-id="fa587-143">contempla Un puntero a un puntero a la entrada abierta.</span><span class="sxs-lookup"><span data-stu-id="fa587-143">[out] A pointer to a pointer to the opened entry.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fa587-144">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fa587-144">Return value</span></span>

<span data-ttu-id="fa587-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="fa587-145">S_OK</span></span> 
  
> <span data-ttu-id="fa587-146">La entrada se abrió correctamente.</span><span class="sxs-lookup"><span data-stu-id="fa587-146">The entry was successfully opened.</span></span>
    
<span data-ttu-id="fa587-147">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="fa587-147">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="fa587-148">Se intentó abrir una entrada para la que el usuario no tiene permisos suficientes.</span><span class="sxs-lookup"><span data-stu-id="fa587-148">An attempt was made to open an entry for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="fa587-149">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="fa587-149">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="fa587-150">La entrada representada por _lpEntryID_ no existe.</span><span class="sxs-lookup"><span data-stu-id="fa587-150">The entry represented by  _lpEntryID_ does not exist.</span></span> 
    
<span data-ttu-id="fa587-151">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="fa587-151">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="fa587-152">No se reconoce el identificador de entrada especificado en _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="fa587-152">The entry identifier specified in  _lpEntryID_ is not recognized.</span></span> <span data-ttu-id="fa587-153">Normalmente, este valor se devuelve si el proveedor de la libreta de direcciones responsable de la entrada correspondiente no está abierto.</span><span class="sxs-lookup"><span data-stu-id="fa587-153">This value is typically returned if the address book provider responsible for the corresponding entry is not open.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fa587-154">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fa587-154">Remarks</span></span>

<span data-ttu-id="fa587-155">Los clientes y los proveedores de servicios llaman al método **IAddrBook:: OpenEntry** para abrir una entrada de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="fa587-155">Clients and service providers call the **IAddrBook::OpenEntry** method to open an address book entry.</span></span> <span data-ttu-id="fa587-156">MAPI reenvía la llamada al proveedor de libreta de direcciones adecuado, en función de la estructura [MAPIUID](mapiuid.md) incluida en el identificador de entrada que se ha pasado en el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="fa587-156">MAPI forwards the call to the appropriate address book provider, based on the [MAPIUID](mapiuid.md) structure included in the entry identifier passed in the  _lpEntryID_ parameter.</span></span> <span data-ttu-id="fa587-157">El proveedor de la libreta de direcciones abre la entrada como de solo lectura a menos que se establezca el indicador MAPI_MODIFY o MAPI_BEST_ACCESS en el parámetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="fa587-157">The address book provider opens the entry as read-only unless the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter is set.</span></span> <span data-ttu-id="fa587-158">Sin embargo, estos marcadores son sugerencias.</span><span class="sxs-lookup"><span data-stu-id="fa587-158">However, these flags are suggestions.</span></span> <span data-ttu-id="fa587-159">Si el proveedor de la libreta de direcciones no permite la modificación de la entrada solicitada, devuelve MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="fa587-159">If the address book provider does not allow modification for the entry requested, it returns MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="fa587-160">El parámetro _lpInterface_ indica qué interfaz debe usarse para tener acceso a la entrada abierta.</span><span class="sxs-lookup"><span data-stu-id="fa587-160">The  _lpInterface_ parameter indicates which interface should be used to access the opened entry.</span></span> <span data-ttu-id="fa587-161">Pasar NULL en _lpInterface_ indica que se debe usar la interfaz MAPI estándar para ese tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="fa587-161">Passing NULL in  _lpInterface_ indicates the standard MAPI interface for that type of entry should be used.</span></span> <span data-ttu-id="fa587-162">Como el proveedor de la libreta de direcciones puede devolver una interfaz diferente a la que sugiere el parámetro _lpInterface_ , el autor de la llamada debe comprobar el valor devuelto en el parámetro _lpulObjType_ para determinar si el tipo de objeto devuelto es Qué se esperaba.</span><span class="sxs-lookup"><span data-stu-id="fa587-162">Because the address book provider might return a different interface than the one suggested by the  _lpInterface_ parameter, the caller should check the value returned in the  _lpulObjType_ parameter to determine whether the object type returned is what was expected.</span></span> <span data-ttu-id="fa587-163">Si el tipo de objeto no es del tipo esperado, el autor de la llamada puede convertir el parámetro _lppUnk_ en un tipo más adecuado.</span><span class="sxs-lookup"><span data-stu-id="fa587-163">If the object type is not of the type expected, the caller can cast the  _lppUnk_ parameter to a type that is more appropriate.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fa587-164">Ver también</span><span class="sxs-lookup"><span data-stu-id="fa587-164">See also</span></span>

- [<span data-ttu-id="fa587-165">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="fa587-165">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

