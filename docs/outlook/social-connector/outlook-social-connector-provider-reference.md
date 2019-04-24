---
title: Referencia de proveedores de Outlook Social Connector
manager: soliver
ms.date: 04/04/2016
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13661393-adf6-4870-86c4-303262317675
description: Outlook Social Connector 2013 proporciona un centro de comunicación para las comunicaciones personales y profesionales.
ms.openlocfilehash: e570fe69cbbe0e8d472e712fb3b8592c97fe43c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359839"
---
# <a name="outlook-social-connector-provider-reference"></a><span data-ttu-id="8cf16-103">Referencia de proveedores de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="8cf16-103">Outlook Social Connector provider reference</span></span>

<span data-ttu-id="8cf16-104">Outlook Social Connector 2013 proporciona un centro de comunicación para las comunicaciones personales y profesionales.</span><span class="sxs-lookup"><span data-stu-id="8cf16-104">The Outlook Social Connector 2013 provides a communication hub for personal and professional communications.</span></span> <span data-ttu-id="8cf16-105">Outlook Social Connector (OSC) funciona con SharePoint Server, SharePoint Workspace, cliente de Lync y todas las aplicaciones cliente de Office que admiten la información de presencia y la tarjeta de contacto admite el OSC.</span><span class="sxs-lookup"><span data-stu-id="8cf16-105">The Outlook Social Connector (OSC) works with SharePoint Server, SharePoint Workspace, Lync client, and all Office client applications that support presence information and the Contact Card support the OSC.</span></span> 

<span data-ttu-id="8cf16-106">En Outlook en particular, simplemente seleccionando un elemento de Outlook como un correo electrónico o una convocatoria de reunión y haciendo clic en el remitente o un destinatario en ese elemento, sin salir de Outlook, los usuarios pueden ver en el panel de personas actividades, fotos y actualizaciones de estado de esta persona en su redes sociales favoritas.</span><span class="sxs-lookup"><span data-stu-id="8cf16-106">In Outlook in particular, just by selecting an Outlook item such as an email or meeting request and clicking the sender or a recipient in that item, without leaving Outlook, users can see in the People Pane activities, photos, and status updates of this person on their favorite social networks.</span></span> <span data-ttu-id="8cf16-107">Los usuarios pueden ver fácilmente todos los correos electrónicos, datos adjuntos y reuniones de Outlook recibidas de esta persona.</span><span class="sxs-lookup"><span data-stu-id="8cf16-107">Users can conveniently see all the Outlook emails, attachments, and meetings received from this person.</span></span> <span data-ttu-id="8cf16-108">En un entorno de organización, los usuarios de un sitio de SharePoint también pueden ver en el panel de personas actualizaciones de documentos y otras actividades de sitio de esta persona en el sitio de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="8cf16-108">In an organizational environment, users on a SharePoint site can also see in the People Pane document updates and other site activities of this person on the SharePoint site.</span></span>
  
<span data-ttu-id="8cf16-109">Una red social puede desarrollar un proveedor para que el OSC sincronice y exponga las actualizaciones de red social en servidores y aplicaciones compatibles.</span><span class="sxs-lookup"><span data-stu-id="8cf16-109">A social network can develop a provider for the OSC to synchronize and surface social network updates in supporting servers and applications.</span></span> <span data-ttu-id="8cf16-110">Las redes sociales más populares, como LinkedIn, Facebook y Windows Live, ofrecen proveedores para el OSC.</span><span class="sxs-lookup"><span data-stu-id="8cf16-110">Popular social networks such as LinkedIn, Facebook, and Windows Live are offering providers for the OSC.</span></span> 
  
<span data-ttu-id="8cf16-111">La referencia del proveedor de Outlook Social Connector 2013 describe cómo desarrollar un proveedor de OSC mediante la extensibilidad de proveedores de OSC.</span><span class="sxs-lookup"><span data-stu-id="8cf16-111">The Outlook Social Connector 2013 Provider Reference describes how to develop an OSC provider using OSC provider extensibility.</span></span> 
  
<span data-ttu-id="8cf16-112">Si no tiene experiencia en el desarrollo de soluciones para Outlook, consulte [Seleccionar una API o tecnología para desarrollar soluciones de Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) para identificar las API y tecnologías más adecuadas para sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="8cf16-112">If you are new to developing solutions for Outlook, see [Selecting an API or technology for developing solutions for Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) to identify the APIs and technologies that are most appropriate for your needs.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="8cf16-113">En esta sección</span><span class="sxs-lookup"><span data-stu-id="8cf16-113">In this section</span></span>

- <span data-ttu-id="8cf16-114">Introducción al [desarrollo de un proveedor de Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md): proporciona información general sobre el OSC, incluido lo siguiente: Cómo puede resultar útil un proveedor OSC, pasos rápidos para aprender a desarrollar un proveedor, requisitos técnicos, procedimientos recomendados para desarrollar un proveedor y lo nuevo en esta versión.</span><span class="sxs-lookup"><span data-stu-id="8cf16-114">[Getting Started with Developing an Outlook Social Connector Provider](getting-started-with-developing-an-outlook-social-connector-provider.md): Provides an overview of the OSC, including the following: how an OSC provider can be useful, quick steps for learning to develop a provider, technical requirements, best practices for developing a provider, and what's new in this release.</span></span>
    
- <span data-ttu-id="8cf16-115">[Plantillas de ejemplo OSC](osc-sample-templates.md): describe varias plantillas de Visual Studio para desarrollar un proveedor.</span><span class="sxs-lookup"><span data-stu-id="8cf16-115">[OSC Sample Templates](osc-sample-templates.md): Describes several Visual Studio templates for developing a provider.</span></span>
    
- <span data-ttu-id="8cf16-116">Las [secuencias de llamada típicas de OSC](osc-typical-calling-sequences.md): describe algunas secuencias de llamadas típicas por el OSC de miembros en las interfaces de extensibilidad del proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="8cf16-116">[OSC Typical Calling Sequences](osc-typical-calling-sequences.md): Describes a few typical calling sequences by the OSC of members in the OSC provider extensibility interfaces.</span></span> <span data-ttu-id="8cf16-117">Esto le permitirá comprender mejor cómo implementar estas interfaces.</span><span class="sxs-lookup"><span data-stu-id="8cf16-117">This should enable you to better understand how to implement these interfaces.</span></span>
    
- <span data-ttu-id="8cf16-118">[Desarrollar un proveedor con el esquema XML de OSC](developing-a-provider-with-the-osc-xml-schema.md): describe cómo las interfaces de extensibilidad del proveedor OSC y el esquema XML de OSC están diseñados para admitir un proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="8cf16-118">[Developing a Provider with the OSC XML Schema](developing-a-provider-with-the-osc-xml-schema.md): Describes how the OSC provider extensibility interfaces and OSC XML schema are designed to support an OSC provider.</span></span>
    
- <span data-ttu-id="8cf16-119">[Depurar un proveedor](debugging-a-provider.md): sugiere varias maneras de ayudar a depurar un proveedor OSC.</span><span class="sxs-lookup"><span data-stu-id="8cf16-119">[Debugging a Provider](debugging-a-provider.md): Suggests a few ways to help debug an OSC provider.</span></span>
    
- <span data-ttu-id="8cf16-120">[Implementación de un proveedor](deploying-a-provider.md): describe los requisitos de registro de un proveedor de OSC y proporciona una lista de comprobación para instalar un proveedor.</span><span class="sxs-lookup"><span data-stu-id="8cf16-120">[Deploying a Provider](deploying-a-provider.md): Describes registration requirements for an OSC provider, and provides a checklist for installing a provider.</span></span>
    
- <span data-ttu-id="8cf16-121">[Preparación para la publicación de un proveedor OSC](getting-ready-to-release-an-osc-provider.md): sugiere pruebas que puede hacer antes de liberar un proveedor OSC.</span><span class="sxs-lookup"><span data-stu-id="8cf16-121">[Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md): Suggests tests you can do before releasing an OSC provider.</span></span>
    
- <span data-ttu-id="8cf16-122">[Referencia del proveedor de Outlook Social Connector](outlook-social-connector-provider-reference-0.md): proporciona información de referencia para las interfaces de extensibilidad del proveedor OSC y el esquema XML de OSC, y enumera los códigos de error posibles.</span><span class="sxs-lookup"><span data-stu-id="8cf16-122">[Outlook Social Connector Provider Reference](outlook-social-connector-provider-reference-0.md): Provides reference information for the OSC provider extensibility interfaces and OSC XML schema, and lists possible error codes.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8cf16-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="8cf16-123">See also</span></span>

- [<span data-ttu-id="8cf16-124">Aviso de copyright de referencia del proveedor de Outlook Social Connector 2013</span><span class="sxs-lookup"><span data-stu-id="8cf16-124">Outlook Social Connector 2013 provider reference copyright notice</span></span>](outlook-social-connector-2013-provider-reference-copyright-notice.md) 
- [<span data-ttu-id="8cf16-125">Convenciones del documento</span><span class="sxs-lookup"><span data-stu-id="8cf16-125">Document Conventions</span></span>](https://msdn.microsoft.com/office/aa905365.aspx)   
- [<span data-ttu-id="8cf16-126">Accesibilidad en los productos de Microsoft</span><span class="sxs-lookup"><span data-stu-id="8cf16-126">Accessibility in Microsoft Products</span></span>](https://www.microsoft.com/enable/products/default.aspx)  
- [<span data-ttu-id="8cf16-127">Aviso de privacidad de Microsoft online</span><span class="sxs-lookup"><span data-stu-id="8cf16-127">Microsoft Online Privacy Notice</span></span>](https://privacy.microsoft.com/en-us/privacystatement)
    

