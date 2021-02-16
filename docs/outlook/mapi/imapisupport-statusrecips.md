---
title: IMAPISupportStatusRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.StatusRecips
api_type:
- COM
ms.assetid: 9c34538e-5ba4-47c8-8002-85afa9d6c067
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 39d8786bf558ade4599d69e0a764f87fe60d99f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408771"
---
# <a name="imapisupportstatusrecips"></a><span data-ttu-id="31828-103">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="31828-103">IMAPISupport::StatusRecips</span></span>

  
  
<span data-ttu-id="31828-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31828-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31828-105">Genera informes de entrega y no entrega.</span><span class="sxs-lookup"><span data-stu-id="31828-105">Generates delivery and nondelivery reports.</span></span>
  
```cpp
HRESULT StatusRecips(
LPMESSAGE lpMessage,
LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="31828-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="31828-106">Parameters</span></span>

 <span data-ttu-id="31828-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="31828-107">_lpMessage_</span></span>
  
> <span data-ttu-id="31828-108">[entrada] Puntero al mensaje para el que se debe generar el informe.</span><span class="sxs-lookup"><span data-stu-id="31828-108">[in] A pointer to the message for which the report should be generated.</span></span>
    
 <span data-ttu-id="31828-109">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="31828-109">_lpRecipList_</span></span>
  
> <span data-ttu-id="31828-110">[entrada] Puntero a una [estructura ADRLIST](adrlist.md) que describe los destinatarios del mensaje que apunta  _lpMessage_.</span><span class="sxs-lookup"><span data-stu-id="31828-110">[in] A pointer to an [ADRLIST](adrlist.md) structure that describes the recipients of the message pointed to by  _lpMessage_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="31828-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="31828-111">Return value</span></span>

<span data-ttu-id="31828-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="31828-112">S_OK</span></span> 
  
> <span data-ttu-id="31828-113">El informe se generó correctamente.</span><span class="sxs-lookup"><span data-stu-id="31828-113">The report was successfully generated.</span></span>
    
<span data-ttu-id="31828-114">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="31828-114">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="31828-115">La llamada se ha hecho correctamente en general, pero no hay opciones de destinatario para este tipo de destinatario.</span><span class="sxs-lookup"><span data-stu-id="31828-115">The call succeeded overall, but there are no recipient options for this type of recipient.</span></span> <span data-ttu-id="31828-116">Cuando se devuelve esta advertencia, la llamada debe tratarse como correcta.</span><span class="sxs-lookup"><span data-stu-id="31828-116">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="31828-117">Para probar esta advertencia, use la **macro HR_FAILED** datos.</span><span class="sxs-lookup"><span data-stu-id="31828-117">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="31828-118">Para obtener más información, vea [Usar macros para el control de errores.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="31828-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="31828-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="31828-119">Remarks</span></span>

<span data-ttu-id="31828-120">El **método IMAPISupport::StatusRecips** se implementa para objetos de compatibilidad del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="31828-120">The **IMAPISupport::StatusRecips** method is implemented for transport provider support objects.</span></span> <span data-ttu-id="31828-121">Los proveedores de transporte llaman a **StatusRecips** para solicitar que MAPI envíe un informe de entrega o no entrega a un conjunto de uno o varios de los destinatarios de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="31828-121">Transport providers call **StatusRecips** to request that MAPI send a delivery or nondelivery report to a set of one or more of the recipients of a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="31828-122">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="31828-122">Notes to callers</span></span>

<span data-ttu-id="31828-123">Puede llamar a **StatusRecips varias** veces durante el procesamiento de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="31828-123">You can call **StatusRecips** multiple times during the processing of a message.</span></span> <span data-ttu-id="31828-124">Sin embargo, si llama a **StatusRecips** para un mensaje abierto, haga todo lo posible para recopilar toda la información de entrega y no entrega para los destinatarios del mensaje y llamar a **StatusRecips** para esa lista de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="31828-124">However, if you call **StatusRecips** for an open message, do your best to collect all delivery and nondelivery information for the message recipients and call **StatusRecips** for that recipient list.</span></span> <span data-ttu-id="31828-125">Un único punto de recopilación es importante, ya que varias **llamadas StatusRecips** para un destinatario pueden dar como resultado que se envíen varios informes idénticos.</span><span class="sxs-lookup"><span data-stu-id="31828-125">A single point of collection is important, because multiple **StatusRecips** calls for one recipient can result in multiple identical reports being sent.</span></span> 
  
<span data-ttu-id="31828-126">Almacene las propiedades relacionadas con la entrega de mensajes o nondelivery en la estructura **ADRLIST** indicada por el parámetro _lpRecipList._</span><span class="sxs-lookup"><span data-stu-id="31828-126">Store properties that relate to message delivery or nondelivery in the **ADRLIST** structure indicated by the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="31828-127">Para obtener una lista completa de propiedades obligatorias y opcionales para informes de entrega e informes de no entrega, vea Propiedades de mensaje de informe requeridas y Propiedades opcionales [del mensaje de informe.](optional-report-message-properties.md) [](required-report-message-properties.md)</span><span class="sxs-lookup"><span data-stu-id="31828-127">For a complete list of required and optional properties for delivery reports and nondelivery reports, see [Required Report Message Properties](required-report-message-properties.md) and [Optional Report Message Properties](optional-report-message-properties.md).</span></span> 
  
<span data-ttu-id="31828-128">Asigne memoria para la **estructura ADRLIST** _en lpRecipList_ mediante las [funciones MAPIAllocateBuffer](mapiallocatebuffer.md) y [MAPIAllocateMore.](mapiallocatemore.md)</span><span class="sxs-lookup"><span data-stu-id="31828-128">Allocate memory for the **ADRLIST** structure in  _lpRecipList_ by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIAllocateMore](mapiallocatemore.md) functions.</span></span> <span data-ttu-id="31828-129">MAPI libera la memoria llamando a la [función MAPIFreeBuffer](mapifreebuffer.md) solo si **StatusRecips se realiza** correctamente.</span><span class="sxs-lookup"><span data-stu-id="31828-129">MAPI releases the memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function only if **StatusRecips** succeeds.</span></span> 
  
<span data-ttu-id="31828-130">Para obtener información general sobre los informes de entrega y no entrega, vea [mensajes de informe MAPI](mapi-report-messages.md).</span><span class="sxs-lookup"><span data-stu-id="31828-130">For an overview of delivery and nondelivery reports, see [MAPI Report Messages](mapi-report-messages.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="31828-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="31828-131">See also</span></span>



[<span data-ttu-id="31828-132">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="31828-132">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="31828-133">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="31828-133">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="31828-134">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="31828-134">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="31828-135">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="31828-135">IXPLogon::EndMessage</span></span>](ixplogon-endmessage.md)
  
[<span data-ttu-id="31828-136">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="31828-136">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="31828-137">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="31828-137">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="31828-138">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="31828-138">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="31828-139">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="31828-139">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

