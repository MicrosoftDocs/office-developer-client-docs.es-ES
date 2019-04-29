---
title: IMAPIStatusFlushQueues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.FlushQueues
api_type:
- COM
ms.assetid: d6b01a91-b452-4b2c-9802-698e7b0f4169
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5f8396ca84192e485d33fb5a96f641361b717584
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432607"
---
# <a name="imapistatusflushqueues"></a><span data-ttu-id="8d163-103">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="8d163-103">IMAPIStatus::FlushQueues</span></span>

  
  
<span data-ttu-id="8d163-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d163-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d163-105">Obliga a que se carguen o descarguen inmediatamente todos los mensajes que esperan ser enviados o recibidos.</span><span class="sxs-lookup"><span data-stu-id="8d163-105">Forces all messages waiting to be sent or received to be immediately uploaded or downloaded.</span></span> <span data-ttu-id="8d163-106">El objeto de estado de cola MAPI y los objetos de estado que implementan los proveedores de transporte admiten este método.</span><span class="sxs-lookup"><span data-stu-id="8d163-106">The MAPI spooler status object and status objects that transport providers implement support this method.</span></span>
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="8d163-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="8d163-107">Parameters</span></span>

 <span data-ttu-id="8d163-108">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="8d163-108">_ulUIParam_</span></span>
  
> <span data-ttu-id="8d163-109">a Identificador de la ventana primaria de los cuadros de diálogo o ventanas que muestra este método.</span><span class="sxs-lookup"><span data-stu-id="8d163-109">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="8d163-110">_cbTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="8d163-110">_cbTargetTransport_</span></span>
  
> <span data-ttu-id="8d163-111">a El recuento de bytes en el identificador de entrada al que apunta el parámetro _lpTargetTransport_ .</span><span class="sxs-lookup"><span data-stu-id="8d163-111">[in] The byte count in the entry identifier pointed to by the  _lpTargetTransport_ parameter.</span></span> <span data-ttu-id="8d163-112">El parámetro _cbTargetTransport_ se establece únicamente en llamadas al objeto status del administrador de trabajos de MAPI.</span><span class="sxs-lookup"><span data-stu-id="8d163-112">The  _cbTargetTransport_ parameter is set only on calls to the MAPI spooler's status object.</span></span> <span data-ttu-id="8d163-113">Para las llamadas a un proveedor de transporte, el parámetro _cbTargetTransport_ se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="8d163-113">For calls to a transport provider, the  _cbTargetTransport_ parameter is set to 0.</span></span> 
    
 <span data-ttu-id="8d163-114">_lpTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="8d163-114">_lpTargetTransport_</span></span>
  
> <span data-ttu-id="8d163-115">a Un puntero al identificador de entrada del proveedor de transporte que va a vaciar sus colas de mensajes.</span><span class="sxs-lookup"><span data-stu-id="8d163-115">[in] A pointer to the entry identifier of the transport provider that is to flush its message queues.</span></span> <span data-ttu-id="8d163-116">El parámetro _lpTargetTransport_ se establece únicamente en llamadas al objeto status del administrador de trabajos de MAPI.</span><span class="sxs-lookup"><span data-stu-id="8d163-116">The  _lpTargetTransport_ parameter is set only on calls to the MAPI spooler's status object.</span></span> <span data-ttu-id="8d163-117">Para las llamadas a un proveedor de transporte, el parámetro _lpTargetTransport_ se establece en NULL.</span><span class="sxs-lookup"><span data-stu-id="8d163-117">For calls to a transport provider, the  _lpTargetTransport_ parameter is set to NULL.</span></span> 
    
 <span data-ttu-id="8d163-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8d163-118">_ulFlags_</span></span>
  
> <span data-ttu-id="8d163-119">a Una máscara de máscara de marcadores que controla la operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="8d163-119">[in] A bitmask of flags that controls the flush operation.</span></span> <span data-ttu-id="8d163-120">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="8d163-120">The following flags can be set:</span></span>
    
<span data-ttu-id="8d163-121">FLUSH_ASYNC_OK</span><span class="sxs-lookup"><span data-stu-id="8d163-121">FLUSH_ASYNC_OK</span></span> 
  
> <span data-ttu-id="8d163-122">La operación de vaciado puede realizarse de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="8d163-122">The flush operation can occur asynchronously.</span></span> <span data-ttu-id="8d163-123">Esta marca solo se aplica al objeto de estado del administrador de trabajos en cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="8d163-123">This flag applies only to the MAPI spooler's status object.</span></span> 
    
<span data-ttu-id="8d163-124">FLUSH_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="8d163-124">FLUSH_DOWNLOAD</span></span> 
  
> <span data-ttu-id="8d163-125">Se deben vaciar las colas de mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="8d163-125">The incoming message queues should be flushed.</span></span>
    
<span data-ttu-id="8d163-126">FLUSH_FORCE</span><span class="sxs-lookup"><span data-stu-id="8d163-126">FLUSH_FORCE</span></span> 
  
> <span data-ttu-id="8d163-127">La operación de vaciado debe producirse, a pesar de la posibilidad de una disminución en el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="8d163-127">The flush operation should occur regardless, in spite of the chance of a decrease in performance.</span></span> <span data-ttu-id="8d163-128">Esta marca se debe establecer cuando se destina un proveedor de transporte asincrónico.</span><span class="sxs-lookup"><span data-stu-id="8d163-128">This flag must be set when an asynchronous transport provider is targeted.</span></span>
    
<span data-ttu-id="8d163-129">FLUSH_NO_UI</span><span class="sxs-lookup"><span data-stu-id="8d163-129">FLUSH_NO_UI</span></span> 
  
> <span data-ttu-id="8d163-130">El objeto status no debe mostrar un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="8d163-130">The status object should not display a progress indicator.</span></span>
    
<span data-ttu-id="8d163-131">FLUSH_UPLOAD</span><span class="sxs-lookup"><span data-stu-id="8d163-131">FLUSH_UPLOAD</span></span> 
  
> <span data-ttu-id="8d163-132">Se deben vaciar las colas de mensajes salientes.</span><span class="sxs-lookup"><span data-stu-id="8d163-132">The outgoing message queues should be flushed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8d163-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8d163-133">Return value</span></span>

<span data-ttu-id="8d163-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="8d163-134">S_OK</span></span> 
  
> <span data-ttu-id="8d163-135">La operación de vaciado se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="8d163-135">The flush operation was successful.</span></span>
    
<span data-ttu-id="8d163-136">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="8d163-136">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="8d163-137">Hay otra operación en curso; se debe permitir que se complete o debe detenerse antes de que se pueda iniciar esta operación.</span><span class="sxs-lookup"><span data-stu-id="8d163-137">Another operation is in progress; it should be allowed to complete, or it should be stopped, before this operation can be initiated.</span></span>
    
<span data-ttu-id="8d163-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="8d163-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="8d163-139">El objeto status no admite esta operación, como indica la ausencia de la marca STATUS_FLUSH_QUEUES en la propiedad **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) del objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="8d163-139">The status object does not support this operation, as indicated by the absence of the STATUS_FLUSH_QUEUES flag in the status object's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8d163-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8d163-140">Remarks</span></span>

<span data-ttu-id="8d163-141">El método **IMAPIStatus:: FlushQueues** solicita que la cola MAPI o un proveedor de transporte envíen inmediatamente todos los mensajes en la cola de salida o reciban todos los mensajes de la cola entrante.</span><span class="sxs-lookup"><span data-stu-id="8d163-141">The **IMAPIStatus::FlushQueues** method requests that the MAPI spooler or a transport provider immediately send all messages in the outgoing queue or receive all messages from the incoming queue.</span></span> <span data-ttu-id="8d163-142">**FlushQueues** se implementa solo mediante el objeto de estado de cola de MAPI y los objetos de estado que suministran los proveedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="8d163-142">**FlushQueues** is implemented only by the MAPI spooler status object and by status objects that transport providers supply.</span></span> 
  
<span data-ttu-id="8d163-143">MAPI_E_BUSY debe devolverse para las solicitudes asincrónicas, de modo que los clientes puedan continuar su trabajo.</span><span class="sxs-lookup"><span data-stu-id="8d163-143">MAPI_E_BUSY should be returned for asynchronous requests so that clients can continue work.</span></span> 
  
<span data-ttu-id="8d163-144">De forma predeterminada, **FlushQueues** es una operación sincrónica; el control no vuelve al autor de la llamada hasta que el vaciado se ha completado.</span><span class="sxs-lookup"><span data-stu-id="8d163-144">By default, **FlushQueues** is a synchronous operation; control does not return to the caller until the flush has completed.</span></span> <span data-ttu-id="8d163-145">Solo la operación de vaciado que realiza la cola MAPI puede ser asincrónica; los clientes solicitan este comportamiento estableciendo la marca FLUSH_ASYNC_OK.</span><span class="sxs-lookup"><span data-stu-id="8d163-145">Only the flush operation performed by the MAPI spooler can be asynchronous; clients request this behavior by setting the FLUSH_ASYNC_OK flag.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8d163-146">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="8d163-146">Notes to implementers</span></span>

<span data-ttu-id="8d163-147">La implementación de **FlushQueues** establece bits en la propiedad **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de la fila de estado del objeto de inicio de sesión para controlar cómo se vacían las colas.</span><span class="sxs-lookup"><span data-stu-id="8d163-147">A remote transport provider's implementation of **FlushQueues** sets bits in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property in the logon object's status row to control how queues are flushed.</span></span> <span data-ttu-id="8d163-148">Si un visor remoto pasa la marca FLUSH_UPLOAD, el método **FlushQueues** debe establecer los bits STATUS_INBOUND_ENABLED y STATUS_INBOUND_ACTIVE.</span><span class="sxs-lookup"><span data-stu-id="8d163-148">If a remote viewer passes in the FLUSH_UPLOAD flag, the **FlushQueues** method should set the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits.</span></span> <span data-ttu-id="8d163-149">Si un visor remoto pasa la marca FLUSH_DOWNLOAD, el método **FlushQueues** debe establecer los bits STATUS_OUTBOUND_ENABLED y STATUS_OUTBOUND_ACTIVE.</span><span class="sxs-lookup"><span data-stu-id="8d163-149">If a remote viewer passes in the FLUSH_DOWNLOAD flag, the **FlushQueues** method should set the STATUS_OUTBOUND_ENABLED and STATUS_OUTBOUND_ACTIVE bits.</span></span> <span data-ttu-id="8d163-150">**FlushQueues** debe devolver S_OK.</span><span class="sxs-lookup"><span data-stu-id="8d163-150">**FlushQueues** should then return S_OK.</span></span> <span data-ttu-id="8d163-151">A continuación, la cola de MAPI iniciará las acciones adecuadas para cargar y descargar mensajes.</span><span class="sxs-lookup"><span data-stu-id="8d163-151">The MAPI spooler will then initiate the appropriate actions to upload and download messages.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8d163-152">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="8d163-152">Notes to callers</span></span>

<span data-ttu-id="8d163-153">Una llamada al objeto de estado de cola MAPI es una directiva para transferir todos los mensajes hacia o desde el proveedor de transporte correspondiente.</span><span class="sxs-lookup"><span data-stu-id="8d163-153">A call to the MAPI spooler status object is a directive to transfer all messages either to or from the appropriate transport provider.</span></span> <span data-ttu-id="8d163-154">Cuando se llama a un objeto de estado de un proveedor de transporte individual, solo se ven afectados los mensajes de ese proveedor.</span><span class="sxs-lookup"><span data-stu-id="8d163-154">When you call an individual transport provider's status object, only the messages for that provider are affected.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8d163-155">Ver también</span><span class="sxs-lookup"><span data-stu-id="8d163-155">See also</span></span>



[<span data-ttu-id="8d163-156">Propiedad canónica PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="8d163-156">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="8d163-157">Propiedad canónica PidTagStatusCode</span><span class="sxs-lookup"><span data-stu-id="8d163-157">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)
  
[<span data-ttu-id="8d163-158">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8d163-158">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

