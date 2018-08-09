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
ms.openlocfilehash: 7f81a0c3c9a9ad0a9bcef5c5685aa5b343237f19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817999"
---
# <a name="ixplogonendmessage"></a><span data-ttu-id="480d9-103">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="480d9-103">IXPLogon::EndMessage</span></span>

  
  
<span data-ttu-id="480d9-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="480d9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="480d9-105">Informa al proveedor de transporte que la cola MAPI completó su procesamiento en un mensaje de salida.</span><span class="sxs-lookup"><span data-stu-id="480d9-105">Informs the transport provider that the MAPI spooler completed its processing on an outbound message.</span></span>
  
```cpp
HRESULT EndMessage(
  ULONG ulMsgRef,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="480d9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="480d9-106">Parameters</span></span>

 <span data-ttu-id="480d9-107">_ulMsgRef_</span><span class="sxs-lookup"><span data-stu-id="480d9-107">_ulMsgRef_</span></span>
  
> <span data-ttu-id="480d9-108">[entrada] Un valor de referencia específicas de mensaje que se ha obtenido en una llamada anterior al método [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="480d9-108">[in] A message-specific reference value that was obtained in an earlier call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method.</span></span> 
    
 <span data-ttu-id="480d9-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="480d9-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="480d9-110">[out] Una máscara de bits de marcadores que indica a la cola MAPI, lo que debe hacer con el mensaje.</span><span class="sxs-lookup"><span data-stu-id="480d9-110">[out] A bitmask of flags that indicates to the MAPI spooler what it should do with the message.</span></span> <span data-ttu-id="480d9-111">Si no se establecen indicadores, el mensaje se ha enviado.</span><span class="sxs-lookup"><span data-stu-id="480d9-111">If no flags are set, the message has been sent.</span></span> <span data-ttu-id="480d9-112">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="480d9-112">The following flags can be set:</span></span>
    
<span data-ttu-id="480d9-113">END_DONT_RESEND</span><span class="sxs-lookup"><span data-stu-id="480d9-113">END_DONT_RESEND</span></span> 
  
> <span data-ttu-id="480d9-114">El proveedor de transporte tiene toda la información que necesita acerca de este mensaje por ahora.</span><span class="sxs-lookup"><span data-stu-id="480d9-114">The transport provider has all the information it needs about this message for now.</span></span> <span data-ttu-id="480d9-115">Cuando el proveedor de transporte requiere más información o cuando ha enviado el mensaje, se lo comunica a la cola MAPI llamando al método [SpoolerNotify](imapisupport-spoolernotify.md) con el indicador NOTIFY_SENTDEFERRED y pasando el identificador de entrada del mensaje.</span><span class="sxs-lookup"><span data-stu-id="480d9-115">When the transport provider requires more information or when it has sent the message, it notifies the MAPI spooler by calling the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method with the NOTIFY_SENTDEFERRED flag and by passing the message's entry identifier.</span></span> 
    
<span data-ttu-id="480d9-116">END_RESEND_LATER</span><span class="sxs-lookup"><span data-stu-id="480d9-116">END_RESEND_LATER</span></span> 
  
> <span data-ttu-id="480d9-117">El proveedor de transporte no está enviando el mensaje en el tiempo actual por motivos que no sean las condiciones de error.</span><span class="sxs-lookup"><span data-stu-id="480d9-117">The transport provider is not sending the message at the current time for reasons that are not error conditions.</span></span> <span data-ttu-id="480d9-118">El proveedor de transporte debe se vuelva a llamar más tarde para enviar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="480d9-118">The transport provider should be called again later to send the message.</span></span>
    
<span data-ttu-id="480d9-119">END_RESEND_NOW</span><span class="sxs-lookup"><span data-stu-id="480d9-119">END_RESEND_NOW</span></span> 
  
> <span data-ttu-id="480d9-120">El proveedor de transporte es necesario reiniciar el mensaje que se pasa a ella en una llamada al método [IMessage::SubmitMessage](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="480d9-120">The transport provider needs to restart the message passed to it in an [IMessage::SubmitMessage](imessage-submitmessage.md) method call.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="480d9-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="480d9-121">Return value</span></span>

<span data-ttu-id="480d9-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="480d9-122">S_OK</span></span> 
  
> <span data-ttu-id="480d9-123">La llamada se ha realizado correctamente y devuelve el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="480d9-123">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="480d9-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="480d9-124">Remarks</span></span>

<span data-ttu-id="480d9-125">La cola MAPI llama al método de **IXPLogon::EndMessage** después de que finalice el procesamiento necesarios para proporcionar información de no entrega o entrega extendida.</span><span class="sxs-lookup"><span data-stu-id="480d9-125">The MAPI spooler calls the **IXPLogon::EndMessage** method after it completes the processing involved in providing extended delivery or nondelivery information.</span></span> 
  
<span data-ttu-id="480d9-126">Una vez que devuelve esta llamada, el valor en el parámetro _ulMsgRef_ ya no es válido para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="480d9-126">Once this call returns, the value in the  _ulMsgRef_ parameter is no longer valid for this message.</span></span> <span data-ttu-id="480d9-127">El proveedor de transporte puede volver a usar el mismo valor en un mensaje futuro.</span><span class="sxs-lookup"><span data-stu-id="480d9-127">The transport provider can reuse the same value on a future message.</span></span> 
  
<span data-ttu-id="480d9-128">Todos los objetos que se abre el proveedor de transporte durante la transferencia de un mensaje deben liberarse antes de la devolución de llamada **EndMessage** , excepto el objeto de mensaje que la cola MAPI se pasa al proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="480d9-128">All objects that the transport provider opens during the transfer of a message should be released before the **EndMessage** call returns, with the exception of the message object that the MAPI spooler passes to the transport provider.</span></span> <span data-ttu-id="480d9-129">El objeto de mensaje pasado por la cola MAPI no es válido después de la llamada **EndMessage** .</span><span class="sxs-lookup"><span data-stu-id="480d9-129">The message object passed by the MAPI spooler is invalid after the **EndMessage** call.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="480d9-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="480d9-130">See also</span></span>



[<span data-ttu-id="480d9-131">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="480d9-131">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="480d9-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="480d9-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="480d9-133">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="480d9-133">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
  
[<span data-ttu-id="480d9-134">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="480d9-134">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

