---
title: IMAPIContainerOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.OpenEntry
api_type:
- COM
ms.assetid: 0c46c1fb-dd63-4ac5-960e-80f68e75d8f4
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9598e0c90c16db14cdc3a46d2b2ae74e0d9a9300
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423639"
---
# <a name="imapicontaineropenentry"></a><span data-ttu-id="51934-103">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="51934-103">IMAPIContainer::OpenEntry</span></span>

  
  
<span data-ttu-id="51934-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51934-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51934-105">Abre un objeto en el contenedor y devuelve un puntero de interfaz para obtener más acceso.</span><span class="sxs-lookup"><span data-stu-id="51934-105">Opens an object in the container, returning an interface pointer for further access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="51934-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="51934-106">Parameters</span></span>

 <span data-ttu-id="51934-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="51934-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="51934-108">[entrada] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="51934-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="51934-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="51934-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="51934-110">[entrada] Puntero al identificador de entrada del objeto que se debe abrir.</span><span class="sxs-lookup"><span data-stu-id="51934-110">[in] A pointer to the entry identifier of the object to open.</span></span> <span data-ttu-id="51934-111">Si  _lpEntryID_ se establece en NULL, se abre el contenedor de nivel superior de la jerarquía del contenedor.</span><span class="sxs-lookup"><span data-stu-id="51934-111">If  _lpEntryID_ is set to NULL, the top-level container in the container's hierarchy is opened.</span></span> 
    
 <span data-ttu-id="51934-112">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="51934-112">_lpInterface_</span></span>
  
> <span data-ttu-id="51934-113">[entrada] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso al objeto.</span><span class="sxs-lookup"><span data-stu-id="51934-113">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object.</span></span> <span data-ttu-id="51934-114">Si se pasa NULL, se devuelve el identificador de la interfaz estándar del objeto.</span><span class="sxs-lookup"><span data-stu-id="51934-114">Passing NULL results in the identifier for the object's standard interface being returned.</span></span> <span data-ttu-id="51934-115">Para los mensajes, la interfaz estándar [es IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md); para carpetas, es [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="51934-115">For messages, the standard interface is [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md); for folders, it is [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="51934-116">Las interfaces estándar para objetos de libreta de direcciones son [IDistList: IMAPIContainer](idistlistimapicontainer.md) para una lista de distribución e [IMailUser : IMAPIProp](imailuserimapiprop.md) para un usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="51934-116">The standard interfaces for address book objects are [IDistList : IMAPIContainer](idistlistimapicontainer.md) for a distribution list and [IMailUser : IMAPIProp](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="51934-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="51934-117">_ulFlags_</span></span>
  
> <span data-ttu-id="51934-118">[entrada] Máscara de bits de marcas que controla cómo se abre el objeto.</span><span class="sxs-lookup"><span data-stu-id="51934-118">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="51934-119">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="51934-119">The following flags can be set:</span></span>
    
<span data-ttu-id="51934-120">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="51934-120">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="51934-121">Solicita que el objeto se abra con los permisos de red máximos permitidos para el usuario y el acceso máximo a la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="51934-121">Requests that the object will be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="51934-122">Por ejemplo, si el cliente tiene permiso de lectura y escritura, el objeto debe abrirse con permiso de lectura y escritura; si el cliente tiene acceso de solo lectura, el objeto debe abrirse con acceso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="51934-122">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only access, the object should be opened with read-only access.</span></span> 
    
<span data-ttu-id="51934-123">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="51934-123">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="51934-124">Permite **que OpenEntry** vuelva correctamente, posiblemente antes de que el objeto esté totalmente disponible para el cliente que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="51934-124">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="51934-125">Si el objeto no está disponible, realizar una llamada a objeto posterior puede generar un error.</span><span class="sxs-lookup"><span data-stu-id="51934-125">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="51934-126">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="51934-126">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="51934-127">Solicita permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="51934-127">Requests read/write permission.</span></span> <span data-ttu-id="51934-128">De forma predeterminada, los objetos se abren con acceso de solo lectura y los clientes no deben trabajar en la suposición de que se ha concedido permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="51934-128">By default, objects are opened with read-only access, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
<span data-ttu-id="51934-129">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="51934-129">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="51934-130">Muestra los elementos que están marcados actualmente como eliminados temporalmente, es decir, están en la fase de tiempo de retención de elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="51934-130">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="51934-131">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="51934-131">_lpulObjType_</span></span>
  
> <span data-ttu-id="51934-132">[salida] Puntero al tipo del objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="51934-132">[out] A pointer to the opened object's type.</span></span>
    
 <span data-ttu-id="51934-133">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="51934-133">_lppUnk_</span></span>
  
> <span data-ttu-id="51934-134">[salida] Puntero a un puntero a la implementación de la interfaz que se usa para tener acceso al objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="51934-134">[out] A pointer to a pointer to the interface implementation to use to access the open object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="51934-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="51934-135">Return value</span></span>

<span data-ttu-id="51934-136">S_OK</span><span class="sxs-lookup"><span data-stu-id="51934-136">S_OK</span></span> 
  
> <span data-ttu-id="51934-137">El objeto se abrió correctamente.</span><span class="sxs-lookup"><span data-stu-id="51934-137">The object was successfully opened.</span></span>
    
<span data-ttu-id="51934-138">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="51934-138">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="51934-139">El usuario no tiene permisos suficientes para abrir el objeto o se intentó abrir un objeto de solo lectura con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="51934-139">Either the user has insufficient permissions to open the object or an attempt was made to open a read-only object with read/write permission.</span></span>
    
<span data-ttu-id="51934-140">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="51934-140">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="51934-141">El identificador de entrada especificado  _por lpEntryID_ no representa un objeto.</span><span class="sxs-lookup"><span data-stu-id="51934-141">The entry identifier specified by  _lpEntryID_ does not represent an object.</span></span> 
    
<span data-ttu-id="51934-142">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="51934-142">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="51934-143">El identificador de entrada del  _parámetro lpEntryID_ no tiene un formato reconocido por el contenedor.</span><span class="sxs-lookup"><span data-stu-id="51934-143">The entry identifier in the  _lpEntryID_ parameter is not of a format recognized by the container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="51934-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="51934-144">Remarks</span></span>

<span data-ttu-id="51934-145">El **método IMAPIContainer::OpenEntry** abre un objeto en todo un contenedor y devuelve un puntero a una implementación de interfaz para usarlo para obtener más acceso.</span><span class="sxs-lookup"><span data-stu-id="51934-145">The **IMAPIContainer::OpenEntry** method opens an object throughout a container and returns a pointer to an interface implementation to use for further access.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="51934-146">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="51934-146">Notes to callers</span></span>

<span data-ttu-id="51934-147">Dado que no es necesario que los proveedores de servicios devuelvan una implementación de interfaz del tipo especificado por el identificador de interfaz en el parámetro _lpInterface,_ compruebe el valor al que apunta el parámetro _lpulObjType._</span><span class="sxs-lookup"><span data-stu-id="51934-147">Because service providers are not required to return an interface implementation of the type specified by the interface identifier in the  _lpInterface_ parameter, check the value pointed to by the  _lpulObjType_ parameter.</span></span> <span data-ttu-id="51934-148">Si es necesario, convierte el puntero devuelto en  _lppUnk_ en un puntero del tipo adecuado.</span><span class="sxs-lookup"><span data-stu-id="51934-148">If necessary, cast the pointer returned in  _lppUnk_ to a pointer of the appropriate type.</span></span> 
  
<span data-ttu-id="51934-149">De forma predeterminada, los proveedores de servicios abren objetos con acceso de solo lectura a menos que establezca la marca MAPI_MODIFY o MAPI_BEST_ACCESS usuario.</span><span class="sxs-lookup"><span data-stu-id="51934-149">By default, service providers open objects with read-only access unless you set either the MAPI_MODIFY or MAPI_BEST_ACCESS flag.</span></span> <span data-ttu-id="51934-150">Cuando se establece una de estas marcas, los proveedores de servicios intentan devolver un objeto modificable.</span><span class="sxs-lookup"><span data-stu-id="51934-150">When one of these flags is set, service providers attempt to return a modifiable object.</span></span> <span data-ttu-id="51934-151">Sin embargo, no suponga que, dado que solicitó un objeto modificable, el objeto abierto tiene permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="51934-151">However, do not assume that because you requested a modifiable object that the opened object has read/write permission.</span></span> <span data-ttu-id="51934-152">Planee la posibilidad de que se producirá un  error en una modificación posterior o recupere la propiedad PR_ACCESS_LEVEL del objeto para determinar el nivel de acceso concedido por **OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="51934-152">Either plan for the chance of a subsequent modification to fail or retrieve the object's **PR_ACCESS_LEVEL** property to determine the access level granted by **OpenEntry**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="51934-153">Consulte también</span><span class="sxs-lookup"><span data-stu-id="51934-153">See also</span></span>



[<span data-ttu-id="51934-154">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="51934-154">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)

