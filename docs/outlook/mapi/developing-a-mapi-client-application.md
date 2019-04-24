---
title: Desarrollo de una aplicación de cliente MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bcb59b08-e6d7-4739-8cb5-e545bd0d478f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7f66d2e4d46519dd186a676a0d0fbb836322893b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316691"
---
# <a name="developing-a-mapi-client-application"></a><span data-ttu-id="155a7-103">Desarrollo de una aplicación de cliente MAPI</span><span class="sxs-lookup"><span data-stu-id="155a7-103">Developing a MAPI Client Application</span></span>

  
  
<span data-ttu-id="155a7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="155a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="155a7-105">Las aplicaciones cliente de MAPI se escriben con la interfaz de cliente MAPI orientada a objetos.</span><span class="sxs-lookup"><span data-stu-id="155a7-105">MAPI client applications are written with the object oriented MAPI client interface.</span></span> <span data-ttu-id="155a7-106">Los clientes MAPI interactúan con uno o varios sistemas de mensajería a través del subsistema MAPI y los proveedores de servicios compatibles con MAPI.</span><span class="sxs-lookup"><span data-stu-id="155a7-106">MAPI clients interact with one or more messaging systems through the MAPI subsystem and MAPI-compliant service providers.</span></span> <span data-ttu-id="155a7-107">Esta interacción puede producirse de muchas maneras diferentes; hay una variedad enorme en las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="155a7-107">This interaction can occur in many different ways; there is an enormous variety in client applications.</span></span> <span data-ttu-id="155a7-108">La mayoría de los clientes son clientes de mensajería, ya sea integrando la mensajería en su conjunto de características establecido o realizando mensajería como característica principal.</span><span class="sxs-lookup"><span data-stu-id="155a7-108">Most clients are messaging clients, either integrating messaging into their established feature set or performing messaging as their primary feature.</span></span> <span data-ttu-id="155a7-109">Otras características que pueden proporcionar los clientes MAPI son la administración de perfiles o la administración de la libreta de direcciones y el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="155a7-109">Other features that MAPI clients might provide include profile administration or address book and message store management.</span></span>
  
<span data-ttu-id="155a7-110">Todos los clientes de mensajería inicializan las bibliotecas MAPI e inician una **sesión** con el subsistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="155a7-110">All messaging clients initialize the MAPI libraries and start a **session** with the MAPI subsystem.</span></span> <span data-ttu-id="155a7-111">Para obtener más información, vea [acceso a objetos mediante la sesión](accessing-objects-by-using-the-session.md).</span><span class="sxs-lookup"><span data-stu-id="155a7-111">For more information, see [Accessing Objects by Using the Session](accessing-objects-by-using-the-session.md).</span></span> <span data-ttu-id="155a7-112">Una vez establecida la sesión, un cliente puede:</span><span class="sxs-lookup"><span data-stu-id="155a7-112">After a session has been established, a client can:</span></span>
  
- <span data-ttu-id="155a7-113">Administrar los mensajes salientes, incluidas las respuestas, los mensajes reenviados y las retransmisiones.</span><span class="sxs-lookup"><span data-stu-id="155a7-113">Handle outgoing messages, including replies, forwarded messages, and retransmissions.</span></span>
    
- <span data-ttu-id="155a7-114">Controlar los mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="155a7-114">Handle incoming messages.</span></span>
    
- <span data-ttu-id="155a7-115">Controlar el almacén de mensajes mediante la apertura de carpetas y mensajes, la creación, modificación, copia y el envío de mensajes, el seguimiento de conversaciones y la búsqueda de una o varias carpetas.</span><span class="sxs-lookup"><span data-stu-id="155a7-115">Handle the message store by opening folders and messages, creating, modifying, copying, and sending messages, tracking conversations, and searching one or more folders.</span></span>
    
- <span data-ttu-id="155a7-116">Controle la libreta de direcciones mediante la creación y modificación de destinatarios, la ubicación de entradas y el recorrido de la jerarquía de contenedores.</span><span class="sxs-lookup"><span data-stu-id="155a7-116">Handle the address book by creating and modifying recipients, locating entries, and traversing the container hierarchy.</span></span>
    
- <span data-ttu-id="155a7-117">Administrar un proveedor de transporte mediante la realización de una reconfiguración, la configuración de las opciones y el orden de transporte y el envío de mensajes a petición.</span><span class="sxs-lookup"><span data-stu-id="155a7-117">Handle a transport provider by performing reconfiguration, setting options and transport order, and sending messages on demand.</span></span>
    
- <span data-ttu-id="155a7-118">Controlar la notificación de eventos.</span><span class="sxs-lookup"><span data-stu-id="155a7-118">Handle event notification.</span></span>
    
- <span data-ttu-id="155a7-119">Controlar los formularios.</span><span class="sxs-lookup"><span data-stu-id="155a7-119">Handle forms.</span></span>
    
- <span data-ttu-id="155a7-120">Administrar perfiles y servicios de mensajes.</span><span class="sxs-lookup"><span data-stu-id="155a7-120">Handle profiles and message services.</span></span>
    
<span data-ttu-id="155a7-121">Use los temas de esta sección para ayudarle a implementar estas tareas básicas y las características específicas que harán que el cliente MAPI sea único.</span><span class="sxs-lookup"><span data-stu-id="155a7-121">Use the topics in this section to help you implement these basic tasks and the specific features that will make your MAPI client unique.</span></span>
  

