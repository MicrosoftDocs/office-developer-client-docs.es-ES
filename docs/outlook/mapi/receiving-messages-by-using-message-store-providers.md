---
title: Recibir mensajes con proveedores de almacenamiento de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4763951e-ccfd-453e-b99c-5c7d5efb90c2
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c93a4b56489c2bfb458e2e1cd872073e64d9998a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328451"
---
# <a name="receiving-messages-by-using-message-store-providers"></a><span data-ttu-id="acd07-103">Recibir mensajes con proveedores de almacenamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="acd07-103">Receiving Messages by Using Message Store Providers</span></span>

  
  
<span data-ttu-id="acd07-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="acd07-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="acd07-105">Los proveedores de almacenamiento de mensajes no tienen que admitir envíos de mensajes entrantes (es decir, admiten la capacidad de los proveedores de transporte y la cola MAPI para usar el proveedor de almacén de mensajes como punto de entrega para los mensajes).</span><span class="sxs-lookup"><span data-stu-id="acd07-105">Message store providers do not have to support incoming message submissions (that is, support the ability for transport providers and the MAPI spooler to use the message store provider as a delivery point for messages).</span></span> <span data-ttu-id="acd07-106">Sin embargo, si su proveedor de almacenamiento de mensajes no admite envíos de mensajes entrantes, no se puede usar como almacén de mensajes predeterminado.</span><span class="sxs-lookup"><span data-stu-id="acd07-106">However, if your message store provider does not support incoming message submissions, it cannot be used as the default message store.</span></span>
  
<span data-ttu-id="acd07-107">Para admitir envíos de mensajes entrantes, su proveedor de almacenamiento de mensajes debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="acd07-107">To support incoming message submissions, your message store provider must do the following:</span></span>
  
- <span data-ttu-id="acd07-108">Admitir los métodos [IMsgStore:: GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) y [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md) para que las aplicaciones cliente puedan encontrar los mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="acd07-108">Support the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) and [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) methods so client applications can find incoming messages.</span></span> 
    
- <span data-ttu-id="acd07-109">Admitir el método [IMsgStore:: NotifyNewMail](imsgstore-notifynewmail.md) para que la cola MAPI pueda informar al proveedor de almacenamiento de mensajes de que ha recibido un mensaje nuevo.</span><span class="sxs-lookup"><span data-stu-id="acd07-109">Support the [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method so that the MAPI spooler can inform the message store provider that a new message has arrived.</span></span> 
    
- <span data-ttu-id="acd07-110">Implemente las notificaciones para que los clientes puedan registrarse en la notificación de nuevos mensajes.</span><span class="sxs-lookup"><span data-stu-id="acd07-110">Implement notifications so that clients can register for new message notification.</span></span> <span data-ttu-id="acd07-111">Las notificaciones son opcionales, pero el proveedor debe implementarlas.</span><span class="sxs-lookup"><span data-stu-id="acd07-111">Notifications are optional, but your provider should implement them.</span></span>
    
<span data-ttu-id="acd07-112">La secuencia de llamadas de método que se produce cuando un mensaje entrante se entrega a un almacén de mensajes es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="acd07-112">The sequence of method calls that occurs when an incoming message is delivered to a message store is as follows:</span></span>
  
1. <span data-ttu-id="acd07-113">La cola MAPI llama a [IMsgStore:: OpenEntry](imsgstore-openentry.md) con el [EntryID](entryid.md) de la bandeja de entrada para obtener una interfaz de [IMAPIFolder](imapifolderimapicontainer.md) .</span><span class="sxs-lookup"><span data-stu-id="acd07-113">The MAPI spooler calls [IMsgStore::OpenEntry](imsgstore-openentry.md) with the Inbox [EntryID](entryid.md) to get an [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> 
    
2. <span data-ttu-id="acd07-114">La cola MAPI llama a [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) para obtener un nuevo objeto Message.</span><span class="sxs-lookup"><span data-stu-id="acd07-114">The MAPI spooler calls [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to get a new message object.</span></span> 
    
3. <span data-ttu-id="acd07-115">La cola MAPI pasa el objeto de mensaje al proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="acd07-115">The MAPI spooler passes the message object to the transport provider.</span></span>
    
4. <span data-ttu-id="acd07-116">El proveedor de transporte rellena las propiedades del mensaje con datos del sistema de mensajería subyacente y llama al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) del objeto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="acd07-116">The transport provider fills in the message's properties with data from the underlying messaging system and calls the message object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
    
5. <span data-ttu-id="acd07-117">El proveedor de almacenamiento de mensajes utiliza su método de notificación para informar a los clientes registrados de que ha recibido un nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="acd07-117">The message store provider uses its notification method to inform registered clients that a new message has arrived.</span></span>
    
6. <span data-ttu-id="acd07-118">La cola MAPI llama al método [IMsgStore:: NotifyNewMail](imsgstore-notifynewmail.md) del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="acd07-118">The MAPI spooler calls the message store's [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="acd07-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="acd07-119">See also</span></span>



[<span data-ttu-id="acd07-120">Caracter�sticas de almac�n de mensajes</span><span class="sxs-lookup"><span data-stu-id="acd07-120">Message Store Features</span></span>](message-store-features.md)

