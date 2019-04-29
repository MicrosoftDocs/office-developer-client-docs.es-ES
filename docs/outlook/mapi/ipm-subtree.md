---
title: Subárbol IPM
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b5fc6084-722d-44e8-8637-f4160a4fb19b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 92c7a09d9d608ac31920d49b20f78bedd26f5fcd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421224"
---
# <a name="ipm-subtree"></a><span data-ttu-id="0d093-103">Subárbol IPM</span><span class="sxs-lookup"><span data-stu-id="0d093-103">IPM Subtree</span></span>

  
  
<span data-ttu-id="0d093-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d093-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d093-105">MAPI crea un árbol de carpetas debajo de la carpeta raíz de un almacén de mensajes para todos los clientes que envían y reciben mensajes de los destinatarios humanos, no de los equipos.</span><span class="sxs-lookup"><span data-stu-id="0d093-105">MAPI creates a tree of folders beneath the root folder of a message store for all clients that send messages to and receive messages from human, rather than computer, recipients.</span></span> <span data-ttu-id="0d093-106">Los mensajes intercambiados entre destinatarios humanos se denominan mensajes interpersonales y este árbol se conoce como mensaje interpersonal, o subárbol IPM.</span><span class="sxs-lookup"><span data-stu-id="0d093-106">Messages exchanged between human recipients are known as interpersonal messages, and this tree is known as the interpersonal message, or IPM, subtree.</span></span> 
  
<span data-ttu-id="0d093-107">Un subárbol IPM para un almacén de entrega consta de al menos las siguientes carpetas:</span><span class="sxs-lookup"><span data-stu-id="0d093-107">An IPM subtree for a delivery store consists of at least the following folders:</span></span>
  
- <span data-ttu-id="0d093-108">Bandeja de entrada</span><span class="sxs-lookup"><span data-stu-id="0d093-108">Inbox</span></span>
    
- <span data-ttu-id="0d093-109">Bandeja de salida</span><span class="sxs-lookup"><span data-stu-id="0d093-109">Outbox</span></span>
    
- <span data-ttu-id="0d093-110">Elementos enviados</span><span class="sxs-lookup"><span data-stu-id="0d093-110">Sent Items</span></span>
    
- <span data-ttu-id="0d093-111">Elementos eliminados</span><span class="sxs-lookup"><span data-stu-id="0d093-111">Deleted Items</span></span>
    
<span data-ttu-id="0d093-112">Estos son los nombres y los roles predeterminados de cada una de estas carpetas; un cliente puede especificar sus propios nombres si los nombres predeterminados no son apropiados.</span><span class="sxs-lookup"><span data-stu-id="0d093-112">These are the default names and roles for each of these folders; a client can specify its own names if the default names are not appropriate.</span></span> <span data-ttu-id="0d093-113">MAPI asigna nombres y asociaciones predeterminados para estas carpetas para evitar que los mensajes desaparezcan de forma inadvertida si un cliente no establece carpetas de recepción para los mensajes.</span><span class="sxs-lookup"><span data-stu-id="0d093-113">MAPI assigns default names and associations for these folders to keep messages from inadvertently disappearing if a client neglects to establish receiving folders for messages.</span></span> 
  
<span data-ttu-id="0d093-114">En un contexto de Microsoft Office Outlook, un subárbol IPM consta de carpetas predeterminadas adicionales para calendario, contactos, tareas, notas y diario.</span><span class="sxs-lookup"><span data-stu-id="0d093-114">In a Microsoft Office Outlook context, an IPM subtree consists of additional default folders for Calendar, Contacts, Tasks, Notes, and Journal.</span></span>
  
<span data-ttu-id="0d093-115">Normalmente, la bandeja de entrada retiene los mensajes entrantes y la bandeja de salida retiene los mensajes salientes (es decir, mensajes en espera de enviarse).</span><span class="sxs-lookup"><span data-stu-id="0d093-115">The Inbox typically holds incoming messages, and the Outbox holds outgoing messages (that is, messages waiting to be sent).</span></span> <span data-ttu-id="0d093-116">La carpeta elementos enviados contiene una copia de cada mensaje enviado si el cliente ha establecido la propiedad **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) en el identificador de entrada de esta carpeta.</span><span class="sxs-lookup"><span data-stu-id="0d093-116">The Sent Items folder holds a copy of each sent message if the client has set the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property to the entry identifier of this folder.</span></span> <span data-ttu-id="0d093-117">La carpeta elementos eliminados contiene mensajes marcados para su eliminación.</span><span class="sxs-lookup"><span data-stu-id="0d093-117">The Deleted Items folder contains messages marked for removal.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0d093-118">Ver también</span><span class="sxs-lookup"><span data-stu-id="0d093-118">See also</span></span>



[<span data-ttu-id="0d093-119">Carpetas de MAPI</span><span class="sxs-lookup"><span data-stu-id="0d093-119">MAPI Folders</span></span>](mapi-folders.md)

