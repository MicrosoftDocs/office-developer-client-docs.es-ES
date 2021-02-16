---
title: Juegos de caracteres MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: fbe63916-b3eb-4ea7-bc42-80a8b0281b03
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 898883d8c93b69762883a502b7a4313b3417d0d3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417556"
---
# <a name="mapi-character-sets"></a><span data-ttu-id="7d444-103">Juegos de caracteres MAPI</span><span class="sxs-lookup"><span data-stu-id="7d444-103">MAPI Character Sets</span></span>

  
  
<span data-ttu-id="7d444-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d444-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d444-105">Las aplicaciones cliente compatibles con MAPI y los proveedores de servicios pueden usar caracteres ANSI (byte único) o caracteres Unicode (doble byte).</span><span class="sxs-lookup"><span data-stu-id="7d444-105">MAPI-compliant client applications and service providers can use ANSI characters (single byte) or Unicode characters (double byte).</span></span> <span data-ttu-id="7d444-106">No se admiten juegos de caracteres OEM.</span><span class="sxs-lookup"><span data-stu-id="7d444-106">OEM character sets are not supported.</span></span> <span data-ttu-id="7d444-107">Una cadena OEM pasada a un método o función MAPI hará que ese método o función falle.</span><span class="sxs-lookup"><span data-stu-id="7d444-107">An OEM string passed to a MAPI method or function will cause that method or function to fail.</span></span> <span data-ttu-id="7d444-108">Las aplicaciones cliente que funcionan con nombres de archivo en el juego de caracteres OEM deben tener cuidado de convertirlas a ANSI antes de pasarlas a un método o función MAPI.</span><span class="sxs-lookup"><span data-stu-id="7d444-108">Client applications that work with filenames in the OEM character set must be careful to convert them to ANSI before passing them to a MAPI method or function.</span></span>
  
<span data-ttu-id="7d444-109">La compatibilidad con el juego de caracteres Unicode es opcional, tanto para clientes como para proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="7d444-109">Supporting the Unicode character set is optional, both for clients and service providers.</span></span> <span data-ttu-id="7d444-110">Todos los proveedores de servicios deben escribir su código para que puedan compilar independientemente de si admiten o no Unicode.</span><span class="sxs-lookup"><span data-stu-id="7d444-110">All service providers should write their code so that they can compile regardless of whether or not they support Unicode.</span></span> <span data-ttu-id="7d444-111">Los clientes se compilan condicionalmente, en función de su nivel de compatibilidad, pero los proveedores de servicios no lo hacen.</span><span class="sxs-lookup"><span data-stu-id="7d444-111">Clients compile conditionally, depending on their level of support, but service providers do not.</span></span> <span data-ttu-id="7d444-112">No deben volver a compilarse cuando cambie el juego de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7d444-112">They should not have to be recompiled when the character set changes.</span></span> <span data-ttu-id="7d444-113">Nada en el código del proveedor de servicios debe ser condicional.</span><span class="sxs-lookup"><span data-stu-id="7d444-113">Nothing in service provider code should be conditional.</span></span> 
  
<span data-ttu-id="7d444-114">Cuando los clientes o proveedores de servicios compatibles con Unicode hacen una llamada de método que incluye cadenas de caracteres como parámetros de entrada o salida, establecen la marca MAPI_UNICODE caracteres.</span><span class="sxs-lookup"><span data-stu-id="7d444-114">When clients or service providers that support Unicode make a method call that includes character strings as input or output parameters, they set the MAPI_UNICODE flag.</span></span> <span data-ttu-id="7d444-115">Establecer esta marca indica a la implementación que todas las cadenas entrantes son cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="7d444-115">Setting this flag indicates to the implementation that all incoming strings are Unicode strings.</span></span> <span data-ttu-id="7d444-116">En el resultado, al establecer esta marca se solicita que todas las cadenas que se han pasado desde la implementación sean cadenas Unicode si es posible.</span><span class="sxs-lookup"><span data-stu-id="7d444-116">On output, setting this flag requests that all strings passed back from the implementation should be Unicode strings if possible.</span></span> <span data-ttu-id="7d444-117">Los implementadores de métodos compatibles con Unicode cumplirán con la solicitud; los implementadores de métodos que no proporcionan compatibilidad con Unicode no cumplirán.</span><span class="sxs-lookup"><span data-stu-id="7d444-117">Method implementers that support Unicode will comply with the request; method implementers that do not provide Unicode support will not comply.</span></span> <span data-ttu-id="7d444-118">Las propiedades de cadena que no están en formato Unicode son de tipo PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="7d444-118">String properties that are not in Unicode format are of type PT_STRING8.</span></span>
  
<span data-ttu-id="7d444-119">MAPI define la **constante fMapiUnicode** en el archivo de encabezado MAPIDEFS. H para representar el juego de caracteres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="7d444-119">MAPI defines the **fMapiUnicode** constant in the header file MAPIDEFS.H to represent the default character set.</span></span> <span data-ttu-id="7d444-120">Si un cliente o proveedor de servicios admite Unicode, **fMapiUnicode** se establece en MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="7d444-120">If a client or service provider supports Unicode, **fMapiUnicode** is set to MAPI_UNICODE.</span></span> <span data-ttu-id="7d444-121">Los clientes y proveedores de servicios que no admiten Unicode establecen **fMapiUnicode** en cero.</span><span class="sxs-lookup"><span data-stu-id="7d444-121">Clients and service providers that do not support Unicode set **fMapiUnicode** to zero.</span></span> 
  
<span data-ttu-id="7d444-122">Los proveedores de servicios que no admiten Unicode deben:</span><span class="sxs-lookup"><span data-stu-id="7d444-122">Service providers that do not support Unicode should:</span></span>
  
- <span data-ttu-id="7d444-123">No realizar conversiones entre juegos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7d444-123">Refuse to perform conversions between character sets.</span></span>
    
- <span data-ttu-id="7d444-124">No pase nunca la MAPI_UNICODE en llamadas a métodos.</span><span class="sxs-lookup"><span data-stu-id="7d444-124">Never pass the MAPI_UNICODE flag in method calls.</span></span>
    
- <span data-ttu-id="7d444-125">Devuelve MAPI_E_BAD_CHARWIDTH cuando se pasa MAPI_UNICODE marca.</span><span class="sxs-lookup"><span data-stu-id="7d444-125">Return MAPI_E_BAD_CHARWIDTH when the MAPI_UNICODE flag is passed in.</span></span>
    
- <span data-ttu-id="7d444-126">Declara las propiedades de cadena ANSI explícitamente.</span><span class="sxs-lookup"><span data-stu-id="7d444-126">Declare ANSI string properties explicitly.</span></span> 
    
<span data-ttu-id="7d444-127">Los proveedores de servicios también pueden MAPI_E_BAD_CHARWIDTH cuando solo admiten Unicode y los clientes no pasan la marca MAPI_UNICODE servicio.</span><span class="sxs-lookup"><span data-stu-id="7d444-127">Service providers can also return MAPI_E_BAD_CHARWIDTH when they only support Unicode and clients do not pass the MAPI_UNICODE flag.</span></span> 
  
 <span data-ttu-id="7d444-128">La versión actual de MAPI admite Unicode en los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="7d444-128">The current version of MAPI supports Unicode in the following methods:</span></span> 
  
[<span data-ttu-id="7d444-129">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="7d444-129">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="7d444-130">IAddrBook::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="7d444-130">IAddrBook::CreateOneOff</span></span>](iaddrbook-createoneoff.md)
  
[<span data-ttu-id="7d444-131">IAddrBook::Details</span><span class="sxs-lookup"><span data-stu-id="7d444-131">IAddrBook::Details</span></span>](iaddrbook-details.md)
  
[<span data-ttu-id="7d444-132">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="7d444-132">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
<span data-ttu-id="7d444-133">[IMAPIProp::GetLastError](imapiprop-getlasterror.md) (**solo implementación de IAddrBook)**</span><span class="sxs-lookup"><span data-stu-id="7d444-133">[IMAPIProp::GetLastError](imapiprop-getlasterror.md) (**IAddrBook** implementation only)</span></span> 
  
<span data-ttu-id="7d444-134">Para estos métodos, los autores de llamadas pueden esperar que las cadenas devueltas sean cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="7d444-134">For these methods, callers can expect any returned strings to be Unicode strings.</span></span> <span data-ttu-id="7d444-135">Las cadenas de caracteres devueltas de implementaciones MAPI de cualquier otro método serán cadenas de caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="7d444-135">Character strings returned from MAPI implementations of any other method will be ANSI character strings.</span></span>
  

