---
title: Comprobar la configuración del proveedor de servicio
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dc23dc61-7b51-43ab-a184-ce0bdac91d03
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f6190b2860e227b24b34e31a4ee9741468383460
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589640"
---
# <a name="verifying-service-provider-configuration"></a><span data-ttu-id="30ac3-103">Comprobar la configuración del proveedor de servicio</span><span class="sxs-lookup"><span data-stu-id="30ac3-103">Verifying service provider configuration</span></span>
  
<span data-ttu-id="30ac3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30ac3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30ac3-105">El método de inicio de sesión ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md)o [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) debe comprobar la configuración de su proveedor.</span><span class="sxs-lookup"><span data-stu-id="30ac3-105">Your logon method ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md), or [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) must verify your provider's configuration.</span></span> <span data-ttu-id="30ac3-106">Esto implica comprobar que todas las propiedades necesarias para la operación completa se establecen correctamente.</span><span class="sxs-lookup"><span data-stu-id="30ac3-106">This involves checking that all of the properties needed for full operation are set correctly.</span></span> <span data-ttu-id="30ac3-107">Cada proveedor requiere un número diferente de propiedades; configuración depende de su proveedor y el grado de interacción del usuario que va a permitir.</span><span class="sxs-lookup"><span data-stu-id="30ac3-107">Every provider requires a different number of properties; configuration depends on your provider and the degree of user interaction you allow.</span></span> <span data-ttu-id="30ac3-108">Algunos proveedores de servicios tenga todas las propiedades necesarias en el perfil.</span><span class="sxs-lookup"><span data-stu-id="30ac3-108">Some service providers keep all of the necessary properties in the profile.</span></span> 

<span data-ttu-id="30ac3-109">Otros proveedores de servicios de mantener un conjunto parcial de propiedades en el perfil y pedir al usuario los valores que faltan.</span><span class="sxs-lookup"><span data-stu-id="30ac3-109">Other service providers keep a partial set of properties in the profile and prompt the user for missing values.</span></span> <span data-ttu-id="30ac3-110">Aún otros proveedores no almacene las propiedades en el perfil en absoluto, confiar en el usuario para proporcionar toda la información necesaria para la configuración de.</span><span class="sxs-lookup"><span data-stu-id="30ac3-110">Still other providers do not store properties in the profile at all, relying on the user to supply all of the information needed for configuration.</span></span>
  
### <a name="to-retrieve-properties-stored-in-the-profile"></a><span data-ttu-id="30ac3-111">Para recuperar las propiedades almacenadas en el perfil</span><span class="sxs-lookup"><span data-stu-id="30ac3-111">To retrieve properties stored in the profile</span></span>
  
1. <span data-ttu-id="30ac3-112">Llame a [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), pasando el [MAPIUID](mapiuid.md) de su proveedor como un parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="30ac3-112">Call [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), passing the [MAPIUID](mapiuid.md) of your provider as an input parameter.</span></span> 
    
2. <span data-ttu-id="30ac3-113">Llame a métodos [IMAPIProp::GetProps](imapiprop-getprops.md) o [IMAPIProp::GetPropList](imapiprop-getproplist.md) de la sección de perfil para recuperar las propiedades individuales o una lista de propiedades.</span><span class="sxs-lookup"><span data-stu-id="30ac3-113">Call the profile section's [IMAPIProp::GetProps](imapiprop-getprops.md) or [IMAPIProp::GetPropList](imapiprop-getproplist.md) methods to retrieve individual properties or a property list.</span></span> 
    
### <a name="to-set-properties-from-user-information"></a><span data-ttu-id="30ac3-114">Para establecer las propiedades de información del usuario</span><span class="sxs-lookup"><span data-stu-id="30ac3-114">To set properties from user information</span></span>
  
<span data-ttu-id="30ac3-115">Mostrar una hoja de propiedades, si MAPI no ha establecido una marca de prohibición de la presentación.</span><span class="sxs-lookup"><span data-stu-id="30ac3-115">Display a property sheet, if MAPI has not set a flag prohibiting the display.</span></span> <span data-ttu-id="30ac3-116">Los siguientes marcadores de indican que no se puede presentar una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="30ac3-116">The following flags indicate that a user interface cannot be presented.</span></span>
  
|<span data-ttu-id="30ac3-117">**Flag**</span><span class="sxs-lookup"><span data-stu-id="30ac3-117">**Flag**</span></span>|<span data-ttu-id="30ac3-118">**Proveedor de servicios**</span><span class="sxs-lookup"><span data-stu-id="30ac3-118">**Service provider**</span></span>|
|:-----|:-----|
|<span data-ttu-id="30ac3-119">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="30ac3-119">AB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="30ac3-120">Proveedor de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="30ac3-120">Address book provider</span></span>  <br/> |
|<span data-ttu-id="30ac3-121">LOGON_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="30ac3-121">LOGON_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="30ac3-122">Proveedor de transporte</span><span class="sxs-lookup"><span data-stu-id="30ac3-122">Transport provider</span></span>  <br/> |
|<span data-ttu-id="30ac3-123">MDB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="30ac3-123">MDB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="30ac3-124">Proveedor de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="30ac3-124">Message store provider</span></span>  <br/> |
   
<span data-ttu-id="30ac3-125">Si su proveedor no almacenar todas sus propiedades de configuración en el perfil, requerir la interacción del usuario, y MAPI uno de los indicadores de supresión del cuadro de diálogo pasa al método de inicio de sesión, devolver MAPI_E_UNCONFIGURED.</span><span class="sxs-lookup"><span data-stu-id="30ac3-125">If your provider does not store all of its configuration properties in the profile, requiring user interaction, and MAPI passes one of the dialog box suppression flags to your logon method, return MAPI_E_UNCONFIGURED.</span></span> <span data-ttu-id="30ac3-126">También puede devolver este error cuando no está establecido el indicador de supresión del cuadro de diálogo, pero el usuario no proporciona toda la información necesaria.</span><span class="sxs-lookup"><span data-stu-id="30ac3-126">Also return this error when the dialog suppression flag is not set, but the user does not supply all of the required information.</span></span>
  
<span data-ttu-id="30ac3-127">Cuando su proveedor de servicios se produce un error de su método de inicio de sesión con MAPI_E_UNCONFIGURED, MAPI llama la función de punto de entrada de nuevo.</span><span class="sxs-lookup"><span data-stu-id="30ac3-127">When your service provider fails its logon method with MAPI_E_UNCONFIGURED, MAPI calls your entry point function again.</span></span> <span data-ttu-id="30ac3-128">Si la información no se puede encontrar con la segunda llamada, es posible que terminar la sesión, dependiendo de cómo importante es de su proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="30ac3-128">If the information cannot be located with the second call, the session might terminate, depending on how important your service provider is.</span></span> 
  
<span data-ttu-id="30ac3-129">En la siguiente ilustración se muestra la lógica de requerido para la configuración en el método de inicio de sesión del proveedor de servicio.</span><span class="sxs-lookup"><span data-stu-id="30ac3-129">The following illustration shows the logic required for configuration in your service provider logon method.</span></span> 
  
<span data-ttu-id="30ac3-130">**Diagrama de flujo de comprobación de configuración**</span><span class="sxs-lookup"><span data-stu-id="30ac3-130">**Configuration verification flowchart**</span></span>
  
<span data-ttu-id="30ac3-131">![Diagrama de flujo de comprobación de configuración] (media/amapi_62.gif "Diagrama de flujo de comprobación de configuración")</span><span class="sxs-lookup"><span data-stu-id="30ac3-131">![Configuration verification flowchart](media/amapi_62.gif "Configuration verification flowchart")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="30ac3-132">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="30ac3-132">See also</span></span>

- [<span data-ttu-id="30ac3-133">Implementar el inicio de sesión del proveedor de servicios</span><span class="sxs-lookup"><span data-stu-id="30ac3-133">Implementing Service Provider Logon</span></span>](implementing-service-provider-logon.md)

