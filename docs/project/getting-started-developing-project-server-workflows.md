---
title: Empezar a desarrollar flujos de trabajo de Project Server
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 735bbb04-a8c1-46c0-a346-42050f0ac9b1
description: Propuestas en Project Server 2013 los procesos de administración incluyen los flujos de trabajo que le ayudan a administrar las propuestas de proyecto y análisis de cartera. En esta sección se incluye artículos que muestran cómo crear flujos de trabajo de Project Server.
ms.openlocfilehash: 0a09022e63528f50ee4f0c8bd69bd6c34c5d8753
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384097"
---
# <a name="getting-started-developing-project-server-workflows"></a><span data-ttu-id="d4e7b-104">Empezar a desarrollar flujos de trabajo de Project Server</span><span class="sxs-lookup"><span data-stu-id="d4e7b-104">Getting started developing Project Server workflows</span></span>

<span data-ttu-id="d4e7b-105">Propuestas en Project Server 2013 los procesos de administración incluyen los flujos de trabajo que le ayudan a administrar las propuestas de proyecto y análisis de cartera.</span><span class="sxs-lookup"><span data-stu-id="d4e7b-105">Demand management processes in Project Server 2013 include workflows that help you manage project proposals and portfolio analyses.</span></span> <span data-ttu-id="d4e7b-106">En esta sección se incluye artículos que muestran cómo crear flujos de trabajo de Project Server.</span><span class="sxs-lookup"><span data-stu-id="d4e7b-106">This section includes articles that show how to create workflows for Project Server.</span></span>
  
<span data-ttu-id="d4e7b-107">Flujos de trabajo de Project Server 2013 usan la plataforma de flujo de trabajo de SharePoint Server 2013, que se basa en la versión 4 de Windows Workflow Foundation (WF4).</span><span class="sxs-lookup"><span data-stu-id="d4e7b-107">Project Server 2013 workflows use the SharePoint Server 2013 workflow platform, which is built on version 4 of Windows Workflow Foundation (WF4).</span></span> <span data-ttu-id="d4e7b-108">Flujos de trabajo basados en WF4 son declarativos, lo que significa que la herramienta de diseño de flujo de trabajo guarda las etapas de flujo de trabajo, acciones, condiciones y otros elementos en el código XAML, que se interpreta en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="d4e7b-108">WF4-based workflows are declarative, which means that the workflow design tool saves workflow stages, actions, conditions, and other elements to XAML code, which is interpreted at run-time.</span></span> <span data-ttu-id="d4e7b-109">Puede usar SharePoint Designer 2013 o Visual Studio 2012 para crear flujos de trabajo declarativos.</span><span class="sxs-lookup"><span data-stu-id="d4e7b-109">You can use either SharePoint Designer 2013 or Visual Studio 2012 to create declarative workflows.</span></span> <span data-ttu-id="d4e7b-110">Un flujo de trabajo requiere el motor de ejecución 1.0 de cliente del Administrador de flujo de trabajo, que puede estar en un servidor local para las soluciones locales o en un servidor remoto para soluciones de Project Online.</span><span class="sxs-lookup"><span data-stu-id="d4e7b-110">A workflow requires the Workflow Manager Client 1.0 execution engine, which can be on a local server for on-premises solutions or on a remote server for Project Online solutions.</span></span>
  
<span data-ttu-id="d4e7b-111">Puede usar SharePoint Designer 2013 para crear flujos de trabajo declarativos relativamente simples.</span><span class="sxs-lookup"><span data-stu-id="d4e7b-111">You can use SharePoint Designer 2013 to create relatively simple declarative workflows.</span></span> <span data-ttu-id="d4e7b-112">Para flujos de trabajo complejos y plantillas de flujo de trabajo que se pueden reutilizar, puede usar Visual Studio 2012 para desarrollar y depurar flujos de trabajo de Project Web App.</span><span class="sxs-lookup"><span data-stu-id="d4e7b-112">For complex workflows, and workflow templates that can be reused, you can use Visual Studio 2012 to develop and debug workflows for Project Web App.</span></span> <span data-ttu-id="d4e7b-113">Para obtener más información, vea [creación de flujos de trabajo de proyecto con Visual Studio 2012](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx).</span><span class="sxs-lookup"><span data-stu-id="d4e7b-113">For more information, see [Creating Project Workflows using Visual Studio 2012](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="d4e7b-114">Usar una instalación de prueba de Project Server, no es una instalación de producción, para desarrollar y probar los flujos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="d4e7b-114">Use a test installation of Project Server, not a production installation, to develop and test workflows.</span></span> <span data-ttu-id="d4e7b-115">Los flujos de trabajo que se ha desarrollado para versiones anteriores a la versión de Project Server 2013 deben probarse para la versión de lanzamiento y que tenga que se vuelve a crear y volver a implementar.</span><span class="sxs-lookup"><span data-stu-id="d4e7b-115">Workflows that are developed for pre-release versions of Project Server 2013 must be tested for the release version, and may have to be created again and redeployed.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="d4e7b-116">En esta sección</span><span class="sxs-lookup"><span data-stu-id="d4e7b-116">In this section</span></span>

[<span data-ttu-id="d4e7b-117">Crear un flujo de trabajo de Project Server para Administración de propuestas</span><span class="sxs-lookup"><span data-stu-id="d4e7b-117">Create a Project Server workflow for Demand Management</span></span>](create-a-project-server-workflow-for-demand-management.md)
  
## <a name="see-also"></a><span data-ttu-id="d4e7b-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4e7b-118">See also</span></span>



[<span data-ttu-id="d4e7b-119">Actualizar los campos personalizados de forma masiva y crear sitios de proyecto desde un flujo de trabajo de Project Online</span><span class="sxs-lookup"><span data-stu-id="d4e7b-119">Bulk update custom fields and create project sites from a Project Online workflow</span></span>](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)


[<span data-ttu-id="d4e7b-120">Desarrollo de flujos de trabajo en SharePoint Designer 2013 y Visio 2013</span><span class="sxs-lookup"><span data-stu-id="d4e7b-120">Workflow development in SharePoint Designer 2013 and Visio 2013</span></span>](https://msdn.microsoft.com/library/jj163272%28office.15%29.aspx)
  
[<span data-ttu-id="d4e7b-121">Novedades en flujos de trabajo para SharePoint 2013</span><span class="sxs-lookup"><span data-stu-id="d4e7b-121">What's new in workflows for SharePoint 2013</span></span>](https://msdn.microsoft.com/library/jj163177.aspx)
  
[<span data-ttu-id="d4e7b-122">Desarrollar de flujos de trabajo de SharePoint 2013 mediante Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d4e7b-122">Develop SharePoint 2013 workflows using Visual Studio</span></span>](https://msdn.microsoft.com/library/jj163199.aspx)
  
[<span data-ttu-id="d4e7b-123">Creación de flujos de trabajo de proyecto con Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="d4e7b-123">Creating Project Workflows using Visual Studio 2012</span></span>](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx)
  
[<span data-ttu-id="d4e7b-124">Windows Workflow Foundation</span><span class="sxs-lookup"><span data-stu-id="d4e7b-124">Windows Workflow Foundation</span></span>](https://msdn.microsoft.com/library/dd489441.aspx)
  
[<span data-ttu-id="d4e7b-125">Introducción para desarrolladores a Windows Workflow Foundation (WF) en .NET 4</span><span class="sxs-lookup"><span data-stu-id="d4e7b-125">A developer's introduction to Windows Workflow Foundation (WF) in .NET 4</span></span>](https://msdn.microsoft.com/library/ee342461.aspx)
  
[<span data-ttu-id="d4e7b-126">Guía para la administración de propuestas (notas del producto)</span><span class="sxs-lookup"><span data-stu-id="d4e7b-126">Hitchhiker's guide to demand management (white paper)</span></span>](https://msdn.microsoft.com/library/ff973112.aspx)

