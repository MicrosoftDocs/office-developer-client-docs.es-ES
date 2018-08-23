---
title: Iniciar un proveedor de servicios
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4b61cc3-d9fe-4616-a05c-d1e4096b5abd
description: '�ltima modificaci�n: lunes, 7 de diciembre de 2015'
ms.openlocfilehash: d14a9961002d63733423af474e147ec5001051fb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586336"
---
# <a name="starting-a-service-provider"></a><span data-ttu-id="0e5c7-103">Iniciar un proveedor de servicios</span><span class="sxs-lookup"><span data-stu-id="0e5c7-103">Starting a Service Provider</span></span>

 
  
<span data-ttu-id="0e5c7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e5c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e5c7-105">En algún momento después de que un cliente inicia una sesión con MAPI, su proveedor de servicios se iniciarán.</span><span class="sxs-lookup"><span data-stu-id="0e5c7-105">At some point after a client starts a session with MAPI, your service provider will be started.</span></span> <span data-ttu-id="0e5c7-106">Los proveedores de transporte se inician cuando un cliente realiza una solicitud para sus servicios.</span><span class="sxs-lookup"><span data-stu-id="0e5c7-106">Transport providers are started when a client makes a request for their services.</span></span> <span data-ttu-id="0e5c7-107">Proveedores de almacén de libreta de direcciones y el mensaje de dirección se inician durante el proceso de inicio de sesión del cliente.</span><span class="sxs-lookup"><span data-stu-id="0e5c7-107">Address book and message store providers are started during the client's logon process.</span></span>
  
<span data-ttu-id="0e5c7-108">Un cliente llama a [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) para cada uno de los proveedores de libreta de direcciones incluidos en el perfil y [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) cargar un proveedor de almacén de mensaje específico de carga.</span><span class="sxs-lookup"><span data-stu-id="0e5c7-108">A client calls [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) to load each of the address book providers included in the profile and [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) to load a specific message store provider.</span></span> <span data-ttu-id="0e5c7-109">Los proveedores de la libreta de direcciones que forman parte de un servicio de mensajes se hayan iniciado antes de cualquiera de los otros proveedores en el servicio.</span><span class="sxs-lookup"><span data-stu-id="0e5c7-109">Address book providers that are part of a message service are started before any of the other providers in the service.</span></span> 
  
<span data-ttu-id="0e5c7-110">MAPI inicia cada proveedor de servicios en el perfil activo haciendo lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="0e5c7-110">MAPI starts each service provider in the active profile by doing the following:</span></span>
  
- <span data-ttu-id="0e5c7-111">Localizar el nombre de su archivo DLL en el perfil.</span><span class="sxs-lookup"><span data-stu-id="0e5c7-111">Locating the name of its DLL in the profile.</span></span> <span data-ttu-id="0e5c7-112">Son necesarios para registrar el nombre del proveedor de DLL en el archivo Mapisvc.inf de configuración para asegurarse de que aparece en el perfil.</span><span class="sxs-lookup"><span data-stu-id="0e5c7-112">You are required to register the name of your provider DLL in the Mapisvc.inf configuration file to ensure that it appears in the profile.</span></span> <span data-ttu-id="0e5c7-113">Cuando su proveedor de servicios se agrega a un perfil, ya sea individualmente o como parte de un servicio de mensajes, todas las secciones **[Servicio proveedor]** desde Mapisvc.inf que se aplican a su proveedor se copian en el perfil.</span><span class="sxs-lookup"><span data-stu-id="0e5c7-113">When your service provider is added to a profile, either individually or as part of a message service, all of the **[Service Provider]** sections from Mapisvc.inf that apply to your provider are copied into the profile.</span></span> <span data-ttu-id="0e5c7-114">Para obtener más información acerca de la estructura de Mapisvc.inf, vea [Formato de archivo de MapiSvc.inf](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="0e5c7-114">For more information about the structure of Mapisvc.inf, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
    
- <span data-ttu-id="0e5c7-115">Llamar a la función **LoadLibrary** para cargar el archivo DLL de API de Windows.</span><span class="sxs-lookup"><span data-stu-id="0e5c7-115">Calling the Windows API function **LoadLibrary** to load the DLL.</span></span> <span data-ttu-id="0e5c7-116">Debido a que las llamadas de MAPI **LoadLibrary** uno cada vez que usa un proveedor de servicios DLL (independientemente de si ya se ha cargado) o sólo la primera vez, su proveedor de servicios no debe hacer suposiciones sobre el número de veces que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="0e5c7-116">Because MAPI calls **LoadLibrary** either every time it uses a service provider DLL (regardless of whether it has already been loaded) or only the first time, your service provider must not make assumptions about the number of times that it will be loaded.</span></span> <span data-ttu-id="0e5c7-117">Para todas las llamadas a **LoadLibrary**, MAPI realiza una llamada a la función **FreeLibrary** cuando un proveedor de servicios que ya no se necesita el archivo DLL de API de Windows.</span><span class="sxs-lookup"><span data-stu-id="0e5c7-117">For every call to **LoadLibrary**, MAPI makes a call to the Windows API function **FreeLibrary** when a service provider DLL is no longer needed.</span></span> 
    
- <span data-ttu-id="0e5c7-118">Llamar a la función de punto de entrada para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="0e5c7-118">Calling the entry point function for the provider.</span></span> <span data-ttu-id="0e5c7-119">MAPI llama a la función de punto de entrada de su proveedor para iniciar el proceso de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="0e5c7-119">MAPI calls your provider's entry point function to initiate the logon process.</span></span> <span data-ttu-id="0e5c7-120">Funciones de punto de entrada Asegúrese de que está usando una versión de la interfaz de proveedor de servicios (SPI) que es compatible con la versión que se está usa de MAPI.</span><span class="sxs-lookup"><span data-stu-id="0e5c7-120">Entry point functions ensure that you are using a version of the service provider interface (SPI) that is compatible with the version being used by MAPI.</span></span> <span data-ttu-id="0e5c7-121">Estas funciones también devuelven punteros a objetos de proveedor recién creado.</span><span class="sxs-lookup"><span data-stu-id="0e5c7-121">These functions also return pointers to newly created provider objects.</span></span> <span data-ttu-id="0e5c7-122">Para obtener más información sobre la creación de una entrada de función de punto de su proveedor, vea [implementar una función de punto de servicio de proveedor de entrada](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="0e5c7-122">For more information about creating an entry point function for your provider, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0e5c7-123">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="0e5c7-123">See also</span></span>



[<span data-ttu-id="0e5c7-124">Proveedores de servicios de MAPI</span><span class="sxs-lookup"><span data-stu-id="0e5c7-124">MAPI Service Providers</span></span>](mapi-service-providers.md)

