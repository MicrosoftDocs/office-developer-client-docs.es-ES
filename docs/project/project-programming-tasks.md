---
title: Tareas de programación de Project
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: ac5544e7-ff7a-4af5-ac1b-33a49bc6be0d
description: En esta sección se incluye algún modo-toarticles que muestra cómo usar la biblioteca de JavaScript para el modelo de objetos de cliente (CSOM) y realizar otras tareas de programación para Project Server 2013 y Project Online. Tareas de programación ejemplos de creación de una aplicación hospedada en SharePoint Project Server, la creación de flujos de trabajo para la administración de propuestas; programación de aplicaciones de Project Server con Windows Communication Foundation (WCF); personalización de la cinta de Project Web App; creación de elementos Web de Project Server; creación de controladores de eventos de Project Server y receptores de eventos remotos; y actualización de los campos personalizados y la creación de sitios de proyectos para Project Online de forma masiva.
ms.openlocfilehash: 385b9fa53c2c7faf2a218816bf4d3f0499b9ecd1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388612"
---
# <a name="project-programming-tasks"></a><span data-ttu-id="1fd2e-104">Tareas de programación de Project</span><span class="sxs-lookup"><span data-stu-id="1fd2e-104">Project programming tasks</span></span>

<span data-ttu-id="1fd2e-105">Esta sección incluyen algunos artículos de "procedimientos" que se muestra cómo usar la biblioteca de JavaScript para el modelo de objetos de cliente (CSOM) y realizar otras tareas de programación para Project Server 2013 y Project Online.</span><span class="sxs-lookup"><span data-stu-id="1fd2e-105">This section includes some "how-to" articles that show how to use the JavaScript library for the client-side object model (CSOM), and perform other programming tasks for Project Server 2013 and Project Online.</span></span> <span data-ttu-id="1fd2e-106">Tareas de programación ejemplos de creación de una aplicación hospedada en SharePoint Project Server, la creación de flujos de trabajo para la administración de propuestas; programación de aplicaciones de Project Server con Windows Communication Foundation (WCF); personalización de la cinta de Project Web App; creación de elementos Web de Project Server; creación de controladores de eventos de Project Server y receptores de eventos remotos; y actualización de los campos personalizados y la creación de sitios de proyectos para Project Online de forma masiva.</span><span class="sxs-lookup"><span data-stu-id="1fd2e-106">Examples of programming tasks include creating a SharePoint-hosted Project Server app, creating workflows for demand management; programming Project Server applications with the Windows Communication Foundation (WCF); customizing the Project Web App ribbon; creating Project Server Web Parts; creating Project Server event handlers and remote event receivers; and bulk updating custom fields and creating project sites for Project Online.</span></span>
  
> [!NOTE]
> <span data-ttu-id="1fd2e-107">Para obtener información acerca de la programación con el control de cuadrícula JS, consulte [Control de cuadrícula JS](https://msdn.microsoft.com/library/ee535898%28office.14%29.aspx) en la referencia del programador de SharePoint 2010.</span><span class="sxs-lookup"><span data-stu-id="1fd2e-107">For information about programming with the JS Grid control, see [JS Grid Control](https://msdn.microsoft.com/library/ee535898%28office.14%29.aspx) in the SharePoint 2010 developer reference.</span></span> <span data-ttu-id="1fd2e-108">Para la referencia de código administrado, vea [Microsoft.SharePoint.JSGrid Namespace](https://msdn.microsoft.com/library/microsoft.sharepoint.jsgrid%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="1fd2e-108">For the managed code reference, see [Microsoft.SharePoint.JSGrid Namespace](https://msdn.microsoft.com/library/microsoft.sharepoint.jsgrid%28Office.15%29.aspx).</span></span> <span data-ttu-id="1fd2e-109">Para los controles web de control de cuadrícula JS, vea la [clase JSGrid](https://msdn.microsoft.com/library/microsoft.sharepoint.webcontrols.jsgrid%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="1fd2e-109">For the JS Grid control web controls, see [JSGrid class](https://msdn.microsoft.com/library/microsoft.sharepoint.webcontrols.jsgrid%28Office.15%29.aspx).</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="1fd2e-110">En esta sección</span><span class="sxs-lookup"><span data-stu-id="1fd2e-110">In this section</span></span>

[<span data-ttu-id="1fd2e-111">Empezar a desarrollar flujos de trabajo de Project Server</span><span class="sxs-lookup"><span data-stu-id="1fd2e-111">Getting started developing Project Server workflows</span></span>](getting-started-developing-project-server-workflows.md)
  
[<span data-ttu-id="1fd2e-112">Actualización en masa de los campos personalizados y crear sitios de proyecto desde un flujo de trabajo en Project Online</span><span class="sxs-lookup"><span data-stu-id="1fd2e-112">Bulk update custom fields and create project sites from a workflow in Project Online</span></span>](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)
  
[<span data-ttu-id="1fd2e-113">Crear, recuperar, actualizar y eliminar proyectos mediante el modelo de objetos de JavaScript de Project Server</span><span class="sxs-lookup"><span data-stu-id="1fd2e-113">Create, retrieve, update, and delete projects by using the Project Server JavaScript object model</span></span>](create-retrieve-update-delete-projects-using-project-server-javascript.md)
  
<span data-ttu-id="1fd2e-114">[Crear un servidor de Project Server hospedada en SharePoint complemento](create-a-sharepoint-hosted-project-server-add-in.md) : incluye una sección sobre cómo modificar la cinta de opciones de Project Web App</span><span class="sxs-lookup"><span data-stu-id="1fd2e-114">[Create a SharePoint-hosted Project Server add-in](create-a-sharepoint-hosted-project-server-add-in.md) : includes a section on how to modify the Project Web App ribbon</span></span> 
  
## <a name="reference"></a><span data-ttu-id="1fd2e-115">Referencia</span><span class="sxs-lookup"><span data-stu-id="1fd2e-115">Reference</span></span>

[<span data-ttu-id="1fd2e-116">Información general de referencia PSI de Project</span><span class="sxs-lookup"><span data-stu-id="1fd2e-116">Project PSI reference overview</span></span>](project-psi-reference-overview.md)
  
## <a name="see-also"></a><span data-ttu-id="1fd2e-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="1fd2e-117">See also</span></span>



[<span data-ttu-id="1fd2e-118">Modelo de objetos de cliente (COM) de Project 2013</span><span class="sxs-lookup"><span data-stu-id="1fd2e-118">Client-side object model (CSOM) for Project 2013</span></span>](client-side-object-model-csom-for-project-2013.md)

