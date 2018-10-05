---
title: IMAPIFormDoVerb
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.DoVerb
api_type:
- COM
ms.assetid: 8b582571-b448-4476-91d9-4cc94dbec710
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 60a8c89afe0d70a1737c6ce694c66359fd6aae4f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398097"
---
# <a name="imapiformdoverb"></a><span data-ttu-id="4d956-103">IMAPIForm::DoVerb</span><span class="sxs-lookup"><span data-stu-id="4d956-103">IMAPIForm::DoVerb</span></span>

  
  
<span data-ttu-id="4d956-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d956-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d956-105">Las solicitudes que el formulario realiza tareas con independencia de se asocia a un verbo específico.</span><span class="sxs-lookup"><span data-stu-id="4d956-105">Requests that the form perform whatever tasks it associates with a specific verb.</span></span>
  
```cpp
HRESULT DoVerb(
  LONG iVerb,
  LPMAPIVIEWCONTEXT lpViewContext,
  ULONG_PTR hwndParent,
  LPCRECT lprcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="4d956-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4d956-106">Parameters</span></span>

 <span data-ttu-id="4d956-107">_iVerb_</span><span class="sxs-lookup"><span data-stu-id="4d956-107">_iVerb_</span></span>
  
> <span data-ttu-id="4d956-108">[entrada] El número asociado con uno de los verbos del formulario.</span><span class="sxs-lookup"><span data-stu-id="4d956-108">[in] The number associated with one of the form's verbs.</span></span>
    
 <span data-ttu-id="4d956-109">_lpViewContext_</span><span class="sxs-lookup"><span data-stu-id="4d956-109">_lpViewContext_</span></span>
  
> <span data-ttu-id="4d956-110">[entrada] Un puntero a un objeto de contexto de la vista.</span><span class="sxs-lookup"><span data-stu-id="4d956-110">[in] A pointer to a view context object.</span></span> <span data-ttu-id="4d956-111">El parámetro _lpViewContext_ puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="4d956-111">The  _lpViewContext_ parameter can be **null**.</span></span>
    
 <span data-ttu-id="4d956-112">_hwndParent_</span><span class="sxs-lookup"><span data-stu-id="4d956-112">_hwndParent_</span></span>
  
> <span data-ttu-id="4d956-113">[entrada] Un identificador de la ventana principal de windows o cuadros de diálogo que muestra este método.</span><span class="sxs-lookup"><span data-stu-id="4d956-113">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="4d956-114">El parámetro _hwndParent_ debe ser **null** si la ventana o el cuadro de diálogo no es modal.</span><span class="sxs-lookup"><span data-stu-id="4d956-114">The  _hwndParent_ parameter should be **null** if the dialog box or window is not modal.</span></span> 
    
 <span data-ttu-id="4d956-115">_lprcPosRect_</span><span class="sxs-lookup"><span data-stu-id="4d956-115">_lprcPosRect_</span></span>
  
> <span data-ttu-id="4d956-116">[entrada] Un puntero a un Win32 estructura de [rectángulo](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) que contiene el tamaño y la posición de la ventana del formulario.</span><span class="sxs-lookup"><span data-stu-id="4d956-116">[in] A pointer to a Win32 [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) structure that contains the size and position of the form's window.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4d956-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4d956-117">Return value</span></span>

<span data-ttu-id="4d956-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="4d956-118">S_OK</span></span> 
  
> <span data-ttu-id="4d956-119">Correctamente que se invocó el verbo.</span><span class="sxs-lookup"><span data-stu-id="4d956-119">The verb was successfully invoked.</span></span>
    
<span data-ttu-id="4d956-120">OLEOBJ_S_CANNOT_DOVERB_NOW</span><span class="sxs-lookup"><span data-stu-id="4d956-120">OLEOBJ_S_CANNOT_DOVERB_NOW</span></span> 
  
> <span data-ttu-id="4d956-121">El verbo representado por el parámetro _iVerb_ es válido, pero el formulario no puede realizar las operaciones asociadas actualmente con él.</span><span class="sxs-lookup"><span data-stu-id="4d956-121">The verb represented by the  _iVerb_ parameter is valid, but the form cannot perform the operations currently associated with it.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4d956-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4d956-122">Remarks</span></span>

<span data-ttu-id="4d956-123">Visores de formulario llamar al método **IMAPIForm::DoVerb** para solicitar que el formulario realice las tareas que asocia con cada verbo que es compatible con el formulario.</span><span class="sxs-lookup"><span data-stu-id="4d956-123">Form viewers call the **IMAPIForm::DoVerb** method to request that the form perform the tasks that it associates with each verb that the form supports.</span></span> 
  
<span data-ttu-id="4d956-124">Cada uno de los verbos admitidos se identifica mediante un valor numérico, pasado a **DoVerb** en el parámetro _iVerb_ .</span><span class="sxs-lookup"><span data-stu-id="4d956-124">Each of the supported verbs is identified by a numeric value, passed to **DoVerb** in the  _iVerb_ parameter.</span></span> <span data-ttu-id="4d956-125">Las implementaciones típicas de **DoVerb** contienen una instrucción **switch** que comprueba los valores que son válidos para el parámetro _iVerb_ para el formulario.</span><span class="sxs-lookup"><span data-stu-id="4d956-125">Typical implementations of **DoVerb** contain a **switch** statement that tests the values that are valid for the  _iVerb_ parameter for the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4d956-126">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="4d956-126">Notes to implementers</span></span>

<span data-ttu-id="4d956-127">Si el Visor de formulario especifica un contexto de vista en el parámetro _lpViewContext_ , usar en su implementación **DoVerb** en lugar de al contexto de la vista que se pasan en una llamada anterior al método [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="4d956-127">If the form viewer specifies a view context in the  _lpViewContext_ parameter, use it in your **DoVerb** implementation instead of the view context passed in an earlier call to the [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method.</span></span> <span data-ttu-id="4d956-128">Hacer que los cambios son necesarios para las estructuras de datos internos y no guardar el contexto de vista.</span><span class="sxs-lookup"><span data-stu-id="4d956-128">Make whatever changes are necessary to your internal data structures and do not save the view context.</span></span> 
  
<span data-ttu-id="4d956-129">En su implementación **DoVerb** , realice las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="4d956-129">Perform the following tasks in your **DoVerb** implementation:</span></span> 
  
- <span data-ttu-id="4d956-130">Ejecutar el código que es necesario para el verbo concreto que está asociado con el parámetro _iVerb_ .</span><span class="sxs-lookup"><span data-stu-id="4d956-130">Execute whatever code is necessary for the particular verb that is associated with the  _iVerb_ parameter.</span></span> 
    
- <span data-ttu-id="4d956-131">Si es necesario, restaure el contexto de vista original.</span><span class="sxs-lookup"><span data-stu-id="4d956-131">If necessary, restore the original view context.</span></span>
    
- <span data-ttu-id="4d956-132">Si se ha pasado un número de verbo desconocido en, devolver MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="4d956-132">If an unknown verb number was passed in, return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="4d956-133">De lo contrario, devolver un resultado basándose en el éxito o el fracaso de cualquier verbo se ha ejecutado.</span><span class="sxs-lookup"><span data-stu-id="4d956-133">Otherwise, return a result based on the success or failure of whatever verb was executed.</span></span>
    
- <span data-ttu-id="4d956-134">Cerrar el formulario.</span><span class="sxs-lookup"><span data-stu-id="4d956-134">Close the form.</span></span> <span data-ttu-id="4d956-135">Siempre es su responsabilidad para cerrar el formulario una vez que finaliza una llamada **DoVerb** .</span><span class="sxs-lookup"><span data-stu-id="4d956-135">It is always your responsibility to close the form after a **DoVerb** call completes.</span></span> 
    
<span data-ttu-id="4d956-136">Algunos verbos, como la impresión, deben ser modales con respecto a la llamada **DoVerb** , es decir, la operación indicada se debe finalizar antes de la llamada **DoVerb** devuelve.</span><span class="sxs-lookup"><span data-stu-id="4d956-136">Some verbs, such as Print, should be modal with respect to the **DoVerb** call — that is, the indicated operation must be finished before the **DoVerb** call returns.</span></span> 
  
<span data-ttu-id="4d956-137">Para obtener la estructura de **rectángulo** usada por la ventana de un formulario, llame a la función [GetWindowRect](https://msdn.microsoft.com/library/ms633519) .</span><span class="sxs-lookup"><span data-stu-id="4d956-137">To obtain the **RECT** structure used by a form's window, call the [GetWindowRect](https://msdn.microsoft.com/library/ms633519) function.</span></span> 
  
<span data-ttu-id="4d956-138">No guarde el controlador en el parámetro _hwndParent_ porque, aunque normalmente permanece válido hasta la finalización de **DoVerb**, puede ser destruir inmediatamente tras la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="4d956-138">Do not save the handle in the  _hwndParent_ parameter because, although it usually remains valid until the completion of **DoVerb**, it can be destroyed immediately upon the call's return.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="4d956-139">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="4d956-139">Notes to callers</span></span>

<span data-ttu-id="4d956-140">Puede realizar los verbos no modal actuar como verbos modales señalando _lpViewContext_ a una implementación de contexto de vista que devuelve la marca VCSTATUS_MODAL desde su método [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="4d956-140">You can make non-modal verbs act as modal verbs by pointing  _lpViewContext_ to a view context implementation that returns the VCSTATUS_MODAL flag from its [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method.</span></span> 
  
<span data-ttu-id="4d956-141">Para obtener más información acerca de los verbos en MAPI, vea [Verbos de formulario](form-verbs.md).</span><span class="sxs-lookup"><span data-stu-id="4d956-141">For more information about verbs in MAPI, see [Form Verbs](form-verbs.md).</span></span> <span data-ttu-id="4d956-142">Para obtener más información acerca de cómo se administran los verbos en OLE, vea [OLE y la transferencia de datos](https://msdn.microsoft.com/library/ms693425%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="4d956-142">For more information about how verbs are handled in OLE, see [OLE and Data Transfer](https://msdn.microsoft.com/library/ms693425%28VS.85%29.aspx).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4d956-143">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="4d956-143">MFCMAPI reference</span></span>

<span data-ttu-id="4d956-144">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="4d956-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4d956-145">**File**</span><span class="sxs-lookup"><span data-stu-id="4d956-145">**File**</span></span>|<span data-ttu-id="4d956-146">**Función**</span><span class="sxs-lookup"><span data-stu-id="4d956-146">**Function**</span></span>|<span data-ttu-id="4d956-147">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="4d956-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4d956-148">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="4d956-148">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="4d956-149">CMyMAPIFormViewer::CallDoVerb</span><span class="sxs-lookup"><span data-stu-id="4d956-149">CMyMAPIFormViewer::CallDoVerb</span></span>  <br/> |<span data-ttu-id="4d956-150">MFCMAPI usa el método **IMAPIForm::DoVerb** para invocar un verbo en un formulario.</span><span class="sxs-lookup"><span data-stu-id="4d956-150">MFCMAPI uses the **IMAPIForm::DoVerb** method to invoke a verb on a form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4d956-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d956-151">See also</span></span>



[<span data-ttu-id="4d956-152">IMAPIForm::SetViewContext</span><span class="sxs-lookup"><span data-stu-id="4d956-152">IMAPIForm::SetViewContext</span></span>](imapiform-setviewcontext.md)
  
[<span data-ttu-id="4d956-153">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="4d956-153">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
  
[<span data-ttu-id="4d956-154">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4d956-154">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="4d956-155">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="4d956-155">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="4d956-156">Verbos de formulario</span><span class="sxs-lookup"><span data-stu-id="4d956-156">Form Verbs</span></span>](form-verbs.md)

