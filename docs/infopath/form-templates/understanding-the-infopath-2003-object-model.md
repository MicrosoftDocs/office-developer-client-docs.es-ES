---
title: Comprender el modelo de objetos de InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, object model,InfoPath 2003-compatible object model,object models [InfoPath 2003]
localization_priority: Normal
ms.assetid: cd0a890b-5a8b-42c0-abdd-5ce28aff1ba1
description: En esta sección, se trata el modelo de objeto de las soluciones de código administrado de InfoPath y se describe las tareas de programación más comunes.
ms.openlocfilehash: 0c07201475bb7bfe24182faf61cc1bf6df733709
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299786"
---
# <a name="understanding-the-infopath-2003-object-model"></a><span data-ttu-id="0b6a1-104">Descripción del modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="0b6a1-104">Understanding the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="0b6a1-105">En esta sección, se trata el modelo de objeto de las soluciones de código administrado de InfoPath y se describe las tareas de programación más comunes.</span><span class="sxs-lookup"><span data-stu-id="0b6a1-105">This section discusses the object model for InfoPath managed-code solutions, and describes common programming tasks.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="0b6a1-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="0b6a1-106">In this section</span></span>

[<span data-ttu-id="0b6a1-107">Modelos de objetos compatibles con InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="0b6a1-107">InfoPath 2003 Compatible Object Models</span></span>](infopath-2003-compatible-object-models.md)
  
> <span data-ttu-id="0b6a1-108">Ofrece información general sobre los modelos de objetos que se utilizan en los proyectos de código administrado de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="0b6a1-108">Provides an overview of the object models used in InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="0b6a1-109">Obtener acceso a datos de aplicaciones mediante el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="0b6a1-109">Access Application Data Using the InfoPath 2003 Object Model</span></span>](how-to-access-application-data-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="0b6a1-110">Trata de cómo obtener acceso a información sobre la aplicación InfoPath, el documento XML subyacente del formulario y el archivo de definición de formularios (.xsf).</span><span class="sxs-lookup"><span data-stu-id="0b6a1-110">Discusses how to access information about the InfoPath application, the form's underlying XML document, and the form definition (.xsf) file.</span></span>
    
[<span data-ttu-id="0b6a1-111">Obtener acceso a orígenes de datos externos mediante el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="0b6a1-111">Access External Data Sources Using the InfoPath 2003 Object Model</span></span>](how-to-access-external-data-sources-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="0b6a1-112">Trata de cómo obtener acceso a los datos de orígenes externos.</span><span class="sxs-lookup"><span data-stu-id="0b6a1-112">Discusses how to access data from external data sources.</span></span>
    
[<span data-ttu-id="0b6a1-113">Obtener acceso a datos de formulario con el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="0b6a1-113">Access Form Data Using the InfoPath 2003 Object Model</span></span>](how-to-access-form-data-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="0b6a1-114">Trata de cómo obtener acceso a información sobre el documento XML subyacente del formulario y los datos que contiene y cómo realizar alguna acción en el mismo.</span><span class="sxs-lookup"><span data-stu-id="0b6a1-114">Discusses how to access information about the form's underlying XML document, the data it contains, or to perform some action on the XML document.</span></span>
    
[<span data-ttu-id="0b6a1-115">Mostrar alertas y cuadros de diálogo con el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="0b6a1-115">Display Alerts and Dialog Boxes Using the InfoPath 2003 Object Model</span></span>](how-to-display-alerts-and-dialog-boxes-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="0b6a1-116">Trata de cómo mostrar alertas y cuadros de diálogo en los proyectos de código administrado de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="0b6a1-116">Discusses how to display alerts and dialog boxes in InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="0b6a1-117">Controlar errores con el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="0b6a1-117">Handle Errors Using the InfoPath 2003 Object Model</span></span>](how-to-handle-errors-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="0b6a1-118">Explica cómo tratar los errores en los proyectos de código administrado de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="0b6a1-118">Discusses how to handle errors in InfoPath managed-code projects.</span></span>
    
[<span data-ttu-id="0b6a1-119">Responder a eventos de formulario con el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="0b6a1-119">Respond to Form Events Using the InfoPath 2003 Object Model</span></span>](how-to-respond-to-form-events-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="0b6a1-120">Trata de cómo crear controladores de eventos que respondan a los eventos que se producen mientras el usuario rellena el formulario.</span><span class="sxs-lookup"><span data-stu-id="0b6a1-120">Discusses how to create event handlers that respond to events that occur as a user fills out a form.</span></span>
    
[<span data-ttu-id="0b6a1-121">Trabajar con ventanas de formularios mediante el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="0b6a1-121">Work with Form Windows Using the InfoPath 2003 Object Model</span></span>](how-to-work-with-form-windows-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="0b6a1-122">Trata de cómo trabajar con ventanas de formularios.</span><span class="sxs-lookup"><span data-stu-id="0b6a1-122">Discusses how to work with form windows.</span></span>
    
[<span data-ttu-id="0b6a1-123">Trabajar con vistas mediante el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="0b6a1-123">Work with Views Using the InfoPath 2003 Object Model</span></span>](how-to-work-with-views-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="0b6a1-124">Trata de cómo trabajar con vistas.</span><span class="sxs-lookup"><span data-stu-id="0b6a1-124">Discusses how to work with views.</span></span>
    
[<span data-ttu-id="0b6a1-125">Trabajar con firmas digitales mediante el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="0b6a1-125">Work with Digital Signatures Using the InfoPath 2003 Object Model</span></span>](how-to-work-with-digital-signatures-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="0b6a1-126">Trata de cómo trabajar con firmas digitales.</span><span class="sxs-lookup"><span data-stu-id="0b6a1-126">Discusses how to work with digital signatures.</span></span>
    
[<span data-ttu-id="0b6a1-127">Trabajar con soluciones sin conexión mediante el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="0b6a1-127">Work with Offline Solutions Using the InfoPath 2003 Object Model</span></span>](how-to-work-with-offline-solutions-using-the-infopath-2003-object-model.md)
  
> <span data-ttu-id="0b6a1-128">Trata de cómo trabajar con soluciones sin conexión.</span><span class="sxs-lookup"><span data-stu-id="0b6a1-128">Discusses how to work with offline solutions.</span></span>
    

