---
title: Pasos rápidos para aprender a desarrollar un proveedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13c0ae8c-d268-4bf0-942d-2a6160142f5e
description: En este tema se sugiere algunos pasos para obtener más información acerca de cómo desarrollar un proveedor de Outlook Social Connector (OSC).
ms.openlocfilehash: 345e8600c704504be091ee23c66b7f85575cde90
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821212"
---
# <a name="quick-steps-for-learning-to-develop-a-provider"></a><span data-ttu-id="756c3-103">Pasos rápidos para aprender a desarrollar un proveedor</span><span class="sxs-lookup"><span data-stu-id="756c3-103">Quick steps for learning to develop a provider</span></span>

<span data-ttu-id="756c3-104">Para desarrollar un proveedor de OSC, debe completar los siguientes pasos generales:</span><span class="sxs-lookup"><span data-stu-id="756c3-104">To develop an OSC provider, you need to complete the following general steps:</span></span>
  
- <span data-ttu-id="756c3-105">Implementar las cuatro interfaces obligatorias: [ISocialProvider](isocialprovideriunknown.md), [ISocialSession](isocialsessioniunknown.md), [ISocialProfile](isocialprofileisocialperson.md)y [ISocialPerson](isocialpersoniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="756c3-105">Implement the four mandatory interfaces: [ISocialProvider](isocialprovideriunknown.md), [ISocialSession](isocialsessioniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), and [ISocialPerson](isocialpersoniunknown.md).</span></span> <span data-ttu-id="756c3-106">Función de soporte técnico de su red social para almacenar en caché las credenciales de inicio de sesión, seguimiento de una persona en la red social, o dinámicamente sincronización amigos y sus actividades, es posible que desee implementar la interfaz [ISocialSession2](isocialsession2iunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="756c3-106">Depending on your social network's support for caching logon credentials, following a person on the social network, or dynamically synchronizing friends and their activities, you might want to implement the [ISocialSession2](isocialsession2iunknown.md) interface.</span></span> 
    
- <span data-ttu-id="756c3-107">En paralelo con la implementación de interfaces, probar y depurar el proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="756c3-107">In parallel with implementing interfaces, test and debug the OSC provider.</span></span> 

- <span data-ttu-id="756c3-108">Implementar el proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="756c3-108">Deploy the OSC provider.</span></span>  

- <span data-ttu-id="756c3-109">Realice pruebas finales antes del lanzamiento.</span><span class="sxs-lookup"><span data-stu-id="756c3-109">Do final testing before release.</span></span>
    
## <a name="step-a-implementing-interfaces"></a><span data-ttu-id="756c3-110">Paso A: implementar interfaces</span><span class="sxs-lookup"><span data-stu-id="756c3-110">Step A: Implementing interfaces</span></span>

<span data-ttu-id="756c3-111">Un proveedor de OSC implementa interfaces para que el OSC puede usar estas interfaces para obtener la información necesaria sobre o desde la red social, a través del proveedor OSC.</span><span class="sxs-lookup"><span data-stu-id="756c3-111">An OSC provider implements interfaces so that the OSC can use these interfaces to obtain necessary information about or from the social network, through the OSC provider.</span></span> <span data-ttu-id="756c3-112">Dicha información incluye lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="756c3-112">Such information includes the following:</span></span>
  
- <span data-ttu-id="756c3-113">Procedimiento para presentar el cuadro de diálogo de inicio de sesión de cuenta para un usuario.</span><span class="sxs-lookup"><span data-stu-id="756c3-113">How to present the account logon dialog to a user.</span></span>    
- <span data-ttu-id="756c3-114">Si el proveedor admite que muestra amigos o actividades, tal como se muestra en la red social.</span><span class="sxs-lookup"><span data-stu-id="756c3-114">Whether the provider supports showing friends or activities as displayed on the social network.</span></span>    
- <span data-ttu-id="756c3-115">Cómo mostrar amigos y actividades en la tarjeta de contacto o el panel de personas de Outlook.</span><span class="sxs-lookup"><span data-stu-id="756c3-115">How to display friends and activities in the Contact Card or Outlook People Pane.</span></span>     
- <span data-ttu-id="756c3-116">Cuándo se debe actualizar la información de amigos o actividades en la tarjeta de contacto o el panel de personas.</span><span class="sxs-lookup"><span data-stu-id="756c3-116">When to refresh friends or activities information on the Contact Card or People Pane.</span></span>
    
<span data-ttu-id="756c3-117">La información normalmente se pasa desde el proveedor al OSC, con el formato de cadenas XML como parámetros de salida de los métodos de interfaz.</span><span class="sxs-lookup"><span data-stu-id="756c3-117">The information is typically passed from the provider to the OSC, in the form of XML strings as output parameters of interface methods.</span></span> <span data-ttu-id="756c3-118">El OSC y un proveedor de OSC cumplan con el esquema XML de proveedor OSC.</span><span class="sxs-lookup"><span data-stu-id="756c3-118">Both the OSC and an OSC provider comply with the OSC provider XML schema.</span></span> <span data-ttu-id="756c3-119">Por lo tanto, en el transcurso de implementar las interfaces, necesita una buena comprensión de cómo el esquema XML permite especificar información como enumerados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="756c3-119">Therefore, in the course of implementing the interfaces, you need a good understanding of how the XML schema allows you to specify information as listed above.</span></span> 

<span data-ttu-id="756c3-120">Los siguientes recursos explican cómo especificar XML de actividades, amigos y capacidades de proveedor:</span><span class="sxs-lookup"><span data-stu-id="756c3-120">The following resources explain how to specify XML for provider capabilities, friends, and activities:</span></span>
  
- [<span data-ttu-id="756c3-121">Secuencias de llamada típicas de OSC</span><span class="sxs-lookup"><span data-stu-id="756c3-121">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)    
- [<span data-ttu-id="756c3-122">Sincronización de amigos y actividades</span><span class="sxs-lookup"><span data-stu-id="756c3-122">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)    
- [<span data-ttu-id="756c3-123">Ejemplo de XML de capacidades</span><span class="sxs-lookup"><span data-stu-id="756c3-123">Capabilities XML Example</span></span>](capabilities-xml-example.md)   
- [<span data-ttu-id="756c3-124">XML de capacidades</span><span class="sxs-lookup"><span data-stu-id="756c3-124">XML for Capabilities</span></span>](xml-for-capabilities.md)    
- [<span data-ttu-id="756c3-125">Ejemplo de XML de amigos</span><span class="sxs-lookup"><span data-stu-id="756c3-125">Friends XML Example</span></span>](friends-xml-example.md)    
- [<span data-ttu-id="756c3-126">XML de amigos</span><span class="sxs-lookup"><span data-stu-id="756c3-126">XML for Friends</span></span>](xml-for-friends.md)   
- [<span data-ttu-id="756c3-127">Ejemplo de XML de fuentes de actividades</span><span class="sxs-lookup"><span data-stu-id="756c3-127">Activity Feed XML Example</span></span>](activity-feed-xml-example.md)   
- [<span data-ttu-id="756c3-128">XML de actividades</span><span class="sxs-lookup"><span data-stu-id="756c3-128">XML for Activities</span></span>](xml-for-activities.md)
    
<span data-ttu-id="756c3-129">Antes de comenzar la implementación, consulte también los temas siguientes para ahorrar tiempo más adelante en el proceso de depuración:</span><span class="sxs-lookup"><span data-stu-id="756c3-129">Before you start implementation, also consult the following topics to save you time later in the debugging process:</span></span>
  
- [<span data-ttu-id="756c3-130">Requisitos técnicos</span><span class="sxs-lookup"><span data-stu-id="756c3-130">Technical Requirements</span></span>](technical-requirements.md)    
- [<span data-ttu-id="756c3-131">Prácticas recomendadas para desarrollar un proveedor</span><span class="sxs-lookup"><span data-stu-id="756c3-131">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)    
- [<span data-ttu-id="756c3-132">Plantillas de ejemplo OSC</span><span class="sxs-lookup"><span data-stu-id="756c3-132">OSC Sample Templates</span></span>](osc-sample-templates.md)
    
## <a name="step-b-debugging"></a><span data-ttu-id="756c3-133">Depuración de paso B:</span><span class="sxs-lookup"><span data-stu-id="756c3-133">Step B: Debugging</span></span>

<span data-ttu-id="756c3-134">El tema [Depurar un proveedor](debugging-a-provider.md) se sugieren procedimientos que puede utilizar al desarrollar un proveedor de OSC de depuración.</span><span class="sxs-lookup"><span data-stu-id="756c3-134">The topic [Debugging a Provider](debugging-a-provider.md) suggests debugging procedures you can use while developing an OSC provider.</span></span> 
  
<span data-ttu-id="756c3-135">Mientras desarrolla, también puede hacer referencia a [Introducción listo para liberar un proveedor de OSC](getting-ready-to-release-an-osc-provider.md) para obtener una mejor comprensión del comportamiento esperado en ciertos escenarios (por ejemplo, la autenticación básica y basada en formularios).</span><span class="sxs-lookup"><span data-stu-id="756c3-135">While you are developing, you can also refer to [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md) to gain a better understanding of the expected behavior in certain scenarios (for example, basic and forms-based authentication).</span></span> 
  
## <a name="step-c-deploying"></a><span data-ttu-id="756c3-136">Implementación de paso C:</span><span class="sxs-lookup"><span data-stu-id="756c3-136">Step C: Deploying</span></span>

<span data-ttu-id="756c3-137">Consulte los siguientes temas para obtener más información acerca de los requisitos de implementación:</span><span class="sxs-lookup"><span data-stu-id="756c3-137">See the following topics to learn about deployment requirements:</span></span>
  
- [<span data-ttu-id="756c3-138">Implementación de un proveedor</span><span class="sxs-lookup"><span data-stu-id="756c3-138">Deploying a Provider</span></span>](deploying-a-provider.md)    
- [<span data-ttu-id="756c3-139">Registrar un proveedor</span><span class="sxs-lookup"><span data-stu-id="756c3-139">Registering a Provider</span></span>](registering-a-provider.md)   
- [<span data-ttu-id="756c3-140">Lista de comprobación de instalación</span><span class="sxs-lookup"><span data-stu-id="756c3-140">Installation Checklist</span></span>](installation-checklist.md)
    
## <a name="step-d-final-testing-before-release"></a><span data-ttu-id="756c3-141">Paso D: las pruebas antes del lanzamiento de Final</span><span class="sxs-lookup"><span data-stu-id="756c3-141">Step D: Final testing before release</span></span>

<span data-ttu-id="756c3-142">Dependiendo de su red social y el proveedor de OSC, existen pruebas específicas del proveedor normalmente que debe llevar a cabo antes de liberar su proveedor.</span><span class="sxs-lookup"><span data-stu-id="756c3-142">Depending on your social network and the OSC provider, there are usually provider-specific tests you should carry out before you release your provider.</span></span> <span data-ttu-id="756c3-143">Para obtener una lista sugerida de pruebas, vea [Introducción listo para liberar un proveedor de OSC](getting-ready-to-release-an-osc-provider.md).</span><span class="sxs-lookup"><span data-stu-id="756c3-143">For a suggested list of tests, see [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="756c3-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="756c3-144">See also</span></span>

- [<span data-ttu-id="756c3-145">Introducción al desarrollo de un proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="756c3-145">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

