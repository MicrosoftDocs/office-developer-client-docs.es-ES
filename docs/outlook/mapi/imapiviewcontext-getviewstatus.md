---
title: IMAPIViewContextGetViewStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetViewStatus
api_type:
- COM
ms.assetid: 2e5ec914-7171-41ce-a6fe-78dd80ac32ff
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bb8699746b3f4207ee70edd4e56d0ec6041beac2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351180"
---
# <a name="imapiviewcontextgetviewstatus"></a><span data-ttu-id="d8157-103">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="d8157-103">IMAPIViewContext::GetViewStatus</span></span>

  
  
<span data-ttu-id="d8157-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8157-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8157-105">Recupera el estado actual del visor.</span><span class="sxs-lookup"><span data-stu-id="d8157-105">Retrieves the current viewer status.</span></span> 
  
```cpp
HRESULT GetViewStatus(
ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a><span data-ttu-id="d8157-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="d8157-106">Parameters</span></span>

 <span data-ttu-id="d8157-107">_lpulStatus_</span><span class="sxs-lookup"><span data-stu-id="d8157-107">_lpulStatus_</span></span>
  
> <span data-ttu-id="d8157-108">contempla Puntero a una máscara de máscara de indicadores que proporciona el estado del visor.</span><span class="sxs-lookup"><span data-stu-id="d8157-108">[out] Pointer to a bitmask of flags providing the status of the viewer.</span></span> <span data-ttu-id="d8157-109">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="d8157-109">The following flags can be set:</span></span>
    
<span data-ttu-id="d8157-110">VCSTATUS_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="d8157-110">VCSTATUS_CATEGORY</span></span> 
  
> <span data-ttu-id="d8157-111">Hay un mensaje siguiente o anterior en otra categoría.</span><span class="sxs-lookup"><span data-stu-id="d8157-111">There is a next or previous message in another category.</span></span> 
    
<span data-ttu-id="d8157-112">VCSTATUS_DELETE</span><span class="sxs-lookup"><span data-stu-id="d8157-112">VCSTATUS_DELETE</span></span> 
  
> <span data-ttu-id="d8157-113">El formulario permite quitar los mensajes.</span><span class="sxs-lookup"><span data-stu-id="d8157-113">The form allows messages to be removed.</span></span> 
    
<span data-ttu-id="d8157-114">VCSTATUS_INTERACTIVE</span><span class="sxs-lookup"><span data-stu-id="d8157-114">VCSTATUS_INTERACTIVE</span></span> 
  
> <span data-ttu-id="d8157-115">El formulario debe mostrar una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="d8157-115">The form should display a user interface.</span></span> <span data-ttu-id="d8157-116">Si no se establece esta marca, el formulario debe suprimir la visualización de una interfaz de usuario incluso en respuesta a un verbo que normalmente hace que se muestre una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="d8157-116">If this flag is not set, the form should suppress displaying a user interface even in response to a verb that usually causes a user interface to be displayed.</span></span> 
    
<span data-ttu-id="d8157-117">VCSTATUS_MODAL</span><span class="sxs-lookup"><span data-stu-id="d8157-117">VCSTATUS_MODAL</span></span> 
  
> <span data-ttu-id="d8157-118">El formulario es modal para el visor.</span><span class="sxs-lookup"><span data-stu-id="d8157-118">The form is modal to the viewer.</span></span> 
    
<span data-ttu-id="d8157-119">VCSTATUS_NEXT</span><span class="sxs-lookup"><span data-stu-id="d8157-119">VCSTATUS_NEXT</span></span> 
  
> <span data-ttu-id="d8157-120">Hay un mensaje siguiente en la vista.</span><span class="sxs-lookup"><span data-stu-id="d8157-120">There is a next message in the view.</span></span> 
    
<span data-ttu-id="d8157-121">VCSTATUS_PREV</span><span class="sxs-lookup"><span data-stu-id="d8157-121">VCSTATUS_PREV</span></span> 
  
> <span data-ttu-id="d8157-122">Hay un mensaje anterior en la vista.</span><span class="sxs-lookup"><span data-stu-id="d8157-122">There is a previous message in the view.</span></span> 
    
<span data-ttu-id="d8157-123">VCSTATUS_READONLY</span><span class="sxs-lookup"><span data-stu-id="d8157-123">VCSTATUS_READONLY</span></span> 
  
> <span data-ttu-id="d8157-124">El mensaje debe abrirse en modo de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d8157-124">The message is to be opened in read-only mode.</span></span> <span data-ttu-id="d8157-125">Las operaciones de eliminar, enviar y mover deben estar deshabilitadas.</span><span class="sxs-lookup"><span data-stu-id="d8157-125">Delete, submit, and move operations should be disabled.</span></span> 
    
<span data-ttu-id="d8157-126">VCSTATUS_UNREAD</span><span class="sxs-lookup"><span data-stu-id="d8157-126">VCSTATUS_UNREAD</span></span> 
  
> <span data-ttu-id="d8157-127">Hay un mensaje no leído siguiente o anterior en la vista.</span><span class="sxs-lookup"><span data-stu-id="d8157-127">There is a next or previous unread message in the view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d8157-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d8157-128">Return value</span></span>

<span data-ttu-id="d8157-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="d8157-129">S_OK</span></span> 
  
> <span data-ttu-id="d8157-130">El estado del visor se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="d8157-130">The viewer's status was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d8157-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d8157-131">Remarks</span></span>

<span data-ttu-id="d8157-132">Los objetos de formulario llaman al método **IMAPIViewContext:: GetViewStatus** para determinar si hay más mensajes que se van a activar en una vista de formulario en una o ambas direcciones, es decir, en la dirección en la que un comando **siguiente** activa los mensajes, en el Dirección en la que un comando **anterior** activa los mensajes o en ambas direcciones.</span><span class="sxs-lookup"><span data-stu-id="d8157-132">Form objects call the **IMAPIViewContext::GetViewStatus** method to determine whether there are more messages to be activated in a form view in either or both directions that is, in the direction in which a **Next** command activates messages, in the direction in which a **Previous** command activates messages, or in both directions.</span></span> <span data-ttu-id="d8157-133">El valor al que señala el parámetro _lpulStatus_ se usa para determinar si las marcas VCSTATUS_NEXT y VCSTATUS_PREV son válidas para [IMAPIViewContext:: ActivateNext](imapiviewcontext-activatenext.md).</span><span class="sxs-lookup"><span data-stu-id="d8157-133">The value pointed to by the  _lpulStatus_ parameter is used to determine whether the VCSTATUS_NEXT and VCSTATUS_PREV flags are valid for [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md).</span></span> <span data-ttu-id="d8157-134">Si se establece la marca VCSTATUS_DELETE, pero no la marca VCSTATUS_READONLY, el mensaje se puede eliminar mediante el método [IMAPIMessageSite::D eletemessage](imapimessagesite-deletemessage.md) .</span><span class="sxs-lookup"><span data-stu-id="d8157-134">If the VCSTATUS_DELETE flag is set, but not the VCSTATUS_READONLY flag, then the message can be deleted using the [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) method.</span></span> 
  
<span data-ttu-id="d8157-135">Por lo general, los formularios deshabilitan botones y comandos de menú si no son válidos para el contexto del visor.</span><span class="sxs-lookup"><span data-stu-id="d8157-135">Typically, forms disable menu commands and buttons if they are not valid for the viewer's context.</span></span> <span data-ttu-id="d8157-136">Un visor puede enviar una alerta de un formulario a un cambio de estado llamando a su método [IMAPIFormAdviseSink:: onchange](imapiformadvisesink-onchange.md) .</span><span class="sxs-lookup"><span data-stu-id="d8157-136">A viewer can alert a form to a change in status by calling its [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) method.</span></span> 
  
<span data-ttu-id="d8157-137">La marca VCSTATUS_MODAL se establece si el formulario tiene que ser modal a la ventana cuyo controlador se pasa en la anterior [IMAPIForm::D llamada overb](imapiform-doverb.md) .</span><span class="sxs-lookup"><span data-stu-id="d8157-137">The VCSTATUS_MODAL flag is set if the form must be modal to the window whose handle is passed in the earlier [IMAPIForm::DoVerb](imapiform-doverb.md) call.</span></span> <span data-ttu-id="d8157-138">Si se establece VCSTATUS_MODAL, el formulario puede usar el subproceso en el que se realizó la llamada a **doverb** hasta que se cierre el formulario.</span><span class="sxs-lookup"><span data-stu-id="d8157-138">If VCSTATUS_MODAL is set, the form can use the thread on which the **DoVerb** call was made until the form closes.</span></span> <span data-ttu-id="d8157-139">Si no se establece VCSTATUS_MODAL, el formulario no debe ser modal a esta ventana y no debe usar el subproceso.</span><span class="sxs-lookup"><span data-stu-id="d8157-139">If VCSTATUS_MODAL is not set, the form should not be modal to this window and must not use the thread.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d8157-140">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d8157-140">MFCMAPI reference</span></span>

<span data-ttu-id="d8157-141">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="d8157-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d8157-142">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="d8157-142">**File**</span></span>|<span data-ttu-id="d8157-143">**Función**</span><span class="sxs-lookup"><span data-stu-id="d8157-143">**Function**</span></span>|<span data-ttu-id="d8157-144">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="d8157-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d8157-145">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="d8157-145">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="d8157-146">CMyMAPIFormViewer:: GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="d8157-146">CMyMAPIFormViewer::GetViewStatus</span></span>  <br/> |<span data-ttu-id="d8157-147">MFCMAPI implementa el método **IMAPIViewContext:: GetViewStatus** en esta función.</span><span class="sxs-lookup"><span data-stu-id="d8157-147">MFCMAPI implements the **IMAPIViewContext::GetViewStatus** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d8157-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8157-148">See also</span></span>



[<span data-ttu-id="d8157-149">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="d8157-149">IMAPIMessageSite::GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md)
  
[<span data-ttu-id="d8157-150">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d8157-150">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)


[<span data-ttu-id="d8157-151">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="d8157-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

