---
title: Programación y arquitectura de Project Server 2013
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- architecture
- platform
- Project
- Project architecture
- Project programmability
- Project Server architecture
- Project Server programmability
keywords:
- project 2013, arquitectura y programación,Programación, Project Server,Project 2013, ventajas para EPM,Architecture y Project Server
localization_priority: Normal
ms.assetid: 9ea3b3c1-fb90-454a-b8e6-abc44fca663d
description: Los artículos de esta sección describen la arquitectura general de la solución Enterprise Project Management (EPM), que combina Project Professional 2013, Project Server 2013, Project Web App y SharePoint Server 2013.
ms.openlocfilehash: 44cd5a32b8d3de421ffe3b2d9bf0137146bc4c4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413790"
---
# <a name="project-server-2013-architecture-and-programmability"></a><span data-ttu-id="de953-104">Programación y arquitectura de Project Server 2013</span><span class="sxs-lookup"><span data-stu-id="de953-104">Project Server 2013 architecture and programmability</span></span>

<span data-ttu-id="de953-105">Los artículos de esta sección describen la arquitectura general de la solución Enterprise Project Management (EPM), que combina Project Professional 2013, Project Server 2013, Project Web App y SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="de953-105">The articles in this section describe the overall architecture of the Enterprise Project Management (EPM) solution, which combines Project Professional 2013, Project Server 2013, Project Web App, and SharePoint Server 2013.</span></span>
  
<span data-ttu-id="de953-106">Project Server 2013 se creó con .NET Framework 4 y es la tercera versión principal de Project Server que proporciona una verdadera arquitectura de varios mundos.</span><span class="sxs-lookup"><span data-stu-id="de953-106">Project Server 2013 is built with the .NET Framework 4 and is the third major release of Project Server to provide a true multitier architecture.</span></span> <span data-ttu-id="de953-107">Para el acceso a la nube, Project Server 2013 implementa un modelo de objetos de cliente (CSOM) y un servicio OData para los informes que se pueden usar en aplicaciones web, aplicaciones móviles y aplicaciones de Silverlight.</span><span class="sxs-lookup"><span data-stu-id="de953-107">For cloud access, Project Server 2013 implements a client-side object model (CSOM) and an OData service for reporting that can be used in web applications, mobile applications, and Silverlight applications.</span></span> <span data-ttu-id="de953-108">Para aplicaciones locales, los clientes pueden usar el CSOM o bien los servicios de Interfaz de Project Server (PSI).</span><span class="sxs-lookup"><span data-stu-id="de953-108">For applications on-premises, clients can use either the CSOM or the Project Server Interface (PSI) services.</span></span> 
  
## <a name="introduction-to-project-server-architecture"></a><span data-ttu-id="de953-109">Introducción a la arquitectura de Project Server</span><span class="sxs-lookup"><span data-stu-id="de953-109">Introduction to Project Server architecture</span></span>

<span data-ttu-id="de953-110">En los temas de esta sección se describe la arquitectura general de la solución Enterprise Project Management (EPM), que combina Project Professional 2013, Project Server 2013, Project Web App y SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="de953-110">The topics in this section describe the overall architecture of the Enterprise Project Management (EPM) solution, which combines Project Professional 2013, Project Server 2013, Project Web App, and SharePoint Server 2013.</span></span>
  
<span data-ttu-id="de953-111">Para obtener acceso mediante programación a Project Server, debe usar el CSOM o los servicios de PSI con la interfaz de Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="de953-111">For programmatic access to Project Server, you should use either the CSOM or the PSI services with the Windows Communication Foundation (WCF) interface.</span></span> <span data-ttu-id="de953-112">La interfaz del servicio web ASMX de PSI está en desuso en Project Server 2013, pero sigue funcionando.</span><span class="sxs-lookup"><span data-stu-id="de953-112">The ASMX web service interface of the PSI is deprecated in Project Server 2013, but still works.</span></span> <span data-ttu-id="de953-113">La PSI permite el acceso eficiente utilizando conjuntos de datos y puede crear controladores para eventos de servidor.</span><span class="sxs-lookup"><span data-stu-id="de953-113">The PSI enables efficient access by using datasets and you can create handlers for server-side events.</span></span> <span data-ttu-id="de953-114">El CSOM utiliza la PSI para acceder a la capa de objeto de negocios de Project Server.</span><span class="sxs-lookup"><span data-stu-id="de953-114">The CSOM itself uses the PSI to access the Project Server business object layer.</span></span> <span data-ttu-id="de953-115">En lugar de cuatro bases de datos de Project Server, Project Server 2013 usa una sola base de datos en el nivel de acceso a datos.</span><span class="sxs-lookup"><span data-stu-id="de953-115">Instead of four Project Server databases, Project Server 2013 uses a single database in the data access layer.</span></span>
  
<span data-ttu-id="de953-116">Project Server 2013 se integra profundamente con SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="de953-116">Project Server 2013 integrates deeply with SharePoint Server 2013.</span></span> <span data-ttu-id="de953-117">El Servicio de aplicación de Project puede asociarse con otros grupos de sitio de SharePoint de la granja de servidores.</span><span class="sxs-lookup"><span data-stu-id="de953-117">The Project Application Service can be associated with other SharePoint site collections in the farm.</span></span> <span data-ttu-id="de953-118">Project Server puede funcionar con las listas de tareas de SharePoint en el grupo de sitios y elaborar informes sobre ellas y tambi{en puede obtener control pleno cuando Project Server importa y administra las listas de tareas como proyectos empresariales.</span><span class="sxs-lookup"><span data-stu-id="de953-118">Project Server can operate with and report on SharePoint task lists in the site collection, and can also get full control where Project Server imports and manages the task lists as enterprise projects.</span></span> <span data-ttu-id="de953-119">Project Server también usa la versión 4 de Windows Workflow Foundation (WF4) y agrega actividades de flujo de trabajo para soluciones de administración de demanda.</span><span class="sxs-lookup"><span data-stu-id="de953-119">Project Server also uses version 4 of the Windows Workflow Foundation (WF4) and adds workflow activities for Demand Management solutions.</span></span>
  
<span data-ttu-id="de953-120">Para obtener una explicación de las muchas características nuevas que Project 2013 proporciona a los desarrolladores y de las características que están en desuso, vea Actualizaciones para desarrolladores en [Project 2013.](updates-for-developers-in-project-2013.md)</span><span class="sxs-lookup"><span data-stu-id="de953-120">For a discussion of the many new features that Project 2013 provides for developers, and of the features that are deprecated, see [Updates for developers in Project 2013](updates-for-developers-in-project-2013.md).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="de953-121">En esta sección</span><span class="sxs-lookup"><span data-stu-id="de953-121">In this section</span></span>

<span data-ttu-id="de953-122">[La arquitectura de Project Server 2013](project-server-2013-architecture.md) describe las partes principales de la plataforma de Project 2013, incluidos los clientes y servidores.</span><span class="sxs-lookup"><span data-stu-id="de953-122">[Project Server 2013 architecture](project-server-2013-architecture.md) describes the major parts of the Project 2013 platform, including the clients and servers.</span></span> 
  
<span data-ttu-id="de953-123">[La programación](project-server-programmability.md) de Project Server analiza las principales características de extensibilidad de Project Server 2013, la personalización de Project Web App y la actualización de aplicaciones creadas para versiones anteriores de Project Server.</span><span class="sxs-lookup"><span data-stu-id="de953-123">[Project Server programmability](project-server-programmability.md) discusses the main extensibility features of Project Server 2013, customization of Project Web App, and upgrading applications that are built for previous Project Server versions.</span></span> 
  
<span data-ttu-id="de953-124">[What the PSI does and does not do](what-the-psi-does-and-does-not-do.md) describe escenarios en los que la PSI puede utilizarse y menciona cosas que la PSI no puede realizar.</span><span class="sxs-lookup"><span data-stu-id="de953-124">[What the PSI does and does not do](what-the-psi-does-and-does-not-do.md) describes scenarios where the PSI can be used and lists things that the PSI cannot do.</span></span> 
  
<span data-ttu-id="de953-125">[What the CSOM does and does not do](what-the-csom-does-and-does-not-do.md) describe escenarios en los que el CSOM puede utilizarse y menciona cosas que el CSOM no puede realizar.</span><span class="sxs-lookup"><span data-stu-id="de953-125">[What the CSOM does and does not do](what-the-csom-does-and-does-not-do.md) describes scenarios where the CSOM can be used and lists things that the CSOM cannot do.</span></span> 
  
### <a name="topics-not-covered"></a><span data-ttu-id="de953-126">Temas no abordados</span><span class="sxs-lookup"><span data-stu-id="de953-126">Topics not covered</span></span>

<span data-ttu-id="de953-127">Los artículos  de la sección Arquitectura y programación no documentan las características de los clientes de escritorio de Project (Project Standard 2013 y Project Professional 2013) ni Project Web App.</span><span class="sxs-lookup"><span data-stu-id="de953-127">The articles in the  *Architecture and programmability*  section do not document features of the Project desktop clients (Project Standard 2013 and Project Professional 2013) or Project Web App.</span></span> 
  
<span data-ttu-id="de953-128">La ayuda de Visual Basic para aplicaciones (VBA) está disponible en el editor de Visual Basic dentro de Project Standard y Project Professional.</span><span class="sxs-lookup"><span data-stu-id="de953-128">Visual Basic for Applications (VBA) help is available in the Visual Basic editor within Project Standard and Project Professional.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="de953-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="de953-129">See also</span></span>
<span data-ttu-id="de953-130"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="de953-130"><a name="bk_addresources"> </a></span></span>

- [<span data-ttu-id="de953-131">Actualizaciones para desarrolladores en Project 2013</span><span class="sxs-lookup"><span data-stu-id="de953-131">Updates for developers in Project 2013</span></span>](updates-for-developers-in-project-2013.md)
    
- [<span data-ttu-id="de953-132">Introducción al desarrollo de flujos de trabajo de Project Server</span><span class="sxs-lookup"><span data-stu-id="de953-132">Getting started developing Project Server workflows</span></span>](getting-started-developing-project-server-workflows.md)
    

