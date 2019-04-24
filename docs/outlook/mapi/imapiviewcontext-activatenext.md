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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351159"
---
# <a name="imapiviewcontextactivatenext"></a><span data-ttu-id="ff5f6-103">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="ff5f6-103">IMAPIViewContext::ActivateNext</span></span>

<span data-ttu-id="ff5f6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff5f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff5f6-105">Activa el mensaje siguiente o anterior en el orden de vista.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-105">Activates the next or previous message in the view order.</span></span> 
  
```cpp
HRESULT ActivateNext(
ULONG ulDir,
LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="ff5f6-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="ff5f6-106">Parameters</span></span>

<span data-ttu-id="ff5f6-107">_ulDir_</span><span class="sxs-lookup"><span data-stu-id="ff5f6-107">_ulDir_</span></span>
  
> <span data-ttu-id="ff5f6-108">a Indicadores de estado que proporcionan información sobre el mensaje que se va a activar.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-108">[in] Status flags giving information about the message to be activated.</span></span> <span data-ttu-id="ff5f6-109">La configuración válida del indicador es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="ff5f6-109">Valid flag settings are:</span></span>
    
  - <span data-ttu-id="ff5f6-110">VCDIR_CATEGORY: el visor debe activar un mensaje en otra categoría de la vista.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-110">VCDIR_CATEGORY: The viewer should activate a message in another category of the view.</span></span> <span data-ttu-id="ff5f6-111">El mensaje que se va a activar es:</span><span class="sxs-lookup"><span data-stu-id="ff5f6-111">The message to be activated is:</span></span> 
        
    - <span data-ttu-id="ff5f6-112">El primer mensaje de la siguiente categoría de vista si esta marca es **o**Ed con VCDIR_NEXT.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-112">The first message in the next view category if this flag is **OR**ed with VCDIR_NEXT.</span></span> 
        
    - <span data-ttu-id="ff5f6-113">Último mensaje de la categoría de vista anterior si este indicador es **o**Ed con VCDIR_PREV y se expande la categoría anterior.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-113">The last message in the previous view category if this flag is **OR**ed with VCDIR_PREV and the previous category is expanded.</span></span> 
        
    - <span data-ttu-id="ff5f6-114">El primer mensaje de la categoría de vista anterior si esta marca es **o**Ed con VCDIR_PREV y la categoría anterior no se expande.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-114">The first message in the previous view category if this flag is **OR**ed with VCDIR_PREV and the previous category is not expanded.</span></span> <span data-ttu-id="ff5f6-115">En este caso, la categoría anterior sufre una expansión automática.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-115">In this case the previous category undergoes automatic expansion.</span></span> 
        
  - <span data-ttu-id="ff5f6-116">VCDIR_DELETE: el visor debe activar el mensaje siguiente o anterior porque se ha eliminado el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-116">VCDIR_DELETE: The viewer should activate the next or previous message because the current message has been deleted.</span></span> 
        
  - <span data-ttu-id="ff5f6-117">VCDIR_MOVE: el visor debe activar el mensaje siguiente o anterior porque el mensaje actual se ha movido.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-117">VCDIR_MOVE: The viewer should activate the next or previous message because the current message has been moved.</span></span> 
        
  - <span data-ttu-id="ff5f6-118">VCDIR_NEXT: el visor debe activar el siguiente mensaje en el orden de vista.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-118">VCDIR_NEXT: The viewer should activate the next message in the view order.</span></span> 
        
  - <span data-ttu-id="ff5f6-119">VCDIR_PREV: el visor debe activar el mensaje anterior en el orden de la vista.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-119">VCDIR_PREV: The viewer should activate the previous message in the view order.</span></span> 
        
  - <span data-ttu-id="ff5f6-120">VCDIR_UNREAD: el visor debe activar el mensaje no leído siguiente o anterior en el orden de vista.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-120">VCDIR_UNREAD: The viewer should activate the next or previous unread message in the view order.</span></span> 
    
<span data-ttu-id="ff5f6-121">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="ff5f6-121">_prcPosRect_</span></span>
  
> <span data-ttu-id="ff5f6-122">a Puntero a una estructura de Windows **Rect** que contiene el tamaño y la posición de la ventana que se va a usar para mostrar el mensaje activado.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-122">[in] Pointer to a Windows **RECT** structure containing the size and position of the window to be used to display the activated message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ff5f6-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ff5f6-123">Return value</span></span>

<span data-ttu-id="ff5f6-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="ff5f6-124">S_OK</span></span> 
  
> <span data-ttu-id="ff5f6-125">El mensaje se activó correctamente.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-125">The message was activated successfully.</span></span> 
    
<span data-ttu-id="ff5f6-126">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="ff5f6-126">S_FALSE</span></span> 
  
> <span data-ttu-id="ff5f6-127">El mensaje se activó correctamente, pero se abrió un tipo diferente de formulario en el proceso.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-127">The message was activated successfully, but a different type of form was opened in the process.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ff5f6-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ff5f6-128">Remarks</span></span>

<span data-ttu-id="ff5f6-129">Los objetos de formulario llaman al método **IMAPIViewContext:: ActivateNext** para cambiar el mensaje que se muestra al usuario.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-129">Form objects call the **IMAPIViewContext::ActivateNext** method to change what message is displayed to the user.</span></span> <span data-ttu-id="ff5f6-130">El valor que se pasa en el parámetro _ulDir_ indica qué mensaje debe activarse y, en algunos casos, por qué.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-130">The value passed in the  _ulDir_ parameter indicates which message should be activated and, in some cases, why.</span></span> <span data-ttu-id="ff5f6-131">Los indicadores VCDIR_NEXT y VCDIR_PREVIOUS corresponden a los usuarios que eligen el comando **siguiente** o **anterior** en una vista, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-131">The VCDIR_NEXT and VCDIR_PREVIOUS flags correspond to users choosing the **Next** or **Previous** command in a view, respectively.</span></span> <span data-ttu-id="ff5f6-132">Estas operaciones suelen corresponderse para subir o bajar un mensaje en la lista de mensajes del visor de formulario.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-132">These operations usually correspond to moving up or down one message in the form viewer's list of messages.</span></span> 
  
<span data-ttu-id="ff5f6-133">Los indicadores VCDIR_DELETE y VCDIR_MOVE los establecen los métodos [IMAPIMessageSite::D eletemessage](imapimessagesite-deletemessage.md) y [IMAPIMessageSite:: MoveMessage](imapimessagesite-movemessage.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-133">The VCDIR_DELETE and VCDIR_MOVE flags are set by the [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) and [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) methods, respectively.</span></span> <span data-ttu-id="ff5f6-134">Las implementaciones de estos métodos llaman a **ActivateNext** con la dirección adecuada y, a continuación, realizan la operación solicitada en el mensaje si la llamada **ActivateNext** no se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-134">Implementations of these methods call **ActivateNext** with the appropriate direction and then perform the requested operation on the message if the **ActivateNext** call did not fail.</span></span> <span data-ttu-id="ff5f6-135">Los visores de formularios normalmente permiten a los usuarios especificar la dirección que se va a mover en la lista de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-135">Form viewers typically enable users to specify the direction to move in the message list.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ff5f6-136">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="ff5f6-136">Notes to implementers</span></span>

<span data-ttu-id="ff5f6-137">La implementación de [IMAPIViewContext:: ActivateNext](imapiviewcontext-activatenext.md) hace que el mensaje siguiente o anterior de la carpeta, según el valor de _ulDir_, el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-137">Your implementation of [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) makes the next or previous message in the folder, depending on the value of  _ulDir_, the current message.</span></span> <span data-ttu-id="ff5f6-138">Una vez que **ActivateNext** devuelve un, llame a [IMAPIMessageSite:: GetMessage](imapimessagesite-getmessage.md) para obtener un puntero al mensaje recién activado.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-138">After **ActivateNext** returns, call [IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md) to get a pointer to the newly activated message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ff5f6-139">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="ff5f6-139">Notes to callers</span></span>

<span data-ttu-id="ff5f6-140">Si **ActivateNext** devuelve S_FALSE, o si no hay un mensaje actual, realice el procedimiento de cierre normal que deba incluir una llamada al método [IMAPIForm:: ShutdownForm](imapiform-shutdownform.md) del formulario.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-140">If **ActivateNext** returns S_FALSE, or if a current message is not present, perform your normal shutdown procedure which should include calling your form's [IMAPIForm::ShutdownForm](imapiform-shutdownform.md) method.</span></span> <span data-ttu-id="ff5f6-141">Si se muestra un mensaje próximo o anterior, use el rectángulo de la ventana que se pasa en el parámetro _prcPosRect_ para mostrarlo.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-141">If a next or previous message is displayed, use the window rectangle passed in the  _prcPosRect_ parameter to display it.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ff5f6-142">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ff5f6-142">MFCMAPI reference</span></span>

<span data-ttu-id="ff5f6-143">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-143">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ff5f6-144">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="ff5f6-144">**File**</span></span>|<span data-ttu-id="ff5f6-145">**Función**</span><span class="sxs-lookup"><span data-stu-id="ff5f6-145">**Function**</span></span>|<span data-ttu-id="ff5f6-146">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="ff5f6-146">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ff5f6-147">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="ff5f6-147">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="ff5f6-148">CMyMAPIFormViewer:: ActivateNext</span><span class="sxs-lookup"><span data-stu-id="ff5f6-148">CMyMAPIFormViewer::ActivateNext</span></span>  <br/> |<span data-ttu-id="ff5f6-149">MFCMAPI implementa el método **IMAPIViewContext:: ActivateNext** en esta función.</span><span class="sxs-lookup"><span data-stu-id="ff5f6-149">MFCMAPI implements the **IMAPIViewContext::ActivateNext** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ff5f6-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff5f6-150">See also</span></span>

- [<span data-ttu-id="ff5f6-151">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="ff5f6-151">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
- [<span data-ttu-id="ff5f6-152">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ff5f6-152">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
- [<span data-ttu-id="ff5f6-153">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="ff5f6-153">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

