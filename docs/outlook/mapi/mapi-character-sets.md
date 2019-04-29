---
title: Conjuntos de caracteres MAPI
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
# <a name="mapi-character-sets"></a><span data-ttu-id="4a23c-103">Conjuntos de caracteres MAPI</span><span class="sxs-lookup"><span data-stu-id="4a23c-103">MAPI Character Sets</span></span>

  
  
<span data-ttu-id="4a23c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a23c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a23c-105">Las aplicaciones cliente compatibles con MAPI y los proveedores de servicios pueden usar caracteres ANSI (bit único) o caracteres Unicode (byte doble).</span><span class="sxs-lookup"><span data-stu-id="4a23c-105">MAPI-compliant client applications and service providers can use ANSI characters (single byte) or Unicode characters (double byte).</span></span> <span data-ttu-id="4a23c-106">No se admiten juegos de caracteres OEM.</span><span class="sxs-lookup"><span data-stu-id="4a23c-106">OEM character sets are not supported.</span></span> <span data-ttu-id="4a23c-107">Una cadena OEM pasada a un método o función MAPI hará que se produzca un error en ese método o función.</span><span class="sxs-lookup"><span data-stu-id="4a23c-107">An OEM string passed to a MAPI method or function will cause that method or function to fail.</span></span> <span data-ttu-id="4a23c-108">Las aplicaciones cliente que trabajan con nombres de archivo en el juego de caracteres OEM deben tener cuidado de convertirlas a ANSI antes de pasarlas a un método o función MAPI.</span><span class="sxs-lookup"><span data-stu-id="4a23c-108">Client applications that work with filenames in the OEM character set must be careful to convert them to ANSI before passing them to a MAPI method or function.</span></span>
  
<span data-ttu-id="4a23c-109">La compatibilidad con el juego de caracteres Unicode es opcional tanto para los clientes como para los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="4a23c-109">Supporting the Unicode character set is optional, both for clients and service providers.</span></span> <span data-ttu-id="4a23c-110">Todos los proveedores de servicios deben escribir su código para que se puedan compilar independientemente de si admiten Unicode.</span><span class="sxs-lookup"><span data-stu-id="4a23c-110">All service providers should write their code so that they can compile regardless of whether or not they support Unicode.</span></span> <span data-ttu-id="4a23c-111">Los clientes se compilan condicionalmente, en función de su nivel de compatibilidad, pero no lo hacen los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="4a23c-111">Clients compile conditionally, depending on their level of support, but service providers do not.</span></span> <span data-ttu-id="4a23c-112">No deben volver a compilarse cuando cambia el juego de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4a23c-112">They should not have to be recompiled when the character set changes.</span></span> <span data-ttu-id="4a23c-113">Ningún código del proveedor de servicios debe ser condicional.</span><span class="sxs-lookup"><span data-stu-id="4a23c-113">Nothing in service provider code should be conditional.</span></span> 
  
<span data-ttu-id="4a23c-114">Cuando los clientes o proveedores de servicios que admiten Unicode realizan una llamada de método que incluye cadenas de caracteres como parámetros de entrada o salida, establecen la marca MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="4a23c-114">When clients or service providers that support Unicode make a method call that includes character strings as input or output parameters, they set the MAPI_UNICODE flag.</span></span> <span data-ttu-id="4a23c-115">Establecer esta marca indica a la implementación que todas las cadenas entrantes son cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="4a23c-115">Setting this flag indicates to the implementation that all incoming strings are Unicode strings.</span></span> <span data-ttu-id="4a23c-116">En la salida, al establecer este indicador se solicita que todas las cadenas que se devuelvan de la implementación deban ser cadenas Unicode, si es posible.</span><span class="sxs-lookup"><span data-stu-id="4a23c-116">On output, setting this flag requests that all strings passed back from the implementation should be Unicode strings if possible.</span></span> <span data-ttu-id="4a23c-117">Los implementadores de métodos compatibles con Unicode cumplirán con la solicitud; los implementadores de métodos que no proporcionan compatibilidad con Unicode no cumplen con lo especificado.</span><span class="sxs-lookup"><span data-stu-id="4a23c-117">Method implementers that support Unicode will comply with the request; method implementers that do not provide Unicode support will not comply.</span></span> <span data-ttu-id="4a23c-118">Las propiedades de cadena que no están en formato Unicode son del tipo PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="4a23c-118">String properties that are not in Unicode format are of type PT_STRING8.</span></span>
  
<span data-ttu-id="4a23c-119">MAPI define la constante **fMapiUnicode** en el archivo de encabezado MAPIDEFS. H para representar el juego de caracteres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4a23c-119">MAPI defines the **fMapiUnicode** constant in the header file MAPIDEFS.H to represent the default character set.</span></span> <span data-ttu-id="4a23c-120">Si un cliente o un proveedor de servicios admite Unicode, **fMapiUnicode** se establece en MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="4a23c-120">If a client or service provider supports Unicode, **fMapiUnicode** is set to MAPI_UNICODE.</span></span> <span data-ttu-id="4a23c-121">Los clientes y los proveedores de servicios que no admiten Unicode set **fMapiUnicode** en cero.</span><span class="sxs-lookup"><span data-stu-id="4a23c-121">Clients and service providers that do not support Unicode set **fMapiUnicode** to zero.</span></span> 
  
<span data-ttu-id="4a23c-122">Los proveedores de servicios que no admiten Unicode deben:</span><span class="sxs-lookup"><span data-stu-id="4a23c-122">Service providers that do not support Unicode should:</span></span>
  
- <span data-ttu-id="4a23c-123">Rehusar realizar conversiones entre conjuntos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4a23c-123">Refuse to perform conversions between character sets.</span></span>
    
- <span data-ttu-id="4a23c-124">Nunca pase la marca MAPI_UNICODE en las llamadas de método.</span><span class="sxs-lookup"><span data-stu-id="4a23c-124">Never pass the MAPI_UNICODE flag in method calls.</span></span>
    
- <span data-ttu-id="4a23c-125">Devuelve MAPI_E_BAD_CHARWIDTH cuando se pasa la marca MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="4a23c-125">Return MAPI_E_BAD_CHARWIDTH when the MAPI_UNICODE flag is passed in.</span></span>
    
- <span data-ttu-id="4a23c-126">Declarar explícitamente las propiedades de la cadena ANSI.</span><span class="sxs-lookup"><span data-stu-id="4a23c-126">Declare ANSI string properties explicitly.</span></span> 
    
<span data-ttu-id="4a23c-127">Los proveedores de servicios también pueden devolver MAPI_E_BAD_CHARWIDTH cuando solo admiten Unicode y los clientes no pasan la marca MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="4a23c-127">Service providers can also return MAPI_E_BAD_CHARWIDTH when they only support Unicode and clients do not pass the MAPI_UNICODE flag.</span></span> 
  
 <span data-ttu-id="4a23c-128">La versión actual de MAPI admite Unicode en los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="4a23c-128">The current version of MAPI supports Unicode in the following methods:</span></span> 
  
[<span data-ttu-id="4a23c-129">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="4a23c-129">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="4a23c-130">IAddrBook::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="4a23c-130">IAddrBook::CreateOneOff</span></span>](iaddrbook-createoneoff.md)
  
[<span data-ttu-id="4a23c-131">IAddrBook::Details</span><span class="sxs-lookup"><span data-stu-id="4a23c-131">IAddrBook::Details</span></span>](iaddrbook-details.md)
  
[<span data-ttu-id="4a23c-132">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="4a23c-132">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
<span data-ttu-id="4a23c-133">[IMAPIProp:: GetLastError](imapiprop-getlasterror.md) (Solo implementación de**IAddrBook** )</span><span class="sxs-lookup"><span data-stu-id="4a23c-133">[IMAPIProp::GetLastError](imapiprop-getlasterror.md) (**IAddrBook** implementation only)</span></span> 
  
<span data-ttu-id="4a23c-134">Para estos métodos, los autores de las llamadas pueden esperar que las cadenas que se devuelvan sean Unicode.</span><span class="sxs-lookup"><span data-stu-id="4a23c-134">For these methods, callers can expect any returned strings to be Unicode strings.</span></span> <span data-ttu-id="4a23c-135">Las cadenas de caracteres devueltas por las implementaciones MAPI de cualquier otro método serán cadenas de caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="4a23c-135">Character strings returned from MAPI implementations of any other method will be ANSI character strings.</span></span>
  

