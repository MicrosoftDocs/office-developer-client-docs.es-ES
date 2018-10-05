---
title: IMAPIFormSetViewContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.SetViewContext
api_type:
- COM
ms.assetid: a7b10007-42d8-4755-8362-f8ad9a8dad68
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 81d99b2bbe6ef7914a4b7d253a3472026872260d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384314"
---
# <a name="imapiformsetviewcontext"></a><span data-ttu-id="47457-103">IMAPIForm::SetViewContext</span><span class="sxs-lookup"><span data-stu-id="47457-103">IMAPIForm::SetViewContext</span></span>

  
  
<span data-ttu-id="47457-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47457-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47457-105">Establece un contexto de vista para el formulario.</span><span class="sxs-lookup"><span data-stu-id="47457-105">Establishes a view context for the form.</span></span> 
  
```cpp
HRESULT SetViewContext(
  LPMAPIVIEWCONTEXT pViewContext
);
```

## <a name="parameters"></a><span data-ttu-id="47457-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47457-106">Parameters</span></span>

 <span data-ttu-id="47457-107">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="47457-107">_pViewContext_</span></span>
  
> <span data-ttu-id="47457-108">[entrada] Un puntero al nuevo contexto de vista para el formulario.</span><span class="sxs-lookup"><span data-stu-id="47457-108">[in] A pointer to the new view context for the form.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="47457-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="47457-109">Return value</span></span>

<span data-ttu-id="47457-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="47457-110">S_OK</span></span> 
  
> <span data-ttu-id="47457-111">Se estableció correctamente en el contexto de vista.</span><span class="sxs-lookup"><span data-stu-id="47457-111">The view context was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="47457-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="47457-112">Remarks</span></span>

<span data-ttu-id="47457-113">Visores de formulario llamar al método **IMAPIForm::SetViewContext** para establecer un contexto de vista de formulario en particular como actual.</span><span class="sxs-lookup"><span data-stu-id="47457-113">Form viewers call the **IMAPIForm::SetViewContext** method to establish a particular form view context as current.</span></span> <span data-ttu-id="47457-114">Un formulario puede tener solo un contexto de vista a la vez.</span><span class="sxs-lookup"><span data-stu-id="47457-114">A form can have only one view context at a time.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="47457-115">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="47457-115">Notes to implementers</span></span>

<span data-ttu-id="47457-116">La mayoría de los servidores de formulario implementan **SetViewContext** mediante el siguiente algoritmo:</span><span class="sxs-lookup"><span data-stu-id="47457-116">Most form servers implement **SetViewContext** by using the following algorithm:</span></span> 
  
- <span data-ttu-id="47457-117">Si ya existe un contexto de vista para el formulario, cancelar el registro del formulario llamando al método [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) con **null** en el parámetro _pmnvs_ y, a continuación, llamar [IUnknown:: Release al contexto la vista](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) método para reducir su recuento de referencia.</span><span class="sxs-lookup"><span data-stu-id="47457-117">If a view context already exists for the form, cancel the form's registration by calling the [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method with **null** in the  _pmnvs_ parameter, and then call the view context's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method to decrement its reference count.</span></span> 
    
- <span data-ttu-id="47457-118">Si el contexto de vista nueva no es **null**, llamada **IMAPIViewContext::SetAdviseSink** mediante el parámetro _pViewContext_ para configurar una nueva vista de aviso receptor.</span><span class="sxs-lookup"><span data-stu-id="47457-118">If the new view context is not **null**, call **IMAPIViewContext::SetAdviseSink** by using the  _pViewContext_ parameter to set up a new view advise sink.</span></span> 
    
- <span data-ttu-id="47457-119">Si el contexto de vista nueva no es **null**, llame al método [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) para determinar qué indicadores de estado se hayan establecido.</span><span class="sxs-lookup"><span data-stu-id="47457-119">If the new view context is not **null**, call the [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method to determine which status flags have been set.</span></span> 
    
- <span data-ttu-id="47457-120">Si el contexto de vista nueva no es **null**, guárdelo y llamar al método [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) para incrementar su recuento de referencia.</span><span class="sxs-lookup"><span data-stu-id="47457-120">If the new view context is not **null**, store it and call its [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method to increment its reference count.</span></span> 
    
- <span data-ttu-id="47457-121">Actualizar todos los elementos de interfaz de usuario que dependen del contexto de la vista.</span><span class="sxs-lookup"><span data-stu-id="47457-121">Update any user interface elements that depend on the view context.</span></span> 
    
<span data-ttu-id="47457-122">Dependiendo de los indicadores de estado devueltos desde **IMAPIViewContext::GetViewStatus**, **SetViewContext** también pueden realizar otras acciones.</span><span class="sxs-lookup"><span data-stu-id="47457-122">Depending on the status flags returned from **IMAPIViewContext::GetViewStatus**, **SetViewContext** can also perform other actions.</span></span> <span data-ttu-id="47457-123">Por ejemplo, si se devuelven los indicadores VCSTATUS_NEXT y VCSTATUS_PREV, **SetViewContext** puede habilitar los botones **siguiente** y **anterior** para el contexto de vista nueva.</span><span class="sxs-lookup"><span data-stu-id="47457-123">For example, if the VCSTATUS_NEXT and VCSTATUS_PREV flags are returned, **SetViewContext** can enable the **Next** and **Previous** buttons for the new view context.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="47457-124">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="47457-124">MFCMAPI reference</span></span>

<span data-ttu-id="47457-125">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="47457-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="47457-126">**File**</span><span class="sxs-lookup"><span data-stu-id="47457-126">**File**</span></span>|<span data-ttu-id="47457-127">**Función**</span><span class="sxs-lookup"><span data-stu-id="47457-127">**Function**</span></span>|<span data-ttu-id="47457-128">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="47457-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="47457-129">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="47457-129">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="47457-130">CreateAndDisplayNewMailInFolder</span><span class="sxs-lookup"><span data-stu-id="47457-130">CreateAndDisplayNewMailInFolder</span></span>  <br/> |<span data-ttu-id="47457-131">MFCMAPI usa el método **IMAPIForm::SetViewContext** para establecer el contexto de vista del MFCMAPI en el formulario antes de que se muestre el formulario.</span><span class="sxs-lookup"><span data-stu-id="47457-131">MFCMAPI uses the **IMAPIForm::SetViewContext** method to set MFCMAPI's view context on the form before the form is displayed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="47457-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="47457-132">See also</span></span>



[<span data-ttu-id="47457-133">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="47457-133">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
  
[<span data-ttu-id="47457-134">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="47457-134">IMAPIViewContext::SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md)
  
[<span data-ttu-id="47457-135">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="47457-135">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="47457-136">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="47457-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

