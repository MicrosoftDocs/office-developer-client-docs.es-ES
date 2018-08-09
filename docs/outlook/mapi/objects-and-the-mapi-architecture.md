---
title: Objetos y la arquitectura MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c3bcbda5-820d-4ef5-bffd-c254eea9dff6
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 0e89c2ad37b700a977962e5e0ff0ca30b9d910e2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818442"
---
# <a name="objects-and-the-mapi-architecture"></a><span data-ttu-id="33749-103">Objetos y la arquitectura MAPI</span><span class="sxs-lookup"><span data-stu-id="33749-103">Objects and the MAPI architecture</span></span>

<span data-ttu-id="33749-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="33749-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="33749-105">Todos los objetos que define MAPI se dividen en una o más capas en la arquitectura de MAPI.</span><span class="sxs-lookup"><span data-stu-id="33749-105">All of the objects that MAPI defines fall into one or more layers in the MAPI architecture.</span></span> <span data-ttu-id="33749-106">La capa de interfaz de cliente contiene todos los objetos que puede implementar una aplicación cliente, el Visor de formulario o el servidor de formulario.</span><span class="sxs-lookup"><span data-stu-id="33749-106">The client interface layer contains all the objects that a client application, form viewer, or form server can implement.</span></span> <span data-ttu-id="33749-107">La capa de interfaz de proveedor de servicio contiene los objetos que puede implementar un proveedor de servicios de cualquier tipo.</span><span class="sxs-lookup"><span data-stu-id="33749-107">The service provider interface layer contains the objects that a service provider of any type can implement.</span></span> <span data-ttu-id="33749-108">Esta capa incluye objetos implementados por libretas de direcciones, almacenes de mensajes, los proveedores de transporte y las bibliotecas de formularios.</span><span class="sxs-lookup"><span data-stu-id="33749-108">This layer includes objects implemented by address books, message stores, transport providers, and form libraries.</span></span> <span data-ttu-id="33749-109">La capa que representa el subsistema MAPI se coloca entre las capas de interfaz de proveedor de cliente y el servicio.</span><span class="sxs-lookup"><span data-stu-id="33749-109">The layer that represents the MAPI subsystem is positioned between the client and service provider interface layers.</span></span> <span data-ttu-id="33749-110">La capa MAPI contiene todos los objetos que implementa MAPI para que los clientes o proveedores de servicios para utilizar.</span><span class="sxs-lookup"><span data-stu-id="33749-110">The MAPI layer contains all of the objects that MAPI implements for clients or service providers to use.</span></span> 
  
<span data-ttu-id="33749-111">La siguiente ilustración se muestra donde cada uno de los objetos MAPI encaja en la arquitectura MAPI.</span><span class="sxs-lookup"><span data-stu-id="33749-111">The following illustration shows where each of the MAPI objects fits into the MAPI architecture.</span></span> <span data-ttu-id="33749-112">Los objetos se representan con los nombres de sus interfaces derivadas.</span><span class="sxs-lookup"><span data-stu-id="33749-112">The objects are represented with the names of their derived interfaces.</span></span> <span data-ttu-id="33749-113">Por ejemplo, se muestra un objeto de receptor advise como [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md), la interfaz que se deriva de [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) y que cada objeto de receptor advise implementa.</span><span class="sxs-lookup"><span data-stu-id="33749-113">For example, an advise sink object is shown as [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md), the interface that derives from [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) and that every advise sink object implements.</span></span> <span data-ttu-id="33749-114">Las interfaces que capas de puente se usa o implementadas por varios componentes.</span><span class="sxs-lookup"><span data-stu-id="33749-114">The interfaces that bridge layers are either used or implemented by multiple components.</span></span> <span data-ttu-id="33749-115">Aunque la capa MAPI aparece separar los niveles de cliente y de proveedor, lo que implica que deben flujo de todas las comunicaciones a través de MAPI, no es el caso.</span><span class="sxs-lookup"><span data-stu-id="33749-115">Although the MAPI layer appears to separate the client and provider layers, implying that all communication must flow through MAPI, this is not the case.</span></span> <span data-ttu-id="33749-116">Los clientes pueden y comunicarse directamente a los objetos de proveedor de servicio.</span><span class="sxs-lookup"><span data-stu-id="33749-116">Clients can and do communicate directly to service provider objects.</span></span> 
  
<span data-ttu-id="33749-117">**Capas de objetos en MAPI**</span><span class="sxs-lookup"><span data-stu-id="33749-117">**Object layers in MAPI**</span></span>
  
<span data-ttu-id="33749-118">![Capas de objetos en MAPI] (media/amapi_38.gif "Capas de objetos en MAPI")</span><span class="sxs-lookup"><span data-stu-id="33749-118">![Object layers in MAPI](media/amapi_38.gif "Object layers in MAPI")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="33749-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="33749-119">See also</span></span>

- [<span data-ttu-id="33749-120">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="33749-120">IMAPIAdviseSink : IUnknown</span></span>](imapiadvisesinkiunknown.md)
- [<span data-ttu-id="33749-121">Objeto MAPI e Introducción a la interfaz</span><span class="sxs-lookup"><span data-stu-id="33749-121">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

