---
title: Implementaci�n de los mensajes en los almacenes de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: df5003d5-cbfe-40b2-a481-e2e11dce4b3e
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 1d68a5258739a8952df97ddceb07ebe6d9c8d2d7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568136"
---
# <a name="implementing-messages-in-message-stores"></a><span data-ttu-id="66ed1-103">Implementaci�n de los mensajes en los almacenes de mensajes</span><span class="sxs-lookup"><span data-stu-id="66ed1-103">Implementing Messages in Message Stores</span></span>

  
  
<span data-ttu-id="66ed1-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66ed1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66ed1-p101">The [IMessage: IMAPIProp](imessageimapiprop.md) interface is similar to the [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) interface in that both interfaces derive from the [IMAPIProp: IUnknown](imapipropiunknown.md) interface. Clients use the **IMAPIProp** methods to access the contents of a message. The **IMessage** interface supplies additional methods for manipulating messages (for example, adding attachments or modifying the recipients of a message). The methods in the **IMessage** interface modify attributes of messages that are not stored directly in the message's properties.</span><span class="sxs-lookup"><span data-stu-id="66ed1-p101">The [IMessage : IMAPIProp](imessageimapiprop.md) interface is similar to the [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) interface in that both interfaces derive from the [IMAPIProp : IUnknown](imapipropiunknown.md) interface. Clients use the **IMAPIProp** methods to access the contents of a message. The **IMessage** interface supplies additional methods for manipulating messages (for example, adding attachments or modifying the recipients of a message). The methods in the **IMessage** interface modify attributes of messages that are not stored directly in the message's properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="66ed1-109">Vea tambi�n</span><span class="sxs-lookup"><span data-stu-id="66ed1-109">See also</span></span>



[<span data-ttu-id="66ed1-110">Caracter�sticas de almac�n de mensajes</span><span class="sxs-lookup"><span data-stu-id="66ed1-110">Message Store Features</span></span>](message-store-features.md)

