---
title: Nombres de propiedades y conjuntos de propiedades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cb216f5c-c965-4372-a15b-82090a410266
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: fa9d6afcaf1b360f37e8c8873c9d1a823fcd4888
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328549"
---
# <a name="property-names-and-property-sets"></a><span data-ttu-id="387f2-103">Nombres de propiedades y conjuntos de propiedades</span><span class="sxs-lookup"><span data-stu-id="387f2-103">Property Names and Property Sets</span></span>

  
  
<span data-ttu-id="387f2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="387f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="387f2-105">El nombre de cada propiedad con nombre tiene dos partes:</span><span class="sxs-lookup"><span data-stu-id="387f2-105">The name of every named property has two parts:</span></span>
  
- <span data-ttu-id="387f2-106">Un identificador único global, o GUID, que especifica un conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="387f2-106">A globally unique identifier, or GUID, that specifies a property set.</span></span>
    
- <span data-ttu-id="387f2-107">Una cadena de caracteres Unicode o un valor numérico de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="387f2-107">A Unicode character string or 32-bit numeric value.</span></span> 
    
<span data-ttu-id="387f2-108">Los nombres de las propiedades con nombre se describen mediante [una estructura MAPINAMEID.](mapinameid.md)</span><span class="sxs-lookup"><span data-stu-id="387f2-108">Names of named properties are described using a [MAPINAMEID](mapinameid.md) structure.</span></span> <span data-ttu-id="387f2-109">Esta estructura contiene un miembro del conjunto de propiedades, un miembro para especificar el nombre en formato numérico o de cadena y un miembro para identificar qué formato se usa.</span><span class="sxs-lookup"><span data-stu-id="387f2-109">This structure contains a property set member, a member for specifying the name in either numeric or string format, and a member for identifying which format is used.</span></span> <span data-ttu-id="387f2-110">Dado que el conjunto de propiedades forma parte del nombre de la propiedad, no es opcional.</span><span class="sxs-lookup"><span data-stu-id="387f2-110">Because the property set is part of the property's name, it is not optional.</span></span> <span data-ttu-id="387f2-111">MAPI ha definido varios conjuntos de propiedades para su uso por parte de clientes y proveedores de servicios, pero si un conjunto de propiedades existente es inadecuado, se puede definir un nuevo conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="387f2-111">MAPI has defined several property sets for use by clients and service providers, but if an existing property set is inappropriate, a new property set can be defined.</span></span> <span data-ttu-id="387f2-112">Los clientes y proveedores de servicios pueden definir sus propios conjuntos de propiedades llamando a [la función CoCreateGUID.](https://msdn.microsoft.com/library/ms688568.aspx)</span><span class="sxs-lookup"><span data-stu-id="387f2-112">Clients and service providers can define their own property sets by calling [CoCreateGUID](https://msdn.microsoft.com/library/ms688568.aspx) function.</span></span> <span data-ttu-id="387f2-113">Normalmente, estos conjuntos de propiedades se crean para aplicaciones cliente personalizadas.</span><span class="sxs-lookup"><span data-stu-id="387f2-113">Typically these property sets are created for custom client applications.</span></span> 
  
<span data-ttu-id="387f2-114">Los conjuntos de propiedades de MAPI se representan mediante las siguientes constantes:</span><span class="sxs-lookup"><span data-stu-id="387f2-114">MAPI's property sets are represented by the following constants:</span></span>
  
<span data-ttu-id="387f2-115">PS_MAPI</span><span class="sxs-lookup"><span data-stu-id="387f2-115">PS_MAPI</span></span>
  
<span data-ttu-id="387f2-116">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="387f2-116">PS_PUBLIC_STRINGS</span></span>
  
<span data-ttu-id="387f2-117">PS_ROUTING_EMAIL_ADDRESSES</span><span class="sxs-lookup"><span data-stu-id="387f2-117">PS_ROUTING_EMAIL_ADDRESSES</span></span>
  
<span data-ttu-id="387f2-118">PS_ROUTING_ADDRTYPE</span><span class="sxs-lookup"><span data-stu-id="387f2-118">PS_ROUTING_ADDRTYPE</span></span>
  
<span data-ttu-id="387f2-119">PS_ROUTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="387f2-119">PS_ROUTING_SEARCH_KEY</span></span>
  
<span data-ttu-id="387f2-120">PS_ROUTING_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="387f2-120">PS_ROUTING_DISPLAY_NAME</span></span>
  
<span data-ttu-id="387f2-121">PS_ROUTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="387f2-121">PS_ROUTING_ENTRYID</span></span>
  
<span data-ttu-id="387f2-122">El PS_MAPI de propiedades está reservado; los proveedores de servicios lo usan para generar nombres para propiedades con identificadores por debajo del intervalo de propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="387f2-122">The PS_MAPI property set is reserved; it is used by service providers to generate names for properties with identifiers below the named property range.</span></span> <span data-ttu-id="387f2-123">El PS_PUBLIC_STRINGS de propiedades es usado por los clientes para las propiedades con nombre de los mensajes IPM.</span><span class="sxs-lookup"><span data-stu-id="387f2-123">The PS_PUBLIC_STRINGS property set is used by clients for named properties of IPM messages.</span></span> <span data-ttu-id="387f2-124">Dado que las propiedades con nombre del conjunto de propiedades PS_PUBLIC_STRINGS aparecen en la interfaz de usuario de un cliente, los mensajes novisibles como los que pertenecen a la clase de mensaje IPC deben evitar crear propiedades con nombre con este conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="387f2-124">Because named properties in the PS_PUBLIC_STRINGS property set appear in a client's user interface, nonvisible messages such as those that belong to the IPC message class should avoid creating named properties with this property set.</span></span> <span data-ttu-id="387f2-125">En su lugar, deben crear propiedades en el intervalo específico de la clase del mensaje, 0x6800 a través de 0x7FFF.</span><span class="sxs-lookup"><span data-stu-id="387f2-125">Instead, they should create properties in the message class-specific range, 0x6800 through 0x7FFF.</span></span>
  
<span data-ttu-id="387f2-126">Los demás conjuntos de propiedades contienen propiedades con nombre que describen los destinatarios que normalmente son miembros de una lista de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="387f2-126">The other property sets hold named properties describing recipients that are typically members of a routing list.</span></span> <span data-ttu-id="387f2-127">Con el mismo tipo de información que las propiedades asociadas con propiedades de lista de destinatarios, las puertas de enlace entienden que las propiedades de estos conjuntos de propiedades requieren la asignación de un sistema de mensajería de destino.</span><span class="sxs-lookup"><span data-stu-id="387f2-127">Containing the same type of information as the properties that are associated with recipient list properties, properties in these property sets are understood by gateways to require mapping for a target messaging system.</span></span> <span data-ttu-id="387f2-128">Dado que hay cinco tipos de información para describir propiedades, MAPI ha definido cinco conjuntos de propiedades diferentes.</span><span class="sxs-lookup"><span data-stu-id="387f2-128">Because there are five types of information for describing properties, MAPI has defined five different property sets.</span></span> <span data-ttu-id="387f2-129">Un cliente que envía un mensaje que debe incluir una dirección y un tipo de dirección para sus miembros de lista de enrutamiento asigna una propiedad con nombre para cada miembro de los conjuntos de propiedades PS_ROUTING_EMAIL_ADDRESSES y PS_ROUTING_ADDRTYPE de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="387f2-129">A client sending a message that must include an address and address type for its routing list members assigns a named property for each member in the PS_ROUTING_EMAIL_ADDRESSES and PS_ROUTING_ADDRTYPE property sets.</span></span> <span data-ttu-id="387f2-130">Esto garantiza que la dirección y el tipo de dirección permanecen viables cuando se envían a un sistema de mensajería externo.</span><span class="sxs-lookup"><span data-stu-id="387f2-130">This ensures that the address and address type remain viable when sent to a foreign messaging system.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="387f2-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="387f2-131">See also</span></span>



[<span data-ttu-id="387f2-132">Propiedades con nombre MAPI</span><span class="sxs-lookup"><span data-stu-id="387f2-132">MAPI Named Properties</span></span>](mapi-named-properties.md)

