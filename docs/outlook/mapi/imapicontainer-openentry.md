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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286935"
---
# <a name="imapicontaineropenentry"></a><span data-ttu-id="b1815-103">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="b1815-103">IMAPIContainer::OpenEntry</span></span>

  
  
<span data-ttu-id="b1815-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1815-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1815-105">Abre un objeto en el contenedor y devuelve un puntero de interfaz para obtener más acceso.</span><span class="sxs-lookup"><span data-stu-id="b1815-105">Opens an object in the container, returning an interface pointer for further access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="b1815-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="b1815-106">Parameters</span></span>

 <span data-ttu-id="b1815-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="b1815-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="b1815-108">a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="b1815-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="b1815-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="b1815-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="b1815-110">a Un puntero al identificador de entrada del objeto que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="b1815-110">[in] A pointer to the entry identifier of the object to open.</span></span> <span data-ttu-id="b1815-111">Si _lpEntryID_ se establece en null, se abre el contenedor de nivel superior de la jerarquía del contenedor.</span><span class="sxs-lookup"><span data-stu-id="b1815-111">If  _lpEntryID_ is set to NULL, the top-level container in the container's hierarchy is opened.</span></span> 
    
 <span data-ttu-id="b1815-112">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="b1815-112">_lpInterface_</span></span>
  
> <span data-ttu-id="b1815-113">a Un puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para obtener acceso al objeto.</span><span class="sxs-lookup"><span data-stu-id="b1815-113">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object.</span></span> <span data-ttu-id="b1815-114">Al pasar NULL se obtiene el identificador de la interfaz estándar del objeto que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="b1815-114">Passing NULL results in the identifier for the object's standard interface being returned.</span></span> <span data-ttu-id="b1815-115">Para los mensajes, la interfaz estándar es [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md); para las carpetas, es [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="b1815-115">For messages, the standard interface is [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md); for folders, it is [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="b1815-116">Las interfaces estándar para los objetos de la libreta de direcciones son [IDistList: IMAPIContainer](idistlistimapicontainer.md) para una lista de distribución y [IMailUser: IMAPIProp](imailuserimapiprop.md) para un usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="b1815-116">The standard interfaces for address book objects are [IDistList : IMAPIContainer](idistlistimapicontainer.md) for a distribution list and [IMailUser : IMAPIProp](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="b1815-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b1815-117">_ulFlags_</span></span>
  
> <span data-ttu-id="b1815-118">a Máscara de máscara de marcadores que controla cómo se abre el objeto.</span><span class="sxs-lookup"><span data-stu-id="b1815-118">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="b1815-119">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="b1815-119">The following flags can be set:</span></span>
    
<span data-ttu-id="b1815-120">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="b1815-120">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="b1815-121">Solicita que el objeto se abra con los permisos de red máximos permitidos para el usuario y el acceso máximo a la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="b1815-121">Requests that the object will be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="b1815-122">Por ejemplo, si el cliente tiene permiso de lectura y escritura, el objeto debe abrirse con permiso de lectura y escritura; Si el cliente tiene acceso de solo lectura, el objeto debe abrirse con acceso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b1815-122">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only access, the object should be opened with read-only access.</span></span> 
    
<span data-ttu-id="b1815-123">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="b1815-123">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="b1815-124">Permite que **OpenEntry** se devuelva correctamente, posiblemente antes de que el objeto esté completamente disponible para el cliente que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="b1815-124">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="b1815-125">Si el objeto no está disponible, la realización de una llamada de objeto subsiguiente puede generar un error.</span><span class="sxs-lookup"><span data-stu-id="b1815-125">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="b1815-126">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="b1815-126">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="b1815-127">Solicita el permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="b1815-127">Requests read/write permission.</span></span> <span data-ttu-id="b1815-128">De forma predeterminada, los objetos se abren con acceso de solo lectura y los clientes no deben trabajar en el supuesto de que se ha concedido el permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="b1815-128">By default, objects are opened with read-only access, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
<span data-ttu-id="b1815-129">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="b1815-129">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="b1815-130">Muestra los elementos que están marcados actualmente como eliminados temporalmente, es decir, se encuentran en la fase de retención de elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="b1815-130">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="b1815-131">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="b1815-131">_lpulObjType_</span></span>
  
> <span data-ttu-id="b1815-132">contempla Un puntero al tipo del objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="b1815-132">[out] A pointer to the opened object's type.</span></span>
    
 <span data-ttu-id="b1815-133">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="b1815-133">_lppUnk_</span></span>
  
> <span data-ttu-id="b1815-134">contempla Un puntero a un puntero a la implementación de la interfaz que se va a usar para obtener acceso al objeto Open.</span><span class="sxs-lookup"><span data-stu-id="b1815-134">[out] A pointer to a pointer to the interface implementation to use to access the open object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b1815-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b1815-135">Return value</span></span>

<span data-ttu-id="b1815-136">S_OK</span><span class="sxs-lookup"><span data-stu-id="b1815-136">S_OK</span></span> 
  
> <span data-ttu-id="b1815-137">El objeto se abrió correctamente.</span><span class="sxs-lookup"><span data-stu-id="b1815-137">The object was successfully opened.</span></span>
    
<span data-ttu-id="b1815-138">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="b1815-138">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="b1815-139">Puede que el usuario no tenga permisos suficientes para abrir el objeto o que se haya intentado abrir un objeto de solo lectura con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="b1815-139">Either the user has insufficient permissions to open the object or an attempt was made to open a read-only object with read/write permission.</span></span>
    
<span data-ttu-id="b1815-140">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="b1815-140">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="b1815-141">El identificador de entrada especificado por _lpEntryID_ no representa un objeto.</span><span class="sxs-lookup"><span data-stu-id="b1815-141">The entry identifier specified by  _lpEntryID_ does not represent an object.</span></span> 
    
<span data-ttu-id="b1815-142">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="b1815-142">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="b1815-143">El identificador de entrada en el parámetro _lpEntryID_ no tiene un formato reconocido por el contenedor.</span><span class="sxs-lookup"><span data-stu-id="b1815-143">The entry identifier in the  _lpEntryID_ parameter is not of a format recognized by the container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b1815-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b1815-144">Remarks</span></span>

<span data-ttu-id="b1815-145">El método **IMAPIContainer:: OpenEntry** abre un objeto a lo largo de un contenedor y devuelve un puntero a una implementación de interfaz que se va a usar para obtener más acceso.</span><span class="sxs-lookup"><span data-stu-id="b1815-145">The **IMAPIContainer::OpenEntry** method opens an object throughout a container and returns a pointer to an interface implementation to use for further access.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b1815-146">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="b1815-146">Notes to callers</span></span>

<span data-ttu-id="b1815-147">Dado que los proveedores de servicios no son necesarios para devolver una implementación de interfaz del tipo especificado por el identificador de interfaz en el parámetro _lpInterface_ , compruebe el valor al que señala el parámetro _lpulObjType_ .</span><span class="sxs-lookup"><span data-stu-id="b1815-147">Because service providers are not required to return an interface implementation of the type specified by the interface identifier in the  _lpInterface_ parameter, check the value pointed to by the  _lpulObjType_ parameter.</span></span> <span data-ttu-id="b1815-148">Si es necesario, convierta el puntero devuelto en _lppUnk_ en un puntero del tipo apropiado.</span><span class="sxs-lookup"><span data-stu-id="b1815-148">If necessary, cast the pointer returned in  _lppUnk_ to a pointer of the appropriate type.</span></span> 
  
<span data-ttu-id="b1815-149">De forma predeterminada, los proveedores de servicios abren objetos con acceso de solo lectura a menos que establezcas la marca MAPI_MODIFY o MAPI_BEST_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="b1815-149">By default, service providers open objects with read-only access unless you set either the MAPI_MODIFY or MAPI_BEST_ACCESS flag.</span></span> <span data-ttu-id="b1815-150">Cuando se establece una de estas marcas, los proveedores de servicios intentan devolver un objeto modificable.</span><span class="sxs-lookup"><span data-stu-id="b1815-150">When one of these flags is set, service providers attempt to return a modifiable object.</span></span> <span data-ttu-id="b1815-151">Sin embargo, no suponga que, porque solicitó un objeto modificable que el objeto abierto tiene permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="b1815-151">However, do not assume that because you requested a modifiable object that the opened object has read/write permission.</span></span> <span data-ttu-id="b1815-152">Planee la posibilidad de que una modificación posterior dé error o recupere la propiedad **PR_ACCESS_LEVEL** del objeto para determinar el nivel de acceso concedido por **OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="b1815-152">Either plan for the chance of a subsequent modification to fail or retrieve the object's **PR_ACCESS_LEVEL** property to determine the access level granted by **OpenEntry**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b1815-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="b1815-153">See also</span></span>



[<span data-ttu-id="b1815-154">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b1815-154">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)

