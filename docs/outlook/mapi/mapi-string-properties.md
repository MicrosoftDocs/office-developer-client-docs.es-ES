---
title: Propiedades de la cadena MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63d7360a-e3a3-4365-9d46-50df1c715bde
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3e16a373ec35696f6d1a8ccc52263a1cf8570cfc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572329"
---
# <a name="mapi-string-properties"></a><span data-ttu-id="5f4db-103">Propiedades de la cadena MAPI</span><span class="sxs-lookup"><span data-stu-id="5f4db-103">MAPI String Properties</span></span>

  
  
<span data-ttu-id="5f4db-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f4db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f4db-105">MAPI proporciona tres tipos de propiedad diferentes para describir las propiedades de cadena:</span><span class="sxs-lookup"><span data-stu-id="5f4db-105">MAPI provides three different property types to describe string properties:</span></span>
  
<span data-ttu-id="5f4db-106">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="5f4db-106">PT_TSTRING</span></span>
  
<span data-ttu-id="5f4db-107">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="5f4db-107">PT_STRING8</span></span>
  
<span data-ttu-id="5f4db-108">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5f4db-108">PT_UNICODE</span></span>
  
<span data-ttu-id="5f4db-109">Propiedades de cadena con más frecuencia se definen como PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="5f4db-109">String properties are most commonly defined as PT_TSTRING.</span></span> <span data-ttu-id="5f4db-110">El tipo de propiedad PT_TSTRING compila condicionalmente a uno de los otros cadena tipos de propiedad, dependiendo del dependiendo de si se ha definido la macro UNICODE.</span><span class="sxs-lookup"><span data-stu-id="5f4db-110">The PT_TSTRING property type conditionally compiles to one of the other string property types, depending depending on whether the UNICODE macro has been defined.</span></span> <span data-ttu-id="5f4db-111">PT_STRING8 describe las cadenas de caracteres terminada en null de 8 bits en el formato ANSI; PT_UNICODE describe las cadenas de caracteres de doble byte terminada en null.</span><span class="sxs-lookup"><span data-stu-id="5f4db-111">PT_STRING8 describes 8-bit null-terminated character strings in the ANSI format; PT_UNICODE describes double-byte null-terminated character strings.</span></span> 
  
<span data-ttu-id="5f4db-112">Pueden elegir ya sea un cliente o un proveedor de servicios, o cliente y proveedor admitir las cadenas de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="5f4db-112">Either a client or a service provider, or both client and provider can choose to support Unicode character strings.</span></span> <span data-ttu-id="5f4db-113">No es necesario.</span><span class="sxs-lookup"><span data-stu-id="5f4db-113">It is not required.</span></span> <span data-ttu-id="5f4db-114">Un cliente que admite cadenas de PT_STRING8 sólo puede funcionar con un proveedor que es compatible con Unicode y viceversa.</span><span class="sxs-lookup"><span data-stu-id="5f4db-114">A client that supports only PT_STRING8 strings can operate with a provider that supports Unicode and vice versa.</span></span> <span data-ttu-id="5f4db-115">Para habilitar esta interoperabilidad, clientes y proveedores de servicios de pasan una marca, el indicador MAPI_UNICODE., para indicar que Unicode es compatible con métodos que impliquen el intercambio de cadenas de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5f4db-115">To enable this interoperability, clients and service providers pass a flag, the MAPI_UNICODE flag, to indicate that Unicode is supported in methods that involve the exchange of character strings.</span></span> 
  
<span data-ttu-id="5f4db-116">Por ejemplo, supongamos que un cliente compatible con Unicode y necesita recuperar el nombre para mostrar de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="5f4db-116">For example, suppose a client supports Unicode and needs to retrieve the display name of a folder.</span></span> <span data-ttu-id="5f4db-117">Todas las propiedades del cliente PT_TSTRING se compilan para escriba PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="5f4db-117">All of the client's PT_TSTRING properties are compiled to type PT_UNICODE.</span></span> <span data-ttu-id="5f4db-118">Cuando el cliente llama (método) [IMAPIProp::GetProps](imapiprop-getprops.md) de la carpeta para recuperar su propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), se pasa el indicador MAPI_UNICODE para solicitar que se devuelva la cadena de nombre para mostrar en el formato Unicode .</span><span class="sxs-lookup"><span data-stu-id="5f4db-118">When the client calls the folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, it passes the MAPI_UNICODE flag to request that the display name string be returned in the Unicode format.</span></span> 
  
<span data-ttu-id="5f4db-119">Los clientes y proveedores de servicios deben tener en cuenta que especificar un juego de caracteres de una llamada al método es sólo una solicitud.</span><span class="sxs-lookup"><span data-stu-id="5f4db-119">Clients and service providers need to be aware that specifying a character set in a method call is only a request.</span></span> <span data-ttu-id="5f4db-120">Compatibilidad con uno o ambos conjuntos de caracteres es responsabilidad del implementador del objeto.</span><span class="sxs-lookup"><span data-stu-id="5f4db-120">Supporting one or both character sets is up to the implementer of the object.</span></span> <span data-ttu-id="5f4db-121">No obstante, los proveedores de servicios se recomienda para admitir ambos conjuntos de caracteres porque permite conseguir una distribución más generalizada que los proveedores que admiten un solo conjunto.</span><span class="sxs-lookup"><span data-stu-id="5f4db-121">However, service providers are encouraged to support both character sets because it allows them to achieve more widespread distribution than providers that support only one set.</span></span> 
  
<span data-ttu-id="5f4db-122">Propiedades de cadena pueden llegar a ser bastante grande tal como se pueden propiedades binarias, las propiedades que utilice la propiedad escriba PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="5f4db-122">String properties can grow to be quite large as can binary properties — properties that use the property type PT_BINARY.</span></span> <span data-ttu-id="5f4db-123">Para facilitar la trabajar con propiedades de gran tamaño, MAPI permite que los proveedores de servicios establecer estas propiedades aplicar los límites de tamaño.</span><span class="sxs-lookup"><span data-stu-id="5f4db-123">To ease working with large properties, MAPI allows service providers setting these properties to enforce size limits.</span></span> <span data-ttu-id="5f4db-124">Estos límites pueden variar, dependiendo del:</span><span class="sxs-lookup"><span data-stu-id="5f4db-124">These limits can vary, depending on:</span></span>
  
- <span data-ttu-id="5f4db-125">Si se va las propiedades leído o escrito.</span><span class="sxs-lookup"><span data-stu-id="5f4db-125">Whether the properties are being read or written.</span></span>
    
- <span data-ttu-id="5f4db-126">Cómo el proveedor de servicios implementa los métodos de **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="5f4db-126">How the service provider implements the **IMAPIProp** methods.</span></span> 
    
- <span data-ttu-id="5f4db-127">Consideraciones de tiempo de ejecución, como las restricciones de memoria.</span><span class="sxs-lookup"><span data-stu-id="5f4db-127">Runtime considerations, such as memory constraints.</span></span>
    
- <span data-ttu-id="5f4db-128">Juego de caracteres posibles problemas de traducción.</span><span class="sxs-lookup"><span data-stu-id="5f4db-128">Character set translation issues.</span></span> 
    
<span data-ttu-id="5f4db-129">También se pueden colocar los límites de tamaño en la cadena y establecen propiedades binarias cuando se usan en la columna de una tabla debido a que a veces es imposible que todos los de un gran valor de la propiedad visible.</span><span class="sxs-lookup"><span data-stu-id="5f4db-129">Size limits can also be placed on string and binary properties when they are used in the column set of a table because it is sometimes impossible to make all of a large property's value visible.</span></span> <span data-ttu-id="5f4db-130">Muchos proveedores de servicios truncan la cadena de gran tamaño o propiedades binarias que se usan en las tablas a 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="5f4db-130">Many service providers truncate large string or binary properties that are used in tables to 255 bytes.</span></span> 
  
<span data-ttu-id="5f4db-131">Cuando un cliente llama a un método del objeto **GetProps** o **SetProps** para funcionar con una cadena de gran tamaño o propiedad binaria y se produce un error en la llamada debido al tamaño de la propiedad, el método devuelve el valor de error MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="5f4db-131">When a client calls an object's **GetProps** or **SetProps** method to work with a large string or binary property and the call fails because of the property size, the method returns the error value MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="5f4db-132">Si es así **GetProps** que tiene errores para una propiedad concreta, el cliente puede recuperar llamando a [IMAPIProp::OpenProperty](imapiprop-openproperty.md) y solicitar la **IStream** para el acceso mediante la especificación de IID_IStream como el identificador de interfaz.</span><span class="sxs-lookup"><span data-stu-id="5f4db-132">If it is **GetProps** that is failing for a specific property, the client can recover by calling [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and requesting the **IStream** for access by specifying IID_IStream as the interface identifier.</span></span> <span data-ttu-id="5f4db-133">Uso de **OpenProperty**, el cliente puede recuperar una propiedad de gran tamaño mediante una interfaz como **IStream** que es más adecuado para trabajar con propiedades de gran tamaño.</span><span class="sxs-lookup"><span data-stu-id="5f4db-133">Using **OpenProperty**, the client can retrieve a large property using an interface such as **IStream** that is better suited for working with large properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5f4db-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f4db-134">See also</span></span>



[<span data-ttu-id="5f4db-135">Información general sobre MAPI (propiedad)</span><span class="sxs-lookup"><span data-stu-id="5f4db-135">MAPI Property Overview</span></span>](mapi-property-overview.md)

