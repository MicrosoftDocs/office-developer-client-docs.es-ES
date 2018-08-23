---
title: IMAPIFormShutdownForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.ShutdownForm
api_type:
- COM
ms.assetid: f1e2a526-40ad-4a93-908f-8ab9a65928a8
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 49ed8669a5496524917c15ac86e4a13060931057
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578573"
---
# <a name="imapiformshutdownform"></a><span data-ttu-id="c420b-103">IMAPIForm::ShutdownForm</span><span class="sxs-lookup"><span data-stu-id="c420b-103">IMAPIForm::ShutdownForm</span></span>

  
  
<span data-ttu-id="c420b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c420b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c420b-105">Cierra el formulario.</span><span class="sxs-lookup"><span data-stu-id="c420b-105">Closes the form.</span></span>
  
```cpp
HRESULT ShutdownForm(
  ULONG ulSaveOptions
);
```

## <a name="parameters"></a><span data-ttu-id="c420b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c420b-106">Parameters</span></span>

 <span data-ttu-id="c420b-107">_ulSaveOptions_</span><span class="sxs-lookup"><span data-stu-id="c420b-107">_ulSaveOptions_</span></span>
  
> <span data-ttu-id="c420b-108">[entrada] Un valor que controla cómo o si se guardan los datos en el formulario antes de cerrar el formulario.</span><span class="sxs-lookup"><span data-stu-id="c420b-108">[in] A value that controls how or whether data in the form is saved before the form is closed.</span></span> <span data-ttu-id="c420b-109">Puede establecer uno de los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="c420b-109">One of the following flags can be set:</span></span>
    
<span data-ttu-id="c420b-110">SAVEOPTS_NOSAVE</span><span class="sxs-lookup"><span data-stu-id="c420b-110">SAVEOPTS_NOSAVE</span></span> 
  
> <span data-ttu-id="c420b-111">No se deben guardar los datos del formulario.</span><span class="sxs-lookup"><span data-stu-id="c420b-111">Form data should not be saved.</span></span>
    
<span data-ttu-id="c420b-112">SAVEOPTS_PROMPTSAVE</span><span class="sxs-lookup"><span data-stu-id="c420b-112">SAVEOPTS_PROMPTSAVE</span></span> 
  
> <span data-ttu-id="c420b-113">El usuario se debe pedir para guardar los datos modificados en el formulario.</span><span class="sxs-lookup"><span data-stu-id="c420b-113">The user should be prompted to save any changed data in the form.</span></span>
    
<span data-ttu-id="c420b-114">SAVEOPTS_SAVEIFDIRTY</span><span class="sxs-lookup"><span data-stu-id="c420b-114">SAVEOPTS_SAVEIFDIRTY</span></span> 
  
> <span data-ttu-id="c420b-115">Si ha cambiado desde la última vez que se guardó, se deben guardar datos de formulario.</span><span class="sxs-lookup"><span data-stu-id="c420b-115">Form data should be saved if it has changed since the last save.</span></span> <span data-ttu-id="c420b-116">Si no se muestra ninguna interfaz de usuario, el formulario, opcionalmente, puede pasar a usar la funcionalidad para la opción SAVEOPTS_NOSAVE.</span><span class="sxs-lookup"><span data-stu-id="c420b-116">If no user interface is being displayed, the form can optionally switch to using the functionality for the SAVEOPTS_NOSAVE option.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c420b-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c420b-117">Return value</span></span>

<span data-ttu-id="c420b-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="c420b-118">S_OK</span></span> 
  
> <span data-ttu-id="c420b-119">Se ha cerrado el formulario.</span><span class="sxs-lookup"><span data-stu-id="c420b-119">The form was closed.</span></span>
    
<span data-ttu-id="c420b-120">E_UNEXPECTED</span><span class="sxs-lookup"><span data-stu-id="c420b-120">E_UNEXPECTED</span></span> 
  
> <span data-ttu-id="c420b-121">El formulario ya se ha cerrado por una llamada anterior a **ShutdownForm**.</span><span class="sxs-lookup"><span data-stu-id="c420b-121">The form was already closed by a prior call to **ShutdownForm**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c420b-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c420b-122">Remarks</span></span>

<span data-ttu-id="c420b-123">Visores de formulario llamar al método **IMAPIForm::ShutdownForm** para cerrar un formulario.</span><span class="sxs-lookup"><span data-stu-id="c420b-123">Form viewers call the **IMAPIForm::ShutdownForm** method to close a form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c420b-124">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="c420b-124">Notes to implementers</span></span>

<span data-ttu-id="c420b-125">Realizar las siguientes tareas en su implementación de **ShutdownForm**:</span><span class="sxs-lookup"><span data-stu-id="c420b-125">Perform the following tasks in your implementation of **ShutdownForm**:</span></span>
  
1. <span data-ttu-id="c420b-126">Comprobar que un visor ya no llamado **ShutdownForm**y devolver E_UNEXPECTED si lo tiene.</span><span class="sxs-lookup"><span data-stu-id="c420b-126">Check that a viewer has not already called **ShutdownForm**, and return E_UNEXPECTED if it has.</span></span> <span data-ttu-id="c420b-127">Aunque es poco probable, se debe comprobar.</span><span class="sxs-lookup"><span data-stu-id="c420b-127">Although this is unlikely, you should check.</span></span>
    
2. <span data-ttu-id="c420b-128">Llamar al método [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) de su formulario para que el almacenamiento de información para el formulario y las estructuras de datos internos permanecen disponibles hasta que haya terminado el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="c420b-128">Call your form's [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) method so that storage for the form and any internal data structures remain available until processing is finished.</span></span> 
    
3. <span data-ttu-id="c420b-129">Determinar si hay cambios no guardados para los datos del formulario.</span><span class="sxs-lookup"><span data-stu-id="c420b-129">Determine whether there are any unsaved changes to the form's data.</span></span> <span data-ttu-id="c420b-130">Guarde los datos no guardados según cómo se establece el parámetro _ulSaveOptions_ al llamar al método de [IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md) del Visor.</span><span class="sxs-lookup"><span data-stu-id="c420b-130">Save unsaved data according to how the  _ulSaveOptions_ parameter is set by calling your viewer's [IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md) method.</span></span> 
    
4. <span data-ttu-id="c420b-131">Destruir la ventana de interfaz de usuario de su formulario.</span><span class="sxs-lookup"><span data-stu-id="c420b-131">Destroy your form's user interface window.</span></span>
    
5. <span data-ttu-id="c420b-132">Liberar el formulario mensaje y objetos de sitio de mensaje llamando a sus métodos [IUnknown:: Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c420b-132">Release your form's message and message site objects by calling their [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) methods.</span></span> 
    
6. <span data-ttu-id="c420b-133">Notificar a todos los visores del cierre pendiente llamando a sus métodos [IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="c420b-133">Notify all registered viewers of the pending shutdown by calling their [IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md) methods.</span></span> 
    
7. <span data-ttu-id="c420b-134">Llame al método [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) para cancelar el registro de su formulario para notificación estableciendo el puntero de receptor advise en **null**.</span><span class="sxs-lookup"><span data-stu-id="c420b-134">Call the [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method to cancel your form's registration for notification by setting the advise sink pointer to **null**.</span></span>
    
8. <span data-ttu-id="c420b-135">Llame a la función [MAPIFreeBuffer](mapifreebuffer.md) para liberar la memoria para las propiedades del formulario.</span><span class="sxs-lookup"><span data-stu-id="c420b-135">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the memory for your form's properties.</span></span> 
    
9. <span data-ttu-id="c420b-136">Llamar al método **IUnknown:: Release** de su formulario, que coincidan con la llamada de **AddRef** realizada en el paso 2.</span><span class="sxs-lookup"><span data-stu-id="c420b-136">Call your form's **IUnknown::Release** method, matching the **AddRef** call made in step 2.</span></span> 
    
10. <span data-ttu-id="c420b-137">Devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="c420b-137">Return S_OK.</span></span>
    
> [!NOTE]
> <span data-ttu-id="c420b-138">Después de que se hayan completado estas acciones, los métodos solo es válidos en el objeto de formulario que se puede llamar son los de la interfaz [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c420b-138">After these actions have been completed, the only valid methods on the form object that may be called are those from the [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) interface.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c420b-139">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="c420b-139">Notes to callers</span></span>

<span data-ttu-id="c420b-140">Cuando se devuelve **ShutdownForm** , independientemente de si devuelve un error, la versión del formulario llamando a su método **IUnknown:: Release** .</span><span class="sxs-lookup"><span data-stu-id="c420b-140">When **ShutdownForm** returns, regardless of whether it returns an error, release the form by calling its **IUnknown::Release** method.</span></span> <span data-ttu-id="c420b-141">Puede omitir sin ningún riesgo los errores devueltos por **ShutdownForm**.</span><span class="sxs-lookup"><span data-stu-id="c420b-141">You can safely ignore any errors returned by **ShutdownForm**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c420b-142">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="c420b-142">See also</span></span>



[<span data-ttu-id="c420b-143">IMAPIMessageSite::SaveMessage</span><span class="sxs-lookup"><span data-stu-id="c420b-143">IMAPIMessageSite::SaveMessage</span></span>](imapimessagesite-savemessage.md)
  
[<span data-ttu-id="c420b-144">IMAPIViewAdviseSink::OnShutdown</span><span class="sxs-lookup"><span data-stu-id="c420b-144">IMAPIViewAdviseSink::OnShutdown</span></span>](imapiviewadvisesink-onshutdown.md)
  
[<span data-ttu-id="c420b-145">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="c420b-145">IMAPIViewContext::SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md)
  
[<span data-ttu-id="c420b-146">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="c420b-146">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="c420b-147">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c420b-147">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)

