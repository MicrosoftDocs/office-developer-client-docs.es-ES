---
title: Información sobre la indexación de almacenes basada en notificaciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b3685890-117c-9acc-e19f-cf22a349a088
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 338ae3c3c8d8b4037ab0c7b46916e45cf5a8ded2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816355"
---
# <a name="about-notification-based-store-indexing"></a><span data-ttu-id="b1a91-103">Información sobre la indexación de almacenes basada en notificaciones</span><span class="sxs-lookup"><span data-stu-id="b1a91-103">About Notification-Based Store Indexing</span></span>

  
  
<span data-ttu-id="b1a91-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b1a91-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b1a91-105">Un proveedor de almacén MAPI puede especificar si los mensajes de los rastreos de controlador de protocolo MAPI y los índices en el almacén, o si el almacén envía notificaciones al indizador cuando hay mensajes que se va a indizar.</span><span class="sxs-lookup"><span data-stu-id="b1a91-105">A MAPI store provider can specify whether the MAPI Protocol Handler crawls and indexes messages in the store, or whether the store sends notifications to the indexer when there are messages to be indexed.</span></span> <span data-ttu-id="b1a91-106">Se conoce como indización de notificación y un almacén que admite la indización de notificación es un conocido como un almacén de empuje.</span><span class="sxs-lookup"><span data-stu-id="b1a91-106">The latter is known as notification-based indexing, and a store that supports notification-based indexing is a known as a pusher store.</span></span>
  
<span data-ttu-id="b1a91-107">Un proveedor de almacenamiento que admite la marca **STORE_PUSHER_OK** de conjuntos de indización basada en notificación en la propiedad **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** .</span><span class="sxs-lookup"><span data-stu-id="b1a91-107">A store provider that supports notification-based indexing sets the **STORE_PUSHER_OK** flag in the **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** property.</span></span> <span data-ttu-id="b1a91-108">El controlador de protocolo MAPI o un cliente puede obtener la propiedad **PR_STORE_SUPPORT_MASK** para determinar las características del almacén.</span><span class="sxs-lookup"><span data-stu-id="b1a91-108">The MAPI Protocol Handler or a client can get the **PR_STORE_SUPPORT_MASK** property to determine the characteristics of the store.</span></span> 
  
<span data-ttu-id="b1a91-109">Cada vez que hay un archivo adjunto, carpeta o un mensaje que se va a indizar, el proveedor de almacenamiento genera una MAPI localizador de recursos (URL) que identifica el objeto que se va a indizar y lo envía al indizador.</span><span class="sxs-lookup"><span data-stu-id="b1a91-109">Whenever there is an attachment, folder, or a message to be indexed, the store provider generates a MAPI Uniform Resource Locator (URL) identifying the object to be indexed and sends it to the indexer.</span></span> <span data-ttu-id="b1a91-110">Esta dirección URL de MAPI está codificada en Unicode y debe identificar de forma exclusiva el objeto para el controlador de protocolo MAPI.</span><span class="sxs-lookup"><span data-stu-id="b1a91-110">This MAPI URL is encoded in Unicode and must uniquely identify the object to the MAPI Protocol Handler.</span></span> <span data-ttu-id="b1a91-111">Para obtener más información acerca de las direcciones URL de MAPI, vea [Acerca de direcciones URL MAPI para indización basada en notificaciones](about-mapi-urls-for-notification-based-indexing.md).</span><span class="sxs-lookup"><span data-stu-id="b1a91-111">For more information about MAPI URLs, see [About MAPI URLs for Notification-Based Indexing](about-mapi-urls-for-notification-based-indexing.md).</span></span>
  
<span data-ttu-id="b1a91-112">Debido a que un indizador siempre no puede indizar todo el contenido antes de que se produce un apagado en un almacén de empuje, debe conservar el almacén de empuje lo que necesita que se va a insertar.</span><span class="sxs-lookup"><span data-stu-id="b1a91-112">Because an indexer cannot always index everything before a shutdown occurs in a pusher store, the pusher store must persist what needs to be pushed.</span></span> <span data-ttu-id="b1a91-113">Cuando un proveedor de almacén envía una notificación sobre un objeto que se debe indizar, especifica el tipo de notificación **fnevIndexing** en el miembro **ulEventType** de la estructura de **[notificación](notification.md)** .</span><span class="sxs-lookup"><span data-stu-id="b1a91-113">When a store provider sends a notification about an object that needs to be indexed, it specifies the notification type **fnevIndexing** in the **ulEventType** member of the **[NOTIFICATION](notification.md)** structure.</span></span> <span data-ttu-id="b1a91-114">El miembro de la **información** de la estructura de **notificación** contiene una estructura **[EXTENDED_NOTIFICATION](extended_notification.md)** .</span><span class="sxs-lookup"><span data-stu-id="b1a91-114">The **info** member of the **NOTIFICATION** structure contains an **[EXTENDED_NOTIFICATION](extended_notification.md)** structure.</span></span> <span data-ttu-id="b1a91-115">El proveedor de almacenamiento identifica el proceso en la propiedad **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** .</span><span class="sxs-lookup"><span data-stu-id="b1a91-115">The store provider identifies the process in the **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** property.</span></span> <span data-ttu-id="b1a91-116">También identifica el proceso de la estructura de [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md) y pasa esta información como parte del miembro **pbEventParameters** de la estructura **EXTENDED_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="b1a91-116">It also identifies the process in the [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md) structure, and passes this information as part of the **pbEventParameters** member of the **EXTENDED_NOTIFICATION** structure.</span></span> <span data-ttu-id="b1a91-117">Si el proceso se cierra o se bloquea, el controlador de protocolo MAPI podrán detectar inmediatamente y detener el almacén de empuje de indización.</span><span class="sxs-lookup"><span data-stu-id="b1a91-117">If the process is shut down or crashes, the MAPI Protocol Handler will be able to immediately detect that and stop indexing the pusher store.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b1a91-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="b1a91-118">See also</span></span>



[<span data-ttu-id="b1a91-119">Información sobre la API del almacén</span><span class="sxs-lookup"><span data-stu-id="b1a91-119">About the Store API</span></span>](about-the-store-api.md)
  
[<span data-ttu-id="b1a91-120">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="b1a91-120">MAPI Constants</span></span>](mapi-constants.md)

