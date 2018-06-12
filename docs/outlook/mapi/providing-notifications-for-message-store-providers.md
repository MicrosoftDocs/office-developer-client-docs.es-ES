---
title: Proporcionar notificaciones para los proveedores de almacén de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0e1cdba-ceb6-4a3f-8449-79d1a0ad1adf
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 3abb4ba67ff5f0cf2284fa9286b6968698877b84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820464"
---
# <a name="providing-notifications-for-message-store-providers"></a><span data-ttu-id="3f0e3-103">Proporcionar notificaciones para los proveedores de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="3f0e3-103">Providing Notifications for Message Store Providers</span></span>

  
  
<span data-ttu-id="3f0e3-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3f0e3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3f0e3-105">Mientras que las notificaciones son opcionales, son una parte muy importante de un proveedor de almacén de mensaje válida.</span><span class="sxs-lookup"><span data-stu-id="3f0e3-105">While notifications are optional, they are a very important part of a good message store provider.</span></span> <span data-ttu-id="3f0e3-106">Las aplicaciones cliente y la cola MAPI se basan en las notificaciones desde el proveedor de almacenamiento de mensajes para obtener un buen rendimiento al enviar los mensajes salientes o recibir mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="3f0e3-106">Client applications and the MAPI spooler rely on notifications from the message store provider to get good performance when submitting outgoing messages or receiving incoming messages.</span></span> <span data-ttu-id="3f0e3-107">Los clientes y la cola MAPI pueden funcionar sin recibir notificaciones desde el proveedor de almacenamiento de mensajes, pero no podrán informar a los usuarios los cambios en el almacén de mensajes sin ellos.</span><span class="sxs-lookup"><span data-stu-id="3f0e3-107">Clients and the MAPI spooler can function without receiving notifications from the message store provider, but they will not be able to inform users of changes in the message store without them.</span></span> <span data-ttu-id="3f0e3-108">Normalmente, esto significa que los usuarios no podrán ver que ha recibido un nuevo mensaje de hasta que su cliente siguiente abre el almacén de mensajes reciben carpeta.</span><span class="sxs-lookup"><span data-stu-id="3f0e3-108">Typically, this means that users will be unable to see that a new message has arrived until their client next opens the message store's receive folder.</span></span>
  
<span data-ttu-id="3f0e3-109">Registro de clientes para las notificaciones llamando al método [IMsgStore::Advise](imsgstore-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="3f0e3-109">Clients register for notifications by calling the [IMsgStore::Advise](imsgstore-advise.md) method.</span></span> <span data-ttu-id="3f0e3-110">El cliente pasa un [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) de la interfaz, una máscara de bits que indica qué tipo de notificaciones en la que el cliente está interesado en recibir, y un **EntryID** que indica qué objeto en el mensaje de almacenar el **Advise** solicitud se aplica a.</span><span class="sxs-lookup"><span data-stu-id="3f0e3-110">The client passes in an [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface, a bitmask that indicates what type of notifications the client is interested in receiving, and an **EntryID** that indicates which object in the message store the **Advise** request applies to.</span></span> <span data-ttu-id="3f0e3-111">Cuando se producen eventos relevantes en el objeto (por ejemplo, cuando llegue un nuevo mensaje en la carpeta de recepción en el almacén de mensajes), el proveedor de almacenamiento de mensaje o el propio objeto debe llamar al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para todas las ** IMAPIAdviseSink** objetos que se hayan registrado para ese tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="3f0e3-111">When relevant events occur in the object (for example, when a new message arrives in the receive folder in the message store), the message store provider or the object itself should call the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for all of the **IMAPIAdviseSink** objects that have registered for that event type.</span></span> 
  
<span data-ttu-id="3f0e3-112">Incluso si el mensaje almacenar proveedor nunca notifica a otros componentes MAPI de cambios realizados en el almacén de mensajes, aún debe implementar **IMsgStore::Advise** para devolver MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="3f0e3-112">Even if your message store provider never notifies other MAPI components of changes in the message store, it should still implement **IMsgStore::Advise** to return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="3f0e3-113">Esto informa a otros componentes para que no espera que el proveedor de almacén de notificaciones desde el mensaje.</span><span class="sxs-lookup"><span data-stu-id="3f0e3-113">This informs other components not to expect notifications from the message store provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3f0e3-114">Ver también</span><span class="sxs-lookup"><span data-stu-id="3f0e3-114">See also</span></span>



[<span data-ttu-id="3f0e3-115">Caracter�sticas de almac�n de mensajes</span><span class="sxs-lookup"><span data-stu-id="3f0e3-115">Message Store Features</span></span>](message-store-features.md)

