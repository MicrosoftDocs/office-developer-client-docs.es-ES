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
ms.openlocfilehash: cd93866ae8823eb5897318fc2dda4e8432d974b0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578468"
---
# <a name="imapicontaineropenentry"></a><span data-ttu-id="54e4e-103">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="54e4e-103">IMAPIContainer::OpenEntry</span></span>

  
  
<span data-ttu-id="54e4e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54e4e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54e4e-105">Abre un objeto en el contenedor, la devolución de un puntero de interfaz para aún más el acceso.</span><span class="sxs-lookup"><span data-stu-id="54e4e-105">Opens an object in the container, returning an interface pointer for further access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="54e4e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="54e4e-106">Parameters</span></span>

 <span data-ttu-id="54e4e-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="54e4e-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="54e4e-108">[entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="54e4e-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="54e4e-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="54e4e-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="54e4e-110">[entrada] Un puntero al identificador de entrada del objeto que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="54e4e-110">[in] A pointer to the entry identifier of the object to open.</span></span> <span data-ttu-id="54e4e-111">Si _lpEntryID_ se establece en NULL, se abre el contenedor de nivel superior en la jerarquía del contenedor.</span><span class="sxs-lookup"><span data-stu-id="54e4e-111">If  _lpEntryID_ is set to NULL, the top-level container in the container's hierarchy is opened.</span></span> 
    
 <span data-ttu-id="54e4e-112">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="54e4e-112">_lpInterface_</span></span>
  
> <span data-ttu-id="54e4e-113">[entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso al objeto.</span><span class="sxs-lookup"><span data-stu-id="54e4e-113">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object.</span></span> <span data-ttu-id="54e4e-114">Si se pasa NULL da como resultado el identificador de la interfaz del objeto estándar que se devuelven.</span><span class="sxs-lookup"><span data-stu-id="54e4e-114">Passing NULL results in the identifier for the object's standard interface being returned.</span></span> <span data-ttu-id="54e4e-115">Para los mensajes, es la interfaz estándar de [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md); para las carpetas, es [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="54e4e-115">For messages, the standard interface is [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md); for folders, it is [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="54e4e-116">El estándar de interfaces de objetos de la libreta de direcciones son [IDistList: IMAPIContainer](idistlistimapicontainer.md) para obtener una lista de distribución y [IMailUser: IMAPIProp](imailuserimapiprop.md) para un usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="54e4e-116">The standard interfaces for address book objects are [IDistList : IMAPIContainer](idistlistimapicontainer.md) for a distribution list and [IMailUser : IMAPIProp](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="54e4e-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="54e4e-117">_ulFlags_</span></span>
  
> <span data-ttu-id="54e4e-118">[entrada] Una máscara de bits de indicadores que controla cómo se abre el objeto.</span><span class="sxs-lookup"><span data-stu-id="54e4e-118">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="54e4e-119">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="54e4e-119">The following flags can be set:</span></span>
    
<span data-ttu-id="54e4e-120">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="54e4e-120">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="54e4e-121">Solicita que el objeto se abrirá con los permisos de red máximo permitidos para el acceso de usuarios y el número máximo de clientes aplicación.</span><span class="sxs-lookup"><span data-stu-id="54e4e-121">Requests that the object will be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="54e4e-122">Por ejemplo, si el cliente no tiene permiso de lectura y escritura, se debe abrir el objeto con permisos de lectura y escritura; Si el cliente no tiene acceso de solo lectura, el objeto se debe abrir con acceso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="54e4e-122">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only access, the object should be opened with read-only access.</span></span> 
    
<span data-ttu-id="54e4e-123">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="54e4e-123">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="54e4e-124">Permite **OpenEntry** devolver de correctamente, posiblemente antes de que el objeto está totalmente disponible para el cliente de la llamada.</span><span class="sxs-lookup"><span data-stu-id="54e4e-124">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="54e4e-125">Si el objeto no está disponible, realizar una llamada de objeto posteriores puede provocar un error.</span><span class="sxs-lookup"><span data-stu-id="54e4e-125">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="54e4e-126">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="54e4e-126">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="54e4e-127">Las solicitudes de permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="54e4e-127">Requests read/write permission.</span></span> <span data-ttu-id="54e4e-128">De forma predeterminada, los objetos se abren con acceso de solo lectura y los clientes no deben trabajar en la suposición de que se ha concedido permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="54e4e-128">By default, objects are opened with read-only access, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
<span data-ttu-id="54e4e-129">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="54e4e-129">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="54e4e-130">Muestra los elementos que actualmente están marcados como suaves eliminan, es decir, se encuentran en la retención de elementos eliminados fase de tiempo.</span><span class="sxs-lookup"><span data-stu-id="54e4e-130">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="54e4e-131">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="54e4e-131">_lpulObjType_</span></span>
  
> <span data-ttu-id="54e4e-132">[out] Un puntero al tipo de objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="54e4e-132">[out] A pointer to the opened object's type.</span></span>
    
 <span data-ttu-id="54e4e-133">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="54e4e-133">_lppUnk_</span></span>
  
> <span data-ttu-id="54e4e-134">[out] Un puntero a un puntero a la implementación de la interfaz a usar para tener acceso al objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="54e4e-134">[out] A pointer to a pointer to the interface implementation to use to access the open object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="54e4e-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="54e4e-135">Return value</span></span>

<span data-ttu-id="54e4e-136">S_OK</span><span class="sxs-lookup"><span data-stu-id="54e4e-136">S_OK</span></span> 
  
> <span data-ttu-id="54e4e-137">El objeto se abrió correctamente.</span><span class="sxs-lookup"><span data-stu-id="54e4e-137">The object was successfully opened.</span></span>
    
<span data-ttu-id="54e4e-138">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="54e4e-138">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="54e4e-139">El usuario no tiene permisos suficientes para abrir el objeto o se ha intentado abrir un objeto de sólo lectura con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="54e4e-139">Either the user has insufficient permissions to open the object or an attempt was made to open a read-only object with read/write permission.</span></span>
    
<span data-ttu-id="54e4e-140">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="54e4e-140">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="54e4e-141">El identificador de entrada especificado por _lpEntryID_ no representan un objeto.</span><span class="sxs-lookup"><span data-stu-id="54e4e-141">The entry identifier specified by  _lpEntryID_ does not represent an object.</span></span> 
    
<span data-ttu-id="54e4e-142">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="54e4e-142">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="54e4e-143">El identificador de entrada en el parámetro _lpEntryID_ no es un formato reconocido por el contenedor.</span><span class="sxs-lookup"><span data-stu-id="54e4e-143">The entry identifier in the  _lpEntryID_ parameter is not of a format recognized by the container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="54e4e-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="54e4e-144">Remarks</span></span>

<span data-ttu-id="54e4e-145">El método **IMAPIContainer::OpenEntry** abre un objeto a lo largo de un contenedor y devuelve un puntero a una implementación de interfaz que se usará para aún más el acceso.</span><span class="sxs-lookup"><span data-stu-id="54e4e-145">The **IMAPIContainer::OpenEntry** method opens an object throughout a container and returns a pointer to an interface implementation to use for further access.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="54e4e-146">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="54e4e-146">Notes to callers</span></span>

<span data-ttu-id="54e4e-147">Dado que los proveedores de servicios no son necesarios para devolver una implementación de interfaz del tipo especificado por el identificador de interfaz en el parámetro _lpInterface_ , comprobar el valor al que señala el parámetro _lpulObjType_ .</span><span class="sxs-lookup"><span data-stu-id="54e4e-147">Because service providers are not required to return an interface implementation of the type specified by the interface identifier in the  _lpInterface_ parameter, check the value pointed to by the  _lpulObjType_ parameter.</span></span> <span data-ttu-id="54e4e-148">Si es necesario, convertir el puntero devuelto en _lppUnk_ a un puntero del tipo apropiado.</span><span class="sxs-lookup"><span data-stu-id="54e4e-148">If necessary, cast the pointer returned in  _lppUnk_ to a pointer of the appropriate type.</span></span> 
  
<span data-ttu-id="54e4e-149">De forma predeterminada, los proveedores de servicios abran objetos con acceso de sólo lectura a menos que establezca marca la MAPI_MODIFY o MAPI_BEST_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="54e4e-149">By default, service providers open objects with read-only access unless you set either the MAPI_MODIFY or MAPI_BEST_ACCESS flag.</span></span> <span data-ttu-id="54e4e-150">Cuando se establece una de estas marcas, proveedores de servicios intentan devolver un objeto modificable.</span><span class="sxs-lookup"><span data-stu-id="54e4e-150">When one of these flags is set, service providers attempt to return a modifiable object.</span></span> <span data-ttu-id="54e4e-151">Sin embargo, no asuma que debido a que se solicitó un objeto modificable que el objeto abierto tiene permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="54e4e-151">However, do not assume that because you requested a modifiable object that the opened object has read/write permission.</span></span> <span data-ttu-id="54e4e-152">Ya sea, la planeación de la posibilidad de que una modificación posterior para producir un error o recuperar la propiedad del objeto **PR_ACCESS_LEVEL** determinar el nivel de acceso concedido por **OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="54e4e-152">Either plan for the chance of a subsequent modification to fail or retrieve the object's **PR_ACCESS_LEVEL** property to determine the access level granted by **OpenEntry**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="54e4e-153">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="54e4e-153">See also</span></span>



[<span data-ttu-id="54e4e-154">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="54e4e-154">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)

