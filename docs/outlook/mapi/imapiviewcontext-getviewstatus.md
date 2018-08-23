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
ms.openlocfilehash: 992d51526c45334f6db3738e36994f4bb9c07c6e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572259"
---
# <a name="imapiviewcontextgetviewstatus"></a><span data-ttu-id="8a2cc-103">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="8a2cc-103">IMAPIViewContext::GetViewStatus</span></span>

  
  
<span data-ttu-id="8a2cc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a2cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8a2cc-105">Recupera el estado actual del Visor.</span><span class="sxs-lookup"><span data-stu-id="8a2cc-105">Retrieves the current viewer status.</span></span> 
  
```cpp
HRESULT GetViewStatus(
ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a><span data-ttu-id="8a2cc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8a2cc-106">Parameters</span></span>

 <span data-ttu-id="8a2cc-107">_lpulStatus_</span><span class="sxs-lookup"><span data-stu-id="8a2cc-107">_lpulStatus_</span></span>
  
> <span data-ttu-id="8a2cc-108">[out] Puntero a una máscara de bits de marcadores que indica el estado del Visor del.</span><span class="sxs-lookup"><span data-stu-id="8a2cc-108">[out] Pointer to a bitmask of flags providing the status of the viewer.</span></span> <span data-ttu-id="8a2cc-109">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="8a2cc-109">The following flags can be set:</span></span>
    
<span data-ttu-id="8a2cc-110">VCSTATUS_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="8a2cc-110">VCSTATUS_CATEGORY</span></span> 
  
> <span data-ttu-id="8a2cc-111">Hay un mensaje siguiente o anterior en otra categoría.</span><span class="sxs-lookup"><span data-stu-id="8a2cc-111">There is a next or previous message in another category.</span></span> 
    
<span data-ttu-id="8a2cc-112">VCSTATUS_DELETE</span><span class="sxs-lookup"><span data-stu-id="8a2cc-112">VCSTATUS_DELETE</span></span> 
  
> <span data-ttu-id="8a2cc-113">El formulario permite que los mensajes que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="8a2cc-113">The form allows messages to be removed.</span></span> 
    
<span data-ttu-id="8a2cc-114">VCSTATUS_INTERACTIVE</span><span class="sxs-lookup"><span data-stu-id="8a2cc-114">VCSTATUS_INTERACTIVE</span></span> 
  
> <span data-ttu-id="8a2cc-115">El formulario debe mostrar una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="8a2cc-115">The form should display a user interface.</span></span> <span data-ttu-id="8a2cc-116">Si no se establece este indicador, el formulario debe suprimir mostrar la interfaz de usuario incluso en respuesta a un verbo que normalmente hace que una interfaz de usuario que se mostrará.</span><span class="sxs-lookup"><span data-stu-id="8a2cc-116">If this flag is not set, the form should suppress displaying a user interface even in response to a verb that usually causes a user interface to be displayed.</span></span> 
    
<span data-ttu-id="8a2cc-117">VCSTATUS_MODAL</span><span class="sxs-lookup"><span data-stu-id="8a2cc-117">VCSTATUS_MODAL</span></span> 
  
> <span data-ttu-id="8a2cc-118">El formulario es modal al Visor.</span><span class="sxs-lookup"><span data-stu-id="8a2cc-118">The form is modal to the viewer.</span></span> 
    
<span data-ttu-id="8a2cc-119">VCSTATUS_NEXT</span><span class="sxs-lookup"><span data-stu-id="8a2cc-119">VCSTATUS_NEXT</span></span> 
  
> <span data-ttu-id="8a2cc-120">Hay un mensaje siguiente en la vista.</span><span class="sxs-lookup"><span data-stu-id="8a2cc-120">There is a next message in the view.</span></span> 
    
<span data-ttu-id="8a2cc-121">VCSTATUS_PREV</span><span class="sxs-lookup"><span data-stu-id="8a2cc-121">VCSTATUS_PREV</span></span> 
  
> <span data-ttu-id="8a2cc-122">Hay un mensaje anterior en la vista.</span><span class="sxs-lookup"><span data-stu-id="8a2cc-122">There is a previous message in the view.</span></span> 
    
<span data-ttu-id="8a2cc-123">VCSTATUS_READONLY</span><span class="sxs-lookup"><span data-stu-id="8a2cc-123">VCSTATUS_READONLY</span></span> 
  
> <span data-ttu-id="8a2cc-124">El mensaje es para abrirse en modo de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="8a2cc-124">The message is to be opened in read-only mode.</span></span> <span data-ttu-id="8a2cc-125">Eliminar, enviar y mover las operaciones deben deshabilitarse.</span><span class="sxs-lookup"><span data-stu-id="8a2cc-125">Delete, submit, and move operations should be disabled.</span></span> 
    
<span data-ttu-id="8a2cc-126">VCSTATUS_UNREAD</span><span class="sxs-lookup"><span data-stu-id="8a2cc-126">VCSTATUS_UNREAD</span></span> 
  
> <span data-ttu-id="8a2cc-127">Hay un mensaje no leído siguiente o anterior en la vista.</span><span class="sxs-lookup"><span data-stu-id="8a2cc-127">There is a next or previous unread message in the view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8a2cc-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8a2cc-128">Return value</span></span>

<span data-ttu-id="8a2cc-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="8a2cc-129">S_OK</span></span> 
  
> <span data-ttu-id="8a2cc-130">Estado del Visor se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="8a2cc-130">The viewer's status was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8a2cc-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8a2cc-131">Remarks</span></span>

<span data-ttu-id="8a2cc-132">Objetos de formulario, llame al método **IMAPIViewContext::GetViewStatus** para determinar si hay más mensajes que se activará en una vista de formulario en cualquiera o ambas direcciones es decir, en la dirección en la que se activa un comando **a continuación** los mensajes, en el dirección en la que un comando **anterior** activa de los mensajes, o en ambas direcciones.</span><span class="sxs-lookup"><span data-stu-id="8a2cc-132">Form objects call the **IMAPIViewContext::GetViewStatus** method to determine whether there are more messages to be activated in a form view in either or both directions that is, in the direction in which a **Next** command activates messages, in the direction in which a **Previous** command activates messages, or in both directions.</span></span> <span data-ttu-id="8a2cc-133">El valor al que señala el parámetro _lpulStatus_ se usa para determinar si los indicadores VCSTATUS_NEXT y VCSTATUS_PREV son válidos para [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md).</span><span class="sxs-lookup"><span data-stu-id="8a2cc-133">The value pointed to by the  _lpulStatus_ parameter is used to determine whether the VCSTATUS_NEXT and VCSTATUS_PREV flags are valid for [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md).</span></span> <span data-ttu-id="8a2cc-134">Si el indicador VCSTATUS_DELETE es set, pero no la marca VCSTATUS_READONLY, a continuación, el mensaje se puede eliminar mediante el método [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) .</span><span class="sxs-lookup"><span data-stu-id="8a2cc-134">If the VCSTATUS_DELETE flag is set, but not the VCSTATUS_READONLY flag, then the message can be deleted using the [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) method.</span></span> 
  
<span data-ttu-id="8a2cc-135">Normalmente, formularios deshabilitación botones y comandos de menú si no son válidos para el contexto del Visor.</span><span class="sxs-lookup"><span data-stu-id="8a2cc-135">Typically, forms disable menu commands and buttons if they are not valid for the viewer's context.</span></span> <span data-ttu-id="8a2cc-136">Un visor puede un formulario a un cambio en el estado de alerta llamando a su método [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) .</span><span class="sxs-lookup"><span data-stu-id="8a2cc-136">A viewer can alert a form to a change in status by calling its [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) method.</span></span> 
  
<span data-ttu-id="8a2cc-137">Se establece la marca VCSTATUS_MODAL si el formulario debe ser modal a la ventana cuyo controlador se pasa en la llamada de [IMAPIForm::DoVerb](imapiform-doverb.md) anterior.</span><span class="sxs-lookup"><span data-stu-id="8a2cc-137">The VCSTATUS_MODAL flag is set if the form must be modal to the window whose handle is passed in the earlier [IMAPIForm::DoVerb](imapiform-doverb.md) call.</span></span> <span data-ttu-id="8a2cc-138">Si se establece VCSTATUS_MODAL, el formulario puede usar el subproceso en el que se realizó la llamada **DoVerb** hasta que se cierra el formulario.</span><span class="sxs-lookup"><span data-stu-id="8a2cc-138">If VCSTATUS_MODAL is set, the form can use the thread on which the **DoVerb** call was made until the form closes.</span></span> <span data-ttu-id="8a2cc-139">Si VCSTATUS_MODAL no está establecido, el formulario no debe ser modal a esta ventana y no debe usar el subproceso.</span><span class="sxs-lookup"><span data-stu-id="8a2cc-139">If VCSTATUS_MODAL is not set, the form should not be modal to this window and must not use the thread.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8a2cc-140">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="8a2cc-140">MFCMAPI reference</span></span>

<span data-ttu-id="8a2cc-141">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="8a2cc-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8a2cc-142">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="8a2cc-142">**File**</span></span>|<span data-ttu-id="8a2cc-143">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="8a2cc-143">**Function**</span></span>|<span data-ttu-id="8a2cc-144">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="8a2cc-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8a2cc-145">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="8a2cc-145">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="8a2cc-146">CMyMAPIFormViewer::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="8a2cc-146">CMyMAPIFormViewer::GetViewStatus</span></span>  <br/> |<span data-ttu-id="8a2cc-147">MFCMAPI implementa el método **IMAPIViewContext::GetViewStatus** en esta función.</span><span class="sxs-lookup"><span data-stu-id="8a2cc-147">MFCMAPI implements the **IMAPIViewContext::GetViewStatus** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8a2cc-148">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="8a2cc-148">See also</span></span>



[<span data-ttu-id="8a2cc-149">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="8a2cc-149">IMAPIMessageSite::GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md)
  
[<span data-ttu-id="8a2cc-150">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8a2cc-150">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)


[<span data-ttu-id="8a2cc-151">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="8a2cc-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

