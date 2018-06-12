---
title: Comprender el modelo de objetos de InfoPath y las tareas de programación más comunes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- examples [infopath 2007],InfoPath 2007, developer tasks,developer tasks [InfoPath 2007],InfoPath 2007, object models,object models [InfoPath 2007]
localization_priority: Normal
ms.assetid: a2c18b72-426b-4f63-8454-187e96d26199
description: En esta sección se ofrece información sobre tareas de desarrollo habituales cuando se desarrollan plantillas de formulario con código administrado de InfoPath.
ms.openlocfilehash: 9f0bbf36b2533b12ca3f31100c3abc21173d7c6b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815971"
---
# <a name="understanding-the-infopath-object-model-and-common-developer-tasks"></a><span data-ttu-id="7a5b5-104">Comprender el modelo de objetos de InfoPath y las tareas de programación más comunes</span><span class="sxs-lookup"><span data-stu-id="7a5b5-104">Understanding the InfoPath Object Model and Common Developer Tasks</span></span>

<span data-ttu-id="7a5b5-105">En esta sección se ofrece información sobre tareas de desarrollo habituales cuando se desarrollan plantillas de formulario con código administrado de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="7a5b5-105">This section provides information on common developer tasks when developing InfoPath managed code form templates.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="7a5b5-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="7a5b5-106">In this section</span></span>

[<span data-ttu-id="7a5b5-107">Datos de la aplicación de Access</span><span class="sxs-lookup"><span data-stu-id="7a5b5-107">Access Application Data</span></span>](how-to-access-application-data.md)
  
> <span data-ttu-id="7a5b5-108">Se ofrece información sobre el acceso a información acerca de la aplicación de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="7a5b5-108">Discusses how to access information about the InfoPath application.</span></span>
    
[<span data-ttu-id="7a5b5-109">Responder a eventos de formulario</span><span class="sxs-lookup"><span data-stu-id="7a5b5-109">Respond to Form Events</span></span>](how-to-respond-to-form-events.md)
  
> <span data-ttu-id="7a5b5-110">Trata de cómo crear controladores de eventos que respondan a los eventos que se producen mientras el usuario rellena el formulario.</span><span class="sxs-lookup"><span data-stu-id="7a5b5-110">Discusses how to create event handlers that respond to events that occur as a user fills out a form.</span></span>
    
[<span data-ttu-id="7a5b5-111">Acceso a datos del formulario</span><span class="sxs-lookup"><span data-stu-id="7a5b5-111">Access Form Data</span></span>](how-to-access-form-data.md)
  
> <span data-ttu-id="7a5b5-112">Trata de cómo obtener acceso a información sobre el documento XML subyacente del formulario y los datos que contiene y cómo realizar alguna acción en el mismo.</span><span class="sxs-lookup"><span data-stu-id="7a5b5-112">Discusses how to access information about the form's underlying XML document, the data it contains, or to perform some action on the XML document.</span></span>
    
[<span data-ttu-id="7a5b5-113">Acceso a orígenes de datos externos</span><span class="sxs-lookup"><span data-stu-id="7a5b5-113">Access External Data Sources</span></span>](how-to-access-external-data-sources.md)
  
> <span data-ttu-id="7a5b5-114">Trata de cómo obtener acceso a los datos de orígenes externos.</span><span class="sxs-lookup"><span data-stu-id="7a5b5-114">Discusses how to access data from external data sources.</span></span>
    
[<span data-ttu-id="7a5b5-115">Escribir lógica condicional que determina el entorno de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="7a5b5-115">Write Conditional Logic That Determines the Run-time Environment</span></span>](how-to-write-conditional-logic-that-determines-the-run-time-environment.md)
  
> <span data-ttu-id="7a5b5-116">Se explica cómo escribir código que lleve a cabo una acción diferente dependiendo de si está abierto en InfoPath, un explorador web o un explorador móvil.</span><span class="sxs-lookup"><span data-stu-id="7a5b5-116">Discusses how to write code that performs a different action depending on whether the form is open in InfoPath, a Web browser, or a mobile browser.</span></span>
    
[<span data-ttu-id="7a5b5-117">Trabajar con ventanas de formularios</span><span class="sxs-lookup"><span data-stu-id="7a5b5-117">Work with Form Windows</span></span>](how-to-work-with-form-windows.md)
  
> <span data-ttu-id="7a5b5-118">Trata de cómo trabajar con ventanas de formularios.</span><span class="sxs-lookup"><span data-stu-id="7a5b5-118">Discusses how to work with form windows.</span></span>
    
[<span data-ttu-id="7a5b5-119">Trabajar con vistas</span><span class="sxs-lookup"><span data-stu-id="7a5b5-119">Work with Views</span></span>](how-to-work-with-views.md)
  
> <span data-ttu-id="7a5b5-120">Trata de cómo trabajar con vistas.</span><span class="sxs-lookup"><span data-stu-id="7a5b5-120">Discusses how to work with views.</span></span>
    
[<span data-ttu-id="7a5b5-121">Trabajar con soluciones sin conexión</span><span class="sxs-lookup"><span data-stu-id="7a5b5-121">Work with Offline Solutions</span></span>](how-to-work-with-offline-solutions.md)
  
> <span data-ttu-id="7a5b5-122">Trata de cómo trabajar con soluciones sin conexión.</span><span class="sxs-lookup"><span data-stu-id="7a5b5-122">Discusses how to work with offline solutions.</span></span>
    
[<span data-ttu-id="7a5b5-123">Trabajar con firmas digitales</span><span class="sxs-lookup"><span data-stu-id="7a5b5-123">Work with Digital Signatures</span></span>](how-to-work-with-digital-signatures.md)
  
> <span data-ttu-id="7a5b5-124">Trata de cómo trabajar con firmas digitales.</span><span class="sxs-lookup"><span data-stu-id="7a5b5-124">Discusses how to work with digital signatures.</span></span>
    
[<span data-ttu-id="7a5b5-125">Controlar errores</span><span class="sxs-lookup"><span data-stu-id="7a5b5-125">Handle Errors</span></span>](how-to-handle-errors.md)
  
> <span data-ttu-id="7a5b5-126">Explica cómo tratar los errores en los proyectos de código administrado de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="7a5b5-126">Discusses how to handle errors in InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="7a5b5-127">Trabajar con derechos de información de configuración de administración</span><span class="sxs-lookup"><span data-stu-id="7a5b5-127">Work with Information Rights Management Settings</span></span>](how-to-work-with-information-rights-management-settings.md)
  
> <span data-ttu-id="7a5b5-128">Explica cómo trabajar con la configuración de Information Rights Management</span><span class="sxs-lookup"><span data-stu-id="7a5b5-128">Discusses how to work with Information Rights Management (IRM) settings.</span></span>
    
[<span data-ttu-id="7a5b5-129">Agregar y hacer referencia a ensamblados personalizados</span><span class="sxs-lookup"><span data-stu-id="7a5b5-129">Add and Reference Custom Assemblies</span></span>](how-to-add-and-reference-custom-assemblies.md)
  
> <span data-ttu-id="7a5b5-130">Explica cómo agregar ensamblados personalizados a un proyecto de plantilla de formulario.</span><span class="sxs-lookup"><span data-stu-id="7a5b5-130">Discusses how to add custom assemblies to a form template project.</span></span>
    

