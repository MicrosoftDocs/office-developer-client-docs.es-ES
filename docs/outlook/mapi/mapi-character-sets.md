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
ms.openlocfilehash: 5f7da3da8d23b28e13c39570b8f5971cb75a3310
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582535"
---
# <a name="mapi-character-sets"></a><span data-ttu-id="68298-103">Conjuntos de caracteres MAPI</span><span class="sxs-lookup"><span data-stu-id="68298-103">MAPI Character Sets</span></span>

  
  
<span data-ttu-id="68298-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68298-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68298-105">Pueden usar proveedores de servicios y aplicaciones de cliente compatible con MAPI (byte único) los caracteres ANSI o Unicode (de doble byte).</span><span class="sxs-lookup"><span data-stu-id="68298-105">MAPI-compliant client applications and service providers can use ANSI characters (single byte) or Unicode characters (double byte).</span></span> <span data-ttu-id="68298-106">No se admiten los conjuntos de caracteres OEM.</span><span class="sxs-lookup"><span data-stu-id="68298-106">OEM character sets are not supported.</span></span> <span data-ttu-id="68298-107">Una cadena de OEM se pasa a un método MAPI o función hará que dicho método o función se lleve a cabo.</span><span class="sxs-lookup"><span data-stu-id="68298-107">An OEM string passed to a MAPI method or function will cause that method or function to fail.</span></span> <span data-ttu-id="68298-108">Las aplicaciones de cliente que funcionan con los nombres de archivo en el juego de caracteres OEM deben tener cuidadas convertir a ANSI antes de pasarlas a un método MAPI o función.</span><span class="sxs-lookup"><span data-stu-id="68298-108">Client applications that work with filenames in the OEM character set must be careful to convert them to ANSI before passing them to a MAPI method or function.</span></span>
  
<span data-ttu-id="68298-109">Compatibilidad con Unicode juego de caracteres es opcional, tanto para los clientes y proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="68298-109">Supporting the Unicode character set is optional, both for clients and service providers.</span></span> <span data-ttu-id="68298-110">Todos los proveedores de servicios deben escribir su código para que puede compilar independientemente de si o no admiten Unicode.</span><span class="sxs-lookup"><span data-stu-id="68298-110">All service providers should write their code so that they can compile regardless of whether or not they support Unicode.</span></span> <span data-ttu-id="68298-111">Los clientes compilación condicionalmente, dependiendo de su nivel de compatibilidad, pero no lo hacen los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="68298-111">Clients compile conditionally, depending on their level of support, but service providers do not.</span></span> <span data-ttu-id="68298-112">No tendrán que volver a compilar cuando el juego de los cambios.</span><span class="sxs-lookup"><span data-stu-id="68298-112">They should not have to be recompiled when the character set changes.</span></span> <span data-ttu-id="68298-113">Nada en el código de proveedor de servicio debe ser condicional.</span><span class="sxs-lookup"><span data-stu-id="68298-113">Nothing in service provider code should be conditional.</span></span> 
  
<span data-ttu-id="68298-114">Cuando los clientes o proveedores de servicios que admiten Unicode realizar una llamada de método que incluye las cadenas de caracteres como parámetros de entrada o salidas, establecer el indicador MAPI_UNICODE..</span><span class="sxs-lookup"><span data-stu-id="68298-114">When clients or service providers that support Unicode make a method call that includes character strings as input or output parameters, they set the MAPI_UNICODE flag.</span></span> <span data-ttu-id="68298-115">Establecer esta marca indica a la implementación que todas las cadenas entrantes son cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="68298-115">Setting this flag indicates to the implementation that all incoming strings are Unicode strings.</span></span> <span data-ttu-id="68298-116">En la salida, establecer este las solicitudes de marca que hacer una copia de todas las cadenas que se pasan desde la implementación debe ser cadenas Unicode si es posible.</span><span class="sxs-lookup"><span data-stu-id="68298-116">On output, setting this flag requests that all strings passed back from the implementation should be Unicode strings if possible.</span></span> <span data-ttu-id="68298-117">Los implementadores de método que admiten Unicode cumplirá la solicitud; no se cumplen los implementadores de método que no proporcionan compatibilidad con Unicode.</span><span class="sxs-lookup"><span data-stu-id="68298-117">Method implementers that support Unicode will comply with the request; method implementers that do not provide Unicode support will not comply.</span></span> <span data-ttu-id="68298-118">Propiedades de cadena que no están en formato Unicode son de tipo PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="68298-118">String properties that are not in Unicode format are of type PT_STRING8.</span></span>
  
<span data-ttu-id="68298-119">MAPI define la constante **fMapiUnicode** en el archivo de encabezado MAPIDEFS. H para representar el juego de caracteres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="68298-119">MAPI defines the **fMapiUnicode** constant in the header file MAPIDEFS.H to represent the default character set.</span></span> <span data-ttu-id="68298-120">Si un proveedor de servicio o cliente es compatible con Unicode, **fMapiUnicode** se establece en MAPI_UNICODE..</span><span class="sxs-lookup"><span data-stu-id="68298-120">If a client or service provider supports Unicode, **fMapiUnicode** is set to MAPI_UNICODE.</span></span> <span data-ttu-id="68298-121">Los clientes y proveedores de servicios que no admiten Unicode establecen **fMapiUnicode** a cero.</span><span class="sxs-lookup"><span data-stu-id="68298-121">Clients and service providers that do not support Unicode set **fMapiUnicode** to zero.</span></span> 
  
<span data-ttu-id="68298-122">Proveedores de servicios que no admiten Unicode deben:</span><span class="sxs-lookup"><span data-stu-id="68298-122">Service providers that do not support Unicode should:</span></span>
  
- <span data-ttu-id="68298-123">Denegar realizar las conversiones entre conjuntos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="68298-123">Refuse to perform conversions between character sets.</span></span>
    
- <span data-ttu-id="68298-124">Nunca pase el indicador MAPI_UNICODE llamadas al método.</span><span class="sxs-lookup"><span data-stu-id="68298-124">Never pass the MAPI_UNICODE flag in method calls.</span></span>
    
- <span data-ttu-id="68298-125">Devolver MAPI_E_BAD_CHARWIDTH cuando se pasa el indicador MAPI_UNICODE en.</span><span class="sxs-lookup"><span data-stu-id="68298-125">Return MAPI_E_BAD_CHARWIDTH when the MAPI_UNICODE flag is passed in.</span></span>
    
- <span data-ttu-id="68298-126">Declarar explícitamente las propiedades de cadena ANSI.</span><span class="sxs-lookup"><span data-stu-id="68298-126">Declare ANSI string properties explicitly.</span></span> 
    
<span data-ttu-id="68298-127">Proveedores de servicio también pueden devolver MAPI_E_BAD_CHARWIDTH cuando solo admiten Unicode y los clientes no se pasa el indicador MAPI_UNICODE..</span><span class="sxs-lookup"><span data-stu-id="68298-127">Service providers can also return MAPI_E_BAD_CHARWIDTH when they only support Unicode and clients do not pass the MAPI_UNICODE flag.</span></span> 
  
 <span data-ttu-id="68298-128">La versión actual de MAPI admite Unicode en los siguientes métodos:</span><span class="sxs-lookup"><span data-stu-id="68298-128">The current version of MAPI supports Unicode in the following methods:</span></span> 
  
[<span data-ttu-id="68298-129">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="68298-129">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="68298-130">IAddrBook::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="68298-130">IAddrBook::CreateOneOff</span></span>](iaddrbook-createoneoff.md)
  
[<span data-ttu-id="68298-131">IAddrBook::Details</span><span class="sxs-lookup"><span data-stu-id="68298-131">IAddrBook::Details</span></span>](iaddrbook-details.md)
  
[<span data-ttu-id="68298-132">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="68298-132">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
<span data-ttu-id="68298-133">[IMAPIProp::GetLastError](imapiprop-getlasterror.md) (Sólo en la implementación**IAddrBook** )</span><span class="sxs-lookup"><span data-stu-id="68298-133">[IMAPIProp::GetLastError](imapiprop-getlasterror.md) (**IAddrBook** implementation only)</span></span> 
  
<span data-ttu-id="68298-134">Para estos métodos, los autores de llamadas pueden esperar cualquier cadenas devueltas como cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="68298-134">For these methods, callers can expect any returned strings to be Unicode strings.</span></span> <span data-ttu-id="68298-135">Las cadenas de caracteres devueltas desde las implementaciones de MAPI de cualquier otro método será cadenas de caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="68298-135">Character strings returned from MAPI implementations of any other method will be ANSI character strings.</span></span>
  

