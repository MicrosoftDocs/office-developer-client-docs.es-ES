---
title: IMAPIFormAdviseSink IUnknown
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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392063"
---
# <a name="imapiformadvisesink--iunknown"></a><span data-ttu-id="8c30d-103">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8c30d-103">IMAPIFormAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="8c30d-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c30d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c30d-105">Permite que los servidores de formulario para recibir notificaciones de los visores del formulario.</span><span class="sxs-lookup"><span data-stu-id="8c30d-105">Enables form servers to receive notifications from form viewers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8c30d-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="8c30d-106">Header file:</span></span>  <br/> |<span data-ttu-id="8c30d-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="8c30d-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="8c30d-108">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="8c30d-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="8c30d-109">Formulario de aviso receptor objetos</span><span class="sxs-lookup"><span data-stu-id="8c30d-109">Form advise sink objects</span></span>  <br/> |
|<span data-ttu-id="8c30d-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="8c30d-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="8c30d-111">Servidores de formulario</span><span class="sxs-lookup"><span data-stu-id="8c30d-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="8c30d-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="8c30d-112">Called by:</span></span>  <br/> |<span data-ttu-id="8c30d-113">Visores de formulario</span><span class="sxs-lookup"><span data-stu-id="8c30d-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="8c30d-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="8c30d-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="8c30d-115">IID_IMAPIFormAdviseSink</span><span class="sxs-lookup"><span data-stu-id="8c30d-115">IID_IMAPIFormAdviseSink</span></span>  <br/> |
|<span data-ttu-id="8c30d-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="8c30d-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="8c30d-117">LPMAPIFORMADVISESINK</span><span class="sxs-lookup"><span data-stu-id="8c30d-117">LPMAPIFORMADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="8c30d-118">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="8c30d-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="8c30d-119">OnChange</span><span class="sxs-lookup"><span data-stu-id="8c30d-119">OnChange</span></span>](imapiformadvisesink-onchange.md) <br/> |<span data-ttu-id="8c30d-120">Indica que se ha producido un cambio en el estado del Visor del formulario.</span><span class="sxs-lookup"><span data-stu-id="8c30d-120">Indicates that a change has occurred in the status of the form viewer.</span></span>  <br/> |
|[<span data-ttu-id="8c30d-121">OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="8c30d-121">OnActivateNext</span></span>](imapiformadvisesink-onactivatenext.md) <br/> |<span data-ttu-id="8c30d-122">Indica si el formulario puede controlar la clase de mensaje del mensaje siguiente para mostrar.</span><span class="sxs-lookup"><span data-stu-id="8c30d-122">Indicates whether the form can handle the message class of the next message to display.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8c30d-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8c30d-123">Remarks</span></span>

<span data-ttu-id="8c30d-124">Uso de servidores de formulario un formulario de aviso objeto receptor para implementar **IMAPIFormAdviseSink** en lugar de incluir con su objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="8c30d-124">Form servers use a form advise sink object to implement **IMAPIFormAdviseSink** instead of including it with their form object.</span></span> <span data-ttu-id="8c30d-125">Por lo tanto, los visores de formulario deben esperar un error de la llamada al método [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) de un formulario para obtener un puntero a esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="8c30d-125">Therefore, form viewers should expect a failed call to a form's [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method to obtain a pointer to this interface.</span></span> 
  
<span data-ttu-id="8c30d-126">Formulario servidores llamar [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) al método de un visor registrar para recibir notificaciones.</span><span class="sxs-lookup"><span data-stu-id="8c30d-126">Form servers call a viewer's [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method to register for notifications.</span></span> <span data-ttu-id="8c30d-127">Un puntero a su implementación de **IMAPIFormAdviseSink** se incluye como un parámetro.</span><span class="sxs-lookup"><span data-stu-id="8c30d-127">A pointer to their **IMAPIFormAdviseSink** implementation is included as a parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8c30d-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c30d-128">See also</span></span>



[<span data-ttu-id="8c30d-129">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="8c30d-129">MAPI Interfaces</span></span>](mapi-interfaces.md)

