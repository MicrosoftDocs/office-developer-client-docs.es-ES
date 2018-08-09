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
ms.openlocfilehash: eebc029d4ed72f355170710061c4d3717ed0aa1e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817871"
---
# <a name="ipm-subtree"></a><span data-ttu-id="58727-103">Subárbol IPM</span><span class="sxs-lookup"><span data-stu-id="58727-103">IPM Subtree</span></span>

  
  
<span data-ttu-id="58727-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="58727-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="58727-105">MAPI, crea un árbol de carpetas bajo la carpeta raíz de un almacén de mensajes para todos los clientes que envían y reciben mensajes desde humana, en lugar de equipo, los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="58727-105">MAPI creates a tree of folders beneath the root folder of a message store for all clients that send messages to and receive messages from human, rather than computer, recipients.</span></span> <span data-ttu-id="58727-106">Mensajes que se intercambian entre destinatarios humanos se conocen como mensajes interpersonales y este árbol se conoce como mensajes interpersonales o IPM, del subárbol.</span><span class="sxs-lookup"><span data-stu-id="58727-106">Messages exchanged between human recipients are known as interpersonal messages, and this tree is known as the interpersonal message, or IPM, subtree.</span></span> 
  
<span data-ttu-id="58727-107">Un subárbol IPM de un almacén de entrega consta de al menos las siguientes carpetas:</span><span class="sxs-lookup"><span data-stu-id="58727-107">An IPM subtree for a delivery store consists of at least the following folders:</span></span>
  
- <span data-ttu-id="58727-108">Bandeja de entrada</span><span class="sxs-lookup"><span data-stu-id="58727-108">Inbox</span></span>
    
- <span data-ttu-id="58727-109">Bandeja de salida</span><span class="sxs-lookup"><span data-stu-id="58727-109">Outbox</span></span>
    
- <span data-ttu-id="58727-110">Elementos enviados</span><span class="sxs-lookup"><span data-stu-id="58727-110">Sent Items</span></span>
    
- <span data-ttu-id="58727-111">Elementos eliminados</span><span class="sxs-lookup"><span data-stu-id="58727-111">Deleted Items</span></span>
    
<span data-ttu-id="58727-112">Estos son los nombres predeterminados y los roles para cada una de estas carpetas; un cliente puede especificar sus propio nombres si los nombres predeterminados no son adecuados.</span><span class="sxs-lookup"><span data-stu-id="58727-112">These are the default names and roles for each of these folders; a client can specify its own names if the default names are not appropriate.</span></span> <span data-ttu-id="58727-113">MAPI asigna nombres predeterminados y asociaciones para estas carpetas mantener los mensajes sin darse cuenta desaparece si un cliente no establecer carpetas receptora para los mensajes.</span><span class="sxs-lookup"><span data-stu-id="58727-113">MAPI assigns default names and associations for these folders to keep messages from inadvertently disappearing if a client neglects to establish receiving folders for messages.</span></span> 
  
<span data-ttu-id="58727-114">En un contexto de Microsoft Office Outlook, un subárbol IPM consta de las carpetas predeterminadas adicionales para el calendario, contactos, tareas, notas y diario.</span><span class="sxs-lookup"><span data-stu-id="58727-114">In a Microsoft Office Outlook context, an IPM subtree consists of additional default folders for Calendar, Contacts, Tasks, Notes, and Journal.</span></span>
  
<span data-ttu-id="58727-115">Normalmente, la Bandeja de entrada contiene los mensajes entrantes y la Bandeja de salida contiene los mensajes salientes (es decir, espera que se envíen mensajes).</span><span class="sxs-lookup"><span data-stu-id="58727-115">The Inbox typically holds incoming messages, and the Outbox holds outgoing messages (that is, messages waiting to be sent).</span></span> <span data-ttu-id="58727-116">La carpeta Elementos enviados contiene una copia de cada mensaje enviado si el cliente ha establecido la propiedad **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) en el identificador de entrada de esta carpeta.</span><span class="sxs-lookup"><span data-stu-id="58727-116">The Sent Items folder holds a copy of each sent message if the client has set the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property to the entry identifier of this folder.</span></span> <span data-ttu-id="58727-117">La carpeta Elementos eliminados contiene mensajes marcados para eliminación.</span><span class="sxs-lookup"><span data-stu-id="58727-117">The Deleted Items folder contains messages marked for removal.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="58727-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="58727-118">See also</span></span>



[<span data-ttu-id="58727-119">Carpetas de MAPI</span><span class="sxs-lookup"><span data-stu-id="58727-119">MAPI Folders</span></span>](mapi-folders.md)

