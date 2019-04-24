---
title: IProfSect IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfSect
api_type:
- COM
ms.assetid: 4e704044-5230-4521-a0d2-b7c2f981c954
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 99ce944bec94a1e832f77fa8b0916ac1c76f6dc6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344796"
---
# <a name="iprofsect--imapiprop"></a><span data-ttu-id="704d2-103">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="704d2-103">IProfSect : IMAPIProp</span></span>

  
  
<span data-ttu-id="704d2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="704d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="704d2-105">Funciona con las propiedades de los objetos de sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="704d2-105">Works with the properties of profile section objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="704d2-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="704d2-106">Header file:</span></span>  <br/> |<span data-ttu-id="704d2-107">Mapix. h</span><span class="sxs-lookup"><span data-stu-id="704d2-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="704d2-108">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="704d2-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="704d2-109">Objetos de sección de perfil</span><span class="sxs-lookup"><span data-stu-id="704d2-109">Profile section objects</span></span>  <br/> |
|<span data-ttu-id="704d2-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="704d2-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="704d2-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="704d2-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="704d2-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="704d2-112">Called by:</span></span>  <br/> |<span data-ttu-id="704d2-113">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="704d2-113">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="704d2-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="704d2-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="704d2-115">IID_IProfSect</span><span class="sxs-lookup"><span data-stu-id="704d2-115">IID_IProfSect</span></span>  <br/> |
|<span data-ttu-id="704d2-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="704d2-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="704d2-117">LPPROFSECT</span><span class="sxs-lookup"><span data-stu-id="704d2-117">LPPROFSECT</span></span>  <br/> |
|<span data-ttu-id="704d2-118">Modelo de transacción:</span><span class="sxs-lookup"><span data-stu-id="704d2-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="704d2-119">No transactd</span><span class="sxs-lookup"><span data-stu-id="704d2-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="704d2-120">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="704d2-120">Vtable order</span></span>

<span data-ttu-id="704d2-121">Esta interfaz no tiene ningún método único.</span><span class="sxs-lookup"><span data-stu-id="704d2-121">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="704d2-122">**Propiedades requeridas**</span><span class="sxs-lookup"><span data-stu-id="704d2-122">**Required properties**</span></span>|<span data-ttu-id="704d2-123">**Access**</span><span class="sxs-lookup"><span data-stu-id="704d2-123">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="704d2-124">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="704d2-124">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="704d2-125">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="704d2-125">Read-only</span></span>  <br/> |
|<span data-ttu-id="704d2-126">**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="704d2-126">**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="704d2-127">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="704d2-127">Read-only</span></span>  <br/> |
   
## <a name="notes-to-callers"></a><span data-ttu-id="704d2-128">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="704d2-128">Notes to callers</span></span>

<span data-ttu-id="704d2-129">La interfaz **IProfSect** no tiene ningún método único propio, pero puede llamar a los métodos [IMAPIProp](imapipropiunknown.md) de la sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="704d2-129">The **IProfSect** interface does not have any unique methods of its own, but you can call the profile section's [IMAPIProp](imapipropiunknown.md) methods.</span></span> <span data-ttu-id="704d2-130">Existen algunas diferencias entre la implementación de **IProfSect** y otras implementaciones de **IMAPIProp**:</span><span class="sxs-lookup"><span data-stu-id="704d2-130">There are some differences between the **IProfSect** implementation and other implementations of **IMAPIProp**:</span></span>
  
- <span data-ttu-id="704d2-131">**IProfSect** no admite un modelo de transacción.</span><span class="sxs-lookup"><span data-stu-id="704d2-131">**IProfSect** does not support a transaction model.</span></span> 
    
- <span data-ttu-id="704d2-132">**IProfSect** no admite propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="704d2-132">**IProfSect** does not support named properties.</span></span> 
    
- <span data-ttu-id="704d2-133">**IProfSect** reserva el intervalo de identificadores 0x67F0 a 0x67ff para las propiedades seguras.</span><span class="sxs-lookup"><span data-stu-id="704d2-133">**IProfSect** reserves the identifier range 0x67F0 to 0x67ff for secure properties.</span></span> 
    
<span data-ttu-id="704d2-134">No admitir un modelo de transacción significa que todos los cambios que se realizaron en una sección de perfil que sigue a las llamadas a los métodos [IMAPIProp:: CopyProps](imapiprop-copyprops.md) y [IMAPIProp:: CopyTo](imapiprop-copyto.md) se producen inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="704d2-134">Not supporting a transaction model means that all changes that were made to a profile section following calls to the [IMAPIProp::CopyProps](imapiprop-copyprops.md) and [IMAPIProp::CopyTo](imapiprop-copyto.md) methods occur immediately.</span></span> <span data-ttu-id="704d2-135">Las llamadas al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) se realizan correctamente pero no guardan realmente los cambios.</span><span class="sxs-lookup"><span data-stu-id="704d2-135">Calls to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method succeed but do not actually save any changes.</span></span> 
  
<span data-ttu-id="704d2-136">Para protegerse de los cambios que se producen prematuramente, los proveedores de servicios deben hacer copias de sus secciones de perfil que se muestran a los usuarios a través de las hojas de propiedades.</span><span class="sxs-lookup"><span data-stu-id="704d2-136">To be protected from changes that occur prematurely, service providers need to make copies of their profile sections that are displayed to users through property sheets.</span></span> <span data-ttu-id="704d2-137">Las hojas de propiedades deben funcionar con la copia, en lugar de con la sección de perfil real.</span><span class="sxs-lookup"><span data-stu-id="704d2-137">The property sheets should work with the copy, instead of the real profile section.</span></span> <span data-ttu-id="704d2-138">Cuando el usuario hace clic en el botón **Aceptar** para comprobar que los cambios son correctos, los cambios se pueden guardar en la sección de perfil real.</span><span class="sxs-lookup"><span data-stu-id="704d2-138">When the user clicks the **OK** button to verify that the changes are accurate, the changes can be saved to the real profile section.</span></span> 
  
<span data-ttu-id="704d2-139">Para implementar una hoja de propiedades mediante una sección de perfil copiada, use el procedimiento siguiente:</span><span class="sxs-lookup"><span data-stu-id="704d2-139">To implement a property sheet by using a copied profile section, use the following procedure:</span></span>
  
1. <span data-ttu-id="704d2-140">Para abrir la sección de perfil, llame al método [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) o [IProviderAdmin:: OpenProfileSection](iprovideradmin-openprofilesection.md) .</span><span class="sxs-lookup"><span data-stu-id="704d2-140">Open the profile section by calling the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) or [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) method.</span></span> 
    
2. <span data-ttu-id="704d2-141">Llame a la función [CreateIProp](createiprop.md) para recuperar un objeto de datos de propiedad (un objeto que admita la interfaz **IPropData** .</span><span class="sxs-lookup"><span data-stu-id="704d2-141">Call the [CreateIProp](createiprop.md) function to retrieve a property data object — an object that supports the **IPropData** interface.</span></span> 
    
3. <span data-ttu-id="704d2-142">Llame al método [IMAPIProp:: CopyTo](imapiprop-copyto.md) de la sección de perfil para copiar las propiedades que aparecerán en la hoja de propiedades de la sección de perfil en el objeto de datos de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="704d2-142">Call the profile section's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties that will appear on the property sheet from the profile section to the property data object.</span></span> 
    
4. <span data-ttu-id="704d2-143">Llame al método [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md) para solicitar que el proveedor de servicios muestre una hoja de propiedades y pase un puntero al objeto de datos de la propiedad en el parámetro _lpConfigData_ .</span><span class="sxs-lookup"><span data-stu-id="704d2-143">Call the [IMAPISupport::DoConfigPropSheet](imapisupport-doconfigpropsheet.md) method to request that the service provider display a property sheet, and pass a pointer to the property data object in the  _lpConfigData_ parameter.</span></span> 
    
5. <span data-ttu-id="704d2-144">Cuando el usuario guarda los cambios en las propiedades de configuración en la hoja de propiedades, llame al método [IMAPIProp:: CopyTo](imapiprop-copyto.md) para copiar las propiedades del objeto de datos de la propiedad de nuevo en la sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="704d2-144">When the user saves changes to configuration properties in the property sheet, call the [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties from the property data object back to the profile section.</span></span> 
    
<span data-ttu-id="704d2-145">Las secciones de perfil, a diferencia de otros objetos, no admiten propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="704d2-145">Profile sections, unlike other objects, do not support named properties.</span></span> <span data-ttu-id="704d2-146">Los métodos [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) y [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md) devuelven MAPI_E_NO_SUPPORT si se llaman en un objeto de sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="704d2-146">The [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) and [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) methods return MAPI_E_NO_SUPPORT if they are called on a profile section object.</span></span> <span data-ttu-id="704d2-147">Si usa el método [IMAPIProp:: SetProps](imapiprop-setprops.md) para establecer los identificadores de propiedad del intervalo superior a 0x8000, se devolverá el tipo de propiedad PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="704d2-147">If you use the [IMAPIProp::SetProps](imapiprop-setprops.md) method to set property identifiers in the range above 0x8000, the PT_ERROR property type will be returned.</span></span> 
  
<span data-ttu-id="704d2-148">Las secciones de perfil reservan el intervalo de identificadores 0x67F0 a 0x67FF para las propiedades seguras.</span><span class="sxs-lookup"><span data-stu-id="704d2-148">Profile sections reserve the identifier range 0x67F0 to 0x67FF for secure properties.</span></span> <span data-ttu-id="704d2-149">Los proveedores de servicios pueden usar este intervalo para almacenar contraseñas y otras credenciales específicas del proveedor.</span><span class="sxs-lookup"><span data-stu-id="704d2-149">Service providers can use this range to store passwords and other provider-specific credentials.</span></span> <span data-ttu-id="704d2-150">Las propiedades de este rango no se devuelven en la lista completa de propiedades cuando se pasa NULL en el parámetro _lpPropTag_ del método [IMAPIProp:: GetProps](imapiprop-getprops.md) , y tampoco se devuelven en el parámetro _lppPropTagArray_ del [ Método IMAPIProp:: GetPropList](imapiprop-getproplist.md) .</span><span class="sxs-lookup"><span data-stu-id="704d2-150">Properties in this range are not returned in the complete list of properties when NULL is passed in the  _lpPropTag_ parameter of the [IMAPIProp::GetProps](imapiprop-getprops.md) method, nor are they returned in the  _lppPropTagArray_ parameter of the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> <span data-ttu-id="704d2-151">Las propiedades seguras deben ser solicitadas específicamente por sus identificadores.</span><span class="sxs-lookup"><span data-stu-id="704d2-151">Secure properties must be requested specifically by their identifiers.</span></span> 
  
<span data-ttu-id="704d2-152">MAPI proporciona una sección de perfil con la constante codificada de forma rígida MUID_PROFILE_INSTANCE como su identificador y **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) como su única propiedad.</span><span class="sxs-lookup"><span data-stu-id="704d2-152">MAPI furnishes a profile section with the hard-coded constant MUID_PROFILE_INSTANCE as its identifier and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) as its single property.</span></span> <span data-ttu-id="704d2-153">MAPI garantiza que el valor de la propiedad **PR_SEARCH_KEY** será único entre todos los perfiles creados.</span><span class="sxs-lookup"><span data-stu-id="704d2-153">MAPI ensures that the **PR_SEARCH_KEY** property value will be unique among all created profiles.</span></span> <span data-ttu-id="704d2-154">Use **PR_SEARCH_KEY** en lugar de **PR_PROFILE_NAME** cuando la exclusividad es importante, ya que es posible que un perfil eliminado siga seguido por otro perfil con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="704d2-154">Use **PR_SEARCH_KEY** instead of **PR_PROFILE_NAME** when uniqueness is important, because it is possible for a deleted profile to be followed by another profile with the same name.</span></span> 
  
<span data-ttu-id="704d2-155">Para obtener más información acerca de cómo usar secciones de perfil, consulte adMinistering proFiles [and Message Services](administering-profiles-and-message-services.md).</span><span class="sxs-lookup"><span data-stu-id="704d2-155">For more information about how to use profile sections, see [Administering Profiles and Message Services](administering-profiles-and-message-services.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="704d2-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="704d2-156">See also</span></span>



[<span data-ttu-id="704d2-157">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="704d2-157">MAPI Interfaces</span></span>](mapi-interfaces.md)

