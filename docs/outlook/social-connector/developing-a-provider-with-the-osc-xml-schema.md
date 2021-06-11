---
title: Desarrollar un proveedor con el esquema XML de OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0872b1b9-c21f-4bba-8cf1-4b010d8d7fb6
description: El esquema XML del proveedor Outlook Social Connector (OSC) define el formato de una cantidad significativa de información que se pasa de una red social a través del proveedor de OSC de la red al OSC.
ms.openlocfilehash: 2346e23beb2de1664ec90263a8f5db5d46c54e6f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539258"
---
# <a name="developing-a-provider-with-the-osc-xml-schema"></a><span data-ttu-id="b295a-103">Desarrollar un proveedor con el esquema XML de OSC</span><span class="sxs-lookup"><span data-stu-id="b295a-103">Developing a provider with the OSC XML schema</span></span>

<span data-ttu-id="b295a-104">El esquema XML del proveedor Outlook Social Connector (OSC) define el formato de una cantidad significativa de información que se pasa de una red social a través del proveedor de OSC de la red al OSC.</span><span class="sxs-lookup"><span data-stu-id="b295a-104">The Outlook Social Connector (OSC) provider XML schema defines the format of a significant amount of information that is passed from a social network through the network's OSC provider to the OSC.</span></span> <span data-ttu-id="b295a-105">El esquema XML permite a un proveedor de OSC especificar las capacidades del proveedor, los amigos y los elementos de fuente de actividad en la red social, mediante el uso de los tres elementos principales, **capacidades,** amigos y **activityFeed** y sus elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="b295a-105">The XML schema allows an OSC provider to specify capabilities of the provider, friends, and activity feed items on the social network, by using the three main elements, **capabilities**, **friends**, and **activityFeed**, and their child elements.</span></span> <span data-ttu-id="b295a-106">El proveedor de OSC implementa interfaces y sus métodos en la extensibilidad del proveedor de OSC, devolviendo cadenas XML como parámetros de salida que cumplen con el esquema XML del proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="b295a-106">The OSC provider implements interfaces and their methods in the OSC provider extensibility, returning XML strings as output parameters that comply with the OSC provider XML schema.</span></span> <span data-ttu-id="b295a-107">El OSC llama a estos métodos para obtener información que puede comprender según lo definido por el esquema XML.</span><span class="sxs-lookup"><span data-stu-id="b295a-107">The OSC calls these methods to obtain information that it can understand as defined by the XML schema.</span></span>
  
> [!NOTE]
> <span data-ttu-id="b295a-108">La extensibilidad del proveedor OSC admite la depuración de proveedores estableciendo el `DebugProviders` valor de la clave del Registro en  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` 1.</span><span class="sxs-lookup"><span data-stu-id="b295a-108">OSC provider extensibility supports debugging providers by setting the `DebugProviders` value of the  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` registry key to 1.</span></span> <span data-ttu-id="b295a-109">Al activar la depuración del proveedor, el OSC valida el XML del proveedor con la versión del esquema XML de OSC que especifique en el atributo XML **xmlns.**</span><span class="sxs-lookup"><span data-stu-id="b295a-109">When you turn on provider debugging, the OSC validates the provider XML against the version of the OSC XML schema that you specify in the **xmlns** XML attribute.</span></span> <span data-ttu-id="b295a-110">Para OSC 1.1 y versiones del OSC desde Outlook Social Connector 2013, especifique el atributo **xmlns** de la siguiente manera:`xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`</span><span class="sxs-lookup"><span data-stu-id="b295a-110">For OSC 1.1 and versions of the OSC since Outlook Social Connector 2013, specify the **xmlns** attribute as follows: `xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="b295a-111">En esta sección</span><span class="sxs-lookup"><span data-stu-id="b295a-111">In this section</span></span>

- <span data-ttu-id="b295a-112">[Sincronizar amigos](synchronizing-friends-and-activities.md)y actividades: describe las distintas formas en que los proveedores de OSC pueden sincronizar amigos, no amigos y actividades en una red social.</span><span class="sxs-lookup"><span data-stu-id="b295a-112">[Synchronizing Friends and Activities](synchronizing-friends-and-activities.md): Describes the various ways that OSC providers can synchronize friends, non-friends, and activities on a social network.</span></span> 
    
- <span data-ttu-id="b295a-113">Ejemplos XML del proveedor de [OSC:](osc-provider-xml-examples.md)incluye ejemplos XML que muestran cómo especificar funcionalidades de un proveedor de OSC, amigos y elementos de fuente de actividad en una red social mediante el esquema XML de OSC.</span><span class="sxs-lookup"><span data-stu-id="b295a-113">[OSC Provider XML Examples](osc-provider-xml-examples.md): Includes XML examples that show how to specify capabilities of an OSC provider, friends, and activity feed items on a social network by using the OSC XML schema.</span></span>
    
- <span data-ttu-id="b295a-114">[XML para funcionalidades:](xml-for-capabilities.md)explica el método - [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) que el OSC usa para obtener información de capacidades, expresada en **XML** de capacidades, del proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="b295a-114">[XML for Capabilities](xml-for-capabilities.md): Explains the - [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method that the OSC uses to obtain capabilities information, expressed in **capabilities** XML, from the OSC provider.</span></span> <span data-ttu-id="b295a-115">En esta sección también se describen los elementos XML del esquema XML del proveedor de OSC que permiten a un proveedor de OSC especificar su funcionalidad, incluida la forma en que autentica a los usuarios y sincroniza amigos y actividades.</span><span class="sxs-lookup"><span data-stu-id="b295a-115">This section also describes the XML elements in the OSC provider XML schema that allow an OSC provider to specify its functionality, including how it authenticates users and synchronizes friends and activities.</span></span> 
    
- <span data-ttu-id="b295a-116">[XML para amigos:](xml-for-friends.md)proporciona ejemplos de las API que usa el OSC para obtener información de amigos, expresada en **XML** de amigos, del proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="b295a-116">[XML for Friends](xml-for-friends.md): Gives examples of the APIs that the OSC uses to obtain friends' information, expressed in **friends** XML, from the OSC provider.</span></span> <span data-ttu-id="b295a-117">En esta sección también se describen los elementos del XML **de amigos.**</span><span class="sxs-lookup"><span data-stu-id="b295a-117">This section also describes elements in the **friends** XML.</span></span> 
    
- <span data-ttu-id="b295a-118">[XML para actividades:](xml-for-activities.md)proporciona ejemplos de las API que usa el OSC para obtener información de actividades, expresada en **activityFeed** XML, del proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="b295a-118">[XML for Activities](xml-for-activities.md): Gives examples of the APIs that the OSC uses to obtain activities information, expressed in **activityFeed** XML, from the OSC provider.</span></span> <span data-ttu-id="b295a-119">En esta sección también se describen los elementos XML del esquema XML del proveedor de OSC que permiten a un proveedor de OSC especificar una fuente de actividad.</span><span class="sxs-lookup"><span data-stu-id="b295a-119">This section also describes the XML elements in the OSC provider XML schema that allow an OSC provider to specify an activity feed.</span></span> <span data-ttu-id="b295a-120">Una fuente de actividad incluye la red donde se originaron los elementos de fuente de actividad, los detalles de cada elemento de fuente de actividad (como el propietario, el tipo y la fecha de publicación de la actividad) y la plantilla para mostrar la actividad.</span><span class="sxs-lookup"><span data-stu-id="b295a-120">An activity feed includes the network where the activity feed items originated, details of each activity feed item (such as owner, type, and publish date of the activity), and the template to display the activity.</span></span> 
    
## <a name="reference"></a><span data-ttu-id="b295a-121">Referencia</span><span class="sxs-lookup"><span data-stu-id="b295a-121">Reference</span></span>

- [<span data-ttu-id="b295a-122">Outlook Referencia del proveedor de Social Connector</span><span class="sxs-lookup"><span data-stu-id="b295a-122">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="b295a-123">Secciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="b295a-123">Related sections</span></span>

- [<span data-ttu-id="b295a-124">Introducción al desarrollo de un Outlook social connector</span><span class="sxs-lookup"><span data-stu-id="b295a-124">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [<span data-ttu-id="b295a-125">Plantillas de ejemplo de OSC</span><span class="sxs-lookup"><span data-stu-id="b295a-125">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="b295a-126">Secuencias de llamadas típicas de OSC</span><span class="sxs-lookup"><span data-stu-id="b295a-126">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="b295a-127">Depuración de un proveedor</span><span class="sxs-lookup"><span data-stu-id="b295a-127">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="b295a-128">Implementación de un proveedor</span><span class="sxs-lookup"><span data-stu-id="b295a-128">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="b295a-129">Procedimientos recomendados para desarrollar un proveedor</span><span class="sxs-lookup"><span data-stu-id="b295a-129">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="b295a-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="b295a-130">See also</span></span>

- [<span data-ttu-id="b295a-131">Depuración de un proveedor</span><span class="sxs-lookup"><span data-stu-id="b295a-131">Debugging a Provider</span></span>](debugging-a-provider.md)

