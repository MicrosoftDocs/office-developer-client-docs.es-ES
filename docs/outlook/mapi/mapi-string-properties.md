---
title: Propiedades de cadena MAPI
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
# <a name="mapi-string-properties"></a><span data-ttu-id="92492-103">Propiedades de cadena MAPI</span><span class="sxs-lookup"><span data-stu-id="92492-103">MAPI String Properties</span></span>

  
  
<span data-ttu-id="92492-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92492-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92492-105">MAPI proporciona tres tipos de propiedades diferentes para describir las propiedades de cadena:</span><span class="sxs-lookup"><span data-stu-id="92492-105">MAPI provides three different property types to describe string properties:</span></span>
  
<span data-ttu-id="92492-106">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="92492-106">PT_TSTRING</span></span>
  
<span data-ttu-id="92492-107">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="92492-107">PT_STRING8</span></span>
  
<span data-ttu-id="92492-108">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="92492-108">PT_UNICODE</span></span>
  
<span data-ttu-id="92492-109">Las propiedades de cadena se definen normalmente como PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="92492-109">String properties are most commonly defined as PT_TSTRING.</span></span> <span data-ttu-id="92492-110">El PT_TSTRING de propiedad se compila condicionalmente en uno de los otros tipos de propiedad de cadena, dependiendo de si se ha definido la macro UNICODE.</span><span class="sxs-lookup"><span data-stu-id="92492-110">The PT_TSTRING property type conditionally compiles to one of the other string property types, depending depending on whether the UNICODE macro has been defined.</span></span> <span data-ttu-id="92492-111">PT_STRING8 describe cadenas de caracteres terminadas en null de 8 bits en formato ANSI; PT_UNICODE describe las cadenas de caracteres terminadas en null de doble byte.</span><span class="sxs-lookup"><span data-stu-id="92492-111">PT_STRING8 describes 8-bit null-terminated character strings in the ANSI format; PT_UNICODE describes double-byte null-terminated character strings.</span></span> 
  
<span data-ttu-id="92492-112">Un cliente o un proveedor de servicios, o tanto el cliente como el proveedor pueden elegir admitir cadenas de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="92492-112">Either a client or a service provider, or both client and provider can choose to support Unicode character strings.</span></span> <span data-ttu-id="92492-113">No es necesario.</span><span class="sxs-lookup"><span data-stu-id="92492-113">It is not required.</span></span> <span data-ttu-id="92492-114">Un cliente que solo admite PT_STRING8 cadenas pueden funcionar con un proveedor compatible con Unicode y viceversa.</span><span class="sxs-lookup"><span data-stu-id="92492-114">A client that supports only PT_STRING8 strings can operate with a provider that supports Unicode and vice versa.</span></span> <span data-ttu-id="92492-115">Para habilitar esta interoperabilidad, los clientes y proveedores de servicios pasan una marca, la marca MAPI_UNICODE, para indicar que Unicode es compatible con métodos que implican el intercambio de cadenas de caracteres.</span><span class="sxs-lookup"><span data-stu-id="92492-115">To enable this interoperability, clients and service providers pass a flag, the MAPI_UNICODE flag, to indicate that Unicode is supported in methods that involve the exchange of character strings.</span></span> 
  
<span data-ttu-id="92492-116">Por ejemplo, supongamos que un cliente admite Unicode y necesita recuperar el nombre para mostrar de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="92492-116">For example, suppose a client supports Unicode and needs to retrieve the display name of a folder.</span></span> <span data-ttu-id="92492-117">Todas las propiedades de PT_TSTRING cliente se compilan para escribir PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="92492-117">All of the client's PT_TSTRING properties are compiled to type PT_UNICODE.</span></span> <span data-ttu-id="92492-118">Cuando el cliente llama al método [IMAPIProp::GetProps](imapiprop-getprops.md) de la carpeta para recuperar su propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), pasa la marca MAPI_UNICODE para solicitar que la cadena de nombre para mostrar se devuelva en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="92492-118">When the client calls the folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, it passes the MAPI_UNICODE flag to request that the display name string be returned in the Unicode format.</span></span> 
  
<span data-ttu-id="92492-119">Los clientes y proveedores de servicios deben tener en cuenta que especificar un juego de caracteres en una llamada de método es solo una solicitud.</span><span class="sxs-lookup"><span data-stu-id="92492-119">Clients and service providers need to be aware that specifying a character set in a method call is only a request.</span></span> <span data-ttu-id="92492-120">La compatibilidad con uno o ambos conjuntos de caracteres es cosa del implementador del objeto.</span><span class="sxs-lookup"><span data-stu-id="92492-120">Supporting one or both character sets is up to the implementer of the object.</span></span> <span data-ttu-id="92492-121">Sin embargo, se recomienda a los proveedores de servicios que admitan ambos conjuntos de caracteres porque les permite lograr una distribución más generalizada que los proveedores que solo admiten un conjunto.</span><span class="sxs-lookup"><span data-stu-id="92492-121">However, service providers are encouraged to support both character sets because it allows them to achieve more widespread distribution than providers that support only one set.</span></span> 
  
<span data-ttu-id="92492-122">Las propiedades de cadena pueden crecer hasta ser bastante grandes como las propiedades binarias( propiedades que usan el tipo de propiedad PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="92492-122">String properties can grow to be quite large as can binary properties — properties that use the property type PT_BINARY.</span></span> <span data-ttu-id="92492-123">Para facilitar el trabajo con propiedades de gran tamaño, MAPI permite a los proveedores de servicios establecer estas propiedades para aplicar límites de tamaño.</span><span class="sxs-lookup"><span data-stu-id="92492-123">To ease working with large properties, MAPI allows service providers setting these properties to enforce size limits.</span></span> <span data-ttu-id="92492-124">Estos límites pueden variar en función de:</span><span class="sxs-lookup"><span data-stu-id="92492-124">These limits can vary, depending on:</span></span>
  
- <span data-ttu-id="92492-125">Si las propiedades se leen o escriben.</span><span class="sxs-lookup"><span data-stu-id="92492-125">Whether the properties are being read or written.</span></span>
    
- <span data-ttu-id="92492-126">Cómo implementa el proveedor de servicios los **métodos IMAPIProp.**</span><span class="sxs-lookup"><span data-stu-id="92492-126">How the service provider implements the **IMAPIProp** methods.</span></span> 
    
- <span data-ttu-id="92492-127">Consideraciones en tiempo de ejecución, como restricciones de memoria.</span><span class="sxs-lookup"><span data-stu-id="92492-127">Runtime considerations, such as memory constraints.</span></span>
    
- <span data-ttu-id="92492-128">Problemas de traducción de juego de caracteres.</span><span class="sxs-lookup"><span data-stu-id="92492-128">Character set translation issues.</span></span> 
    
<span data-ttu-id="92492-129">Los límites de tamaño también se pueden colocar en propiedades binarias y de cadena cuando se usan en el conjunto de columnas de una tabla porque a veces es imposible hacer visible todo el valor de una propiedad grande.</span><span class="sxs-lookup"><span data-stu-id="92492-129">Size limits can also be placed on string and binary properties when they are used in the column set of a table because it is sometimes impossible to make all of a large property's value visible.</span></span> <span data-ttu-id="92492-130">Muchos proveedores de servicios truncan las propiedades binarias o de cadena de gran tamaño que se usan en las tablas a 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="92492-130">Many service providers truncate large string or binary properties that are used in tables to 255 bytes.</span></span> 
  
<span data-ttu-id="92492-131">Cuando un cliente llama al método **GetProps** o **SetProps** de un objeto para trabajar con una cadena de gran tamaño o una propiedad binaria y se produce un error en la llamada debido al tamaño de la propiedad, el método devuelve el valor de error MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="92492-131">When a client calls an object's **GetProps** or **SetProps** method to work with a large string or binary property and the call fails because of the property size, the method returns the error value MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="92492-132">Si se trata de **GetProps** que está fallando para una propiedad específica, el cliente puede recuperar llamando a [IMAPIProp::OpenProperty](imapiprop-openproperty.md) y solicitando el **IStream** para obtener acceso especificando IID_IStream como identificador de interfaz.</span><span class="sxs-lookup"><span data-stu-id="92492-132">If it is **GetProps** that is failing for a specific property, the client can recover by calling [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and requesting the **IStream** for access by specifying IID_IStream as the interface identifier.</span></span> <span data-ttu-id="92492-133">Con **OpenProperty,** el cliente puede recuperar una propiedad grande mediante una interfaz como **IStream** que sea más adecuada para trabajar con propiedades de gran tamaño.</span><span class="sxs-lookup"><span data-stu-id="92492-133">Using **OpenProperty**, the client can retrieve a large property using an interface such as **IStream** that is better suited for working with large properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="92492-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="92492-134">See also</span></span>



[<span data-ttu-id="92492-135">Información general sobre MAPI (propiedad)</span><span class="sxs-lookup"><span data-stu-id="92492-135">MAPI Property Overview</span></span>](mapi-property-overview.md)

