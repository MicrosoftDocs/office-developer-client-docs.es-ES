---
title: IMAPISupportPrepareSubmit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.PrepareSubmit
api_type:
- COM
ms.assetid: 467242e3-96c9-4280-9cbc-9ecfe3f279cf
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 738eb346ec5388cbd94b32598236ef2ca05740f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425739"
---
# <a name="imapisupportpreparesubmit"></a><span data-ttu-id="aea38-103">IMAPISupport::PrepareSubmit</span><span class="sxs-lookup"><span data-stu-id="aea38-103">IMAPISupport::PrepareSubmit</span></span>

  
  
<span data-ttu-id="aea38-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aea38-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aea38-105">Prepara un mensaje para enviarlo a la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="aea38-105">Prepares a message for submission to the MAPI spooler.</span></span>
  
```cpp
HRESULT PrepareSubmit(
LPMESSAGE lpMessage,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="aea38-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="aea38-106">Parameters</span></span>

 <span data-ttu-id="aea38-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="aea38-107">_lpMessage_</span></span>
  
> <span data-ttu-id="aea38-108">a Un puntero al mensaje que se va a preparar.</span><span class="sxs-lookup"><span data-stu-id="aea38-108">[in] A pointer to the message to prepare.</span></span>
    
 <span data-ttu-id="aea38-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="aea38-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="aea38-110">[in, out] En la entrada, el parámetro _lpulFlags_ está reservado y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="aea38-110">[in, out] On input, the  _lpulFlags_ parameter is reserved and must be zero.</span></span> <span data-ttu-id="aea38-111">En la salida, _lpulFlags_ debe ser null.</span><span class="sxs-lookup"><span data-stu-id="aea38-111">On output,  _lpulFlags_ must be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="aea38-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aea38-112">Return value</span></span>

<span data-ttu-id="aea38-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="aea38-113">S_OK</span></span> 
  
> <span data-ttu-id="aea38-114">El mensaje se ha preparado correctamente.</span><span class="sxs-lookup"><span data-stu-id="aea38-114">The message was successfully prepared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="aea38-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aea38-115">Remarks</span></span>

<span data-ttu-id="aea38-116">El método **IMAPISupport::P reparesubmit** se implementa para los objetos de compatibilidad del proveedor de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="aea38-116">The **IMAPISupport::PrepareSubmit** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="aea38-117">Los proveedores de almacenamiento de mensajes llaman a **PrepareSubmit** en su implementación del método [IMessage:: SubmitMessage](imessage-submitmessage.md) para preparar un mensaje para su envío a la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="aea38-117">Message store providers call **PrepareSubmit** in their implementation of the [IMessage::SubmitMessage](imessage-submitmessage.md) method to prepare a message for submission to the MAPI spooler.</span></span> 
  
 <span data-ttu-id="aea38-118">**PrepareSubmit** se usa para controlar los mensajes que tienen la marca MSGFLAG_RESEND establecida en su propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="aea38-118">**PrepareSubmit** is used to handle messages that have the MSGFLAG_RESEND flag set in their **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="aea38-119">MSGFLAG_RESEND se establece para los mensajes que incluyen una solicitud que se va a reenviar cuando se produce un error en la transmisión inicial.</span><span class="sxs-lookup"><span data-stu-id="aea38-119">MSGFLAG_RESEND is set for messages that include a request to be resent when an initial transmission fails.</span></span> <span data-ttu-id="aea38-120">**PrepareSubmit** determina cuáles de los destinatarios de la lista de destinatarios recibieron correctamente el mensaje y cuáles no.</span><span class="sxs-lookup"><span data-stu-id="aea38-120">**PrepareSubmit** determines which of the recipients in the recipient list successfully received the message and which did not.</span></span> 
  
<span data-ttu-id="aea38-121">Para obtener acceso a la lista de destinatarios, **PrepareSubmit** llama al método [IMessage:: GetRecipientTable](imessage-getrecipienttable.md) del mensaje.</span><span class="sxs-lookup"><span data-stu-id="aea38-121">To access the recipient list, **PrepareSubmit** calls the message's [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method.</span></span> <span data-ttu-id="aea38-122">Para recuperar los datos del destinatario, **PrepareSubmit** llama al método [IMAPITable:: QueryRows](imapitable-queryrows.md) de la tabla del destinatario.</span><span class="sxs-lookup"><span data-stu-id="aea38-122">To retrieve the recipient data, **PrepareSubmit** calls the recipient table's [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> <span data-ttu-id="aea38-123">Para cada fila de la tabla, **PrepareSubmit** comprueba la propiedad **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) y realiza una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="aea38-123">For each row in the table, **PrepareSubmit** checks the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property and takes one of the following actions:</span></span>
  
- <span data-ttu-id="aea38-124">Si se establece la marca MAPI_SUBMITTED, **PrepareSubmit** borra la marca y establece la propiedad **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) en false.</span><span class="sxs-lookup"><span data-stu-id="aea38-124">If the MAPI_SUBMITTED flag is set, **PrepareSubmit** clears the flag and sets the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property to FALSE.</span></span>
    
- <span data-ttu-id="aea38-125">Si no se establece la marca MAPI_SUBMITTED, **PrepareSubmit** cambia **PR_RECIPIENT_TYPE** a MAPI_P1 y establece **PR_RESPONSIBILITY** en true.</span><span class="sxs-lookup"><span data-stu-id="aea38-125">If the MAPI_SUBMITTED flag is not set, **PrepareSubmit** changes **PR_RECIPIENT_TYPE** to MAPI_P1 and sets **PR_RESPONSIBILITY** to TRUE.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="aea38-126">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="aea38-126">Notes to callers</span></span>

<span data-ttu-id="aea38-127">Antes de llamar a **PrepareSubmit**, asegúrese de que ha llamado al método [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) y establezca la marca NOTIFY_READYTOSEND en el parámetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="aea38-127">Before you call **PrepareSubmit**, be sure you have called the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method and set the NOTIFY_READYTOSEND flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="aea38-128">La llamada a **SpoolerNotify** debe realizarse una vez por sesión antes de la llamada a **PrepareSubmit**.</span><span class="sxs-lookup"><span data-stu-id="aea38-128">The **SpoolerNotify** call must be made once per session before the call to **PrepareSubmit**.</span></span> <span data-ttu-id="aea38-129">**SpoolerNotify** sincroniza la cola MAPI y garantiza que todos los proveedores de transporte necesarios inicien sesión y que se registren sus tipos de direcciones.</span><span class="sxs-lookup"><span data-stu-id="aea38-129">**SpoolerNotify** synchronizes the MAPI spooler and ensures that all needed transport providers are logged on and their address types are registered.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="aea38-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="aea38-130">See also</span></span>



[<span data-ttu-id="aea38-131">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="aea38-131">IMAPIFolder::GetMessageStatus</span></span>](imapifolder-getmessagestatus.md)
  
[<span data-ttu-id="aea38-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="aea38-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="aea38-133">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="aea38-133">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

