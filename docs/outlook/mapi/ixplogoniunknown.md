---
title: IXPLogon IUnknown
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
ms.openlocfilehash: ecfbf33641c86d4f162c521466ca2bf0b79a61d5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581408"
---
# <a name="ixplogon--iunknown"></a><span data-ttu-id="86227-103">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="86227-103">IXPLogon : IUnknown</span></span>

  
  
<span data-ttu-id="86227-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86227-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86227-105">Proporciona el acceso a la cola de impresión MAPI a un proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="86227-105">Gives the MAPI spooler access to a transport provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="86227-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="86227-106">Header file:</span></span>  <br/> |<span data-ttu-id="86227-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="86227-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="86227-108">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="86227-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="86227-109">Objetos de inicio de sesión de transporte</span><span class="sxs-lookup"><span data-stu-id="86227-109">Transport logon objects</span></span>  <br/> |
|<span data-ttu-id="86227-110">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="86227-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="86227-111">Proveedores de transporte</span><span class="sxs-lookup"><span data-stu-id="86227-111">Transport providers</span></span>  <br/> |
|<span data-ttu-id="86227-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="86227-112">Called by:</span></span>  <br/> |<span data-ttu-id="86227-113">La cola MAPI</span><span class="sxs-lookup"><span data-stu-id="86227-113">The MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="86227-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="86227-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="86227-115">IID_IXPLogon</span><span class="sxs-lookup"><span data-stu-id="86227-115">IID_IXPLogon</span></span>  <br/> |
|<span data-ttu-id="86227-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="86227-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="86227-117">LXPLOGON</span><span class="sxs-lookup"><span data-stu-id="86227-117">LXPLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="86227-118">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="86227-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="86227-119">AddressTypes</span><span class="sxs-lookup"><span data-stu-id="86227-119">AddressTypes</span></span>](ixplogon-addresstypes.md) <br/> |<span data-ttu-id="86227-120">Devuelve los tipos de destinatarios que administra el proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="86227-120">Returns the types of recipients that the transport provider handles.</span></span>  <br/> |
|<span data-ttu-id="86227-121">**RegisterOptions**</span><span class="sxs-lookup"><span data-stu-id="86227-121">**RegisterOptions**</span></span> <br/> | <span data-ttu-id="86227-122">*No se admiten o documentado.*</span><span class="sxs-lookup"><span data-stu-id="86227-122">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="86227-123">TransportNotify</span><span class="sxs-lookup"><span data-stu-id="86227-123">TransportNotify</span></span>](ixplogon-transportnotify.md) <br/> |<span data-ttu-id="86227-124">Indica la aparición de un evento sobre el que el proveedor de transporte solicita la notificación.</span><span class="sxs-lookup"><span data-stu-id="86227-124">Signals the occurrence of an event about which the transport provider requested notification.</span></span>  <br/> |
|[<span data-ttu-id="86227-125">Inactividad</span><span class="sxs-lookup"><span data-stu-id="86227-125">Idle</span></span>](ixplogon-idle.md) <br/> |<span data-ttu-id="86227-126">Indica que el sistema está inactivo, habilitar el proveedor de transporte realizar operaciones de prioridad baja.</span><span class="sxs-lookup"><span data-stu-id="86227-126">Indicates that the system is idle, enabling the transport provider to perform low-priority operations.</span></span>  <br/> |
|[<span data-ttu-id="86227-127">TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="86227-127">TransportLogoff</span></span>](ixplogon-transportlogoff.md) <br/> |<span data-ttu-id="86227-128">Inicia el proceso de cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="86227-128">Initiates the logoff process.</span></span>  <br/> |
|[<span data-ttu-id="86227-129">SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="86227-129">SubmitMessage</span></span>](ixplogon-submitmessage.md) <br/> |<span data-ttu-id="86227-130">Indica que la cola MAPI tiene un mensaje para el proveedor de transporte entregar.</span><span class="sxs-lookup"><span data-stu-id="86227-130">Indicates that the MAPI spooler has a message for the transport provider to deliver.</span></span>  <br/> |
|[<span data-ttu-id="86227-131">EndMessage</span><span class="sxs-lookup"><span data-stu-id="86227-131">EndMessage</span></span>](ixplogon-endmessage.md) <br/> |<span data-ttu-id="86227-132">Informa al proveedor de transporte que la cola MAPI completó su procesamiento en un mensaje de salida.</span><span class="sxs-lookup"><span data-stu-id="86227-132">Informs the transport provider that the MAPI spooler completed its processing on an outbound message.</span></span>  <br/> |
|[<span data-ttu-id="86227-133">Sondeo</span><span class="sxs-lookup"><span data-stu-id="86227-133">Poll</span></span>](ixplogon-poll.md) <br/> |<span data-ttu-id="86227-134">Indica si el proveedor de transporte ha recibido uno o más mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="86227-134">Indicates whether the transport provider has received one or more inbound messages.</span></span>  <br/> |
|[<span data-ttu-id="86227-135">Desea iniciar</span><span class="sxs-lookup"><span data-stu-id="86227-135">StartMessage</span></span>](ixplogon-startmessage.md) <br/> |<span data-ttu-id="86227-136">Inicia a la transferencia de un mensaje entrante desde el proveedor de transporte a la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="86227-136">Initiates the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span>  <br/> |
|[<span data-ttu-id="86227-137">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="86227-137">OpenStatusEntry</span></span>](ixplogon-openstatusentry.md) <br/> |<span data-ttu-id="86227-138">Se abre el objeto de estado del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="86227-138">Opens the transport provider's status object.</span></span>  <br/> |
|[<span data-ttu-id="86227-139">ValidateState</span><span class="sxs-lookup"><span data-stu-id="86227-139">ValidateState</span></span>](ixplogon-validatestate.md) <br/> |<span data-ttu-id="86227-140">Comprobaciones de estado externo del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="86227-140">Checks the transport provider's external status.</span></span>  <br/> |
|[<span data-ttu-id="86227-141">FlushQueues</span><span class="sxs-lookup"><span data-stu-id="86227-141">FlushQueues</span></span>](ixplogon-flushqueues.md) <br/> |<span data-ttu-id="86227-142">Solicitudes que el proveedor de transporte entrega inmediatamente todos los mensajes entrantes o salientes pendientes.</span><span class="sxs-lookup"><span data-stu-id="86227-142">Requests that the transport provider immediately deliver all pending inbound or outbound messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="86227-143">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="86227-143">See also</span></span>



[<span data-ttu-id="86227-144">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="86227-144">MAPI Interfaces</span></span>](mapi-interfaces.md)

