---
title: Introducción al desarrollo de un proveedor de Outlook Social Connector
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c65d2df-86a3-48d5-9fec-a9040f3b878c
description: La referencia del proveedor de Outlook Social Connector (OSC) describe cómo desarrollar un proveedor OSC mediante la extensibilidad de proveedores de OSC.
ms.openlocfilehash: 24f8eabe33103f53e848f055b72fd402bc5dd89a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327163"
---
# <a name="getting-started-with-developing-an-outlook-social-connector-provider"></a><span data-ttu-id="1641c-103">Introducción al desarrollo de un proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="1641c-103">Getting started with developing an Outlook Social Connector provider</span></span>

<span data-ttu-id="1641c-104">La referencia del proveedor de Outlook Social Connector (OSC) describe cómo desarrollar un proveedor OSC mediante la extensibilidad de proveedores de OSC.</span><span class="sxs-lookup"><span data-stu-id="1641c-104">The Outlook Social Connector (OSC) Provider Reference describes how to develop an OSC provider by using OSC provider extensibility.</span></span> <span data-ttu-id="1641c-105">Si no está familiarizado con el desarrollo de soluciones para Outlook, vea [seleccionar una API o tecnología para desarrollar soluciones de Outlook](https://msdn.microsoft.com/library/8295da20-e567-4d08-b8e4-5c9b4498edd4%28Office.15%29.aspx) para identificar las API y tecnologías más adecuadas para sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="1641c-105">If you are new to developing solutions for Outlook, see [Selecting an API or Technology for Developing Outlook Solutions](https://msdn.microsoft.com/library/8295da20-e567-4d08-b8e4-5c9b4498edd4%28Office.15%29.aspx) to identify the APIs and technologies that are most appropriate for your needs.</span></span> 

<span data-ttu-id="1641c-106">En esta sección se ofrece información general sobre el OSC, el modo en que un proveedor OSC puede resultar útil, los pasos rápidos para aprender a desarrollar un proveedor, los requisitos técnicos, los procedimientos recomendados para desarrollar un proveedor y las novedades de esta versión.</span><span class="sxs-lookup"><span data-stu-id="1641c-106">This section gives an overview of the OSC, how an OSC provider can be useful, quick steps for learning to develop a provider, technical requirements, best practices for developing a provider, and what's new in this release.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="1641c-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="1641c-107">In this section</span></span>

- <span data-ttu-id="1641c-108">[What's New for Providers](what-s-new-for-providers.md): compara las características de OSC en la versión anterior y actual, y describe los miembros de la interfaz y los elementos del esquema XML que se han agregado, modificado o en desuso en esta versión.</span><span class="sxs-lookup"><span data-stu-id="1641c-108">[What's New for Providers](what-s-new-for-providers.md): Compares OSC features in the previous and current release, and describes interface members and XML schema elements that have been added, changed, or deprecated in this release.</span></span> 
    
- <span data-ttu-id="1641c-109">[Por qué desarrollar un proveedor de Outlook Social Connector](why-develop-an-outlook-social-connector-provider.md): se describe el modo en que un proveedor OSC puede resultar útil para sitios de redes sociales comunes y otras herramientas de red interna.</span><span class="sxs-lookup"><span data-stu-id="1641c-109">[Why Develop an Outlook Social Connector Provider](why-develop-an-outlook-social-connector-provider.md): Describes how an OSC provider can be useful for common social network sites and other internal networking tools.</span></span>
    
- <span data-ttu-id="1641c-110">[Relacionar el OSC con Outlook y las redes sociales](relating-the-osc-with-outlook-and-social-networks.md): proporciona una vista arquitectónica de cómo el OSC conecta a los usuarios de Outlook con redes sociales.</span><span class="sxs-lookup"><span data-stu-id="1641c-110">[Relating the OSC with Outlook and Social Networks](relating-the-osc-with-outlook-and-social-networks.md): Provides an architectural view of how the OSC connects Outlook users with social networks.</span></span> <span data-ttu-id="1641c-111">También define el modo en que se usan los términos comunes, como "redes sociales", "amigos", "non-Friends" y "Contacts" en el resto de esta referencia.</span><span class="sxs-lookup"><span data-stu-id="1641c-111">Also defines the way that common terms, like "social networks," "friends," "non-friends," and "contacts" are used in the rest of this reference.</span></span>
    
- <span data-ttu-id="1641c-112">[Pasos rápidos para aprender a desarrollar un proveedor](quick-steps-for-learning-to-develop-a-provider.md): proporciona un resumen de los pasos para aprender a desarrollar un proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="1641c-112">[Quick Steps for Learning to Develop a Provider](quick-steps-for-learning-to-develop-a-provider.md): Provides a summary of steps to learn to develop an OSC provider.</span></span>
    
- <span data-ttu-id="1641c-113">[Requisitos técnicos](technical-requirements.md): describe los lenguajes de programación admitidos, los requisitos de visibilidad de com, los requisitos de tipo de valor devuelto del método y los detalles de la dll de extensibilidad del proveedor OSC.</span><span class="sxs-lookup"><span data-stu-id="1641c-113">[Technical Requirements](technical-requirements.md): Describes the supported programming languages, COM visibility requirements, method return type requirements, and details of the OSC provider extensibility DLL.</span></span>
    
- <span data-ttu-id="1641c-114">[Procedimientos recomendados para desarrollar un proveedor](best-practices-for-developing-a-provider.md): proporciona una lista de procedimientos recomendados para seguir desarrollando un proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="1641c-114">[Best Practices for Developing a Provider](best-practices-for-developing-a-provider.md): Provides a list of best practices to follow while developing an OSC provider.</span></span>
    
## <a name="reference"></a><span data-ttu-id="1641c-115">Referencia</span><span class="sxs-lookup"><span data-stu-id="1641c-115">Reference</span></span>

- [<span data-ttu-id="1641c-116">Referencia del proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="1641c-116">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="1641c-117">Secciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="1641c-117">Related sections</span></span>

- [<span data-ttu-id="1641c-118">Plantillas de ejemplo de OSC</span><span class="sxs-lookup"><span data-stu-id="1641c-118">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="1641c-119">Secuencias de llamada típicas de OSC</span><span class="sxs-lookup"><span data-stu-id="1641c-119">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="1641c-120">Desarrollo de un proveedor con el esquema XML de OSC</span><span class="sxs-lookup"><span data-stu-id="1641c-120">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="1641c-121">DePuración de un proveedor</span><span class="sxs-lookup"><span data-stu-id="1641c-121">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="1641c-122">Implementación de un proveedor</span><span class="sxs-lookup"><span data-stu-id="1641c-122">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="1641c-123">Preparación para la publicación de un proveedor OSC</span><span class="sxs-lookup"><span data-stu-id="1641c-123">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="1641c-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="1641c-124">See also</span></span>

- [<span data-ttu-id="1641c-125">Microsoft Outlook Social Connector 32-bit</span><span class="sxs-lookup"><span data-stu-id="1641c-125">Microsoft Outlook Social Connector 32-bit</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=b638cc14-11e5-448a-b5a6-4f553ce81b94)
- [<span data-ttu-id="1641c-126">Actualización para Outlook Social Connector (KB983403), 32-bit Edition</span><span class="sxs-lookup"><span data-stu-id="1641c-126">Update for Outlook Social Connector (KB983403), 32-Bit Edition</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=9886faca-f1c5-4579-83e2-c872c7abc61a)
- [<span data-ttu-id="1641c-127">Actualización para Outlook Social Connector (KB983403), 64-bit Edition</span><span class="sxs-lookup"><span data-stu-id="1641c-127">Update for Outlook Social Connector (KB983403), 64-bit Edition</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=72a506a7-8a91-4d56-8b27-bf3b3f58fe9a)
- [<span data-ttu-id="1641c-128">Outlook Social Connector 2013: plantillas de proveedor</span><span class="sxs-lookup"><span data-stu-id="1641c-128">Outlook Social Connector 2013: Provider templates</span></span>](https://code.msdn.microsoft.com/Outlook-Social-Connector-73fd8d2c)

