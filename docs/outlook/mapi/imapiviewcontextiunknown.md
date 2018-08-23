---
title: IMAPIViewContext IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext
api_type:
- COM
ms.assetid: d566ff39-92c1-4a14-85e5-1c406825f805
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ae2729ec5620b6b408a5c999d4b6ede7143bed2f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584571"
---
# <a name="imapiviewcontext--iunknown"></a><span data-ttu-id="95856-103">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="95856-103">IMAPIViewContext : IUnknown</span></span>

  
  
<span data-ttu-id="95856-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95856-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95856-105">Administra un formulario en el Visor de formulario de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="95856-105">Manages a form in a client application's form viewer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="95856-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="95856-106">Header file:</span></span>  <br/> |<span data-ttu-id="95856-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="95856-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="95856-108">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="95856-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="95856-109">Objetos de contexto de vista</span><span class="sxs-lookup"><span data-stu-id="95856-109">View context objects</span></span>  <br/> |
|<span data-ttu-id="95856-110">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="95856-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="95856-111">Visores de formulario</span><span class="sxs-lookup"><span data-stu-id="95856-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="95856-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="95856-112">Called by:</span></span>  <br/> |<span data-ttu-id="95856-113">Objetos de formulario</span><span class="sxs-lookup"><span data-stu-id="95856-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="95856-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="95856-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="95856-115">IID_IMAPIViewContext</span><span class="sxs-lookup"><span data-stu-id="95856-115">IID_IMAPIViewContext</span></span>  <br/> |
|<span data-ttu-id="95856-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="95856-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="95856-117">LPMAPIVIEWCONTEXT</span><span class="sxs-lookup"><span data-stu-id="95856-117">LPMAPIVIEWCONTEXT</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="95856-118">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="95856-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="95856-119">SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="95856-119">SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md) <br/> |<span data-ttu-id="95856-120">Administra el registro de un formulario para recibir las notificaciones sobre cambios en el Visor.</span><span class="sxs-lookup"><span data-stu-id="95856-120">Manages a form's registration to receive notifications about changes in the viewer.</span></span>  <br/> |
|[<span data-ttu-id="95856-121">ActivateNext</span><span class="sxs-lookup"><span data-stu-id="95856-121">ActivateNext</span></span>](imapiviewcontext-activatenext.md) <br/> |<span data-ttu-id="95856-122">Activa el mensaje siguiente o anterior en el Visor de formulario.</span><span class="sxs-lookup"><span data-stu-id="95856-122">Activates the next or previous message in the form viewer.</span></span>  <br/> |
|[<span data-ttu-id="95856-123">GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="95856-123">GetPrintSetup</span></span>](imapiviewcontext-getprintsetup.md) <br/> |<span data-ttu-id="95856-124">Recupera información de impresión actual.</span><span class="sxs-lookup"><span data-stu-id="95856-124">Retrieves current printing information.</span></span>  <br/> |
|[<span data-ttu-id="95856-125">GetSaveStream</span><span class="sxs-lookup"><span data-stu-id="95856-125">GetSaveStream</span></span>](imapiviewcontext-getsavestream.md) <br/> |<span data-ttu-id="95856-126">Recupera una secuencia que se utilizará para guardar el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="95856-126">Retrieves a stream to be used for saving the current message.</span></span>  <br/> |
|[<span data-ttu-id="95856-127">GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="95856-127">GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md) <br/> |<span data-ttu-id="95856-128">Recupera el estado actual del Visor.</span><span class="sxs-lookup"><span data-stu-id="95856-128">Retrieves the current viewer status.</span></span>  <br/> |
|[<span data-ttu-id="95856-129">GetLastError</span><span class="sxs-lookup"><span data-stu-id="95856-129">GetLastError</span></span>](imapiviewcontext-getlasterror.md) <br/> |<span data-ttu-id="95856-130">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se producen en el objeto de contexto de la vista.</span><span class="sxs-lookup"><span data-stu-id="95856-130">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring in the view context object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="95856-131">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="95856-131">See also</span></span>



[<span data-ttu-id="95856-132">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="95856-132">MAPI Interfaces</span></span>](mapi-interfaces.md)

