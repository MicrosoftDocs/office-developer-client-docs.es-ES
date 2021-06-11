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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429022"
---
# <a name="imapiviewcontextgetviewstatus"></a><span data-ttu-id="106ae-103">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="106ae-103">IMAPIViewContext::GetViewStatus</span></span>

  
  
<span data-ttu-id="106ae-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="106ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="106ae-105">Recupera el estado actual del visor.</span><span class="sxs-lookup"><span data-stu-id="106ae-105">Retrieves the current viewer status.</span></span> 
  
```cpp
HRESULT GetViewStatus(
ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a><span data-ttu-id="106ae-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="106ae-106">Parameters</span></span>

 <span data-ttu-id="106ae-107">_lpulStatus_</span><span class="sxs-lookup"><span data-stu-id="106ae-107">_lpulStatus_</span></span>
  
> <span data-ttu-id="106ae-108">[salida] Puntero a una máscara de bits de marcas que proporciona el estado del visor.</span><span class="sxs-lookup"><span data-stu-id="106ae-108">[out] Pointer to a bitmask of flags providing the status of the viewer.</span></span> <span data-ttu-id="106ae-109">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="106ae-109">The following flags can be set:</span></span>
    
<span data-ttu-id="106ae-110">VCSTATUS_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="106ae-110">VCSTATUS_CATEGORY</span></span> 
  
> <span data-ttu-id="106ae-111">Hay un mensaje siguiente o anterior en otra categoría.</span><span class="sxs-lookup"><span data-stu-id="106ae-111">There is a next or previous message in another category.</span></span> 
    
<span data-ttu-id="106ae-112">VCSTATUS_DELETE</span><span class="sxs-lookup"><span data-stu-id="106ae-112">VCSTATUS_DELETE</span></span> 
  
> <span data-ttu-id="106ae-113">El formulario permite quitar mensajes.</span><span class="sxs-lookup"><span data-stu-id="106ae-113">The form allows messages to be removed.</span></span> 
    
<span data-ttu-id="106ae-114">VCSTATUS_INTERACTIVE</span><span class="sxs-lookup"><span data-stu-id="106ae-114">VCSTATUS_INTERACTIVE</span></span> 
  
> <span data-ttu-id="106ae-115">El formulario debe mostrar una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="106ae-115">The form should display a user interface.</span></span> <span data-ttu-id="106ae-116">Si no se establece esta marca, el formulario debe suprimir la visualización de una interfaz de usuario incluso en respuesta a un verbo que normalmente hace que se muestre una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="106ae-116">If this flag is not set, the form should suppress displaying a user interface even in response to a verb that usually causes a user interface to be displayed.</span></span> 
    
<span data-ttu-id="106ae-117">VCSTATUS_MODAL</span><span class="sxs-lookup"><span data-stu-id="106ae-117">VCSTATUS_MODAL</span></span> 
  
> <span data-ttu-id="106ae-118">El formulario es modal para el visor.</span><span class="sxs-lookup"><span data-stu-id="106ae-118">The form is modal to the viewer.</span></span> 
    
<span data-ttu-id="106ae-119">VCSTATUS_NEXT</span><span class="sxs-lookup"><span data-stu-id="106ae-119">VCSTATUS_NEXT</span></span> 
  
> <span data-ttu-id="106ae-120">Hay un siguiente mensaje en la vista.</span><span class="sxs-lookup"><span data-stu-id="106ae-120">There is a next message in the view.</span></span> 
    
<span data-ttu-id="106ae-121">VCSTATUS_PREV</span><span class="sxs-lookup"><span data-stu-id="106ae-121">VCSTATUS_PREV</span></span> 
  
> <span data-ttu-id="106ae-122">Hay un mensaje anterior en la vista.</span><span class="sxs-lookup"><span data-stu-id="106ae-122">There is a previous message in the view.</span></span> 
    
<span data-ttu-id="106ae-123">VCSTATUS_READONLY</span><span class="sxs-lookup"><span data-stu-id="106ae-123">VCSTATUS_READONLY</span></span> 
  
> <span data-ttu-id="106ae-124">El mensaje se abrirá en modo de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="106ae-124">The message is to be opened in read-only mode.</span></span> <span data-ttu-id="106ae-125">Las operaciones eliminar, enviar y mover deben deshabilitarse.</span><span class="sxs-lookup"><span data-stu-id="106ae-125">Delete, submit, and move operations should be disabled.</span></span> 
    
<span data-ttu-id="106ae-126">VCSTATUS_UNREAD</span><span class="sxs-lookup"><span data-stu-id="106ae-126">VCSTATUS_UNREAD</span></span> 
  
> <span data-ttu-id="106ae-127">Hay un mensaje no leído siguiente o anterior en la vista.</span><span class="sxs-lookup"><span data-stu-id="106ae-127">There is a next or previous unread message in the view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="106ae-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="106ae-128">Return value</span></span>

<span data-ttu-id="106ae-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="106ae-129">S_OK</span></span> 
  
> <span data-ttu-id="106ae-130">El estado del visor se ha devuelto correctamente.</span><span class="sxs-lookup"><span data-stu-id="106ae-130">The viewer's status was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="106ae-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="106ae-131">Remarks</span></span>

<span data-ttu-id="106ae-132">Los objetos Form llaman al método **IMAPIViewContext::GetViewStatus** para determinar si hay más mensajes que se activarán en  una vista de formulario en una o en ambas direcciones, es decir, en la dirección en que un comando Next activa los mensajes, en la dirección en la que un comando **Previous** activa mensajes o en ambas direcciones.</span><span class="sxs-lookup"><span data-stu-id="106ae-132">Form objects call the **IMAPIViewContext::GetViewStatus** method to determine whether there are more messages to be activated in a form view in either or both directions that is, in the direction in which a **Next** command activates messages, in the direction in which a **Previous** command activates messages, or in both directions.</span></span> <span data-ttu-id="106ae-133">El valor al que apunta el parámetro  _lpulStatus_ se usa para determinar si las marcas VCSTATUS_NEXT y VCSTATUS_PREV son válidas para [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md).</span><span class="sxs-lookup"><span data-stu-id="106ae-133">The value pointed to by the  _lpulStatus_ parameter is used to determine whether the VCSTATUS_NEXT and VCSTATUS_PREV flags are valid for [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md).</span></span> <span data-ttu-id="106ae-134">Si la marca VCSTATUS_DELETE está establecida, pero no la marca VCSTATUS_READONLY, el mensaje se puede eliminar mediante el método [IMAPIMessageSite::D eleteMessage.](imapimessagesite-deletemessage.md)</span><span class="sxs-lookup"><span data-stu-id="106ae-134">If the VCSTATUS_DELETE flag is set, but not the VCSTATUS_READONLY flag, then the message can be deleted using the [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) method.</span></span> 
  
<span data-ttu-id="106ae-135">Normalmente, los formularios deshabilitan los comandos de menú y los botones si no son válidos para el contexto del visor.</span><span class="sxs-lookup"><span data-stu-id="106ae-135">Typically, forms disable menu commands and buttons if they are not valid for the viewer's context.</span></span> <span data-ttu-id="106ae-136">Un visor puede alertar a un formulario de un cambio de estado llamando a su [método IMAPIFormAdviseSink::OnChange.](imapiformadvisesink-onchange.md)</span><span class="sxs-lookup"><span data-stu-id="106ae-136">A viewer can alert a form to a change in status by calling its [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) method.</span></span> 
  
<span data-ttu-id="106ae-137">La VCSTATUS_MODAL se establece si el formulario debe ser modal a la ventana cuyo identificador se pasa en la llamada [imapiform::D oVerb](imapiform-doverb.md) anterior.</span><span class="sxs-lookup"><span data-stu-id="106ae-137">The VCSTATUS_MODAL flag is set if the form must be modal to the window whose handle is passed in the earlier [IMAPIForm::DoVerb](imapiform-doverb.md) call.</span></span> <span data-ttu-id="106ae-138">Si VCSTATUS_MODAL se establece, el formulario puede usar el subproceso en el que se realizó la llamada **a DoVerb** hasta que se cierre el formulario.</span><span class="sxs-lookup"><span data-stu-id="106ae-138">If VCSTATUS_MODAL is set, the form can use the thread on which the **DoVerb** call was made until the form closes.</span></span> <span data-ttu-id="106ae-139">Si VCSTATUS_MODAL está establecido, el formulario no debe ser modal en esta ventana y no debe usar el subproceso.</span><span class="sxs-lookup"><span data-stu-id="106ae-139">If VCSTATUS_MODAL is not set, the form should not be modal to this window and must not use the thread.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="106ae-140">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="106ae-140">MFCMAPI reference</span></span>

<span data-ttu-id="106ae-141">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="106ae-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="106ae-142">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="106ae-142">**File**</span></span>|<span data-ttu-id="106ae-143">**Función**</span><span class="sxs-lookup"><span data-stu-id="106ae-143">**Function**</span></span>|<span data-ttu-id="106ae-144">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="106ae-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="106ae-145">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="106ae-145">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="106ae-146">CMyMAPIFormViewer::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="106ae-146">CMyMAPIFormViewer::GetViewStatus</span></span>  <br/> |<span data-ttu-id="106ae-147">MFCMAPI implementa el método **IMAPIViewContext::GetViewStatus** en esta función.</span><span class="sxs-lookup"><span data-stu-id="106ae-147">MFCMAPI implements the **IMAPIViewContext::GetViewStatus** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="106ae-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="106ae-148">See also</span></span>



[<span data-ttu-id="106ae-149">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="106ae-149">IMAPIMessageSite::GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md)
  
[<span data-ttu-id="106ae-150">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="106ae-150">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)


[<span data-ttu-id="106ae-151">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="106ae-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

