---
title: IUnknown IMAPIFormAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink
api_type:
- COM
ms.assetid: 180022af-4c1c-408c-a3fe-ed075cef79ab
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 68c2af0cd8d7ccddf6aa6017cfb830b196ac0771
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286607"
---
# <a name="imapiformadvisesink--iunknown"></a><span data-ttu-id="4aaac-103">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4aaac-103">IMAPIFormAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="4aaac-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4aaac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4aaac-105">Permite que los servidores de formularios reciban notificaciones de visores de formulario.</span><span class="sxs-lookup"><span data-stu-id="4aaac-105">Enables form servers to receive notifications from form viewers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4aaac-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="4aaac-106">Header file:</span></span>  <br/> |<span data-ttu-id="4aaac-107">MAPIForm. h</span><span class="sxs-lookup"><span data-stu-id="4aaac-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="4aaac-108">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="4aaac-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="4aaac-109">Notificar a los objetos de receptor de formulario</span><span class="sxs-lookup"><span data-stu-id="4aaac-109">Form advise sink objects</span></span>  <br/> |
|<span data-ttu-id="4aaac-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="4aaac-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="4aaac-111">Servidores de formulario</span><span class="sxs-lookup"><span data-stu-id="4aaac-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="4aaac-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="4aaac-112">Called by:</span></span>  <br/> |<span data-ttu-id="4aaac-113">Visores de formularios</span><span class="sxs-lookup"><span data-stu-id="4aaac-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="4aaac-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="4aaac-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="4aaac-115">IID_IMAPIFormAdviseSink</span><span class="sxs-lookup"><span data-stu-id="4aaac-115">IID_IMAPIFormAdviseSink</span></span>  <br/> |
|<span data-ttu-id="4aaac-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="4aaac-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="4aaac-117">LPMAPIFORMADVISESINK</span><span class="sxs-lookup"><span data-stu-id="4aaac-117">LPMAPIFORMADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="4aaac-118">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="4aaac-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="4aaac-119">OnChange</span><span class="sxs-lookup"><span data-stu-id="4aaac-119">OnChange</span></span>](imapiformadvisesink-onchange.md) <br/> |<span data-ttu-id="4aaac-120">Indica que se ha producido un cambio en el estado del visor de formularios.</span><span class="sxs-lookup"><span data-stu-id="4aaac-120">Indicates that a change has occurred in the status of the form viewer.</span></span>  <br/> |
|[<span data-ttu-id="4aaac-121">OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="4aaac-121">OnActivateNext</span></span>](imapiformadvisesink-onactivatenext.md) <br/> |<span data-ttu-id="4aaac-122">Indica si el formulario puede controlar la clase de mensaje del siguiente mensaje que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="4aaac-122">Indicates whether the form can handle the message class of the next message to display.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4aaac-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4aaac-123">Remarks</span></span>

<span data-ttu-id="4aaac-124">Los servidores de formularios usan un objeto Sink de notificaciones de formulario para implementar **IMAPIFormAdviseSink** en lugar de incluirlos con el objeto Form.</span><span class="sxs-lookup"><span data-stu-id="4aaac-124">Form servers use a form advise sink object to implement **IMAPIFormAdviseSink** instead of including it with their form object.</span></span> <span data-ttu-id="4aaac-125">Por lo tanto, los visores de formulario deben esperar una llamada fallida al método [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) de un formulario para obtener un puntero a esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="4aaac-125">Therefore, form viewers should expect a failed call to a form's [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method to obtain a pointer to this interface.</span></span> 
  
<span data-ttu-id="4aaac-126">Los servidores de formularios llaman al método [IMAPIViewContext:: SetAdviseSink](imapiviewcontext-setadvisesink.md) del visor para registrarse en las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="4aaac-126">Form servers call a viewer's [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method to register for notifications.</span></span> <span data-ttu-id="4aaac-127">Un puntero a su implementación de **IMAPIFormAdviseSink** se incluye como parámetro.</span><span class="sxs-lookup"><span data-stu-id="4aaac-127">A pointer to their **IMAPIFormAdviseSink** implementation is included as a parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4aaac-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="4aaac-128">See also</span></span>



[<span data-ttu-id="4aaac-129">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="4aaac-129">MAPI Interfaces</span></span>](mapi-interfaces.md)

