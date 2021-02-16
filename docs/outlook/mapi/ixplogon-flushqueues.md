---
title: IXPLogonFlushQueues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.FlushQueues
api_type:
- COM
ms.assetid: c1f630c6-9e95-49c0-9757-4685c98184dc
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: fb26c7f366ce6a262362001773e825c60d0e4ec3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421973"
---
# <a name="ixplogonflushqueues"></a><span data-ttu-id="c97d7-103">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="c97d7-103">IXPLogon::FlushQueues</span></span>

  
  
<span data-ttu-id="c97d7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c97d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c97d7-105">Solicita que el proveedor de transporte entregue inmediatamente todos los mensajes entrantes o salientes pendientes.</span><span class="sxs-lookup"><span data-stu-id="c97d7-105">Requests that the transport provider immediately deliver all pending inbound or outbound messages.</span></span>
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c97d7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c97d7-106">Parameters</span></span>

 <span data-ttu-id="c97d7-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="c97d7-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="c97d7-108">[entrada] Identificador de la ventana principal de los cuadros de diálogo o ventanas que muestra este método.</span><span class="sxs-lookup"><span data-stu-id="c97d7-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="c97d7-109">_cbTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="c97d7-109">_cbTargetTransport_</span></span>
  
> <span data-ttu-id="c97d7-110">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c97d7-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="c97d7-111">_lpTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="c97d7-111">_lpTargetTransport_</span></span>
  
> <span data-ttu-id="c97d7-112">[entrada] Reservado; debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="c97d7-112">[in] Reserved; must be NULL.</span></span>
    
 <span data-ttu-id="c97d7-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c97d7-113">_ulFlags_</span></span>
  
> <span data-ttu-id="c97d7-114">[entrada] Máscara de bits de marcas que controla cómo se realiza el vaciado de la cola de mensajes.</span><span class="sxs-lookup"><span data-stu-id="c97d7-114">[in] A bitmask of flags that controls how message queue flushing is accomplished.</span></span> <span data-ttu-id="c97d7-115">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="c97d7-115">The following flags can be set:</span></span>
    
<span data-ttu-id="c97d7-116">FLUSH_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="c97d7-116">FLUSH_DOWNLOAD</span></span> 
  
> <span data-ttu-id="c97d7-117">Las colas o colas de mensajes entrantes deben vaciarse.</span><span class="sxs-lookup"><span data-stu-id="c97d7-117">The inbound message queue or queues should be flushed.</span></span>
    
<span data-ttu-id="c97d7-118">FLUSH_FORCE</span><span class="sxs-lookup"><span data-stu-id="c97d7-118">FLUSH_FORCE</span></span> 
  
> <span data-ttu-id="c97d7-119">El proveedor de transporte debe procesar esta solicitud, si es posible, incluso si hacerlo requiere mucho tiempo.</span><span class="sxs-lookup"><span data-stu-id="c97d7-119">The transport provider should process this request, if possible, even if doing so is time consuming.</span></span> 
    
<span data-ttu-id="c97d7-120">FLUSH_NO_UI</span><span class="sxs-lookup"><span data-stu-id="c97d7-120">FLUSH_NO_UI</span></span> 
  
> <span data-ttu-id="c97d7-121">El proveedor de transporte no debe mostrar una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="c97d7-121">The transport provider should not display a user interface.</span></span>
    
<span data-ttu-id="c97d7-122">FLUSH_UPLOAD</span><span class="sxs-lookup"><span data-stu-id="c97d7-122">FLUSH_UPLOAD</span></span> 
  
> <span data-ttu-id="c97d7-123">Las colas o colas de mensajes salientes deben vaciarse.</span><span class="sxs-lookup"><span data-stu-id="c97d7-123">The outbound message queue or queues should be flushed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c97d7-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c97d7-124">Return value</span></span>

<span data-ttu-id="c97d7-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="c97d7-125">S_OK</span></span> 
  
> <span data-ttu-id="c97d7-126">La llamada se realiza correctamente y devuelve el valor o los valores esperados.</span><span class="sxs-lookup"><span data-stu-id="c97d7-126">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c97d7-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c97d7-127">Remarks</span></span>

<span data-ttu-id="c97d7-128">La cola MAPI llama al método **IXPLogon::FlushQueues** para informar al proveedor de transporte de que la cola MAPI está a punto de comenzar a procesar mensajes.</span><span class="sxs-lookup"><span data-stu-id="c97d7-128">The MAPI spooler calls the **IXPLogon::FlushQueues** method to advise the transport provider that the MAPI spooler is about to begin processing messages.</span></span> <span data-ttu-id="c97d7-129">El proveedor de transporte debe llamar al método [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) para establecer un bit adecuado para su estado en la propiedad **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de su fila de estado.</span><span class="sxs-lookup"><span data-stu-id="c97d7-129">The transport provider should call the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method to set an appropriate bit for its state in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property of its status row.</span></span> <span data-ttu-id="c97d7-130">Después de actualizar su fila de estado, el proveedor de transporte debe devolver S_OK para la **llamada FlushQueues.**</span><span class="sxs-lookup"><span data-stu-id="c97d7-130">After updating its status row, the transport provider should return S_OK for the **FlushQueues** call.</span></span> <span data-ttu-id="c97d7-131">A continuación, la cola MAPI inicia el envío de mensajes, con la operación sincrónica en la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="c97d7-131">The MAPI spooler then starts sending messages, with the operation being synchronous to the MAPI spooler.</span></span> 
  
<span data-ttu-id="c97d7-132">Para admitir su implementación del método [IMAPIStatus::FlushQueues,](imapistatus-flushqueues.md) la cola MAPI llama a **IXPLogon::FlushQueues** para todos los objetos de inicio de sesión de los proveedores de transporte activos que se ejecutan en una sesión de perfil.</span><span class="sxs-lookup"><span data-stu-id="c97d7-132">To support its implementation of the [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method, the MAPI spooler calls **IXPLogon::FlushQueues** for all logon objects for active transport providers that are running in a profile session.</span></span> <span data-ttu-id="c97d7-133">Cuando se llama al método **FlushQueues** de un proveedor de transporte como resultado de una llamada de aplicación cliente a **IMAPIStatus::FlushQueues**, el procesamiento de mensajes se produce de forma asincrónica para el cliente.</span><span class="sxs-lookup"><span data-stu-id="c97d7-133">When a transport provider's **FlushQueues** method is called as a result of a client application call to **IMAPIStatus::FlushQueues**, the message processing occurs asynchronously to the client.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c97d7-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c97d7-134">See also</span></span>



[<span data-ttu-id="c97d7-135">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="c97d7-135">IMAPIStatus::FlushQueues</span></span>](imapistatus-flushqueues.md)
  
[<span data-ttu-id="c97d7-136">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c97d7-136">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

