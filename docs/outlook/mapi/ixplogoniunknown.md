---
title: IUnknown IXPLogon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon
api_type:
- COM
ms.assetid: 4d24ecaf-11d0-4362-8207-be3407736d7b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 46f4e3fc8f554f332ab9b1d8a6cb33e9e21dd9a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432537"
---
# <a name="ixplogon--iunknown"></a><span data-ttu-id="5c894-103">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5c894-103">IXPLogon : IUnknown</span></span>

  
  
<span data-ttu-id="5c894-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c894-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c894-105">Permite que el administrador de trabajos en cola MAPI tenga acceso a un proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="5c894-105">Gives the MAPI spooler access to a transport provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5c894-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="5c894-106">Header file:</span></span>  <br/> |<span data-ttu-id="5c894-107">Mapispi. h</span><span class="sxs-lookup"><span data-stu-id="5c894-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="5c894-108">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="5c894-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="5c894-109">Objetos de inicio de sesión de transporte</span><span class="sxs-lookup"><span data-stu-id="5c894-109">Transport logon objects</span></span>  <br/> |
|<span data-ttu-id="5c894-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="5c894-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="5c894-111">Proveedores de transporte</span><span class="sxs-lookup"><span data-stu-id="5c894-111">Transport providers</span></span>  <br/> |
|<span data-ttu-id="5c894-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="5c894-112">Called by:</span></span>  <br/> |<span data-ttu-id="5c894-113">La cola MAPI</span><span class="sxs-lookup"><span data-stu-id="5c894-113">The MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="5c894-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="5c894-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="5c894-115">IID_IXPLogon</span><span class="sxs-lookup"><span data-stu-id="5c894-115">IID_IXPLogon</span></span>  <br/> |
|<span data-ttu-id="5c894-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="5c894-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="5c894-117">LXPLOGON</span><span class="sxs-lookup"><span data-stu-id="5c894-117">LXPLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="5c894-118">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="5c894-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="5c894-119">AddressTypes</span><span class="sxs-lookup"><span data-stu-id="5c894-119">AddressTypes</span></span>](ixplogon-addresstypes.md) <br/> |<span data-ttu-id="5c894-120">Devuelve los tipos de destinatarios que controla el proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="5c894-120">Returns the types of recipients that the transport provider handles.</span></span>  <br/> |
|<span data-ttu-id="5c894-121">**RegisterOptions**</span><span class="sxs-lookup"><span data-stu-id="5c894-121">**RegisterOptions**</span></span> <br/> | <span data-ttu-id="5c894-122">*No es compatible o documentado.*</span><span class="sxs-lookup"><span data-stu-id="5c894-122">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="5c894-123">TransportNotify</span><span class="sxs-lookup"><span data-stu-id="5c894-123">TransportNotify</span></span>](ixplogon-transportnotify.md) <br/> |<span data-ttu-id="5c894-124">Indica la ocurrencia de un evento sobre el cual el proveedor de transporte solicitó la notificación.</span><span class="sxs-lookup"><span data-stu-id="5c894-124">Signals the occurrence of an event about which the transport provider requested notification.</span></span>  <br/> |
|[<span data-ttu-id="5c894-125">Usado</span><span class="sxs-lookup"><span data-stu-id="5c894-125">Idle</span></span>](ixplogon-idle.md) <br/> |<span data-ttu-id="5c894-126">Indica que el sistema está inactivo, lo que permite al proveedor de transporte realizar operaciones de baja prioridad.</span><span class="sxs-lookup"><span data-stu-id="5c894-126">Indicates that the system is idle, enabling the transport provider to perform low-priority operations.</span></span>  <br/> |
|[<span data-ttu-id="5c894-127">TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="5c894-127">TransportLogoff</span></span>](ixplogon-transportlogoff.md) <br/> |<span data-ttu-id="5c894-128">Inicia el proceso de cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="5c894-128">Initiates the logoff process.</span></span>  <br/> |
|[<span data-ttu-id="5c894-129">SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="5c894-129">SubmitMessage</span></span>](ixplogon-submitmessage.md) <br/> |<span data-ttu-id="5c894-130">Indica que la cola MAPI tiene un mensaje para que lo entregue el proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="5c894-130">Indicates that the MAPI spooler has a message for the transport provider to deliver.</span></span>  <br/> |
|[<span data-ttu-id="5c894-131">EndMessage</span><span class="sxs-lookup"><span data-stu-id="5c894-131">EndMessage</span></span>](ixplogon-endmessage.md) <br/> |<span data-ttu-id="5c894-132">Informa al proveedor de transporte que la cola MAPI completó el procesamiento en un mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="5c894-132">Informs the transport provider that the MAPI spooler completed its processing on an outbound message.</span></span>  <br/> |
|[<span data-ttu-id="5c894-133">Buscar</span><span class="sxs-lookup"><span data-stu-id="5c894-133">Poll</span></span>](ixplogon-poll.md) <br/> |<span data-ttu-id="5c894-134">Indica si el proveedor de transporte ha recibido uno o más mensajes de entrada.</span><span class="sxs-lookup"><span data-stu-id="5c894-134">Indicates whether the transport provider has received one or more inbound messages.</span></span>  <br/> |
|[<span data-ttu-id="5c894-135">StartMessage</span><span class="sxs-lookup"><span data-stu-id="5c894-135">StartMessage</span></span>](ixplogon-startmessage.md) <br/> |<span data-ttu-id="5c894-136">Inicia la transferencia de un mensaje entrante del proveedor de transporte a la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="5c894-136">Initiates the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span>  <br/> |
|[<span data-ttu-id="5c894-137">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="5c894-137">OpenStatusEntry</span></span>](ixplogon-openstatusentry.md) <br/> |<span data-ttu-id="5c894-138">Abre el objeto de estado del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="5c894-138">Opens the transport provider's status object.</span></span>  <br/> |
|[<span data-ttu-id="5c894-139">ValidateState</span><span class="sxs-lookup"><span data-stu-id="5c894-139">ValidateState</span></span>](ixplogon-validatestate.md) <br/> |<span data-ttu-id="5c894-140">Comprueba el estado externo del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="5c894-140">Checks the transport provider's external status.</span></span>  <br/> |
|[<span data-ttu-id="5c894-141">FlushQueues</span><span class="sxs-lookup"><span data-stu-id="5c894-141">FlushQueues</span></span>](ixplogon-flushqueues.md) <br/> |<span data-ttu-id="5c894-142">Solicita que el proveedor de transporte entregue inmediatamente todos los mensajes entrantes o salientes pendientes.</span><span class="sxs-lookup"><span data-stu-id="5c894-142">Requests that the transport provider immediately deliver all pending inbound or outbound messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5c894-143">Ver también</span><span class="sxs-lookup"><span data-stu-id="5c894-143">See also</span></span>



[<span data-ttu-id="5c894-144">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="5c894-144">MAPI Interfaces</span></span>](mapi-interfaces.md)

