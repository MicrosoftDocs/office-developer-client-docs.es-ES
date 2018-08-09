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
ms.openlocfilehash: 0b16fba054533f1cb5d21f3f4b1788c073eca13b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818028"
---
# <a name="ixplogon--iunknown"></a><span data-ttu-id="1e02c-103">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1e02c-103">IXPLogon : IUnknown</span></span>

  
  
<span data-ttu-id="1e02c-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1e02c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1e02c-105">Proporciona el acceso a la cola de impresión MAPI a un proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="1e02c-105">Gives the MAPI spooler access to a transport provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1e02c-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="1e02c-106">Header file:</span></span>  <br/> |<span data-ttu-id="1e02c-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="1e02c-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="1e02c-108">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="1e02c-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="1e02c-109">Objetos de inicio de sesión de transporte</span><span class="sxs-lookup"><span data-stu-id="1e02c-109">Transport logon objects</span></span>  <br/> |
|<span data-ttu-id="1e02c-110">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="1e02c-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="1e02c-111">Proveedores de transporte</span><span class="sxs-lookup"><span data-stu-id="1e02c-111">Transport providers</span></span>  <br/> |
|<span data-ttu-id="1e02c-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="1e02c-112">Called by:</span></span>  <br/> |<span data-ttu-id="1e02c-113">La cola MAPI</span><span class="sxs-lookup"><span data-stu-id="1e02c-113">The MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="1e02c-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="1e02c-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="1e02c-115">IID_IXPLogon</span><span class="sxs-lookup"><span data-stu-id="1e02c-115">IID_IXPLogon</span></span>  <br/> |
|<span data-ttu-id="1e02c-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="1e02c-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="1e02c-117">LXPLOGON</span><span class="sxs-lookup"><span data-stu-id="1e02c-117">LXPLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="1e02c-118">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="1e02c-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="1e02c-119">AddressTypes</span><span class="sxs-lookup"><span data-stu-id="1e02c-119">AddressTypes</span></span>](ixplogon-addresstypes.md) <br/> |<span data-ttu-id="1e02c-120">Devuelve los tipos de destinatarios que administra el proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="1e02c-120">Returns the types of recipients that the transport provider handles.</span></span>  <br/> |
|<span data-ttu-id="1e02c-121">**RegisterOptions**</span><span class="sxs-lookup"><span data-stu-id="1e02c-121">**RegisterOptions**</span></span> <br/> | <span data-ttu-id="1e02c-122">*No se admiten o documentado.*</span><span class="sxs-lookup"><span data-stu-id="1e02c-122">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="1e02c-123">TransportNotify</span><span class="sxs-lookup"><span data-stu-id="1e02c-123">TransportNotify</span></span>](ixplogon-transportnotify.md) <br/> |<span data-ttu-id="1e02c-124">Indica la aparición de un evento sobre el que el proveedor de transporte solicita la notificación.</span><span class="sxs-lookup"><span data-stu-id="1e02c-124">Signals the occurrence of an event about which the transport provider requested notification.</span></span>  <br/> |
|[<span data-ttu-id="1e02c-125">Inactividad</span><span class="sxs-lookup"><span data-stu-id="1e02c-125">Idle</span></span>](ixplogon-idle.md) <br/> |<span data-ttu-id="1e02c-126">Indica que el sistema está inactivo, habilitar el proveedor de transporte realizar operaciones de prioridad baja.</span><span class="sxs-lookup"><span data-stu-id="1e02c-126">Indicates that the system is idle, enabling the transport provider to perform low-priority operations.</span></span>  <br/> |
|[<span data-ttu-id="1e02c-127">TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="1e02c-127">TransportLogoff</span></span>](ixplogon-transportlogoff.md) <br/> |<span data-ttu-id="1e02c-128">Inicia el proceso de cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="1e02c-128">Initiates the logoff process.</span></span>  <br/> |
|[<span data-ttu-id="1e02c-129">SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="1e02c-129">SubmitMessage</span></span>](ixplogon-submitmessage.md) <br/> |<span data-ttu-id="1e02c-130">Indica que la cola MAPI tiene un mensaje para el proveedor de transporte entregar.</span><span class="sxs-lookup"><span data-stu-id="1e02c-130">Indicates that the MAPI spooler has a message for the transport provider to deliver.</span></span>  <br/> |
|[<span data-ttu-id="1e02c-131">EndMessage</span><span class="sxs-lookup"><span data-stu-id="1e02c-131">EndMessage</span></span>](ixplogon-endmessage.md) <br/> |<span data-ttu-id="1e02c-132">Informa al proveedor de transporte que la cola MAPI completó su procesamiento en un mensaje de salida.</span><span class="sxs-lookup"><span data-stu-id="1e02c-132">Informs the transport provider that the MAPI spooler completed its processing on an outbound message.</span></span>  <br/> |
|[<span data-ttu-id="1e02c-133">Sondeo</span><span class="sxs-lookup"><span data-stu-id="1e02c-133">Poll</span></span>](ixplogon-poll.md) <br/> |<span data-ttu-id="1e02c-134">Indica si el proveedor de transporte ha recibido uno o más mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="1e02c-134">Indicates whether the transport provider has received one or more inbound messages.</span></span>  <br/> |
|[<span data-ttu-id="1e02c-135">Desea iniciar</span><span class="sxs-lookup"><span data-stu-id="1e02c-135">StartMessage</span></span>](ixplogon-startmessage.md) <br/> |<span data-ttu-id="1e02c-136">Inicia a la transferencia de un mensaje entrante desde el proveedor de transporte a la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="1e02c-136">Initiates the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span>  <br/> |
|[<span data-ttu-id="1e02c-137">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="1e02c-137">OpenStatusEntry</span></span>](ixplogon-openstatusentry.md) <br/> |<span data-ttu-id="1e02c-138">Se abre el objeto de estado del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="1e02c-138">Opens the transport provider's status object.</span></span>  <br/> |
|[<span data-ttu-id="1e02c-139">ValidateState</span><span class="sxs-lookup"><span data-stu-id="1e02c-139">ValidateState</span></span>](ixplogon-validatestate.md) <br/> |<span data-ttu-id="1e02c-140">Comprobaciones de estado externo del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="1e02c-140">Checks the transport provider's external status.</span></span>  <br/> |
|[<span data-ttu-id="1e02c-141">FlushQueues</span><span class="sxs-lookup"><span data-stu-id="1e02c-141">FlushQueues</span></span>](ixplogon-flushqueues.md) <br/> |<span data-ttu-id="1e02c-142">Solicitudes que el proveedor de transporte entrega inmediatamente todos los mensajes entrantes o salientes pendientes.</span><span class="sxs-lookup"><span data-stu-id="1e02c-142">Requests that the transport provider immediately deliver all pending inbound or outbound messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1e02c-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e02c-143">See also</span></span>



[<span data-ttu-id="1e02c-144">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="1e02c-144">MAPI Interfaces</span></span>](mapi-interfaces.md)

