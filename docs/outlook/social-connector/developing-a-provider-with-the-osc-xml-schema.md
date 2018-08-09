---
title: Desarrollar un proveedor con el esquema XML de OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0872b1b9-c21f-4bba-8cf1-4b010d8d7fb6
description: El esquema XML de proveedor de Outlook Social Connector (OSC) define el formato de una gran cantidad de información que se pasa de una red social a través de proveedor OSC de la red para el OSC.
ms.openlocfilehash: 93df682751146b501a316be62641b8cfd47a74a8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821100"
---
# <a name="developing-a-provider-with-the-osc-xml-schema"></a><span data-ttu-id="985e5-103">Desarrollar un proveedor con el esquema XML de OSC</span><span class="sxs-lookup"><span data-stu-id="985e5-103">Developing a provider with the OSC XML schema</span></span>

<span data-ttu-id="985e5-104">El esquema XML de proveedor de Outlook Social Connector (OSC) define el formato de una gran cantidad de información que se pasa de una red social a través de proveedor OSC de la red para el OSC.</span><span class="sxs-lookup"><span data-stu-id="985e5-104">The Outlook Social Connector (OSC) provider XML schema defines the format of a significant amount of information that is passed from a social network through the network's OSC provider to the OSC.</span></span> <span data-ttu-id="985e5-105">El esquema XML permite que un proveedor de OSC especificar las capacidades del proveedor, amigos y fuente de elementos de la red social, mediante el uso de los tres elementos principales, **capacidades**, **amigos**y **activityFeed**y sus secundarios de actividades elementos.</span><span class="sxs-lookup"><span data-stu-id="985e5-105">The XML schema allows an OSC provider to specify capabilities of the provider, friends, and activity feed items on the social network, by using the three main elements, **capabilities**, **friends**, and **activityFeed**, and their child elements.</span></span> <span data-ttu-id="985e5-106">El proveedor OSC implementa interfaces y sus métodos en la extensibilidad del proveedor OSC, devolver cadenas XML como parámetros de salida que cumplen con el esquema XML de proveedor OSC.</span><span class="sxs-lookup"><span data-stu-id="985e5-106">The OSC provider implements interfaces and their methods in the OSC provider extensibility, returning XML strings as output parameters that comply with the OSC provider XML schema.</span></span> <span data-ttu-id="985e5-107">El OSC llama a estos métodos para obtener información que puede comprender como se define en el esquema XML.</span><span class="sxs-lookup"><span data-stu-id="985e5-107">The OSC calls these methods to obtain information that it can understand as defined by the XML schema.</span></span>
  
> [!NOTE]
> <span data-ttu-id="985e5-108">Extensibilidad de proveedores OSC es compatible con los proveedores de depuración estableciendo el `DebugProviders` valor de la `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` clave del registro en 1.</span><span class="sxs-lookup"><span data-stu-id="985e5-108">OSC provider extensibility supports debugging providers by setting the `DebugProviders` value of the  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` registry key to 1.</span></span> <span data-ttu-id="985e5-109">Cuando se activa el proveedor de depuración, el OSC valida el proveedor XML frente a la versión del esquema XML de OSC que especifique en el atributo XML **xmlns** .</span><span class="sxs-lookup"><span data-stu-id="985e5-109">When you turn on provider debugging, the OSC validates the provider XML against the version of the OSC XML schema that you specify in the **xmlns** XML attribute.</span></span> <span data-ttu-id="985e5-110">Para 1.1 OSC y versiones de la OSC desde Outlook Social Connector 2013, especifique el atributo **xmlns** como se indica a continuación:`xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`</span><span class="sxs-lookup"><span data-stu-id="985e5-110">For OSC 1.1 and versions of the OSC since Outlook Social Connector 2013, specify the **xmlns** attribute as follows: `xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="985e5-111">En esta sección</span><span class="sxs-lookup"><span data-stu-id="985e5-111">In this section</span></span>

- <span data-ttu-id="985e5-112">[Sincronización de amigos y actividades](synchronizing-friends-and-activities.md): describe las distintas maneras en que pueden sincronizar proveedores de OSC amigos, que no sean de amigos y actividades en una red social.</span><span class="sxs-lookup"><span data-stu-id="985e5-112">[Synchronizing Friends and Activities](synchronizing-friends-and-activities.md): Describes the various ways that OSC providers can synchronize friends, non-friends, and activities on a social network.</span></span> 
    
- <span data-ttu-id="985e5-113">[Ejemplos de XML de proveedor de OSC](osc-provider-xml-examples.md): ejemplos de XML incluye que muestran cómo especificar las capacidades de un proveedor de OSC, amigos y actividad de fuente de los elementos en una red social utilizando el esquema XML de OSC.</span><span class="sxs-lookup"><span data-stu-id="985e5-113">[OSC Provider XML Examples](osc-provider-xml-examples.md): Includes XML examples that show how to specify capabilities of an OSC provider, friends, and activity feed items on a social network by using the OSC XML schema.</span></span>
    
- <span data-ttu-id="985e5-114">[XML de capacidades](xml-for-capabilities.md): se explica el - método de [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) que usa el OSC para obtener información sobre las capacidades, expresado en el XML de las **capacidades** , desde el proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="985e5-114">[XML for Capabilities](xml-for-capabilities.md): Explains the - [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method that the OSC uses to obtain capabilities information, expressed in **capabilities** XML, from the OSC provider.</span></span> <span data-ttu-id="985e5-115">Esta sección también describen los elementos XML en el esquema XML de proveedor OSC que permiten a un proveedor de OSC especificar su funcionalidad, incluido cómo autentica a los usuarios y se sincroniza amigos y actividades.</span><span class="sxs-lookup"><span data-stu-id="985e5-115">This section also describes the XML elements in the OSC provider XML schema that allow an OSC provider to specify its functionality, including how it authenticates users and synchronizes friends and activities.</span></span> 
    
- <span data-ttu-id="985e5-116">[XML para amigos](xml-for-friends.md): se proporcionan ejemplos de las API que usa el OSC para obtener información de amigos, expresado en **amigos** XML, desde el proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="985e5-116">[XML for Friends](xml-for-friends.md): Gives examples of the APIs that the OSC uses to obtain friends' information, expressed in **friends** XML, from the OSC provider.</span></span> <span data-ttu-id="985e5-117">Esta sección también describen los elementos de **amigos** XML.</span><span class="sxs-lookup"><span data-stu-id="985e5-117">This section also describes elements in the **friends** XML.</span></span> 
    
- <span data-ttu-id="985e5-118">[XML para actividades](xml-for-activities.md): se proporcionan ejemplos de las API que usa el OSC para obtener información sobre actividades, expresado en **activityFeed** XML, desde el proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="985e5-118">[XML for Activities](xml-for-activities.md): Gives examples of the APIs that the OSC uses to obtain activities information, expressed in **activityFeed** XML, from the OSC provider.</span></span> <span data-ttu-id="985e5-119">Esta sección también describen los elementos XML en el esquema XML de proveedor OSC que permiten a un proveedor de OSC especificar una fuente de actividades.</span><span class="sxs-lookup"><span data-stu-id="985e5-119">This section also describes the XML elements in the OSC provider XML schema that allow an OSC provider to specify an activity feed.</span></span> <span data-ttu-id="985e5-120">Una fuente de actividades incluye la red donde la actividad de fuente de los elementos de origen, detalles de cada elemento de la fuente de actividades (como propietario, escriba y fecha de publicación de la actividad) y la plantilla para mostrar la actividad.</span><span class="sxs-lookup"><span data-stu-id="985e5-120">An activity feed includes the network where the activity feed items originated, details of each activity feed item (such as owner, type, and publish date of the activity), and the template to display the activity.</span></span> 
    
## <a name="reference"></a><span data-ttu-id="985e5-121">Referencia</span><span class="sxs-lookup"><span data-stu-id="985e5-121">Reference</span></span>

- [<span data-ttu-id="985e5-122">Referencia del proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="985e5-122">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="985e5-123">Secciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="985e5-123">Related sections</span></span>

- [<span data-ttu-id="985e5-124">Introducción al desarrollo de un proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="985e5-124">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [<span data-ttu-id="985e5-125">Plantillas de ejemplo OSC</span><span class="sxs-lookup"><span data-stu-id="985e5-125">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="985e5-126">Secuencias de llamada típicas de OSC</span><span class="sxs-lookup"><span data-stu-id="985e5-126">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="985e5-127">Depurar un proveedor</span><span class="sxs-lookup"><span data-stu-id="985e5-127">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="985e5-128">Implementación de un proveedor</span><span class="sxs-lookup"><span data-stu-id="985e5-128">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="985e5-129">Prácticas recomendadas para desarrollar un proveedor</span><span class="sxs-lookup"><span data-stu-id="985e5-129">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="985e5-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="985e5-130">See also</span></span>

- [<span data-ttu-id="985e5-131">Depurar un proveedor</span><span class="sxs-lookup"><span data-stu-id="985e5-131">Debugging a Provider</span></span>](debugging-a-provider.md)

