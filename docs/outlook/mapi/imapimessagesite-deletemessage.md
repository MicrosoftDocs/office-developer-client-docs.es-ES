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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321416"
---
# <a name="imapimessagesitedeletemessage"></a><span data-ttu-id="78bfe-103">IMAPIMessageSite::DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="78bfe-103">IMAPIMessageSite::DeleteMessage</span></span>

  
  
<span data-ttu-id="78bfe-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78bfe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78bfe-105">Elimina el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="78bfe-105">Deletes the current message.</span></span>
  
```cpp
HRESULT DeleteMessage(
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="78bfe-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="78bfe-106">Parameters</span></span>

 <span data-ttu-id="78bfe-107">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="78bfe-107">_pViewContext_</span></span>
  
> <span data-ttu-id="78bfe-108">a Un puntero a un objeto de contexto de vista.</span><span class="sxs-lookup"><span data-stu-id="78bfe-108">[in] A pointer to a view context object.</span></span>
    
 <span data-ttu-id="78bfe-109">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="78bfe-109">_prcPosRect_</span></span>
  
> <span data-ttu-id="78bfe-110">a Un puntero a una estructura [Rect](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) que contiene el tamaño y la posición de la ventana del formulario actual.</span><span class="sxs-lookup"><span data-stu-id="78bfe-110">[in] A pointer to a [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) structure that contains the current form's window size and position.</span></span> <span data-ttu-id="78bfe-111">El siguiente formulario que se muestra también usa este rectángulo de la ventana.</span><span class="sxs-lookup"><span data-stu-id="78bfe-111">The next form displayed also uses this window rectangle.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="78bfe-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="78bfe-112">Return value</span></span>

<span data-ttu-id="78bfe-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="78bfe-113">S_OK</span></span> 
  
> <span data-ttu-id="78bfe-114">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="78bfe-114">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="78bfe-115">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="78bfe-115">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="78bfe-116">La operación no es compatible con este sitio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="78bfe-116">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="78bfe-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="78bfe-117">Remarks</span></span>

<span data-ttu-id="78bfe-118">Un objeto Form llama al método **IMAPIMessageSite::D eletemessage** para eliminar el mensaje que se muestra actualmente en el formulario.</span><span class="sxs-lookup"><span data-stu-id="78bfe-118">A form object calls the **IMAPIMessageSite::DeleteMessage** method to delete the message that the form is currently displaying.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="78bfe-119">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="78bfe-119">Notes to callers</span></span>

<span data-ttu-id="78bfe-120">Tras la devolución de **DeleteMessage**, los objetos de formulario deben comprobar si hay un nuevo mensaje y, a continuación, descartarse si no hay ninguno.</span><span class="sxs-lookup"><span data-stu-id="78bfe-120">Following the return of **DeleteMessage**, form objects must check for a new message and then dismiss themselves if none exists.</span></span> <span data-ttu-id="78bfe-121">Para determinar si el mensaje en el que se actuó **DeleteMessage** se eliminó o movió a una carpeta de **elementos eliminados** , un objeto de formulario puede llamar al método [IMAPIMessageSite:: GetSiteStatus](imapimessagesite-getsitestatus.md) para determinar si se ha devuelto la marca DELETE_IS_MOVE.</span><span class="sxs-lookup"><span data-stu-id="78bfe-121">To determine whether the message **DeleteMessage** acted on was deleted or moved to a **Deleted Items** folder, a form object can call the [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) method to determine whether the DELETE_IS_MOVE flag was returned.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="78bfe-122">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="78bfe-122">Notes to implementers</span></span>

<span data-ttu-id="78bfe-123">Si una implementación de Form Viewer del método **DeleteMessage** pasa al siguiente mensaje después de eliminar un mensaje, la implementación debe llamar al método [IMAPIViewContext:: ActivateNext](imapiviewcontext-activatenext.md) y pasar la marca VCDIR_DELETE antes de realizar la eliminación real.</span><span class="sxs-lookup"><span data-stu-id="78bfe-123">If a form viewer's implementation of the **DeleteMessage** method moves to the next message after it deletes a message, the implementation should call the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method and pass the VCDIR_DELETE flag before performing the actual deletion.</span></span> <span data-ttu-id="78bfe-124">Si la implementación de **DeleteMessage** del visor de formularios mueve el mensaje eliminado (por ejemplo, a una carpeta de **elementos eliminados** ), la implementación debe guardar los cambios en el mensaje si se modificó el mensaje.</span><span class="sxs-lookup"><span data-stu-id="78bfe-124">If a form viewer's implementation of **DeleteMessage** moves the deleted message (for example, to a **Deleted Items** folder), the implementation must save changes to the message if the message was modified.</span></span> 
  
<span data-ttu-id="78bfe-125">Una implementación típica de **DeleteMessage** realiza las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="78bfe-125">A typical implementation of **DeleteMessage** performs the following tasks:</span></span> 
  
1. <span data-ttu-id="78bfe-126">Si la implementación mueve el mensaje, llama al método [IPersistMessage:: Save](ipersistmessage-save.md) , pasando **null** en el parámetro _pMessage_ y **true** en el parámetro _fSameAsLoad_ .</span><span class="sxs-lookup"><span data-stu-id="78bfe-126">If the implementation is moving the message, it calls the [IPersistMessage::Save](ipersistmessage-save.md) method, passing **null** in the  _pMessage_ parameter and **true** in the  _fSameAsLoad_ parameter.</span></span> 
    
2. <span data-ttu-id="78bfe-127">Llama al método **IMAPIViewContext:: ActivateNext** , pasando la marca VCDIR_DELETE en el parámetro _ulDir_ .</span><span class="sxs-lookup"><span data-stu-id="78bfe-127">It calls the **IMAPIViewContext::ActivateNext** method, passing the VCDIR_DELETE flag in the  _ulDir_ parameter.</span></span> 
    
3. <span data-ttu-id="78bfe-128">Si la llamada a **ActivateNext** produce un error, devuelve.</span><span class="sxs-lookup"><span data-stu-id="78bfe-128">If the **ActivateNext** call fails, it returns.</span></span> <span data-ttu-id="78bfe-129">Si **ActivateNext** devuelve S_FALSE, llama al método [IPersistMessage:: HandsOffMessage](ipersistmessage-handsoffmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="78bfe-129">If **ActivateNext** returns S_FALSE, it calls the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method.</span></span> 
    
4. <span data-ttu-id="78bfe-130">Elimina o mueve el mensaje.</span><span class="sxs-lookup"><span data-stu-id="78bfe-130">It deletes or moves the message.</span></span>
    
<span data-ttu-id="78bfe-131">Para obtener la estructura **Rect** que utiliza la ventana de un formulario, llame a la función [GetWindowRect](https://msdn.microsoft.com/library/ms633519) de Windows.</span><span class="sxs-lookup"><span data-stu-id="78bfe-131">To obtain the **RECT** structure used by a form's window, call the Windows [GetWindowRect](https://msdn.microsoft.com/library/ms633519) function.</span></span> 
  
<span data-ttu-id="78bfe-132">Para obtener una lista de las interfaces relacionadas con los servidores de formularios, consulte [MAPI Form interfaces](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="78bfe-132">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="78bfe-133">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="78bfe-133">MFCMAPI reference</span></span>

<span data-ttu-id="78bfe-134">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="78bfe-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="78bfe-135">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="78bfe-135">**File**</span></span>|<span data-ttu-id="78bfe-136">**Función**</span><span class="sxs-lookup"><span data-stu-id="78bfe-136">**Function**</span></span>|<span data-ttu-id="78bfe-137">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="78bfe-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="78bfe-138">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="78bfe-138">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="78bfe-139">CMyMAPIFormViewer::D eleteMessage</span><span class="sxs-lookup"><span data-stu-id="78bfe-139">CMyMAPIFormViewer::DeleteMessage</span></span>  <br/> |<span data-ttu-id="78bfe-140">No implementado.</span><span class="sxs-lookup"><span data-stu-id="78bfe-140">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="78bfe-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="78bfe-141">See also</span></span>



[<span data-ttu-id="78bfe-142">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="78bfe-142">IMAPIMessageSite::GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md)
  
[<span data-ttu-id="78bfe-143">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="78bfe-143">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="78bfe-144">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="78bfe-144">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="78bfe-145">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="78bfe-145">IPersistMessage::Save</span></span>](ipersistmessage-save.md)
  
[<span data-ttu-id="78bfe-146">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="78bfe-146">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="78bfe-147">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="78bfe-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="78bfe-148">Interfaces de formulario de MAPI</span><span class="sxs-lookup"><span data-stu-id="78bfe-148">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

