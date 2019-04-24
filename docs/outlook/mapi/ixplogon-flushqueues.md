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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282834"
---
# <a name="ixplogonflushqueues"></a><span data-ttu-id="61aab-103">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="61aab-103">IXPLogon::FlushQueues</span></span>

  
  
<span data-ttu-id="61aab-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61aab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="61aab-105">Solicita que el proveedor de transporte entregue inmediatamente todos los mensajes entrantes o salientes pendientes.</span><span class="sxs-lookup"><span data-stu-id="61aab-105">Requests that the transport provider immediately deliver all pending inbound or outbound messages.</span></span>
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="61aab-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="61aab-106">Parameters</span></span>

 <span data-ttu-id="61aab-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="61aab-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="61aab-108">a Identificador de la ventana primaria de los cuadros de diálogo o ventanas que muestra este método.</span><span class="sxs-lookup"><span data-stu-id="61aab-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="61aab-109">_cbTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="61aab-109">_cbTargetTransport_</span></span>
  
> <span data-ttu-id="61aab-110">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="61aab-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="61aab-111">_lpTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="61aab-111">_lpTargetTransport_</span></span>
  
> <span data-ttu-id="61aab-112">a Reserve debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="61aab-112">[in] Reserved; must be NULL.</span></span>
    
 <span data-ttu-id="61aab-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="61aab-113">_ulFlags_</span></span>
  
> <span data-ttu-id="61aab-114">a Una máscara de máscara de marcadores que controla cómo se realiza el vaciado de la cola de mensajes.</span><span class="sxs-lookup"><span data-stu-id="61aab-114">[in] A bitmask of flags that controls how message queue flushing is accomplished.</span></span> <span data-ttu-id="61aab-115">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="61aab-115">The following flags can be set:</span></span>
    
<span data-ttu-id="61aab-116">FLUSH_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="61aab-116">FLUSH_DOWNLOAD</span></span> 
  
> <span data-ttu-id="61aab-117">Las colas de mensajes entrantes deben vaciarse.</span><span class="sxs-lookup"><span data-stu-id="61aab-117">The inbound message queue or queues should be flushed.</span></span>
    
<span data-ttu-id="61aab-118">FLUSH_FORCE</span><span class="sxs-lookup"><span data-stu-id="61aab-118">FLUSH_FORCE</span></span> 
  
> <span data-ttu-id="61aab-119">El proveedor de transporte debe procesar esta solicitud, si es posible, incluso si se trata de tiempo largo.</span><span class="sxs-lookup"><span data-stu-id="61aab-119">The transport provider should process this request, if possible, even if doing so is time consuming.</span></span> 
    
<span data-ttu-id="61aab-120">FLUSH_NO_UI</span><span class="sxs-lookup"><span data-stu-id="61aab-120">FLUSH_NO_UI</span></span> 
  
> <span data-ttu-id="61aab-121">El proveedor de transporte no debe mostrar una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="61aab-121">The transport provider should not display a user interface.</span></span>
    
<span data-ttu-id="61aab-122">FLUSH_UPLOAD</span><span class="sxs-lookup"><span data-stu-id="61aab-122">FLUSH_UPLOAD</span></span> 
  
> <span data-ttu-id="61aab-123">Se deben vaciar las colas de mensajes salientes.</span><span class="sxs-lookup"><span data-stu-id="61aab-123">The outbound message queue or queues should be flushed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="61aab-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="61aab-124">Return value</span></span>

<span data-ttu-id="61aab-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="61aab-125">S_OK</span></span> 
  
> <span data-ttu-id="61aab-126">La llamada se ha realizado correctamente y ha devuelto el valor o los valores esperados.</span><span class="sxs-lookup"><span data-stu-id="61aab-126">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="61aab-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="61aab-127">Remarks</span></span>

<span data-ttu-id="61aab-128">La cola MAPI llama al método **IXPLogon:: FlushQueues** para informar al proveedor de transporte que la cola MAPI va a empezar a procesar mensajes.</span><span class="sxs-lookup"><span data-stu-id="61aab-128">The MAPI spooler calls the **IXPLogon::FlushQueues** method to advise the transport provider that the MAPI spooler is about to begin processing messages.</span></span> <span data-ttu-id="61aab-129">El proveedor de transporte debería llamar al método [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) para establecer un bit adecuado para su estado en la propiedad **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de su fila de estado.</span><span class="sxs-lookup"><span data-stu-id="61aab-129">The transport provider should call the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method to set an appropriate bit for its state in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property of its status row.</span></span> <span data-ttu-id="61aab-130">Después de actualizar la fila de estado, el proveedor de transporte debe devolver S_OK para la llamada **FlushQueues** .</span><span class="sxs-lookup"><span data-stu-id="61aab-130">After updating its status row, the transport provider should return S_OK for the **FlushQueues** call.</span></span> <span data-ttu-id="61aab-131">A continuación, la cola MAPI comienza a enviar mensajes, con la operación sincrónica a la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="61aab-131">The MAPI spooler then starts sending messages, with the operation being synchronous to the MAPI spooler.</span></span> 
  
<span data-ttu-id="61aab-132">Para admitir su implementación del método [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md) , la cola MAPI llama a **IXPLogon:: FlushQueues** para todos los objetos de inicio de sesión de los proveedores de transporte activos que se ejecutan en una sesión de perfil.</span><span class="sxs-lookup"><span data-stu-id="61aab-132">To support its implementation of the [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method, the MAPI spooler calls **IXPLogon::FlushQueues** for all logon objects for active transport providers that are running in a profile session.</span></span> <span data-ttu-id="61aab-133">Cuando se llama a un método **FlushQueues** de un proveedor de transporte como resultado de una llamada de aplicación cliente a **IMAPIStatus:: FlushQueues**, el procesamiento de mensajes se produce de forma asincrónica en el cliente.</span><span class="sxs-lookup"><span data-stu-id="61aab-133">When a transport provider's **FlushQueues** method is called as a result of a client application call to **IMAPIStatus::FlushQueues**, the message processing occurs asynchronously to the client.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="61aab-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="61aab-134">See also</span></span>



[<span data-ttu-id="61aab-135">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="61aab-135">IMAPIStatus::FlushQueues</span></span>](imapistatus-flushqueues.md)
  
[<span data-ttu-id="61aab-136">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="61aab-136">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

