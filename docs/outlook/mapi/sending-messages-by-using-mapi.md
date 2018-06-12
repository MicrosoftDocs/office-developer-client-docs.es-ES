---
title: Envío de mensajes mediante el uso de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3edfbfff-ea15-4926-bf0f-47137251d921
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 36de3b70b0ab7b16f8abed85bbd0983224e00568
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820620"
---
# <a name="sending-messages-by-using-mapi"></a><span data-ttu-id="ecca4-103">Envío de mensajes mediante el uso de MAPI</span><span class="sxs-lookup"><span data-stu-id="ecca4-103">Sending Messages by Using MAPI</span></span>

  
  
<span data-ttu-id="ecca4-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ecca4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ecca4-105">Las aplicaciones cliente de llaman al método [IMessage::SubmitMessage](imessage-submitmessage.md) para enviar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="ecca4-105">Client applications call the [IMessage::SubmitMessage](imessage-submitmessage.md) method to send a message.</span></span> <span data-ttu-id="ecca4-106">**SubmitMessage** llama a [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para guardar el mensaje antes de transferir el control a cualquiera la cola MAPI o directamente a un proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="ecca4-106">**SubmitMessage** calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md) to save the message before transferring control to either the MAPI spooler or directly to a transport provider.</span></span> 
  
<span data-ttu-id="ecca4-107">La cola MAPI recibe el mensaje si se produce alguna de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="ecca4-107">The MAPI spooler receives the message if any of the following occur:</span></span>
  
- <span data-ttu-id="ecca4-108">El proveedor de almacén de mensajes y el proveedor de transporte no están íntimamente relacionadas.</span><span class="sxs-lookup"><span data-stu-id="ecca4-108">The message store provider and transport provider are not tightly coupled.</span></span>
    
- <span data-ttu-id="ecca4-109">El mensaje requiere preprocesamiento.</span><span class="sxs-lookup"><span data-stu-id="ecca4-109">The message requires preprocessing.</span></span>
    
- <span data-ttu-id="ecca4-110">El almacén de mensajes acoplado y el transporte no pueden controlar todos los destinatarios a quienes se envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="ecca4-110">The tightly coupled message store and transport cannot handle all of the recipients to whom the message is addressed.</span></span>
    
<span data-ttu-id="ecca4-111">Un almacén de mensajes acoplado debe tener en cuenta el estado de un mensaje antes de que presenta a la cola MAPI para descargarse a un proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="ecca4-111">A tightly coupled message store must take into account a message's status before it presents it to the MAPI spooler to be downloaded to a transport provider.</span></span> <span data-ttu-id="ecca4-112">Hay situaciones en las que es posible que aparezca un mensaje requerir a la cola MAPI, pero la cola MAPI debe realmente no participar.</span><span class="sxs-lookup"><span data-stu-id="ecca4-112">There are situations where a message may appear to require the MAPI spooler, but the MAPI spooler should really not be involved.</span></span>
  
<span data-ttu-id="ecca4-113">Por ejemplo, considere la situación donde un usuario envía un mensaje de la Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="ecca4-113">For example, consider the situation where a user submits a message from the Inbox.</span></span> <span data-ttu-id="ecca4-114">El cliente está usando un almacén acoplado y transporte.</span><span class="sxs-lookup"><span data-stu-id="ecca4-114">The client is using a tightly coupled store and transport.</span></span> <span data-ttu-id="ecca4-115">Si el almacén de mensajes acoplado usa ubicación del mensaje como el único criterio para que decidir sobre si deben o no permitir a la cola MAPI administrar el mensaje, la cola MAPI siempre recibirán el mensaje.</span><span class="sxs-lookup"><span data-stu-id="ecca4-115">If the tightly coupled message store uses the message's location as the sole criteria for deciding about whether or not to allow the MAPI spooler to handle the message, the MAPI spooler will always receive the message.</span></span> <span data-ttu-id="ecca4-116">Para evitar este tipo de problema, un almacén de mensajes acoplado debe comprobar el estado del mensaje además de la ubicación del mensaje.</span><span class="sxs-lookup"><span data-stu-id="ecca4-116">To avoid this kind of problem, a tightly coupled message store must check the message status in addition to message location.</span></span> <span data-ttu-id="ecca4-117">En concreto, el proveedor de transporte no debería solicitar que la cola MAPI descargar los mensajes que se envían de forma activa.</span><span class="sxs-lookup"><span data-stu-id="ecca4-117">Specifically, the transport provider should not request that the MAPI spooler download any message that is actively submitted.</span></span>
  
<span data-ttu-id="ecca4-118">El proceso de transmisión de mensajes implica el proveedor de almacenamiento de mensajes, uno o varios proveedores de transporte y MAPI.</span><span class="sxs-lookup"><span data-stu-id="ecca4-118">The message transmission process involves the message store provider, one or more transport providers, and MAPI.</span></span> <span data-ttu-id="ecca4-119">En los temas de esta sección proporcionan información detallada acerca de las funciones específicas en el proceso de transmisión de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ecca4-119">The topics in this section provide detailed information about specific roles in the message transmission process.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ecca4-120">Ver también</span><span class="sxs-lookup"><span data-stu-id="ecca4-120">See also</span></span>



[<span data-ttu-id="ecca4-121">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="ecca4-121">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="ecca4-122">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="ecca4-122">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)

