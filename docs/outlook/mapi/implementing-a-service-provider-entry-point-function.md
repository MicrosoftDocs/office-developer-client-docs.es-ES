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
ms.openlocfilehash: 14dd11f873493e32b83dbd1960cac8ff8ef8e436
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332994"
---
# <a name="implementing-a-service-provider-entry-point-function"></a><span data-ttu-id="7e88e-103">Implementar una función de punto de entrada de proveedor de servicios</span><span class="sxs-lookup"><span data-stu-id="7e88e-103">Implementing a Service Provider Entry Point Function</span></span>

  
  
<span data-ttu-id="7e88e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7e88e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7e88e-105">Cada DLL de proveedor de servicios tiene una función de punto de entrada a la que MAPI llama para cargarla.</span><span class="sxs-lookup"><span data-stu-id="7e88e-105">Every service provider DLL has an entry point function that MAPI calls to load it.</span></span> <span data-ttu-id="7e88e-106">Tenga en cuenta que esta función de punto de entrada no es lo mismo que [DllMain](https://msdn.microsoft.com/library/ms682583.aspx), la función de punto de entrada de dll de Win32.</span><span class="sxs-lookup"><span data-stu-id="7e88e-106">Be aware that this entry point function is not the same as [DllMain](https://msdn.microsoft.com/library/ms682583.aspx), the Win32 DLL entry point function.</span></span>
  
<span data-ttu-id="7e88e-107">Según el tipo de proveedor, la función de punto de entrada de proveedor se ajusta a un prototipo diferente.</span><span class="sxs-lookup"><span data-stu-id="7e88e-107">Depending on the type of your provider, your provider entry point function conforms to a different prototype.</span></span> <span data-ttu-id="7e88e-108">MAPI define distintos prototipos de función de punto de entrada para proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="7e88e-108">MAPI defines different entry point function prototypes for service providers.</span></span>
  
|<span data-ttu-id="7e88e-109">**Provider**</span><span class="sxs-lookup"><span data-stu-id="7e88e-109">**Provider**</span></span>|<span data-ttu-id="7e88e-110">**Prototipo de función de punto de entrada**</span><span class="sxs-lookup"><span data-stu-id="7e88e-110">**Entry point function prototype**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7e88e-111">Proveedores de almacenamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="7e88e-111">Message store providers</span></span>  <br/> |[<span data-ttu-id="7e88e-112">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="7e88e-112">MSProviderInit</span></span>](msproviderinit.md) <br/> |
|<span data-ttu-id="7e88e-113">Proveedores de transporte</span><span class="sxs-lookup"><span data-stu-id="7e88e-113">Transport providers</span></span>  <br/> |[<span data-ttu-id="7e88e-114">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="7e88e-114">XPProviderInit</span></span>](xpproviderinit.md) <br/> |
|<span data-ttu-id="7e88e-115">Proveedores de libretas de direcciones</span><span class="sxs-lookup"><span data-stu-id="7e88e-115">Address book providers</span></span>  <br/> |[<span data-ttu-id="7e88e-116">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="7e88e-116">ABProviderInit</span></span>](abproviderinit.md) <br/> |
   
<span data-ttu-id="7e88e-117">Gran parte de la funcionalidad de estos prototipos es la misma para todos los tipos de proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="7e88e-117">Much of the functionality in these prototypes is the same for all service provider types.</span></span> 
  
<span data-ttu-id="7e88e-118">La libreta de direcciones, el almacén de mensajes y los proveedores de transporte realizan las dos siguientes tareas principales en sus funciones de punto de entrada:</span><span class="sxs-lookup"><span data-stu-id="7e88e-118">Address book, message store, and transport providers perform the following two main tasks in their entry point functions:</span></span>
  
1. <span data-ttu-id="7e88e-119">Compruebe la versión de la interfaz del proveedor de servicios (SPI) para asegurarse de que MAPI está usando una versión compatible con la versión que usa el proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="7e88e-119">Check the version of the service provider interface (SPI) to be sure that MAPI is using a version that is compatible with the version that your service provider is using.</span></span> <span data-ttu-id="7e88e-120">Use el parámetro _lpulMAPIVer_ , que contiene la versión de MAPI SPI, y el parámetro _lpulProviderVer_ , que contiene la versión de SPI, para realizar la comprobación.</span><span class="sxs-lookup"><span data-stu-id="7e88e-120">Use the  _lpulMAPIVer_ parameter, which contains the MAPI SPI version, and the  _lpulProviderVer_ parameter, which contains your SPI version, to perform the check.</span></span> <span data-ttu-id="7e88e-121">Estos parámetros son enteros sin signo de 32 bits compuestos por tres partes:</span><span class="sxs-lookup"><span data-stu-id="7e88e-121">These parameters are 32-bit unsigned integers composed of three parts:</span></span> 
    
  - <span data-ttu-id="7e88e-122">Los bits del 24 al 31 representan la versión principal.</span><span class="sxs-lookup"><span data-stu-id="7e88e-122">Bits 24 through 31 represent the major version.</span></span>
    
  - <span data-ttu-id="7e88e-123">Los bits 16 a 23 representan la versión secundaria.</span><span class="sxs-lookup"><span data-stu-id="7e88e-123">Bits 16 through 23 represent the minor version.</span></span>
    
  - <span data-ttu-id="7e88e-124">Los bits del 0 al 15 representan el identificador de actualización.</span><span class="sxs-lookup"><span data-stu-id="7e88e-124">Bits 0 through 15 represent the update identifier.</span></span> <span data-ttu-id="7e88e-125">Aunque el número de versión principal rara vez cambia, el número de versión secundaria cambia siempre que se suelta MAPI y el SPI ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="7e88e-125">Although the major version number rarely changes, the minor version number changes whenever MAPI is released and the SPI has changed.</span></span> <span data-ttu-id="7e88e-126">El identificador de actualización es la versión de compilación interna de Microsoft; se usa para realizar un seguimiento de los cambios durante el proceso de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="7e88e-126">The update identifier is the Microsoft internal build version; it is used to track changes during the development process.</span></span> <span data-ttu-id="7e88e-127">MAPI define la constante CURRENT_SPI_VERSION, documentada en el archivo de encabezado Mapispi. h, para indicar la versión de SPI actual.</span><span class="sxs-lookup"><span data-stu-id="7e88e-127">MAPI defines the CURRENT_SPI_VERSION constant, documented in the Mapispi.h header file, to indicate the present SPI version.</span></span> <span data-ttu-id="7e88e-128">Si usa una versión de SPI que sea más reciente que la versión que MAPI está usando, no podrá realizar la comprobación con el error MAPI_E_VERSION.</span><span class="sxs-lookup"><span data-stu-id="7e88e-128">Fail your check with the error MAPI_E_VERSION if you are using a version of the SPI that is newer than the version that MAPI is using.</span></span>
    
2. <span data-ttu-id="7e88e-129">Cree una instancia de un objeto de proveedor.</span><span class="sxs-lookup"><span data-stu-id="7e88e-129">Create an instance of a provider object.</span></span> <span data-ttu-id="7e88e-130">Dado que el proveedor se puede iniciar e inicializar varias veces, debe crear una nueva instancia cada vez que se produzca este error.</span><span class="sxs-lookup"><span data-stu-id="7e88e-130">Because your provider can be started and initialized multiple times, you should create a new instance each time this occurs.</span></span> <span data-ttu-id="7e88e-131">Los proveedores se inician varias veces cuando aparecen en varios perfiles que están en uso simultáneamente por uno o más clientes, o cuando aparecen varias veces en un solo perfil.</span><span class="sxs-lookup"><span data-stu-id="7e88e-131">Providers are started multiple times when they appear in multiple profiles that are in use simultaneously by one or more clients, or when they appear multiple times in a single profile.</span></span> <span data-ttu-id="7e88e-132">Al igual que el prototipo de función de punto de entrada difiere en función del tipo de proveedor, también lo hace el tipo de objeto de proveedor.</span><span class="sxs-lookup"><span data-stu-id="7e88e-132">Just as the entry point function prototype differs depending on the type of your provider, so does the type of provider object.</span></span> 
    
    <span data-ttu-id="7e88e-133">Si está escribiendo un proveedor de libreta de direcciones, implemente [IABProvider: IUnknown](iabprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="7e88e-133">If you are writing an address book provider, implement [IABProvider : IUnknown](iabprovideriunknown.md).</span></span> <span data-ttu-id="7e88e-134">Si está escribiendo un proveedor de almacenamiento de mensajes, implemente [IMSProvider: IUnknown](imsprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="7e88e-134">If you are writing a message store provider, implement [IMSProvider : IUnknown](imsprovideriunknown.md).</span></span> <span data-ttu-id="7e88e-135">Para obtener más información, vea [cargar proveedores de almacenamiento de mensajes](loading-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="7e88e-135">For more information, see [Loading Message Store Providers](loading-message-store-providers.md).</span></span>
    
    <span data-ttu-id="7e88e-136">Si está escribiendo un proveedor de transporte, implemente [IXPProvider: IUnknown](ixpprovideriunknown.md).</span><span class="sxs-lookup"><span data-stu-id="7e88e-136">If you are writing a transport provider, implement [IXPProvider : IUnknown](ixpprovideriunknown.md).</span></span> <span data-ttu-id="7e88e-137">Para obtener más información, consulte [inicializar el proveedor de transporte](initializing-the-transport-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7e88e-137">For more information, see [Initializing the Transport Provider](initializing-the-transport-provider.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7e88e-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e88e-138">See also</span></span>



[<span data-ttu-id="7e88e-139">Inicio de un proveedor de servicios</span><span class="sxs-lookup"><span data-stu-id="7e88e-139">Starting a Service Provider</span></span>](starting-a-service-provider.md)

