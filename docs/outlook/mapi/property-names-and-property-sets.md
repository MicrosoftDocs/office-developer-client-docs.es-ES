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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391660"
---
# <a name="property-names-and-property-sets"></a><span data-ttu-id="64630-103">Nombres de propiedad y conjuntos de propiedades</span><span class="sxs-lookup"><span data-stu-id="64630-103">Property Names and Property Sets</span></span>

  
  
<span data-ttu-id="64630-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64630-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64630-105">El nombre de cada propiedad con nombre consta de dos partes:</span><span class="sxs-lookup"><span data-stu-id="64630-105">The name of every named property has two parts:</span></span>
  
- <span data-ttu-id="64630-106">Un identificador único global o GUID, que especifica un conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="64630-106">A globally unique identifier, or GUID, that specifies a property set.</span></span>
    
- <span data-ttu-id="64630-107">Una cadena de caracteres Unicode o el valor numérico de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="64630-107">A Unicode character string or 32-bit numeric value.</span></span> 
    
<span data-ttu-id="64630-108">Nombres de propiedades con nombre se describen mediante una estructura [MAPINAMEID](mapinameid.md) .</span><span class="sxs-lookup"><span data-stu-id="64630-108">Names of named properties are described using a [MAPINAMEID](mapinameid.md) structure.</span></span> <span data-ttu-id="64630-109">Esta estructura contiene un miembro del grupo de propiedad, un miembro para especificar el nombre de formato numérico o de cadena y un miembro para la identificación de formato que se usa.</span><span class="sxs-lookup"><span data-stu-id="64630-109">This structure contains a property set member, a member for specifying the name in either numeric or string format, and a member for identifying which format is used.</span></span> <span data-ttu-id="64630-110">Dado que el conjunto de propiedades es parte del nombre de la propiedad, no es opcional.</span><span class="sxs-lookup"><span data-stu-id="64630-110">Because the property set is part of the property's name, it is not optional.</span></span> <span data-ttu-id="64630-111">MAPI ha definido varios conjuntos de propiedades para que usen los clientes y proveedores de servicios, pero si un conjunto de propiedades existentes es inadecuado, se puede definir un nuevo conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="64630-111">MAPI has defined several property sets for use by clients and service providers, but if an existing property set is inappropriate, a new property set can be defined.</span></span> <span data-ttu-id="64630-112">Los clientes y proveedores de servicios pueden definir sus propios conjuntos de propiedades mediante una llamada a función [CoCreateGUID](https://msdn.microsoft.com/library/ms688568.aspx) .</span><span class="sxs-lookup"><span data-stu-id="64630-112">Clients and service providers can define their own property sets by calling [CoCreateGUID](https://msdn.microsoft.com/library/ms688568.aspx) function.</span></span> <span data-ttu-id="64630-113">Normalmente, estos conjuntos de propiedades se crean para las aplicaciones cliente personalizadas.</span><span class="sxs-lookup"><span data-stu-id="64630-113">Typically these property sets are created for custom client applications.</span></span> 
  
<span data-ttu-id="64630-114">Conjuntos de propiedades de MAPI se representan mediante las siguientes constantes:</span><span class="sxs-lookup"><span data-stu-id="64630-114">MAPI's property sets are represented by the following constants:</span></span>
  
<span data-ttu-id="64630-115">PS_MAPI</span><span class="sxs-lookup"><span data-stu-id="64630-115">PS_MAPI</span></span>
  
<span data-ttu-id="64630-116">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="64630-116">PS_PUBLIC_STRINGS</span></span>
  
<span data-ttu-id="64630-117">PS_ROUTING_EMAIL_ADDRESSES</span><span class="sxs-lookup"><span data-stu-id="64630-117">PS_ROUTING_EMAIL_ADDRESSES</span></span>
  
<span data-ttu-id="64630-118">PS_ROUTING_ADDRTYPE</span><span class="sxs-lookup"><span data-stu-id="64630-118">PS_ROUTING_ADDRTYPE</span></span>
  
<span data-ttu-id="64630-119">PS_ROUTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="64630-119">PS_ROUTING_SEARCH_KEY</span></span>
  
<span data-ttu-id="64630-120">PS_ROUTING_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="64630-120">PS_ROUTING_DISPLAY_NAME</span></span>
  
<span data-ttu-id="64630-121">PS_ROUTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="64630-121">PS_ROUTING_ENTRYID</span></span>
  
<span data-ttu-id="64630-122">El conjunto de propiedades PS_MAPI está reservado; se usa por los proveedores de servicio para generar los nombres de propiedades con identificadores por debajo del rango con nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="64630-122">The PS_MAPI property set is reserved; it is used by service providers to generate names for properties with identifiers below the named property range.</span></span> <span data-ttu-id="64630-123">El conjunto de propiedades PS_PUBLIC_STRINGS se usa en los clientes para propiedades con nombre de los mensajes IPM.</span><span class="sxs-lookup"><span data-stu-id="64630-123">The PS_PUBLIC_STRINGS property set is used by clients for named properties of IPM messages.</span></span> <span data-ttu-id="64630-124">Debido a que las propiedades con nombre en el conjunto de propiedades PS_PUBLIC_STRINGS aparecen en la interfaz de usuario de un cliente, los mensajes no visible, como aquellas que pertenecen a la clase de mensaje IPC deben evitar la creación de las propiedades con este conjunto de propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="64630-124">Because named properties in the PS_PUBLIC_STRINGS property set appear in a client's user interface, nonvisible messages such as those that belong to the IPC message class should avoid creating named properties with this property set.</span></span> <span data-ttu-id="64630-125">En su lugar, deben crear propiedades en el intervalo específico de la clase de mensaje, 0x6800 a través de 0x7FFF.</span><span class="sxs-lookup"><span data-stu-id="64630-125">Instead, they should create properties in the message class-specific range, 0x6800 through 0x7FFF.</span></span>
  
<span data-ttu-id="64630-126">Los otros conjuntos de propiedades mantenga propiedades con nombre que describa a los destinatarios que suelen ser miembros de una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="64630-126">The other property sets hold named properties describing recipients that are typically members of a routing list.</span></span> <span data-ttu-id="64630-127">Que contiene el mismo tipo de información como las propiedades que están asociadas con las propiedades de la lista de destinatarios, las propiedades de estos conjuntos de propiedades se entienden que las puertas de enlace requieren asignación para un sistema de mensajería de destino.</span><span class="sxs-lookup"><span data-stu-id="64630-127">Containing the same type of information as the properties that are associated with recipient list properties, properties in these property sets are understood by gateways to require mapping for a target messaging system.</span></span> <span data-ttu-id="64630-128">Debido a que hay cinco tipos de información para describir las propiedades, MAPI ha definido cinco conjuntos de propiedades diferentes.</span><span class="sxs-lookup"><span data-stu-id="64630-128">Because there are five types of information for describing properties, MAPI has defined five different property sets.</span></span> <span data-ttu-id="64630-129">Establece un cliente envía un mensaje que debe incluir una dirección y el tipo de dirección para sus miembros de la lista enrutamiento asigna una propiedad con nombre para cada miembro de la PS_ROUTING_EMAIL_ADDRESSES y la propiedad PS_ROUTING_ADDRTYPE.</span><span class="sxs-lookup"><span data-stu-id="64630-129">A client sending a message that must include an address and address type for its routing list members assigns a named property for each member in the PS_ROUTING_EMAIL_ADDRESSES and PS_ROUTING_ADDRTYPE property sets.</span></span> <span data-ttu-id="64630-130">Esto garantiza que la dirección y el tipo de dirección siguen siendo viables cuando se envían a un sistema de mensajería externo.</span><span class="sxs-lookup"><span data-stu-id="64630-130">This ensures that the address and address type remain viable when sent to a foreign messaging system.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="64630-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="64630-131">See also</span></span>



[<span data-ttu-id="64630-132">Con el nombre de las propiedades de MAPI</span><span class="sxs-lookup"><span data-stu-id="64630-132">MAPI Named Properties</span></span>](mapi-named-properties.md)

