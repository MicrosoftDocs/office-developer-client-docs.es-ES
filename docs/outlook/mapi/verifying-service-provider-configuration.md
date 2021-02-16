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
# <a name="verifying-service-provider-configuration"></a><span data-ttu-id="34e74-103">Comprobar la configuración del proveedor de servicios</span><span class="sxs-lookup"><span data-stu-id="34e74-103">Verifying service provider configuration</span></span>
  
<span data-ttu-id="34e74-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34e74-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34e74-105">El método de inicio de sesión ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md)o [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) debe comprobar la configuración del proveedor.</span><span class="sxs-lookup"><span data-stu-id="34e74-105">Your logon method ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md), or [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) must verify your provider's configuration.</span></span> <span data-ttu-id="34e74-106">Esto implica comprobar que todas las propiedades necesarias para el funcionamiento completo estén establecidas correctamente.</span><span class="sxs-lookup"><span data-stu-id="34e74-106">This involves checking that all of the properties needed for full operation are set correctly.</span></span> <span data-ttu-id="34e74-107">Cada proveedor requiere un número diferente de propiedades; depende del proveedor y del grado de interacción del usuario que permitas.</span><span class="sxs-lookup"><span data-stu-id="34e74-107">Every provider requires a different number of properties; configuration depends on your provider and the degree of user interaction you allow.</span></span> <span data-ttu-id="34e74-108">Algunos proveedores de servicios mantienen todas las propiedades necesarias en el perfil.</span><span class="sxs-lookup"><span data-stu-id="34e74-108">Some service providers keep all of the necessary properties in the profile.</span></span> 

<span data-ttu-id="34e74-109">Otros proveedores de servicios mantienen un conjunto parcial de propiedades en el perfil y solicitan al usuario los valores que faltan.</span><span class="sxs-lookup"><span data-stu-id="34e74-109">Other service providers keep a partial set of properties in the profile and prompt the user for missing values.</span></span> <span data-ttu-id="34e74-110">Aún así, otros proveedores no almacenan propiedades en el perfil, y dependen del usuario para proporcionar toda la información necesaria para la configuración.</span><span class="sxs-lookup"><span data-stu-id="34e74-110">Still other providers do not store properties in the profile at all, relying on the user to supply all of the information needed for configuration.</span></span>
  
### <a name="to-retrieve-properties-stored-in-the-profile"></a><span data-ttu-id="34e74-111">Para recuperar propiedades almacenadas en el perfil</span><span class="sxs-lookup"><span data-stu-id="34e74-111">To retrieve properties stored in the profile</span></span>
  
1. <span data-ttu-id="34e74-112">Llame [a IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)y pase [el MAPIUID](mapiuid.md) del proveedor como parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="34e74-112">Call [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), passing the [MAPIUID](mapiuid.md) of your provider as an input parameter.</span></span> 
    
2. <span data-ttu-id="34e74-113">Llame a los métodos [IMAPIProp::GetProps](imapiprop-getprops.md) o [IMAPIProp::GetPropList](imapiprop-getproplist.md) de la sección de perfil para recuperar propiedades individuales o una lista de propiedades.</span><span class="sxs-lookup"><span data-stu-id="34e74-113">Call the profile section's [IMAPIProp::GetProps](imapiprop-getprops.md) or [IMAPIProp::GetPropList](imapiprop-getproplist.md) methods to retrieve individual properties or a property list.</span></span> 
    
### <a name="to-set-properties-from-user-information"></a><span data-ttu-id="34e74-114">Para establecer propiedades a partir de la información del usuario</span><span class="sxs-lookup"><span data-stu-id="34e74-114">To set properties from user information</span></span>
  
<span data-ttu-id="34e74-115">Mostrar una hoja de propiedades, si MAPI no ha establecido una marca que prohíba la presentación.</span><span class="sxs-lookup"><span data-stu-id="34e74-115">Display a property sheet, if MAPI has not set a flag prohibiting the display.</span></span> <span data-ttu-id="34e74-116">Las siguientes marcas indican que no se puede presentar una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="34e74-116">The following flags indicate that a user interface cannot be presented.</span></span>
  
|<span data-ttu-id="34e74-117">**Flag**</span><span class="sxs-lookup"><span data-stu-id="34e74-117">**Flag**</span></span>|<span data-ttu-id="34e74-118">**Proveedor de servicios**</span><span class="sxs-lookup"><span data-stu-id="34e74-118">**Service provider**</span></span>|
|:-----|:-----|
|<span data-ttu-id="34e74-119">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="34e74-119">AB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="34e74-120">Proveedor de libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="34e74-120">Address book provider</span></span>  <br/> |
|<span data-ttu-id="34e74-121">LOGON_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="34e74-121">LOGON_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="34e74-122">Proveedor de transporte</span><span class="sxs-lookup"><span data-stu-id="34e74-122">Transport provider</span></span>  <br/> |
|<span data-ttu-id="34e74-123">MDB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="34e74-123">MDB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="34e74-124">Proveedor de almacenamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="34e74-124">Message store provider</span></span>  <br/> |
   
<span data-ttu-id="34e74-125">Si el proveedor no almacena todas sus propiedades de configuración en el perfil, lo que requiere la interacción del usuario y MAPI pasa una de las marcas de supresión del cuadro de diálogo al método de inicio de sesión, MAPI_E_UNCONFIGURED.</span><span class="sxs-lookup"><span data-stu-id="34e74-125">If your provider does not store all of its configuration properties in the profile, requiring user interaction, and MAPI passes one of the dialog box suppression flags to your logon method, return MAPI_E_UNCONFIGURED.</span></span> <span data-ttu-id="34e74-126">Devuelve también este error cuando no se establece la marca de supresión de cuadros de diálogo, pero el usuario no proporciona toda la información necesaria.</span><span class="sxs-lookup"><span data-stu-id="34e74-126">Also return this error when the dialog suppression flag is not set, but the user does not supply all of the required information.</span></span>
  
<span data-ttu-id="34e74-127">Cuando el proveedor de servicios no puede iniciar sesión con MAPI_E_UNCONFIGURED, MAPI vuelve a llamar a la función de punto de entrada.</span><span class="sxs-lookup"><span data-stu-id="34e74-127">When your service provider fails its logon method with MAPI_E_UNCONFIGURED, MAPI calls your entry point function again.</span></span> <span data-ttu-id="34e74-128">Si la información no se puede localizar con la segunda llamada, la sesión podría finalizar, en función de la importancia que tenga el proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="34e74-128">If the information cannot be located with the second call, the session might terminate, depending on how important your service provider is.</span></span> 
  
<span data-ttu-id="34e74-129">En la siguiente ilustración se muestra la lógica necesaria para la configuración en el método de inicio de sesión del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="34e74-129">The following illustration shows the logic required for configuration in your service provider logon method.</span></span> 
  
<span data-ttu-id="34e74-130">**Diagrama de flujo de comprobación de configuración**</span><span class="sxs-lookup"><span data-stu-id="34e74-130">**Configuration verification flowchart**</span></span>
  
<span data-ttu-id="34e74-131">![Diagrama de flujo de comprobación de configuración:](media/amapi_62.gif "diagrama de flujo de comprobación de configuración")</span><span class="sxs-lookup"><span data-stu-id="34e74-131">![Configuration verification flowchart](media/amapi_62.gif "Configuration verification flowchart")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="34e74-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="34e74-132">See also</span></span>

- [<span data-ttu-id="34e74-133">Implementación del inicio de sesión del proveedor de servicios</span><span class="sxs-lookup"><span data-stu-id="34e74-133">Implementing Service Provider Logon</span></span>](implementing-service-provider-logon.md)

