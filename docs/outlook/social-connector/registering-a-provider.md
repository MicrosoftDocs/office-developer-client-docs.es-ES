---
title: Registrar un proveedor
manager: soliver
ms.date: 03/05/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b60b3634-4c8b-4273-97a0-0a8a5a8a5342
description: En este tema se describe las ubicaciones del registro de Windows que se usan cuando se instala un proveedor de Outlook Social Connector (OSC).
ms.openlocfilehash: 3ec594ec94b045d2ceb583144781a5746b945b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821206"
---
# <a name="registering-a-provider"></a><span data-ttu-id="e3f46-103">Registrar un proveedor</span><span class="sxs-lookup"><span data-stu-id="e3f46-103">Registering a provider</span></span>

<span data-ttu-id="e3f46-104">En este tema se describe las ubicaciones del registro de Windows que se usan cuando se instala un proveedor de Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="e3f46-104">This topic describes the Windows registry locations that are used when you install an Outlook Social Connector (OSC) provider.</span></span>
  
## <a name="com-registration"></a><span data-ttu-id="e3f46-105">Registro COM</span><span class="sxs-lookup"><span data-stu-id="e3f46-105">COM registration</span></span>

<span data-ttu-id="e3f46-106">Debe configurar el proveedor de OSC DLL para registrar el uso de registro automático de COM o regsvr32 durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="e3f46-106">You must configure the OSC provider DLL to register using COM self-registration or regsvr32 during installation.</span></span> <span data-ttu-id="e3f46-107">Registro de COM de la DLL del proveedor registra el proveedor de OSC bajo la `HKEY_CLASSES_ROOT` subárbol del registro.</span><span class="sxs-lookup"><span data-stu-id="e3f46-107">COM registration of the provider DLL registers the OSC provider under the `HKEY_CLASSES_ROOT` registry hive.</span></span> 
  
<span data-ttu-id="e3f46-108">Un proveedor de OSC desarrollado en código administrado tiene un ensamblado COM-visible del proveedor.</span><span class="sxs-lookup"><span data-stu-id="e3f46-108">An OSC provider developed in managed code has a COM-visible provider assembly.</span></span> <span data-ttu-id="e3f46-109">Debe usar un dominio de aplicación independiente para el componente de proveedor.</span><span class="sxs-lookup"><span data-stu-id="e3f46-109">You should use a separate application domain for the provider component.</span></span> <span data-ttu-id="e3f46-110">De lo contrario, el proveedor de OSC usa el dominio de aplicación compartida predeterminada que se usa en otros componentes, y el proveedor no funcionen según lo previsto.</span><span class="sxs-lookup"><span data-stu-id="e3f46-110">Otherwise, the OSC provider uses the default shared application domain that is used by other components, and the provider may not operate as expected.</span></span>
  
## <a name="registering-provider-progid"></a><span data-ttu-id="e3f46-111">Registrar proveedor ProgID</span><span class="sxs-lookup"><span data-stu-id="e3f46-111">Registering provider ProgID</span></span>

<span data-ttu-id="e3f46-112">Cada proveedor de OSC debe registrar un identificador de programación (`ProgID`).</span><span class="sxs-lookup"><span data-stu-id="e3f46-112">Each OSC provider must register a programmatic identifier (`ProgID`).</span></span> <span data-ttu-id="e3f46-113">El instalador de proveedor puede elegir una de las siguientes ubicaciones para agregar o quitar el `ProgID`:</span><span class="sxs-lookup"><span data-stu-id="e3f46-113">The provider installer can choose one of the following locations to add or remove the `ProgID`:</span></span>
  
- <span data-ttu-id="e3f46-114">`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash; Al instalador del proveedor debe usar esta ubicación si el proveedor está instalado para sólo el usuario que inició sesión actualmente.</span><span class="sxs-lookup"><span data-stu-id="e3f46-114">`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` &ndash; Your provider installer should use this location if the provider is installed for only the currently logged-on user.</span></span>
    
- <span data-ttu-id="e3f46-115">`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash; Al instalador del proveedor debe usar esta ubicación si el proveedor está instalado para todos los usuarios en el equipo.</span><span class="sxs-lookup"><span data-stu-id="e3f46-115">`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` &ndash; Your provider installer should use this location if the provider is installed for all users on the computer.</span></span>
    
<span data-ttu-id="e3f46-116">Busca el OSC para el proveedor de `ProgID` en las ubicaciones anteriores, a menos que el equipo cliente tenga Outlook de 32 bits que se ejecutan en un sistema operativo de Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="e3f46-116">The OSC looks for the provider  `ProgID` in the above locations, unless the client computer has 32-bit Outlook running on a 64-bit Windows operating system.</span></span> <span data-ttu-id="e3f46-117">En tal caso, el instalador de proveedor debe elegir una de las siguientes ubicaciones en la `HKEY_CURRENT_USER` o `HKEY_LOCAL_MACHINE` subárbol:</span><span class="sxs-lookup"><span data-stu-id="e3f46-117">In such a case, your provider installer should choose one of the following locations in the  `HKEY_CURRENT_USER` or  `HKEY_LOCAL_MACHINE` hive:</span></span> 
  
- `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
<span data-ttu-id="e3f46-118">Para obtener una versión de hacer clic y ejecutar de Office, el instalador de proveedor debe elegir una de las siguientes ubicaciones en el subárbol HKEY_CURRENT_USER o HKEY_LOCAL_MACHINE:</span><span class="sxs-lookup"><span data-stu-id="e3f46-118">For a Click-to-Run version of Office, your provider installer should choose one of the following locations in the HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE hive:</span></span>
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Outlook\SocialConnector\SocialProviders`
    
## <a name="see-also"></a><span data-ttu-id="e3f46-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3f46-119">See also</span></span>

- [<span data-ttu-id="e3f46-120">Lista de comprobación de instalación</span><span class="sxs-lookup"><span data-stu-id="e3f46-120">Installation Checklist</span></span>](installation-checklist.md)
- [<span data-ttu-id="e3f46-121">Pasos rápidos para aprender a desarrollar un proveedor</span><span class="sxs-lookup"><span data-stu-id="e3f46-121">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)
- [<span data-ttu-id="e3f46-122">Implementación de un proveedor</span><span class="sxs-lookup"><span data-stu-id="e3f46-122">Deploying a Provider</span></span>](deploying-a-provider.md)

