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
ms.openlocfilehash: 116e3cfaace9c0965001021575b76ec371667877
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818008"
---
# <a name="ixplogonflushqueues"></a><span data-ttu-id="1e258-103">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="1e258-103">IXPLogon::FlushQueues</span></span>

  
  
<span data-ttu-id="1e258-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1e258-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1e258-105">Solicitudes que el proveedor de transporte entrega inmediatamente todos los mensajes entrantes o salientes pendientes.</span><span class="sxs-lookup"><span data-stu-id="1e258-105">Requests that the transport provider immediately deliver all pending inbound or outbound messages.</span></span>
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="1e258-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e258-106">Parameters</span></span>

 <span data-ttu-id="1e258-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="1e258-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="1e258-108">[entrada] Identificador de la ventana principal de los cuadros de diálogo o windows que muestra este método.</span><span class="sxs-lookup"><span data-stu-id="1e258-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="1e258-109">_cbTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="1e258-109">_cbTargetTransport_</span></span>
  
> <span data-ttu-id="1e258-110">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="1e258-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="1e258-111">_lpTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="1e258-111">_lpTargetTransport_</span></span>
  
> <span data-ttu-id="1e258-112">[entrada] Reservado; debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="1e258-112">[in] Reserved; must be NULL.</span></span>
    
 <span data-ttu-id="1e258-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1e258-113">_ulFlags_</span></span>
  
> <span data-ttu-id="1e258-114">[entrada] Una máscara de bits de indicadores que controla cómo se realiza el vaciado de la cola de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1e258-114">[in] A bitmask of flags that controls how message queue flushing is accomplished.</span></span> <span data-ttu-id="1e258-115">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="1e258-115">The following flags can be set:</span></span>
    
<span data-ttu-id="1e258-116">FLUSH_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="1e258-116">FLUSH_DOWNLOAD</span></span> 
  
> <span data-ttu-id="1e258-117">Deben vaciar la cola de mensajes entrantes o colas.</span><span class="sxs-lookup"><span data-stu-id="1e258-117">The inbound message queue or queues should be flushed.</span></span>
    
<span data-ttu-id="1e258-118">FLUSH_FORCE</span><span class="sxs-lookup"><span data-stu-id="1e258-118">FLUSH_FORCE</span></span> 
  
> <span data-ttu-id="1e258-119">El proveedor de transporte debe procesar esta solicitud, si es posible, incluso si esto es mucho tiempo.</span><span class="sxs-lookup"><span data-stu-id="1e258-119">The transport provider should process this request, if possible, even if doing so is time consuming.</span></span> 
    
<span data-ttu-id="1e258-120">FLUSH_NO_UI</span><span class="sxs-lookup"><span data-stu-id="1e258-120">FLUSH_NO_UI</span></span> 
  
> <span data-ttu-id="1e258-121">El proveedor de transporte no debe mostrar una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1e258-121">The transport provider should not display a user interface.</span></span>
    
<span data-ttu-id="1e258-122">FLUSH_UPLOAD</span><span class="sxs-lookup"><span data-stu-id="1e258-122">FLUSH_UPLOAD</span></span> 
  
> <span data-ttu-id="1e258-123">Deben vaciar la cola de mensajes salientes o colas.</span><span class="sxs-lookup"><span data-stu-id="1e258-123">The outbound message queue or queues should be flushed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1e258-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e258-124">Return value</span></span>

<span data-ttu-id="1e258-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="1e258-125">S_OK</span></span> 
  
> <span data-ttu-id="1e258-126">La llamada se ha realizado correctamente y devuelve el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="1e258-126">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1e258-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1e258-127">Remarks</span></span>

<span data-ttu-id="1e258-128">La cola MAPI llama al método de **IXPLogon::FlushQueues** para indicar que el proveedor de transporte que la cola MAPI está a punto de comenzar el procesamiento de los mensajes.</span><span class="sxs-lookup"><span data-stu-id="1e258-128">The MAPI spooler calls the **IXPLogon::FlushQueues** method to advise the transport provider that the MAPI spooler is about to begin processing messages.</span></span> <span data-ttu-id="1e258-129">El proveedor de transporte debe llamar al método [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) para establecer un bit apropiado para su estado en la propiedad **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de la fila de estado correspondiente.</span><span class="sxs-lookup"><span data-stu-id="1e258-129">The transport provider should call the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method to set an appropriate bit for its state in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property of its status row.</span></span> <span data-ttu-id="1e258-130">Después de actualizar su fila de estado, el proveedor de transporte debe devolver S_OK para la llamada de **FlushQueues** .</span><span class="sxs-lookup"><span data-stu-id="1e258-130">After updating its status row, the transport provider should return S_OK for the **FlushQueues** call.</span></span> <span data-ttu-id="1e258-131">La cola MAPI, a continuación, inicia el envío de mensajes, con la operación que se va a sincrónica a la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="1e258-131">The MAPI spooler then starts sending messages, with the operation being synchronous to the MAPI spooler.</span></span> 
  
<span data-ttu-id="1e258-132">Para admitir su implementación del método [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) , la cola MAPI llama a **IXPLogon::FlushQueues** para todos los objetos de inicio de sesión para los proveedores de transporte de activo que se ejecutan en una sesión de perfil.</span><span class="sxs-lookup"><span data-stu-id="1e258-132">To support its implementation of the [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method, the MAPI spooler calls **IXPLogon::FlushQueues** for all logon objects for active transport providers that are running in a profile session.</span></span> <span data-ttu-id="1e258-133">Cuando se llama a método de **FlushQueues** del proveedor de transporte como resultado de una llamada de la aplicación de cliente a **IMAPIStatus::FlushQueues**, el procesamiento del mensaje se produce de forma asincrónica al cliente.</span><span class="sxs-lookup"><span data-stu-id="1e258-133">When a transport provider's **FlushQueues** method is called as a result of a client application call to **IMAPIStatus::FlushQueues**, the message processing occurs asynchronously to the client.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1e258-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e258-134">See also</span></span>



[<span data-ttu-id="1e258-135">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="1e258-135">IMAPIStatus::FlushQueues</span></span>](imapistatus-flushqueues.md)
  
[<span data-ttu-id="1e258-136">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1e258-136">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

