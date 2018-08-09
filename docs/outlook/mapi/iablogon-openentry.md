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
ms.openlocfilehash: 53dfb62bb33a4941e2b5627e729763101e24319d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817096"
---
# <a name="iablogonopenentry"></a><span data-ttu-id="0aed5-103">IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="0aed5-103">IABLogon::OpenEntry</span></span>

  
  
<span data-ttu-id="0aed5-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0aed5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0aed5-105">Se abre un contenedor, usuario o lista de distribución, de mensajería y devuelve un puntero a una implementación de interfaz para proporcionar más acceso.</span><span class="sxs-lookup"><span data-stu-id="0aed5-105">Opens a container, messaging user, or distribution list, and returns a pointer to an interface implementation to provide further access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="0aed5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0aed5-106">Parameters</span></span>

 <span data-ttu-id="0aed5-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="0aed5-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="0aed5-108">[entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="0aed5-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="0aed5-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="0aed5-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="0aed5-110">[entrada] Un puntero al identificador de entrada del contenedor, usuario o lista de distribución para abrir de mensajería.</span><span class="sxs-lookup"><span data-stu-id="0aed5-110">[in] A pointer to the entry identifier of the container, messaging user, or distribution list to open.</span></span>
    
 <span data-ttu-id="0aed5-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="0aed5-111">_lpInterface_</span></span>
  
> <span data-ttu-id="0aed5-112">[entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso al objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="0aed5-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the open object.</span></span> <span data-ttu-id="0aed5-113">Pasando NULL, devuelve el identificador de la interfaz del objeto estándar.</span><span class="sxs-lookup"><span data-stu-id="0aed5-113">Passing NULL returns the identifier for the object's standard interface.</span></span> <span data-ttu-id="0aed5-114">Para contenedores, es la interfaz estándar de [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="0aed5-114">For containers, the standard interface is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="0aed5-115">El estándar de interfaces de objetos de la libreta de direcciones son [IDistList: IMAPIContainer](idistlistimapicontainer.md) para obtener una lista de distribución y [IMailUser: IMAPIProp](imailuserimapiprop.md) para un usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="0aed5-115">The standard interfaces for address book objects are [IDistList : IMAPIContainer](idistlistimapicontainer.md) for a distribution list and [IMailUser : IMAPIProp](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="0aed5-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0aed5-116">_ulFlags_</span></span>
  
> <span data-ttu-id="0aed5-117">[entrada] Una máscara de bits de indicadores que controla cómo se abre el objeto.</span><span class="sxs-lookup"><span data-stu-id="0aed5-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="0aed5-118">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="0aed5-118">The following flags can be set:</span></span>
    
<span data-ttu-id="0aed5-119">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="0aed5-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="0aed5-120">Solicita que el objeto se abran con los permisos de red máximo permitidos para el acceso de usuarios y el número máximo de clientes aplicación.</span><span class="sxs-lookup"><span data-stu-id="0aed5-120">Requests that the object be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="0aed5-121">Por ejemplo, si el cliente no tiene permiso de lectura y escritura, se debe abrir el objeto con permisos de lectura y escritura; Si el cliente no tiene permiso de sólo lectura, se debe abrir el objeto con permiso de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="0aed5-121">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only permission, the object should be opened with read-only permission.</span></span>
    
<span data-ttu-id="0aed5-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="0aed5-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="0aed5-123">Permite que el método **OpenEntry** correctamente, devolver, posiblemente, antes de que el cliente de la llamada totalmente tener acceso a los objetos.</span><span class="sxs-lookup"><span data-stu-id="0aed5-123">Allows the **OpenEntry** method to return successfully, possibly before the calling client has fully accessed the object.</span></span> <span data-ttu-id="0aed5-124">Si no se tiene acceso al objeto, realizar una llamada de objeto posteriores puede provocar un error.</span><span class="sxs-lookup"><span data-stu-id="0aed5-124">If the object is not accessed, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="0aed5-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="0aed5-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="0aed5-126">Las solicitudes de permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="0aed5-126">Requests read/write permission.</span></span> <span data-ttu-id="0aed5-127">De forma predeterminada, los objetos se abren con acceso de solo lectura y clientes no deben asumir que se ha concedido permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="0aed5-127">By default, objects are opened with read-only access, and clients should not assume that read/write permission has been granted.</span></span>
    
 <span data-ttu-id="0aed5-128">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="0aed5-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="0aed5-129">[out] Un puntero al tipo del objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="0aed5-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="0aed5-130">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="0aed5-130">_lppUnk_</span></span>
  
> <span data-ttu-id="0aed5-131">[out] Un puntero a un puntero al objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="0aed5-131">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0aed5-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0aed5-132">Remarks</span></span>

<span data-ttu-id="0aed5-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="0aed5-133">S_OK</span></span> 
  
> <span data-ttu-id="0aed5-134">El objeto se abrió correctamente.</span><span class="sxs-lookup"><span data-stu-id="0aed5-134">The object was successfully opened.</span></span>
    
<span data-ttu-id="0aed5-135">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="0aed5-135">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="0aed5-136">Puede que el usuario no tiene permisos suficientes para abrir el objeto o se ha intentado abrir un objeto de sólo lectura con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="0aed5-136">Either the user has insufficient permissions to open the object, or an attempt was made to open a read-only object with read/write permission.</span></span>
    
<span data-ttu-id="0aed5-137">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="0aed5-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="0aed5-138">El identificador de entrada especificado por _lpEntryID_ no representan un objeto.</span><span class="sxs-lookup"><span data-stu-id="0aed5-138">The entry identifier specified by  _lpEntryID_ does not represent an object.</span></span> 
    
<span data-ttu-id="0aed5-139">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="0aed5-139">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="0aed5-140">El identificador de entrada en el parámetro _lpEntryID_ no es un formato reconocido por el proveedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="0aed5-140">The entry identifier in the  _lpEntryID_ parameter is not of a format recognized by the address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0aed5-141">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0aed5-141">Remarks</span></span>

<span data-ttu-id="0aed5-142">MAPI llama al método de **OpenEntry** para abrir un contenedor, usuario o lista de distribución de mensajería.</span><span class="sxs-lookup"><span data-stu-id="0aed5-142">MAPI calls the **OpenEntry** method to open a container, messaging user, or distribution list.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="0aed5-143">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="0aed5-143">Notes to implementers</span></span>

<span data-ttu-id="0aed5-144">Antes de MAPI llama a su método **OpenEntry** , determina que el identificador de entrada en el parámetro _lpEntryID_ pertenece a usted y no a otro proveedor.</span><span class="sxs-lookup"><span data-stu-id="0aed5-144">Before MAPI calls your **OpenEntry** method, it determines that the entry identifier in the  _lpEntryID_ parameter belongs to you and not to another provider.</span></span> <span data-ttu-id="0aed5-145">Para ello, MAPI que coincidan con la estructura [MAPIUID](mapiuid.md) en el identificador de entrada con el **MAPIUID** que se ha registrado llamando al método [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) en el inicio.</span><span class="sxs-lookup"><span data-stu-id="0aed5-145">MAPI does this by matching the [MAPIUID](mapiuid.md) structure in the entry identifier with the **MAPIUID** that you registered by calling the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method at startup.</span></span> 
  
<span data-ttu-id="0aed5-146">Abra el objeto como de solo lectura, a menos que se establece la marca MAPI_MODIFY o MAPI_BEST_ACCESS en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="0aed5-146">Open the object as read-only, unless the MAPI_MODIFY or MAPI_BEST_ACCESS flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="0aed5-147">Si no permite la modificación para el objeto solicitado, no abra el objeto en absoluto y devolver MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="0aed5-147">If you do not allow modification for the requested object, do not open the object at all and return MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="0aed5-148">Si MAPI pasa NULL para _lpEntryID_, abra el contenedor raíz en la jerarquía del contenedor.</span><span class="sxs-lookup"><span data-stu-id="0aed5-148">If MAPI passes NULL for  _lpEntryID_, open the root container in your container hierarchy.</span></span>
  
<span data-ttu-id="0aed5-149">El objeto que se le pide para abrir podría ser un objeto copiado de otro proveedor.</span><span class="sxs-lookup"><span data-stu-id="0aed5-149">The object that you are being asked to open might be an object copied from another provider.</span></span> <span data-ttu-id="0aed5-150">En este caso, admitirá la propiedad **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0aed5-150">In this case, it will support the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property.</span></span> <span data-ttu-id="0aed5-151">Si el objeto es compatible con esta propiedad, llame al método [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) para enlazar al código para esta entrada en el proveedor extranjero, pasando **PR_TEMPLATEID** en el parámetro _lpTemplateID_ y 0 en la ulTemplateFlags _ _parámetro.</span><span class="sxs-lookup"><span data-stu-id="0aed5-151">If the object does support this property, call the [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) method to bind to code for this entry in the foreign provider, passing **PR_TEMPLATEID** in the  _lpTemplateID_ parameter and 0 in the  _ulTemplateFlags_ parameter.</span></span> <span data-ttu-id="0aed5-152">**IMAPISupport::OpenTemplateID** pasa esta información al proveedor de externa en una llamada al método [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) del proveedor externo.</span><span class="sxs-lookup"><span data-stu-id="0aed5-152">**IMAPISupport::OpenTemplateID** passes this information to the foreign provider in a call to the foreign provider's [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) method.</span></span> <span data-ttu-id="0aed5-153">Si **IMAPISupport::OpenTemplateID** genera un error, suele ser debido a que el proveedor externo no está disponible o no está incluido en el perfil, intente continuar por el tratamiento de la entrada independiente como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0aed5-153">If **IMAPISupport::OpenTemplateID** raises an error, usually because the foreign provider is unavailable or not included in the profile, try to continue by treating the unbound entry as read-only.</span></span> <span data-ttu-id="0aed5-154">Para obtener más información acerca de cómo abrir entradas de la libreta de direcciones externa, vea [actuar como un proveedor de libreta de direcciones de Host](acting-as-a-host-address-book-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0aed5-154">For more information about opening foreign address book entries, see [Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0aed5-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="0aed5-155">See also</span></span>



[<span data-ttu-id="0aed5-156">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0aed5-156">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

