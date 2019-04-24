---
title: Pasos rápidos para aprender a desarrollar un proveedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13c0ae8c-d268-4bf0-942d-2a6160142f5e
description: En este tema se sugieren algunos pasos para aprender a desarrollar un proveedor de Outlook Social Connector (OSC).
ms.openlocfilehash: 581997ab257d59062761d97bfef49a88b90bb1e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329221"
---
# <a name="quick-steps-for-learning-to-develop-a-provider"></a><span data-ttu-id="36a02-103">Pasos rápidos para aprender a desarrollar un proveedor</span><span class="sxs-lookup"><span data-stu-id="36a02-103">Quick steps for learning to develop a provider</span></span>

<span data-ttu-id="36a02-104">Para desarrollar un proveedor OSC, debe completar los siguientes pasos generales:</span><span class="sxs-lookup"><span data-stu-id="36a02-104">To develop an OSC provider, you need to complete the following general steps:</span></span>
  
- <span data-ttu-id="36a02-105">Implemente las cuatro interfaces obligatorias: [ISocialProvider](isocialprovideriunknown.md), [ISocialSession](isocialsessioniunknown.md), [ISocialProfile](isocialprofileisocialperson.md)y [ISocialPerson](isocialpersoniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="36a02-105">Implement the four mandatory interfaces: [ISocialProvider](isocialprovideriunknown.md), [ISocialSession](isocialsessioniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), and [ISocialPerson](isocialpersoniunknown.md).</span></span> <span data-ttu-id="36a02-106">Según la compatibilidad de su red social con el almacenamiento en caché de las credenciales de inicio de sesión, el seguimiento de una persona en la red social o la sincronización dinámica de amigos y sus actividades, es posible que desee implementar la interfaz de [ISocialSession2](isocialsession2iunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="36a02-106">Depending on your social network's support for caching logon credentials, following a person on the social network, or dynamically synchronizing friends and their activities, you might want to implement the [ISocialSession2](isocialsession2iunknown.md) interface.</span></span> 
    
- <span data-ttu-id="36a02-107">En paralelo con la implementación de interfaces, pruebe y Depure el proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="36a02-107">In parallel with implementing interfaces, test and debug the OSC provider.</span></span> 

- <span data-ttu-id="36a02-108">Implemente el proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="36a02-108">Deploy the OSC provider.</span></span>  

- <span data-ttu-id="36a02-109">Realice las pruebas finales antes de la publicación.</span><span class="sxs-lookup"><span data-stu-id="36a02-109">Do final testing before release.</span></span>
    
## <a name="step-a-implementing-interfaces"></a><span data-ttu-id="36a02-110">Paso A: implementación de interfaces</span><span class="sxs-lookup"><span data-stu-id="36a02-110">Step A: Implementing interfaces</span></span>

<span data-ttu-id="36a02-111">Un proveedor OSC implementa interfaces para que el OSC pueda usarlas para obtener información necesaria sobre o desde la red social a través del proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="36a02-111">An OSC provider implements interfaces so that the OSC can use these interfaces to obtain necessary information about or from the social network, through the OSC provider.</span></span> <span data-ttu-id="36a02-112">Esta información incluye lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="36a02-112">Such information includes the following:</span></span>
  
- <span data-ttu-id="36a02-113">Cómo presentar el cuadro de diálogo de inicio de sesión de la cuenta a un usuario.</span><span class="sxs-lookup"><span data-stu-id="36a02-113">How to present the account logon dialog to a user.</span></span>    
- <span data-ttu-id="36a02-114">Si el proveedor admite la visualización de amigos o actividades como se muestra en la red social.</span><span class="sxs-lookup"><span data-stu-id="36a02-114">Whether the provider supports showing friends or activities as displayed on the social network.</span></span>    
- <span data-ttu-id="36a02-115">Cómo mostrar amigos y actividades en el panel de la tarjeta de contacto o de personas de Outlook.</span><span class="sxs-lookup"><span data-stu-id="36a02-115">How to display friends and activities in the Contact Card or Outlook People Pane.</span></span>     
- <span data-ttu-id="36a02-116">Cuándo actualizar la información de amigos o actividades en la tarjeta de contacto o en el panel de personas.</span><span class="sxs-lookup"><span data-stu-id="36a02-116">When to refresh friends or activities information on the Contact Card or People Pane.</span></span>
    
<span data-ttu-id="36a02-117">Normalmente, la información se pasa del proveedor al OSC, en forma de cadenas XML como parámetros de salida de los métodos de interfaz.</span><span class="sxs-lookup"><span data-stu-id="36a02-117">The information is typically passed from the provider to the OSC, in the form of XML strings as output parameters of interface methods.</span></span> <span data-ttu-id="36a02-118">Tanto OSC como un proveedor de OSC cumplen con el esquema XML del proveedor OSC.</span><span class="sxs-lookup"><span data-stu-id="36a02-118">Both the OSC and an OSC provider comply with the OSC provider XML schema.</span></span> <span data-ttu-id="36a02-119">Por lo tanto, en el transcurso de la implementación de las interfaces, necesitará una buena comprensión de cómo el esquema XML le permite especificar la información indicada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="36a02-119">Therefore, in the course of implementing the interfaces, you need a good understanding of how the XML schema allows you to specify information as listed above.</span></span> 

<span data-ttu-id="36a02-120">Los siguientes recursos explican cómo especificar XML para capacidades, amigos y actividades del proveedor:</span><span class="sxs-lookup"><span data-stu-id="36a02-120">The following resources explain how to specify XML for provider capabilities, friends, and activities:</span></span>
  
- [<span data-ttu-id="36a02-121">Secuencias de llamada típicas de OSC</span><span class="sxs-lookup"><span data-stu-id="36a02-121">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)    
- [<span data-ttu-id="36a02-122">Sincronización de amigos y actividades</span><span class="sxs-lookup"><span data-stu-id="36a02-122">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)    
- [<span data-ttu-id="36a02-123">Ejemplo de XML de capacidades</span><span class="sxs-lookup"><span data-stu-id="36a02-123">Capabilities XML Example</span></span>](capabilities-xml-example.md)   
- [<span data-ttu-id="36a02-124">XML para funcionalidades</span><span class="sxs-lookup"><span data-stu-id="36a02-124">XML for Capabilities</span></span>](xml-for-capabilities.md)    
- [<span data-ttu-id="36a02-125">Ejemplo de XML de amigos</span><span class="sxs-lookup"><span data-stu-id="36a02-125">Friends XML Example</span></span>](friends-xml-example.md)    
- [<span data-ttu-id="36a02-126">XML para amigos</span><span class="sxs-lookup"><span data-stu-id="36a02-126">XML for Friends</span></span>](xml-for-friends.md)   
- [<span data-ttu-id="36a02-127">Ejemplo de XML de fuente de actividades</span><span class="sxs-lookup"><span data-stu-id="36a02-127">Activity Feed XML Example</span></span>](activity-feed-xml-example.md)   
- [<span data-ttu-id="36a02-128">XML para actividades</span><span class="sxs-lookup"><span data-stu-id="36a02-128">XML for Activities</span></span>](xml-for-activities.md)
    
<span data-ttu-id="36a02-129">Antes de comenzar con la implementación, consulte también los siguientes temas para ahorrar tiempo más adelante en el proceso de depuración:</span><span class="sxs-lookup"><span data-stu-id="36a02-129">Before you start implementation, also consult the following topics to save you time later in the debugging process:</span></span>
  
- [<span data-ttu-id="36a02-130">Requisitos técnicos</span><span class="sxs-lookup"><span data-stu-id="36a02-130">Technical Requirements</span></span>](technical-requirements.md)    
- [<span data-ttu-id="36a02-131">Procedimientos recomendados para desarrollar un proveedor</span><span class="sxs-lookup"><span data-stu-id="36a02-131">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)    
- [<span data-ttu-id="36a02-132">Plantillas de ejemplo de OSC</span><span class="sxs-lookup"><span data-stu-id="36a02-132">OSC Sample Templates</span></span>](osc-sample-templates.md)
    
## <a name="step-b-debugging"></a><span data-ttu-id="36a02-133">Paso B: dePurar</span><span class="sxs-lookup"><span data-stu-id="36a02-133">Step B: Debugging</span></span>

<span data-ttu-id="36a02-134">El tema [depuración de un proveedor](debugging-a-provider.md) sugiere procedimientos de depuración que puede usar al desarrollar un proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="36a02-134">The topic [Debugging a Provider](debugging-a-provider.md) suggests debugging procedures you can use while developing an OSC provider.</span></span> 
  
<span data-ttu-id="36a02-135">Mientras está desarrollando, también puede consultar el tema [Getting Ready to release a OSC Provider](getting-ready-to-release-an-osc-provider.md) para obtener una mejor comprensión del comportamiento esperado en determinados escenarios (por ejemplo, autenticación básica y basada en formularios).</span><span class="sxs-lookup"><span data-stu-id="36a02-135">While you are developing, you can also refer to [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md) to gain a better understanding of the expected behavior in certain scenarios (for example, basic and forms-based authentication).</span></span> 
  
## <a name="step-c-deploying"></a><span data-ttu-id="36a02-136">Paso C: implementación</span><span class="sxs-lookup"><span data-stu-id="36a02-136">Step C: Deploying</span></span>

<span data-ttu-id="36a02-137">Consulte los siguientes temas para obtener información sobre los requisitos de implementación:</span><span class="sxs-lookup"><span data-stu-id="36a02-137">See the following topics to learn about deployment requirements:</span></span>
  
- [<span data-ttu-id="36a02-138">Implementación de un proveedor</span><span class="sxs-lookup"><span data-stu-id="36a02-138">Deploying a Provider</span></span>](deploying-a-provider.md)    
- [<span data-ttu-id="36a02-139">Registrar un proveedor</span><span class="sxs-lookup"><span data-stu-id="36a02-139">Registering a Provider</span></span>](registering-a-provider.md)   
- [<span data-ttu-id="36a02-140">Lista de comprobación de instalación</span><span class="sxs-lookup"><span data-stu-id="36a02-140">Installation Checklist</span></span>](installation-checklist.md)
    
## <a name="step-d-final-testing-before-release"></a><span data-ttu-id="36a02-141">Paso D: pruebas finales antes de la publicación</span><span class="sxs-lookup"><span data-stu-id="36a02-141">Step D: Final testing before release</span></span>

<span data-ttu-id="36a02-142">En función de su red social y del proveedor de OSC, normalmente hay pruebas específicas del proveedor que debe realizar antes de publicar el proveedor.</span><span class="sxs-lookup"><span data-stu-id="36a02-142">Depending on your social network and the OSC provider, there are usually provider-specific tests you should carry out before you release your provider.</span></span> <span data-ttu-id="36a02-143">Para obtener una lista de pruebas recomendadas, vea [Getting Ready to release a OSC Provider](getting-ready-to-release-an-osc-provider.md).</span><span class="sxs-lookup"><span data-stu-id="36a02-143">For a suggested list of tests, see [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="36a02-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="36a02-144">See also</span></span>

- [<span data-ttu-id="36a02-145">Introducción al desarrollo de un proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="36a02-145">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

