---
title: Referencia de proveedores de Outlook Social Connector
manager: soliver
ms.date: 04/04/2016
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13661393-adf6-4870-86c4-303262317675
description: El Outlook Social Connector 2013 proporciona un concentrador de comunicación para las comunicaciones personales y profesionales.
ms.openlocfilehash: 32a9eb88b7724f8735d0eb8623bb3716ad836a7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821208"
---
# <a name="outlook-social-connector-provider-reference"></a><span data-ttu-id="de1bb-103">Referencia de proveedores de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="de1bb-103">Outlook Social Connector provider reference</span></span>

<span data-ttu-id="de1bb-104">El Outlook Social Connector 2013 proporciona un concentrador de comunicación para las comunicaciones personales y profesionales.</span><span class="sxs-lookup"><span data-stu-id="de1bb-104">The Outlook Social Connector 2013 provides a communication hub for personal and professional communications.</span></span> <span data-ttu-id="de1bb-105">Outlook Social Connector (OSC) funciona con SharePoint Server, SharePoint Workspace, cliente de Lync, y todas las aplicaciones de cliente de Office que admiten la información de presencia y la tarjeta de contacto admiten el OSC.</span><span class="sxs-lookup"><span data-stu-id="de1bb-105">The Outlook Social Connector (OSC) works with SharePoint Server, SharePoint Workspace, Lync client, and all Office client applications that support presence information and the Contact Card support the OSC.</span></span> 

<span data-ttu-id="de1bb-106">En Outlook en particular, simplemente, al seleccionar un elemento de Outlook como un correo electrónico o convocatoria de reunión y hacer clic en el remitente o un destinatario en ese elemento, sin salir de Outlook, los usuarios pueden ver en el panel de personas actividades, fotos y las actualizaciones de estado de esta persona en su redes sociales favoritas.</span><span class="sxs-lookup"><span data-stu-id="de1bb-106">In Outlook in particular, just by selecting an Outlook item such as an email or meeting request and clicking the sender or a recipient in that item, without leaving Outlook, users can see in the People Pane activities, photos, and status updates of this person on their favorite social networks.</span></span> <span data-ttu-id="de1bb-107">Los usuarios pueden ver fácilmente todas la Outlook mensajes de correo electrónico, datos adjuntos y reuniones recibidas de esta persona.</span><span class="sxs-lookup"><span data-stu-id="de1bb-107">Users can conveniently see all the Outlook emails, attachments, and meetings received from this person.</span></span> <span data-ttu-id="de1bb-108">En un entorno de la organización, también pueden ver los usuarios en un sitio de SharePoint en las actualizaciones de documentos del panel de personas y otras actividades de sitio de esta persona en el sitio de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="de1bb-108">In an organizational environment, users on a SharePoint site can also see in the People Pane document updates and other site activities of this person on the SharePoint site.</span></span>
  
<span data-ttu-id="de1bb-109">Una red social puede desarrollar un proveedor para el OSC para sincronizar y actualizaciones de redes sociales en servidores de apoyo y las aplicaciones de superficie.</span><span class="sxs-lookup"><span data-stu-id="de1bb-109">A social network can develop a provider for the OSC to synchronize and surface social network updates in supporting servers and applications.</span></span> <span data-ttu-id="de1bb-110">Las redes sociales más populares, como LinkedIn, Facebook y Windows Live ofrecen proveedores para el OSC.</span><span class="sxs-lookup"><span data-stu-id="de1bb-110">Popular social networks such as LinkedIn, Facebook, and Windows Live are offering providers for the OSC.</span></span> 
  
<span data-ttu-id="de1bb-111">La referencia de proveedores de Outlook Social Connector 2013 describe cómo desarrollar un proveedor OSC mediante extensibilidad del proveedor OSC.</span><span class="sxs-lookup"><span data-stu-id="de1bb-111">The Outlook Social Connector 2013 Provider Reference describes how to develop an OSC provider using OSC provider extensibility.</span></span> 
  
<span data-ttu-id="de1bb-112">Si está familiarizado con el desarrollo de soluciones para Outlook, vea [Seleccionar una API o tecnología para desarrollar soluciones de Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) para identificar las API y tecnologías que son los más adecuadas para sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="de1bb-112">If you are new to developing solutions for Outlook, see [Selecting an API or technology for developing solutions for Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) to identify the APIs and technologies that are most appropriate for your needs.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="de1bb-113">En esta sección</span><span class="sxs-lookup"><span data-stu-id="de1bb-113">In this section</span></span>

- <span data-ttu-id="de1bb-114">[Introducción al desarrollo de un proveedor de Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md): proporciona información general sobre el OSC, incluidos los siguientes: cómo un proveedor de OSC puede ser útil, pasos rápidos para aprender a desarrollar un proveedor, requisitos técnicos, procedimientos recomendados para desarrollar un proveedor, y cuáles son las novedades en esta versión.</span><span class="sxs-lookup"><span data-stu-id="de1bb-114">[Getting Started with Developing an Outlook Social Connector Provider](getting-started-with-developing-an-outlook-social-connector-provider.md): Provides an overview of the OSC, including the following: how an OSC provider can be useful, quick steps for learning to develop a provider, technical requirements, best practices for developing a provider, and what's new in this release.</span></span>
    
- <span data-ttu-id="de1bb-115">[Plantillas de ejemplo de OSC](osc-sample-templates.md): describe varias plantillas de Visual Studio para desarrollar un proveedor.</span><span class="sxs-lookup"><span data-stu-id="de1bb-115">[OSC Sample Templates](osc-sample-templates.md): Describes several Visual Studio templates for developing a provider.</span></span>
    
- <span data-ttu-id="de1bb-116">[Secuencias de llamada típicas OSC](osc-typical-calling-sequences.md): describe algunas secuencias de llamada típicas por el OSC de miembros de las interfaces de extensibilidad de proveedor OSC.</span><span class="sxs-lookup"><span data-stu-id="de1bb-116">[OSC Typical Calling Sequences](osc-typical-calling-sequences.md): Describes a few typical calling sequences by the OSC of members in the OSC provider extensibility interfaces.</span></span> <span data-ttu-id="de1bb-117">Esto debe permiten comprender mejor cómo implementar estas interfaces.</span><span class="sxs-lookup"><span data-stu-id="de1bb-117">This should enable you to better understand how to implement these interfaces.</span></span>
    
- <span data-ttu-id="de1bb-118">[Desarrollar un proveedor con el esquema XML de OSC](developing-a-provider-with-the-osc-xml-schema.md): describe cómo las interfaces de extensibilidad de proveedor OSC y el esquema XML de OSC están diseñados para admitir un proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="de1bb-118">[Developing a Provider with the OSC XML Schema](developing-a-provider-with-the-osc-xml-schema.md): Describes how the OSC provider extensibility interfaces and OSC XML schema are designed to support an OSC provider.</span></span>
    
- <span data-ttu-id="de1bb-119">[Depurar un proveedor](debugging-a-provider.md): sugiere varias maneras para ayudar a depurar un proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="de1bb-119">[Debugging a Provider](debugging-a-provider.md): Suggests a few ways to help debug an OSC provider.</span></span>
    
- <span data-ttu-id="de1bb-120">[Implementación de un proveedor](deploying-a-provider.md): se describen los requisitos de registro para un proveedor de OSC y proporciona una lista de comprobación para la instalación de un proveedor.</span><span class="sxs-lookup"><span data-stu-id="de1bb-120">[Deploying a Provider](deploying-a-provider.md): Describes registration requirements for an OSC provider, and provides a checklist for installing a provider.</span></span>
    
- <span data-ttu-id="de1bb-121">[Preparativos para liberar un proveedor de OSC](getting-ready-to-release-an-osc-provider.md): sugiere las pruebas que se puede hacer antes de liberar un proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="de1bb-121">[Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md): Suggests tests you can do before releasing an OSC provider.</span></span>
    
- <span data-ttu-id="de1bb-122">[Referencia del proveedor de Outlook Social Connector](outlook-social-connector-provider-reference-0.md): referencia de proporciona información para las interfaces de extensibilidad de proveedor OSC y esquema XML de OSC y las listas de posibles códigos de error.</span><span class="sxs-lookup"><span data-stu-id="de1bb-122">[Outlook Social Connector Provider Reference](outlook-social-connector-provider-reference-0.md): Provides reference information for the OSC provider extensibility interfaces and OSC XML schema, and lists possible error codes.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="de1bb-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="de1bb-123">See also</span></span>

- [<span data-ttu-id="de1bb-124">Aviso de copyright de la referencia del proveedor de Outlook Social Connector de 2013</span><span class="sxs-lookup"><span data-stu-id="de1bb-124">Outlook Social Connector 2013 provider reference copyright notice</span></span>](outlook-social-connector-2013-provider-reference-copyright-notice.md) 
- [<span data-ttu-id="de1bb-125">Convenciones de documentos</span><span class="sxs-lookup"><span data-stu-id="de1bb-125">Document Conventions</span></span>](http://msdn.microsoft.com/en-us/office/aa905365.aspx)   
- [<span data-ttu-id="de1bb-126">Accesibilidad en productos de Microsoft</span><span class="sxs-lookup"><span data-stu-id="de1bb-126">Accessibility in Microsoft Products</span></span>](http://www.microsoft.com/enable/products/default.aspx)  
- [<span data-ttu-id="de1bb-127">Aviso de privacidad en línea de Microsoft</span><span class="sxs-lookup"><span data-stu-id="de1bb-127">Microsoft Online Privacy Notice</span></span>](https://privacy.microsoft.com/en-us/privacystatement)
    

