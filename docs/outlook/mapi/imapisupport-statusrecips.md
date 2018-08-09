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
ms.openlocfilehash: f3642c890c3922611d57dea6f03aca5606876864
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817569"
---
# <a name="imapisupportstatusrecips"></a><span data-ttu-id="93d12-103">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="93d12-103">IMAPISupport::StatusRecips</span></span>

  
  
<span data-ttu-id="93d12-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="93d12-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="93d12-105">Genera informes de entrega y no entrega.</span><span class="sxs-lookup"><span data-stu-id="93d12-105">Generates delivery and nondelivery reports.</span></span>
  
```cpp
HRESULT StatusRecips(
LPMESSAGE lpMessage,
LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="93d12-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="93d12-106">Parameters</span></span>

 <span data-ttu-id="93d12-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="93d12-107">_lpMessage_</span></span>
  
> <span data-ttu-id="93d12-108">[entrada] Un puntero al mensaje para el que se debe generar el informe.</span><span class="sxs-lookup"><span data-stu-id="93d12-108">[in] A pointer to the message for which the report should be generated.</span></span>
    
 <span data-ttu-id="93d12-109">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="93d12-109">_lpRecipList_</span></span>
  
> <span data-ttu-id="93d12-110">[entrada] Un puntero a una estructura [ADRLIST](adrlist.md) que describe a los destinatarios del mensaje que apunta _lpMessage_.</span><span class="sxs-lookup"><span data-stu-id="93d12-110">[in] A pointer to an [ADRLIST](adrlist.md) structure that describes the recipients of the message pointed to by  _lpMessage_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="93d12-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="93d12-111">Return value</span></span>

<span data-ttu-id="93d12-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="93d12-112">S_OK</span></span> 
  
> <span data-ttu-id="93d12-113">El informe se ha generado correctamente.</span><span class="sxs-lookup"><span data-stu-id="93d12-113">The report was successfully generated.</span></span>
    
<span data-ttu-id="93d12-114">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="93d12-114">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="93d12-115">La llamada satisfactoria, pero no hay ningún destinatarios opciones para este tipo de destinatario.</span><span class="sxs-lookup"><span data-stu-id="93d12-115">The call succeeded overall, but there are no recipient options for this type of recipient.</span></span> <span data-ttu-id="93d12-116">Cuando se devuelve esta advertencia, la llamada se debe controlarse como correcta.</span><span class="sxs-lookup"><span data-stu-id="93d12-116">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="93d12-117">Para probar esta advertencia, utilice la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="93d12-117">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="93d12-118">Para obtener más información, vea [Uso de Macros para el control de errores](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="93d12-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="93d12-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="93d12-119">Remarks</span></span>

<span data-ttu-id="93d12-120">El método **IMAPISupport::StatusRecips** se implementa para los objetos de soporte técnico del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="93d12-120">The **IMAPISupport::StatusRecips** method is implemented for transport provider support objects.</span></span> <span data-ttu-id="93d12-121">Los proveedores de transporte llame a **StatusRecips** para solicitar que envían MAPI un informe de entrega o de no entrega a un conjunto de uno o varios de los destinatarios de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="93d12-121">Transport providers call **StatusRecips** to request that MAPI send a delivery or nondelivery report to a set of one or more of the recipients of a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="93d12-122">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="93d12-122">Notes to callers</span></span>

<span data-ttu-id="93d12-123">Puede llamar varias veces a **StatusRecips** durante el procesamiento de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="93d12-123">You can call **StatusRecips** multiple times during the processing of a message.</span></span> <span data-ttu-id="93d12-124">Sin embargo, si se llama a **StatusRecips** para abrir el mensaje, realice los procedimientos para recopilar toda la información de entrega y no entrega de los destinatarios del mensaje y llamar a **StatusRecips** para esa lista de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="93d12-124">However, if you call **StatusRecips** for an open message, do your best to collect all delivery and nondelivery information for the message recipients and call **StatusRecips** for that recipient list.</span></span> <span data-ttu-id="93d12-125">Un único punto de colección es importante, porque pueden producir varias llamadas **StatusRecips** para un destinatario en varios informes idénticos que se está enviados.</span><span class="sxs-lookup"><span data-stu-id="93d12-125">A single point of collection is important, because multiple **StatusRecips** calls for one recipient can result in multiple identical reports being sent.</span></span> 
  
<span data-ttu-id="93d12-126">Almacenar propiedades relacionadas con la entrega del mensaje o no entrega en la estructura **ADRLIST** indicada por el parámetro _lpRecipList_ .</span><span class="sxs-lookup"><span data-stu-id="93d12-126">Store properties that relate to message delivery or nondelivery in the **ADRLIST** structure indicated by the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="93d12-127">Para obtener una lista completa de las propiedades opcionales y obligatorios para informes de entrega e informes de no entrega, vea [Propiedades de mensaje de informe necesarias](required-report-message-properties.md) y [Propiedades de mensaje de informe opcionales](optional-report-message-properties.md).</span><span class="sxs-lookup"><span data-stu-id="93d12-127">For a complete list of required and optional properties for delivery reports and nondelivery reports, see [Required Report Message Properties](required-report-message-properties.md) and [Optional Report Message Properties](optional-report-message-properties.md).</span></span> 
  
<span data-ttu-id="93d12-128">Asignar memoria para la estructura **ADRLIST** en _lpRecipList_ mediante el uso de las funciones [MAPIAllocateBuffer](mapiallocatebuffer.md) y [MAPIAllocateMore](mapiallocatemore.md) .</span><span class="sxs-lookup"><span data-stu-id="93d12-128">Allocate memory for the **ADRLIST** structure in  _lpRecipList_ by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIAllocateMore](mapiallocatemore.md) functions.</span></span> <span data-ttu-id="93d12-129">MAPI libera la memoria mediante una llamada a la función [MAPIFreeBuffer](mapifreebuffer.md) sólo si **StatusRecips** se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="93d12-129">MAPI releases the memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function only if **StatusRecips** succeeds.</span></span> 
  
<span data-ttu-id="93d12-130">Para obtener información general de informes de entrega y no entrega, vea [Los mensajes de informe de MAPI](mapi-report-messages.md).</span><span class="sxs-lookup"><span data-stu-id="93d12-130">For an overview of delivery and nondelivery reports, see [MAPI Report Messages](mapi-report-messages.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="93d12-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="93d12-131">See also</span></span>



[<span data-ttu-id="93d12-132">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="93d12-132">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="93d12-133">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="93d12-133">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="93d12-134">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="93d12-134">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="93d12-135">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="93d12-135">IXPLogon::EndMessage</span></span>](ixplogon-endmessage.md)
  
[<span data-ttu-id="93d12-136">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="93d12-136">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="93d12-137">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="93d12-137">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="93d12-138">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="93d12-138">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="93d12-139">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="93d12-139">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

