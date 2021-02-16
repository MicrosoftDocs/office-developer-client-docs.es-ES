---
title: Introducción al desarrollo de un proveedor de Outlook Social Connector
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c65d2df-86a3-48d5-9fec-a9040f3b878c
description: La referencia del proveedor de Outlook Social Connector (OSC) describe cómo desarrollar un proveedor de OSC mediante la extensibilidad del proveedor de OSC.
ms.openlocfilehash: 24f8eabe33103f53e848f055b72fd402bc5dd89a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327163"
---
# <a name="getting-started-with-developing-an-outlook-social-connector-provider"></a><span data-ttu-id="e881d-103">Introducción al desarrollo de un proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="e881d-103">Getting started with developing an Outlook Social Connector provider</span></span>

<span data-ttu-id="e881d-104">La referencia del proveedor de Outlook Social Connector (OSC) describe cómo desarrollar un proveedor de OSC mediante la extensibilidad del proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="e881d-104">The Outlook Social Connector (OSC) Provider Reference describes how to develop an OSC provider by using OSC provider extensibility.</span></span> <span data-ttu-id="e881d-105">Si no tiene experiencia en el desarrollo de soluciones para Outlook, consulte Seleccionar una API o tecnología para desarrollar soluciones de Outlook para identificar las [API](https://msdn.microsoft.com/library/8295da20-e567-4d08-b8e4-5c9b4498edd4%28Office.15%29.aspx) y tecnologías más adecuadas para sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="e881d-105">If you are new to developing solutions for Outlook, see [Selecting an API or Technology for Developing Outlook Solutions](https://msdn.microsoft.com/library/8295da20-e567-4d08-b8e4-5c9b4498edd4%28Office.15%29.aspx) to identify the APIs and technologies that are most appropriate for your needs.</span></span> 

<span data-ttu-id="e881d-106">En esta sección se proporciona información general sobre la OSC, cómo un proveedor de OSC puede ser útil, pasos rápidos para aprender a desarrollar un proveedor, requisitos técnicos, procedimientos recomendados para desarrollar un proveedor y novedades de esta versión.</span><span class="sxs-lookup"><span data-stu-id="e881d-106">This section gives an overview of the OSC, how an OSC provider can be useful, quick steps for learning to develop a provider, technical requirements, best practices for developing a provider, and what's new in this release.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="e881d-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="e881d-107">In this section</span></span>

- <span data-ttu-id="e881d-108">[Novedades](what-s-new-for-providers.md)para proveedores: compara las características de OSC de la versión anterior y actual, y describe los miembros de la interfaz y los elementos de esquema XML que se han agregado, cambiado o desusado en esta versión.</span><span class="sxs-lookup"><span data-stu-id="e881d-108">[What's New for Providers](what-s-new-for-providers.md): Compares OSC features in the previous and current release, and describes interface members and XML schema elements that have been added, changed, or deprecated in this release.</span></span> 
    
- <span data-ttu-id="e881d-109">[Por qué desarrollar un proveedor de Outlook Social Connector:](why-develop-an-outlook-social-connector-provider.md)describe cómo un proveedor de OSC puede ser útil para sitios de redes sociales comunes y otras herramientas de red interna.</span><span class="sxs-lookup"><span data-stu-id="e881d-109">[Why Develop an Outlook Social Connector Provider](why-develop-an-outlook-social-connector-provider.md): Describes how an OSC provider can be useful for common social network sites and other internal networking tools.</span></span>
    
- <span data-ttu-id="e881d-110">[Relación del sistema operativo con Outlook](relating-the-osc-with-outlook-and-social-networks.md)y redes sociales: proporciona una vista arquitectónica de cómo el OSC conecta a los usuarios de Outlook con las redes sociales.</span><span class="sxs-lookup"><span data-stu-id="e881d-110">[Relating the OSC with Outlook and Social Networks](relating-the-osc-with-outlook-and-social-networks.md): Provides an architectural view of how the OSC connects Outlook users with social networks.</span></span> <span data-ttu-id="e881d-111">También define la forma en que se usan términos comunes, como "redes sociales", "amigos", "no amigos" y "contactos" en el resto de esta referencia.</span><span class="sxs-lookup"><span data-stu-id="e881d-111">Also defines the way that common terms, like "social networks," "friends," "non-friends," and "contacts" are used in the rest of this reference.</span></span>
    
- <span data-ttu-id="e881d-112">[Pasos rápidos para aprender a desarrollar un](quick-steps-for-learning-to-develop-a-provider.md)proveedor: proporciona un resumen de los pasos para aprender a desarrollar un proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="e881d-112">[Quick Steps for Learning to Develop a Provider](quick-steps-for-learning-to-develop-a-provider.md): Provides a summary of steps to learn to develop an OSC provider.</span></span>
    
- <span data-ttu-id="e881d-113">[Requisitos técnicos:](technical-requirements.md)describe los lenguajes de programación compatibles, los requisitos de visibilidad COM, los requisitos de tipo de devolución de métodos y los detalles de la DLL de extensibilidad del proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="e881d-113">[Technical Requirements](technical-requirements.md): Describes the supported programming languages, COM visibility requirements, method return type requirements, and details of the OSC provider extensibility DLL.</span></span>
    
- <span data-ttu-id="e881d-114">[Procedimientos recomendados para desarrollar un proveedor:](best-practices-for-developing-a-provider.md)proporciona una lista de procedimientos recomendados a seguir durante el desarrollo de un proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="e881d-114">[Best Practices for Developing a Provider](best-practices-for-developing-a-provider.md): Provides a list of best practices to follow while developing an OSC provider.</span></span>
    
## <a name="reference"></a><span data-ttu-id="e881d-115">Referencia</span><span class="sxs-lookup"><span data-stu-id="e881d-115">Reference</span></span>

- [<span data-ttu-id="e881d-116">Referencia del proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="e881d-116">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="e881d-117">Secciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="e881d-117">Related sections</span></span>

- [<span data-ttu-id="e881d-118">Plantillas de ejemplo de OSC</span><span class="sxs-lookup"><span data-stu-id="e881d-118">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="e881d-119">Secuencias de llamada típicas de OSC</span><span class="sxs-lookup"><span data-stu-id="e881d-119">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="e881d-120">Desarrollo de un proveedor con el esquema XML de OSC</span><span class="sxs-lookup"><span data-stu-id="e881d-120">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="e881d-121">Depurar un proveedor</span><span class="sxs-lookup"><span data-stu-id="e881d-121">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="e881d-122">Implementación de un proveedor</span><span class="sxs-lookup"><span data-stu-id="e881d-122">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="e881d-123">Prepararse para publicar un proveedor de OSC</span><span class="sxs-lookup"><span data-stu-id="e881d-123">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="e881d-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e881d-124">See also</span></span>

- [<span data-ttu-id="e881d-125">Microsoft Outlook Social Connector de 32 bits</span><span class="sxs-lookup"><span data-stu-id="e881d-125">Microsoft Outlook Social Connector 32-bit</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=b638cc14-11e5-448a-b5a6-4f553ce81b94)
- [<span data-ttu-id="e881d-126">Actualización de Outlook Social Connector (KB983403), edición de 32 bits</span><span class="sxs-lookup"><span data-stu-id="e881d-126">Update for Outlook Social Connector (KB983403), 32-Bit Edition</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=9886faca-f1c5-4579-83e2-c872c7abc61a)
- [<span data-ttu-id="e881d-127">Actualización de Outlook Social Connector (KB983403), edición de 64 bits</span><span class="sxs-lookup"><span data-stu-id="e881d-127">Update for Outlook Social Connector (KB983403), 64-bit Edition</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=72a506a7-8a91-4d56-8b27-bf3b3f58fe9a)
- [<span data-ttu-id="e881d-128">Outlook Social Connector 2013: Plantillas de proveedor</span><span class="sxs-lookup"><span data-stu-id="e881d-128">Outlook Social Connector 2013: Provider templates</span></span>](https://code.msdn.microsoft.com/Outlook-Social-Connector-73fd8d2c)

