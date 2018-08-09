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
ms.openlocfilehash: eb64f2780530fd30784bf9a9b197bcde205b4a5a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817703"
---
# <a name="implementing-service-provider-logon"></a><span data-ttu-id="0c58e-103">Implementar el inicio de sesión del proveedor de servicios</span><span class="sxs-lookup"><span data-stu-id="0c58e-103">Implementing Service Provider Logon</span></span>

<span data-ttu-id="0c58e-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0c58e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0c58e-105">MAPI llama a un método en el objeto de proveedor para comenzar el proceso de inicio de sesión mediante el puntero que devuelve desde la función de punto de entrada.</span><span class="sxs-lookup"><span data-stu-id="0c58e-105">MAPI calls a method in your provider object to begin the logon process by using the pointer that you return from your entry point function.</span></span> <span data-ttu-id="0c58e-106">El método manera, varía según el tipo de proveedor de servicios:</span><span class="sxs-lookup"><span data-stu-id="0c58e-106">The method varies as follows, depending on the type of your service provider:</span></span>
  
- <span data-ttu-id="0c58e-107">[IABProvider::Logon](iabprovider-logon.md) para los proveedores de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="0c58e-107">[IABProvider::Logon](iabprovider-logon.md) for address book providers</span></span> 
    
- <span data-ttu-id="0c58e-108">[IMSProvider::Logon](imsprovider-logon.md) para los proveedores de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="0c58e-108">[IMSProvider::Logon](imsprovider-logon.md) for message store providers</span></span> 
    
- <span data-ttu-id="0c58e-109">[IXPProvider::TransportLogon](ixpprovider-transportlogon.md) para los proveedores de transporte</span><span class="sxs-lookup"><span data-stu-id="0c58e-109">[IXPProvider::TransportLogon](ixpprovider-transportlogon.md) for transport providers</span></span> 
    
<span data-ttu-id="0c58e-110">Realizar las siguientes tareas en el método de inicio de sesión que implementa:</span><span class="sxs-lookup"><span data-stu-id="0c58e-110">Perform the following tasks in whatever logon method you implement:</span></span>
  
1. <span data-ttu-id="0c58e-111">Incrementar el recuento de referencia en el objeto de soporte técnico que se pasa como un parámetro de entrada mediante una llamada a su método [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0c58e-111">Increment the reference count on the support object that is passed as an input parameter by calling its [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) method.</span></span> 
    
2. <span data-ttu-id="0c58e-112">Llamar al método [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) del objeto de soporte para obtener acceso a la sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="0c58e-112">Call the support object's [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to access your profile section.</span></span> 
    
3. <span data-ttu-id="0c58e-113">Llamar al método [IMAPIProp::SetProps](imapiprop-setprops.md) de la sección de perfil para establecer las propiedades siguientes:</span><span class="sxs-lookup"><span data-stu-id="0c58e-113">Call the profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set the following properties:</span></span> 
    
  - <span data-ttu-id="0c58e-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0c58e-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
  - <span data-ttu-id="0c58e-115">**Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0c58e-115">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
  - <span data-ttu-id="0c58e-116">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0c58e-116">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>
    
  - <span data-ttu-id="0c58e-117">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0c58e-117">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="0c58e-118">No intente establecer las propiedades de la sección de perfil **PR_RESOURCE_FLAGS** o **PR_PROVIDER_DLL_NAME** .</span><span class="sxs-lookup"><span data-stu-id="0c58e-118">Do not attempt to set the profile section's **PR_RESOURCE_FLAGS** or **PR_PROVIDER_DLL_NAME** properties.</span></span> <span data-ttu-id="0c58e-119">En tiempo de inicio de sesión, estas propiedades son de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="0c58e-119">At logon time, these properties are read-only.</span></span> 
  
4. <span data-ttu-id="0c58e-120">Compruebe que las propiedades que necesita para la configuración se almacenan en el perfil o están disponibles desde el usuario.</span><span class="sxs-lookup"><span data-stu-id="0c58e-120">Check that the properties you need for configuration are either stored in the profile or are available from the user.</span></span> <span data-ttu-id="0c58e-121">Para obtener más información acerca de cómo comprobar la configuración, vea [Comprobar la configuración del proveedor de servicio](verifying-service-provider-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="0c58e-121">For more information about checking your configuration, see [Verifying Service Provider Configuration](verifying-service-provider-configuration.md).</span></span>
    
5. <span data-ttu-id="0c58e-122">Llame al método [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) del objeto de soporte técnico para registrar un identificador único o [MAPIUID](mapiuid.md), si su proveedor es un proveedor de almacén de mensaje o de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="0c58e-122">Call the support object's [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register a unique identifier, or [MAPIUID](mapiuid.md), if your provider is an address book or message store provider.</span></span> <span data-ttu-id="0c58e-123">Los proveedores de transporte registrar **MAPIUID** estructuras cuando MAPI llama a su método [IXPLogon::AddressTypes](ixplogon-addresstypes.md) .</span><span class="sxs-lookup"><span data-stu-id="0c58e-123">Transport providers register **MAPIUID** structures when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="0c58e-124">Para obtener más información acerca de cómo registrar un **MAPIUID**, vea [Identificadores únicos proveedor de servicio de registro](registering-service-provider-unique-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="0c58e-124">For more information about registering a **MAPIUID**, see [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).</span></span>
    
6. <span data-ttu-id="0c58e-125">Crear una instancia de un objeto de inicio de sesión y devolver con uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="0c58e-125">Instantiate a logon object and return with one of the following values:</span></span>
    
  - <span data-ttu-id="0c58e-126">S_OK para indicar un inicio de sesión correcto.</span><span class="sxs-lookup"><span data-stu-id="0c58e-126">S_OK to indicate a successful logon.</span></span>
    
  - <span data-ttu-id="0c58e-127">MAPI_E_UNCONFIGURED para indicar que uno o más de las propiedades de configuración no estaban disponibles.</span><span class="sxs-lookup"><span data-stu-id="0c58e-127">MAPI_E_UNCONFIGURED to indicate that one or more of the configuration properties were unavailable.</span></span>
    
  - <span data-ttu-id="0c58e-128">MAPI_E_USER_CANCEL para indicar que el usuario canceló el cuadro de diálogo Configuración, lo que provoca que las propiedades de configuración que no esté disponible.</span><span class="sxs-lookup"><span data-stu-id="0c58e-128">MAPI_E_USER_CANCEL to indicate that the user canceled the configuration dialog box, causing configuration properties to be unavailable.</span></span>
    
  - <span data-ttu-id="0c58e-129">MAPI_E_FAILONEPROVIDER para indicar que no se pudo configurar su proveedor, pero que debe permitir la MAPI para usarse independientemente de la forma.</span><span class="sxs-lookup"><span data-stu-id="0c58e-129">MAPI_E_FAILONEPROVIDER to indicate that your provider could not be configured, but that MAPI should allow it to be used regardless.</span></span> <span data-ttu-id="0c58e-130">Métodos de inicio de sesión deben devolver este valor para notificar un error no grave, como cuando el proveedor requiere una contraseña y no puede solicitar al usuario para él debido a que la interfaz de usuario está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="0c58e-130">Logon methods should return this value to report a nonfatal error, such as when the provider requires a password and cannot prompt the user for it because the user interface is disabled.</span></span> 
    
<span data-ttu-id="0c58e-131">La lista anterior de tareas describe una implementación mínima para un método de inicio de sesión del proveedor de servicio.</span><span class="sxs-lookup"><span data-stu-id="0c58e-131">The preceding list of tasks describes a minimum implementation for a service provider logon method.</span></span> <span data-ttu-id="0c58e-132">Puede incluir funciones adicionales, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="0c58e-132">You can include additional functionality, if necessary.</span></span> <span data-ttu-id="0c58e-133">Por ejemplo, algunos proveedores de llamar a [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) para actualizar la tabla de estado en el método de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="0c58e-133">For example, some providers call [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) to update the status table in their logon method.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0c58e-134">Para conseguir el mejor rendimiento en tiempo de inicio de sesión, evite llamar a [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) o [SpoolerNotify](imapisupport-spoolernotify.md).</span><span class="sxs-lookup"><span data-stu-id="0c58e-134">To achieve the best performance at logon time, avoid calling either [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) or [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md).</span></span> <span data-ttu-id="0c58e-135">Antes de estas llamadas pueden completar y devolver el control al método de inicio de sesión, se debe iniciar la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="0c58e-135">Before these calls can complete and return control to your logon method, the MAPI spooler must be started.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0c58e-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c58e-136">See also</span></span>

- [<span data-ttu-id="0c58e-137">Iniciar un proveedor de servicios</span><span class="sxs-lookup"><span data-stu-id="0c58e-137">Starting a Service Provider</span></span>](starting-a-service-provider.md)

