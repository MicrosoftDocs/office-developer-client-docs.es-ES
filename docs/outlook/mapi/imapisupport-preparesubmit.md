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
# <a name="imapisupportpreparesubmit"></a><span data-ttu-id="bdbbb-103">IMAPISupport::PrepareSubmit</span><span class="sxs-lookup"><span data-stu-id="bdbbb-103">IMAPISupport::PrepareSubmit</span></span>

  
  
<span data-ttu-id="bdbbb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bdbbb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bdbbb-105">Prepara un mensaje para su envío a la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="bdbbb-105">Prepares a message for submission to the MAPI spooler.</span></span>
  
```cpp
HRESULT PrepareSubmit(
LPMESSAGE lpMessage,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="bdbbb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bdbbb-106">Parameters</span></span>

 <span data-ttu-id="bdbbb-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="bdbbb-107">_lpMessage_</span></span>
  
> <span data-ttu-id="bdbbb-108">[entrada] Puntero al mensaje que se debe preparar.</span><span class="sxs-lookup"><span data-stu-id="bdbbb-108">[in] A pointer to the message to prepare.</span></span>
    
 <span data-ttu-id="bdbbb-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="bdbbb-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="bdbbb-110">[entrada, salida] En la entrada, el  _parámetro lpulFlags_ está reservado y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="bdbbb-110">[in, out] On input, the  _lpulFlags_ parameter is reserved and must be zero.</span></span> <span data-ttu-id="bdbbb-111">En el resultado,  _lpulFlags_ debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="bdbbb-111">On output,  _lpulFlags_ must be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bdbbb-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bdbbb-112">Return value</span></span>

<span data-ttu-id="bdbbb-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="bdbbb-113">S_OK</span></span> 
  
> <span data-ttu-id="bdbbb-114">El mensaje se preparó correctamente.</span><span class="sxs-lookup"><span data-stu-id="bdbbb-114">The message was successfully prepared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bdbbb-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bdbbb-115">Remarks</span></span>

<span data-ttu-id="bdbbb-116">El **método IMAPISupport::P repareSubmit** se implementa para objetos de compatibilidad del proveedor de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="bdbbb-116">The **IMAPISupport::PrepareSubmit** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="bdbbb-117">Los proveedores del almacén de mensajes llaman a **PrepareSubmit** en su implementación del método [IMessage::SubmitMessage](imessage-submitmessage.md) para preparar un mensaje para su envío a la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="bdbbb-117">Message store providers call **PrepareSubmit** in their implementation of the [IMessage::SubmitMessage](imessage-submitmessage.md) method to prepare a message for submission to the MAPI spooler.</span></span> 
  
 <span data-ttu-id="bdbbb-118">**PrepareSubmit** se usa para controlar los mensajes que tienen la marca MSGFLAG_RESEND establecida en su propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="bdbbb-118">**PrepareSubmit** is used to handle messages that have the MSGFLAG_RESEND flag set in their **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="bdbbb-119">MSGFLAG_RESEND se establece para los mensajes que incluyen una solicitud que se va a enviar cuando se produce un error de transmisión inicial.</span><span class="sxs-lookup"><span data-stu-id="bdbbb-119">MSGFLAG_RESEND is set for messages that include a request to be resent when an initial transmission fails.</span></span> <span data-ttu-id="bdbbb-120">**PrepareSubmit** determina cuál de los destinatarios de la lista de destinatarios recibió correctamente el mensaje y cuál no.</span><span class="sxs-lookup"><span data-stu-id="bdbbb-120">**PrepareSubmit** determines which of the recipients in the recipient list successfully received the message and which did not.</span></span> 
  
<span data-ttu-id="bdbbb-121">Para obtener acceso a la lista de destinatarios, **PrepareSubmit** llama al método [IMessage::GetRecipientTable del](imessage-getrecipienttable.md) mensaje.</span><span class="sxs-lookup"><span data-stu-id="bdbbb-121">To access the recipient list, **PrepareSubmit** calls the message's [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method.</span></span> <span data-ttu-id="bdbbb-122">Para recuperar los datos del destinatario, **PrepareSubmit** llama al método [IMAPITable::QueryRows](imapitable-queryrows.md) de la tabla de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="bdbbb-122">To retrieve the recipient data, **PrepareSubmit** calls the recipient table's [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> <span data-ttu-id="bdbbb-123">Para cada fila de la tabla, **PrepareSubmit** comprueba la propiedad **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) y realiza una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="bdbbb-123">For each row in the table, **PrepareSubmit** checks the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property and takes one of the following actions:</span></span>
  
- <span data-ttu-id="bdbbb-124">Si se MAPI_SUBMITTED marca, **PrepareSubmit** borra la marca y establece la propiedad **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) en FALSE.</span><span class="sxs-lookup"><span data-stu-id="bdbbb-124">If the MAPI_SUBMITTED flag is set, **PrepareSubmit** clears the flag and sets the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property to FALSE.</span></span>
    
- <span data-ttu-id="bdbbb-125">Si no MAPI_SUBMITTED marca, **PrepareSubmit** cambia  PR_RECIPIENT_TYPE a MAPI_P1 y establece **PR_RESPONSIBILITY** en TRUE.</span><span class="sxs-lookup"><span data-stu-id="bdbbb-125">If the MAPI_SUBMITTED flag is not set, **PrepareSubmit** changes **PR_RECIPIENT_TYPE** to MAPI_P1 and sets **PR_RESPONSIBILITY** to TRUE.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="bdbbb-126">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="bdbbb-126">Notes to callers</span></span>

<span data-ttu-id="bdbbb-127">Antes de llamar a **PrepareSubmit,** asegúrese de haber llamado al método [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) y de establecer la marca NOTIFY_READYTOSEND en el _parámetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="bdbbb-127">Before you call **PrepareSubmit**, be sure you have called the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method and set the NOTIFY_READYTOSEND flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="bdbbb-128">La **llamada SpoolerNotify** debe realizarse una vez por sesión antes de llamar a **PrepareSubmit**.</span><span class="sxs-lookup"><span data-stu-id="bdbbb-128">The **SpoolerNotify** call must be made once per session before the call to **PrepareSubmit**.</span></span> <span data-ttu-id="bdbbb-129">**SpoolerNotify** sincroniza la cola MAPI y garantiza que todos los proveedores de transporte necesarios hayan iniciado sesión y que sus tipos de direcciones estén registrados.</span><span class="sxs-lookup"><span data-stu-id="bdbbb-129">**SpoolerNotify** synchronizes the MAPI spooler and ensures that all needed transport providers are logged on and their address types are registered.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bdbbb-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bdbbb-130">See also</span></span>



[<span data-ttu-id="bdbbb-131">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="bdbbb-131">IMAPIFolder::GetMessageStatus</span></span>](imapifolder-getmessagestatus.md)
  
[<span data-ttu-id="bdbbb-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="bdbbb-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="bdbbb-133">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="bdbbb-133">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

