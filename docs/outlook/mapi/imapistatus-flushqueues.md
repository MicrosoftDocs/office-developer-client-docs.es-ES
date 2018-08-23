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
ms.openlocfilehash: 30aaaaa250155215149a941da7f7e528d65b8dc3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592202"
---
# <a name="imapistatusflushqueues"></a><span data-ttu-id="1d7ed-103">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="1d7ed-103">IMAPIStatus::FlushQueues</span></span>

  
  
<span data-ttu-id="1d7ed-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d7ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1d7ed-105">Obliga a todos los mensajes en espera de ser enviados o recibidos para cargarse o descargarse inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="1d7ed-105">Forces all messages waiting to be sent or received to be immediately uploaded or downloaded.</span></span> <span data-ttu-id="1d7ed-106">El objeto de estado de cola de impresión MAPI y objetos de estado que implementan los proveedores de transporte admiten este método.</span><span class="sxs-lookup"><span data-stu-id="1d7ed-106">The MAPI spooler status object and status objects that transport providers implement support this method.</span></span>
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="1d7ed-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1d7ed-107">Parameters</span></span>

 <span data-ttu-id="1d7ed-108">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="1d7ed-108">_ulUIParam_</span></span>
  
> <span data-ttu-id="1d7ed-109">[entrada] Identificador de la ventana principal de los cuadros de diálogo o windows que muestra este método.</span><span class="sxs-lookup"><span data-stu-id="1d7ed-109">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="1d7ed-110">_cbTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="1d7ed-110">_cbTargetTransport_</span></span>
  
> <span data-ttu-id="1d7ed-111">[entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpTargetTransport_ .</span><span class="sxs-lookup"><span data-stu-id="1d7ed-111">[in] The byte count in the entry identifier pointed to by the  _lpTargetTransport_ parameter.</span></span> <span data-ttu-id="1d7ed-112">El parámetro _cbTargetTransport_ se establece únicamente en las llamadas al objeto de estado de la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="1d7ed-112">The  _cbTargetTransport_ parameter is set only on calls to the MAPI spooler's status object.</span></span> <span data-ttu-id="1d7ed-113">Para las llamadas a un proveedor de transporte, el parámetro _cbTargetTransport_ se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="1d7ed-113">For calls to a transport provider, the  _cbTargetTransport_ parameter is set to 0.</span></span> 
    
 <span data-ttu-id="1d7ed-114">_lpTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="1d7ed-114">_lpTargetTransport_</span></span>
  
> <span data-ttu-id="1d7ed-115">[entrada] Un puntero al identificador del proveedor de transporte que se a vaciar las colas de mensajes de entrada.</span><span class="sxs-lookup"><span data-stu-id="1d7ed-115">[in] A pointer to the entry identifier of the transport provider that is to flush its message queues.</span></span> <span data-ttu-id="1d7ed-116">El parámetro _lpTargetTransport_ se establece únicamente en las llamadas al objeto de estado de la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="1d7ed-116">The  _lpTargetTransport_ parameter is set only on calls to the MAPI spooler's status object.</span></span> <span data-ttu-id="1d7ed-117">Para las llamadas a un proveedor de transporte, el parámetro _lpTargetTransport_ se establece en NULL.</span><span class="sxs-lookup"><span data-stu-id="1d7ed-117">For calls to a transport provider, the  _lpTargetTransport_ parameter is set to NULL.</span></span> 
    
 <span data-ttu-id="1d7ed-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1d7ed-118">_ulFlags_</span></span>
  
> <span data-ttu-id="1d7ed-119">[entrada] Una máscara de bits de indicadores que controla la operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="1d7ed-119">[in] A bitmask of flags that controls the flush operation.</span></span> <span data-ttu-id="1d7ed-120">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="1d7ed-120">The following flags can be set:</span></span>
    
<span data-ttu-id="1d7ed-121">FLUSH_ASYNC_OK</span><span class="sxs-lookup"><span data-stu-id="1d7ed-121">FLUSH_ASYNC_OK</span></span> 
  
> <span data-ttu-id="1d7ed-122">La operación de vaciado puede producirse de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="1d7ed-122">The flush operation can occur asynchronously.</span></span> <span data-ttu-id="1d7ed-123">Esta marca sólo se aplica a objetos de estado de la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="1d7ed-123">This flag applies only to the MAPI spooler's status object.</span></span> 
    
<span data-ttu-id="1d7ed-124">FLUSH_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="1d7ed-124">FLUSH_DOWNLOAD</span></span> 
  
> <span data-ttu-id="1d7ed-125">Se deben vaciar las colas de mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="1d7ed-125">The incoming message queues should be flushed.</span></span>
    
<span data-ttu-id="1d7ed-126">FLUSH_FORCE</span><span class="sxs-lookup"><span data-stu-id="1d7ed-126">FLUSH_FORCE</span></span> 
  
> <span data-ttu-id="1d7ed-127">La operación de vaciado debe producirse independientemente de la forma, a pesar de las posibilidades de una disminución del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="1d7ed-127">The flush operation should occur regardless, in spite of the chance of a decrease in performance.</span></span> <span data-ttu-id="1d7ed-128">Este indicador se debe establecer cuando el destino es de un proveedor de transporte asincrónico.</span><span class="sxs-lookup"><span data-stu-id="1d7ed-128">This flag must be set when an asynchronous transport provider is targeted.</span></span>
    
<span data-ttu-id="1d7ed-129">FLUSH_NO_UI</span><span class="sxs-lookup"><span data-stu-id="1d7ed-129">FLUSH_NO_UI</span></span> 
  
> <span data-ttu-id="1d7ed-130">El objeto de estado no debe mostrar un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="1d7ed-130">The status object should not display a progress indicator.</span></span>
    
<span data-ttu-id="1d7ed-131">FLUSH_UPLOAD</span><span class="sxs-lookup"><span data-stu-id="1d7ed-131">FLUSH_UPLOAD</span></span> 
  
> <span data-ttu-id="1d7ed-132">Se deben vaciar las colas de mensajes salientes.</span><span class="sxs-lookup"><span data-stu-id="1d7ed-132">The outgoing message queues should be flushed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1d7ed-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1d7ed-133">Return value</span></span>

<span data-ttu-id="1d7ed-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="1d7ed-134">S_OK</span></span> 
  
> <span data-ttu-id="1d7ed-135">La operación de vaciado fue correcta.</span><span class="sxs-lookup"><span data-stu-id="1d7ed-135">The flush operation was successful.</span></span>
    
<span data-ttu-id="1d7ed-136">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="1d7ed-136">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="1d7ed-137">Otra operación está en curso; se debe permitir para llevar a cabo o se debe detener, antes de que se puede iniciar esta operación.</span><span class="sxs-lookup"><span data-stu-id="1d7ed-137">Another operation is in progress; it should be allowed to complete, or it should be stopped, before this operation can be initiated.</span></span>
    
<span data-ttu-id="1d7ed-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="1d7ed-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="1d7ed-139">El objeto de estado no es compatible con esta operación, tal como se indica por la ausencia de la marca STATUS_FLUSH_QUEUES en propiedad de **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) del objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="1d7ed-139">The status object does not support this operation, as indicated by the absence of the STATUS_FLUSH_QUEUES flag in the status object's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1d7ed-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1d7ed-140">Remarks</span></span>

<span data-ttu-id="1d7ed-141">El método **IMAPIStatus::FlushQueues** solicita que la cola MAPI o un proveedor de transporte inmediatamente enviar todos los mensajes en la cola de salida o recibir todos los mensajes de la cola entrante.</span><span class="sxs-lookup"><span data-stu-id="1d7ed-141">The **IMAPIStatus::FlushQueues** method requests that the MAPI spooler or a transport provider immediately send all messages in the outgoing queue or receive all messages from the incoming queue.</span></span> <span data-ttu-id="1d7ed-142">**FlushQueues** se implementa solo por el objeto de estado de cola de impresión MAPI y objetos de estado que suministro de proveedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="1d7ed-142">**FlushQueues** is implemented only by the MAPI spooler status object and by status objects that transport providers supply.</span></span> 
  
<span data-ttu-id="1d7ed-143">MAPI_E_BUSY se deben devolver para las solicitudes asincrónicas para que los clientes pueden continuar trabajo.</span><span class="sxs-lookup"><span data-stu-id="1d7ed-143">MAPI_E_BUSY should be returned for asynchronous requests so that clients can continue work.</span></span> 
  
<span data-ttu-id="1d7ed-144">De forma predeterminada, **FlushQueues** es una operación sincrónica; control no vuelve al autor de la llamada hasta que haya finalizado el vaciado.</span><span class="sxs-lookup"><span data-stu-id="1d7ed-144">By default, **FlushQueues** is a synchronous operation; control does not return to the caller until the flush has completed.</span></span> <span data-ttu-id="1d7ed-145">Sólo la operación de vaciado realizada por la cola MAPI puede ser asincrónica; los clientes solicitan este comportamiento estableciendo el indicador FLUSH_ASYNC_OK.</span><span class="sxs-lookup"><span data-stu-id="1d7ed-145">Only the flush operation performed by the MAPI spooler can be asynchronous; clients request this behavior by setting the FLUSH_ASYNC_OK flag.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1d7ed-146">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="1d7ed-146">Notes to implementers</span></span>

<span data-ttu-id="1d7ed-147">Implementación del proveedor de transporte remoto de **FlushQueues** establece bits en la propiedad **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) en la fila de estado del objeto de inicio de sesión para controlar cómo se vacían colas.</span><span class="sxs-lookup"><span data-stu-id="1d7ed-147">A remote transport provider's implementation of **FlushQueues** sets bits in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property in the logon object's status row to control how queues are flushed.</span></span> <span data-ttu-id="1d7ed-148">Si un visor remoto pasa el indicador FLUSH_UPLOAD, el método **FlushQueues** debe establecer los bits STATUS_INBOUND_ENABLED y STATUS_INBOUND_ACTIVE.</span><span class="sxs-lookup"><span data-stu-id="1d7ed-148">If a remote viewer passes in the FLUSH_UPLOAD flag, the **FlushQueues** method should set the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits.</span></span> <span data-ttu-id="1d7ed-149">Si un visor remoto pasa el indicador FLUSH_DOWNLOAD, el método **FlushQueues** debe establecer los bits STATUS_OUTBOUND_ENABLED y STATUS_OUTBOUND_ACTIVE.</span><span class="sxs-lookup"><span data-stu-id="1d7ed-149">If a remote viewer passes in the FLUSH_DOWNLOAD flag, the **FlushQueues** method should set the STATUS_OUTBOUND_ENABLED and STATUS_OUTBOUND_ACTIVE bits.</span></span> <span data-ttu-id="1d7ed-150">**FlushQueues** , a continuación, se debe devolver S_OK.</span><span class="sxs-lookup"><span data-stu-id="1d7ed-150">**FlushQueues** should then return S_OK.</span></span> <span data-ttu-id="1d7ed-151">La cola MAPI, a continuación, iniciará las acciones adecuadas para cargar y descargar los mensajes.</span><span class="sxs-lookup"><span data-stu-id="1d7ed-151">The MAPI spooler will then initiate the appropriate actions to upload and download messages.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1d7ed-152">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="1d7ed-152">Notes to callers</span></span>

<span data-ttu-id="1d7ed-153">Una llamada al objeto de estado de cola de impresión MAPI es una directiva para transferir todos los mensajes a o desde el proveedor de transporte apropiado.</span><span class="sxs-lookup"><span data-stu-id="1d7ed-153">A call to the MAPI spooler status object is a directive to transfer all messages either to or from the appropriate transport provider.</span></span> <span data-ttu-id="1d7ed-154">Cuando se llama el objeto de estado de un proveedor de transporte individual, sólo los mensajes de ese proveedor se ven afectados.</span><span class="sxs-lookup"><span data-stu-id="1d7ed-154">When you call an individual transport provider's status object, only the messages for that provider are affected.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1d7ed-155">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="1d7ed-155">See also</span></span>



[<span data-ttu-id="1d7ed-156">Propiedad canónica PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="1d7ed-156">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="1d7ed-157">Propiedad canónica PidTagStatusCode</span><span class="sxs-lookup"><span data-stu-id="1d7ed-157">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)
  
[<span data-ttu-id="1d7ed-158">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1d7ed-158">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

