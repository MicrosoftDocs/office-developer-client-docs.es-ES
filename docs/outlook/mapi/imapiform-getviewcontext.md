---
title: IMAPIFormGetViewContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.GetViewContext
api_type:
- COM
ms.assetid: c6938986-a9f9-4ef4-9655-ded55b7357db
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9f09f29d67bff6588c826b92d93aead491510cef
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574821"
---
# <a name="imapiformgetviewcontext"></a><span data-ttu-id="2aebd-103">IMAPIForm::GetViewContext</span><span class="sxs-lookup"><span data-stu-id="2aebd-103">IMAPIForm::GetViewContext</span></span>

  
  
<span data-ttu-id="2aebd-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2aebd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2aebd-105">Devuelve el contexto de la vista actual para el formulario.</span><span class="sxs-lookup"><span data-stu-id="2aebd-105">Returns the current view context for the form.</span></span> 
  
```cpp
HRESULT GetViewContext(
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a><span data-ttu-id="2aebd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2aebd-106">Parameters</span></span>

 <span data-ttu-id="2aebd-107">_ppViewContext_</span><span class="sxs-lookup"><span data-stu-id="2aebd-107">_ppViewContext_</span></span>
  
> <span data-ttu-id="2aebd-108">[out] Un puntero a un puntero al contexto de la vista del formulario.</span><span class="sxs-lookup"><span data-stu-id="2aebd-108">[out] A pointer to a pointer to the form's view context.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2aebd-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2aebd-109">Return value</span></span>

<span data-ttu-id="2aebd-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="2aebd-110">S_OK</span></span> 
  
> <span data-ttu-id="2aebd-111">Contexto de la vista actual del formulario se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="2aebd-111">The form's current view context was successfully returned.</span></span> 
    
<span data-ttu-id="2aebd-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="2aebd-112">S_FALSE</span></span> 
  
> <span data-ttu-id="2aebd-113">No hay ningún contexto de vista para el formulario.</span><span class="sxs-lookup"><span data-stu-id="2aebd-113">There is no view context for the form.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2aebd-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2aebd-114">Remarks</span></span>

<span data-ttu-id="2aebd-115">Visores de formulario, llame a **GetViewContext** para obtener un puntero para el contexto de vista establecido en una llamada anterior a [IMAPIForm::SetViewContext](imapiform-setviewcontext.md).</span><span class="sxs-lookup"><span data-stu-id="2aebd-115">Form viewers call **GetViewContext** to obtain a pointer to the view context established in a previous call to [IMAPIForm::SetViewContext](imapiform-setviewcontext.md).</span></span> <span data-ttu-id="2aebd-116">Si no se ha realizado ninguna llamada anterior a **SetViewContext**, **GetViewContext** _ppViewContext_ se establece en NULL.</span><span class="sxs-lookup"><span data-stu-id="2aebd-116">If no prior call has been made to **SetViewContext**, **GetViewContext** sets  _ppViewContext_ to NULL.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="2aebd-117">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="2aebd-117">Notes to implementers</span></span>

<span data-ttu-id="2aebd-118">Copie el puntero de contexto de vista de su formulario en el puntero que se pasó por el Visor de formulario llamada en el parámetro _ppViewContext_ .</span><span class="sxs-lookup"><span data-stu-id="2aebd-118">Copy your form's view context pointer into the pointer passed in by the calling form viewer in the  _ppViewContext_ parameter.</span></span> <span data-ttu-id="2aebd-119">Si el formulario no tiene un contexto de vista, establezca _ppViewContext_ en NULL.</span><span class="sxs-lookup"><span data-stu-id="2aebd-119">If the form does not have a view context, set  _ppViewContext_ to NULL.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2aebd-120">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="2aebd-120">MFCMAPI reference</span></span>

<span data-ttu-id="2aebd-121">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="2aebd-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2aebd-122">**File**</span><span class="sxs-lookup"><span data-stu-id="2aebd-122">**File**</span></span>|<span data-ttu-id="2aebd-123">**Función**</span><span class="sxs-lookup"><span data-stu-id="2aebd-123">**Function**</span></span>|<span data-ttu-id="2aebd-124">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="2aebd-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2aebd-125">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="2aebd-125">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="2aebd-126">OpenMessageNonModal</span><span class="sxs-lookup"><span data-stu-id="2aebd-126">OpenMessageNonModal</span></span>  <br/> |<span data-ttu-id="2aebd-127">MFCMAPI utiliza el método **IMAPIForm::GetViewContext** para comprobar si un formulario tiene un contexto de vista.</span><span class="sxs-lookup"><span data-stu-id="2aebd-127">MFCMAPI uses the **IMAPIForm::GetViewContext** method to check whether a form has a view context.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2aebd-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="2aebd-128">See also</span></span>



[<span data-ttu-id="2aebd-129">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2aebd-129">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
  
[<span data-ttu-id="2aebd-130">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2aebd-130">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="2aebd-131">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="2aebd-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

