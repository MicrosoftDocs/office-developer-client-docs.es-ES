---
title: IMAPISupportOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenEntry
api_type:
- COM
ms.assetid: 84662230-6a25-4403-b87e-871427a40c6e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: cfbb799336aa1e75fa36e03e55d82c3af3409f10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409618"
---
# <a name="imapisupportopenentry"></a><span data-ttu-id="d6772-103">IMAPISupport::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="d6772-103">IMAPISupport::OpenEntry</span></span>

  
  
<span data-ttu-id="d6772-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6772-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6772-105">Abre un objeto y devuelve un puntero de interfaz para obtener más acceso.</span><span class="sxs-lookup"><span data-stu-id="d6772-105">Opens an object and returns an interface pointer for further access.</span></span> 
  
```cpp
HRESULT OpenEntry(
ULONG cbEntryID,
LPENTRYID lpEntryID,
LPCIID lpInterface,
ULONG ulOpenFlags,
ULONG FAR * lpulObjType,
LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="d6772-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d6772-106">Parameters</span></span>

 <span data-ttu-id="d6772-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="d6772-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="d6772-108">[entrada] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="d6772-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="d6772-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="d6772-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="d6772-110">[entrada] Puntero al identificador de entrada del objeto que se debe abrir.</span><span class="sxs-lookup"><span data-stu-id="d6772-110">[in] A pointer to the entry identifier of the object to open.</span></span>
    
 <span data-ttu-id="d6772-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="d6772-111">_lpInterface_</span></span>
  
> <span data-ttu-id="d6772-112">[entrada] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso al objeto.</span><span class="sxs-lookup"><span data-stu-id="d6772-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object.</span></span> <span data-ttu-id="d6772-113">Si se pasa NULL, se devuelve la interfaz estándar del objeto.</span><span class="sxs-lookup"><span data-stu-id="d6772-113">Passing NULL results in the object's standard interface being returned.</span></span> <span data-ttu-id="d6772-114">Por ejemplo, si el objeto que se va a abrir es un mensaje, la interfaz estándar es [IMessage](imessageimapiprop.md); para carpetas, es [IMAPIFolder](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="d6772-114">For example, if the object to be opened is a message, the standard interface is [IMessage](imessageimapiprop.md); for folders, it is [IMAPIFolder](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="d6772-115">Las interfaces estándar para objetos de libreta de direcciones son [IDistList](idistlistimapicontainer.md) para una lista de distribución e [IMailUser](imailuserimapiprop.md) para un usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="d6772-115">The standard interfaces for address book objects are [IDistList](idistlistimapicontainer.md) for a distribution list and [IMailUser](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="d6772-116">_ulOpenFlags_</span><span class="sxs-lookup"><span data-stu-id="d6772-116">_ulOpenFlags_</span></span>
  
> <span data-ttu-id="d6772-117">[entrada] Máscara de bits de marcas que controla cómo se abre el objeto.</span><span class="sxs-lookup"><span data-stu-id="d6772-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="d6772-118">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="d6772-118">The following flags can be set:</span></span>
    
<span data-ttu-id="d6772-119">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="d6772-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="d6772-120">Solicita que el objeto se abra con los permisos de red máximos permitidos para el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="d6772-120">Requests that the object be opened with the maximum network permissions allowed for the caller.</span></span> <span data-ttu-id="d6772-121">Por ejemplo, si el autor de la llamada tiene permiso de lectura y escritura, el objeto debe abrirse como lectura y escritura; si el autor de la llamada tiene permiso de solo lectura, el objeto debe abrirse como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d6772-121">For example, if the caller has read/write permission, the object should be opened as read/write; if the caller has read-only permission, the object should be opened as read-only.</span></span> 
    
<span data-ttu-id="d6772-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="d6772-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="d6772-123">Permite **que OpenEntry** vuelva correctamente, posiblemente antes de que el objeto sea totalmente accesible para el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="d6772-123">Allows **OpenEntry** to return successfully, possibly before the object is fully accessible to the caller.</span></span> <span data-ttu-id="d6772-124">Si no se puede obtener acceso al objeto, realizar una llamada a objeto posterior puede provocar un error.</span><span class="sxs-lookup"><span data-stu-id="d6772-124">If the object is not accessible, making a subsequent object call can result in an error.</span></span> 
    
<span data-ttu-id="d6772-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="d6772-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="d6772-126">Solicita permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d6772-126">Requests read/write permission.</span></span> <span data-ttu-id="d6772-127">De forma predeterminada, los objetos se abren como de solo lectura y los autores de llamadas no deben trabajar en la suposición de que se ha concedido permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d6772-127">By default, objects are opened as read-only, and callers should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="d6772-128">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="d6772-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="d6772-129">[salida] Puntero al tipo del objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="d6772-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="d6772-130">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="d6772-130">_lppUnk_</span></span>
  
> <span data-ttu-id="d6772-131">[salida] Puntero a un puntero al objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="d6772-131">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d6772-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d6772-132">Return value</span></span>

<span data-ttu-id="d6772-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="d6772-133">S_OK</span></span> 
  
> <span data-ttu-id="d6772-134">El objeto se abrió correctamente.</span><span class="sxs-lookup"><span data-stu-id="d6772-134">The object was successfully opened.</span></span>
    
<span data-ttu-id="d6772-135">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="d6772-135">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="d6772-136">Se intentó modificar un objeto de solo lectura o se intentó obtener acceso a un objeto para el que el usuario no tiene permisos suficientes.</span><span class="sxs-lookup"><span data-stu-id="d6772-136">An attempt was made to modify a read-only object, or an attempt was made to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="d6772-137">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="d6772-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="d6772-138">No hay ningún objeto asociado con el identificador de entrada pasado en el _parámetro lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="d6772-138">There is not an object associated with the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="d6772-139">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="d6772-139">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="d6772-140">El identificador de entrada pasado en  _el parámetro lpEntryID_ está en un formato irreconocible.</span><span class="sxs-lookup"><span data-stu-id="d6772-140">The entry identifier passed in the  _lpEntryID_ parameter is in an unrecognizable format.</span></span> <span data-ttu-id="d6772-141">Normalmente, este valor se devuelve si el proveedor de libreta de direcciones que contiene el objeto no está abierto.</span><span class="sxs-lookup"><span data-stu-id="d6772-141">This value is typically returned if the address book provider that contains the object is not open.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d6772-142">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d6772-142">Remarks</span></span>

<span data-ttu-id="d6772-143">El **método IMAPISupport::OpenEntry** se implementa para todos los objetos de compatibilidad del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="d6772-143">The **IMAPISupport::OpenEntry** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="d6772-144">Los proveedores de servicios llaman a **IMAPISupport::OpenEntry** para recuperar un puntero a una interfaz que se puede usar para tener acceso a un objeto determinado.</span><span class="sxs-lookup"><span data-stu-id="d6772-144">Service providers call **IMAPISupport::OpenEntry** to retrieve a pointer to an interface that can be used to access a particular object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d6772-145">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="d6772-145">Notes to callers</span></span>

<span data-ttu-id="d6772-146">Llame **a IMAPISupport::OpenEntry** solo cuando no sepa qué tipo de objeto está abriendo.</span><span class="sxs-lookup"><span data-stu-id="d6772-146">Call **IMAPISupport::OpenEntry** only when you do not know what kind of object you are opening.</span></span> <span data-ttu-id="d6772-147">Si sabe que está abriendo una carpeta o un mensaje, llame a [IMsgStore::OpenEntry en su](imsgstore-openentry.md) lugar.</span><span class="sxs-lookup"><span data-stu-id="d6772-147">If you know you are opening a folder or a message, call [IMsgStore::OpenEntry](imsgstore-openentry.md) instead.</span></span> <span data-ttu-id="d6772-148">Si sabe que está abriendo un contenedor de libreta de direcciones, un usuario de mensajería o una lista de distribución, llame a [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="d6772-148">If you know you are opening an address book container, a messaging user, or a distribution list, call [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="d6772-149">Estos métodos más específicos son más **rápidos que IMAPISupport::OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="d6772-149">These more specific methods are faster than **IMAPISupport::OpenEntry**.</span></span> 
  
 <span data-ttu-id="d6772-150">**IMAPISupport::OpenEntry** abre todos los objetos como de solo lectura, a menos que establezca la marca MAPI_MODIFY o MAPI_BEST_ACCESS en el parámetro  _ulFlags_ y los permisos sean suficientes.</span><span class="sxs-lookup"><span data-stu-id="d6772-150">**IMAPISupport::OpenEntry** opens all objects as read-only, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter and your permissions are sufficient.</span></span> <span data-ttu-id="d6772-151">Establecer una de estas marcas no garantiza un tipo concreto de acceso; los permisos que se le conceden dependen del nivel de acceso, el objeto y el proveedor de servicios que posee el objeto.</span><span class="sxs-lookup"><span data-stu-id="d6772-151">Setting one of these flags does not guarantee a particular type of access; the permissions that you are granted depend on your access level, the object, and the service provider that owns the object.</span></span> <span data-ttu-id="d6772-152">Para determinar el nivel de acceso del objeto abierto, recupere **su PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d6772-152">To determine the access level of the opened object, retrieve its **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="d6772-153">Compruebe el valor devuelto en el  _parámetro lpulObjType_ para determinar que el tipo de objeto devuelto es el esperado.</span><span class="sxs-lookup"><span data-stu-id="d6772-153">Check the value returned in the  _lpulObjType_ parameter to determine that the object type returned is what you expected.</span></span> <span data-ttu-id="d6772-154">Si el tipo de objeto es el esperado, convierte el puntero del parámetro  _lppUnk_ en un puntero del tipo adecuado.</span><span class="sxs-lookup"><span data-stu-id="d6772-154">If the object type is as expected, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type.</span></span> <span data-ttu-id="d6772-155">Por ejemplo, si abre una carpeta, convierte  _lppUnk_ en un puntero de tipo LPMAPIFOLDER.</span><span class="sxs-lookup"><span data-stu-id="d6772-155">For example, if you are opening a folder, cast  _lppUnk_ to a pointer of type LPMAPIFOLDER.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d6772-156">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d6772-156">See also</span></span>



[<span data-ttu-id="d6772-157">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d6772-157">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

