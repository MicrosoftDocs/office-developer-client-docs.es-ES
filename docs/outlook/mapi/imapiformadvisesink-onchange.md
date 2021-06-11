---
title: IMAPIFormAdviseSinkOnChange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink.OnChange
api_type:
- COM
ms.assetid: d700b40f-e5b2-4d37-bf1f-8fd3dfa0dda5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 02663570e3173bbd696af732e71f060d9dee49bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431900"
---
# <a name="imapiformadvisesinkonchange"></a><span data-ttu-id="80b16-103">IMAPIFormAdviseSink::OnChange</span><span class="sxs-lookup"><span data-stu-id="80b16-103">IMAPIFormAdviseSink::OnChange</span></span>

  
  
<span data-ttu-id="80b16-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80b16-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80b16-105">Indica que se ha producido un cambio en el estado del visor de formularios.</span><span class="sxs-lookup"><span data-stu-id="80b16-105">Indicates that a change has occurred in the status of the form viewer.</span></span> 
  
```cpp
HRESULT OnChange(
  ULONG ulDir
);
```

## <a name="parameters"></a><span data-ttu-id="80b16-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="80b16-106">Parameters</span></span>

 <span data-ttu-id="80b16-107">_ulDir_</span><span class="sxs-lookup"><span data-stu-id="80b16-107">_ulDir_</span></span>
  
> <span data-ttu-id="80b16-108">[in] Máscara de bits de marcas que proporciona información sobre el cambio que se ha producido en el visor y la respuesta esperada en el formulario.</span><span class="sxs-lookup"><span data-stu-id="80b16-108">[in] A bitmask of flags that provides information about the change that has occurred in the viewer and the expected response in the form.</span></span> <span data-ttu-id="80b16-109">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="80b16-109">The following flags can be set:</span></span>
    
<span data-ttu-id="80b16-110">VCSTATUS_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="80b16-110">VCSTATUS_CATEGORY</span></span> 
  
> <span data-ttu-id="80b16-111">Hay un mensaje siguiente o anterior en otra categoría.</span><span class="sxs-lookup"><span data-stu-id="80b16-111">There is a next or previous message in another category.</span></span> 
    
<span data-ttu-id="80b16-112">VCSTATUS_INTERACTIVE</span><span class="sxs-lookup"><span data-stu-id="80b16-112">VCSTATUS_INTERACTIVE</span></span> 
  
> <span data-ttu-id="80b16-113">El formulario debe mostrar una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="80b16-113">The form should display a user interface.</span></span> <span data-ttu-id="80b16-114">Si no se establece esta marca, el formulario debe suprimir la visualización de una interfaz de usuario, incluso en respuesta a un verbo que normalmente hace que se muestre una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="80b16-114">If this flag is not set, the form should suppress displaying a user interface, even in response to a verb that usually causes a user interface to be displayed.</span></span> 
    
<span data-ttu-id="80b16-115">VCSTATUS_MODAL</span><span class="sxs-lookup"><span data-stu-id="80b16-115">VCSTATUS_MODAL</span></span> 
  
> <span data-ttu-id="80b16-116">El formulario debe ser modal para el visor de formularios.</span><span class="sxs-lookup"><span data-stu-id="80b16-116">The form is to be modal to the form viewer.</span></span> 
    
<span data-ttu-id="80b16-117">VCSTATUS_NEXT</span><span class="sxs-lookup"><span data-stu-id="80b16-117">VCSTATUS_NEXT</span></span> 
  
> <span data-ttu-id="80b16-118">Hay un siguiente mensaje en el visor de formularios.</span><span class="sxs-lookup"><span data-stu-id="80b16-118">There is a next message in the form viewer.</span></span> 
    
<span data-ttu-id="80b16-119">VCSTATUS_PREV</span><span class="sxs-lookup"><span data-stu-id="80b16-119">VCSTATUS_PREV</span></span> 
  
> <span data-ttu-id="80b16-120">Hay un mensaje anterior en el visor de formularios.</span><span class="sxs-lookup"><span data-stu-id="80b16-120">There is a previous message in the form viewer.</span></span> 
    
<span data-ttu-id="80b16-121">VCSTATUS_READONLY</span><span class="sxs-lookup"><span data-stu-id="80b16-121">VCSTATUS_READONLY</span></span> 
  
> <span data-ttu-id="80b16-122">Las operaciones eliminar, enviar y mover deben deshabilitarse.</span><span class="sxs-lookup"><span data-stu-id="80b16-122">Delete, submit, and move operations should be disabled.</span></span> 
    
<span data-ttu-id="80b16-123">VCSTATUS_UNREAD</span><span class="sxs-lookup"><span data-stu-id="80b16-123">VCSTATUS_UNREAD</span></span> 
  
> <span data-ttu-id="80b16-124">Hay un mensaje no leído siguiente o anterior en el visor de formularios.</span><span class="sxs-lookup"><span data-stu-id="80b16-124">There is a next or previous unread message in the form viewer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="80b16-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="80b16-125">Return value</span></span>

<span data-ttu-id="80b16-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="80b16-126">S_OK</span></span> 
  
> <span data-ttu-id="80b16-127">La notificación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="80b16-127">The notification was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="80b16-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="80b16-128">Remarks</span></span>

<span data-ttu-id="80b16-129">Los visores de formularios llaman al método **IMAPIFormAdviseSink::OnChange** para notificar al formulario sobre un cambio en el estado de un visor.</span><span class="sxs-lookup"><span data-stu-id="80b16-129">Form viewers call the **IMAPIFormAdviseSink::OnChange** method to notify the form about a change in a viewer's status.</span></span> <span data-ttu-id="80b16-130">Normalmente, el único cambio es establecer o borrar la marca VCSTATUS_NEXT o VCSTATUS_PREVIOUS en función de la presencia o ausencia de un mensaje siguiente o anterior en el visor.</span><span class="sxs-lookup"><span data-stu-id="80b16-130">Usually, the only change is setting or clearing the VCSTATUS_NEXT or VCSTATUS_PREVIOUS flag based on the presence or absence of a next or previous message in the viewer.</span></span> <span data-ttu-id="80b16-131">En consecuencia, el objeto de formulario habilita o deshabilita las acciones siguientes o anteriores que admita.</span><span class="sxs-lookup"><span data-stu-id="80b16-131">Accordingly, the form object then enables or disables any next or previous actions it supports.</span></span> 
  
<span data-ttu-id="80b16-132">La configuración de VCSTATUS_MODAL y VCSTATUS_INTERACTIVE no pueden cambiar en un contexto de vista después de su creación.</span><span class="sxs-lookup"><span data-stu-id="80b16-132">The settings of VCSTATUS_MODAL and VCSTATUS_INTERACTIVE cannot change in a view context after it has been created.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="80b16-133">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="80b16-133">Notes to implementers</span></span>

<span data-ttu-id="80b16-134">La implementación específica de este método depende completamente de los detalles del formulario.</span><span class="sxs-lookup"><span data-stu-id="80b16-134">The specific implementation of this method is completely dependent on the specifics of the form.</span></span> <span data-ttu-id="80b16-135">La mayoría de los objetos de formulario usan este método para cambiar su interfaz de usuario (por ejemplo, para habilitar o deshabilitar comandos de menú o botones para que coincidan con el parámetro de indicadores de estado del visor).</span><span class="sxs-lookup"><span data-stu-id="80b16-135">Most form objects use this method to change their user interface (for example, to enable or disable menu commands or buttons to match the viewer status flags parameter).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="80b16-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="80b16-136">See also</span></span>



[<span data-ttu-id="80b16-137">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="80b16-137">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="80b16-138">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="80b16-138">IMAPIFormAdviseSink : IUnknown</span></span>](imapiformadvisesinkiunknown.md)

