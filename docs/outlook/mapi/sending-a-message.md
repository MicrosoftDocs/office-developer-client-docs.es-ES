---
title: Enviar un mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4fa47824-b4ef-41e1-9096-c1b1cdacd7ac
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 68a842ccfdaea8ecdb975e1c510711b0e43fd576
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820596"
---
# <a name="sending-a-message"></a><span data-ttu-id="ce026-103">Enviar un mensaje</span><span class="sxs-lookup"><span data-stu-id="ce026-103">Sending a Message</span></span>

  
  
<span data-ttu-id="ce026-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ce026-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ce026-105">Cuando esté listo para enviar un mensaje, llame a su método [IMessage::SubmitMessage](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="ce026-105">When you are ready to send a message, call its [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> <span data-ttu-id="ce026-106">**SubmitMessage** coloca el mensaje en la cola de salida y establece el indicador MSGFLAG_SUBMIT en la propiedad del mensaje **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ce026-106">**SubmitMessage** places the message in the outgoing queue and sets the MSGFLAG_SUBMIT flag in the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="ce026-107">El proveedor de almacén de mensajes, si estrechamente con un proveedor de transporte, muestra el mensaje directamente en el transporte que ofrece para el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="ce026-107">The message store provider, if tightly coupled to a transport provider, gives the message directly to the transport which delivers it to the messaging system.</span></span> <span data-ttu-id="ce026-108">Si no se estrechamente acoplamiento, el proveedor de almacén de mensajes informa a la cola MAPI que ha cambiado la cola de salida y la cola MAPI transfiere el mensaje a un proveedor de transporte apropiado.</span><span class="sxs-lookup"><span data-stu-id="ce026-108">If not tightly coupled, the message store provider informs the MAPI spooler that the outgoing queue has changed and the MAPI spooler transfers the message to an appropriate transport provider.</span></span>
  
<span data-ttu-id="ce026-109">Si se permiten a los usuarios cancelar una operación de envío, llame a [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) para implementar esta característica.</span><span class="sxs-lookup"><span data-stu-id="ce026-109">If you allow users to cancel a send operation, call [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) to implement this feature.</span></span> <span data-ttu-id="ce026-110">**AbortSubmit** quita el mensaje de la cola de salida.</span><span class="sxs-lookup"><span data-stu-id="ce026-110">**AbortSubmit** removes the message from the outgoing queue.</span></span> <span data-ttu-id="ce026-111">Los usuarios pueden dejar un envío suceda hasta que el mensaje se le da al sistema de mensajería subyacente.</span><span class="sxs-lookup"><span data-stu-id="ce026-111">Users can be allowed to stop a send from happening until the message is given to the underlying messaging system.</span></span> 
  
<span data-ttu-id="ce026-112">Si **SubmitMessage** devuelve MAPI_E_CORRUPT_DATA, se supone que los datos enviados están ahora perdido.</span><span class="sxs-lookup"><span data-stu-id="ce026-112">If **SubmitMessage** returns MAPI_E_CORRUPT_DATA, assume that the data being sent is now lost.</span></span> <span data-ttu-id="ce026-113">Antes de intentar enviar una segunda vez, volver a escribir el mensaje mediante una llamada a [IMAPIProp::SetProps](imapiprop-setprops.md) y [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="ce026-113">Before attempting to send a second time, re-write the message by calling [IMAPIProp::SetProps](imapiprop-setprops.md) and [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="ce026-114">Mostrar un error al usuario si estas llamadas **IMAPIProp** producirá un error o si se produce un error en **SubmitMessage** una segunda vez.</span><span class="sxs-lookup"><span data-stu-id="ce026-114">Display an error to the user if these **IMAPIProp** calls fail or if **SubmitMessage** fails a second time.</span></span> 
  
<span data-ttu-id="ce026-115">Después de una llamada correcta a **SubmitMessage**, liberar cualquier memoria que se ha asignado para la lista de destinatarios y suelte el mensaje y sus datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="ce026-115">After a successful call to **SubmitMessage**, free any memory that was allocated for the recipient list and release the message and its attachments.</span></span> <span data-ttu-id="ce026-116">Una vez que se ha enviado un mensaje, MAPI no permite las operaciones posteriores en los punteros para estos objetos.</span><span class="sxs-lookup"><span data-stu-id="ce026-116">Once a message has been sent, MAPI does not permit any further operations on the pointers for these objects.</span></span> <span data-ttu-id="ce026-117">La única excepción es llamar a **IUnknown:: Release**.</span><span class="sxs-lookup"><span data-stu-id="ce026-117">The one exception is calling **IUnknown::Release**.</span></span> <span data-ttu-id="ce026-118">No hay otras llamadas se permiten porque muchos de los proveedores de almacén de mensajes invalidarán los identificadores de entrada para los mensajes que se han enviado.</span><span class="sxs-lookup"><span data-stu-id="ce026-118">No other calls are allowed because many message store providers invalidate entry identifiers for messages that have been sent.</span></span>
  

