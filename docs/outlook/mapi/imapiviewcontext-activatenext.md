---
title: IMAPIViewContextActivateNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.ActivateNext
api_type:
- COM
ms.assetid: 25ce90ac-526e-48a0-9edb-bd266375d4f4
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5b10f744e3033aab63820e4cd5e414f4c01c27cf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410619"
---
# <a name="imapiviewcontextactivatenext"></a><span data-ttu-id="ebb0d-103">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="ebb0d-103">IMAPIViewContext::ActivateNext</span></span>

<span data-ttu-id="ebb0d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ebb0d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ebb0d-105">Activa el mensaje siguiente o anterior en el orden de vista.</span><span class="sxs-lookup"><span data-stu-id="ebb0d-105">Activates the next or previous message in the view order.</span></span> 
  
```cpp
HRESULT ActivateNext(
ULONG ulDir,
LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="ebb0d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ebb0d-106">Parameters</span></span>

<span data-ttu-id="ebb0d-107">_ulDir_</span><span class="sxs-lookup"><span data-stu-id="ebb0d-107">_ulDir_</span></span>
  
> <span data-ttu-id="ebb0d-108">[entrada] Marcas de estado que dan información sobre el mensaje que se activará.</span><span class="sxs-lookup"><span data-stu-id="ebb0d-108">[in] Status flags giving information about the message to be activated.</span></span> <span data-ttu-id="ebb0d-109">Las opciones de marca válidas son:</span><span class="sxs-lookup"><span data-stu-id="ebb0d-109">Valid flag settings are:</span></span>
    
  - <span data-ttu-id="ebb0d-110">VCDIR_CATEGORY: el visor debe activar un mensaje en otra categoría de la vista.</span><span class="sxs-lookup"><span data-stu-id="ebb0d-110">VCDIR_CATEGORY: The viewer should activate a message in another category of the view.</span></span> <span data-ttu-id="ebb0d-111">El mensaje que se activará es:</span><span class="sxs-lookup"><span data-stu-id="ebb0d-111">The message to be activated is:</span></span> 
        
    - <span data-ttu-id="ebb0d-112">El primer mensaje de la siguiente categoría de vista si esta marca es **OR** ed con VCDIR_NEXT.</span><span class="sxs-lookup"><span data-stu-id="ebb0d-112">The first message in the next view category if this flag is **OR** ed with VCDIR_NEXT.</span></span> 
        
    - <span data-ttu-id="ebb0d-113">El último mensaje de la categoría de vista anterior si esta marca es **OR** con VCDIR_PREV y se expande la categoría anterior.</span><span class="sxs-lookup"><span data-stu-id="ebb0d-113">The last message in the previous view category if this flag is **OR** ed with VCDIR_PREV and the previous category is expanded.</span></span> 
        
    - <span data-ttu-id="ebb0d-114">El primer mensaje de la categoría de vista anterior si esta marca es **OR** ed con VCDIR_PREV y la categoría anterior no se expande.</span><span class="sxs-lookup"><span data-stu-id="ebb0d-114">The first message in the previous view category if this flag is **OR** ed with VCDIR_PREV and the previous category is not expanded.</span></span> <span data-ttu-id="ebb0d-115">En este caso, la categoría anterior se somete a una expansión automática.</span><span class="sxs-lookup"><span data-stu-id="ebb0d-115">In this case the previous category undergoes automatic expansion.</span></span> 
        
  - <span data-ttu-id="ebb0d-116">VCDIR_DELETE: el visor debe activar el mensaje siguiente o anterior porque se ha eliminado el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="ebb0d-116">VCDIR_DELETE: The viewer should activate the next or previous message because the current message has been deleted.</span></span> 
        
  - <span data-ttu-id="ebb0d-117">VCDIR_MOVE: el visor debe activar el mensaje siguiente o anterior porque se ha movido el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="ebb0d-117">VCDIR_MOVE: The viewer should activate the next or previous message because the current message has been moved.</span></span> 
        
  - <span data-ttu-id="ebb0d-118">VCDIR_NEXT: el visor debe activar el siguiente mensaje en el orden de vista.</span><span class="sxs-lookup"><span data-stu-id="ebb0d-118">VCDIR_NEXT: The viewer should activate the next message in the view order.</span></span> 
        
  - <span data-ttu-id="ebb0d-119">VCDIR_PREV: el visor debe activar el mensaje anterior en el orden de vista.</span><span class="sxs-lookup"><span data-stu-id="ebb0d-119">VCDIR_PREV: The viewer should activate the previous message in the view order.</span></span> 
        
  - <span data-ttu-id="ebb0d-120">VCDIR_UNREAD: el visor debe activar el mensaje no leído siguiente o anterior en el orden de vista.</span><span class="sxs-lookup"><span data-stu-id="ebb0d-120">VCDIR_UNREAD: The viewer should activate the next or previous unread message in the view order.</span></span> 
    
<span data-ttu-id="ebb0d-121">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="ebb0d-121">_prcPosRect_</span></span>
  
> <span data-ttu-id="ebb0d-122">[entrada] Puntero a una estructura **RECT** de Windows que contiene el tamaño y la posición de la ventana que se va a usar para mostrar el mensaje activado.</span><span class="sxs-lookup"><span data-stu-id="ebb0d-122">[in] Pointer to a Windows **RECT** structure containing the size and position of the window to be used to display the activated message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ebb0d-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ebb0d-123">Return value</span></span>

<span data-ttu-id="ebb0d-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="ebb0d-124">S_OK</span></span> 
  
> <span data-ttu-id="ebb0d-125">El mensaje se activó correctamente.</span><span class="sxs-lookup"><span data-stu-id="ebb0d-125">The message was activated successfully.</span></span> 
    
<span data-ttu-id="ebb0d-126">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="ebb0d-126">S_FALSE</span></span> 
  
> <span data-ttu-id="ebb0d-127">El mensaje se activó correctamente, pero se abrió un tipo de formulario diferente en el proceso.</span><span class="sxs-lookup"><span data-stu-id="ebb0d-127">The message was activated successfully, but a different type of form was opened in the process.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ebb0d-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ebb0d-128">Remarks</span></span>

<span data-ttu-id="ebb0d-129">Los objetos de formulario llaman **al método IMAPIViewContext::ActivateNext** para cambiar el mensaje que se muestra al usuario.</span><span class="sxs-lookup"><span data-stu-id="ebb0d-129">Form objects call the **IMAPIViewContext::ActivateNext** method to change what message is displayed to the user.</span></span> <span data-ttu-id="ebb0d-130">El valor pasado en el  _parámetro ulDir_ indica qué mensaje debe activarse y, en algunos casos, por qué.</span><span class="sxs-lookup"><span data-stu-id="ebb0d-130">The value passed in the  _ulDir_ parameter indicates which message should be activated and, in some cases, why.</span></span> <span data-ttu-id="ebb0d-131">Las VCDIR_NEXT y VCDIR_PREVIOUS correspondientes a los usuarios que  eligen  el comando Siguiente o Anterior en una vista, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="ebb0d-131">The VCDIR_NEXT and VCDIR_PREVIOUS flags correspond to users choosing the **Next** or **Previous** command in a view, respectively.</span></span> <span data-ttu-id="ebb0d-132">Estas operaciones normalmente corresponden a mover hacia arriba o hacia abajo un mensaje en la lista de mensajes del visor de formularios.</span><span class="sxs-lookup"><span data-stu-id="ebb0d-132">These operations usually correspond to moving up or down one message in the form viewer's list of messages.</span></span> 
  
<span data-ttu-id="ebb0d-133">Los VCDIR_DELETE VCDIR_MOVE [imapiMessageSite::D los métodos IMAPIMessageSite::D e](imapimessagesite-deletemessage.md) [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) se establecen respectivamente.</span><span class="sxs-lookup"><span data-stu-id="ebb0d-133">The VCDIR_DELETE and VCDIR_MOVE flags are set by the [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) and [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) methods, respectively.</span></span> <span data-ttu-id="ebb0d-134">Las implementaciones de estos métodos llaman a **ActivateNext** con la  dirección adecuada y, a continuación, realizan la operación solicitada en el mensaje si no se ha producir un error en la llamada ActivateNext.</span><span class="sxs-lookup"><span data-stu-id="ebb0d-134">Implementations of these methods call **ActivateNext** with the appropriate direction and then perform the requested operation on the message if the **ActivateNext** call did not fail.</span></span> <span data-ttu-id="ebb0d-135">Los visores de formularios normalmente permiten a los usuarios especificar la dirección para moverse en la lista de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ebb0d-135">Form viewers typically enable users to specify the direction to move in the message list.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ebb0d-136">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="ebb0d-136">Notes to implementers</span></span>

<span data-ttu-id="ebb0d-137">La implementación de [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) hace que el mensaje siguiente o anterior en la carpeta, según el valor de  _ulDir_, el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="ebb0d-137">Your implementation of [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) makes the next or previous message in the folder, depending on the value of  _ulDir_, the current message.</span></span> <span data-ttu-id="ebb0d-138">Después **de que ActivateNext** vuelva, llame a [IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md) para obtener un puntero al mensaje recién activado.</span><span class="sxs-lookup"><span data-stu-id="ebb0d-138">After **ActivateNext** returns, call [IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md) to get a pointer to the newly activated message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ebb0d-139">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="ebb0d-139">Notes to callers</span></span>

<span data-ttu-id="ebb0d-140">Si **ActivateNext** devuelve S_FALSE, o si un mensaje actual no está presente, realice el procedimiento de cierre normal que debe incluir llamar al método [IMAPIForm::ShutdownForm del](imapiform-shutdownform.md) formulario.</span><span class="sxs-lookup"><span data-stu-id="ebb0d-140">If **ActivateNext** returns S_FALSE, or if a current message is not present, perform your normal shutdown procedure which should include calling your form's [IMAPIForm::ShutdownForm](imapiform-shutdownform.md) method.</span></span> <span data-ttu-id="ebb0d-141">Si se muestra un mensaje siguiente o anterior, use el rectángulo de ventana pasado en el  _parámetro prcPosRect_ para mostrarlo.</span><span class="sxs-lookup"><span data-stu-id="ebb0d-141">If a next or previous message is displayed, use the window rectangle passed in the  _prcPosRect_ parameter to display it.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ebb0d-142">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ebb0d-142">MFCMAPI reference</span></span>

<span data-ttu-id="ebb0d-143">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="ebb0d-143">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ebb0d-144">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="ebb0d-144">**File**</span></span>|<span data-ttu-id="ebb0d-145">**Función**</span><span class="sxs-lookup"><span data-stu-id="ebb0d-145">**Function**</span></span>|<span data-ttu-id="ebb0d-146">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="ebb0d-146">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ebb0d-147">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="ebb0d-147">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="ebb0d-148">CMyMAPIFormViewer::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="ebb0d-148">CMyMAPIFormViewer::ActivateNext</span></span>  <br/> |<span data-ttu-id="ebb0d-149">MFCMAPI implementa el **método IMAPIViewContext::ActivateNext** en esta función.</span><span class="sxs-lookup"><span data-stu-id="ebb0d-149">MFCMAPI implements the **IMAPIViewContext::ActivateNext** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ebb0d-150">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ebb0d-150">See also</span></span>

- [<span data-ttu-id="ebb0d-151">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="ebb0d-151">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
- [<span data-ttu-id="ebb0d-152">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ebb0d-152">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
- [<span data-ttu-id="ebb0d-153">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="ebb0d-153">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

