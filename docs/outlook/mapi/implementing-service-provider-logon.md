---
title: Implementar el inicio de sesión del proveedor de servicios
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d3c309f-fe60-43a9-beda-16b09ec769db
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 533c00a0c994e7dfc5adc476899553bc39a2a9ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310090"
---
# <a name="implementing-service-provider-logon"></a><span data-ttu-id="e1fdb-103">Implementar el inicio de sesión del proveedor de servicios</span><span class="sxs-lookup"><span data-stu-id="e1fdb-103">Implementing Service Provider Logon</span></span>

<span data-ttu-id="e1fdb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1fdb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1fdb-105">MAPI llama a un método en el objeto de proveedor para comenzar el proceso de inicio de sesión mediante el puntero que se devuelve de la función de punto de entrada.</span><span class="sxs-lookup"><span data-stu-id="e1fdb-105">MAPI calls a method in your provider object to begin the logon process by using the pointer that you return from your entry point function.</span></span> <span data-ttu-id="e1fdb-106">El método varía como se indica a continuación, según el tipo de proveedor de servicios:</span><span class="sxs-lookup"><span data-stu-id="e1fdb-106">The method varies as follows, depending on the type of your service provider:</span></span>
  
- <span data-ttu-id="e1fdb-107">[IABProvider:: Inicio de sesión](iabprovider-logon.md) para los proveedores de libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="e1fdb-107">[IABProvider::Logon](iabprovider-logon.md) for address book providers</span></span> 
    
- <span data-ttu-id="e1fdb-108">[IMSProvider:: Inicio de sesión](imsprovider-logon.md) para proveedores de almacenamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="e1fdb-108">[IMSProvider::Logon](imsprovider-logon.md) for message store providers</span></span> 
    
- <span data-ttu-id="e1fdb-109">[IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) para proveedores de transporte</span><span class="sxs-lookup"><span data-stu-id="e1fdb-109">[IXPProvider::TransportLogon](ixpprovider-transportlogon.md) for transport providers</span></span> 
    
<span data-ttu-id="e1fdb-110">Realice las siguientes tareas en cualquier método de inicio de sesión que implemente:</span><span class="sxs-lookup"><span data-stu-id="e1fdb-110">Perform the following tasks in whatever logon method you implement:</span></span>
  
1. <span data-ttu-id="e1fdb-111">Para incrementar el recuento de referencia en el objeto de soporte que se pasa como parámetro de entrada, llame a su método [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e1fdb-111">Increment the reference count on the support object that is passed as an input parameter by calling its [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method.</span></span> 
    
2. <span data-ttu-id="e1fdb-112">Llame al método [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) del objeto support para obtener acceso a su sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="e1fdb-112">Call the support object's [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to access your profile section.</span></span> 
    
3. <span data-ttu-id="e1fdb-113">Llame al método [IMAPIProp:: SetProps](imapiprop-setprops.md) de la sección de perfil para establecer las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="e1fdb-113">Call the profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set the following properties:</span></span> 
    
  - <span data-ttu-id="e1fdb-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e1fdb-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
  - <span data-ttu-id="e1fdb-115">\*\*\*\* Es ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e1fdb-115">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
  - <span data-ttu-id="e1fdb-116">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e1fdb-116">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>
    
  - <span data-ttu-id="e1fdb-117">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e1fdb-117">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="e1fdb-118">No intente establecer las propiedades **PR_RESOURCE_FLAGS** o **PR_PROVIDER_DLL_NAME** de la sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="e1fdb-118">Do not attempt to set the profile section's **PR_RESOURCE_FLAGS** or **PR_PROVIDER_DLL_NAME** properties.</span></span> <span data-ttu-id="e1fdb-119">En el momento del inicio de sesión, estas propiedades son de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e1fdb-119">At logon time, these properties are read-only.</span></span> 
  
4. <span data-ttu-id="e1fdb-120">Compruebe que las propiedades que necesita para la configuración se almacenan en el perfil o están disponibles para el usuario.</span><span class="sxs-lookup"><span data-stu-id="e1fdb-120">Check that the properties you need for configuration are either stored in the profile or are available from the user.</span></span> <span data-ttu-id="e1fdb-121">Para obtener más información acerca de la comprobación de la configuración, vea [verifyIng Service Provider Configuration](verifying-service-provider-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="e1fdb-121">For more information about checking your configuration, see [Verifying Service Provider Configuration](verifying-service-provider-configuration.md).</span></span>
    
5. <span data-ttu-id="e1fdb-122">Llame al método [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) del objeto support para registrar un identificador único, o [MAPIUID](mapiuid.md), si el proveedor es una libreta de direcciones o un proveedor de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="e1fdb-122">Call the support object's [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register a unique identifier, or [MAPIUID](mapiuid.md), if your provider is an address book or message store provider.</span></span> <span data-ttu-id="e1fdb-123">Los proveedores de transporte registran estructuras **MAPIUID** cuando MAPI llama a su método [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) .</span><span class="sxs-lookup"><span data-stu-id="e1fdb-123">Transport providers register **MAPIUID** structures when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="e1fdb-124">Para obtener más información acerca de cómo registrar una **MAPIUID**, consulte [registraNdo identificadores únicos del proveedor de servicios](registering-service-provider-unique-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="e1fdb-124">For more information about registering a **MAPIUID**, see [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).</span></span>
    
6. <span data-ttu-id="e1fdb-125">Cree una instancia de un objeto de inicio de sesión y vuelva con uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="e1fdb-125">Instantiate a logon object and return with one of the following values:</span></span>
    
  - <span data-ttu-id="e1fdb-126">S_OK para indicar que el inicio de sesión se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="e1fdb-126">S_OK to indicate a successful logon.</span></span>
    
  - <span data-ttu-id="e1fdb-127">MAPI_E_UNCONFIGURED para indicar que una o varias de las propiedades de configuración no estaban disponibles.</span><span class="sxs-lookup"><span data-stu-id="e1fdb-127">MAPI_E_UNCONFIGURED to indicate that one or more of the configuration properties were unavailable.</span></span>
    
  - <span data-ttu-id="e1fdb-128">MAPI_E_USER_CANCEL para indicar que el usuario canceló el cuadro de diálogo de configuración, lo que hace que las propiedades de configuración no estén disponibles.</span><span class="sxs-lookup"><span data-stu-id="e1fdb-128">MAPI_E_USER_CANCEL to indicate that the user canceled the configuration dialog box, causing configuration properties to be unavailable.</span></span>
    
  - <span data-ttu-id="e1fdb-129">MAPI_E_FAILONEPROVIDER para indicar que no se ha podido configurar el proveedor, pero MAPI debe permitir su uso independientemente.</span><span class="sxs-lookup"><span data-stu-id="e1fdb-129">MAPI_E_FAILONEPROVIDER to indicate that your provider could not be configured, but that MAPI should allow it to be used regardless.</span></span> <span data-ttu-id="e1fdb-130">Los métodos de inicio de sesión deben devolver este valor para informar de un error no grave, como cuando el proveedor requiere una contraseña y no puede solicitarlo al usuario porque la interfaz de usuario está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="e1fdb-130">Logon methods should return this value to report a nonfatal error, such as when the provider requires a password and cannot prompt the user for it because the user interface is disabled.</span></span> 
    
<span data-ttu-id="e1fdb-131">La lista anterior de tareas describe una implementación mínima de un método de inicio de sesión de un proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="e1fdb-131">The preceding list of tasks describes a minimum implementation for a service provider logon method.</span></span> <span data-ttu-id="e1fdb-132">Puede incluir una funcionalidad adicional, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="e1fdb-132">You can include additional functionality, if necessary.</span></span> <span data-ttu-id="e1fdb-133">Por ejemplo, algunos proveedores llaman a [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) para actualizar la tabla de estado en su método de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="e1fdb-133">For example, some providers call [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) to update the status table in their logon method.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e1fdb-134">Para obtener el mejor rendimiento en el momento del inicio de sesión, evite llamar a [IMAPISupport::P reparesubmit](imapisupport-preparesubmit.md) o [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md).</span><span class="sxs-lookup"><span data-stu-id="e1fdb-134">To achieve the best performance at logon time, avoid calling either [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) or [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md).</span></span> <span data-ttu-id="e1fdb-135">Para que estas llamadas puedan completarse y devuelvan el control al método de inicio de sesión, es necesario iniciar la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="e1fdb-135">Before these calls can complete and return control to your logon method, the MAPI spooler must be started.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e1fdb-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1fdb-136">See also</span></span>

- [<span data-ttu-id="e1fdb-137">Inicio de un proveedor de servicios</span><span class="sxs-lookup"><span data-stu-id="e1fdb-137">Starting a Service Provider</span></span>](starting-a-service-provider.md)

