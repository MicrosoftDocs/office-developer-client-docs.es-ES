---
title: Inicio de un proveedor de servicios
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4b61cc3-d9fe-4616-a05c-d1e4096b5abd
description: '�ltima modificaci�n: lunes, 7 de diciembre de 2015'
ms.openlocfilehash: f67976681ef0283c86e1c09c49e531572668ff50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439558"
---
# <a name="starting-a-service-provider"></a><span data-ttu-id="bee40-103">Inicio de un proveedor de servicios</span><span class="sxs-lookup"><span data-stu-id="bee40-103">Starting a Service Provider</span></span>

 
  
<span data-ttu-id="bee40-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bee40-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bee40-105">En algún momento después de que un cliente inicie una sesión con MAPI, se iniciará el proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="bee40-105">At some point after a client starts a session with MAPI, your service provider will be started.</span></span> <span data-ttu-id="bee40-106">Los proveedores de transporte se inician cuando un cliente realiza una solicitud para sus servicios.</span><span class="sxs-lookup"><span data-stu-id="bee40-106">Transport providers are started when a client makes a request for their services.</span></span> <span data-ttu-id="bee40-107">Los proveedores de libreta de direcciones y almacén de mensajes se inician durante el proceso de inicio de sesión del cliente.</span><span class="sxs-lookup"><span data-stu-id="bee40-107">Address book and message store providers are started during the client's logon process.</span></span>
  
<span data-ttu-id="bee40-108">Un cliente llama a [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) para cargar cada uno de los proveedores de libretas de direcciones incluidos en el perfil y [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) para cargar un proveedor de almacén de mensajes específico.</span><span class="sxs-lookup"><span data-stu-id="bee40-108">A client calls [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) to load each of the address book providers included in the profile and [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) to load a specific message store provider.</span></span> <span data-ttu-id="bee40-109">Los proveedores de libretas de direcciones que forman parte de un servicio de mensajes se inician antes que cualquier otro proveedor del servicio.</span><span class="sxs-lookup"><span data-stu-id="bee40-109">Address book providers that are part of a message service are started before any of the other providers in the service.</span></span> 
  
<span data-ttu-id="bee40-110">MAPI inicia cada proveedor de servicios en el perfil activo haciendo lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="bee40-110">MAPI starts each service provider in the active profile by doing the following:</span></span>
  
- <span data-ttu-id="bee40-111">Buscar el nombre de su DLL en el perfil.</span><span class="sxs-lookup"><span data-stu-id="bee40-111">Locating the name of its DLL in the profile.</span></span> <span data-ttu-id="bee40-112">Debe registrar el nombre de la DLL del proveedor en el archivo de configuración Mapisvc.inf para asegurarse de que aparece en el perfil.</span><span class="sxs-lookup"><span data-stu-id="bee40-112">You are required to register the name of your provider DLL in the Mapisvc.inf configuration file to ensure that it appears in the profile.</span></span> <span data-ttu-id="bee40-113">Cuando el proveedor de servicios se agrega a un perfil, ya sea individualmente o como parte de un servicio de mensajes, todas las secciones [Proveedor de **servicios]** de Mapisvc.inf que se aplican al proveedor se copian en el perfil.</span><span class="sxs-lookup"><span data-stu-id="bee40-113">When your service provider is added to a profile, either individually or as part of a message service, all of the **[Service Provider]** sections from Mapisvc.inf that apply to your provider are copied into the profile.</span></span> <span data-ttu-id="bee40-114">Para obtener más información acerca de la estructura de Mapisvc.inf, vea formato [de archivo de MapiSvc.inf](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="bee40-114">For more information about the structure of Mapisvc.inf, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
    
- <span data-ttu-id="bee40-115">Llamar a la función **loadLibrary** de la API de Windows para cargar la DLL.</span><span class="sxs-lookup"><span data-stu-id="bee40-115">Calling the Windows API function **LoadLibrary** to load the DLL.</span></span> <span data-ttu-id="bee40-116">Dado que MAPI llama a **LoadLibrary** cada vez que usa una DLL del proveedor de servicios (independientemente de si ya se ha cargado) o solo la primera vez, el proveedor de servicios no debe hacer suposiciones sobre el número de veces que se cargará.</span><span class="sxs-lookup"><span data-stu-id="bee40-116">Because MAPI calls **LoadLibrary** either every time it uses a service provider DLL (regardless of whether it has already been loaded) or only the first time, your service provider must not make assumptions about the number of times that it will be loaded.</span></span> <span data-ttu-id="bee40-117">Por cada llamada a **LoadLibrary**, MAPI realiza una llamada a la función de la API de Windows **FreeLibrary** cuando ya no se necesita una DLL del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="bee40-117">For every call to **LoadLibrary**, MAPI makes a call to the Windows API function **FreeLibrary** when a service provider DLL is no longer needed.</span></span> 
    
- <span data-ttu-id="bee40-118">Llamar a la función de punto de entrada para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="bee40-118">Calling the entry point function for the provider.</span></span> <span data-ttu-id="bee40-119">MAPI llama a la función de punto de entrada del proveedor para iniciar el proceso de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="bee40-119">MAPI calls your provider's entry point function to initiate the logon process.</span></span> <span data-ttu-id="bee40-120">Las funciones de punto de entrada garantizan el uso de una versión de la interfaz del proveedor de servicios (SPI) compatible con la versión que usa MAPI.</span><span class="sxs-lookup"><span data-stu-id="bee40-120">Entry point functions ensure that you are using a version of the service provider interface (SPI) that is compatible with the version being used by MAPI.</span></span> <span data-ttu-id="bee40-121">Estas funciones también devuelven punteros a objetos de proveedor recién creados.</span><span class="sxs-lookup"><span data-stu-id="bee40-121">These functions also return pointers to newly created provider objects.</span></span> <span data-ttu-id="bee40-122">Para obtener más información acerca de cómo crear una función de punto de entrada para su proveedor, vea Implementar una función de punto de entrada [del proveedor de servicios.](implementing-a-service-provider-entry-point-function.md)</span><span class="sxs-lookup"><span data-stu-id="bee40-122">For more information about creating an entry point function for your provider, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bee40-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bee40-123">See also</span></span>



[<span data-ttu-id="bee40-124">Proveedores de servicios MAPI</span><span class="sxs-lookup"><span data-stu-id="bee40-124">MAPI Service Providers</span></span>](mapi-service-providers.md)

