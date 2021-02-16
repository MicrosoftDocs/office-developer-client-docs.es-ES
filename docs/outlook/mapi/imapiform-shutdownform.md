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
ms.openlocfilehash: 073a76766a296d86e7a23809921b832d494a8f1b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329480"
---
# <a name="imapiformshutdownform"></a><span data-ttu-id="28d28-103">IMAPIForm::ShutdownForm</span><span class="sxs-lookup"><span data-stu-id="28d28-103">IMAPIForm::ShutdownForm</span></span>

  
  
<span data-ttu-id="28d28-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="28d28-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="28d28-105">Cierra el formulario.</span><span class="sxs-lookup"><span data-stu-id="28d28-105">Closes the form.</span></span>
  
```cpp
HRESULT ShutdownForm(
  ULONG ulSaveOptions
);
```

## <a name="parameters"></a><span data-ttu-id="28d28-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28d28-106">Parameters</span></span>

 <span data-ttu-id="28d28-107">_ulSaveOptions_</span><span class="sxs-lookup"><span data-stu-id="28d28-107">_ulSaveOptions_</span></span>
  
> <span data-ttu-id="28d28-108">[entrada] Valor que controla cómo o si los datos del formulario se guardan antes de cerrar el formulario.</span><span class="sxs-lookup"><span data-stu-id="28d28-108">[in] A value that controls how or whether data in the form is saved before the form is closed.</span></span> <span data-ttu-id="28d28-109">Puede establecer uno de los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="28d28-109">One of the following flags can be set:</span></span>
    
<span data-ttu-id="28d28-110">SAVEOPTS_NOSAVE</span><span class="sxs-lookup"><span data-stu-id="28d28-110">SAVEOPTS_NOSAVE</span></span> 
  
> <span data-ttu-id="28d28-111">No se deben guardar los datos del formulario.</span><span class="sxs-lookup"><span data-stu-id="28d28-111">Form data should not be saved.</span></span>
    
<span data-ttu-id="28d28-112">SAVEOPTS_PROMPTSAVE</span><span class="sxs-lookup"><span data-stu-id="28d28-112">SAVEOPTS_PROMPTSAVE</span></span> 
  
> <span data-ttu-id="28d28-113">Se debe pedir al usuario que guarde los datos modificados en el formulario.</span><span class="sxs-lookup"><span data-stu-id="28d28-113">The user should be prompted to save any changed data in the form.</span></span>
    
<span data-ttu-id="28d28-114">SAVEOPTS_SAVEIFDIRTY</span><span class="sxs-lookup"><span data-stu-id="28d28-114">SAVEOPTS_SAVEIFDIRTY</span></span> 
  
> <span data-ttu-id="28d28-115">Los datos del formulario deben guardarse si han cambiado desde la última vez que se guardaron.</span><span class="sxs-lookup"><span data-stu-id="28d28-115">Form data should be saved if it has changed since the last save.</span></span> <span data-ttu-id="28d28-116">Si no se muestra ninguna interfaz de usuario, el formulario puede cambiar opcionalmente a usar la funcionalidad para la SAVEOPTS_NOSAVE usuario.</span><span class="sxs-lookup"><span data-stu-id="28d28-116">If no user interface is being displayed, the form can optionally switch to using the functionality for the SAVEOPTS_NOSAVE option.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="28d28-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28d28-117">Return value</span></span>

<span data-ttu-id="28d28-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="28d28-118">S_OK</span></span> 
  
> <span data-ttu-id="28d28-119">El formulario se ha cerrado.</span><span class="sxs-lookup"><span data-stu-id="28d28-119">The form was closed.</span></span>
    
<span data-ttu-id="28d28-120">E_UNEXPECTED</span><span class="sxs-lookup"><span data-stu-id="28d28-120">E_UNEXPECTED</span></span> 
  
> <span data-ttu-id="28d28-121">El formulario ya estaba cerrado por una llamada anterior a **ShutdownForm**.</span><span class="sxs-lookup"><span data-stu-id="28d28-121">The form was already closed by a prior call to **ShutdownForm**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="28d28-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="28d28-122">Remarks</span></span>

<span data-ttu-id="28d28-123">Los visores de formularios llaman **al método IMAPIForm::ShutdownForm** para cerrar un formulario.</span><span class="sxs-lookup"><span data-stu-id="28d28-123">Form viewers call the **IMAPIForm::ShutdownForm** method to close a form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="28d28-124">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="28d28-124">Notes to implementers</span></span>

<span data-ttu-id="28d28-125">Realice las siguientes tareas en la implementación de **ShutdownForm:**</span><span class="sxs-lookup"><span data-stu-id="28d28-125">Perform the following tasks in your implementation of **ShutdownForm**:</span></span>
  
1. <span data-ttu-id="28d28-126">Comprueba que un visor aún no ha llamado **ShutdownForm** y devuelve E_UNEXPECTED si lo ha hecho.</span><span class="sxs-lookup"><span data-stu-id="28d28-126">Check that a viewer has not already called **ShutdownForm**, and return E_UNEXPECTED if it has.</span></span> <span data-ttu-id="28d28-127">Aunque esto es poco probable, debe comprobarlo.</span><span class="sxs-lookup"><span data-stu-id="28d28-127">Although this is unlikely, you should check.</span></span>
    
2. <span data-ttu-id="28d28-128">Llame al método [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) del formulario para que el almacenamiento del formulario y las estructuras de datos internas permanezcan disponibles hasta que finalice el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="28d28-128">Call your form's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method so that storage for the form and any internal data structures remain available until processing is finished.</span></span> 
    
3. <span data-ttu-id="28d28-129">Determine si hay cambios no guardados en los datos del formulario.</span><span class="sxs-lookup"><span data-stu-id="28d28-129">Determine whether there are any unsaved changes to the form's data.</span></span> <span data-ttu-id="28d28-130">Guarde los datos no guardados de acuerdo con cómo se establece el parámetro  _ulSaveOptions_ llamando al método [IMAPIMessageSite::SaveMessage del](imapimessagesite-savemessage.md) visor.</span><span class="sxs-lookup"><span data-stu-id="28d28-130">Save unsaved data according to how the  _ulSaveOptions_ parameter is set by calling your viewer's [IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md) method.</span></span> 
    
4. <span data-ttu-id="28d28-131">Destruye la ventana de interfaz de usuario del formulario.</span><span class="sxs-lookup"><span data-stu-id="28d28-131">Destroy your form's user interface window.</span></span>
    
5. <span data-ttu-id="28d28-132">Libere los objetos de sitio de mensajes y mensajes del formulario llamando a sus métodos [IUnknown::Release.](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="28d28-132">Release your form's message and message site objects by calling their [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) methods.</span></span> 
    
6. <span data-ttu-id="28d28-133">Notifica a todos los visores registrados del apagado pendiente llamando a sus [métodos IMAPIViewAdviseSink::OnShutdown.](imapiviewadvisesink-onshutdown.md)</span><span class="sxs-lookup"><span data-stu-id="28d28-133">Notify all registered viewers of the pending shutdown by calling their [IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md) methods.</span></span> 
    
7. <span data-ttu-id="28d28-134">Llame al [método IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) para cancelar el registro del formulario para la notificación estableciendo el puntero receptor de aviso en **null**.</span><span class="sxs-lookup"><span data-stu-id="28d28-134">Call the [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method to cancel your form's registration for notification by setting the advise sink pointer to **null**.</span></span>
    
8. <span data-ttu-id="28d28-135">Llama a [la función MAPIFreeBuffer](mapifreebuffer.md) para liberar la memoria de las propiedades del formulario.</span><span class="sxs-lookup"><span data-stu-id="28d28-135">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the memory for your form's properties.</span></span> 
    
9. <span data-ttu-id="28d28-136">Llame al método **IUnknown::Release** del formulario, que coincida con la **llamada AddRef** realizada en el paso 2.</span><span class="sxs-lookup"><span data-stu-id="28d28-136">Call your form's **IUnknown::Release** method, matching the **AddRef** call made in step 2.</span></span> 
    
10. <span data-ttu-id="28d28-137">Devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="28d28-137">Return S_OK.</span></span>
    
> [!NOTE]
> <span data-ttu-id="28d28-138">Una vez completadas estas acciones, los únicos métodos válidos en el objeto de formulario al que se puede llamar son los de la [interfaz IUnknown.](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="28d28-138">After these actions have been completed, the only valid methods on the form object that may be called are those from the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="28d28-139">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="28d28-139">Notes to callers</span></span>

<span data-ttu-id="28d28-140">Cuando **ShutdownForm** devuelve, independientemente de si devuelve un error, libere el formulario llamando a su **método IUnknown::Release.**</span><span class="sxs-lookup"><span data-stu-id="28d28-140">When **ShutdownForm** returns, regardless of whether it returns an error, release the form by calling its **IUnknown::Release** method.</span></span> <span data-ttu-id="28d28-141">Puede omitir de forma segura los errores devueltos **por ShutdownForm**.</span><span class="sxs-lookup"><span data-stu-id="28d28-141">You can safely ignore any errors returned by **ShutdownForm**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="28d28-142">Consulte también</span><span class="sxs-lookup"><span data-stu-id="28d28-142">See also</span></span>



[<span data-ttu-id="28d28-143">IMAPIMessageSite::SaveMessage</span><span class="sxs-lookup"><span data-stu-id="28d28-143">IMAPIMessageSite::SaveMessage</span></span>](imapimessagesite-savemessage.md)
  
[<span data-ttu-id="28d28-144">IMAPIViewAdviseSink::OnShutdown</span><span class="sxs-lookup"><span data-stu-id="28d28-144">IMAPIViewAdviseSink::OnShutdown</span></span>](imapiviewadvisesink-onshutdown.md)
  
[<span data-ttu-id="28d28-145">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="28d28-145">IMAPIViewContext::SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md)
  
[<span data-ttu-id="28d28-146">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="28d28-146">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="28d28-147">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="28d28-147">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)

