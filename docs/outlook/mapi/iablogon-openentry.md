---
title: IABLogonOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenEntry
api_type:
- COM
ms.assetid: 1cfb82f7-5215-4faa-af25-5b1da7e31209
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 70f61ef553350f08eed96c1ee4e9ab790359d1fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348940"
---
# <a name="iablogonopenentry"></a><span data-ttu-id="bb3fa-103">IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="bb3fa-103">IABLogon::OpenEntry</span></span>

  
  
<span data-ttu-id="bb3fa-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb3fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb3fa-105">Abre un contenedor, un usuario de mensajería o una lista de distribución y devuelve un puntero a una implementación de interfaz para proporcionar más acceso.</span><span class="sxs-lookup"><span data-stu-id="bb3fa-105">Opens a container, messaging user, or distribution list, and returns a pointer to an interface implementation to provide further access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="bb3fa-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="bb3fa-106">Parameters</span></span>

 <span data-ttu-id="bb3fa-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="bb3fa-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="bb3fa-108">a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="bb3fa-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="bb3fa-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="bb3fa-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="bb3fa-110">a Un puntero al identificador de entrada del contenedor, el usuario de mensajería o la lista de distribución que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="bb3fa-110">[in] A pointer to the entry identifier of the container, messaging user, or distribution list to open.</span></span>
    
 <span data-ttu-id="bb3fa-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="bb3fa-111">_lpInterface_</span></span>
  
> <span data-ttu-id="bb3fa-112">a Puntero al identificador de interfaz (IID) que representa la interfaz que se va a utilizar para tener acceso al objeto Open.</span><span class="sxs-lookup"><span data-stu-id="bb3fa-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the open object.</span></span> <span data-ttu-id="bb3fa-113">Si se pasa NULL, se devuelve el identificador de la interfaz estándar del objeto.</span><span class="sxs-lookup"><span data-stu-id="bb3fa-113">Passing NULL returns the identifier for the object's standard interface.</span></span> <span data-ttu-id="bb3fa-114">Para los contenedores, la interfaz estándar es [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="bb3fa-114">For containers, the standard interface is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="bb3fa-115">Las interfaces estándar para los objetos de la libreta de direcciones son [IDistList: IMAPIContainer](idistlistimapicontainer.md) para una lista de distribución y [IMailUser: IMAPIProp](imailuserimapiprop.md) para un usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="bb3fa-115">The standard interfaces for address book objects are [IDistList : IMAPIContainer](idistlistimapicontainer.md) for a distribution list and [IMailUser : IMAPIProp](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="bb3fa-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bb3fa-116">_ulFlags_</span></span>
  
> <span data-ttu-id="bb3fa-117">a Máscara de máscara de marcadores que controla cómo se abre el objeto.</span><span class="sxs-lookup"><span data-stu-id="bb3fa-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="bb3fa-118">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="bb3fa-118">The following flags can be set:</span></span>
    
<span data-ttu-id="bb3fa-119">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="bb3fa-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="bb3fa-120">Solicita que el objeto se abra con los permisos de red máximos permitidos para el usuario y el acceso máximo a la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="bb3fa-120">Requests that the object be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="bb3fa-121">Por ejemplo, si el cliente tiene permiso de lectura y escritura, el objeto debe abrirse con permiso de lectura y escritura; Si el cliente tiene permiso de solo lectura, el objeto debe abrirse con permiso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bb3fa-121">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only permission, the object should be opened with read-only permission.</span></span>
    
<span data-ttu-id="bb3fa-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="bb3fa-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="bb3fa-123">Permite que el método **OpenEntry** se devuelva correctamente, posiblemente antes de que el cliente de la llamada haya tenido acceso total al objeto.</span><span class="sxs-lookup"><span data-stu-id="bb3fa-123">Allows the **OpenEntry** method to return successfully, possibly before the calling client has fully accessed the object.</span></span> <span data-ttu-id="bb3fa-124">Si no se tiene acceso al objeto, realizar una llamada subsiguiente a un objeto puede generar un error.</span><span class="sxs-lookup"><span data-stu-id="bb3fa-124">If the object is not accessed, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="bb3fa-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="bb3fa-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="bb3fa-126">Solicita el permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="bb3fa-126">Requests read/write permission.</span></span> <span data-ttu-id="bb3fa-127">De forma predeterminada, los objetos se abren con acceso de solo lectura y los clientes no deben asumir que se ha concedido el permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="bb3fa-127">By default, objects are opened with read-only access, and clients should not assume that read/write permission has been granted.</span></span>
    
 <span data-ttu-id="bb3fa-128">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="bb3fa-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="bb3fa-129">contempla Un puntero al tipo del objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="bb3fa-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="bb3fa-130">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="bb3fa-130">_lppUnk_</span></span>
  
> <span data-ttu-id="bb3fa-131">contempla Un puntero a un puntero al objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="bb3fa-131">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bb3fa-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bb3fa-132">Remarks</span></span>

<span data-ttu-id="bb3fa-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="bb3fa-133">S_OK</span></span> 
  
> <span data-ttu-id="bb3fa-134">El objeto se abrió correctamente.</span><span class="sxs-lookup"><span data-stu-id="bb3fa-134">The object was successfully opened.</span></span>
    
<span data-ttu-id="bb3fa-135">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="bb3fa-135">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="bb3fa-136">Puede que el usuario no tenga permisos suficientes para abrir el objeto o que se haya intentado abrir un objeto de solo lectura con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="bb3fa-136">Either the user has insufficient permissions to open the object, or an attempt was made to open a read-only object with read/write permission.</span></span>
    
<span data-ttu-id="bb3fa-137">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="bb3fa-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="bb3fa-138">El identificador de entrada especificado por _lpEntryID_ no representa un objeto.</span><span class="sxs-lookup"><span data-stu-id="bb3fa-138">The entry identifier specified by  _lpEntryID_ does not represent an object.</span></span> 
    
<span data-ttu-id="bb3fa-139">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="bb3fa-139">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="bb3fa-140">El identificador de entrada en el parámetro _lpEntryID_ no tiene un formato reconocido por el proveedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="bb3fa-140">The entry identifier in the  _lpEntryID_ parameter is not of a format recognized by the address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="bb3fa-141">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bb3fa-141">Remarks</span></span>

<span data-ttu-id="bb3fa-142">MAPI llama al método **OpenEntry** para abrir un contenedor, un usuario de mensajería o una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="bb3fa-142">MAPI calls the **OpenEntry** method to open a container, messaging user, or distribution list.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="bb3fa-143">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="bb3fa-143">Notes to implementers</span></span>

<span data-ttu-id="bb3fa-144">Antes de que MAPI llame a su método **OpenEntry** , determina que el identificador de entrada en el parámetro _lpEntryID_ le pertenece y no a otro proveedor.</span><span class="sxs-lookup"><span data-stu-id="bb3fa-144">Before MAPI calls your **OpenEntry** method, it determines that the entry identifier in the  _lpEntryID_ parameter belongs to you and not to another provider.</span></span> <span data-ttu-id="bb3fa-145">MAPI hace esto haciendo coincidir la estructura [MAPIUID](mapiuid.md) del identificador de entrada con el **MAPIUID** que ha registrado llamando al método [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) al iniciar.</span><span class="sxs-lookup"><span data-stu-id="bb3fa-145">MAPI does this by matching the [MAPIUID](mapiuid.md) structure in the entry identifier with the **MAPIUID** that you registered by calling the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method at startup.</span></span> 
  
<span data-ttu-id="bb3fa-146">Abra el objeto como de solo lectura, a menos que el marcador MAPI_MODIFY o MAPI_BEST_ACCESS esté establecido en el parámetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="bb3fa-146">Open the object as read-only, unless the MAPI_MODIFY or MAPI_BEST_ACCESS flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="bb3fa-147">Si no permite la modificación del objeto solicitado, no abra el objeto en absoluto y devuelva MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="bb3fa-147">If you do not allow modification for the requested object, do not open the object at all and return MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="bb3fa-148">Si MAPI pasa NULL para _lpEntryID_, abra el contenedor raíz en la jerarquía de contenedores.</span><span class="sxs-lookup"><span data-stu-id="bb3fa-148">If MAPI passes NULL for  _lpEntryID_, open the root container in your container hierarchy.</span></span>
  
<span data-ttu-id="bb3fa-149">El objeto que se le solicita que abra puede ser un objeto copiado de otro proveedor.</span><span class="sxs-lookup"><span data-stu-id="bb3fa-149">The object that you are being asked to open might be an object copied from another provider.</span></span> <span data-ttu-id="bb3fa-150">En este caso, será compatible con la propiedad **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="bb3fa-150">In this case, it will support the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property.</span></span> <span data-ttu-id="bb3fa-151">Si el objeto admite esta propiedad, llame al método [IMAPISupport:: OpenTemplateID](imapisupport-opentemplateid.md) para enlazar con el código de esta entrada en el proveedor externo, pasando **PR_TEMPLATEID** en el parámetro _LpTemplateID_ y 0 en el _ulTemplateFlags _parámetro.</span><span class="sxs-lookup"><span data-stu-id="bb3fa-151">If the object does support this property, call the [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) method to bind to code for this entry in the foreign provider, passing **PR_TEMPLATEID** in the  _lpTemplateID_ parameter and 0 in the  _ulTemplateFlags_ parameter.</span></span> <span data-ttu-id="bb3fa-152">**IMAPISupport:: OpenTemplateID** pasa esta información al proveedor externo en una llamada al método [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md) del proveedor externo.</span><span class="sxs-lookup"><span data-stu-id="bb3fa-152">**IMAPISupport::OpenTemplateID** passes this information to the foreign provider in a call to the foreign provider's [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) method.</span></span> <span data-ttu-id="bb3fa-153">Si **IMAPISupport:: OpenTemplateID** genera un error, normalmente porque el proveedor externo no está disponible o no está incluido en el perfil, intente continuar tratando la entrada independiente como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bb3fa-153">If **IMAPISupport::OpenTemplateID** raises an error, usually because the foreign provider is unavailable or not included in the profile, try to continue by treating the unbound entry as read-only.</span></span> <span data-ttu-id="bb3fa-154">Para obtener más información acerca de cómo abrir entradas de la libreta de direcciones externa, consulte [actuar como proveedor de la libreta de direcciones de host](acting-as-a-host-address-book-provider.md).</span><span class="sxs-lookup"><span data-stu-id="bb3fa-154">For more information about opening foreign address book entries, see [Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bb3fa-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb3fa-155">See also</span></span>



[<span data-ttu-id="bb3fa-156">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bb3fa-156">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

