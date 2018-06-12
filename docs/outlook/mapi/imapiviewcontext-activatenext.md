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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 150a0c6eb7efa83f5ff1d12d915351bf5ca9d45a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817642"
---
# <a name="imapiviewcontextactivatenext"></a><span data-ttu-id="d4d64-103">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="d4d64-103">IMAPIViewContext::ActivateNext</span></span>

<span data-ttu-id="d4d64-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d4d64-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d4d64-105">Activa el mensaje siguiente o anterior en el orden de la vista.</span><span class="sxs-lookup"><span data-stu-id="d4d64-105">Activates the next or previous message in the view order.</span></span> 
  
```cpp
HRESULT ActivateNext(
ULONG ulDir,
LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="d4d64-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d4d64-106">Parameters</span></span>

<span data-ttu-id="d4d64-107">_ulDir_</span><span class="sxs-lookup"><span data-stu-id="d4d64-107">_ulDir_</span></span>
  
> <span data-ttu-id="d4d64-108">[entrada] Indicadores de estado que proporciona información acerca del mensaje que se va a activar.</span><span class="sxs-lookup"><span data-stu-id="d4d64-108">[in] Status flags giving information about the message to be activated.</span></span> <span data-ttu-id="d4d64-109">Valores de indicador válidos son:</span><span class="sxs-lookup"><span data-stu-id="d4d64-109">Valid flag settings are:</span></span>
    
  - <span data-ttu-id="d4d64-110">VCDIR_CATEGORY: El Visor debe activar un mensaje en otra categoría de la vista.</span><span class="sxs-lookup"><span data-stu-id="d4d64-110">VCDIR_CATEGORY: The viewer should activate a message in another category of the view.</span></span> <span data-ttu-id="d4d64-111">El mensaje que se va a activar es:</span><span class="sxs-lookup"><span data-stu-id="d4d64-111">The message to be activated is:</span></span> 
        
    - <span data-ttu-id="d4d64-112">El primer mensaje de la categoría vista siguiente si este marcador es ed **o**con VCDIR_NEXT.</span><span class="sxs-lookup"><span data-stu-id="d4d64-112">The first message in the next view category if this flag is **OR**ed with VCDIR_NEXT.</span></span> 
        
    - <span data-ttu-id="d4d64-113">Se expande el último mensaje de la categoría de la vista anterior, si este marcador es **OR**ed con VCDIR_PREV y la categoría anterior.</span><span class="sxs-lookup"><span data-stu-id="d4d64-113">The last message in the previous view category if this flag is **OR**ed with VCDIR_PREV and the previous category is expanded.</span></span> 
        
    - <span data-ttu-id="d4d64-114">No se expande el primer mensaje de la categoría de la vista anterior, si este marcador es **OR**ed con VCDIR_PREV y la categoría anterior.</span><span class="sxs-lookup"><span data-stu-id="d4d64-114">The first message in the previous view category if this flag is **OR**ed with VCDIR_PREV and the previous category is not expanded.</span></span> <span data-ttu-id="d4d64-115">En este caso la categoría anterior se somete a la expansión automática.</span><span class="sxs-lookup"><span data-stu-id="d4d64-115">In this case the previous category undergoes automatic expansion.</span></span> 
        
  - <span data-ttu-id="d4d64-116">VCDIR_DELETE: El Visor debe activar el mensaje siguiente o anterior porque se ha eliminado el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="d4d64-116">VCDIR_DELETE: The viewer should activate the next or previous message because the current message has been deleted.</span></span> 
        
  - <span data-ttu-id="d4d64-117">VCDIR_MOVE: El Visor debe activar el mensaje siguiente o anterior porque se ha movido el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="d4d64-117">VCDIR_MOVE: The viewer should activate the next or previous message because the current message has been moved.</span></span> 
        
  - <span data-ttu-id="d4d64-118">VCDIR_NEXT: El Visor debe activar el mensaje siguiente en el orden de la vista.</span><span class="sxs-lookup"><span data-stu-id="d4d64-118">VCDIR_NEXT: The viewer should activate the next message in the view order.</span></span> 
        
  - <span data-ttu-id="d4d64-119">VCDIR_PREV: El Visor debe activar el mensaje anterior en el orden de la vista.</span><span class="sxs-lookup"><span data-stu-id="d4d64-119">VCDIR_PREV: The viewer should activate the previous message in the view order.</span></span> 
        
  - <span data-ttu-id="d4d64-120">VCDIR_UNREAD: El Visor debe activar el mensaje no leído siguiente o anterior en el orden de la vista.</span><span class="sxs-lookup"><span data-stu-id="d4d64-120">VCDIR_UNREAD: The viewer should activate the next or previous unread message in the view order.</span></span> 
    
<span data-ttu-id="d4d64-121">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="d4d64-121">_prcPosRect_</span></span>
  
> <span data-ttu-id="d4d64-122">[entrada] Puntero a un **rectángulo** de Windows estructura que contiene el tamaño y la posición de la ventana que se usará para mostrar el mensaje activado.</span><span class="sxs-lookup"><span data-stu-id="d4d64-122">[in] Pointer to a Windows **RECT** structure containing the size and position of the window to be used to display the activated message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d4d64-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d4d64-123">Return value</span></span>

<span data-ttu-id="d4d64-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="d4d64-124">S_OK</span></span> 
  
> <span data-ttu-id="d4d64-125">El mensaje se ha activado correctamente.</span><span class="sxs-lookup"><span data-stu-id="d4d64-125">The message was activated successfully.</span></span> 
    
<span data-ttu-id="d4d64-126">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="d4d64-126">S_FALSE</span></span> 
  
> <span data-ttu-id="d4d64-127">El mensaje se ha activado correctamente, pero se abrió un tipo diferente del formulario en el proceso.</span><span class="sxs-lookup"><span data-stu-id="d4d64-127">The message was activated successfully, but a different type of form was opened in the process.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d4d64-128">Notas</span><span class="sxs-lookup"><span data-stu-id="d4d64-128">Remarks</span></span>

<span data-ttu-id="d4d64-129">Objetos de formulario llamar al método **IMAPIViewContext::ActivateNext** para cambiar qué mensaje se muestra al usuario.</span><span class="sxs-lookup"><span data-stu-id="d4d64-129">Form objects call the **IMAPIViewContext::ActivateNext** method to change what message is displayed to the user.</span></span> <span data-ttu-id="d4d64-130">El valor que se pasa en el parámetro _ulDir_ indica qué mensaje debe estar activado y, en algunos casos, por qué.</span><span class="sxs-lookup"><span data-stu-id="d4d64-130">The value passed in the  _ulDir_ parameter indicates which message should be activated and, in some cases, why.</span></span> <span data-ttu-id="d4d64-131">Los indicadores VCDIR_NEXT y VCDIR_PREVIOUS corresponden a los usuarios elegir el comando **siguiente** o **anterior** en una vista, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d4d64-131">The VCDIR_NEXT and VCDIR_PREVIOUS flags correspond to users choosing the **Next** or **Previous** command in a view, respectively.</span></span> <span data-ttu-id="d4d64-132">Estas operaciones normalmente corresponden a moverse hacia arriba o hacia abajo de un mensaje en la lista del Visor de formulario de mensajes.</span><span class="sxs-lookup"><span data-stu-id="d4d64-132">These operations usually correspond to moving up or down one message in the form viewer's list of messages.</span></span> 
  
<span data-ttu-id="d4d64-133">Los indicadores VCDIR_DELETE y VCDIR_MOVE se establecen por el [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) y los métodos [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d4d64-133">The VCDIR_DELETE and VCDIR_MOVE flags are set by the [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) and [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) methods, respectively.</span></span> <span data-ttu-id="d4d64-134">Implementaciones de estos métodos llame al método **ActivateNext** con la dirección apropiada y, a continuación, realizan la operación solicitada en el mensaje si la llamada **ActivateNext** no produjo un error.</span><span class="sxs-lookup"><span data-stu-id="d4d64-134">Implementations of these methods call **ActivateNext** with the appropriate direction and then perform the requested operation on the message if the **ActivateNext** call did not fail.</span></span> <span data-ttu-id="d4d64-135">Visores de formulario normalmente permiten a los usuarios especificar la dirección que desea mover en la lista de mensajes.</span><span class="sxs-lookup"><span data-stu-id="d4d64-135">Form viewers typically enable users to specify the direction to move in the message list.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d4d64-136">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="d4d64-136">Notes to implementers</span></span>

<span data-ttu-id="d4d64-137">La implementación de [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) hace que el mensaje siguiente o anterior en la carpeta, según el valor de _ulDir_, el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="d4d64-137">Your implementation of [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) makes the next or previous message in the folder, depending on the value of  _ulDir_, the current message.</span></span> <span data-ttu-id="d4d64-138">Una vez **ActivateNext** devuelve, llame a [IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md) para obtener un puntero al mensaje recién activado.</span><span class="sxs-lookup"><span data-stu-id="d4d64-138">After **ActivateNext** returns, call [IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md) to get a pointer to the newly activated message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d4d64-139">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="d4d64-139">Notes to callers</span></span>

<span data-ttu-id="d4d64-140">Si **ActivateNext** devuelve S_FALSE, o si no está presente un mensaje actual, realice el procedimiento de cierre normal que debe incluir una llamada a método de [IMAPIForm::ShutdownForm](imapiform-shutdownform.md) del formulario.</span><span class="sxs-lookup"><span data-stu-id="d4d64-140">If **ActivateNext** returns S_FALSE, or if a current message is not present, perform your normal shutdown procedure which should include calling your form's [IMAPIForm::ShutdownForm](imapiform-shutdownform.md) method.</span></span> <span data-ttu-id="d4d64-141">Si se muestra un mensaje siguiente o anterior, utilice el rectángulo de ventana que se pasa en el parámetro _prcPosRect_ para que se muestre.</span><span class="sxs-lookup"><span data-stu-id="d4d64-141">If a next or previous message is displayed, use the window rectangle passed in the  _prcPosRect_ parameter to display it.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d4d64-142">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d4d64-142">MFCMAPI reference</span></span>

<span data-ttu-id="d4d64-143">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="d4d64-143">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d4d64-144">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="d4d64-144">**File**</span></span>|<span data-ttu-id="d4d64-145">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="d4d64-145">**Function**</span></span>|<span data-ttu-id="d4d64-146">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="d4d64-146">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d4d64-147">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="d4d64-147">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="d4d64-148">CMyMAPIFormViewer::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="d4d64-148">CMyMAPIFormViewer::ActivateNext</span></span>  <br/> |<span data-ttu-id="d4d64-149">MFCMAPI implementa el método **IMAPIViewContext::ActivateNext** en esta función.</span><span class="sxs-lookup"><span data-stu-id="d4d64-149">MFCMAPI implements the **IMAPIViewContext::ActivateNext** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d4d64-150">Ver también</span><span class="sxs-lookup"><span data-stu-id="d4d64-150">See also</span></span>

- [<span data-ttu-id="d4d64-151">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="d4d64-151">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
- [<span data-ttu-id="d4d64-152">IMAPIViewContext: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d4d64-152">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
- [<span data-ttu-id="d4d64-153">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="d4d64-153">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

