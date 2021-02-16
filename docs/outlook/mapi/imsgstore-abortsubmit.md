---
title: IMsgStoreAbortSubmit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.AbortSubmit
api_type:
- COM
ms.assetid: 9be6b88e-2510-4b82-8b35-5f20a0f99fc0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1486730dfa2d76bf8e97439213851b195504962f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414385"
---
# <a name="imsgstoreabortsubmit"></a><span data-ttu-id="778c0-103">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="778c0-103">IMsgStore::AbortSubmit</span></span>

  
  
<span data-ttu-id="778c0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="778c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="778c0-105">Intenta quitar un mensaje de la cola saliente.</span><span class="sxs-lookup"><span data-stu-id="778c0-105">Attempts to remove a message from the outgoing queue.</span></span>
  
```cpp
AbortSubmit(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="778c0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="778c0-106">Parameters</span></span>

 <span data-ttu-id="778c0-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="778c0-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="778c0-108">[entrada] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="778c0-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="778c0-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="778c0-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="778c0-110">[entrada] Puntero al identificador de entrada del mensaje que se quitará de la cola saliente.</span><span class="sxs-lookup"><span data-stu-id="778c0-110">[in] A pointer to the entry identifier of the message to remove from the outgoing queue.</span></span> 
    
 <span data-ttu-id="778c0-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="778c0-111">_ulFlags_</span></span>
  
> <span data-ttu-id="778c0-112">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="778c0-112">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="778c0-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="778c0-113">Return value</span></span>

<span data-ttu-id="778c0-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="778c0-114">S_OK</span></span> 
  
> <span data-ttu-id="778c0-115">El mensaje se quitó correctamente de la cola saliente.</span><span class="sxs-lookup"><span data-stu-id="778c0-115">The message was successfully removed from the outgoing queue.</span></span>
    
<span data-ttu-id="778c0-116">MAPI_E_NOT_IN_QUEUE</span><span class="sxs-lookup"><span data-stu-id="778c0-116">MAPI_E_NOT_IN_QUEUE</span></span> 
  
> <span data-ttu-id="778c0-117">El mensaje identificado por  _lpEntryID_ ya no está en la cola de salida del almacén de mensajes, normalmente porque ya se ha enviado.</span><span class="sxs-lookup"><span data-stu-id="778c0-117">The message identified by  _lpEntryID_ is no longer in the message store's outgoing queue, typically because it has already been sent.</span></span> 
    
<span data-ttu-id="778c0-118">MAPI_E_UNABLE_TO_ABORT</span><span class="sxs-lookup"><span data-stu-id="778c0-118">MAPI_E_UNABLE_TO_ABORT</span></span> 
  
> <span data-ttu-id="778c0-119">El mensaje identificado por  _lpEntryID_ está bloqueado por la cola MAPI y la operación no se puede anular.</span><span class="sxs-lookup"><span data-stu-id="778c0-119">The message identified by  _lpEntryID_ is locked by the MAPI spooler, and the operation cannot be aborted.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="778c0-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="778c0-120">Remarks</span></span>

<span data-ttu-id="778c0-121">El **método IMsgStore::AbortSubmit** intenta quitar un mensaje enviado de la cola saliente del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="778c0-121">The **IMsgStore::AbortSubmit** method attempts to remove a submitted message from the message store's outgoing queue.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="778c0-122">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="778c0-122">Notes to callers</span></span>

<span data-ttu-id="778c0-123">Después de enviar un mensaje, anular el envío llamando a **AbortSubmit** es la única acción que se puede realizar en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="778c0-123">After a message is submitted, aborting the submission by calling **AbortSubmit** is the only action that can be performed on the message.</span></span> <span data-ttu-id="778c0-124">No espere que **AbortSubmit** siempre se realice correctamente.</span><span class="sxs-lookup"><span data-stu-id="778c0-124">Do not expect **AbortSubmit** to always succeed.</span></span> <span data-ttu-id="778c0-125">Según cómo se implemente el sistema de mensajería subyacente, es posible que no sea posible cancelar el envío del mensaje.</span><span class="sxs-lookup"><span data-stu-id="778c0-125">Depending on how the underlying messaging system is implemented, it might not be possible to cancel the sending of the message.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="778c0-126">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="778c0-126">MFCMAPI reference</span></span>

<span data-ttu-id="778c0-127">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="778c0-127">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="778c0-128">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="778c0-128">**File**</span></span>|<span data-ttu-id="778c0-129">**Función**</span><span class="sxs-lookup"><span data-stu-id="778c0-129">**Function**</span></span>|<span data-ttu-id="778c0-130">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="778c0-130">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="778c0-131">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="778c0-131">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="778c0-132">CFolderDlg::OnAbortSubmit</span><span class="sxs-lookup"><span data-stu-id="778c0-132">CFolderDlg::OnAbortSubmit</span></span>  <br/> |<span data-ttu-id="778c0-133">MFCMAPI usa el **método IMsgStore::AbortSubmit** para anular el envío del mensaje seleccionado.</span><span class="sxs-lookup"><span data-stu-id="778c0-133">MFCMAPI uses the **IMsgStore::AbortSubmit** method to abort the submission of the selected message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="778c0-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="778c0-134">See also</span></span>



[<span data-ttu-id="778c0-135">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="778c0-135">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="778c0-136">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="778c0-136">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="778c0-137">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="778c0-137">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

