---
title: Crear y almacenar mensajes en los almacenes de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc74b31c-d7ed-4fcf-9535-a2f9222901b7
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7c923a330c542dff8b1bbc476461ccd21680a5b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332903"
---
# <a name="creating-and-storing-messages-in-message-stores"></a><span data-ttu-id="1b477-103">Crear y almacenar mensajes en los almacenes de mensajes</span><span class="sxs-lookup"><span data-stu-id="1b477-103">Creating and Storing Messages in Message Stores</span></span>

  
  
<span data-ttu-id="1b477-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b477-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b477-p101">La forma en que su proveedor de almacén de mensajes crea y almacena los mensajes en el mecanismo de almacenamiento subyacente depende en gran medida del propio mecanismo de almacenamiento subyacente. En general, sólo necesita escribir código para conservar las propiedades de un mensaje y sus valores.</span><span class="sxs-lookup"><span data-stu-id="1b477-p101">How your message store provider creates and stores messages in the underlying storage mechanism depends heavily on the underlying storage mechanism itself. In general, you need only to write code to preserve the properties of a message and their values.</span></span>
  
<span data-ttu-id="1b477-p102">Cuando el proveedor de almacén de mensajes crea un nuevo mensaje, el proveedor debe crear el mensaje con las propiedades necesarias para los mensajes. Encontrará una lista de estas propiedades en la documentación de la interfaz [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md). Después, las aplicaciones cliente agregan las propiedades adicionales con métodos[IMAPIProp](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="1b477-p102">When the message store provider creates a new message, the provider needs to create the message with the required properties for messages. A list of these properties can be found in the documentation for the [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) interface. After that, client applications add any additional properties with [IMAPIProp](imapipropiunknown.md) methods.</span></span> 
  
<span data-ttu-id="1b477-110">Cuando el proveedor de almacén de mensajes guarda un mensaje en el mecanismo de almacenamiento subyacente, el proveedor debe revisar las propiedades del mensaje y guardarlas en el mecanismo de almacenamiento subyacente para que se puedan recuperar completamente si el mensaje se abre más tarde.</span><span class="sxs-lookup"><span data-stu-id="1b477-110">When the message store provider saves a message to the underlying storage mechanism, the provider needs to iterate over the message's properties, and save them to the underlying storage mechanism such that they can be fully recovered if the message is later opened.</span></span>
  
<span data-ttu-id="1b477-p103">MAPI requiere que las propiedades de las interfaces [IMessage](imessageimapiprop.md) interfaces sean transferidas, lo que significa que los cambios realizados en ellas no se conviertan en permanentes hasta que se llame al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) en el mensaje objeto. El proveedor del almacén de mensajes es responsable de implementar este comportamiento. Normalmente no es difícil; significa simplemente mantener las propiedades en memoria mientras se están modificando y confirmarlas en el mecanismo de almacenamiento subyacente cuando se llame a **SaveChanges**.</span><span class="sxs-lookup"><span data-stu-id="1b477-p103">MAPI requires that the properties on [IMessage](imessageimapiprop.md) interfaces are transacted, meaning that changes made to them do not become permanent until the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is called on the message object. The message store provider is responsible for implementing this behavior. Usually this is not difficult; it simply means holding properties in memory while they are being modified and committing them to the underlying storage mechanism when **SaveChanges** is called.</span></span> 
  
<span data-ttu-id="1b477-114">Algunas propiedades de los objetos de mensaje tienen semántica especial para las aplicaciones cliente con respecto al método **SaveChanges**:</span><span class="sxs-lookup"><span data-stu-id="1b477-114">Some properties on message objects have special semantics for client applications with respect to the **SaveChanges** method, as follows:</span></span> 
  
- <span data-ttu-id="1b477-115">Algunas propiedades deberían ser de lectura y escritura antes de llamar a **SaveChanges**, pero después solo de lectura.</span><span class="sxs-lookup"><span data-stu-id="1b477-115">Some properties should be read/write before **SaveChanges** is called, but read-only afterward.</span></span> <span data-ttu-id="1b477-116">Por ejemplo, **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) se establece inicialmente en la aplicación cliente que crea el mensaje (y por lo tanto es de lectura y escritura), pero no pueden cambiarse tras la primera llamada a **SaveChanges**.</span><span class="sxs-lookup"><span data-stu-id="1b477-116">For example, **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) is set initially by the client application that creates the message (and thus is read/write) but cannot be changed after the first call to **SaveChanges**.</span></span>
    
- <span data-ttu-id="1b477-p105">Algunas propiedades tienen relaciones especiales con propiedades de la carpeta en la que están o con métodos **IMAPIFolder**. Por ejemplo, la propiedad **PR_MESSAGE_FLAGS** está relacionada con los marcadores usados en la llamada [IMAPIFolder::CreateMessage](imapifolder-createmessage.md).</span><span class="sxs-lookup"><span data-stu-id="1b477-p105">Some properties have special relations to properties on the folder they are in or to **IMAPIFolder** methods. For example, the **PR_MESSAGE_FLAGS** property is related to the flags used on the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) call.</span></span> 
    
- <span data-ttu-id="1b477-119">Algunas propiedades pueden no estar disponibles hasta que se llame a **SaveChanges** por primera vez.</span><span class="sxs-lookup"><span data-stu-id="1b477-119">Some properties may not be available until **SaveChanges** is called for the first time.</span></span> <span data-ttu-id="1b477-120">Por ejemplo, la propiedad **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) puede no estar disponible hasta que se llame a **SaveChanges**.</span><span class="sxs-lookup"><span data-stu-id="1b477-120">For example, the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property may not be available until **SaveChanges** is called.</span></span> 
    
- <span data-ttu-id="1b477-121">Algunas propiedades pueden tener relaciones especiales con otras propiedades en el objeto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="1b477-121">Some properties can have special relationships to other properties on the message object.</span></span> <span data-ttu-id="1b477-122">Por ejemplo, la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) normalmente se deriva de la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) en los proveedores de almacén de mensajes que admiten los mensajes de formato de texto enriquecido.</span><span class="sxs-lookup"><span data-stu-id="1b477-122">For example, the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property is usually derived from the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property in message store providers that support Rich Text Format messages.</span></span>
    
- <span data-ttu-id="1b477-123">Algunas propiedades son usadas por más de un tipo de objeto relacionado con los almacenes de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1b477-123">Some properties are used by more than one object type related to message stores.</span></span> <span data-ttu-id="1b477-124">Por ejemplo, se requiere la propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) en los objetos mensaje y carpetas, así como en los objetos almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1b477-124">For example, the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property is required on folder and message objects as well as message store objects.</span></span>
    
<span data-ttu-id="1b477-125">Es responsabilidad del proveedor de almacén de mensajes implementar la semántica correcta de estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1b477-125">It is the responsibility of the message store provider to implement the correct semantics for such properties.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1b477-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="1b477-126">See also</span></span>



[<span data-ttu-id="1b477-127">Implementar mensajes en los almacenes de mensajes</span><span class="sxs-lookup"><span data-stu-id="1b477-127">Implementing Messages in Message Stores</span></span>](implementing-messages-in-message-stores.md)

