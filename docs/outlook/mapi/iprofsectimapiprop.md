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
ms.openlocfilehash: a8152a9cad7623a077cd9df3f678a9ada56e3960
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577964"
---
# <a name="iprofsect--imapiprop"></a><span data-ttu-id="bd0e1-103">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="bd0e1-103">IProfSect : IMAPIProp</span></span>

  
  
<span data-ttu-id="bd0e1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd0e1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd0e1-105">Funciona con las propiedades de objetos de sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="bd0e1-105">Works with the properties of profile section objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bd0e1-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="bd0e1-106">Header file:</span></span>  <br/> |<span data-ttu-id="bd0e1-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="bd0e1-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="bd0e1-108">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="bd0e1-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="bd0e1-109">Objetos de sección de perfil</span><span class="sxs-lookup"><span data-stu-id="bd0e1-109">Profile section objects</span></span>  <br/> |
|<span data-ttu-id="bd0e1-110">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="bd0e1-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="bd0e1-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="bd0e1-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="bd0e1-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="bd0e1-112">Called by:</span></span>  <br/> |<span data-ttu-id="bd0e1-113">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="bd0e1-113">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="bd0e1-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="bd0e1-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="bd0e1-115">IID_IProfSect</span><span class="sxs-lookup"><span data-stu-id="bd0e1-115">IID_IProfSect</span></span>  <br/> |
|<span data-ttu-id="bd0e1-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="bd0e1-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="bd0e1-117">LPPROFSECT</span><span class="sxs-lookup"><span data-stu-id="bd0e1-117">LPPROFSECT</span></span>  <br/> |
|<span data-ttu-id="bd0e1-118">Modelo de transacciones:</span><span class="sxs-lookup"><span data-stu-id="bd0e1-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="bd0e1-119">Nontransacted</span><span class="sxs-lookup"><span data-stu-id="bd0e1-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="bd0e1-120">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="bd0e1-120">Vtable order</span></span>

<span data-ttu-id="bd0e1-121">Esta interfaz no tiene ningún método único.</span><span class="sxs-lookup"><span data-stu-id="bd0e1-121">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="bd0e1-122">**Propiedades requeridas**</span><span class="sxs-lookup"><span data-stu-id="bd0e1-122">**Required properties**</span></span>|<span data-ttu-id="bd0e1-123">**Access**</span><span class="sxs-lookup"><span data-stu-id="bd0e1-123">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bd0e1-124">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bd0e1-124">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="bd0e1-125">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd0e1-125">Read-only</span></span>  <br/> |
|<span data-ttu-id="bd0e1-126">**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bd0e1-126">**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="bd0e1-127">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd0e1-127">Read-only</span></span>  <br/> |
   
## <a name="notes-to-callers"></a><span data-ttu-id="bd0e1-128">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="bd0e1-128">Notes to callers</span></span>

<span data-ttu-id="bd0e1-129">La interfaz **IProfSect** no tiene ningún método único, pero se puede llamar al perfil de los métodos de la sección [IMAPIProp](imapipropiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="bd0e1-129">The **IProfSect** interface does not have any unique methods of its own, but you can call the profile section's [IMAPIProp](imapipropiunknown.md) methods.</span></span> <span data-ttu-id="bd0e1-130">Existen algunas diferencias entre la implementación de **IProfSect** y otras implementaciones de **IMAPIProp**:</span><span class="sxs-lookup"><span data-stu-id="bd0e1-130">There are some differences between the **IProfSect** implementation and other implementations of **IMAPIProp**:</span></span>
  
- <span data-ttu-id="bd0e1-131">**IProfSect** no es compatible con un modelo de transacción.</span><span class="sxs-lookup"><span data-stu-id="bd0e1-131">**IProfSect** does not support a transaction model.</span></span> 
    
- <span data-ttu-id="bd0e1-132">**IProfSect** no es compatible con las propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="bd0e1-132">**IProfSect** does not support named properties.</span></span> 
    
- <span data-ttu-id="bd0e1-133">**IProfSect** se reserva el intervalo de identificadores de 0x67F0 a 0x67ff para propiedades seguras.</span><span class="sxs-lookup"><span data-stu-id="bd0e1-133">**IProfSect** reserves the identifier range 0x67F0 to 0x67ff for secure properties.</span></span> 
    
<span data-ttu-id="bd0e1-134">No se admite un modelo de transacción significa que todos los cambios que se han realizado en una siguiente de sección de perfil llamadas a la [IMAPIProp::CopyProps](imapiprop-copyprops.md) y métodos de [IMAPIProp::CopyTo](imapiprop-copyto.md) se producen inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="bd0e1-134">Not supporting a transaction model means that all changes that were made to a profile section following calls to the [IMAPIProp::CopyProps](imapiprop-copyprops.md) and [IMAPIProp::CopyTo](imapiprop-copyto.md) methods occur immediately.</span></span> <span data-ttu-id="bd0e1-135">Las llamadas al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) correctamente, pero en realidad no guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="bd0e1-135">Calls to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method succeed but do not actually save any changes.</span></span> 
  
<span data-ttu-id="bd0e1-136">Para estar protegidos contra los cambios que se producen de forma prematura, proveedores de servicios necesitan realizar copias de sus perfiles en las secciones que se muestran a los usuarios a través de las hojas de propiedades.</span><span class="sxs-lookup"><span data-stu-id="bd0e1-136">To be protected from changes that occur prematurely, service providers need to make copies of their profile sections that are displayed to users through property sheets.</span></span> <span data-ttu-id="bd0e1-137">Las hojas de propiedades deben trabajar con la copia, en lugar de la sección de perfil real.</span><span class="sxs-lookup"><span data-stu-id="bd0e1-137">The property sheets should work with the copy, instead of the real profile section.</span></span> <span data-ttu-id="bd0e1-138">Cuando el usuario hace clic en el botón **Aceptar** para comprobar que los cambios son precisos, se pueden guardar los cambios a la sección de perfil real.</span><span class="sxs-lookup"><span data-stu-id="bd0e1-138">When the user clicks the **OK** button to verify that the changes are accurate, the changes can be saved to the real profile section.</span></span> 
  
<span data-ttu-id="bd0e1-139">Para implementar una hoja de propiedades mediante el uso de una sección de perfil copiado, use el procedimiento siguiente:</span><span class="sxs-lookup"><span data-stu-id="bd0e1-139">To implement a property sheet by using a copied profile section, use the following procedure:</span></span>
  
1. <span data-ttu-id="bd0e1-140">Abra la sección de perfil llamando al método [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) o [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) .</span><span class="sxs-lookup"><span data-stu-id="bd0e1-140">Open the profile section by calling the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) or [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) method.</span></span> 
    
2. <span data-ttu-id="bd0e1-141">Llame a la función [CreateIProp](createiprop.md) para recuperar un objeto de datos de propiedades: un objeto que admite la interfaz **IPropData** .</span><span class="sxs-lookup"><span data-stu-id="bd0e1-141">Call the [CreateIProp](createiprop.md) function to retrieve a property data object — an object that supports the **IPropData** interface.</span></span> 
    
3. <span data-ttu-id="bd0e1-142">Llamar al método [IMAPIProp::CopyTo](imapiprop-copyto.md) de la sección de perfil para copiar las propiedades que aparecerán en la hoja de propiedades de la sección de perfil para el objeto de datos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="bd0e1-142">Call the profile section's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties that will appear on the property sheet from the profile section to the property data object.</span></span> 
    
4. <span data-ttu-id="bd0e1-143">Llame al método [IMAPISupport::DoConfigPropSheet](imapisupport-doconfigpropsheet.md) para solicitar que el proveedor de servicios de mostrar una hoja de propiedades y pase un puntero al objeto de datos de propiedad en el parámetro _lpConfigData_ .</span><span class="sxs-lookup"><span data-stu-id="bd0e1-143">Call the [IMAPISupport::DoConfigPropSheet](imapisupport-doconfigpropsheet.md) method to request that the service provider display a property sheet, and pass a pointer to the property data object in the  _lpConfigData_ parameter.</span></span> 
    
5. <span data-ttu-id="bd0e1-144">Cuando el usuario guarda los cambios realizados a las propiedades de configuración en la hoja de propiedades, llame al método [IMAPIProp::CopyTo](imapiprop-copyto.md) para copiar las propiedades del objeto de datos de la propiedad a la sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="bd0e1-144">When the user saves changes to configuration properties in the property sheet, call the [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties from the property data object back to the profile section.</span></span> 
    
<span data-ttu-id="bd0e1-145">En las secciones, a diferencia de otros objetos de perfiles, no admiten las propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="bd0e1-145">Profile sections, unlike other objects, do not support named properties.</span></span> <span data-ttu-id="bd0e1-146">Los métodos [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) y [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) devuelven MAPI_E_NO_SUPPORT si se les llama en un objeto de sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="bd0e1-146">The [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) and [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) methods return MAPI_E_NO_SUPPORT if they are called on a profile section object.</span></span> <span data-ttu-id="bd0e1-147">Si se utiliza el método [IMAPIProp::SetProps](imapiprop-setprops.md) para establecer los identificadores de propiedades en el intervalo por encima de 0 x 8000, se devuelve el tipo de propiedad PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="bd0e1-147">If you use the [IMAPIProp::SetProps](imapiprop-setprops.md) method to set property identifiers in the range above 0x8000, the PT_ERROR property type will be returned.</span></span> 
  
<span data-ttu-id="bd0e1-148">Las secciones del perfil reservan el intervalo de identificadores de 0x67F0 a 0x67FF para propiedades seguras.</span><span class="sxs-lookup"><span data-stu-id="bd0e1-148">Profile sections reserve the identifier range 0x67F0 to 0x67FF for secure properties.</span></span> <span data-ttu-id="bd0e1-149">Proveedores de servicios pueden utilizar este intervalo para almacenar contraseñas y otras credenciales específicas del proveedor.</span><span class="sxs-lookup"><span data-stu-id="bd0e1-149">Service providers can use this range to store passwords and other provider-specific credentials.</span></span> <span data-ttu-id="bd0e1-150">No se devuelven las propiedades de este intervalo en la lista completa de propiedades cuando se pasa NULL en el parámetro _lpPropTag_ del método [IMAPIProp::GetProps](imapiprop-getprops.md) , ni tampoco se devuelven en el parámetro _lppPropTagArray_ de la [ IMAPIProp::GetPropList](imapiprop-getproplist.md) (método).</span><span class="sxs-lookup"><span data-stu-id="bd0e1-150">Properties in this range are not returned in the complete list of properties when NULL is passed in the  _lpPropTag_ parameter of the [IMAPIProp::GetProps](imapiprop-getprops.md) method, nor are they returned in the  _lppPropTagArray_ parameter of the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> <span data-ttu-id="bd0e1-151">Propiedades seguras deben solicitarse específicamente por sus identificadores.</span><span class="sxs-lookup"><span data-stu-id="bd0e1-151">Secure properties must be requested specifically by their identifiers.</span></span> 
  
<span data-ttu-id="bd0e1-152">MAPI proporciona una sección de perfil con la MUID_PROFILE_INSTANCE constante codificado de forma rígida como su identificador y **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) como su propiedad único.</span><span class="sxs-lookup"><span data-stu-id="bd0e1-152">MAPI furnishes a profile section with the hard-coded constant MUID_PROFILE_INSTANCE as its identifier and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) as its single property.</span></span> <span data-ttu-id="bd0e1-153">MAPI se asegura de que el valor de la propiedad **PR_SEARCH_KEY** será único entre todos los perfiles creados.</span><span class="sxs-lookup"><span data-stu-id="bd0e1-153">MAPI ensures that the **PR_SEARCH_KEY** property value will be unique among all created profiles.</span></span> <span data-ttu-id="bd0e1-154">Use **PR_SEARCH_KEY** en lugar de **PR_PROFILE_NAME** cuando unicidad es importante, ya que es posible para un perfil eliminado ser seguido por otro perfil con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="bd0e1-154">Use **PR_SEARCH_KEY** instead of **PR_PROFILE_NAME** when uniqueness is important, because it is possible for a deleted profile to be followed by another profile with the same name.</span></span> 
  
<span data-ttu-id="bd0e1-155">Para obtener más información acerca de cómo usar las secciones del perfil, vea [administración de perfiles y servicios de mensajes](administering-profiles-and-message-services.md).</span><span class="sxs-lookup"><span data-stu-id="bd0e1-155">For more information about how to use profile sections, see [Administering Profiles and Message Services](administering-profiles-and-message-services.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bd0e1-156">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="bd0e1-156">See also</span></span>



[<span data-ttu-id="bd0e1-157">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="bd0e1-157">MAPI Interfaces</span></span>](mapi-interfaces.md)

