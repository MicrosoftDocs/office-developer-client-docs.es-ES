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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341772"
---
# <a name="imapisupportstatusrecips"></a><span data-ttu-id="7072f-103">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="7072f-103">IMAPISupport::StatusRecips</span></span>

  
  
<span data-ttu-id="7072f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7072f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7072f-105">Genera informes de entrega y de no entrega.</span><span class="sxs-lookup"><span data-stu-id="7072f-105">Generates delivery and nondelivery reports.</span></span>
  
```cpp
HRESULT StatusRecips(
LPMESSAGE lpMessage,
LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="7072f-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="7072f-106">Parameters</span></span>

 <span data-ttu-id="7072f-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="7072f-107">_lpMessage_</span></span>
  
> <span data-ttu-id="7072f-108">a Un puntero al mensaje para el que se debe generar el informe.</span><span class="sxs-lookup"><span data-stu-id="7072f-108">[in] A pointer to the message for which the report should be generated.</span></span>
    
 <span data-ttu-id="7072f-109">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="7072f-109">_lpRecipList_</span></span>
  
> <span data-ttu-id="7072f-110">a Un puntero a una estructura [ADRLIST](adrlist.md) que describe los destinatarios del mensaje al que señala _lpMessage_.</span><span class="sxs-lookup"><span data-stu-id="7072f-110">[in] A pointer to an [ADRLIST](adrlist.md) structure that describes the recipients of the message pointed to by  _lpMessage_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7072f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7072f-111">Return value</span></span>

<span data-ttu-id="7072f-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="7072f-112">S_OK</span></span> 
  
> <span data-ttu-id="7072f-113">El informe se generó correctamente.</span><span class="sxs-lookup"><span data-stu-id="7072f-113">The report was successfully generated.</span></span>
    
<span data-ttu-id="7072f-114">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="7072f-114">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="7072f-115">La llamada se realizó en general, pero no hay opciones de destinatarios para este tipo de destinatario.</span><span class="sxs-lookup"><span data-stu-id="7072f-115">The call succeeded overall, but there are no recipient options for this type of recipient.</span></span> <span data-ttu-id="7072f-116">Cuando se devuelve esta advertencia, la llamada se debe administrar como correcta.</span><span class="sxs-lookup"><span data-stu-id="7072f-116">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="7072f-117">Para probar esta advertencia, use la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="7072f-117">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="7072f-118">Para obtener más información, consulte [usar macros para el control de errores](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="7072f-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7072f-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7072f-119">Remarks</span></span>

<span data-ttu-id="7072f-120">El método **IMAPISupport:: StatusRecips** se implementa para los objetos de soporte del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="7072f-120">The **IMAPISupport::StatusRecips** method is implemented for transport provider support objects.</span></span> <span data-ttu-id="7072f-121">Los proveedores de transporte llaman a **StatusRecips** para solicitar que MAPI envíe un informe de entrega o de no entrega a un conjunto de uno o varios de los destinatarios de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="7072f-121">Transport providers call **StatusRecips** to request that MAPI send a delivery or nondelivery report to a set of one or more of the recipients of a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7072f-122">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="7072f-122">Notes to callers</span></span>

<span data-ttu-id="7072f-123">Puede llamar a **StatusRecips** varias veces durante el procesamiento de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="7072f-123">You can call **StatusRecips** multiple times during the processing of a message.</span></span> <span data-ttu-id="7072f-124">Sin embargo, si llama a **StatusRecips** para un mensaje abierto, haga lo mejor para recopilar toda la información de entrega y de no entrega para los destinatarios del mensaje y llamar a **StatusRecips** para la lista de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="7072f-124">However, if you call **StatusRecips** for an open message, do your best to collect all delivery and nondelivery information for the message recipients and call **StatusRecips** for that recipient list.</span></span> <span data-ttu-id="7072f-125">Un único punto de recopilación es importante, ya que varias llamadas de **StatusRecips** para un destinatario pueden dar lugar a que se envíen varios informes idénticos.</span><span class="sxs-lookup"><span data-stu-id="7072f-125">A single point of collection is important, because multiple **StatusRecips** calls for one recipient can result in multiple identical reports being sent.</span></span> 
  
<span data-ttu-id="7072f-126">Almacene las propiedades relacionadas con la entrega de mensajes o no entrega en la estructura **ADRLIST** indicada por el parámetro _lpRecipList_ .</span><span class="sxs-lookup"><span data-stu-id="7072f-126">Store properties that relate to message delivery or nondelivery in the **ADRLIST** structure indicated by the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="7072f-127">Para obtener una lista completa de las propiedades necesarias y opcionales para los informes de entrega y los informes de no entrega, consulte reQuired [Report Message Properties](required-report-message-properties.md) y [Optional Report Message Properties](optional-report-message-properties.md).</span><span class="sxs-lookup"><span data-stu-id="7072f-127">For a complete list of required and optional properties for delivery reports and nondelivery reports, see [Required Report Message Properties](required-report-message-properties.md) and [Optional Report Message Properties](optional-report-message-properties.md).</span></span> 
  
<span data-ttu-id="7072f-128">Asigne memoria para la estructura **ADRLIST** en _lpRecipList_ mediante las funciones [MAPIAllocateBuffer](mapiallocatebuffer.md) y [MAPIAllocateMore](mapiallocatemore.md) .</span><span class="sxs-lookup"><span data-stu-id="7072f-128">Allocate memory for the **ADRLIST** structure in  _lpRecipList_ by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIAllocateMore](mapiallocatemore.md) functions.</span></span> <span data-ttu-id="7072f-129">MAPI libera la memoria al llamar a la función [MAPIFreeBuffer](mapifreebuffer.md) solo si **StatusRecips** se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="7072f-129">MAPI releases the memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function only if **StatusRecips** succeeds.</span></span> 
  
<span data-ttu-id="7072f-130">Para obtener información general sobre los informes de entrega y de no entrega, consulte [MAPI Report messages](mapi-report-messages.md).</span><span class="sxs-lookup"><span data-stu-id="7072f-130">For an overview of delivery and nondelivery reports, see [MAPI Report Messages](mapi-report-messages.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7072f-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="7072f-131">See also</span></span>



[<span data-ttu-id="7072f-132">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="7072f-132">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="7072f-133">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="7072f-133">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="7072f-134">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="7072f-134">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="7072f-135">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="7072f-135">IXPLogon::EndMessage</span></span>](ixplogon-endmessage.md)
  
[<span data-ttu-id="7072f-136">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="7072f-136">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="7072f-137">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="7072f-137">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="7072f-138">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="7072f-138">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="7072f-139">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="7072f-139">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

