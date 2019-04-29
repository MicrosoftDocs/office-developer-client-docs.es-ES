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
ms.openlocfilehash: 9720b649eadecc73d84d98926674a1786796ba70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431396"
---
# <a name="mapi-string-properties"></a><span data-ttu-id="879ed-103">Propiedades de la cadena MAPI</span><span class="sxs-lookup"><span data-stu-id="879ed-103">MAPI String Properties</span></span>

  
  
<span data-ttu-id="879ed-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="879ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="879ed-105">MAPI proporciona tres tipos de propiedades diferentes para describir las propiedades de cadena:</span><span class="sxs-lookup"><span data-stu-id="879ed-105">MAPI provides three different property types to describe string properties:</span></span>
  
<span data-ttu-id="879ed-106">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="879ed-106">PT_TSTRING</span></span>
  
<span data-ttu-id="879ed-107">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="879ed-107">PT_STRING8</span></span>
  
<span data-ttu-id="879ed-108">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="879ed-108">PT_UNICODE</span></span>
  
<span data-ttu-id="879ed-109">Las propiedades de cadena suelen definirse como PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="879ed-109">String properties are most commonly defined as PT_TSTRING.</span></span> <span data-ttu-id="879ed-110">El tipo de propiedad PT_TSTRING se compila condicionalmente a uno de los otros tipos de propiedades de cadena, en función de si se ha definido la macro uniCODE.</span><span class="sxs-lookup"><span data-stu-id="879ed-110">The PT_TSTRING property type conditionally compiles to one of the other string property types, depending depending on whether the UNICODE macro has been defined.</span></span> <span data-ttu-id="879ed-111">PT_STRING8 describe las cadenas de caracteres terminadas en NULL de 8 bits en formato ANSI; PT_UNICODE describe las cadenas de caracteres de doble byte terminadas en NULL.</span><span class="sxs-lookup"><span data-stu-id="879ed-111">PT_STRING8 describes 8-bit null-terminated character strings in the ANSI format; PT_UNICODE describes double-byte null-terminated character strings.</span></span> 
  
<span data-ttu-id="879ed-112">Un cliente o proveedor de servicios, o bien el cliente y el proveedor pueden elegir admitir cadenas de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="879ed-112">Either a client or a service provider, or both client and provider can choose to support Unicode character strings.</span></span> <span data-ttu-id="879ed-113">No es necesario.</span><span class="sxs-lookup"><span data-stu-id="879ed-113">It is not required.</span></span> <span data-ttu-id="879ed-114">Un cliente que admite sólo cadenas PT_STRING8 puede operar con un proveedor compatible con Unicode y viceversa.</span><span class="sxs-lookup"><span data-stu-id="879ed-114">A client that supports only PT_STRING8 strings can operate with a provider that supports Unicode and vice versa.</span></span> <span data-ttu-id="879ed-115">Para habilitar esta interoperabilidad, los clientes y los proveedores de servicios pasan una marca, la marca MAPI_UNICODE, para indicar que se admite Unicode en los métodos que implican el intercambio de cadenas de caracteres.</span><span class="sxs-lookup"><span data-stu-id="879ed-115">To enable this interoperability, clients and service providers pass a flag, the MAPI_UNICODE flag, to indicate that Unicode is supported in methods that involve the exchange of character strings.</span></span> 
  
<span data-ttu-id="879ed-116">Por ejemplo, supongamos que un cliente es compatible con Unicode y necesita recuperar el nombre para mostrar de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="879ed-116">For example, suppose a client supports Unicode and needs to retrieve the display name of a folder.</span></span> <span data-ttu-id="879ed-117">Todas las propiedades de PT_TSTRING del cliente se compilan en el tipo PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="879ed-117">All of the client's PT_TSTRING properties are compiled to type PT_UNICODE.</span></span> <span data-ttu-id="879ed-118">Cuando el cliente llama al método [IMAPIProp:: GetProps](imapiprop-getprops.md) de la carpeta para recuperar su propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), pasa la marca MAPI_UNICODE para solicitar que la cadena de nombre para mostrar se devuelva en el formato Unicode .</span><span class="sxs-lookup"><span data-stu-id="879ed-118">When the client calls the folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, it passes the MAPI_UNICODE flag to request that the display name string be returned in the Unicode format.</span></span> 
  
<span data-ttu-id="879ed-119">Los clientes y los proveedores de servicios deben tener en cuenta que especificar un juego de caracteres en una llamada de método es solo una solicitud.</span><span class="sxs-lookup"><span data-stu-id="879ed-119">Clients and service providers need to be aware that specifying a character set in a method call is only a request.</span></span> <span data-ttu-id="879ed-120">La compatibilidad con uno o ambos conjuntos de caracteres depende del implementador del objeto.</span><span class="sxs-lookup"><span data-stu-id="879ed-120">Supporting one or both character sets is up to the implementer of the object.</span></span> <span data-ttu-id="879ed-121">Sin embargo, se recomienda a los proveedores de servicios que admitan ambos conjuntos de caracteres porque les permite obtener una distribución más extendida que los proveedores que admiten un solo conjunto.</span><span class="sxs-lookup"><span data-stu-id="879ed-121">However, service providers are encouraged to support both character sets because it allows them to achieve more widespread distribution than providers that support only one set.</span></span> 
  
<span data-ttu-id="879ed-122">Las propiedades de cadena pueden crecer para ser bastante grandes como propiedades binarias — propiedades que usan el tipo de propiedad PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="879ed-122">String properties can grow to be quite large as can binary properties — properties that use the property type PT_BINARY.</span></span> <span data-ttu-id="879ed-123">Para facilitar el trabajo con propiedades grandes, MAPI permite que los proveedores de servicios establezcan estas propiedades para exigir límites de tamaño.</span><span class="sxs-lookup"><span data-stu-id="879ed-123">To ease working with large properties, MAPI allows service providers setting these properties to enforce size limits.</span></span> <span data-ttu-id="879ed-124">Estos límites pueden variar en función de:</span><span class="sxs-lookup"><span data-stu-id="879ed-124">These limits can vary, depending on:</span></span>
  
- <span data-ttu-id="879ed-125">Si las propiedades se van a leer o escribir.</span><span class="sxs-lookup"><span data-stu-id="879ed-125">Whether the properties are being read or written.</span></span>
    
- <span data-ttu-id="879ed-126">Cómo implementa el proveedor de servicios los métodos **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="879ed-126">How the service provider implements the **IMAPIProp** methods.</span></span> 
    
- <span data-ttu-id="879ed-127">Consideraciones de tiempo de ejecución, como las restricciones de memoria.</span><span class="sxs-lookup"><span data-stu-id="879ed-127">Runtime considerations, such as memory constraints.</span></span>
    
- <span data-ttu-id="879ed-128">Problemas de traducción del juego de caracteres.</span><span class="sxs-lookup"><span data-stu-id="879ed-128">Character set translation issues.</span></span> 
    
<span data-ttu-id="879ed-129">Los límites de tamaño también se pueden colocar en propiedades binarias y de cadena cuando se utilizan en el conjunto de columnas de una tabla porque a veces es imposible hacer visible todo el valor de una propiedad grande.</span><span class="sxs-lookup"><span data-stu-id="879ed-129">Size limits can also be placed on string and binary properties when they are used in the column set of a table because it is sometimes impossible to make all of a large property's value visible.</span></span> <span data-ttu-id="879ed-130">Muchos proveedores de servicios truncan las propiedades binarias o de cadena de gran tamaño que se usan en las tablas a 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="879ed-130">Many service providers truncate large string or binary properties that are used in tables to 255 bytes.</span></span> 
  
<span data-ttu-id="879ed-131">Cuando un cliente llama a un método **GetProps** o **SetProps** de un objeto para trabajar con una propiedad binaria o de cadena de gran tamaño y se produce un error en la llamada debido al tamaño de la propiedad, el método devuelve el valor de error MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="879ed-131">When a client calls an object's **GetProps** or **SetProps** method to work with a large string or binary property and the call fails because of the property size, the method returns the error value MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="879ed-132">Si es **GetProps** que produce errores en una propiedad específica, el cliente puede recuperarse llamando a [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) y solicitando a **IStream** el acceso especificando IID_IStream como identificador de interfaz.</span><span class="sxs-lookup"><span data-stu-id="879ed-132">If it is **GetProps** that is failing for a specific property, the client can recover by calling [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and requesting the **IStream** for access by specifying IID_IStream as the interface identifier.</span></span> <span data-ttu-id="879ed-133">Con **OpenProperty**, el cliente puede recuperar una propiedad grande mediante una interfaz como **IStream** , que es más adecuada para trabajar con propiedades grandes.</span><span class="sxs-lookup"><span data-stu-id="879ed-133">Using **OpenProperty**, the client can retrieve a large property using an interface such as **IStream** that is better suited for working with large properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="879ed-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="879ed-134">See also</span></span>



[<span data-ttu-id="879ed-135">Información general sobre MAPI (propiedad)</span><span class="sxs-lookup"><span data-stu-id="879ed-135">MAPI Property Overview</span></span>](mapi-property-overview.md)

