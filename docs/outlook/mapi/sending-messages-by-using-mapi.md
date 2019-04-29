---
title: Enviar mensajes con MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3edfbfff-ea15-4926-bf0f-47137251d921
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: bf6324b89f06ef7f0553d3de1eaa24ae31a329ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438725"
---
# <a name="sending-messages-by-using-mapi"></a><span data-ttu-id="a86f4-103">Enviar mensajes con MAPI</span><span class="sxs-lookup"><span data-stu-id="a86f4-103">Sending Messages by Using MAPI</span></span>

  
  
<span data-ttu-id="a86f4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a86f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a86f4-105">Las aplicaciones cliente llaman al método [IMessage:: SubmitMessage](imessage-submitmessage.md) para enviar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="a86f4-105">Client applications call the [IMessage::SubmitMessage](imessage-submitmessage.md) method to send a message.</span></span> <span data-ttu-id="a86f4-106">**SubmitMessage** llama a [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) para guardar el mensaje antes de transferir el control a la cola de impresión MAPI o directamente a un proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="a86f4-106">**SubmitMessage** calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md) to save the message before transferring control to either the MAPI spooler or directly to a transport provider.</span></span> 
  
<span data-ttu-id="a86f4-107">La cola MAPI recibe el mensaje si se produce alguna de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="a86f4-107">The MAPI spooler receives the message if any of the following occur:</span></span>
  
- <span data-ttu-id="a86f4-108">El proveedor de almacenamiento de mensajes y el proveedor de transporte no están estrechamente acoplados.</span><span class="sxs-lookup"><span data-stu-id="a86f4-108">The message store provider and transport provider are not tightly coupled.</span></span>
    
- <span data-ttu-id="a86f4-109">El mensaje requiere preprocesamiento.</span><span class="sxs-lookup"><span data-stu-id="a86f4-109">The message requires preprocessing.</span></span>
    
- <span data-ttu-id="a86f4-110">El almacén de mensajes y el transporte estrechamente acoplados no pueden administrar todos los destinatarios a los que se dirige el mensaje.</span><span class="sxs-lookup"><span data-stu-id="a86f4-110">The tightly coupled message store and transport cannot handle all of the recipients to whom the message is addressed.</span></span>
    
<span data-ttu-id="a86f4-111">Un almacén de mensajes estrechamente acoplado debe tener en cuenta el estado de un mensaje antes de presentarlo a la cola MAPI que se va a descargar en un proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="a86f4-111">A tightly coupled message store must take into account a message's status before it presents it to the MAPI spooler to be downloaded to a transport provider.</span></span> <span data-ttu-id="a86f4-112">Hay situaciones en las que puede parecer que un mensaje requiere la cola MAPI, pero la cola MAPI no debería implicarse realmente.</span><span class="sxs-lookup"><span data-stu-id="a86f4-112">There are situations where a message may appear to require the MAPI spooler, but the MAPI spooler should really not be involved.</span></span>
  
<span data-ttu-id="a86f4-113">Por ejemplo, considere la situación en la que un usuario envía un mensaje desde la bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="a86f4-113">For example, consider the situation where a user submits a message from the Inbox.</span></span> <span data-ttu-id="a86f4-114">El cliente usa un almacén y transporte estrechamente acoplados.</span><span class="sxs-lookup"><span data-stu-id="a86f4-114">The client is using a tightly coupled store and transport.</span></span> <span data-ttu-id="a86f4-115">Si el almacén de mensajes muy acoplado usa la ubicación del mensaje como criterio único para decidir si se va a permitir o no que la cola MAPI controle el mensaje, la cola MAPI recibirá siempre el mensaje.</span><span class="sxs-lookup"><span data-stu-id="a86f4-115">If the tightly coupled message store uses the message's location as the sole criteria for deciding about whether or not to allow the MAPI spooler to handle the message, the MAPI spooler will always receive the message.</span></span> <span data-ttu-id="a86f4-116">Para evitar este tipo de problemas, un almacén de mensajes estrechamente acoplado debe comprobar el estado del mensaje además de la ubicación del mensaje.</span><span class="sxs-lookup"><span data-stu-id="a86f4-116">To avoid this kind of problem, a tightly coupled message store must check the message status in addition to message location.</span></span> <span data-ttu-id="a86f4-117">En concreto, el proveedor de transporte no debe solicitar que la cola MAPI Descargue los mensajes que se envían de forma activa.</span><span class="sxs-lookup"><span data-stu-id="a86f4-117">Specifically, the transport provider should not request that the MAPI spooler download any message that is actively submitted.</span></span>
  
<span data-ttu-id="a86f4-118">El proceso de transmisión de mensajes implica el proveedor de almacenamiento de mensajes, uno o varios proveedores de transporte y MAPI.</span><span class="sxs-lookup"><span data-stu-id="a86f4-118">The message transmission process involves the message store provider, one or more transport providers, and MAPI.</span></span> <span data-ttu-id="a86f4-119">En los temas de esta sección se proporciona información detallada sobre roles específicos en el proceso de transmisión de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a86f4-119">The topics in this section provide detailed information about specific roles in the message transmission process.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a86f4-120">Ver también</span><span class="sxs-lookup"><span data-stu-id="a86f4-120">See also</span></span>



[<span data-ttu-id="a86f4-121">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="a86f4-121">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="a86f4-122">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="a86f4-122">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)

