---
title: Creaci�n y almacenamiento de mensajes en los almacenes de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc74b31c-d7ed-4fcf-9535-a2f9222901b7
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 32cfae36fb519654c1fb92d2f3b688c966f9288f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816616"
---
# <a name="creating-and-storing-messages-in-message-stores"></a><span data-ttu-id="47d48-103">Creaci�n y almacenamiento de mensajes en los almacenes de mensajes</span><span class="sxs-lookup"><span data-stu-id="47d48-103">Creating and Storing Messages in Message Stores</span></span>

  
  
<span data-ttu-id="47d48-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="47d48-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="47d48-p101">C�mo el proveedor de almac�n de mensajes se crea y almacena los mensajes en el mecanismo de almacenamiento subyacente depende en gran medida el mecanismo de almacenamiento subyacente propio. En general, s�lo necesita escribir c�digo para conservar las propiedades de un mensaje y sus valores.</span><span class="sxs-lookup"><span data-stu-id="47d48-p101">How your message store provider creates and stores messages in the underlying storage mechanism depends heavily on the underlying storage mechanism itself. In general, you need only to write code to preserve the properties of a message and their values.</span></span>
  
<span data-ttu-id="47d48-p102">Cuando el mensaje Almac�n proveedor crea un nuevo mensaje, el proveedor se necesita para crear el mensaje con las propiedades necesarias para los mensajes. Una lista de estas propiedades se puede encontrar en la documentaci�n para el [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) interfaz. A continuaci�n, las aplicaciones cliente agregan las propiedades adicionales con los m�todos de [IMAPIProp](imapipropiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="47d48-p102">When the message store provider creates a new message, the provider needs to create the message with the required properties for messages. A list of these properties can be found in the documentation for the [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) interface. After that, client applications add any additional properties with [IMAPIProp](imapipropiunknown.md) methods.</span></span> 
  
<span data-ttu-id="47d48-110">Cuando el mensaje almac�n de proveedor guarda un mensaje en el mecanismo de almacenamiento subyacente, el proveedor debe recorrer en iteraci�n las propiedades del mensaje y guardarlos en el mecanismo de almacenamiento subyacente que pueden totalmente recuperarse si m�s adelante se abre el mensaje.</span><span class="sxs-lookup"><span data-stu-id="47d48-110">When the message store provider saves a message to the underlying storage mechanism, the provider needs to iterate over the message's properties, and save them to the underlying storage mechanism such that they can be fully recovered if the message is later opened.</span></span>
  
<span data-ttu-id="47d48-p103">MAPI requiere que se negocian las propiedades en las interfaces de [IMessage](imessageimapiprop.md) , lo que significa que los cambios realizados en ellos no se convierten en permanentes hasta que se llama al m�todo de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) en el objeto de mensaje. El proveedor de almacenamiento de mensajes es responsable de implementar este comportamiento. Normalmente esto no es dif�cil; significa simplemente mantiene las propiedades en la memoria mientras se est�n modificando y confirmar el mecanismo de almacenamiento subyacente cuando se llama a **SaveChanges**.</span><span class="sxs-lookup"><span data-stu-id="47d48-p103">MAPI requires that the properties on [IMessage](imessageimapiprop.md) interfaces are transacted, meaning that changes made to them do not become permanent until the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is called on the message object. The message store provider is responsible for implementing this behavior. Usually this is not difficult; it simply means holding properties in memory while they are being modified and committing them to the underlying storage mechanism when **SaveChanges** is called.</span></span> 
  
<span data-ttu-id="47d48-114">Algunas propiedades de los objetos de mensaje tienen una sem�ntica especial para las aplicaciones de cliente en relaci�n con el m�todo **SaveChanges**, como se indica a continuaci�n:</span><span class="sxs-lookup"><span data-stu-id="47d48-114">Some properties on message objects have special semantics for client applications with respect to the **SaveChanges** method, as follows:</span></span> 
  
- <span data-ttu-id="47d48-115">Algunas propiedades deben ser lectura y escritura antes de **SaveChanges** se llama, pero s�lo lectura posteriormente.</span><span class="sxs-lookup"><span data-stu-id="47d48-115">Some properties should be read/write before **SaveChanges** is called, but read-only afterward.</span></span> <span data-ttu-id="47d48-116">Por ejemplo, **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) se establece inicialmente en la aplicación cliente que crea el mensaje (y, por tanto, es de lectura y escritura), pero no pueden cambiarse tras la primera llamada a **SaveChanges**.</span><span class="sxs-lookup"><span data-stu-id="47d48-116">For example, **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) is set initially by the client application that creates the message (and thus is read/write) but cannot be changed after the first call to **SaveChanges**.</span></span>
    
- <span data-ttu-id="47d48-p105">Algunas propiedades tienen relaciones especiales a las propiedades en la carpeta que se encuentran en o a los m�todos de **IMAPIFolder**. Por ejemplo, la propiedad **PR_MESSAGE_FLAGS** est� relacionada con los indicadores utilizados en la llamada de [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="47d48-p105">Some properties have special relations to properties on the folder they are in or to **IMAPIFolder** methods. For example, the **PR_MESSAGE_FLAGS** property is related to the flags used on the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) call.</span></span> 
    
- <span data-ttu-id="47d48-119">Algunas propiedades no est�n disponibles hasta que se llama **SaveChanges** por primera vez.</span><span class="sxs-lookup"><span data-stu-id="47d48-119">Some properties may not be available until **SaveChanges** is called for the first time.</span></span> <span data-ttu-id="47d48-120">Por ejemplo, la propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) es posible que no estén disponible hasta que se llama **SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="47d48-120">For example, the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property may not be available until **SaveChanges** is called.</span></span> 
    
- <span data-ttu-id="47d48-121">Algunas propiedades pueden tener relaciones especiales a otras propiedades en el objeto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="47d48-121">Some properties can have special relationships to other properties on the message object.</span></span> <span data-ttu-id="47d48-122">Por ejemplo, la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) normalmente se deriva de la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) en los proveedores de almacén de mensajes que admiten los mensajes de formato de texto enriquecido.</span><span class="sxs-lookup"><span data-stu-id="47d48-122">For example, the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property is usually derived from the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property in message store providers that support Rich Text Format messages.</span></span>
    
- <span data-ttu-id="47d48-123">Algunas propiedades se utilizan por m�s de un tipo de objeto relacionados con los almacenes de mensajes.</span><span class="sxs-lookup"><span data-stu-id="47d48-123">Some properties are used by more than one object type related to message stores.</span></span> <span data-ttu-id="47d48-124">Por ejemplo, se requiere la propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) en la carpeta y el mensaje objetos, así como mensaje almacenar objetos.</span><span class="sxs-lookup"><span data-stu-id="47d48-124">For example, the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property is required on folder and message objects as well as message store objects.</span></span>
    
<span data-ttu-id="47d48-125">Es responsabilidad del proveedor de almacenamiento de mensajes para implementar la sem�ntica correcta para esas propiedades.</span><span class="sxs-lookup"><span data-stu-id="47d48-125">It is the responsibility of the message store provider to implement the correct semantics for such properties.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="47d48-126">Vea tambi�n</span><span class="sxs-lookup"><span data-stu-id="47d48-126">See also</span></span>



[<span data-ttu-id="47d48-127">Implementaci�n de los mensajes en los almacenes de mensajes</span><span class="sxs-lookup"><span data-stu-id="47d48-127">Implementing Messages in Message Stores</span></span>](implementing-messages-in-message-stores.md)

