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
ms.openlocfilehash: 4f8bc2a5268d220c17a59148f8b8ba1d320d225b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279794"
---
# <a name="objects-and-the-mapi-architecture"></a><span data-ttu-id="c9b41-103">Objetos y la arquitectura MAPI</span><span class="sxs-lookup"><span data-stu-id="c9b41-103">Objects and the MAPI architecture</span></span>

<span data-ttu-id="c9b41-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9b41-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9b41-105">Todos los objetos que define MAPI están en una o más capas de la arquitectura MAPI.</span><span class="sxs-lookup"><span data-stu-id="c9b41-105">All of the objects that MAPI defines fall into one or more layers in the MAPI architecture.</span></span> <span data-ttu-id="c9b41-106">La capa de interfaz de cliente contiene todos los objetos que puede implementar una aplicación cliente, un visor de formularios o un servidor de formulario.</span><span class="sxs-lookup"><span data-stu-id="c9b41-106">The client interface layer contains all the objects that a client application, form viewer, or form server can implement.</span></span> <span data-ttu-id="c9b41-107">La capa de interfaz del proveedor de servicios contiene los objetos que puede implementar un proveedor de servicios de cualquier tipo.</span><span class="sxs-lookup"><span data-stu-id="c9b41-107">The service provider interface layer contains the objects that a service provider of any type can implement.</span></span> <span data-ttu-id="c9b41-108">Esta capa incluye objetos implementados por libretas de direcciones, almacenes de mensajes, proveedores de transporte y bibliotecas de formularios.</span><span class="sxs-lookup"><span data-stu-id="c9b41-108">This layer includes objects implemented by address books, message stores, transport providers, and form libraries.</span></span> <span data-ttu-id="c9b41-109">La capa que representa el subsistema MAPI se coloca entre las capas de interfaz de cliente y proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="c9b41-109">The layer that represents the MAPI subsystem is positioned between the client and service provider interface layers.</span></span> <span data-ttu-id="c9b41-110">La capa MAPI contiene todos los objetos que MAPI implementa para que los clientes o proveedores de servicios los usen.</span><span class="sxs-lookup"><span data-stu-id="c9b41-110">The MAPI layer contains all of the objects that MAPI implements for clients or service providers to use.</span></span> 
  
<span data-ttu-id="c9b41-111">En la siguiente ilustración se muestra dónde encaja cada uno de los objetos MAPI en la arquitectura MAPI.</span><span class="sxs-lookup"><span data-stu-id="c9b41-111">The following illustration shows where each of the MAPI objects fits into the MAPI architecture.</span></span> <span data-ttu-id="c9b41-112">Los objetos se representan con los nombres de sus interfaces derivadas.</span><span class="sxs-lookup"><span data-stu-id="c9b41-112">The objects are represented with the names of their derived interfaces.</span></span> <span data-ttu-id="c9b41-113">Por ejemplo, un objeto receptor de aviso se muestra como [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md), la interfaz que deriva de [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) y que cada objeto receptor de aviso implementa.</span><span class="sxs-lookup"><span data-stu-id="c9b41-113">For example, an advise sink object is shown as [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md), the interface that derives from [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) and that every advise sink object implements.</span></span> <span data-ttu-id="c9b41-114">Varios componentes usan o implementan las interfaces que unen capas.</span><span class="sxs-lookup"><span data-stu-id="c9b41-114">The interfaces that bridge layers are either used or implemented by multiple components.</span></span> <span data-ttu-id="c9b41-115">Aunque la capa MAPI parece separar las capas de cliente y proveedor, lo que implica que toda la comunicación debe fluir a través de MAPI, este no es el caso.</span><span class="sxs-lookup"><span data-stu-id="c9b41-115">Although the MAPI layer appears to separate the client and provider layers, implying that all communication must flow through MAPI, this is not the case.</span></span> <span data-ttu-id="c9b41-116">Los clientes pueden comunicarse directamente con objetos del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="c9b41-116">Clients can and do communicate directly to service provider objects.</span></span> 
  
<span data-ttu-id="c9b41-117">**Capas de objetos en MAPI**</span><span class="sxs-lookup"><span data-stu-id="c9b41-117">**Object layers in MAPI**</span></span>
  
<span data-ttu-id="c9b41-118">![Capas de objetos en capas de]objetos MAPI en(media/amapi_38.gif "MAPI")</span><span class="sxs-lookup"><span data-stu-id="c9b41-118">![Object layers in MAPI](media/amapi_38.gif "Object layers in MAPI")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c9b41-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c9b41-119">See also</span></span>

- [<span data-ttu-id="c9b41-120">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c9b41-120">IMAPIAdviseSink : IUnknown</span></span>](imapiadvisesinkiunknown.md)
- [<span data-ttu-id="c9b41-121">Información general sobre el objeto MAPI y la interfaz</span><span class="sxs-lookup"><span data-stu-id="c9b41-121">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

