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
ms.openlocfilehash: 03eccfe27c6f93e42ee01a34fbf5df766c145cf1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357354"
---
# <a name="ixplogonendmessage"></a><span data-ttu-id="c5436-103">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="c5436-103">IXPLogon::EndMessage</span></span>

  
  
<span data-ttu-id="c5436-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5436-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5436-105">Informa al proveedor de transporte que la cola MAPI completó el procesamiento en un mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="c5436-105">Informs the transport provider that the MAPI spooler completed its processing on an outbound message.</span></span>
  
```cpp
HRESULT EndMessage(
  ULONG ulMsgRef,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c5436-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="c5436-106">Parameters</span></span>

 <span data-ttu-id="c5436-107">_ulMsgRef_</span><span class="sxs-lookup"><span data-stu-id="c5436-107">_ulMsgRef_</span></span>
  
> <span data-ttu-id="c5436-108">a Un valor de referencia específico del mensaje que se obtuvo en una llamada anterior al método [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="c5436-108">[in] A message-specific reference value that was obtained in an earlier call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method.</span></span> 
    
 <span data-ttu-id="c5436-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="c5436-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="c5436-110">contempla Máscara de máscara de marcadores que indica a la cola MAPI lo que debe hacer con el mensaje.</span><span class="sxs-lookup"><span data-stu-id="c5436-110">[out] A bitmask of flags that indicates to the MAPI spooler what it should do with the message.</span></span> <span data-ttu-id="c5436-111">Si no se establece ningún marcador, se ha enviado el mensaje.</span><span class="sxs-lookup"><span data-stu-id="c5436-111">If no flags are set, the message has been sent.</span></span> <span data-ttu-id="c5436-112">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="c5436-112">The following flags can be set:</span></span>
    
<span data-ttu-id="c5436-113">END_DONT_RESEND</span><span class="sxs-lookup"><span data-stu-id="c5436-113">END_DONT_RESEND</span></span> 
  
> <span data-ttu-id="c5436-114">El proveedor de transporte tiene toda la información que necesita sobre este mensaje en este momento.</span><span class="sxs-lookup"><span data-stu-id="c5436-114">The transport provider has all the information it needs about this message for now.</span></span> <span data-ttu-id="c5436-115">Cuando el proveedor de transporte requiere más información o cuando envía el mensaje, notifica a la cola MAPI llamando al método [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) con la marca NOTIFY_SENTDEFERRED y pasando el identificador de entrada del mensaje.</span><span class="sxs-lookup"><span data-stu-id="c5436-115">When the transport provider requires more information or when it has sent the message, it notifies the MAPI spooler by calling the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method with the NOTIFY_SENTDEFERRED flag and by passing the message's entry identifier.</span></span> 
    
<span data-ttu-id="c5436-116">END_RESEND_LATER</span><span class="sxs-lookup"><span data-stu-id="c5436-116">END_RESEND_LATER</span></span> 
  
> <span data-ttu-id="c5436-117">El proveedor de transporte no envía el mensaje en el momento actual por motivos que no son condiciones de error.</span><span class="sxs-lookup"><span data-stu-id="c5436-117">The transport provider is not sending the message at the current time for reasons that are not error conditions.</span></span> <span data-ttu-id="c5436-118">Se debe llamar al proveedor de transporte más adelante para enviar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="c5436-118">The transport provider should be called again later to send the message.</span></span>
    
<span data-ttu-id="c5436-119">END_RESEND_NOW</span><span class="sxs-lookup"><span data-stu-id="c5436-119">END_RESEND_NOW</span></span> 
  
> <span data-ttu-id="c5436-120">El proveedor de transporte debe reiniciar el mensaje que se le pasó en una llamada al método [IMessage:: SubmitMessage](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="c5436-120">The transport provider needs to restart the message passed to it in an [IMessage::SubmitMessage](imessage-submitmessage.md) method call.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c5436-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c5436-121">Return value</span></span>

<span data-ttu-id="c5436-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="c5436-122">S_OK</span></span> 
  
> <span data-ttu-id="c5436-123">La llamada se ha realizado correctamente y ha devuelto el valor o los valores esperados.</span><span class="sxs-lookup"><span data-stu-id="c5436-123">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c5436-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c5436-124">Remarks</span></span>

<span data-ttu-id="c5436-125">La cola MAPI llama al método **IXPLogon:: EndMessage** después de completar el procesamiento implicado en proporcionar la información de entrega ampliada o no entregada.</span><span class="sxs-lookup"><span data-stu-id="c5436-125">The MAPI spooler calls the **IXPLogon::EndMessage** method after it completes the processing involved in providing extended delivery or nondelivery information.</span></span> 
  
<span data-ttu-id="c5436-126">Una vez que se devuelve esta llamada, el valor del parámetro _ulMsgRef_ ya no es válido para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="c5436-126">Once this call returns, the value in the  _ulMsgRef_ parameter is no longer valid for this message.</span></span> <span data-ttu-id="c5436-127">El proveedor de transporte puede reutilizar el mismo valor en un mensaje futuro.</span><span class="sxs-lookup"><span data-stu-id="c5436-127">The transport provider can reuse the same value on a future message.</span></span> 
  
<span data-ttu-id="c5436-128">Todos los objetos que el proveedor de transporte abre durante la transferencia de un mensaje debe liberarse antes de que se devuelva la llamada a **EndMessage** , con la excepción del objeto Message que la cola MAPI pasa al proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="c5436-128">All objects that the transport provider opens during the transfer of a message should be released before the **EndMessage** call returns, with the exception of the message object that the MAPI spooler passes to the transport provider.</span></span> <span data-ttu-id="c5436-129">El objeto de mensaje que pasa la cola MAPI no es válido después de la llamada **EndMessage** .</span><span class="sxs-lookup"><span data-stu-id="c5436-129">The message object passed by the MAPI spooler is invalid after the **EndMessage** call.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c5436-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5436-130">See also</span></span>



[<span data-ttu-id="c5436-131">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="c5436-131">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="c5436-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="c5436-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="c5436-133">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="c5436-133">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
  
[<span data-ttu-id="c5436-134">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c5436-134">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

