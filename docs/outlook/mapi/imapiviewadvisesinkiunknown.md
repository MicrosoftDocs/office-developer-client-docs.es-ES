---
title: IMAPIViewAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink
api_type:
- COM
ms.assetid: 1231391d-803a-4b41-b252-4d986f99361a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 157703fc9702bb954b4a5c570fc3d5c045e181cc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567191"
---
# <a name="imapiviewadvisesink--iunknown"></a><span data-ttu-id="646f5-103">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="646f5-103">IMAPIViewAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="646f5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="646f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="646f5-105">Recibe las notificaciones de formularios.</span><span class="sxs-lookup"><span data-stu-id="646f5-105">Receives notifications from forms.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="646f5-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="646f5-106">Header file:</span></span>  <br/> |<span data-ttu-id="646f5-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="646f5-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="646f5-108">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="646f5-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="646f5-109">Vista de aviso receptor objetos</span><span class="sxs-lookup"><span data-stu-id="646f5-109">View advise sink objects</span></span>  <br/> |
|<span data-ttu-id="646f5-110">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="646f5-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="646f5-111">Visores de formulario</span><span class="sxs-lookup"><span data-stu-id="646f5-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="646f5-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="646f5-112">Called by:</span></span>  <br/> |<span data-ttu-id="646f5-113">Objetos de formulario</span><span class="sxs-lookup"><span data-stu-id="646f5-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="646f5-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="646f5-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="646f5-115">IID_IMAPIViewAdviseSink</span><span class="sxs-lookup"><span data-stu-id="646f5-115">IID_IMAPIViewAdviseSink</span></span>  <br/> |
|<span data-ttu-id="646f5-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="646f5-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="646f5-117">LPMAPIVIEWADVISESINK</span><span class="sxs-lookup"><span data-stu-id="646f5-117">LPMAPIVIEWADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="646f5-118">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="646f5-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="646f5-119">OnShutdown</span><span class="sxs-lookup"><span data-stu-id="646f5-119">OnShutdown</span></span>](imapiviewadvisesink-onshutdown.md) <br/> |<span data-ttu-id="646f5-120">Se notifica al Visor de formulario que se está cerrando un formulario.</span><span class="sxs-lookup"><span data-stu-id="646f5-120">Notifies the form viewer that a form is being closed.</span></span>  <br/> |
|[<span data-ttu-id="646f5-121">OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="646f5-121">OnNewMessage</span></span>](imapiviewadvisesink-onnewmessage.md) <br/> |<span data-ttu-id="646f5-122">Se notifica al Visor de formulario que ha cargado un nuevo o un mensaje existente en un formulario.</span><span class="sxs-lookup"><span data-stu-id="646f5-122">Notifies the form viewer that either a new or an existing message has been loaded in a form.</span></span>  <br/> |
|[<span data-ttu-id="646f5-123">OnPrint</span><span class="sxs-lookup"><span data-stu-id="646f5-123">OnPrint</span></span>](imapiviewadvisesink-onprint.md) <br/> |<span data-ttu-id="646f5-124">Se notifica el Visor de formulario del estado de impresión de un formulario.</span><span class="sxs-lookup"><span data-stu-id="646f5-124">Notifies the form viewer of the printing status of a form.</span></span>  <br/> |
|[<span data-ttu-id="646f5-125">OnSubmitted</span><span class="sxs-lookup"><span data-stu-id="646f5-125">OnSubmitted</span></span>](imapiviewadvisesink-onsubmitted.md) <br/> |<span data-ttu-id="646f5-126">Se notifica al Visor de formulario que se ha enviado el mensaje actual a la cola de MAPI.</span><span class="sxs-lookup"><span data-stu-id="646f5-126">Notifies the form viewer that the current message has been submitted to MAPI spooler.</span></span>  <br/> |
|[<span data-ttu-id="646f5-127">OnSaved</span><span class="sxs-lookup"><span data-stu-id="646f5-127">OnSaved</span></span>](imapiviewadvisesink-onsaved.md) <br/> |<span data-ttu-id="646f5-128">Se notifica el Visor de formulario que se ha guardado el mensaje actual en un formulario.</span><span class="sxs-lookup"><span data-stu-id="646f5-128">Notifies the form viewer that the current message in a form has been saved.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="646f5-129">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="646f5-129">See also</span></span>



[<span data-ttu-id="646f5-130">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="646f5-130">MAPI Interfaces</span></span>](mapi-interfaces.md)

