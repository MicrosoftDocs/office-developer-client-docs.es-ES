---
title: IMAPISupportReadReceipt
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ReadReceipt
api_type:
- COM
ms.assetid: ef31b61a-93b6-4ae8-bc71-f5ef5caf43f4
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 1915004847fdfd27c97656223866aaab9d3e59c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425326"
---
# <a name="imapisupportreadreceipt"></a><span data-ttu-id="dee94-103">IMAPISupport::ReadReceipt</span><span class="sxs-lookup"><span data-stu-id="dee94-103">IMAPISupport::ReadReceipt</span></span>

  
  
<span data-ttu-id="dee94-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dee94-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dee94-105">Genera un informe de lectura o no leído para un mensaje.</span><span class="sxs-lookup"><span data-stu-id="dee94-105">Generates a read or nonread report for a message.</span></span>
  
```cpp
HRESULT ReadReceipt(
ULONG ulFlags,
LPMESSAGE lpReadMessage,
LPMESSAGE FAR * lppEmptyMessage
);
```

## <a name="parameters"></a><span data-ttu-id="dee94-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="dee94-106">Parameters</span></span>

 <span data-ttu-id="dee94-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dee94-107">_ulFlags_</span></span>
  
> <span data-ttu-id="dee94-108">a Máscara de máscara de marcadores que controla cómo se genera el informe de lectura o no lectura.</span><span class="sxs-lookup"><span data-stu-id="dee94-108">[in] A bitmask of flags that controls how the read or nonread report is generated.</span></span> <span data-ttu-id="dee94-109">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="dee94-109">The following flag can be set:</span></span>
    
<span data-ttu-id="dee94-110">MAPI_NON_READ</span><span class="sxs-lookup"><span data-stu-id="dee94-110">MAPI_NON_READ</span></span> 
  
> <span data-ttu-id="dee94-111">Se genera un informe no leído.</span><span class="sxs-lookup"><span data-stu-id="dee94-111">A nonread report is generated.</span></span> <span data-ttu-id="dee94-112">Si no se establece MAPI_NON_READ, se genera un informe de lectura.</span><span class="sxs-lookup"><span data-stu-id="dee94-112">If MAPI_NON_READ is not set, a read report is generated.</span></span>
    
 <span data-ttu-id="dee94-113">_lpReadMessage_</span><span class="sxs-lookup"><span data-stu-id="dee94-113">_lpReadMessage_</span></span>
  
> <span data-ttu-id="dee94-114">a Un puntero al mensaje sobre el que se debe generar el informe.</span><span class="sxs-lookup"><span data-stu-id="dee94-114">[in] A pointer to the message about which the report should be generated.</span></span>
    
 <span data-ttu-id="dee94-115">_lppEmptyMessage_</span><span class="sxs-lookup"><span data-stu-id="dee94-115">_lppEmptyMessage_</span></span>
  
> <span data-ttu-id="dee94-116">[in, out] En la entrada, _lppEmptyMessage_ apunta a un puntero a un mensaje vacío.</span><span class="sxs-lookup"><span data-stu-id="dee94-116">[in, out] On input,  _lppEmptyMessage_ points to a pointer to an empty message.</span></span> <span data-ttu-id="dee94-117">En la salida, _lppEmptyMessage_ apunta a un puntero al mensaje del informe.</span><span class="sxs-lookup"><span data-stu-id="dee94-117">On output,  _lppEmptyMessage_ points to a pointer to the report message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dee94-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dee94-118">Return value</span></span>

<span data-ttu-id="dee94-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="dee94-119">S_OK</span></span> 
  
> <span data-ttu-id="dee94-120">El informe se generó correctamente.</span><span class="sxs-lookup"><span data-stu-id="dee94-120">The report was successfully generated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dee94-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dee94-121">Remarks</span></span>

<span data-ttu-id="dee94-122">El método **IMAPISupport:: ReadReceipt** solo se implementa para objetos de compatibilidad del proveedor de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="dee94-122">The **IMAPISupport::ReadReceipt** method is implemented only for message store provider support objects.</span></span> <span data-ttu-id="dee94-123">Los proveedores de almacenamiento de mensajes llaman a **ReadReceipt** para indicar a MAPI que genere un informe de lectura o no lectura para el mensaje al que señala el parámetro _lpReadMessage_ .</span><span class="sxs-lookup"><span data-stu-id="dee94-123">Message store providers call **ReadReceipt** to instruct MAPI to generate a read or nonread report for the message pointed to by the  _lpReadMessage_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="dee94-124">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="dee94-124">Notes to callers</span></span>

<span data-ttu-id="dee94-125">Llamar a **ReadReceipt** cuando se establece la propiedad **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) y se cumple una de las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="dee94-125">Call **ReadReceipt** when the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set and one of the following conditions is true:</span></span>
  
- <span data-ttu-id="dee94-126">Se ha leído el mensaje.</span><span class="sxs-lookup"><span data-stu-id="dee94-126">The message has been read.</span></span>
    
- <span data-ttu-id="dee94-127">El mensaje se ha movido.</span><span class="sxs-lookup"><span data-stu-id="dee94-127">The message has been moved.</span></span>
    
- <span data-ttu-id="dee94-128">El mensaje se ha copiado.</span><span class="sxs-lookup"><span data-stu-id="dee94-128">The message has been copied.</span></span>
    
- <span data-ttu-id="dee94-129">Se ha llamado al método [IMessage:: SetReadFlag](imessage-setreadflag.md) del mensaje.</span><span class="sxs-lookup"><span data-stu-id="dee94-129">The message's [IMessage::SetReadFlag](imessage-setreadflag.md) method has been called.</span></span> 
    
<span data-ttu-id="dee94-130">No llame a **ReadReceipt** cuando se elimine un mensaje.</span><span class="sxs-lookup"><span data-stu-id="dee94-130">Do not call **ReadReceipt** when a message is deleted.</span></span> 
  
<span data-ttu-id="dee94-131">Un informe de lectura o no lectura solo debe enviarse una vez para un mensaje.</span><span class="sxs-lookup"><span data-stu-id="dee94-131">A read or nonread report should be sent only once for a message.</span></span> <span data-ttu-id="dee94-132">Realizar un seguimiento del estado de lectura de un mensaje y no enviar varios informes para un solo mensaje.</span><span class="sxs-lookup"><span data-stu-id="dee94-132">Keep track of a message's read status and do not send multiple reports for a single message.</span></span>
  
<span data-ttu-id="dee94-133">Si el parámetro _lppEmptyMessage_ apunta a un mensaje de informe válido cuando MAPI devuelve de **ReadReceipt**, llame al método [IMessage:: SubmitMessage](imessage-submitmessage.md) para enviar el mensaje y, a continuación, libere el puntero llamando a su \*\*IUnknown: Release: Release \*\*método.</span><span class="sxs-lookup"><span data-stu-id="dee94-133">If the  _lppEmptyMessage_ parameter points to a valid report message when MAPI returns from **ReadReceipt**, call the [IMessage::SubmitMessage](imessage-submitmessage.md) method to send the message and then release the pointer by calling its **IUnknown:s:Release** method.</span></span> 
  
<span data-ttu-id="dee94-134">Si **ReadReceipt** produce un error, el mensaje debe liberarse sin enviarse.</span><span class="sxs-lookup"><span data-stu-id="dee94-134">If **ReadReceipt** fails, the message should be released without being submitted.</span></span> <span data-ttu-id="dee94-135">Si almacena el estado de lectura del mensaje, puede intentar generar el informe de lectura o no lectura en otro momento.</span><span class="sxs-lookup"><span data-stu-id="dee94-135">If you store the message's read status, you can attempt to generate the read or nonread report at a later time.</span></span> 
  
<span data-ttu-id="dee94-136">Puede ocultar o mostrar los informes leídos y no leídos generados por los almacenes de las carpetas.</span><span class="sxs-lookup"><span data-stu-id="dee94-136">You can either hide or display read and nonread reports generated by stores in your folders.</span></span> <span data-ttu-id="dee94-137">El almacenamiento de informes leídos y no leídos en carpetas ocultas permite implementar una seguridad más estricta.</span><span class="sxs-lookup"><span data-stu-id="dee94-137">Storing read and nonread reports in hidden folders enables you to implement tighter security.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dee94-138">Ver también</span><span class="sxs-lookup"><span data-stu-id="dee94-138">See also</span></span>



[<span data-ttu-id="dee94-139">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="dee94-139">IMAPIFolder::DeleteMessages</span></span>](imapifolder-deletemessages.md)
  
[<span data-ttu-id="dee94-140">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="dee94-140">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="dee94-141">Propiedad canónica PidTagReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="dee94-141">PidTagReadReceiptRequested Canonical Property</span></span>](pidtagreadreceiptrequested-canonical-property.md)
  
[<span data-ttu-id="dee94-142">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="dee94-142">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

