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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409233"
---
# <a name="iablogonopenentry"></a><span data-ttu-id="82667-103">IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="82667-103">IABLogon::OpenEntry</span></span>

  
  
<span data-ttu-id="82667-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82667-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82667-105">Abre un contenedor, un usuario de mensajería o una lista de distribución y devuelve un puntero a una implementación de interfaz para proporcionar acceso adicional.</span><span class="sxs-lookup"><span data-stu-id="82667-105">Opens a container, messaging user, or distribution list, and returns a pointer to an interface implementation to provide further access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="82667-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="82667-106">Parameters</span></span>

 <span data-ttu-id="82667-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="82667-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="82667-108">[entrada] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="82667-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="82667-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="82667-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="82667-110">[entrada] Puntero al identificador de entrada del contenedor, usuario de mensajería o lista de distribución que se abrirá.</span><span class="sxs-lookup"><span data-stu-id="82667-110">[in] A pointer to the entry identifier of the container, messaging user, or distribution list to open.</span></span>
    
 <span data-ttu-id="82667-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="82667-111">_lpInterface_</span></span>
  
> <span data-ttu-id="82667-112">[entrada] Puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para tener acceso al objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="82667-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the open object.</span></span> <span data-ttu-id="82667-113">Si se pasa NULL, se devuelve el identificador de la interfaz estándar del objeto.</span><span class="sxs-lookup"><span data-stu-id="82667-113">Passing NULL returns the identifier for the object's standard interface.</span></span> <span data-ttu-id="82667-114">Para contenedores, la interfaz estándar [es IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="82667-114">For containers, the standard interface is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="82667-115">Las interfaces estándar para objetos de libreta de direcciones son [IDistList: IMAPIContainer](idistlistimapicontainer.md) para una lista de distribución e [IMailUser : IMAPIProp](imailuserimapiprop.md) para un usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="82667-115">The standard interfaces for address book objects are [IDistList : IMAPIContainer](idistlistimapicontainer.md) for a distribution list and [IMailUser : IMAPIProp](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="82667-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="82667-116">_ulFlags_</span></span>
  
> <span data-ttu-id="82667-117">[entrada] Máscara de bits de marcas que controla cómo se abre el objeto.</span><span class="sxs-lookup"><span data-stu-id="82667-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="82667-118">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="82667-118">The following flags can be set:</span></span>
    
<span data-ttu-id="82667-119">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="82667-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="82667-120">Solicita que el objeto se abra con los permisos de red máximos permitidos para el usuario y el acceso máximo a la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="82667-120">Requests that the object be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="82667-121">Por ejemplo, si el cliente tiene permiso de lectura y escritura, el objeto debe abrirse con permiso de lectura y escritura; si el cliente tiene permiso de solo lectura, el objeto debe abrirse con permiso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="82667-121">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only permission, the object should be opened with read-only permission.</span></span>
    
<span data-ttu-id="82667-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="82667-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="82667-123">Permite que **el método OpenEntry** vuelva correctamente, posiblemente antes de que el cliente de llamada tenga acceso al objeto por completo.</span><span class="sxs-lookup"><span data-stu-id="82667-123">Allows the **OpenEntry** method to return successfully, possibly before the calling client has fully accessed the object.</span></span> <span data-ttu-id="82667-124">Si no se tiene acceso al objeto, realizar una llamada a objeto posterior puede generar un error.</span><span class="sxs-lookup"><span data-stu-id="82667-124">If the object is not accessed, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="82667-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="82667-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="82667-126">Solicita permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="82667-126">Requests read/write permission.</span></span> <span data-ttu-id="82667-127">De forma predeterminada, los objetos se abren con acceso de solo lectura y los clientes no deben suponer que se ha concedido permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="82667-127">By default, objects are opened with read-only access, and clients should not assume that read/write permission has been granted.</span></span>
    
 <span data-ttu-id="82667-128">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="82667-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="82667-129">[salida] Puntero al tipo del objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="82667-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="82667-130">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="82667-130">_lppUnk_</span></span>
  
> <span data-ttu-id="82667-131">[salida] Puntero a un puntero al objeto abierto.</span><span class="sxs-lookup"><span data-stu-id="82667-131">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="82667-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="82667-132">Remarks</span></span>

<span data-ttu-id="82667-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="82667-133">S_OK</span></span> 
  
> <span data-ttu-id="82667-134">El objeto se abrió correctamente.</span><span class="sxs-lookup"><span data-stu-id="82667-134">The object was successfully opened.</span></span>
    
<span data-ttu-id="82667-135">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="82667-135">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="82667-136">El usuario no tiene permisos suficientes para abrir el objeto o se intentó abrir un objeto de solo lectura con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="82667-136">Either the user has insufficient permissions to open the object, or an attempt was made to open a read-only object with read/write permission.</span></span>
    
<span data-ttu-id="82667-137">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="82667-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="82667-138">El identificador de entrada especificado  _por lpEntryID_ no representa un objeto.</span><span class="sxs-lookup"><span data-stu-id="82667-138">The entry identifier specified by  _lpEntryID_ does not represent an object.</span></span> 
    
<span data-ttu-id="82667-139">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="82667-139">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="82667-140">El identificador de entrada en  _el parámetro lpEntryID_ no tiene un formato reconocido por el proveedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="82667-140">The entry identifier in the  _lpEntryID_ parameter is not of a format recognized by the address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="82667-141">Comentarios</span><span class="sxs-lookup"><span data-stu-id="82667-141">Remarks</span></span>

<span data-ttu-id="82667-142">MAPI llama al **método OpenEntry** para abrir un contenedor, un usuario de mensajería o una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="82667-142">MAPI calls the **OpenEntry** method to open a container, messaging user, or distribution list.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="82667-143">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="82667-143">Notes to implementers</span></span>

<span data-ttu-id="82667-144">Antes de que MAPI llame **al método OpenEntry,** determina que el identificador de entrada del parámetro  _lpEntryID_ pertenece a usted y no a otro proveedor.</span><span class="sxs-lookup"><span data-stu-id="82667-144">Before MAPI calls your **OpenEntry** method, it determines that the entry identifier in the  _lpEntryID_ parameter belongs to you and not to another provider.</span></span> <span data-ttu-id="82667-145">MAPI hace esto al hacer coincidir la estructura [MAPIUID](mapiuid.md) en el identificador de entrada con el **MAPIUID** que registró llamando al método [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) en el inicio.</span><span class="sxs-lookup"><span data-stu-id="82667-145">MAPI does this by matching the [MAPIUID](mapiuid.md) structure in the entry identifier with the **MAPIUID** that you registered by calling the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method at startup.</span></span> 
  
<span data-ttu-id="82667-146">Abra el objeto como de solo lectura, a menos MAPI_MODIFY o MAPI_BEST_ACCESS marca esté establecida en el _parámetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="82667-146">Open the object as read-only, unless the MAPI_MODIFY or MAPI_BEST_ACCESS flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="82667-147">Si no permite la modificación del objeto solicitado, no abra el objeto en absoluto y devuelva MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="82667-147">If you do not allow modification for the requested object, do not open the object at all and return MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="82667-148">Si MAPI pasa NULL para  _lpEntryID,_ abra el contenedor raíz en la jerarquía de contenedores.</span><span class="sxs-lookup"><span data-stu-id="82667-148">If MAPI passes NULL for  _lpEntryID_, open the root container in your container hierarchy.</span></span>
  
<span data-ttu-id="82667-149">El objeto que se le pide que abra puede ser un objeto copiado de otro proveedor.</span><span class="sxs-lookup"><span data-stu-id="82667-149">The object that you are being asked to open might be an object copied from another provider.</span></span> <span data-ttu-id="82667-150">En este caso, admitirá la propiedad **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="82667-150">In this case, it will support the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property.</span></span> <span data-ttu-id="82667-151">Si el objeto admite esta propiedad, llame al método [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) para enlazar al código de esta entrada en el proveedor externo, pasando **PR_TEMPLATEID** en el parámetro _lpTemplateID_ y 0 en el parámetro _ulTemplateFlags._</span><span class="sxs-lookup"><span data-stu-id="82667-151">If the object does support this property, call the [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) method to bind to code for this entry in the foreign provider, passing **PR_TEMPLATEID** in the  _lpTemplateID_ parameter and 0 in the  _ulTemplateFlags_ parameter.</span></span> <span data-ttu-id="82667-152">**IMAPISupport::OpenTemplateID** pasa esta información al proveedor externo en una llamada al método [IABLogon::OpenTemplateID del](iablogon-opentemplateid.md) proveedor externo.</span><span class="sxs-lookup"><span data-stu-id="82667-152">**IMAPISupport::OpenTemplateID** passes this information to the foreign provider in a call to the foreign provider's [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) method.</span></span> <span data-ttu-id="82667-153">Si **IMAPISupport::OpenTemplateID** genera un error, normalmente porque el proveedor externo no está disponible o no está incluido en el perfil, intente continuar tratando la entrada independiente como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="82667-153">If **IMAPISupport::OpenTemplateID** raises an error, usually because the foreign provider is unavailable or not included in the profile, try to continue by treating the unbound entry as read-only.</span></span> <span data-ttu-id="82667-154">Para obtener más información acerca de cómo abrir entradas de libretas de direcciones externa, vea [Actuar como proveedor de libretas de direcciones host.](acting-as-a-host-address-book-provider.md)</span><span class="sxs-lookup"><span data-stu-id="82667-154">For more information about opening foreign address book entries, see [Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="82667-155">Consulte también</span><span class="sxs-lookup"><span data-stu-id="82667-155">See also</span></span>



[<span data-ttu-id="82667-156">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="82667-156">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

