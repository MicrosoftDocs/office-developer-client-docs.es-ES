---
title: IUnknown IMAPIViewAdviseSink
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
ms.openlocfilehash: 70f61fe33baa7870a58c4cbc7d75e0df119b5b1a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351143"
---
# <a name="imapiviewadvisesink--iunknown"></a><span data-ttu-id="6b67f-103">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6b67f-103">IMAPIViewAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="6b67f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b67f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b67f-105">Recibe notificaciones de los formularios.</span><span class="sxs-lookup"><span data-stu-id="6b67f-105">Receives notifications from forms.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6b67f-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="6b67f-106">Header file:</span></span>  <br/> |<span data-ttu-id="6b67f-107">MAPIForm. h</span><span class="sxs-lookup"><span data-stu-id="6b67f-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="6b67f-108">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="6b67f-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="6b67f-109">Ver los objetos del receptor de avisos</span><span class="sxs-lookup"><span data-stu-id="6b67f-109">View advise sink objects</span></span>  <br/> |
|<span data-ttu-id="6b67f-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="6b67f-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="6b67f-111">Visores de formularios</span><span class="sxs-lookup"><span data-stu-id="6b67f-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="6b67f-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="6b67f-112">Called by:</span></span>  <br/> |<span data-ttu-id="6b67f-113">Objetos de formulario</span><span class="sxs-lookup"><span data-stu-id="6b67f-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="6b67f-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="6b67f-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="6b67f-115">IID_IMAPIViewAdviseSink</span><span class="sxs-lookup"><span data-stu-id="6b67f-115">IID_IMAPIViewAdviseSink</span></span>  <br/> |
|<span data-ttu-id="6b67f-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="6b67f-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="6b67f-117">LPMAPIVIEWADVISESINK</span><span class="sxs-lookup"><span data-stu-id="6b67f-117">LPMAPIVIEWADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="6b67f-118">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="6b67f-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="6b67f-119">Shutdown</span><span class="sxs-lookup"><span data-stu-id="6b67f-119">OnShutdown</span></span>](imapiviewadvisesink-onshutdown.md) <br/> |<span data-ttu-id="6b67f-120">Notifica al visor de formularios que se va a cerrar un formulario.</span><span class="sxs-lookup"><span data-stu-id="6b67f-120">Notifies the form viewer that a form is being closed.</span></span>  <br/> |
|[<span data-ttu-id="6b67f-121">OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="6b67f-121">OnNewMessage</span></span>](imapiviewadvisesink-onnewmessage.md) <br/> |<span data-ttu-id="6b67f-122">Notifica al visor de formularios que ya se ha cargado un mensaje nuevo o existente en un formulario.</span><span class="sxs-lookup"><span data-stu-id="6b67f-122">Notifies the form viewer that either a new or an existing message has been loaded in a form.</span></span>  <br/> |
|[<span data-ttu-id="6b67f-123">OnPrint</span><span class="sxs-lookup"><span data-stu-id="6b67f-123">OnPrint</span></span>](imapiviewadvisesink-onprint.md) <br/> |<span data-ttu-id="6b67f-124">Notifica al visor del formulario el estado de impresión de un formulario.</span><span class="sxs-lookup"><span data-stu-id="6b67f-124">Notifies the form viewer of the printing status of a form.</span></span>  <br/> |
|[<span data-ttu-id="6b67f-125">Enviado</span><span class="sxs-lookup"><span data-stu-id="6b67f-125">OnSubmitted</span></span>](imapiviewadvisesink-onsubmitted.md) <br/> |<span data-ttu-id="6b67f-126">Notifica al visor de formularios que el mensaje actual se ha enviado al administrador de trabajos en cola de MAPI.</span><span class="sxs-lookup"><span data-stu-id="6b67f-126">Notifies the form viewer that the current message has been submitted to MAPI spooler.</span></span>  <br/> |
|[<span data-ttu-id="6b67f-127">OnSave</span><span class="sxs-lookup"><span data-stu-id="6b67f-127">OnSaved</span></span>](imapiviewadvisesink-onsaved.md) <br/> |<span data-ttu-id="6b67f-128">Notifica al visor de formularios que se ha guardado el mensaje actual en un formulario.</span><span class="sxs-lookup"><span data-stu-id="6b67f-128">Notifies the form viewer that the current message in a form has been saved.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6b67f-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b67f-129">See also</span></span>



[<span data-ttu-id="6b67f-130">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="6b67f-130">MAPI Interfaces</span></span>](mapi-interfaces.md)

