---
title: Definir nuevas propiedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1a2325ea-ddfa-480f-b65f-f5b20471fb40
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 68e877568565cfcc30b60e9b21f55b7dc1600b28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816656"
---
# <a name="defining-new-mapi-properties"></a><span data-ttu-id="58ce7-103">Definir nuevas propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="58ce7-103">Defining New MAPI Properties</span></span>

  
  
<span data-ttu-id="58ce7-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="58ce7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="58ce7-105">A pesar de la gran cantidad de propiedades suministrada por MAPI para que usen los clientes y proveedores de servicios, MAPI permite nuevas propiedades que se creará si es necesario.</span><span class="sxs-lookup"><span data-stu-id="58ce7-105">In spite of the wealth of properties supplied by MAPI for use by clients and service providers, MAPI enables new properties to be created if necessary.</span></span> <span data-ttu-id="58ce7-106">Algunos de los escenarios válidos para definir nuevas propiedades públicas incluyen un cliente de creación de propiedades para admitir una nueva clase de mensaje y un proveedor de servicios creación de nuevas propiedades para exponer características exclusivas de mensajería del sistema.</span><span class="sxs-lookup"><span data-stu-id="58ce7-106">Some of the valid scenarios for defining new public properties include a client creating properties to support a new message class and a service provider creating new properties to expose unique messaging system features.</span></span>
  
<span data-ttu-id="58ce7-107">Normalmente, no es válido para un proveedor de servicios definir nuevas propiedades para una clase de objeto o un mensaje existente de MAPI.</span><span class="sxs-lookup"><span data-stu-id="58ce7-107">It is typically not valid for a service provider to define new properties for an existing MAPI object or message class.</span></span> <span data-ttu-id="58ce7-108">Una de las principales ventajas del uso de MAPI es que los identificadores estándar y formatos para un gran número de sistema de mensajería se establecen elementos de copia de seguridad, permitir a los usuarios sin ningún problema mezclar y hacer coincidir los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="58ce7-108">One of the primary benefits of using MAPI is that standard identifiers and formats for a large number of messaging system elements are set up, enabling users to seamlessly mix and match service providers.</span></span> <span data-ttu-id="58ce7-109">Proveedores de servicios que se utilizan las propiedades no estándar no funcionan así como con otros proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="58ce7-109">Service providers that use nonstandard properties do not work as well with other service providers.</span></span> 
  
<span data-ttu-id="58ce7-110">Los clientes pueden crear propiedades de contenido para nuevas clases de mensaje por:</span><span class="sxs-lookup"><span data-stu-id="58ce7-110">Clients can create content properties for new message classes by:</span></span>
  
- <span data-ttu-id="58ce7-111">Mediante identificadores de propiedad dentro de un intervalo designado para propiedades de contenido específico de la clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="58ce7-111">Using property identifiers within a designated range for message class-specific content properties.</span></span>
    
    - <span data-ttu-id="58ce7-112">O bien -</span><span class="sxs-lookup"><span data-stu-id="58ce7-112">Or -</span></span>
    
- <span data-ttu-id="58ce7-113">Uso de propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="58ce7-113">Using named properties.</span></span> 
    
<span data-ttu-id="58ce7-114">La primera opción es preferible debido a que no todos los proveedores de servicios admiten las propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="58ce7-114">The first option is preferable because not all service providers support named properties.</span></span> <span data-ttu-id="58ce7-115">MAPI define dos rangos independientes para los clientes que se usará para nuevas propiedades de contenido específico de la clase de mensaje:</span><span class="sxs-lookup"><span data-stu-id="58ce7-115">MAPI defines two separate ranges for clients to use for new message class-specific content properties:</span></span>
  
- <span data-ttu-id="58ce7-116">0x6800 a 0x7BFF para propiedades transmisible</span><span class="sxs-lookup"><span data-stu-id="58ce7-116">0x6800 to 0x7BFF for transmittable properties</span></span>
    
- <span data-ttu-id="58ce7-117">0x7C00 a 0x7FFF para las propiedades de nontransmittable</span><span class="sxs-lookup"><span data-stu-id="58ce7-117">0x7C00 to 0x7FFF for nontransmittable properties</span></span>
    
<span data-ttu-id="58ce7-118">Identificadores de propiedad deben estar comprendido en rangos predefinidos para ayudar a evitar conflictos entre las propiedades definidas por distintos proveedores o los usuarios.</span><span class="sxs-lookup"><span data-stu-id="58ce7-118">Property identifiers must fall in predefined ranges to help prevent collisions between properties defined by different vendors or users.</span></span> <span data-ttu-id="58ce7-119">Sin embargo, los usuarios de las propiedades de estos intervalos no pueden realizar suposiciones sobre el comportamiento de las propiedades.</span><span class="sxs-lookup"><span data-stu-id="58ce7-119">However, users of properties in these ranges cannot make assumptions as to the behavior of the properties.</span></span> <span data-ttu-id="58ce7-120">Cada cliente que crea una nueva clase de mensaje tiene acceso a estos intervalos; una propiedad con identificador _xxxx_ puede significar un comportamiento de una clase de mensaje y el otro comportamiento de otra clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="58ce7-120">Every client that creates a new message class has access to these ranges; a property with identifier  _xxxx_ can mean one behavior for one message class and another behavior for another message class.</span></span> 
  
<span data-ttu-id="58ce7-121">Propiedades con nombre se utilizan para garantizar que una propiedad concreta es única para una clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="58ce7-121">Named properties are used to guarantee a specific property is unique to a message class.</span></span> <span data-ttu-id="58ce7-122">Inician de identificadores de propiedad con nombre en el rango de 0 x 8000.</span><span class="sxs-lookup"><span data-stu-id="58ce7-122">Named property identifiers start in the 0x8000 range.</span></span> <span data-ttu-id="58ce7-123">Los clientes definición uno o varios nombres y, a continuación, llamar al método [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) del almacén de mensajes para asociar un identificador a cada nombre.</span><span class="sxs-lookup"><span data-stu-id="58ce7-123">Clients define one or more names and then call the message store's [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method to associate an identifier with each name.</span></span> <span data-ttu-id="58ce7-124">Propiedades con nombre se pueden usar por los clientes o proveedores de servicios para definir nuevas propiedades para cualquier objeto sólo si el propietario del objeto admite propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="58ce7-124">Named properties can be used by clients or service providers to define new properties for any object only if the owner of the object supports named properties.</span></span> <span data-ttu-id="58ce7-125">Los usuarios de estas propiedades llamadas **a GetIDsFromNames** y un método **IMAPIProp** relacionado, [GetNamesFromIDs](imapiprop-getnamesfromids.md), para asignar entre un nombre y su identificador.</span><span class="sxs-lookup"><span data-stu-id="58ce7-125">Users of these properties call **GetIDsFromNames** and a related **IMAPIProp** method, [GetNamesFromIDs](imapiprop-getnamesfromids.md), to map between a name and its identifier.</span></span>
  
<span data-ttu-id="58ce7-126">Todas las propiedades, nuevas o existentes, deben usar el conjunto de tipos de propiedad predefinida.</span><span class="sxs-lookup"><span data-stu-id="58ce7-126">All properties, new or existing, must use the set of predefined property types.</span></span> <span data-ttu-id="58ce7-127">No se puede agregar nuevos tipos de propiedad y no pueden ser modificados o eliminados los tipos existentes.</span><span class="sxs-lookup"><span data-stu-id="58ce7-127">New property types cannot be added and existing types cannot be modified or deleted.</span></span> <span data-ttu-id="58ce7-128">Propiedades simples, pequeñas, como las propiedades de entero de 16 bits o de un solo carácter, se pueden almacenar en cualquier tipo apropiado.</span><span class="sxs-lookup"><span data-stu-id="58ce7-128">Simple, small properties, such as single-character or 16-bit integer properties, can be stored in any appropriate type.</span></span> <span data-ttu-id="58ce7-129">Por ejemplo, se pueden almacenar números enteros como **ULONG** y cadenas pueden almacenarse como **PT_STRING8**.</span><span class="sxs-lookup"><span data-stu-id="58ce7-129">For example, integers can be stored as **ULONG** and strings can be stored as **PT_STRING8**.</span></span> 
  
<span data-ttu-id="58ce7-130">Use el tipo **PT_BINARY** para indicar una matriz de bytes contada.</span><span class="sxs-lookup"><span data-stu-id="58ce7-130">Use the **PT_BINARY** type to indicate a counted byte array.</span></span> <span data-ttu-id="58ce7-131">Este tipo de propiedad es útil para extender los tipos de datos que se pueden almacenar en un objeto.</span><span class="sxs-lookup"><span data-stu-id="58ce7-131">This property type is useful for extending the types of data that can be stored in an object.</span></span> <span data-ttu-id="58ce7-132">Bytes se transmiten en secuencia y no se hacen suposiciones sobre el significado de los datos.</span><span class="sxs-lookup"><span data-stu-id="58ce7-132">Bytes are transmitted in sequence and no assumptions are made about the meaning of the data.</span></span> <span data-ttu-id="58ce7-133">Cuando una aplicación cliente lee datos fuera de este tipo de propiedad, los datos se ha modificado desde cómo se almacenó.</span><span class="sxs-lookup"><span data-stu-id="58ce7-133">When a client application reads data out of such a property, the data is unchanged from how it was stored.</span></span> <span data-ttu-id="58ce7-134">El cliente debe llevar a cabo cualquier byte es necesario intercambiar al mover datos a través de CPU.</span><span class="sxs-lookup"><span data-stu-id="58ce7-134">The client must perform any necessary byte swapping when moving data across CPUs.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="58ce7-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="58ce7-135">See also</span></span>



[<span data-ttu-id="58ce7-136">Información general sobre MAPI (propiedad)</span><span class="sxs-lookup"><span data-stu-id="58ce7-136">MAPI Property Overview</span></span>](mapi-property-overview.md)
