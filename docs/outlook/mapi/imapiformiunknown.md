---
title: IUnknown IMAPIForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm
api_type:
- COM
ms.assetid: e9059739-51b4-4574-bd0f-709eb5144ae7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 172cbf9478d3206742df61d211051594e69ab173
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436387"
---
# <a name="imapiform--iunknown"></a><span data-ttu-id="ba916-103">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ba916-103">IMAPIForm : IUnknown</span></span>

  
  
<span data-ttu-id="ba916-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ba916-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ba916-105">Permite a los visores de formulario trabajar con contextos de la vista de formulario y notificaciones de formulario, realizar verbos de formulario y cerrar formularios.</span><span class="sxs-lookup"><span data-stu-id="ba916-105">Enables form viewers to work with form view contexts and form notification, to perform form verbs, and to shut down forms.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ba916-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="ba916-106">Header file:</span></span>  <br/> |<span data-ttu-id="ba916-107">MAPIForm. h</span><span class="sxs-lookup"><span data-stu-id="ba916-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="ba916-108">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="ba916-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="ba916-109">Objetos de formulario</span><span class="sxs-lookup"><span data-stu-id="ba916-109">Form objects</span></span>  <br/> |
|<span data-ttu-id="ba916-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="ba916-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="ba916-111">Servidores de formulario</span><span class="sxs-lookup"><span data-stu-id="ba916-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="ba916-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="ba916-112">Called by:</span></span>  <br/> |<span data-ttu-id="ba916-113">Visores de formularios</span><span class="sxs-lookup"><span data-stu-id="ba916-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="ba916-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="ba916-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="ba916-115">IID_IMAPIForm</span><span class="sxs-lookup"><span data-stu-id="ba916-115">IID_IMAPIForm</span></span>  <br/> |
|<span data-ttu-id="ba916-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="ba916-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="ba916-117">LPMAPIFORM</span><span class="sxs-lookup"><span data-stu-id="ba916-117">LPMAPIFORM</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="ba916-118">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="ba916-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="ba916-119">SetViewContext</span><span class="sxs-lookup"><span data-stu-id="ba916-119">SetViewContext</span></span>](imapiform-setviewcontext.md) <br/> |<span data-ttu-id="ba916-120">Establece un contexto de vista para el formulario.</span><span class="sxs-lookup"><span data-stu-id="ba916-120">Establishes a view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="ba916-121">GetViewContext</span><span class="sxs-lookup"><span data-stu-id="ba916-121">GetViewContext</span></span>](imapiform-getviewcontext.md) <br/> |<span data-ttu-id="ba916-122">Devuelve el contexto de vista actual del formulario.</span><span class="sxs-lookup"><span data-stu-id="ba916-122">Returns the current view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="ba916-123">ShutdownForm</span><span class="sxs-lookup"><span data-stu-id="ba916-123">ShutdownForm</span></span>](imapiform-shutdownform.md) <br/> |<span data-ttu-id="ba916-124">Cierra el formulario.</span><span class="sxs-lookup"><span data-stu-id="ba916-124">Closes the form.</span></span>  <br/> |
|[<span data-ttu-id="ba916-125">DoVerb</span><span class="sxs-lookup"><span data-stu-id="ba916-125">DoVerb</span></span>](imapiform-doverb.md) <br/> |<span data-ttu-id="ba916-126">Solicita que el formulario realice las tareas que asocie con un verbo específico.</span><span class="sxs-lookup"><span data-stu-id="ba916-126">Requests that the form perform whatever tasks it associates with a specific verb.</span></span>  <br/> |
|[<span data-ttu-id="ba916-127">Aconsej</span><span class="sxs-lookup"><span data-stu-id="ba916-127">Advise</span></span>](imapiform-advise.md) <br/> |<span data-ttu-id="ba916-128">Registra un visor de formularios para notificaciones sobre eventos que afectan al formulario.</span><span class="sxs-lookup"><span data-stu-id="ba916-128">Registers a form viewer for notifications about events that affect the form.</span></span>  <br/> |
|[<span data-ttu-id="ba916-129">Unadvise</span><span class="sxs-lookup"><span data-stu-id="ba916-129">Unadvise</span></span>](imapiform-unadvise.md) <br/> |<span data-ttu-id="ba916-130">Cancela un registro de las notificaciones con un visor de formularios previamente establecido por el **Consejo**de llamada.</span><span class="sxs-lookup"><span data-stu-id="ba916-130">Cancels a registration for notifications with a form viewer previously established by calling **Advise**.</span></span>  <br/> |
|[<span data-ttu-id="ba916-131">Volvió</span><span class="sxs-lookup"><span data-stu-id="ba916-131">GetLastError</span></span>](imapiform-getlasterror.md) <br/> |<span data-ttu-id="ba916-132">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se produce en el objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="ba916-132">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ba916-133">Ver también</span><span class="sxs-lookup"><span data-stu-id="ba916-133">See also</span></span>



[<span data-ttu-id="ba916-134">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="ba916-134">MAPI Interfaces</span></span>](mapi-interfaces.md)

