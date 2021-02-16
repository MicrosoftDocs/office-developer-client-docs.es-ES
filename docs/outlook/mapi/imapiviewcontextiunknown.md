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
ms.openlocfilehash: db0c375218755c3a28475e2ebce2d097fb789f75
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406034"
---
# <a name="imapiviewcontext--iunknown"></a><span data-ttu-id="1defb-103">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1defb-103">IMAPIViewContext : IUnknown</span></span>

  
  
<span data-ttu-id="1defb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1defb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1defb-105">Administra un formulario en el visor de formularios de una aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="1defb-105">Manages a form in a client application's form viewer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1defb-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="1defb-106">Header file:</span></span>  <br/> |<span data-ttu-id="1defb-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="1defb-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="1defb-108">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="1defb-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="1defb-109">Ver objetos de contexto</span><span class="sxs-lookup"><span data-stu-id="1defb-109">View context objects</span></span>  <br/> |
|<span data-ttu-id="1defb-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="1defb-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="1defb-111">Visores de formularios</span><span class="sxs-lookup"><span data-stu-id="1defb-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="1defb-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="1defb-112">Called by:</span></span>  <br/> |<span data-ttu-id="1defb-113">Objetos de formulario</span><span class="sxs-lookup"><span data-stu-id="1defb-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="1defb-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="1defb-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="1defb-115">IID_IMAPIViewContext</span><span class="sxs-lookup"><span data-stu-id="1defb-115">IID_IMAPIViewContext</span></span>  <br/> |
|<span data-ttu-id="1defb-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="1defb-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="1defb-117">LPMAPIVIEWCONTEXT</span><span class="sxs-lookup"><span data-stu-id="1defb-117">LPMAPIVIEWCONTEXT</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="1defb-118">Orden de tabla virtual</span><span class="sxs-lookup"><span data-stu-id="1defb-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="1defb-119">SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="1defb-119">SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md) <br/> |<span data-ttu-id="1defb-120">Administra el registro de un formulario para recibir notificaciones sobre los cambios en el visor.</span><span class="sxs-lookup"><span data-stu-id="1defb-120">Manages a form's registration to receive notifications about changes in the viewer.</span></span>  <br/> |
|[<span data-ttu-id="1defb-121">ActivateNext</span><span class="sxs-lookup"><span data-stu-id="1defb-121">ActivateNext</span></span>](imapiviewcontext-activatenext.md) <br/> |<span data-ttu-id="1defb-122">Activa el mensaje siguiente o anterior en el visor de formularios.</span><span class="sxs-lookup"><span data-stu-id="1defb-122">Activates the next or previous message in the form viewer.</span></span>  <br/> |
|[<span data-ttu-id="1defb-123">GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="1defb-123">GetPrintSetup</span></span>](imapiviewcontext-getprintsetup.md) <br/> |<span data-ttu-id="1defb-124">Recupera la información de impresión actual.</span><span class="sxs-lookup"><span data-stu-id="1defb-124">Retrieves current printing information.</span></span>  <br/> |
|[<span data-ttu-id="1defb-125">GetSaveStream</span><span class="sxs-lookup"><span data-stu-id="1defb-125">GetSaveStream</span></span>](imapiviewcontext-getsavestream.md) <br/> |<span data-ttu-id="1defb-126">Recupera una secuencia que se usará para guardar el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="1defb-126">Retrieves a stream to be used for saving the current message.</span></span>  <br/> |
|[<span data-ttu-id="1defb-127">GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="1defb-127">GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md) <br/> |<span data-ttu-id="1defb-128">Recupera el estado del visor actual.</span><span class="sxs-lookup"><span data-stu-id="1defb-128">Retrieves the current viewer status.</span></span>  <br/> |
|[<span data-ttu-id="1defb-129">GetLastError</span><span class="sxs-lookup"><span data-stu-id="1defb-129">GetLastError</span></span>](imapiviewcontext-getlasterror.md) <br/> |<span data-ttu-id="1defb-130">Devuelve una [estructura MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se produce en el objeto de contexto de vista.</span><span class="sxs-lookup"><span data-stu-id="1defb-130">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring in the view context object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1defb-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1defb-131">See also</span></span>



[<span data-ttu-id="1defb-132">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="1defb-132">MAPI Interfaces</span></span>](mapi-interfaces.md)

