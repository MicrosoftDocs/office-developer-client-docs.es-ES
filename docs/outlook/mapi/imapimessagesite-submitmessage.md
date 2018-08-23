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
ms.openlocfilehash: 587b8bbb7ac25a7977d8962535f1909464ffc248
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571104"
---
# <a name="imapimessagesitesubmitmessage"></a><span data-ttu-id="f2cd7-103">IMAPIMessageSite::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="f2cd7-103">IMAPIMessageSite::SubmitMessage</span></span>

  
  
<span data-ttu-id="f2cd7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2cd7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2cd7-105">Solicitudes que se ponen en cola en el mensaje actual para la entrega.</span><span class="sxs-lookup"><span data-stu-id="f2cd7-105">Requests that the current message be queued for delivery.</span></span>
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="f2cd7-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="f2cd7-106">Parameters</span></span>

 <span data-ttu-id="f2cd7-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f2cd7-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f2cd7-108">[entrada] Una máscara de bits de indicadores que controla cómo se envía un mensaje.</span><span class="sxs-lookup"><span data-stu-id="f2cd7-108">[in] A bitmask of flags that controls how a message is submitted.</span></span> <span data-ttu-id="f2cd7-109">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="f2cd7-109">The following flag can be set:</span></span>
    
<span data-ttu-id="f2cd7-110">FORCE_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="f2cd7-110">FORCE_SUBMIT</span></span> 
  
> <span data-ttu-id="f2cd7-111">MAPI debe enviar el mensaje, incluso si es posible que no se enviarán inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="f2cd7-111">MAPI should submit the message even if it might not be sent immediately.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f2cd7-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2cd7-112">Return value</span></span>

<span data-ttu-id="f2cd7-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="f2cd7-113">S_OK</span></span> 
  
> <span data-ttu-id="f2cd7-114">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="f2cd7-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f2cd7-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f2cd7-115">Remarks</span></span>

<span data-ttu-id="f2cd7-116">Objetos de formulario llamar al método **IMAPIMessageSite::SubmitMessage** para solicitar que un mensaje se ponen en cola para la entrega.</span><span class="sxs-lookup"><span data-stu-id="f2cd7-116">Form objects call the **IMAPIMessageSite::SubmitMessage** method to request that a message be queued for delivery.</span></span> <span data-ttu-id="f2cd7-117">El sitio de mensaje debe llamar al método [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) antes de enviar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="f2cd7-117">The message site should call the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method before submitting the message.</span></span> <span data-ttu-id="f2cd7-118">El mensaje no es necesario que se han guardado anteriormente, debido a que **SubmitMessage** debe producir el mensaje que se guarde si se ha modificado el mensaje.</span><span class="sxs-lookup"><span data-stu-id="f2cd7-118">The message does not need to have been previously saved, because **SubmitMessage** should cause the message to be saved if the message has been modified.</span></span> <span data-ttu-id="f2cd7-119">Después de la devolución de **SubmitMessage**, el formulario debe comprobar si un mensaje actual y descartar propio si no existe ninguno.</span><span class="sxs-lookup"><span data-stu-id="f2cd7-119">After the return of **SubmitMessage**, the form must check for a current message and then dismiss itself if none exists.</span></span> 
  
<span data-ttu-id="f2cd7-120">Para obtener una lista de las interfaces relacionadas con los servidores de formulario, vea [Interfaces de formulario MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="f2cd7-120">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f2cd7-121">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f2cd7-121">MFCMAPI reference</span></span>

<span data-ttu-id="f2cd7-122">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="f2cd7-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f2cd7-123">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="f2cd7-123">**File**</span></span>|<span data-ttu-id="f2cd7-124">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="f2cd7-124">**Function**</span></span>|<span data-ttu-id="f2cd7-125">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="f2cd7-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f2cd7-126">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="f2cd7-126">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="f2cd7-127">CMyMAPIFormViewer::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="f2cd7-127">CMyMAPIFormViewer::SubmitMessage</span></span>  <br/> |<span data-ttu-id="f2cd7-128">MFCMAPI utiliza el método **IMAPIMessageSite::SubmitMessage** para guardar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="f2cd7-128">MFCMAPI uses the **IMAPIMessageSite::SubmitMessage** method to save the message.</span></span> <span data-ttu-id="f2cd7-129">En primer lugar, llama al método **IPersistMessage::HandsOffMessage** y, a continuación, se llama **SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="f2cd7-129">First, it calls the **IPersistMessage::HandsOffMessage** method, and then it calls **SubmitMessage**.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f2cd7-130">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="f2cd7-130">See also</span></span>



[<span data-ttu-id="f2cd7-131">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="f2cd7-131">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="f2cd7-132">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f2cd7-132">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="f2cd7-133">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="f2cd7-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="f2cd7-134">Interfaces de formulario de MAPI</span><span class="sxs-lookup"><span data-stu-id="f2cd7-134">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

