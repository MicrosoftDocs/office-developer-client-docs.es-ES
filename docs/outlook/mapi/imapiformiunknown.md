---
title: IMAPIForm IUnknown
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
ms.openlocfilehash: fce8bc45d5cc87c238288653ab989b62076ad451
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817307"
---
# <a name="imapiform--iunknown"></a><span data-ttu-id="853fe-103">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="853fe-103">IMAPIForm : IUnknown</span></span>

  
  
<span data-ttu-id="853fe-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="853fe-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="853fe-105">Permite que los visores de formulario trabajar con contextos de vista de formulario y notificación de formulario, para llevar a cabo los verbos de formulario y cerrar formularios.</span><span class="sxs-lookup"><span data-stu-id="853fe-105">Enables form viewers to work with form view contexts and form notification, to perform form verbs, and to shut down forms.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="853fe-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="853fe-106">Header file:</span></span>  <br/> |<span data-ttu-id="853fe-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="853fe-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="853fe-108">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="853fe-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="853fe-109">Objetos de formulario</span><span class="sxs-lookup"><span data-stu-id="853fe-109">Form objects</span></span>  <br/> |
|<span data-ttu-id="853fe-110">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="853fe-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="853fe-111">Servidores de formulario</span><span class="sxs-lookup"><span data-stu-id="853fe-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="853fe-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="853fe-112">Called by:</span></span>  <br/> |<span data-ttu-id="853fe-113">Visores de formulario</span><span class="sxs-lookup"><span data-stu-id="853fe-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="853fe-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="853fe-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="853fe-115">IID_IMAPIForm</span><span class="sxs-lookup"><span data-stu-id="853fe-115">IID_IMAPIForm</span></span>  <br/> |
|<span data-ttu-id="853fe-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="853fe-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="853fe-117">LPMAPIFORM</span><span class="sxs-lookup"><span data-stu-id="853fe-117">LPMAPIFORM</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="853fe-118">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="853fe-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="853fe-119">SetViewContext</span><span class="sxs-lookup"><span data-stu-id="853fe-119">SetViewContext</span></span>](imapiform-setviewcontext.md) <br/> |<span data-ttu-id="853fe-120">Establece un contexto de vista para el formulario.</span><span class="sxs-lookup"><span data-stu-id="853fe-120">Establishes a view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="853fe-121">GetViewContext</span><span class="sxs-lookup"><span data-stu-id="853fe-121">GetViewContext</span></span>](imapiform-getviewcontext.md) <br/> |<span data-ttu-id="853fe-122">Devuelve el contexto de la vista actual para el formulario.</span><span class="sxs-lookup"><span data-stu-id="853fe-122">Returns the current view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="853fe-123">ShutdownForm</span><span class="sxs-lookup"><span data-stu-id="853fe-123">ShutdownForm</span></span>](imapiform-shutdownform.md) <br/> |<span data-ttu-id="853fe-124">Cierra el formulario.</span><span class="sxs-lookup"><span data-stu-id="853fe-124">Closes the form.</span></span>  <br/> |
|[<span data-ttu-id="853fe-125">DoVerb</span><span class="sxs-lookup"><span data-stu-id="853fe-125">DoVerb</span></span>](imapiform-doverb.md) <br/> |<span data-ttu-id="853fe-126">Las solicitudes que el formulario realiza tareas con independencia de se asocia a un verbo específico.</span><span class="sxs-lookup"><span data-stu-id="853fe-126">Requests that the form perform whatever tasks it associates with a specific verb.</span></span>  <br/> |
|[<span data-ttu-id="853fe-127">Aviso</span><span class="sxs-lookup"><span data-stu-id="853fe-127">Advise</span></span>](imapiform-advise.md) <br/> |<span data-ttu-id="853fe-128">Registra un visor de formulario para las notificaciones sobre los eventos que afectan a la forma.</span><span class="sxs-lookup"><span data-stu-id="853fe-128">Registers a form viewer for notifications about events that affect the form.</span></span>  <br/> |
|[<span data-ttu-id="853fe-129">Desaconsejar</span><span class="sxs-lookup"><span data-stu-id="853fe-129">Unadvise</span></span>](imapiform-unadvise.md) <br/> |<span data-ttu-id="853fe-130">Cancela un registro para las notificaciones con un visor de formulario establecido previamente mediante una llamada a **Advise**.</span><span class="sxs-lookup"><span data-stu-id="853fe-130">Cancels a registration for notifications with a form viewer previously established by calling **Advise**.</span></span>  <br/> |
|[<span data-ttu-id="853fe-131">GetLastError</span><span class="sxs-lookup"><span data-stu-id="853fe-131">GetLastError</span></span>](imapiform-getlasterror.md) <br/> |<span data-ttu-id="853fe-132">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se producen al objeto form.</span><span class="sxs-lookup"><span data-stu-id="853fe-132">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="853fe-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="853fe-133">See also</span></span>



[<span data-ttu-id="853fe-134">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="853fe-134">MAPI Interfaces</span></span>](mapi-interfaces.md)

