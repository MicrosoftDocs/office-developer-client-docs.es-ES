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
ms.openlocfilehash: e785d42639d51dab154a0bde239f858a92ddd143
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588625"
---
# <a name="imapisupportreadreceipt"></a><span data-ttu-id="94db6-103">IMAPISupport::ReadReceipt</span><span class="sxs-lookup"><span data-stu-id="94db6-103">IMAPISupport::ReadReceipt</span></span>

  
  
<span data-ttu-id="94db6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94db6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94db6-105">Genera una lectura o del informe nonread para un mensaje.</span><span class="sxs-lookup"><span data-stu-id="94db6-105">Generates a read or nonread report for a message.</span></span>
  
```cpp
HRESULT ReadReceipt(
ULONG ulFlags,
LPMESSAGE lpReadMessage,
LPMESSAGE FAR * lppEmptyMessage
);
```

## <a name="parameters"></a><span data-ttu-id="94db6-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="94db6-106">Parameters</span></span>

 <span data-ttu-id="94db6-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="94db6-107">_ulFlags_</span></span>
  
> <span data-ttu-id="94db6-108">[entrada] Una máscara de bits de indicadores que controla cómo se genera la lectura o el informe nonread.</span><span class="sxs-lookup"><span data-stu-id="94db6-108">[in] A bitmask of flags that controls how the read or nonread report is generated.</span></span> <span data-ttu-id="94db6-109">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="94db6-109">The following flag can be set:</span></span>
    
<span data-ttu-id="94db6-110">MAPI_NON_READ</span><span class="sxs-lookup"><span data-stu-id="94db6-110">MAPI_NON_READ</span></span> 
  
> <span data-ttu-id="94db6-111">Se genera un informe nonread.</span><span class="sxs-lookup"><span data-stu-id="94db6-111">A nonread report is generated.</span></span> <span data-ttu-id="94db6-112">Si no se establece MAPI_NON_READ, se genera un informe de lectura.</span><span class="sxs-lookup"><span data-stu-id="94db6-112">If MAPI_NON_READ is not set, a read report is generated.</span></span>
    
 <span data-ttu-id="94db6-113">_lpReadMessage_</span><span class="sxs-lookup"><span data-stu-id="94db6-113">_lpReadMessage_</span></span>
  
> <span data-ttu-id="94db6-114">[entrada] Un puntero al mensaje sobre qué se debe generar el informe.</span><span class="sxs-lookup"><span data-stu-id="94db6-114">[in] A pointer to the message about which the report should be generated.</span></span>
    
 <span data-ttu-id="94db6-115">_lppEmptyMessage_</span><span class="sxs-lookup"><span data-stu-id="94db6-115">_lppEmptyMessage_</span></span>
  
> <span data-ttu-id="94db6-116">[entrada, salida] En la entrada, _lppEmptyMessage_ apunta a un puntero a un mensaje vacío.</span><span class="sxs-lookup"><span data-stu-id="94db6-116">[in, out] On input,  _lppEmptyMessage_ points to a pointer to an empty message.</span></span> <span data-ttu-id="94db6-117">En la salida, _lppEmptyMessage_ apunta a un puntero al mensaje de informe.</span><span class="sxs-lookup"><span data-stu-id="94db6-117">On output,  _lppEmptyMessage_ points to a pointer to the report message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="94db6-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94db6-118">Return value</span></span>

<span data-ttu-id="94db6-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="94db6-119">S_OK</span></span> 
  
> <span data-ttu-id="94db6-120">El informe se ha generado correctamente.</span><span class="sxs-lookup"><span data-stu-id="94db6-120">The report was successfully generated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="94db6-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="94db6-121">Remarks</span></span>

<span data-ttu-id="94db6-122">El método **IMAPISupport::ReadReceipt** sólo se implementa para objetos de soporte técnico de proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="94db6-122">The **IMAPISupport::ReadReceipt** method is implemented only for message store provider support objects.</span></span> <span data-ttu-id="94db6-123">Los proveedores de almacén de mensajes llamada **ReadReceipt** para indicar a MAPI para generar una lectura o del informe nonread para el mensaje que apunta el parámetro _lpReadMessage_ .</span><span class="sxs-lookup"><span data-stu-id="94db6-123">Message store providers call **ReadReceipt** to instruct MAPI to generate a read or nonread report for the message pointed to by the  _lpReadMessage_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="94db6-124">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="94db6-124">Notes to callers</span></span>

<span data-ttu-id="94db6-125">Llamar a **ReadReceipt** cuando se establece la propiedad **PR_READ_RECEIPT_REQUESTED de MAPI** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) y una de las siguientes condiciones es verdadera:</span><span class="sxs-lookup"><span data-stu-id="94db6-125">Call **ReadReceipt** when the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set and one of the following conditions is true:</span></span>
  
- <span data-ttu-id="94db6-126">Lo ha leído el mensaje.</span><span class="sxs-lookup"><span data-stu-id="94db6-126">The message has been read.</span></span>
    
- <span data-ttu-id="94db6-127">El mensaje se ha movido.</span><span class="sxs-lookup"><span data-stu-id="94db6-127">The message has been moved.</span></span>
    
- <span data-ttu-id="94db6-128">El mensaje se ha copiado.</span><span class="sxs-lookup"><span data-stu-id="94db6-128">The message has been copied.</span></span>
    
- <span data-ttu-id="94db6-129">Se ha llamado al método [IMessage::SetReadFlag](imessage-setreadflag.md) del mensaje.</span><span class="sxs-lookup"><span data-stu-id="94db6-129">The message's [IMessage::SetReadFlag](imessage-setreadflag.md) method has been called.</span></span> 
    
<span data-ttu-id="94db6-130">No llame a **ReadReceipt** cuando se elimina un mensaje.</span><span class="sxs-lookup"><span data-stu-id="94db6-130">Do not call **ReadReceipt** when a message is deleted.</span></span> 
  
<span data-ttu-id="94db6-131">Una lectura informe nonread se debe enviar o sólo una vez para un mensaje.</span><span class="sxs-lookup"><span data-stu-id="94db6-131">A read or nonread report should be sent only once for a message.</span></span> <span data-ttu-id="94db6-132">Realizar un seguimiento de estado de lectura de un mensaje y no enviar varios informes para un solo mensaje.</span><span class="sxs-lookup"><span data-stu-id="94db6-132">Keep track of a message's read status and do not send multiple reports for a single message.</span></span>
  
<span data-ttu-id="94db6-133">Si el parámetro _lppEmptyMessage_ apunta a un mensaje de informe válido cuando devuelve MAPI desde **ReadReceipt**, llame al método [IMessage::SubmitMessage](imessage-submitmessage.md) para enviar el mensaje y, a continuación, liberar el puntero llamando a su **IUnknown:s:Release **(método).</span><span class="sxs-lookup"><span data-stu-id="94db6-133">If the  _lppEmptyMessage_ parameter points to a valid report message when MAPI returns from **ReadReceipt**, call the [IMessage::SubmitMessage](imessage-submitmessage.md) method to send the message and then release the pointer by calling its **IUnknown:s:Release** method.</span></span> 
  
<span data-ttu-id="94db6-134">Si se produce un error en **ReadReceipt** , se debe liberar el mensaje sin que se envía.</span><span class="sxs-lookup"><span data-stu-id="94db6-134">If **ReadReceipt** fails, the message should be released without being submitted.</span></span> <span data-ttu-id="94db6-135">Si almacena el estado de lectura del mensaje, puede intentar generar la lectura o el informe nonread en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="94db6-135">If you store the message's read status, you can attempt to generate the read or nonread report at a later time.</span></span> 
  
<span data-ttu-id="94db6-136">Puede ocultar o mostrar informes de lectura y nonread generados por almacenes en las carpetas.</span><span class="sxs-lookup"><span data-stu-id="94db6-136">You can either hide or display read and nonread reports generated by stores in your folders.</span></span> <span data-ttu-id="94db6-137">Almacenamiento de informes de lectura y nonread en las carpetas ocultas le permite implementar una mayor seguridad.</span><span class="sxs-lookup"><span data-stu-id="94db6-137">Storing read and nonread reports in hidden folders enables you to implement tighter security.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="94db6-138">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="94db6-138">See also</span></span>



[<span data-ttu-id="94db6-139">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="94db6-139">IMAPIFolder::DeleteMessages</span></span>](imapifolder-deletemessages.md)
  
[<span data-ttu-id="94db6-140">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="94db6-140">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="94db6-141">Propiedad canónica PidTagReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="94db6-141">PidTagReadReceiptRequested Canonical Property</span></span>](pidtagreadreceiptrequested-canonical-property.md)
  
[<span data-ttu-id="94db6-142">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="94db6-142">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

