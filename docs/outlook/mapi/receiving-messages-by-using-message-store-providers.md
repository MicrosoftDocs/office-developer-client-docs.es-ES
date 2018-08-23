---
title: Recibir mensajes usando proveedores de almacenamiento de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4763951e-ccfd-453e-b99c-5c7d5efb90c2
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 8a5df2e8f50d8de05ec43b03ae5b56887e76d505
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590193"
---
# <a name="receiving-messages-by-using-message-store-providers"></a><span data-ttu-id="ab3c5-103">Recibir mensajes usando proveedores de almacenamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="ab3c5-103">Receiving Messages by Using Message Store Providers</span></span>

  
  
<span data-ttu-id="ab3c5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab3c5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab3c5-105">Los proveedores de almacén de mensajes no es necesario que admitir los envíos de mensajes entrantes (es decir, la compatibilidad con la capacidad de los proveedores de transporte y la cola de MAPI para utilizar el mensaje de proveedor de almacén como punto de entrega de mensajes).</span><span class="sxs-lookup"><span data-stu-id="ab3c5-105">Message store providers do not have to support incoming message submissions (that is, support the ability for transport providers and the MAPI spooler to use the message store provider as a delivery point for messages).</span></span> <span data-ttu-id="ab3c5-106">Sin embargo, si su proveedor de almacén de mensajes no es compatible con los envíos de mensajes entrantes, no puede usarse como el almacén de mensajes predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ab3c5-106">However, if your message store provider does not support incoming message submissions, it cannot be used as the default message store.</span></span>
  
<span data-ttu-id="ab3c5-107">Para admitir los envíos de mensajes entrantes, su proveedor de almacén de mensajes debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="ab3c5-107">To support incoming message submissions, your message store provider must do the following:</span></span>
  
- <span data-ttu-id="ab3c5-108">Admite los métodos [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) y [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) para que las aplicaciones cliente pueden encontrar los mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="ab3c5-108">Support the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) and [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) methods so client applications can find incoming messages.</span></span> 
    
- <span data-ttu-id="ab3c5-109">Admite el método [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) para que la cola MAPI puede informar al proveedor de almacenamiento de mensaje que ha llegado un mensaje nuevo.</span><span class="sxs-lookup"><span data-stu-id="ab3c5-109">Support the [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method so that the MAPI spooler can inform the message store provider that a new message has arrived.</span></span> 
    
- <span data-ttu-id="ab3c5-110">Implementar notificaciones de modo que los clientes pueden registrar para la notificación de mensaje nuevo.</span><span class="sxs-lookup"><span data-stu-id="ab3c5-110">Implement notifications so that clients can register for new message notification.</span></span> <span data-ttu-id="ab3c5-111">Las notificaciones son opcionales, pero su proveedor debe implementarlos.</span><span class="sxs-lookup"><span data-stu-id="ab3c5-111">Notifications are optional, but your provider should implement them.</span></span>
    
<span data-ttu-id="ab3c5-112">La secuencia de llamadas a métodos que se produce cuando se entrega un mensaje entrante a un almacén de mensajes es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="ab3c5-112">The sequence of method calls that occurs when an incoming message is delivered to a message store is as follows:</span></span>
  
1. <span data-ttu-id="ab3c5-113">La cola MAPI llama a [IMsgStore::OpenEntry](imsgstore-openentry.md) con la [propiedad EntryID](entryid.md) de bandeja de entrada para obtener una interfaz [IMAPIFolder](imapifolderimapicontainer.md) .</span><span class="sxs-lookup"><span data-stu-id="ab3c5-113">The MAPI spooler calls [IMsgStore::OpenEntry](imsgstore-openentry.md) with the Inbox [EntryID](entryid.md) to get an [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> 
    
2. <span data-ttu-id="ab3c5-114">La cola MAPI llama a [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) para obtener un nuevo objeto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="ab3c5-114">The MAPI spooler calls [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to get a new message object.</span></span> 
    
3. <span data-ttu-id="ab3c5-115">La cola MAPI pasa el objeto de mensaje para el proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="ab3c5-115">The MAPI spooler passes the message object to the transport provider.</span></span>
    
4. <span data-ttu-id="ab3c5-116">El proveedor de transporte se rellena en las propiedades del mensaje con datos desde el sistema de mensajería subyacente y llama al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) del objeto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="ab3c5-116">The transport provider fills in the message's properties with data from the underlying messaging system and calls the message object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
    
5. <span data-ttu-id="ab3c5-117">El proveedor de almacén de mensajes utiliza su método de notificación para informar a los clientes registrados que ha llegado un mensaje nuevo.</span><span class="sxs-lookup"><span data-stu-id="ab3c5-117">The message store provider uses its notification method to inform registered clients that a new message has arrived.</span></span>
    
6. <span data-ttu-id="ab3c5-118">La cola MAPI llama (método) [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ab3c5-118">The MAPI spooler calls the message store's [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="ab3c5-119">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="ab3c5-119">See also</span></span>



[<span data-ttu-id="ab3c5-120">Caracter�sticas de almac�n de mensajes</span><span class="sxs-lookup"><span data-stu-id="ab3c5-120">Message Store Features</span></span>](message-store-features.md)

