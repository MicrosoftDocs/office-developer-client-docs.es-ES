---
title: Crear plantillas de formulario con código mediante el modelo de objetos de InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, creating,object models [InfoPath 2003], creating managed code form templates for InfoPath 2007,form templates [InfoPath 2007], creating InfoPath 2003-compatible
localization_priority: Normal
ms.assetid: e0513178-ddcb-4086-ab19-1bc80cf114cc
description: En esta sección se explica el código de limpieza e inicialización, cómo agregar controladores de eventos, cómo depurar e implementar plantillas de formulario de InfoPath que utilizan el modelo de objetos compatible con InfoPath 2003, la compatibilidad con los subprocesos y cómo trabajar con Microsoft XML Core Services (MSXML) desde soluciones con código administrado de InfoPath.
ms.openlocfilehash: 5069636dde87eb473a2b8bef4b58a6006d557085
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410535"
---
# <a name="creating-form-templates-using-the-infopath-2003-object-model"></a><span data-ttu-id="9a81a-104">Crear plantillas de formulario con código mediante el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="9a81a-104">Creating Form Templates Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="9a81a-105">En esta sección se explica el código de limpieza e inicialización, cómo agregar controladores de eventos, cómo depurar e implementar plantillas de formulario de InfoPath que utilizan el modelo de objetos compatible con InfoPath 2003, la compatibilidad con los subprocesos y cómo trabajar con Microsoft XML Core Services (MSXML) desde soluciones con código administrado de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="9a81a-105">This section discusses initialization and clean-up code, how to add event handlers, how to debug and deploy InfoPath form templates that use the InfoPath 2003-compatible object model, threading support, and working with Microsoft XML Core Services (MSXML) from InfoPath managed-code solutions.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="9a81a-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="9a81a-106">In this section</span></span>

[<span data-ttu-id="9a81a-107">Utilizar código de limpieza e inicialización mediante el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="9a81a-107">Initialization and Clean-up Code Using InfoPath 2003 Object Model</span></span>](initialization-and-clean-up-code-using-infopath-2003-object-model.md)
  
> <span data-ttu-id="9a81a-108">Describe cómo escribir código de limpieza e inicialización en los métodos _Startup y _Shutdown del proyecto.</span><span class="sxs-lookup"><span data-stu-id="9a81a-108">Discusses how to write initialization and clean-up code in the _Startup and _Shutdown methods of your project.</span></span>
    
[<span data-ttu-id="9a81a-109">Agregar un controlador de eventos mediante el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="9a81a-109">Add an Event Handler Using the InfoPath 2003 Object Model</span></span>](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="9a81a-110">Describe cómo agregar controladores de eventos y los atributos que se aplican para identificar controladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="9a81a-110">Discusses how to add event handlers and the attributes that are applied to identify event handlers.</span></span>
    
[<span data-ttu-id="9a81a-111">Depurar proyectos de InfoPath con el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="9a81a-111">Debug InfoPath Projects Using the InfoPath 2003 Object Model</span></span>](how-to-debug-infopath-projects-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="9a81a-112">Describe cómo depurar proyectos de código administrado de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="9a81a-112">Discusses how to debug InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="9a81a-113">Implementar plantillas de formulario de InfoPath con código</span><span class="sxs-lookup"><span data-stu-id="9a81a-113">Deploy InfoPath Form Templates with Code</span></span>](how-to-deploy-infopath-form-templates-with-code.md)
  
> <span data-ttu-id="9a81a-114">Describe cómo implementar proyectos de código administrado de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="9a81a-114">Discusses how to deploy InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="9a81a-115">Compatibilidad con el subprocesamiento en los proyectos de InfoPath mediante el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="9a81a-115">Threading Support in InfoPath Projects Using the InfoPath 2003 Object Model</span></span>](threading-support-in-infopath-projects-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="9a81a-116">Describe la compatibilidad con el subprocesamiento en los proyectos de código administrado de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="9a81a-116">Discusses threading support in InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="9a81a-117">Trabajar con MSXML y System.Xml con el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="9a81a-117">Working with MSXML and System.Xml Using the InfoPath 2003 Object Model</span></span>](working-with-msxml-and-system-xml-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="9a81a-118">Describe cómo trabajar con código MSXML y System.Xml en los proyectos de código administrado de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="9a81a-118">Discusses how to work with MSXML and System.Xml code in InfoPath managed-code projects.</span></span>
    

