---
title: IMAPIMessageSiteSubmitMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.SubmitMessage
api_type:
- COM
ms.assetid: 6b14c383-8bc6-4e86-bd92-0500272af40d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 496732e334d2d39672048dd1a02346aaee4b70e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417031"
---
# <a name="imapimessagesitesubmitmessage"></a><span data-ttu-id="b9d9b-103">IMAPIMessageSite::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="b9d9b-103">IMAPIMessageSite::SubmitMessage</span></span>

  
  
<span data-ttu-id="b9d9b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9d9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b9d9b-105">Solicita que el mensaje actual se ponga en cola para su entrega.</span><span class="sxs-lookup"><span data-stu-id="b9d9b-105">Requests that the current message be queued for delivery.</span></span>
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="b9d9b-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="b9d9b-106">Parameters</span></span>

 <span data-ttu-id="b9d9b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b9d9b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="b9d9b-108">a Una máscara de máscara de marcadores que controla cómo se envía un mensaje.</span><span class="sxs-lookup"><span data-stu-id="b9d9b-108">[in] A bitmask of flags that controls how a message is submitted.</span></span> <span data-ttu-id="b9d9b-109">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="b9d9b-109">The following flag can be set:</span></span>
    
<span data-ttu-id="b9d9b-110">FORCE_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="b9d9b-110">FORCE_SUBMIT</span></span> 
  
> <span data-ttu-id="b9d9b-111">MAPI debe enviar el mensaje incluso si es posible que no se envíe inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="b9d9b-111">MAPI should submit the message even if it might not be sent immediately.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b9d9b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b9d9b-112">Return value</span></span>

<span data-ttu-id="b9d9b-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="b9d9b-113">S_OK</span></span> 
  
> <span data-ttu-id="b9d9b-114">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="b9d9b-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b9d9b-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b9d9b-115">Remarks</span></span>

<span data-ttu-id="b9d9b-116">Los objetos de formulario llaman al método **IMAPIMessageSite:: SubmitMessage** para solicitar que un mensaje se ponga en la cola para su entrega.</span><span class="sxs-lookup"><span data-stu-id="b9d9b-116">Form objects call the **IMAPIMessageSite::SubmitMessage** method to request that a message be queued for delivery.</span></span> <span data-ttu-id="b9d9b-117">El sitio del mensaje debe llamar al método [IPersistMessage:: HandsOffMessage](ipersistmessage-handsoffmessage.md) antes de enviar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="b9d9b-117">The message site should call the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method before submitting the message.</span></span> <span data-ttu-id="b9d9b-118">No es necesario que el mensaje se haya guardado previamente porque **SubmitMessage** debe hacer que se guarde el mensaje si se ha modificado el mensaje.</span><span class="sxs-lookup"><span data-stu-id="b9d9b-118">The message does not need to have been previously saved, because **SubmitMessage** should cause the message to be saved if the message has been modified.</span></span> <span data-ttu-id="b9d9b-119">Después de la devolución de **SubmitMessage**, el formulario debe comprobar un mensaje actual y, a continuación, descartarse si no hay ninguno.</span><span class="sxs-lookup"><span data-stu-id="b9d9b-119">After the return of **SubmitMessage**, the form must check for a current message and then dismiss itself if none exists.</span></span> 
  
<span data-ttu-id="b9d9b-120">Para obtener una lista de las interfaces relacionadas con los servidores de formularios, consulte [MAPI Form interfaces](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="b9d9b-120">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b9d9b-121">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b9d9b-121">MFCMAPI reference</span></span>

<span data-ttu-id="b9d9b-122">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="b9d9b-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b9d9b-123">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="b9d9b-123">**File**</span></span>|<span data-ttu-id="b9d9b-124">**Función**</span><span class="sxs-lookup"><span data-stu-id="b9d9b-124">**Function**</span></span>|<span data-ttu-id="b9d9b-125">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="b9d9b-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b9d9b-126">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="b9d9b-126">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="b9d9b-127">CMyMAPIFormViewer:: SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="b9d9b-127">CMyMAPIFormViewer::SubmitMessage</span></span>  <br/> |<span data-ttu-id="b9d9b-128">MFCMAPI usa el método **IMAPIMessageSite:: SubmitMessage** para guardar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="b9d9b-128">MFCMAPI uses the **IMAPIMessageSite::SubmitMessage** method to save the message.</span></span> <span data-ttu-id="b9d9b-129">En primer lugar, llama al método **IPersistMessage:: HandsOffMessage** y, a continuación, llama a **SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="b9d9b-129">First, it calls the **IPersistMessage::HandsOffMessage** method, and then it calls **SubmitMessage**.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b9d9b-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="b9d9b-130">See also</span></span>



[<span data-ttu-id="b9d9b-131">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="b9d9b-131">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="b9d9b-132">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b9d9b-132">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="b9d9b-133">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="b9d9b-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="b9d9b-134">Interfaces de formulario de MAPI</span><span class="sxs-lookup"><span data-stu-id="b9d9b-134">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

