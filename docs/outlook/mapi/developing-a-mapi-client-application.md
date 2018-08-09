---
title: Desarrollar una aplicación de cliente MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bcb59b08-e6d7-4739-8cb5-e545bd0d478f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 42558fcc3d94b108c0dabb92d62f7c61fdf3039f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816666"
---
# <a name="developing-a-mapi-client-application"></a><span data-ttu-id="44bc7-103">Desarrollar una aplicación de cliente MAPI</span><span class="sxs-lookup"><span data-stu-id="44bc7-103">Developing a MAPI Client Application</span></span>

  
  
<span data-ttu-id="44bc7-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="44bc7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="44bc7-105">Las aplicaciones cliente MAPI se escriben con la interfaz de cliente MAPI orientado a objetos.</span><span class="sxs-lookup"><span data-stu-id="44bc7-105">MAPI client applications are written with the object oriented MAPI client interface.</span></span> <span data-ttu-id="44bc7-106">Los clientes MAPI interactúan con uno o varios sistemas de mensajería a través de los proveedores de servicio compatible con MAPI y el subsistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="44bc7-106">MAPI clients interact with one or more messaging systems through the MAPI subsystem and MAPI-compliant service providers.</span></span> <span data-ttu-id="44bc7-107">Esta interacción puede producirse de muchas maneras diferentes; hay una enorme diversidad en aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="44bc7-107">This interaction can occur in many different ways; there is an enormous variety in client applications.</span></span> <span data-ttu-id="44bc7-108">La mayoría de los clientes son clientes, ya sea la integración de mensajería en su conjunto de características establecida o realización de mensajería como su característica principal de mensajería.</span><span class="sxs-lookup"><span data-stu-id="44bc7-108">Most clients are messaging clients, either integrating messaging into their established feature set or performing messaging as their primary feature.</span></span> <span data-ttu-id="44bc7-109">Otras características que es posible que proporcionan los clientes MAPI son la administración de perfiles o mensaje y la libreta de direcciones del almacén de administración.</span><span class="sxs-lookup"><span data-stu-id="44bc7-109">Other features that MAPI clients might provide include profile administration or address book and message store management.</span></span>
  
<span data-ttu-id="44bc7-110">Todos los clientes de mensajería inicialización las bibliotecas de MAPI e iniciar una **sesión** con el subsistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="44bc7-110">All messaging clients initialize the MAPI libraries and start a **session** with the MAPI subsystem.</span></span> <span data-ttu-id="44bc7-111">Para obtener más información, vea [Obtener acceso a objetos mediante el uso de la sesión](accessing-objects-by-using-the-session.md).</span><span class="sxs-lookup"><span data-stu-id="44bc7-111">For more information, see [Accessing Objects by Using the Session](accessing-objects-by-using-the-session.md).</span></span> <span data-ttu-id="44bc7-112">Después de que se ha establecido una sesión, un cliente puede:</span><span class="sxs-lookup"><span data-stu-id="44bc7-112">After a session has been established, a client can:</span></span>
  
- <span data-ttu-id="44bc7-113">Controlar los mensajes salientes, incluidas las respuestas, reenviado mensajes y retransmisiones.</span><span class="sxs-lookup"><span data-stu-id="44bc7-113">Handle outgoing messages, including replies, forwarded messages, and retransmissions.</span></span>
    
- <span data-ttu-id="44bc7-114">Administrar los mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="44bc7-114">Handle incoming messages.</span></span>
    
- <span data-ttu-id="44bc7-115">Controlar el almacén de mensajes por abrir carpetas y mensajes, crear, modificar, copiar y envío de mensajes, las conversaciones de seguimiento y una o varias carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="44bc7-115">Handle the message store by opening folders and messages, creating, modifying, copying, and sending messages, tracking conversations, and searching one or more folders.</span></span>
    
- <span data-ttu-id="44bc7-116">Controlar la libreta de direcciones mediante la creación y modificación de los destinatarios, buscar las entradas y atravesar la jerarquía de contenedor.</span><span class="sxs-lookup"><span data-stu-id="44bc7-116">Handle the address book by creating and modifying recipients, locating entries, and traversing the container hierarchy.</span></span>
    
- <span data-ttu-id="44bc7-117">Controlan un proveedor de transporte mediante la realización de reconfiguración, establecer el orden de las opciones y el transporte y enviar mensajes a petición.</span><span class="sxs-lookup"><span data-stu-id="44bc7-117">Handle a transport provider by performing reconfiguration, setting options and transport order, and sending messages on demand.</span></span>
    
- <span data-ttu-id="44bc7-118">Controlar la notificación de evento.</span><span class="sxs-lookup"><span data-stu-id="44bc7-118">Handle event notification.</span></span>
    
- <span data-ttu-id="44bc7-119">Administrar formularios.</span><span class="sxs-lookup"><span data-stu-id="44bc7-119">Handle forms.</span></span>
    
- <span data-ttu-id="44bc7-120">Administrar perfiles y servicios de mensajes.</span><span class="sxs-lookup"><span data-stu-id="44bc7-120">Handle profiles and message services.</span></span>
    
<span data-ttu-id="44bc7-121">Utilice los temas de esta sección para ayudarle a implementar estas tareas básicas y las características específicas que harán que el cliente MAPI único.</span><span class="sxs-lookup"><span data-stu-id="44bc7-121">Use the topics in this section to help you implement these basic tasks and the specific features that will make your MAPI client unique.</span></span>
  

