---
title: Envío de un mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4fa47824-b4ef-41e1-9096-c1b1cdacd7ac
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 01fd66033da0f24948913f47a752d555eca655fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423625"
---
# <a name="sending-a-message"></a><span data-ttu-id="a9beb-103">Envío de un mensaje</span><span class="sxs-lookup"><span data-stu-id="a9beb-103">Sending a Message</span></span>

  
  
<span data-ttu-id="a9beb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a9beb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a9beb-105">Cuando esté listo para enviar un mensaje, llame a su [método IMessage::SubmitMessage.](imessage-submitmessage.md)</span><span class="sxs-lookup"><span data-stu-id="a9beb-105">When you are ready to send a message, call its [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> <span data-ttu-id="a9beb-106">**SubmitMessage** coloca el mensaje en la cola de salida y establece la marca MSGFLAG_SUBMIT en la propiedad PR_MESSAGE_FLAGS **(** [PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) del mensaje.</span><span class="sxs-lookup"><span data-stu-id="a9beb-106">**SubmitMessage** places the message in the outgoing queue and sets the MSGFLAG_SUBMIT flag in the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="a9beb-107">El proveedor de al almacenamiento de mensajes, si está estrechamente unido a un proveedor de transporte, entrega el mensaje directamente al transporte que lo entrega al sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="a9beb-107">The message store provider, if tightly coupled to a transport provider, gives the message directly to the transport which delivers it to the messaging system.</span></span> <span data-ttu-id="a9beb-108">Si no está estrechamente acoplada, el proveedor de almacenamiento de mensajes informa a la cola MAPI de que la cola saliente ha cambiado y la cola MAPI transfiere el mensaje a un proveedor de transporte adecuado.</span><span class="sxs-lookup"><span data-stu-id="a9beb-108">If not tightly coupled, the message store provider informs the MAPI spooler that the outgoing queue has changed and the MAPI spooler transfers the message to an appropriate transport provider.</span></span>
  
<span data-ttu-id="a9beb-109">Si permite que los usuarios cancelen una operación de envío, llame a [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) para implementar esta característica.</span><span class="sxs-lookup"><span data-stu-id="a9beb-109">If you allow users to cancel a send operation, call [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) to implement this feature.</span></span> <span data-ttu-id="a9beb-110">**AbortSubmit** quita el mensaje de la cola saliente.</span><span class="sxs-lookup"><span data-stu-id="a9beb-110">**AbortSubmit** removes the message from the outgoing queue.</span></span> <span data-ttu-id="a9beb-111">Se puede permitir a los usuarios detener el envío hasta que el mensaje se entrega al sistema de mensajería subyacente.</span><span class="sxs-lookup"><span data-stu-id="a9beb-111">Users can be allowed to stop a send from happening until the message is given to the underlying messaging system.</span></span> 
  
<span data-ttu-id="a9beb-112">Si **SubmitMessage** devuelve MAPI_E_CORRUPT_DATA, suponga que los datos que se envían ahora se pierden.</span><span class="sxs-lookup"><span data-stu-id="a9beb-112">If **SubmitMessage** returns MAPI_E_CORRUPT_DATA, assume that the data being sent is now lost.</span></span> <span data-ttu-id="a9beb-113">Antes de intentar enviar una segunda vez, vuelva a escribir el mensaje llamando a [IMAPIProp::SetProps](imapiprop-setprops.md) e [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="a9beb-113">Before attempting to send a second time, re-write the message by calling [IMAPIProp::SetProps](imapiprop-setprops.md) and [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="a9beb-114">Muestra un error al usuario si se produce un error en estas **llamadas IMAPIProp** o **si SubmitMessage falla** una segunda vez.</span><span class="sxs-lookup"><span data-stu-id="a9beb-114">Display an error to the user if these **IMAPIProp** calls fail or if **SubmitMessage** fails a second time.</span></span> 
  
<span data-ttu-id="a9beb-115">Después de realizar una llamada correcta a **SubmitMessage,** libere la memoria asignada para la lista de destinatarios y libere el mensaje y sus datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="a9beb-115">After a successful call to **SubmitMessage**, free any memory that was allocated for the recipient list and release the message and its attachments.</span></span> <span data-ttu-id="a9beb-116">Una vez que se ha enviado un mensaje, MAPI no permite ninguna otra operación en los punteros de estos objetos.</span><span class="sxs-lookup"><span data-stu-id="a9beb-116">Once a message has been sent, MAPI does not permit any further operations on the pointers for these objects.</span></span> <span data-ttu-id="a9beb-117">La única excepción es llamar a **IUnknown::Release**.</span><span class="sxs-lookup"><span data-stu-id="a9beb-117">The one exception is calling **IUnknown::Release**.</span></span> <span data-ttu-id="a9beb-118">No se permiten otras llamadas porque muchos proveedores de al almacenamiento de mensajes invalidan los identificadores de entrada de los mensajes que se han enviado.</span><span class="sxs-lookup"><span data-stu-id="a9beb-118">No other calls are allowed because many message store providers invalidate entry identifiers for messages that have been sent.</span></span>
  

