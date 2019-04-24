---
title: Nombres de propiedad y conjuntos de propiedades
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
# <a name="property-names-and-property-sets"></a><span data-ttu-id="ccaea-103">Nombres de propiedad y conjuntos de propiedades</span><span class="sxs-lookup"><span data-stu-id="ccaea-103">Property Names and Property Sets</span></span>

  
  
<span data-ttu-id="ccaea-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ccaea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ccaea-105">El nombre de cada propiedad con nombre tiene dos partes:</span><span class="sxs-lookup"><span data-stu-id="ccaea-105">The name of every named property has two parts:</span></span>
  
- <span data-ttu-id="ccaea-106">Identificador único global, o GUID, que especifica un conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="ccaea-106">A globally unique identifier, or GUID, that specifies a property set.</span></span>
    
- <span data-ttu-id="ccaea-107">Una cadena de caracteres Unicode o un valor numérico de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="ccaea-107">A Unicode character string or 32-bit numeric value.</span></span> 
    
<span data-ttu-id="ccaea-108">Los nombres de las propiedades con nombre se describen con una estructura [MAPINAMEID](mapinameid.md) .</span><span class="sxs-lookup"><span data-stu-id="ccaea-108">Names of named properties are described using a [MAPINAMEID](mapinameid.md) structure.</span></span> <span data-ttu-id="ccaea-109">Esta estructura contiene un miembro de conjunto de propiedades, un miembro para especificar el nombre en formato numérico o de cadena, y un miembro para identificar el formato que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="ccaea-109">This structure contains a property set member, a member for specifying the name in either numeric or string format, and a member for identifying which format is used.</span></span> <span data-ttu-id="ccaea-110">Como el conjunto de propiedades forma parte del nombre de la propiedad, no es opcional.</span><span class="sxs-lookup"><span data-stu-id="ccaea-110">Because the property set is part of the property's name, it is not optional.</span></span> <span data-ttu-id="ccaea-111">MAPI ha definido varios conjuntos de propiedades para que los utilicen los clientes y los proveedores de servicios, pero si un conjunto de propiedades existente es inadecuado, se puede definir un nuevo conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="ccaea-111">MAPI has defined several property sets for use by clients and service providers, but if an existing property set is inappropriate, a new property set can be defined.</span></span> <span data-ttu-id="ccaea-112">Los clientes y los proveedores de servicios pueden definir sus propios conjuntos de propiedades llamando a la función [CoCreateGUID](https://msdn.microsoft.com/library/ms688568.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ccaea-112">Clients and service providers can define their own property sets by calling [CoCreateGUID](https://msdn.microsoft.com/library/ms688568.aspx) function.</span></span> <span data-ttu-id="ccaea-113">Por lo general, estos conjuntos de propiedades se crean para aplicaciones cliente personalizadas.</span><span class="sxs-lookup"><span data-stu-id="ccaea-113">Typically these property sets are created for custom client applications.</span></span> 
  
<span data-ttu-id="ccaea-114">Los conjuntos de propiedades de MAPI se representan mediante las siguientes constantes:</span><span class="sxs-lookup"><span data-stu-id="ccaea-114">MAPI's property sets are represented by the following constants:</span></span>
  
<span data-ttu-id="ccaea-115">PS_MAPI</span><span class="sxs-lookup"><span data-stu-id="ccaea-115">PS_MAPI</span></span>
  
<span data-ttu-id="ccaea-116">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="ccaea-116">PS_PUBLIC_STRINGS</span></span>
  
<span data-ttu-id="ccaea-117">PS_ROUTING_EMAIL_ADDRESSES</span><span class="sxs-lookup"><span data-stu-id="ccaea-117">PS_ROUTING_EMAIL_ADDRESSES</span></span>
  
<span data-ttu-id="ccaea-118">PS_ROUTING_ADDRTYPE</span><span class="sxs-lookup"><span data-stu-id="ccaea-118">PS_ROUTING_ADDRTYPE</span></span>
  
<span data-ttu-id="ccaea-119">PS_ROUTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="ccaea-119">PS_ROUTING_SEARCH_KEY</span></span>
  
<span data-ttu-id="ccaea-120">PS_ROUTING_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="ccaea-120">PS_ROUTING_DISPLAY_NAME</span></span>
  
<span data-ttu-id="ccaea-121">PS_ROUTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="ccaea-121">PS_ROUTING_ENTRYID</span></span>
  
<span data-ttu-id="ccaea-122">El conjunto de propiedades PS_MAPI está reservado; lo usan los proveedores de servicios para generar nombres para propiedades con identificadores por debajo del intervalo de propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="ccaea-122">The PS_MAPI property set is reserved; it is used by service providers to generate names for properties with identifiers below the named property range.</span></span> <span data-ttu-id="ccaea-123">Los clientes usan el conjunto de propiedades PS_PUBLIC_STRINGS para las propiedades con nombre de los mensajes IPM.</span><span class="sxs-lookup"><span data-stu-id="ccaea-123">The PS_PUBLIC_STRINGS property set is used by clients for named properties of IPM messages.</span></span> <span data-ttu-id="ccaea-124">Dado que las propiedades con nombre en el conjunto de propiedades PS_PUBLIC_STRINGS aparecen en la interfaz de usuario de un cliente, los mensajes no visibles como los que pertenecen a la clase de mensaje IPC deben evitar crear propiedades con nombre con esta propiedad establecida.</span><span class="sxs-lookup"><span data-stu-id="ccaea-124">Because named properties in the PS_PUBLIC_STRINGS property set appear in a client's user interface, nonvisible messages such as those that belong to the IPC message class should avoid creating named properties with this property set.</span></span> <span data-ttu-id="ccaea-125">En su lugar, deben crear propiedades en el rango específico de clase de mensaje, 0x6800 a 0x7FFF.</span><span class="sxs-lookup"><span data-stu-id="ccaea-125">Instead, they should create properties in the message class-specific range, 0x6800 through 0x7FFF.</span></span>
  
<span data-ttu-id="ccaea-126">Los otros conjuntos de propiedades contienen propiedades con nombre que describen destinatarios que suelen ser miembros de una lista de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="ccaea-126">The other property sets hold named properties describing recipients that are typically members of a routing list.</span></span> <span data-ttu-id="ccaea-127">Al contener el mismo tipo de información que las propiedades que se asocian a las propiedades de la lista de destinatarios, las propiedades de estos conjuntos de propiedades se entienden mediante puertas de enlace para requerir asignación para un sistema de mensajería de destino.</span><span class="sxs-lookup"><span data-stu-id="ccaea-127">Containing the same type of information as the properties that are associated with recipient list properties, properties in these property sets are understood by gateways to require mapping for a target messaging system.</span></span> <span data-ttu-id="ccaea-128">Debido a que hay cinco tipos de información para describir propiedades, MAPI ha definido cinco conjuntos de propiedades diferentes.</span><span class="sxs-lookup"><span data-stu-id="ccaea-128">Because there are five types of information for describing properties, MAPI has defined five different property sets.</span></span> <span data-ttu-id="ccaea-129">Un cliente que envía un mensaje que debe incluir una dirección y un tipo de dirección para los miembros de la lista de enrutamiento asigna una propiedad con nombre para cada miembro de los conjuntos de propiedades PS_ROUTING_EMAIL_ADDRESSES y PS_ROUTING_ADDRTYPE.</span><span class="sxs-lookup"><span data-stu-id="ccaea-129">A client sending a message that must include an address and address type for its routing list members assigns a named property for each member in the PS_ROUTING_EMAIL_ADDRESSES and PS_ROUTING_ADDRTYPE property sets.</span></span> <span data-ttu-id="ccaea-130">Esto garantiza que la dirección y el tipo de dirección sigan siendo viables cuando se envíen a un sistema de mensajería externo.</span><span class="sxs-lookup"><span data-stu-id="ccaea-130">This ensures that the address and address type remain viable when sent to a foreign messaging system.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ccaea-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="ccaea-131">See also</span></span>



[<span data-ttu-id="ccaea-132">Propiedades con nombre MAPI</span><span class="sxs-lookup"><span data-stu-id="ccaea-132">MAPI Named Properties</span></span>](mapi-named-properties.md)

