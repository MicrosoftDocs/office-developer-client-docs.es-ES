---
title: Información general sobre el administrador de trabajos en cola de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5866b202-883e-454e-aeb1-61526c43dae9
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 162957ea17b5a82d4da68340e971d328c85cd9f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432719"
---
# <a name="mapi-spooler-overview"></a><span data-ttu-id="0d569-103">Información general sobre el administrador de trabajos en cola de MAPI</span><span class="sxs-lookup"><span data-stu-id="0d569-103">MAPI spooler overview</span></span>
  
<span data-ttu-id="0d569-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d569-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d569-105">La cola MAPI es una función del proceso de Microsoft Office Outlook que se encarga de enviar y recibir mensajes de un sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="0d569-105">MAPI spooler is a function of the Microsoft Office Outlook process that is responsible for sending messages to and receiving messages from a messaging system.</span></span> <span data-ttu-id="0d569-106">La cola MAPI desempeña un papel fundamental en el envío y la entrega de mensajes.</span><span class="sxs-lookup"><span data-stu-id="0d569-106">MAPI spooler plays a vital role in message receipt and delivery.</span></span> <span data-ttu-id="0d569-107">Cuando un sistema de mensajería no está disponible, la cola MAPI almacena los mensajes y los reenvía automáticamente en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="0d569-107">When a messaging system is unavailable, MAPI spooler stores the messages and automatically forwards them at a later time.</span></span> <span data-ttu-id="0d569-108">Esta capacidad de retener datos o enviarlos cuando sea necesario se conoce como almacenamiento y reenvío, una característica crítica en entornos en los que las conexiones remotas son comunes y el tráfico de red es elevado.</span><span class="sxs-lookup"><span data-stu-id="0d569-108">This ability to hold on to or send data when necessary is known as store and forward, a critical feature in environments where remote connections are common and network traffic is high.</span></span> <span data-ttu-id="0d569-109">La cola MAPI se ejecuta como un subproceso en segundo plano en Outlook.</span><span class="sxs-lookup"><span data-stu-id="0d569-109">MAPI spooler runs as a background thread within Outlook.</span></span>
  
<span data-ttu-id="0d569-110">La cola MAPI tiene responsabilidades adicionales relacionadas con la distribución de mensajes.</span><span class="sxs-lookup"><span data-stu-id="0d569-110">MAPI spooler has additional responsibilities related to message distribution.</span></span> <span data-ttu-id="0d569-111">Entre estos deberes adicionales se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="0d569-111">These extra duties include the following:</span></span>
  
- <span data-ttu-id="0d569-112">Mantener un seguimiento de los tipos de destinatarios que administran los proveedores de transporte específicos.</span><span class="sxs-lookup"><span data-stu-id="0d569-112">Keeping track of the recipient types that are handled by specific transport providers.</span></span>
    
- <span data-ttu-id="0d569-113">Informar de una aplicación cliente cuando se ha entregado un nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="0d569-113">Informing a client application when a new message has been delivered.</span></span>
    
- <span data-ttu-id="0d569-114">Invocar el preprocesamiento y el procesamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="0d569-114">Invoking message preprocessing and postprocessing.</span></span>
    
- <span data-ttu-id="0d569-115">Generar informes que indican que se ha producido la entrega de mensajes.</span><span class="sxs-lookup"><span data-stu-id="0d569-115">Generating reports that indicate that message delivery has occurred.</span></span>
    
- <span data-ttu-id="0d569-116">Mantenimiento del estado de los destinatarios procesados.</span><span class="sxs-lookup"><span data-stu-id="0d569-116">Maintaining status on processed recipients.</span></span>
    
<span data-ttu-id="0d569-117">En la siguiente ilustración se muestra a alto nivel cómo fluye un mensaje de un cliente al sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="0d569-117">The following illustration shows at a high level how a message flows from a client to the messaging system.</span></span>
  
<span data-ttu-id="0d569-118">**Flujo de mensajes salientes**</span><span class="sxs-lookup"><span data-stu-id="0d569-118">**Outgoing message flow**</span></span>
  
<span data-ttu-id="0d569-119">![Flujo de mensajes salientes] (media/amapi_46.gif "Flujo de mensajes salientes")</span><span class="sxs-lookup"><span data-stu-id="0d569-119">![Outgoing message flow](media/amapi_46.gif "Outgoing message flow")</span></span>
  
<span data-ttu-id="0d569-120">El usuario de una aplicación cliente envía un mensaje a uno o más destinatarios.</span><span class="sxs-lookup"><span data-stu-id="0d569-120">The user of a client application sends a message to one or more recipients.</span></span> <span data-ttu-id="0d569-121">El proveedor de almacenamiento de mensajes inicia el proceso de envío, da formato al mensaje con la información adicional necesaria para la transmisión.</span><span class="sxs-lookup"><span data-stu-id="0d569-121">The message store provider initiates the sending process, formatting the message with additional information needed for transmission.</span></span>
  
<span data-ttu-id="0d569-122">La cola MAPI recibe el mensaje para procesar si se produce alguna de las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="0d569-122">MAPI spooler receives the message to process if any of the following conditions occur:</span></span>
  
- <span data-ttu-id="0d569-123">El proveedor de almacenamiento de mensajes no está estrechamente acoplado a un proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="0d569-123">The message store provider is not tightly coupled with a transport provider.</span></span>
    
- <span data-ttu-id="0d569-124">El mensaje requiere preprocesamiento.</span><span class="sxs-lookup"><span data-stu-id="0d569-124">The message requires preprocessing.</span></span>
    
- <span data-ttu-id="0d569-125">El almacén de mensajes y el proveedor de transporte están íntimamente acoplados, pero no pueden administrar todos los destinatarios a los que se dirige el mensaje.</span><span class="sxs-lookup"><span data-stu-id="0d569-125">The message store and transport provider are tightly coupled, but they cannot handle all the recipients to whom the message is addressed.</span></span>
    
<span data-ttu-id="0d569-126">Si la cola MAPI recibe el mensaje, realiza los preprocesamientos necesarios y entrega el mensaje al proveedor de transporte correspondiente.</span><span class="sxs-lookup"><span data-stu-id="0d569-126">If MAPI spooler receives the message, it performs any required preprocessing and delivers the message to the appropriate transport provider.</span></span> <span data-ttu-id="0d569-127">El proveedor de transporte entrega el mensaje a su sistema de mensajería, que lo envía a su destinatario previsto.</span><span class="sxs-lookup"><span data-stu-id="0d569-127">The transport provider gives the message to its messaging system, which sends it to its intended recipient.</span></span>
  
<span data-ttu-id="0d569-128">Con los mensajes entrantes, el flujo se invierte.</span><span class="sxs-lookup"><span data-stu-id="0d569-128">With incoming messages, the flow is reversed.</span></span> <span data-ttu-id="0d569-129">El proveedor de transporte recibe un mensaje de su sistema de mensajería y lo notifica a la cola de impresión de MAPI.</span><span class="sxs-lookup"><span data-stu-id="0d569-129">The transport provider receives a message from its messaging system and notifies MAPI spooler.</span></span> <span data-ttu-id="0d569-130">La cola de impresión realiza los postprocesamientos necesarios e informa al proveedor del almacén de mensajes que ha recibido un mensaje nuevo.</span><span class="sxs-lookup"><span data-stu-id="0d569-130">Spooler performs any necessary postprocessing and informs the message store provider that a new message has arrived.</span></span> <span data-ttu-id="0d569-131">Esta notificación hace que el cliente actualice la presentación del mensaje, lo que permite al usuario leer el nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="0d569-131">This notification causes the client to refresh its message display, enabling the user to read the new message.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0d569-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="0d569-132">See also</span></span>

- [<span data-ttu-id="0d569-133">Arquitectura y características de MAPI</span><span class="sxs-lookup"><span data-stu-id="0d569-133">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

