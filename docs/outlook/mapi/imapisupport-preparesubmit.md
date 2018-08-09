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
ms.openlocfilehash: f6902b45cde3e5349d69b6f35c3f8980deb031b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817555"
---
# <a name="imapisupportpreparesubmit"></a><span data-ttu-id="92b5b-103">IMAPISupport::PrepareSubmit</span><span class="sxs-lookup"><span data-stu-id="92b5b-103">IMAPISupport::PrepareSubmit</span></span>

  
  
<span data-ttu-id="92b5b-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="92b5b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="92b5b-105">Prepara un mensaje para el envío a la cola de MAPI.</span><span class="sxs-lookup"><span data-stu-id="92b5b-105">Prepares a message for submission to the MAPI spooler.</span></span>
  
```cpp
HRESULT PrepareSubmit(
LPMESSAGE lpMessage,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="92b5b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="92b5b-106">Parameters</span></span>

 <span data-ttu-id="92b5b-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="92b5b-107">_lpMessage_</span></span>
  
> <span data-ttu-id="92b5b-108">[entrada] Un puntero al mensaje para preparar.</span><span class="sxs-lookup"><span data-stu-id="92b5b-108">[in] A pointer to the message to prepare.</span></span>
    
 <span data-ttu-id="92b5b-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="92b5b-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="92b5b-110">[entrada, salida] En la entrada, el parámetro _lpulFlags_ está reservado y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="92b5b-110">[in, out] On input, the  _lpulFlags_ parameter is reserved and must be zero.</span></span> <span data-ttu-id="92b5b-111">En la salida, _lpulFlags_ debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="92b5b-111">On output,  _lpulFlags_ must be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="92b5b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="92b5b-112">Return value</span></span>

<span data-ttu-id="92b5b-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="92b5b-113">S_OK</span></span> 
  
> <span data-ttu-id="92b5b-114">El mensaje se ha preparado correctamente.</span><span class="sxs-lookup"><span data-stu-id="92b5b-114">The message was successfully prepared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="92b5b-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="92b5b-115">Remarks</span></span>

<span data-ttu-id="92b5b-116">El método **IMAPISupport::PrepareSubmit** se implementa para objetos de soporte técnico de proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="92b5b-116">The **IMAPISupport::PrepareSubmit** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="92b5b-117">Los proveedores de almacén de mensajes llamada **PrepareSubmit** en su implementación del método [IMessage::SubmitMessage](imessage-submitmessage.md) para preparar un mensaje para el envío a la cola de MAPI.</span><span class="sxs-lookup"><span data-stu-id="92b5b-117">Message store providers call **PrepareSubmit** in their implementation of the [IMessage::SubmitMessage](imessage-submitmessage.md) method to prepare a message for submission to the MAPI spooler.</span></span> 
  
 <span data-ttu-id="92b5b-118">**PrepareSubmit** se usa para administrar los mensajes que tienen la marca MSGFLAG_RESEND establecida en su propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="92b5b-118">**PrepareSubmit** is used to handle messages that have the MSGFLAG_RESEND flag set in their **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="92b5b-119">MSGFLAG_RESEND se establece para los mensajes que incluyen una solicitud para ser reenviados cuando se produce un error en una transmisión inicial.</span><span class="sxs-lookup"><span data-stu-id="92b5b-119">MSGFLAG_RESEND is set for messages that include a request to be resent when an initial transmission fails.</span></span> <span data-ttu-id="92b5b-120">**PrepareSubmit** determina cuál de los destinatarios en la lista de destinatarios recibió correctamente el mensaje y que no lo ha hecho.</span><span class="sxs-lookup"><span data-stu-id="92b5b-120">**PrepareSubmit** determines which of the recipients in the recipient list successfully received the message and which did not.</span></span> 
  
<span data-ttu-id="92b5b-121">Para obtener acceso a la lista de destinatarios, **PrepareSubmit** llama (método [IMessage::GetRecipientTable](imessage-getrecipienttable.md) ) del mensaje.</span><span class="sxs-lookup"><span data-stu-id="92b5b-121">To access the recipient list, **PrepareSubmit** calls the message's [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method.</span></span> <span data-ttu-id="92b5b-122">Para recuperar los datos de destinatario, **PrepareSubmit** llama a método [IMAPITable:: QueryRows](imapitable-queryrows.md) de destinatario de la tabla.</span><span class="sxs-lookup"><span data-stu-id="92b5b-122">To retrieve the recipient data, **PrepareSubmit** calls the recipient table's [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> <span data-ttu-id="92b5b-123">Para cada fila de la tabla, **PrepareSubmit** comprueba la propiedad **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) y toma una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="92b5b-123">For each row in the table, **PrepareSubmit** checks the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property and takes one of the following actions:</span></span>
  
- <span data-ttu-id="92b5b-124">Si se establece la marca MAPI_SUBMITTED, **PrepareSubmit** borra la marca y la propiedad **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) se establece en FALSE.</span><span class="sxs-lookup"><span data-stu-id="92b5b-124">If the MAPI_SUBMITTED flag is set, **PrepareSubmit** clears the flag and sets the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property to FALSE.</span></span>
    
- <span data-ttu-id="92b5b-125">Si no está establecido el indicador MAPI_SUBMITTED, **PrepareSubmit** cambia de **PR_RECIPIENT_TYPE** a MAPI_P1 y establece **PR_RESPONSIBILITY** en TRUE.</span><span class="sxs-lookup"><span data-stu-id="92b5b-125">If the MAPI_SUBMITTED flag is not set, **PrepareSubmit** changes **PR_RECIPIENT_TYPE** to MAPI_P1 and sets **PR_RESPONSIBILITY** to TRUE.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="92b5b-126">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="92b5b-126">Notes to callers</span></span>

<span data-ttu-id="92b5b-127">Antes de llamar a **PrepareSubmit**, asegúrese de que se ha llamado al método [SpoolerNotify](imapisupport-spoolernotify.md) y establece el indicador NOTIFY_READYTOSEND en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="92b5b-127">Before you call **PrepareSubmit**, be sure you have called the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method and set the NOTIFY_READYTOSEND flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="92b5b-128">La llamada **SpoolerNotify** debe realizarse una vez por sesión antes de la llamada a **PrepareSubmit**.</span><span class="sxs-lookup"><span data-stu-id="92b5b-128">The **SpoolerNotify** call must be made once per session before the call to **PrepareSubmit**.</span></span> <span data-ttu-id="92b5b-129">**SpoolerNotify** sincroniza a la cola MAPI y se asegura de que todos los proveedores de transporte necesarios se registran y sus tipos de dirección se registran.</span><span class="sxs-lookup"><span data-stu-id="92b5b-129">**SpoolerNotify** synchronizes the MAPI spooler and ensures that all needed transport providers are logged on and their address types are registered.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="92b5b-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="92b5b-130">See also</span></span>



[<span data-ttu-id="92b5b-131">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="92b5b-131">IMAPIFolder::GetMessageStatus</span></span>](imapifolder-getmessagestatus.md)
  
[<span data-ttu-id="92b5b-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="92b5b-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="92b5b-133">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="92b5b-133">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

