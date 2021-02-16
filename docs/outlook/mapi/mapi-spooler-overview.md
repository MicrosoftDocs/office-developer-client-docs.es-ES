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
# <a name="mapi-spooler-overview"></a><span data-ttu-id="ca889-103">Información general sobre el administrador de trabajos en cola de MAPI</span><span class="sxs-lookup"><span data-stu-id="ca889-103">MAPI spooler overview</span></span>
  
<span data-ttu-id="ca889-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca889-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca889-105">La cola MAPI es una función del proceso Microsoft Office Outlook que se encarga de enviar y recibir mensajes de un sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="ca889-105">MAPI spooler is a function of the Microsoft Office Outlook process that is responsible for sending messages to and receiving messages from a messaging system.</span></span> <span data-ttu-id="ca889-106">La cola MAPI desempeña un papel fundamental en la recepción y entrega de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ca889-106">MAPI spooler plays a vital role in message receipt and delivery.</span></span> <span data-ttu-id="ca889-107">Cuando un sistema de mensajería no está disponible, la cola MAPI almacena los mensajes y los reenvía automáticamente más adelante.</span><span class="sxs-lookup"><span data-stu-id="ca889-107">When a messaging system is unavailable, MAPI spooler stores the messages and automatically forwards them at a later time.</span></span> <span data-ttu-id="ca889-108">Esta capacidad de retener o enviar datos cuando sea necesario se conoce como almacenar y reenviar, una característica crítica en entornos donde las conexiones remotas son comunes y el tráfico de red es alto.</span><span class="sxs-lookup"><span data-stu-id="ca889-108">This ability to hold on to or send data when necessary is known as store and forward, a critical feature in environments where remote connections are common and network traffic is high.</span></span> <span data-ttu-id="ca889-109">La cola MAPI se ejecuta como un subproceso en segundo plano en Outlook.</span><span class="sxs-lookup"><span data-stu-id="ca889-109">MAPI spooler runs as a background thread within Outlook.</span></span>
  
<span data-ttu-id="ca889-110">La cola MAPI tiene responsabilidades adicionales relacionadas con la distribución de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ca889-110">MAPI spooler has additional responsibilities related to message distribution.</span></span> <span data-ttu-id="ca889-111">Entre estas tareas adicionales se incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="ca889-111">These extra duties include the following:</span></span>
  
- <span data-ttu-id="ca889-112">Realizar un seguimiento de los tipos de destinatarios que administran proveedores de transporte específicos.</span><span class="sxs-lookup"><span data-stu-id="ca889-112">Keeping track of the recipient types that are handled by specific transport providers.</span></span>
    
- <span data-ttu-id="ca889-113">Informar a una aplicación cliente cuando se ha entregado un nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="ca889-113">Informing a client application when a new message has been delivered.</span></span>
    
- <span data-ttu-id="ca889-114">Invocar preprocesamiento y posprocesamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ca889-114">Invoking message preprocessing and postprocessing.</span></span>
    
- <span data-ttu-id="ca889-115">Generación de informes que indican que se ha producido la entrega de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ca889-115">Generating reports that indicate that message delivery has occurred.</span></span>
    
- <span data-ttu-id="ca889-116">Mantener el estado de los destinatarios procesados.</span><span class="sxs-lookup"><span data-stu-id="ca889-116">Maintaining status on processed recipients.</span></span>
    
<span data-ttu-id="ca889-117">En la siguiente ilustración se muestra en un nivel alto cómo fluye un mensaje desde un cliente al sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="ca889-117">The following illustration shows at a high level how a message flows from a client to the messaging system.</span></span>
  
<span data-ttu-id="ca889-118">**Flujo de mensajes salientes**</span><span class="sxs-lookup"><span data-stu-id="ca889-118">**Outgoing message flow**</span></span>
  
<span data-ttu-id="ca889-119">![Flujo de mensajes salientes Flujo](media/amapi_46.gif "de mensajes salientes")</span><span class="sxs-lookup"><span data-stu-id="ca889-119">![Outgoing message flow](media/amapi_46.gif "Outgoing message flow")</span></span>
  
<span data-ttu-id="ca889-120">El usuario de una aplicación cliente envía un mensaje a uno o más destinatarios.</span><span class="sxs-lookup"><span data-stu-id="ca889-120">The user of a client application sends a message to one or more recipients.</span></span> <span data-ttu-id="ca889-121">El proveedor del almacén de mensajes inicia el proceso de envío, formateando el mensaje con información adicional necesaria para la transmisión.</span><span class="sxs-lookup"><span data-stu-id="ca889-121">The message store provider initiates the sending process, formatting the message with additional information needed for transmission.</span></span>
  
<span data-ttu-id="ca889-122">La cola MAPI recibe el mensaje para procesar si se produce alguna de las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="ca889-122">MAPI spooler receives the message to process if any of the following conditions occur:</span></span>
  
- <span data-ttu-id="ca889-123">El proveedor de almacenamiento de mensajes no está estrechamente asociado con un proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="ca889-123">The message store provider is not tightly coupled with a transport provider.</span></span>
    
- <span data-ttu-id="ca889-124">El mensaje requiere preprocesamiento.</span><span class="sxs-lookup"><span data-stu-id="ca889-124">The message requires preprocessing.</span></span>
    
- <span data-ttu-id="ca889-125">El almacén de mensajes y el proveedor de transporte están estrechamente emparejados, pero no pueden controlar todos los destinatarios a los que se dirige el mensaje.</span><span class="sxs-lookup"><span data-stu-id="ca889-125">The message store and transport provider are tightly coupled, but they cannot handle all the recipients to whom the message is addressed.</span></span>
    
<span data-ttu-id="ca889-126">Si la cola MAPI recibe el mensaje, realiza cualquier preprocesamiento necesario y entrega el mensaje al proveedor de transporte adecuado.</span><span class="sxs-lookup"><span data-stu-id="ca889-126">If MAPI spooler receives the message, it performs any required preprocessing and delivers the message to the appropriate transport provider.</span></span> <span data-ttu-id="ca889-127">El proveedor de transporte entrega el mensaje a su sistema de mensajería, que lo envía a su destinatario previsto.</span><span class="sxs-lookup"><span data-stu-id="ca889-127">The transport provider gives the message to its messaging system, which sends it to its intended recipient.</span></span>
  
<span data-ttu-id="ca889-128">Con los mensajes entrantes, el flujo se invierte.</span><span class="sxs-lookup"><span data-stu-id="ca889-128">With incoming messages, the flow is reversed.</span></span> <span data-ttu-id="ca889-129">El proveedor de transporte recibe un mensaje de su sistema de mensajería y se lo comunica a la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="ca889-129">The transport provider receives a message from its messaging system and notifies MAPI spooler.</span></span> <span data-ttu-id="ca889-130">Spooler realiza el posprocesamiento necesario e informa al proveedor de al almacenamiento de mensajes de que ha llegado un nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="ca889-130">Spooler performs any necessary postprocessing and informs the message store provider that a new message has arrived.</span></span> <span data-ttu-id="ca889-131">Esta notificación hace que el cliente actualice su visualización de mensajes, lo que permite al usuario leer el nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="ca889-131">This notification causes the client to refresh its message display, enabling the user to read the new message.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ca889-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ca889-132">See also</span></span>

- [<span data-ttu-id="ca889-133">Arquitectura y características mapi</span><span class="sxs-lookup"><span data-stu-id="ca889-133">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

