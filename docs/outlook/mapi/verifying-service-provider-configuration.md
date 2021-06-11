---
title: Comprobar la configuración del proveedor de servicios
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dc23dc61-7b51-43ab-a184-ce0bdac91d03
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 381e2c9ec84811b69d666017a568e7b9cca21755
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418851"
---
# <a name="verifying-service-provider-configuration"></a><span data-ttu-id="02f22-103">Comprobar la configuración del proveedor de servicios</span><span class="sxs-lookup"><span data-stu-id="02f22-103">Verifying service provider configuration</span></span>
  
<span data-ttu-id="02f22-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02f22-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02f22-105">El método de inicio de sesión ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md)o [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) debe comprobar la configuración del proveedor.</span><span class="sxs-lookup"><span data-stu-id="02f22-105">Your logon method ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md), or [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) must verify your provider's configuration.</span></span> <span data-ttu-id="02f22-106">Esto implica comprobar que todas las propiedades necesarias para el funcionamiento completo se establecen correctamente.</span><span class="sxs-lookup"><span data-stu-id="02f22-106">This involves checking that all of the properties needed for full operation are set correctly.</span></span> <span data-ttu-id="02f22-107">Cada proveedor requiere un número diferente de propiedades; la configuración depende del proveedor y del grado de interacción del usuario que permita.</span><span class="sxs-lookup"><span data-stu-id="02f22-107">Every provider requires a different number of properties; configuration depends on your provider and the degree of user interaction you allow.</span></span> <span data-ttu-id="02f22-108">Algunos proveedores de servicios mantienen todas las propiedades necesarias en el perfil.</span><span class="sxs-lookup"><span data-stu-id="02f22-108">Some service providers keep all of the necessary properties in the profile.</span></span> 

<span data-ttu-id="02f22-109">Otros proveedores de servicios mantienen un conjunto parcial de propiedades en el perfil y solicitan al usuario valores que faltan.</span><span class="sxs-lookup"><span data-stu-id="02f22-109">Other service providers keep a partial set of properties in the profile and prompt the user for missing values.</span></span> <span data-ttu-id="02f22-110">Sin embargo, otros proveedores no almacenan propiedades en el perfil en absoluto, ya que dependen del usuario para proporcionar toda la información necesaria para la configuración.</span><span class="sxs-lookup"><span data-stu-id="02f22-110">Still other providers do not store properties in the profile at all, relying on the user to supply all of the information needed for configuration.</span></span>
  
### <a name="to-retrieve-properties-stored-in-the-profile"></a><span data-ttu-id="02f22-111">Para recuperar las propiedades almacenadas en el perfil</span><span class="sxs-lookup"><span data-stu-id="02f22-111">To retrieve properties stored in the profile</span></span>
  
1. <span data-ttu-id="02f22-112">Llama [a IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)y pasa [el MAPIUID](mapiuid.md) del proveedor como parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="02f22-112">Call [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), passing the [MAPIUID](mapiuid.md) of your provider as an input parameter.</span></span> 
    
2. <span data-ttu-id="02f22-113">Llame a los [métodos IMAPIProp::GetProps](imapiprop-getprops.md) o [IMAPIProp::GetPropList](imapiprop-getproplist.md) de la sección de perfil para recuperar propiedades individuales o una lista de propiedades.</span><span class="sxs-lookup"><span data-stu-id="02f22-113">Call the profile section's [IMAPIProp::GetProps](imapiprop-getprops.md) or [IMAPIProp::GetPropList](imapiprop-getproplist.md) methods to retrieve individual properties or a property list.</span></span> 
    
### <a name="to-set-properties-from-user-information"></a><span data-ttu-id="02f22-114">Para establecer propiedades a partir de la información del usuario</span><span class="sxs-lookup"><span data-stu-id="02f22-114">To set properties from user information</span></span>
  
<span data-ttu-id="02f22-115">Mostrar una hoja de propiedades, si MAPI no ha establecido una marca que prohíba la presentación.</span><span class="sxs-lookup"><span data-stu-id="02f22-115">Display a property sheet, if MAPI has not set a flag prohibiting the display.</span></span> <span data-ttu-id="02f22-116">Las siguientes marcas indican que no se puede presentar una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="02f22-116">The following flags indicate that a user interface cannot be presented.</span></span>
  
|<span data-ttu-id="02f22-117">**Flag**</span><span class="sxs-lookup"><span data-stu-id="02f22-117">**Flag**</span></span>|<span data-ttu-id="02f22-118">**Proveedor de servicios**</span><span class="sxs-lookup"><span data-stu-id="02f22-118">**Service provider**</span></span>|
|:-----|:-----|
|<span data-ttu-id="02f22-119">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="02f22-119">AB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="02f22-120">Proveedor de libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="02f22-120">Address book provider</span></span>  <br/> |
|<span data-ttu-id="02f22-121">LOGON_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="02f22-121">LOGON_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="02f22-122">Proveedor de transporte</span><span class="sxs-lookup"><span data-stu-id="02f22-122">Transport provider</span></span>  <br/> |
|<span data-ttu-id="02f22-123">MDB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="02f22-123">MDB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="02f22-124">Proveedor de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="02f22-124">Message store provider</span></span>  <br/> |
   
<span data-ttu-id="02f22-125">Si el proveedor no almacena todas sus propiedades de configuración en el perfil, lo que requiere la interacción del usuario, y MAPI pasa una de las marcas de supresión del cuadro de diálogo al método de inicio de sesión, MAPI_E_UNCONFIGURED.</span><span class="sxs-lookup"><span data-stu-id="02f22-125">If your provider does not store all of its configuration properties in the profile, requiring user interaction, and MAPI passes one of the dialog box suppression flags to your logon method, return MAPI_E_UNCONFIGURED.</span></span> <span data-ttu-id="02f22-126">También devuelve este error cuando no se establece la marca de supresión de cuadros de diálogo, pero el usuario no proporciona toda la información necesaria.</span><span class="sxs-lookup"><span data-stu-id="02f22-126">Also return this error when the dialog suppression flag is not set, but the user does not supply all of the required information.</span></span>
  
<span data-ttu-id="02f22-127">Cuando el proveedor de servicios produce un error en su método de inicio de sesión MAPI_E_UNCONFIGURED, MAPI llama de nuevo a la función de punto de entrada.</span><span class="sxs-lookup"><span data-stu-id="02f22-127">When your service provider fails its logon method with MAPI_E_UNCONFIGURED, MAPI calls your entry point function again.</span></span> <span data-ttu-id="02f22-128">Si la información no se puede encontrar con la segunda llamada, la sesión podría finalizar, en función de la importancia que tenga el proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="02f22-128">If the information cannot be located with the second call, the session might terminate, depending on how important your service provider is.</span></span> 
  
<span data-ttu-id="02f22-129">En la siguiente ilustración se muestra la lógica necesaria para la configuración en el método de inicio de sesión del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="02f22-129">The following illustration shows the logic required for configuration in your service provider logon method.</span></span> 
  
<span data-ttu-id="02f22-130">**Diagrama de flujo de comprobación de configuración**</span><span class="sxs-lookup"><span data-stu-id="02f22-130">**Configuration verification flowchart**</span></span>
  
<span data-ttu-id="02f22-131">![Diagrama de flujo de verificación de configuración]Diagrama de flujo de verificación de(media/amapi_62.gif "configuración")</span><span class="sxs-lookup"><span data-stu-id="02f22-131">![Configuration verification flowchart](media/amapi_62.gif "Configuration verification flowchart")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="02f22-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="02f22-132">See also</span></span>

- [<span data-ttu-id="02f22-133">Implementación del inicio de sesión del proveedor de servicios</span><span class="sxs-lookup"><span data-stu-id="02f22-133">Implementing Service Provider Logon</span></span>](implementing-service-provider-logon.md)

