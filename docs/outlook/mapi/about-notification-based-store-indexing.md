---
title: Acerca Notification-Based indexación de la tienda
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b3685890-117c-9acc-e19f-cf22a349a088
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3dd551dd0c1ea229381e5dd01c5cf6fa04790c30
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409177"
---
# <a name="about-notification-based-store-indexing"></a><span data-ttu-id="9b8aa-103">Acerca Notification-Based indexación de la tienda</span><span class="sxs-lookup"><span data-stu-id="9b8aa-103">About Notification-Based Store Indexing</span></span>

  
  
<span data-ttu-id="9b8aa-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b8aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b8aa-105">Un proveedor de almacén MAPI puede especificar si el controlador de protocolo MAPI rastrea e indiza mensajes en el almacén, o si el almacén envía notificaciones al indizador cuando hay mensajes que se van a indizar.</span><span class="sxs-lookup"><span data-stu-id="9b8aa-105">A MAPI store provider can specify whether the MAPI Protocol Handler crawls and indexes messages in the store, or whether the store sends notifications to the indexer when there are messages to be indexed.</span></span> <span data-ttu-id="9b8aa-106">Este último se conoce como indización basada en notificaciones y un almacén que admite la indización basada en notificaciones es un conocido como almacén de impulsor.</span><span class="sxs-lookup"><span data-stu-id="9b8aa-106">The latter is known as notification-based indexing, and a store that supports notification-based indexing is a known as a pusher store.</span></span>
  
<span data-ttu-id="9b8aa-107">Un proveedor de almacén que admite la indización basada en notificaciones establece la **marca STORE_PUSHER_OK** en la **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** propiedad.</span><span class="sxs-lookup"><span data-stu-id="9b8aa-107">A store provider that supports notification-based indexing sets the **STORE_PUSHER_OK** flag in the **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** property.</span></span> <span data-ttu-id="9b8aa-108">El controlador de protocolo MAPI o un cliente puede obtener la **PR_STORE_SUPPORT_MASK** propiedad para determinar las características del almacén.</span><span class="sxs-lookup"><span data-stu-id="9b8aa-108">The MAPI Protocol Handler or a client can get the **PR_STORE_SUPPORT_MASK** property to determine the characteristics of the store.</span></span> 
  
<span data-ttu-id="9b8aa-109">Siempre que haya datos adjuntos, carpetas o un mensaje que se va a indizar, el proveedor de almacenamiento genera un localizador uniforme de recursos (URL) MAPI que identifica el objeto que se va a indizar y lo envía al indizador.</span><span class="sxs-lookup"><span data-stu-id="9b8aa-109">Whenever there is an attachment, folder, or a message to be indexed, the store provider generates a MAPI Uniform Resource Locator (URL) identifying the object to be indexed and sends it to the indexer.</span></span> <span data-ttu-id="9b8aa-110">Esta dirección URL MAPI está codificada en Unicode y debe identificar de forma única el objeto para el controlador de protocolo MAPI.</span><span class="sxs-lookup"><span data-stu-id="9b8aa-110">This MAPI URL is encoded in Unicode and must uniquely identify the object to the MAPI Protocol Handler.</span></span> <span data-ttu-id="9b8aa-111">Para obtener más información acerca de las direcciones URL MAPI, vea [About MAPI URLs for Notification-Based Indexing](about-mapi-urls-for-notification-based-indexing.md).</span><span class="sxs-lookup"><span data-stu-id="9b8aa-111">For more information about MAPI URLs, see [About MAPI URLs for Notification-Based Indexing](about-mapi-urls-for-notification-based-indexing.md).</span></span>
  
<span data-ttu-id="9b8aa-112">Dado que un indizador no siempre puede indizar todo antes de que se produzca un apagado en un almacén de impulsores, el almacén de impulsores debe conservar lo que se debe insertar.</span><span class="sxs-lookup"><span data-stu-id="9b8aa-112">Because an indexer cannot always index everything before a shutdown occurs in a pusher store, the pusher store must persist what needs to be pushed.</span></span> <span data-ttu-id="9b8aa-113">Cuando un proveedor de almacén envía una notificación sobre un objeto que debe indizarse, especifica el tipo de notificación **fnevIndexing** en el **miembro ulEventType** de la **[estructura NOTIFICATION.](notification.md)**</span><span class="sxs-lookup"><span data-stu-id="9b8aa-113">When a store provider sends a notification about an object that needs to be indexed, it specifies the notification type **fnevIndexing** in the **ulEventType** member of the **[NOTIFICATION](notification.md)** structure.</span></span> <span data-ttu-id="9b8aa-114">El miembro **información** de la estructura **notificación** contiene una estructura **[EXTENDED_NOTIFICATION](extended_notification.md)**.</span><span class="sxs-lookup"><span data-stu-id="9b8aa-114">The **info** member of the **NOTIFICATION** structure contains an **[EXTENDED_NOTIFICATION](extended_notification.md)** structure.</span></span> <span data-ttu-id="9b8aa-115">El proveedor de almacenamiento identifica el proceso en la **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** propiedad.</span><span class="sxs-lookup"><span data-stu-id="9b8aa-115">The store provider identifies the process in the **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** property.</span></span> <span data-ttu-id="9b8aa-116">También identifica el proceso en la INDEX_SEARCH_PUSHER_PROCESS [y](index_search_pusher_process.md) pasa esta información como parte del **miembro pbEventParameters** de la **EXTENDED_NOTIFICATION** estructura.</span><span class="sxs-lookup"><span data-stu-id="9b8aa-116">It also identifies the process in the [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md) structure, and passes this information as part of the **pbEventParameters** member of the **EXTENDED_NOTIFICATION** structure.</span></span> <span data-ttu-id="9b8aa-117">Si el proceso se cierra o se bloquea, el controlador de protocolo MAPI podrá detectarlo inmediatamente y dejar de indizar el almacén de impulsor.</span><span class="sxs-lookup"><span data-stu-id="9b8aa-117">If the process is shut down or crashes, the MAPI Protocol Handler will be able to immediately detect that and stop indexing the pusher store.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9b8aa-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b8aa-118">See also</span></span>



[<span data-ttu-id="9b8aa-119">Información sobre la API del almacén</span><span class="sxs-lookup"><span data-stu-id="9b8aa-119">About the Store API</span></span>](about-the-store-api.md)
  
[<span data-ttu-id="9b8aa-120">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="9b8aa-120">MAPI Constants</span></span>](mapi-constants.md)

