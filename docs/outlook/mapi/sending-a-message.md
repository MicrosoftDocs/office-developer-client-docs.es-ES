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
# <a name="sending-a-message"></a><span data-ttu-id="33c1b-103">Envío de un mensaje</span><span class="sxs-lookup"><span data-stu-id="33c1b-103">Sending a Message</span></span>

  
  
<span data-ttu-id="33c1b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33c1b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33c1b-105">Cuando esté listo para enviar un mensaje, llame a su método [IMessage:: SubmitMessage](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="33c1b-105">When you are ready to send a message, call its [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> <span data-ttu-id="33c1b-106">**SubmitMessage** coloca el mensaje en la cola de salida y establece la marca MSGFLAG_SUBMIT en la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) del mensaje.</span><span class="sxs-lookup"><span data-stu-id="33c1b-106">**SubmitMessage** places the message in the outgoing queue and sets the MSGFLAG_SUBMIT flag in the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="33c1b-107">El proveedor de almacenamiento de mensajes, si está estrechamente acoplado a un proveedor de transporte, le envía el mensaje directamente al transporte que lo entrega al sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="33c1b-107">The message store provider, if tightly coupled to a transport provider, gives the message directly to the transport which delivers it to the messaging system.</span></span> <span data-ttu-id="33c1b-108">Si no se combina estrechamente, el proveedor de almacenamiento de mensajes informa a la cola MAPI de que la cola de salida ha cambiado y la cola MAPI transfiere el mensaje a un proveedor de transporte adecuado.</span><span class="sxs-lookup"><span data-stu-id="33c1b-108">If not tightly coupled, the message store provider informs the MAPI spooler that the outgoing queue has changed and the MAPI spooler transfers the message to an appropriate transport provider.</span></span>
  
<span data-ttu-id="33c1b-109">Si permite a los usuarios cancelar una operación de envío, llame a [IMsgStore:: AbortSubmit](imsgstore-abortsubmit.md) para implementar esta característica.</span><span class="sxs-lookup"><span data-stu-id="33c1b-109">If you allow users to cancel a send operation, call [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) to implement this feature.</span></span> <span data-ttu-id="33c1b-110">**AbortSubmit** quita el mensaje de la cola de salida.</span><span class="sxs-lookup"><span data-stu-id="33c1b-110">**AbortSubmit** removes the message from the outgoing queue.</span></span> <span data-ttu-id="33c1b-111">Los usuarios pueden impedir que se produzca un envío hasta que se le dé el mensaje al sistema de mensajería subyacente.</span><span class="sxs-lookup"><span data-stu-id="33c1b-111">Users can be allowed to stop a send from happening until the message is given to the underlying messaging system.</span></span> 
  
<span data-ttu-id="33c1b-112">Si **SubmitMessage** devuelve MAPI_E_CORRUPT_DATA, asuma que los datos que se están enviando se han perdido.</span><span class="sxs-lookup"><span data-stu-id="33c1b-112">If **SubmitMessage** returns MAPI_E_CORRUPT_DATA, assume that the data being sent is now lost.</span></span> <span data-ttu-id="33c1b-113">Antes de intentar enviar una segunda vez, vuelva a escribir el mensaje mediante una llamada a [IMAPIProp:: SetProps](imapiprop-setprops.md) y [IMAPIProp:: SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="33c1b-113">Before attempting to send a second time, re-write the message by calling [IMAPIProp::SetProps](imapiprop-setprops.md) and [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="33c1b-114">Muestra un error al usuario si se produce un error en las llamadas de **IMAPIProp** o si **SubmitMessage** por segunda vez.</span><span class="sxs-lookup"><span data-stu-id="33c1b-114">Display an error to the user if these **IMAPIProp** calls fail or if **SubmitMessage** fails a second time.</span></span> 
  
<span data-ttu-id="33c1b-115">Tras realizar correctamente una llamada a **SubmitMessage**, libere la memoria asignada a la lista de destinatarios y libere el mensaje y sus datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="33c1b-115">After a successful call to **SubmitMessage**, free any memory that was allocated for the recipient list and release the message and its attachments.</span></span> <span data-ttu-id="33c1b-116">Una vez que se ha enviado un mensaje, MAPI no permite más operaciones en los punteros de estos objetos.</span><span class="sxs-lookup"><span data-stu-id="33c1b-116">Once a message has been sent, MAPI does not permit any further operations on the pointers for these objects.</span></span> <span data-ttu-id="33c1b-117">La única excepción está llamando a **IUnknown:: Release**.</span><span class="sxs-lookup"><span data-stu-id="33c1b-117">The one exception is calling **IUnknown::Release**.</span></span> <span data-ttu-id="33c1b-118">No se permiten otras llamadas porque muchos proveedores de almacenamiento de mensajes invalidan identificadores de entrada para los mensajes enviados.</span><span class="sxs-lookup"><span data-stu-id="33c1b-118">No other calls are allowed because many message store providers invalidate entry identifiers for messages that have been sent.</span></span>
  

