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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 01bdf6cdde864d1ea4ed19dfeb01a96236dc9c63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817268"
---
# <a name="imapiformadvisesinkonchange"></a><span data-ttu-id="57c0c-103">IMAPIFormAdviseSink::OnChange</span><span class="sxs-lookup"><span data-stu-id="57c0c-103">IMAPIFormAdviseSink::OnChange</span></span>

  
  
<span data-ttu-id="57c0c-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="57c0c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="57c0c-105">Indica que se ha producido un cambio en el estado del Visor del formulario.</span><span class="sxs-lookup"><span data-stu-id="57c0c-105">Indicates that a change has occurred in the status of the form viewer.</span></span> 
  
```cpp
HRESULT OnChange(
  ULONG ulDir
);
```

## <a name="parameters"></a><span data-ttu-id="57c0c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="57c0c-106">Parameters</span></span>

 <span data-ttu-id="57c0c-107">_ulDir_</span><span class="sxs-lookup"><span data-stu-id="57c0c-107">_ulDir_</span></span>
  
> <span data-ttu-id="57c0c-108">[entrada] Una máscara de bits de indicadores que proporciona información sobre el cambio que se ha producido en el Visor y la respuesta esperada en el formulario.</span><span class="sxs-lookup"><span data-stu-id="57c0c-108">[in] A bitmask of flags that provides information about the change that has occurred in the viewer and the expected response in the form.</span></span> <span data-ttu-id="57c0c-109">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="57c0c-109">The following flags can be set:</span></span>
    
<span data-ttu-id="57c0c-110">VCSTATUS_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="57c0c-110">VCSTATUS_CATEGORY</span></span> 
  
> <span data-ttu-id="57c0c-111">Hay un mensaje siguiente o anterior en otra categoría.</span><span class="sxs-lookup"><span data-stu-id="57c0c-111">There is a next or previous message in another category.</span></span> 
    
<span data-ttu-id="57c0c-112">VCSTATUS_INTERACTIVE</span><span class="sxs-lookup"><span data-stu-id="57c0c-112">VCSTATUS_INTERACTIVE</span></span> 
  
> <span data-ttu-id="57c0c-113">El formulario debe mostrar una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="57c0c-113">The form should display a user interface.</span></span> <span data-ttu-id="57c0c-114">Si no se establece este indicador, el formulario debe suprimir mostrar la interfaz de usuario, incluso en respuesta a un verbo que normalmente hace que una interfaz de usuario que se mostrará.</span><span class="sxs-lookup"><span data-stu-id="57c0c-114">If this flag is not set, the form should suppress displaying a user interface, even in response to a verb that usually causes a user interface to be displayed.</span></span> 
    
<span data-ttu-id="57c0c-115">VCSTATUS_MODAL</span><span class="sxs-lookup"><span data-stu-id="57c0c-115">VCSTATUS_MODAL</span></span> 
  
> <span data-ttu-id="57c0c-116">El formulario es modal en el Visor de formulario.</span><span class="sxs-lookup"><span data-stu-id="57c0c-116">The form is to be modal to the form viewer.</span></span> 
    
<span data-ttu-id="57c0c-117">VCSTATUS_NEXT</span><span class="sxs-lookup"><span data-stu-id="57c0c-117">VCSTATUS_NEXT</span></span> 
  
> <span data-ttu-id="57c0c-118">Hay un mensaje siguiente en el Visor de formulario.</span><span class="sxs-lookup"><span data-stu-id="57c0c-118">There is a next message in the form viewer.</span></span> 
    
<span data-ttu-id="57c0c-119">VCSTATUS_PREV</span><span class="sxs-lookup"><span data-stu-id="57c0c-119">VCSTATUS_PREV</span></span> 
  
> <span data-ttu-id="57c0c-120">Hay un mensaje anterior en el Visor de formulario.</span><span class="sxs-lookup"><span data-stu-id="57c0c-120">There is a previous message in the form viewer.</span></span> 
    
<span data-ttu-id="57c0c-121">VCSTATUS_READONLY</span><span class="sxs-lookup"><span data-stu-id="57c0c-121">VCSTATUS_READONLY</span></span> 
  
> <span data-ttu-id="57c0c-122">Eliminar, enviar y mover las operaciones deben deshabilitarse.</span><span class="sxs-lookup"><span data-stu-id="57c0c-122">Delete, submit, and move operations should be disabled.</span></span> 
    
<span data-ttu-id="57c0c-123">VCSTATUS_UNREAD</span><span class="sxs-lookup"><span data-stu-id="57c0c-123">VCSTATUS_UNREAD</span></span> 
  
> <span data-ttu-id="57c0c-124">Hay un mensaje no leído siguiente o anterior en el Visor de formulario.</span><span class="sxs-lookup"><span data-stu-id="57c0c-124">There is a next or previous unread message in the form viewer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="57c0c-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="57c0c-125">Return value</span></span>

<span data-ttu-id="57c0c-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="57c0c-126">S_OK</span></span> 
  
> <span data-ttu-id="57c0c-127">La notificación fue correcta.</span><span class="sxs-lookup"><span data-stu-id="57c0c-127">The notification was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="57c0c-128">Notas</span><span class="sxs-lookup"><span data-stu-id="57c0c-128">Remarks</span></span>

<span data-ttu-id="57c0c-129">Visores de formulario llamar al método **IMAPIFormAdviseSink::OnChange** para notificar el formulario acerca de un cambio en el estado de un visor.</span><span class="sxs-lookup"><span data-stu-id="57c0c-129">Form viewers call the **IMAPIFormAdviseSink::OnChange** method to notify the form about a change in a viewer's status.</span></span> <span data-ttu-id="57c0c-130">Normalmente, el único cambio es activando o desactivando la marca VCSTATUS_NEXT o VCSTATUS_PREVIOUS en función de la presencia o ausencia de un mensaje siguiente o anterior en el Visor.</span><span class="sxs-lookup"><span data-stu-id="57c0c-130">Usually, the only change is setting or clearing the VCSTATUS_NEXT or VCSTATUS_PREVIOUS flag based on the presence or absence of a next or previous message in the viewer.</span></span> <span data-ttu-id="57c0c-131">Por lo tanto, el objeto de formulario, a continuación, habilita o deshabilita cualquier acciones siguiente o anteriores que admite.</span><span class="sxs-lookup"><span data-stu-id="57c0c-131">Accordingly, the form object then enables or disables any next or previous actions it supports.</span></span> 
  
<span data-ttu-id="57c0c-132">No se puede cambiar la configuración de VCSTATUS_MODAL y VCSTATUS_INTERACTIVE en un contexto de vista después de que se han creado.</span><span class="sxs-lookup"><span data-stu-id="57c0c-132">The settings of VCSTATUS_MODAL and VCSTATUS_INTERACTIVE cannot change in a view context after it has been created.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="57c0c-133">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="57c0c-133">Notes to implementers</span></span>

<span data-ttu-id="57c0c-134">La implementación específica de este método depende completamente de las características específicas del formulario.</span><span class="sxs-lookup"><span data-stu-id="57c0c-134">The specific implementation of this method is completely dependent on the specifics of the form.</span></span> <span data-ttu-id="57c0c-135">La mayoría de los objetos de formulario use este método para cambiar la interfaz de usuario (por ejemplo, para habilitar o deshabilitar comandos de menú o botones para que coincida con el parámetro de indicadores de estado de Visor).</span><span class="sxs-lookup"><span data-stu-id="57c0c-135">Most form objects use this method to change their user interface (for example, to enable or disable menu commands or buttons to match the viewer status flags parameter).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="57c0c-136">Ver también</span><span class="sxs-lookup"><span data-stu-id="57c0c-136">See also</span></span>



[<span data-ttu-id="57c0c-137">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="57c0c-137">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="57c0c-138">IMAPIFormAdviseSink: IUnknown</span><span class="sxs-lookup"><span data-stu-id="57c0c-138">IMAPIFormAdviseSink : IUnknown</span></span>](imapiformadvisesinkiunknown.md)

