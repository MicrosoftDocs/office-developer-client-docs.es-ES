---
title: IXPLogonEndMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.EndMessage
api_type:
- COM
ms.assetid: bb29e6a0-7a92-46eb-bbeb-6f2df6ac6d21
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f727d68e0e193e8f2e148d881968993f836f8ab0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582472"
---
# <a name="ixplogonendmessage"></a><span data-ttu-id="fa5e0-103">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="fa5e0-103">IXPLogon::EndMessage</span></span>

  
  
<span data-ttu-id="fa5e0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa5e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa5e0-105">Informa al proveedor de transporte que la cola MAPI completó su procesamiento en un mensaje de salida.</span><span class="sxs-lookup"><span data-stu-id="fa5e0-105">Informs the transport provider that the MAPI spooler completed its processing on an outbound message.</span></span>
  
```cpp
HRESULT EndMessage(
  ULONG ulMsgRef,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="fa5e0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fa5e0-106">Parameters</span></span>

 <span data-ttu-id="fa5e0-107">_ulMsgRef_</span><span class="sxs-lookup"><span data-stu-id="fa5e0-107">_ulMsgRef_</span></span>
  
> <span data-ttu-id="fa5e0-108">[entrada] Un valor de referencia específicas de mensaje que se ha obtenido en una llamada anterior al método [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="fa5e0-108">[in] A message-specific reference value that was obtained in an earlier call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method.</span></span> 
    
 <span data-ttu-id="fa5e0-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="fa5e0-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="fa5e0-110">[out] Una máscara de bits de marcadores que indica a la cola MAPI, lo que debe hacer con el mensaje.</span><span class="sxs-lookup"><span data-stu-id="fa5e0-110">[out] A bitmask of flags that indicates to the MAPI spooler what it should do with the message.</span></span> <span data-ttu-id="fa5e0-111">Si no se establecen indicadores, el mensaje se ha enviado.</span><span class="sxs-lookup"><span data-stu-id="fa5e0-111">If no flags are set, the message has been sent.</span></span> <span data-ttu-id="fa5e0-112">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="fa5e0-112">The following flags can be set:</span></span>
    
<span data-ttu-id="fa5e0-113">END_DONT_RESEND</span><span class="sxs-lookup"><span data-stu-id="fa5e0-113">END_DONT_RESEND</span></span> 
  
> <span data-ttu-id="fa5e0-114">El proveedor de transporte tiene toda la información que necesita acerca de este mensaje por ahora.</span><span class="sxs-lookup"><span data-stu-id="fa5e0-114">The transport provider has all the information it needs about this message for now.</span></span> <span data-ttu-id="fa5e0-115">Cuando el proveedor de transporte requiere más información o cuando ha enviado el mensaje, se lo comunica a la cola MAPI llamando al método [SpoolerNotify](imapisupport-spoolernotify.md) con el indicador NOTIFY_SENTDEFERRED y pasando el identificador de entrada del mensaje.</span><span class="sxs-lookup"><span data-stu-id="fa5e0-115">When the transport provider requires more information or when it has sent the message, it notifies the MAPI spooler by calling the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method with the NOTIFY_SENTDEFERRED flag and by passing the message's entry identifier.</span></span> 
    
<span data-ttu-id="fa5e0-116">END_RESEND_LATER</span><span class="sxs-lookup"><span data-stu-id="fa5e0-116">END_RESEND_LATER</span></span> 
  
> <span data-ttu-id="fa5e0-117">El proveedor de transporte no está enviando el mensaje en el tiempo actual por motivos que no sean las condiciones de error.</span><span class="sxs-lookup"><span data-stu-id="fa5e0-117">The transport provider is not sending the message at the current time for reasons that are not error conditions.</span></span> <span data-ttu-id="fa5e0-118">El proveedor de transporte debe se vuelva a llamar más tarde para enviar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="fa5e0-118">The transport provider should be called again later to send the message.</span></span>
    
<span data-ttu-id="fa5e0-119">END_RESEND_NOW</span><span class="sxs-lookup"><span data-stu-id="fa5e0-119">END_RESEND_NOW</span></span> 
  
> <span data-ttu-id="fa5e0-120">El proveedor de transporte es necesario reiniciar el mensaje que se pasa a ella en una llamada al método [IMessage::SubmitMessage](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="fa5e0-120">The transport provider needs to restart the message passed to it in an [IMessage::SubmitMessage](imessage-submitmessage.md) method call.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fa5e0-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fa5e0-121">Return value</span></span>

<span data-ttu-id="fa5e0-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="fa5e0-122">S_OK</span></span> 
  
> <span data-ttu-id="fa5e0-123">La llamada se ha realizado correctamente y devuelve el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="fa5e0-123">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fa5e0-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fa5e0-124">Remarks</span></span>

<span data-ttu-id="fa5e0-125">La cola MAPI llama al método de **IXPLogon::EndMessage** después de que finalice el procesamiento necesarios para proporcionar información de no entrega o entrega extendida.</span><span class="sxs-lookup"><span data-stu-id="fa5e0-125">The MAPI spooler calls the **IXPLogon::EndMessage** method after it completes the processing involved in providing extended delivery or nondelivery information.</span></span> 
  
<span data-ttu-id="fa5e0-126">Una vez que devuelve esta llamada, el valor en el parámetro _ulMsgRef_ ya no es válido para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="fa5e0-126">Once this call returns, the value in the  _ulMsgRef_ parameter is no longer valid for this message.</span></span> <span data-ttu-id="fa5e0-127">El proveedor de transporte puede volver a usar el mismo valor en un mensaje futuro.</span><span class="sxs-lookup"><span data-stu-id="fa5e0-127">The transport provider can reuse the same value on a future message.</span></span> 
  
<span data-ttu-id="fa5e0-128">Todos los objetos que se abre el proveedor de transporte durante la transferencia de un mensaje deben liberarse antes de la devolución de llamada **EndMessage** , excepto el objeto de mensaje que la cola MAPI se pasa al proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="fa5e0-128">All objects that the transport provider opens during the transfer of a message should be released before the **EndMessage** call returns, with the exception of the message object that the MAPI spooler passes to the transport provider.</span></span> <span data-ttu-id="fa5e0-129">El objeto de mensaje pasado por la cola MAPI no es válido después de la llamada **EndMessage** .</span><span class="sxs-lookup"><span data-stu-id="fa5e0-129">The message object passed by the MAPI spooler is invalid after the **EndMessage** call.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fa5e0-130">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="fa5e0-130">See also</span></span>



[<span data-ttu-id="fa5e0-131">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="fa5e0-131">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="fa5e0-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="fa5e0-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="fa5e0-133">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="fa5e0-133">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
  
[<span data-ttu-id="fa5e0-134">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fa5e0-134">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

