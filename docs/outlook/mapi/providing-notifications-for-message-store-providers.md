---
title: Ofrecer notificaciones para proveedores de almacenamiento de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0e1cdba-ceb6-4a3f-8449-79d1a0ad1adf
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a28e6e6f008517a6b1c2c82dfa391b478963880f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419936"
---
# <a name="providing-notifications-for-message-store-providers"></a><span data-ttu-id="0f660-103">Ofrecer notificaciones para proveedores de almacenamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="0f660-103">Providing Notifications for Message Store Providers</span></span>

  
  
<span data-ttu-id="0f660-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0f660-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0f660-105">Aunque las notificaciones son opcionales, son una parte muy importante de un buen proveedor de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="0f660-105">While notifications are optional, they are a very important part of a good message store provider.</span></span> <span data-ttu-id="0f660-106">Las aplicaciones cliente y la cola MAPI se basan en las notificaciones del proveedor de almacén de mensajes para obtener un buen rendimiento al enviar mensajes salientes o recibir mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="0f660-106">Client applications and the MAPI spooler rely on notifications from the message store provider to get good performance when submitting outgoing messages or receiving incoming messages.</span></span> <span data-ttu-id="0f660-107">Los clientes y la cola MAPI pueden funcionar sin recibir notificaciones del proveedor de almacén de mensajes, pero no podrán informar a los usuarios de los cambios en el almacén de mensajes sin ellos.</span><span class="sxs-lookup"><span data-stu-id="0f660-107">Clients and the MAPI spooler can function without receiving notifications from the message store provider, but they will not be able to inform users of changes in the message store without them.</span></span> <span data-ttu-id="0f660-108">Normalmente, esto significa que los usuarios no podrán ver que ha llegado un mensaje nuevo hasta que el cliente Abra la carpeta de recepción del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="0f660-108">Typically, this means that users will be unable to see that a new message has arrived until their client next opens the message store's receive folder.</span></span>
  
<span data-ttu-id="0f660-109">Los clientes se registran para las notificaciones llamando al método [IMsgStore:: Advise](imsgstore-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="0f660-109">Clients register for notifications by calling the [IMsgStore::Advise](imsgstore-advise.md) method.</span></span> <span data-ttu-id="0f660-110">El cliente pasa una interfaz [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) , una máscara de que indica el tipo de notificaciones que el cliente está interesado en recibir y un **EntryID** que indica qué objeto del mensaje almacenará la **notificación** . se aplica la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0f660-110">The client passes in an [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface, a bitmask that indicates what type of notifications the client is interested in receiving, and an **EntryID** that indicates which object in the message store the **Advise** request applies to.</span></span> <span data-ttu-id="0f660-111">Cuando se producen eventos relevantes en el objeto (por ejemplo, cuando llega un nuevo mensaje a la carpeta de recepción en el almacén de mensajes), el proveedor de almacenamiento de mensajes o el propio objeto deben llamar al método [IMAPIAdviseSink:: método Notify](imapiadvisesink-onnotify.md) para todos los \*\* Objetos IMAPIAdviseSink\*\* que se han registrado para ese tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="0f660-111">When relevant events occur in the object (for example, when a new message arrives in the receive folder in the message store), the message store provider or the object itself should call the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for all of the **IMAPIAdviseSink** objects that have registered for that event type.</span></span> 
  
<span data-ttu-id="0f660-112">Incluso si su proveedor de almacenamiento de mensajes nunca notifica a otros componentes MAPI los cambios en el almacén de mensajes, debe implementar **IMsgStore:: Advise** para devolver MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="0f660-112">Even if your message store provider never notifies other MAPI components of changes in the message store, it should still implement **IMsgStore::Advise** to return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="0f660-113">Esto informa a otros componentes de no esperar notificaciones del proveedor del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="0f660-113">This informs other components not to expect notifications from the message store provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0f660-114">Ver también</span><span class="sxs-lookup"><span data-stu-id="0f660-114">See also</span></span>



[<span data-ttu-id="0f660-115">Caracter�sticas de almac�n de mensajes</span><span class="sxs-lookup"><span data-stu-id="0f660-115">Message Store Features</span></span>](message-store-features.md)

