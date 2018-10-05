---
title: IMAPIMessageSiteDeleteMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.DeleteMessage
api_type:
- COM
ms.assetid: 09955996-b904-4c0d-8ba5-954a8875c055
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7b2761e20444c51d08380aee01c41eee797733eb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396494"
---
# <a name="imapimessagesitedeletemessage"></a><span data-ttu-id="03475-103">IMAPIMessageSite::DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="03475-103">IMAPIMessageSite::DeleteMessage</span></span>

  
  
<span data-ttu-id="03475-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03475-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03475-105">Elimina el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="03475-105">Deletes the current message.</span></span>
  
```cpp
HRESULT DeleteMessage(
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="03475-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="03475-106">Parameters</span></span>

 <span data-ttu-id="03475-107">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="03475-107">_pViewContext_</span></span>
  
> <span data-ttu-id="03475-108">[entrada] Un puntero a un objeto de contexto de la vista.</span><span class="sxs-lookup"><span data-stu-id="03475-108">[in] A pointer to a view context object.</span></span>
    
 <span data-ttu-id="03475-109">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="03475-109">_prcPosRect_</span></span>
  
> <span data-ttu-id="03475-110">[entrada] Un puntero a una estructura de [rectángulo](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) que contiene el tamaño de la ventana y la posición del formulario actual.</span><span class="sxs-lookup"><span data-stu-id="03475-110">[in] A pointer to a [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) structure that contains the current form's window size and position.</span></span> <span data-ttu-id="03475-111">El siguiente formulario que muestra también usa este rectángulo de la ventana.</span><span class="sxs-lookup"><span data-stu-id="03475-111">The next form displayed also uses this window rectangle.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="03475-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="03475-112">Return value</span></span>

<span data-ttu-id="03475-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="03475-113">S_OK</span></span> 
  
> <span data-ttu-id="03475-114">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="03475-114">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="03475-115">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="03475-115">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="03475-116">La operación no es compatible con este sitio de mensaje.</span><span class="sxs-lookup"><span data-stu-id="03475-116">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="03475-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="03475-117">Remarks</span></span>

<span data-ttu-id="03475-118">Un objeto de formulario llama al método de **IMAPIMessageSite::DeleteMessage** para eliminar el mensaje que el formulario se muestra actualmente.</span><span class="sxs-lookup"><span data-stu-id="03475-118">A form object calls the **IMAPIMessageSite::DeleteMessage** method to delete the message that the form is currently displaying.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="03475-119">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="03475-119">Notes to callers</span></span>

<span data-ttu-id="03475-120">Después de la devolución de **DeleteMessage**, objetos de formulario deben comprobar para un nuevo mensaje y descartar a sí mismos si no existe ninguno.</span><span class="sxs-lookup"><span data-stu-id="03475-120">Following the return of **DeleteMessage**, form objects must check for a new message and then dismiss themselves if none exists.</span></span> <span data-ttu-id="03475-121">Para determinar si el mensaje **en que deletemessage** actúa fue eliminado o movido a una carpeta de **Elementos eliminados** , un objeto de formulario puede llamar al método de [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) para determinar si se ha devuelto la marca DELETE_IS_MOVE.</span><span class="sxs-lookup"><span data-stu-id="03475-121">To determine whether the message **DeleteMessage** acted on was deleted or moved to a **Deleted Items** folder, a form object can call the [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) method to determine whether the DELETE_IS_MOVE flag was returned.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="03475-122">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="03475-122">Notes to implementers</span></span>

<span data-ttu-id="03475-123">Si la implementación del Visor de un formulario del método **DeleteMessage** se mueve hasta el siguiente mensaje después de que elimina un mensaje, la implementación debe llamar al método [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) y pase el indicador VCDIR_DELETE antes de realizar la eliminación real.</span><span class="sxs-lookup"><span data-stu-id="03475-123">If a form viewer's implementation of the **DeleteMessage** method moves to the next message after it deletes a message, the implementation should call the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method and pass the VCDIR_DELETE flag before performing the actual deletion.</span></span> <span data-ttu-id="03475-124">Si la implementación de un visor formulario de **DeleteMessage** mueve el mensaje eliminado (por ejemplo, en una carpeta de **Elementos eliminados** ), la implementación debe guardar cambios en el mensaje, si se modificó el mensaje.</span><span class="sxs-lookup"><span data-stu-id="03475-124">If a form viewer's implementation of **DeleteMessage** moves the deleted message (for example, to a **Deleted Items** folder), the implementation must save changes to the message if the message was modified.</span></span> 
  
<span data-ttu-id="03475-125">Una implementación típica de **DeleteMessage** realiza las tareas siguientes:</span><span class="sxs-lookup"><span data-stu-id="03475-125">A typical implementation of **DeleteMessage** performs the following tasks:</span></span> 
  
1. <span data-ttu-id="03475-126">Si la implementación traslada el mensaje, se llama al método [IPersistMessage::Save](ipersistmessage-save.md) , pasando **null** en el parámetro _pMessage_ y **true** en el parámetro _fSameAsLoad_ .</span><span class="sxs-lookup"><span data-stu-id="03475-126">If the implementation is moving the message, it calls the [IPersistMessage::Save](ipersistmessage-save.md) method, passing **null** in the  _pMessage_ parameter and **true** in the  _fSameAsLoad_ parameter.</span></span> 
    
2. <span data-ttu-id="03475-127">Llama al método **IMAPIViewContext::ActivateNext** , pasando el indicador VCDIR_DELETE en el parámetro _ulDir_ .</span><span class="sxs-lookup"><span data-stu-id="03475-127">It calls the **IMAPIViewContext::ActivateNext** method, passing the VCDIR_DELETE flag in the  _ulDir_ parameter.</span></span> 
    
3. <span data-ttu-id="03475-128">Si se produce un error en la llamada **ActivateNext** , devuelve.</span><span class="sxs-lookup"><span data-stu-id="03475-128">If the **ActivateNext** call fails, it returns.</span></span> <span data-ttu-id="03475-129">Si **ActivateNext** devuelve S_FALSE, llama al método [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="03475-129">If **ActivateNext** returns S_FALSE, it calls the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method.</span></span> 
    
4. <span data-ttu-id="03475-130">Elimina o se mueve el mensaje.</span><span class="sxs-lookup"><span data-stu-id="03475-130">It deletes or moves the message.</span></span>
    
<span data-ttu-id="03475-131">Para obtener la estructura de **rectángulo** usada por la ventana de un formulario, llame a la función de Windows [GetWindowRect](https://msdn.microsoft.com/library/ms633519) .</span><span class="sxs-lookup"><span data-stu-id="03475-131">To obtain the **RECT** structure used by a form's window, call the Windows [GetWindowRect](https://msdn.microsoft.com/library/ms633519) function.</span></span> 
  
<span data-ttu-id="03475-132">Para obtener una lista de las interfaces relacionadas con los servidores de formulario, vea [Interfaces de formulario MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="03475-132">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="03475-133">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="03475-133">MFCMAPI reference</span></span>

<span data-ttu-id="03475-134">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="03475-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="03475-135">**File**</span><span class="sxs-lookup"><span data-stu-id="03475-135">**File**</span></span>|<span data-ttu-id="03475-136">**Función**</span><span class="sxs-lookup"><span data-stu-id="03475-136">**Function**</span></span>|<span data-ttu-id="03475-137">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="03475-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="03475-138">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="03475-138">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="03475-139">CMyMAPIFormViewer::DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="03475-139">CMyMAPIFormViewer::DeleteMessage</span></span>  <br/> |<span data-ttu-id="03475-140">No se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="03475-140">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="03475-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="03475-141">See also</span></span>



[<span data-ttu-id="03475-142">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="03475-142">IMAPIMessageSite::GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md)
  
[<span data-ttu-id="03475-143">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="03475-143">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="03475-144">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="03475-144">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="03475-145">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="03475-145">IPersistMessage::Save</span></span>](ipersistmessage-save.md)
  
[<span data-ttu-id="03475-146">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="03475-146">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="03475-147">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="03475-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="03475-148">Interfaces de formulario de MAPI</span><span class="sxs-lookup"><span data-stu-id="03475-148">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

