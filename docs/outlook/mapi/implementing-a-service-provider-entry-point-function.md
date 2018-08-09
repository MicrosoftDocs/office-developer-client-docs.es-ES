---
title: Implementar una función de punto de entrada de proveedor de servicios
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 83ff54c4-86ce-4529-ae45-260dfb763b30
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 632aff9c0f6fc60ee9730b5e43667b5b610ae8df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817674"
---
# <a name="implementing-a-service-provider-entry-point-function"></a><span data-ttu-id="abc14-103">Implementar una función de punto de entrada de proveedor de servicios</span><span class="sxs-lookup"><span data-stu-id="abc14-103">Implementing a Service Provider Entry Point Function</span></span>

  
  
<span data-ttu-id="abc14-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="abc14-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="abc14-105">Cada proveedor de servicios de DLL tiene una entrada de función que llama MAPI para cargarlo de punto.</span><span class="sxs-lookup"><span data-stu-id="abc14-105">Every service provider DLL has an entry point function that MAPI calls to load it.</span></span> <span data-ttu-id="abc14-106">Tenga en cuenta que esta función de punto de entrada no es el mismo que [DllMain](http://msdn.microsoft.com/en-us/library/ms682583.aspx), la función de punto de entrada de DLL de Win32.</span><span class="sxs-lookup"><span data-stu-id="abc14-106">Be aware that this entry point function is not the same as [DllMain](http://msdn.microsoft.com/en-us/library/ms682583.aspx), the Win32 DLL entry point function.</span></span>
  
<span data-ttu-id="abc14-107">Según el tipo de su proveedor, la función de punto de entrada de proveedor se ajusta a un prototipo diferente.</span><span class="sxs-lookup"><span data-stu-id="abc14-107">Depending on the type of your provider, your provider entry point function conforms to a different prototype.</span></span> <span data-ttu-id="abc14-108">MAPI define los prototipos de función de punto de entrada diferente para los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="abc14-108">MAPI defines different entry point function prototypes for service providers.</span></span>
  
|<span data-ttu-id="abc14-109">**Provider**</span><span class="sxs-lookup"><span data-stu-id="abc14-109">**Provider**</span></span>|<span data-ttu-id="abc14-110">**Prototipo de función de punto de entrada**</span><span class="sxs-lookup"><span data-stu-id="abc14-110">**Entry point function prototype**</span></span>|
|:-----|:-----|
|<span data-ttu-id="abc14-111">Proveedores de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="abc14-111">Message store providers</span></span>  <br/> |[<span data-ttu-id="abc14-112">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="abc14-112">MSProviderInit</span></span>](msproviderinit.md) <br/> |
|<span data-ttu-id="abc14-113">Proveedores de transporte</span><span class="sxs-lookup"><span data-stu-id="abc14-113">Transport providers</span></span>  <br/> |[<span data-ttu-id="abc14-114">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="abc14-114">XPProviderInit</span></span>](xpproviderinit.md) <br/> |
|<span data-ttu-id="abc14-115">Proveedores de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="abc14-115">Address book providers</span></span>  <br/> |[<span data-ttu-id="abc14-116">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="abc14-116">ABProviderInit</span></span>](abproviderinit.md) <br/> |
   
<span data-ttu-id="abc14-117">Gran parte de la funcionalidad de estos prototipos es el mismo para todos los tipos de proveedor de servicio.</span><span class="sxs-lookup"><span data-stu-id="abc14-117">Much of the functionality in these prototypes is the same for all service provider types.</span></span> 
  
<span data-ttu-id="abc14-118">Libreta de direcciones, almacén de mensajes y los proveedores de transporte realizan las dos tareas principales siguientes en sus funciones de punto de entrada:</span><span class="sxs-lookup"><span data-stu-id="abc14-118">Address book, message store, and transport providers perform the following two main tasks in their entry point functions:</span></span>
  
1. <span data-ttu-id="abc14-119">Comprobar la versión de la interfaz de proveedor de servicios (SPI) para asegurarse de que MAPI está usando una versión que sea compatible con la versión que está usando el proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="abc14-119">Check the version of the service provider interface (SPI) to be sure that MAPI is using a version that is compatible with the version that your service provider is using.</span></span> <span data-ttu-id="abc14-120">Use el parámetro _lpulMAPIVer_ , que contiene la versión de MAPI SPI y el parámetro _lpulProviderVer_ , que contiene la versión SPI, para realizar la comprobación.</span><span class="sxs-lookup"><span data-stu-id="abc14-120">Use the  _lpulMAPIVer_ parameter, which contains the MAPI SPI version, and the  _lpulProviderVer_ parameter, which contains your SPI version, to perform the check.</span></span> <span data-ttu-id="abc14-121">Estos parámetros son números enteros sin signo de 32 bits consta de tres partes:</span><span class="sxs-lookup"><span data-stu-id="abc14-121">These parameters are 32-bit unsigned integers composed of three parts:</span></span> 
    
  - <span data-ttu-id="abc14-122">Bits 24 a 31 representan la versión principal.</span><span class="sxs-lookup"><span data-stu-id="abc14-122">Bits 24 through 31 represent the major version.</span></span>
    
  - <span data-ttu-id="abc14-123">Bits 16 a 23 representan la versión secundaria.</span><span class="sxs-lookup"><span data-stu-id="abc14-123">Bits 16 through 23 represent the minor version.</span></span>
    
  - <span data-ttu-id="abc14-124">Bits 0 a 15 representan el identificador de la actualización.</span><span class="sxs-lookup"><span data-stu-id="abc14-124">Bits 0 through 15 represent the update identifier.</span></span> <span data-ttu-id="abc14-125">Aunque rara vez se cambia el número de versión principal, el número de versión secundaria cambios cada vez que se libera MAPI y ha cambiado el SPI.</span><span class="sxs-lookup"><span data-stu-id="abc14-125">Although the major version number rarely changes, the minor version number changes whenever MAPI is released and the SPI has changed.</span></span> <span data-ttu-id="abc14-126">El identificador de actualización es el interno de Microsoft versión; de compilación se utiliza para realizar un seguimiento de los cambios durante el proceso de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="abc14-126">The update identifier is the Microsoft internal build version; it is used to track changes during the development process.</span></span> <span data-ttu-id="abc14-127">MAPI define la constante CURRENT_SPI_VERSION, que se documentaron en el archivo de encabezado Mapispi.h, para indicar la versión SPI presente.</span><span class="sxs-lookup"><span data-stu-id="abc14-127">MAPI defines the CURRENT_SPI_VERSION constant, documented in the Mapispi.h header file, to indicate the present SPI version.</span></span> <span data-ttu-id="abc14-128">Producirá un error en la comprobación con el error MAPI_E_VERSION si está usando una versión de SPI que es más reciente que la versión que está utilizando MAPI.</span><span class="sxs-lookup"><span data-stu-id="abc14-128">Fail your check with the error MAPI_E_VERSION if you are using a version of the SPI that is newer than the version that MAPI is using.</span></span>
    
2. <span data-ttu-id="abc14-129">Cree una instancia de un objeto de proveedor.</span><span class="sxs-lookup"><span data-stu-id="abc14-129">Create an instance of a provider object.</span></span> <span data-ttu-id="abc14-130">Debido a que su proveedor puede ser iniciado e inicializado varias veces, debe crear una nueva instancia cada vez que esto ocurre.</span><span class="sxs-lookup"><span data-stu-id="abc14-130">Because your provider can be started and initialized multiple times, you should create a new instance each time this occurs.</span></span> <span data-ttu-id="abc14-131">Los proveedores se inician varias veces cuando aparecen en varios perfiles que están en uso simultáneamente por uno o más clientes o cuando aparecen varias veces en un único perfil.</span><span class="sxs-lookup"><span data-stu-id="abc14-131">Providers are started multiple times when they appear in multiple profiles that are in use simultaneously by one or more clients, or when they appear multiple times in a single profile.</span></span> <span data-ttu-id="abc14-132">Al igual que el prototipo de función de punto de entrada difiere según el tipo de su proveedor, también lo hace el tipo de objeto de proveedor.</span><span class="sxs-lookup"><span data-stu-id="abc14-132">Just as the entry point function prototype differs depending on the type of your provider, so does the type of provider object.</span></span> 
    
    <span data-ttu-id="abc14-133">Si está escribiendo un proveedor de la libreta de direcciones, implementar [IABProvider: IUnknown](iabprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="abc14-133">If you are writing an address book provider, implement [IABProvider : IUnknown](iabprovideriunknown.md).</span></span> <span data-ttu-id="abc14-134">Si está escribiendo un proveedor de almacén de mensajes, implementar [IMSProvider: IUnknown](imsprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="abc14-134">If you are writing a message store provider, implement [IMSProvider : IUnknown](imsprovideriunknown.md).</span></span> <span data-ttu-id="abc14-135">Para obtener más información, vea [Cargar los proveedores de almacén de mensajes](loading-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="abc14-135">For more information, see [Loading Message Store Providers](loading-message-store-providers.md).</span></span>
    
    <span data-ttu-id="abc14-136">Si está escribiendo un proveedor de transporte, implementar [IXPProvider: IUnknown](ixpprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="abc14-136">If you are writing a transport provider, implement [IXPProvider : IUnknown](ixpprovideriunknown.md).</span></span> <span data-ttu-id="abc14-137">Para obtener más información, vea [inicializar el proveedor de transporte](initializing-the-transport-provider.md).</span><span class="sxs-lookup"><span data-stu-id="abc14-137">For more information, see [Initializing the Transport Provider](initializing-the-transport-provider.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="abc14-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="abc14-138">See also</span></span>



[<span data-ttu-id="abc14-139">Iniciar un proveedor de servicios</span><span class="sxs-lookup"><span data-stu-id="abc14-139">Starting a Service Provider</span></span>](starting-a-service-provider.md)

