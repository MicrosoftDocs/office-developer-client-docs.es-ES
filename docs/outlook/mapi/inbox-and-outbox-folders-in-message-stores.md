---
title: Bandejas de entrada y salida en los almacenes de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8e4ce129-137d-4618-80a6-88781a578d01
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 95a2b7b9bac11404817fb6848d58c45251c141f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414245"
---
# <a name="inbox-and-outbox-folders-in-message-stores"></a><span data-ttu-id="37aea-103">Bandejas de entrada y salida en los almacenes de mensajes</span><span class="sxs-lookup"><span data-stu-id="37aea-103">Inbox and Outbox Folders in Message Stores</span></span>

  
  
<span data-ttu-id="37aea-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37aea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37aea-p101">Para ser el almacén de mensajes predeterminado, el proveedor de almacén de mensajes debe implementar las carpetas Bandeja de entrada y Bandeja de salida. Normalmente se almacenan en el subárbol IPM de un almacén de mensajes. Estas carpetas tienen de especial el estar designadas como las carpetas a las que se entregan y desde las que se envían los mensajes, pero no necesitan ninguna funcionalidad especial. El envío y la recepción de mensajes ocurre por medio de secuencias de llamada definidas entre las aplicaciones cliente, la cola MAPI y el proveedor de almacén de mensajes. Las carpetas Bandeja de entrada y Bandeja de salida son simplemente carpetas que sirven para contener mensajes durante esas secuencias de llamada. Lo importante no es que las carpetas sean especiales, ni siquiera el que se denominen Bandeja de entrada y Bandeja de salida; lo importante es que el proveedor de almacén de mensajes las use como parte de su soporte para el envío y la recepción de mensajes.</span><span class="sxs-lookup"><span data-stu-id="37aea-p101">To be the default message store, a message store provider must implement Inbox and Outbox folders. They are typically stored in the IPM subtree of a message store. These folders are special in that they are designated as the folders that messages are delivered to and sent from, but no special functionality is required of them. Sending and receiving messages happens by way of defined call sequences between client applications, the MAPI spooler, and the message store provider. The Inbox and Outbox folders are simply folders that are used to hold messages during those call sequences. The important point is not that the folders are special, or even that they are named Inbox and Outbox; the important point is that the message store provider uses them as part of its support for sending and receiving messages.</span></span>
  
<span data-ttu-id="37aea-p102">Para permitir la recepción de mensajes, el proveedor de almacén de mensajes debe implementar los métodos [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) y [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md). Para más información, consulte [Recibir mensajes usando proveedores de almacenamiento de mensajes](receiving-messages-by-using-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="37aea-p102">To support receiving messages, the message store provider must implement the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) and [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) methods. For more information, see [Receiving Messages by Using Message Store Providers](receiving-messages-by-using-message-store-providers.md).</span></span>
  
<span data-ttu-id="37aea-p103">Para permitir el envío de mensajes, el proveedor de almacén de mensajes debe admitir el método [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md), además de los demás métodos usados por la cola MAPI durante el proceso de envío de mensajes. La cola de salida de un almacén de mensajes no necesita corresponder a una carpeta real del árbol de carpetas del almacén de mensajes. Pero es habitual que los proveedores de almacén de mensajes muestren el contenido de la cola de mensajes salientes en la carpeta Bandeja de salida, si esta existe. De esta forma, las aplicaciones cliente tienen una manera conveniente de indicar el estado de los mensajes que ha enviado el usuario, porque se puede mostrar una carpeta Bandeja de salida junto con las demás carpetas del almacén de mensajes. Para más información, consulte [Enviar mensajes usando proveedores de almacenamiento de mensajes](sending-messages-by-using-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="37aea-p103">To support sending messages, the message store provider must support the [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) method, in addition to the other methods used by the MAPI spooler during the message sending process. A message store's outgoing queue does not have to correspond to an actual folder anywhere in the message store's folder tree. However, it is customary for a message store provider to show the contents of the outgoing message queue in the Outbox folder, if there is one. Doing so gives client applications a convenient way to indicate the status of messages that the user has sent, because an Outbox folder can be displayed along with all the other folders in a message store. For more information, see [Sending Messages by Using Message Store Providers](sending-messages-by-using-message-store-providers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="37aea-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="37aea-118">See also</span></span>



[<span data-ttu-id="37aea-119">Implementar carpetas en los almacenes de mensajes</span><span class="sxs-lookup"><span data-stu-id="37aea-119">Implementing Folders in Message Stores</span></span>](implementing-folders-in-message-stores.md)

