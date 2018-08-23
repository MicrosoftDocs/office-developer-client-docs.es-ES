---
title: Información general sobre la cola de impresión MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5866b202-883e-454e-aeb1-61526c43dae9
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ec581e2170b92721410106eae00e2d36b3c775a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591341"
---
# <a name="mapi-spooler-overview"></a><span data-ttu-id="59ad3-103">Información general sobre la cola de impresión MAPI</span><span class="sxs-lookup"><span data-stu-id="59ad3-103">MAPI spooler overview</span></span>
  
<span data-ttu-id="59ad3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59ad3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="59ad3-105">Cola MAPI es una función del proceso de Microsoft Office Outlook que se encarga de envío de mensajes a y recibir mensajes desde un sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="59ad3-105">MAPI spooler is a function of the Microsoft Office Outlook process that is responsible for sending messages to and receiving messages from a messaging system.</span></span> <span data-ttu-id="59ad3-106">Cola MAPI desempeña un papel fundamental en la entrega y recepción de mensajes.</span><span class="sxs-lookup"><span data-stu-id="59ad3-106">MAPI spooler plays a vital role in message receipt and delivery.</span></span> <span data-ttu-id="59ad3-107">Cuando un sistema de mensajería no está disponible, cola MAPI almacena los mensajes y los reenvía automáticamente en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="59ad3-107">When a messaging system is unavailable, MAPI spooler stores the messages and automatically forwards them at a later time.</span></span> <span data-ttu-id="59ad3-108">Esta capacidad de suspensión en a o enviar datos cuando sea necesario se conoce como almacenar y reenviar, una característica importante en entornos donde las conexiones remotas son comunes y el tráfico de red es alto.</span><span class="sxs-lookup"><span data-stu-id="59ad3-108">This ability to hold on to or send data when necessary is known as store and forward, a critical feature in environments where remote connections are common and network traffic is high.</span></span> <span data-ttu-id="59ad3-109">Cola MAPI se ejecuta como un subproceso de fondo dentro de Outlook.</span><span class="sxs-lookup"><span data-stu-id="59ad3-109">MAPI spooler runs as a background thread within Outlook.</span></span>
  
<span data-ttu-id="59ad3-110">Cola MAPI tiene responsabilidades adicionales relacionadas con la distribución de mensaje.</span><span class="sxs-lookup"><span data-stu-id="59ad3-110">MAPI spooler has additional responsibilities related to message distribution.</span></span> <span data-ttu-id="59ad3-111">Estos derechos adicionales son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="59ad3-111">These extra duties include the following:</span></span>
  
- <span data-ttu-id="59ad3-112">Seguimiento de los tipos de destinatarios que se controlan mediante proveedores de transporte específica.</span><span class="sxs-lookup"><span data-stu-id="59ad3-112">Keeping track of the recipient types that are handled by specific transport providers.</span></span>
    
- <span data-ttu-id="59ad3-113">Informar a una aplicación cliente cuando se ha entregado un mensaje nuevo.</span><span class="sxs-lookup"><span data-stu-id="59ad3-113">Informing a client application when a new message has been delivered.</span></span>
    
- <span data-ttu-id="59ad3-114">Mensaje de invocación de preprocesamiento y procesamiento posterior.</span><span class="sxs-lookup"><span data-stu-id="59ad3-114">Invoking message preprocessing and postprocessing.</span></span>
    
- <span data-ttu-id="59ad3-115">Se ha producido la generación de informes que indican que la entrega de mensajes.</span><span class="sxs-lookup"><span data-stu-id="59ad3-115">Generating reports that indicate that message delivery has occurred.</span></span>
    
- <span data-ttu-id="59ad3-116">Mantenimiento de estado en los destinatarios procesados.</span><span class="sxs-lookup"><span data-stu-id="59ad3-116">Maintaining status on processed recipients.</span></span>
    
<span data-ttu-id="59ad3-117">En la siguiente ilustración se muestra a un nivel alto, cómo se transmite un mensaje desde un cliente para el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="59ad3-117">The following illustration shows at a high level how a message flows from a client to the messaging system.</span></span>
  
<span data-ttu-id="59ad3-118">**Flujo de mensajes salientes**</span><span class="sxs-lookup"><span data-stu-id="59ad3-118">**Outgoing message flow**</span></span>
  
<span data-ttu-id="59ad3-119">![Flujo de mensajes de salida] (media/amapi_46.gif "Flujo de mensajes de salida")</span><span class="sxs-lookup"><span data-stu-id="59ad3-119">![Outgoing message flow](media/amapi_46.gif "Outgoing message flow")</span></span>
  
<span data-ttu-id="59ad3-120">El usuario de una aplicación cliente envía un mensaje a uno o más destinatarios.</span><span class="sxs-lookup"><span data-stu-id="59ad3-120">The user of a client application sends a message to one or more recipients.</span></span> <span data-ttu-id="59ad3-121">El mensaje almacenar proveedor inicia el proceso de envío, dar formato al mensaje con información adicional que sea necesaria para la transmisión.</span><span class="sxs-lookup"><span data-stu-id="59ad3-121">The message store provider initiates the sending process, formatting the message with additional information needed for transmission.</span></span>
  
<span data-ttu-id="59ad3-122">Cola MAPI recibe el mensaje para procesar si se produce alguna de las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="59ad3-122">MAPI spooler receives the message to process if any of the following conditions occur:</span></span>
  
- <span data-ttu-id="59ad3-123">El proveedor de almacén de mensajes no se complementa con un proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="59ad3-123">The message store provider is not tightly coupled with a transport provider.</span></span>
    
- <span data-ttu-id="59ad3-124">El mensaje requiere preprocesamiento.</span><span class="sxs-lookup"><span data-stu-id="59ad3-124">The message requires preprocessing.</span></span>
    
- <span data-ttu-id="59ad3-125">El almacén de mensajes y transporte de proveedor se complementa muy bien, pero no pueden administrar todos los destinatarios a quienes está dirigido el mensaje.</span><span class="sxs-lookup"><span data-stu-id="59ad3-125">The message store and transport provider are tightly coupled, but they cannot handle all the recipients to whom the message is addressed.</span></span>
    
<span data-ttu-id="59ad3-126">Si la cola MAPI recibe el mensaje, realiza cualquier preprocesamiento necesarios y entrega el mensaje con el proveedor de transporte apropiado.</span><span class="sxs-lookup"><span data-stu-id="59ad3-126">If MAPI spooler receives the message, it performs any required preprocessing and delivers the message to the appropriate transport provider.</span></span> <span data-ttu-id="59ad3-127">El proveedor de transporte proporciona el mensaje a su sistema de mensajería, que se envía a su destinatario.</span><span class="sxs-lookup"><span data-stu-id="59ad3-127">The transport provider gives the message to its messaging system, which sends it to its intended recipient.</span></span>
  
<span data-ttu-id="59ad3-128">Con los mensajes entrantes, se invierte el flujo.</span><span class="sxs-lookup"><span data-stu-id="59ad3-128">With incoming messages, the flow is reversed.</span></span> <span data-ttu-id="59ad3-129">El proveedor de transporte recibe un mensaje de su sistema de mensajería y se lo comunica a cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="59ad3-129">The transport provider receives a message from its messaging system and notifies MAPI spooler.</span></span> <span data-ttu-id="59ad3-130">Cola de impresión realiza cualquier procesamiento posterior es necesario e informa que el proveedor de almacenamiento de mensaje que ha recibido un nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="59ad3-130">Spooler performs any necessary postprocessing and informs the message store provider that a new message has arrived.</span></span> <span data-ttu-id="59ad3-131">Esta notificación hace que el cliente actualizar su presentación de mensajes, permitiendo al usuario leer el mensaje de nuevo.</span><span class="sxs-lookup"><span data-stu-id="59ad3-131">This notification causes the client to refresh its message display, enabling the user to read the new message.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="59ad3-132">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="59ad3-132">See also</span></span>

- [<span data-ttu-id="59ad3-133">Arquitectura y las características MAPI</span><span class="sxs-lookup"><span data-stu-id="59ad3-133">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

