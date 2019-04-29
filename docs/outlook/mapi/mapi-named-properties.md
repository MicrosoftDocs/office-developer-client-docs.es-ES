---
title: Propiedades con nombre MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 464b1297-9d90-47bd-afc4-3dc63b106cb7
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d83b98b4f06c648676852673a694a63b78f568b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435050"
---
# <a name="mapi-named-properties"></a><span data-ttu-id="a74ec-103">Propiedades con nombre MAPI</span><span class="sxs-lookup"><span data-stu-id="a74ec-103">MAPI Named Properties</span></span>
 
<span data-ttu-id="a74ec-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a74ec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a74ec-105">MAPI proporciona una función para asignar nombres a las propiedades, para asignar estos nombres a identificadores únicos y para que esta asignación sea persistente.</span><span class="sxs-lookup"><span data-stu-id="a74ec-105">MAPI provides a facility for assigning names to properties, for mapping these names to unique identifiers, and for making this mapping persistent.</span></span> <span data-ttu-id="a74ec-106">El nombre persistente para la asignación de identificadores garantiza que los nombres de propiedad sigan siendo válidos en todas las sesiones.</span><span class="sxs-lookup"><span data-stu-id="a74ec-106">Persistent name to identifier mapping ensures that property names remain valid across sessions.</span></span>
  
<span data-ttu-id="a74ec-107">Para definir una propiedad con nombre, un cliente o un proveedor de servicios constituye un nombre y lo almacena en una estructura [MAPINAMEID](mapinameid.md) .</span><span class="sxs-lookup"><span data-stu-id="a74ec-107">To define a named property, a client or service provider makes up a name and stores it in a [MAPINAMEID](mapinameid.md) structure.</span></span> <span data-ttu-id="a74ec-108">Dado que los nombres se componen de un identificador único global (GUID) de 32 bits, y una cadena de caracteres Unicode o un valor numérico, los creadores de propiedades con nombre pueden crear nombres significativos sin temor a la duplicación.</span><span class="sxs-lookup"><span data-stu-id="a74ec-108">Because names are made up of a 32-bit globally unique identifier, or GUID, and either a Unicode character string or numeric value, creators of named properties can create meaningful names without fear of duplication.</span></span> <span data-ttu-id="a74ec-109">Los nombres son únicos y se pueden usar sin tener en cuenta el valor de sus identificadores.</span><span class="sxs-lookup"><span data-stu-id="a74ec-109">Names are unique and they can be used without regard to the value of their identifiers.</span></span> 
  
<span data-ttu-id="a74ec-110">Para admitir propiedades con nombre, un proveedor de servicios implementa dos métodos ( [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) y [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md) ) para traducir entre nombres e identificadores y permitir su [IMAPIProp:: GetProps](imapiprop-getprops.md) [ IMAPIProp:: SetProps](imapiprop-setprops.md) métodos para recuperar y modificar propiedades con identificadores en el intervalo de propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="a74ec-110">To support named properties, a service provider implements two methods — [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) and [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) — to translate between names and identifiers and to allow its [IMAPIProp::GetProps](imapiprop-getprops.md)[IMAPIProp::SetProps](imapiprop-setprops.md) methods to retrieve and modify properties with identifiers in the named property range.</span></span> <span data-ttu-id="a74ec-111">El intervalo para los identificadores de propiedad con nombre está comprendido entre 0x8000 y 0xFFFE.</span><span class="sxs-lookup"><span data-stu-id="a74ec-111">The range for named property identifiers is between 0x8000 and 0xFFFE.</span></span> 
  
<span data-ttu-id="a74ec-112">Cualquier objeto que implemente la interfaz **IMAPIProp** puede admitir propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="a74ec-112">Any object that implements the **IMAPIProp** interface can support named properties.</span></span> <span data-ttu-id="a74ec-113">Los proveedores de libretas de direcciones que permiten que las entradas de otros proveedores se copien en sus contenedores y los proveedores de almacenamiento de mensajes que se pueden usar para crear tipos de mensaje arbitrarios son necesarios para proporcionar esta compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="a74ec-113">Address book providers that allow entries from other providers to be copied into their containers and message store providers that can be used to create arbitrary message types are required to supply this support.</span></span> <span data-ttu-id="a74ec-114">Es una opción para todos los demás proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="a74ec-114">It is an option for all other service providers.</span></span> <span data-ttu-id="a74ec-115">Los proveedores que no admiten propiedades con nombre devuelven MAPI_E_NO_SUPPORT desde los métodos **GetIDsFromNames** y **GetNamesFromIDs** y deniegan el establecimiento de las propiedades con identificadores de 0x8000 o superior, y devuelven MAPI_E_UNEXPECTED en el \*\* SPropProblemarray\*\*.</span><span class="sxs-lookup"><span data-stu-id="a74ec-115">Providers that do not support named properties return MAPI_E_NO_SUPPORT from the **GetIDsFromNames** and **GetNamesFromIDs** methods and refuse to set any properties with identifiers of 0x8000 or greater, returning MAPI_E_UNEXPECTED in the **SPropProblemarray**.</span></span>
  
<span data-ttu-id="a74ec-116">La creación de nombres para las propiedades es una forma de que los clientes definan nuevas propiedades para las clases de mensaje personalizadas o existentes.</span><span class="sxs-lookup"><span data-stu-id="a74ec-116">Creating names for properties is one way for clients to define new properties for existing or custom message classes.</span></span> <span data-ttu-id="a74ec-117">Los proveedores de servicios pueden usar propiedades con nombre para exponer características únicas de sus sistemas de mensajería.</span><span class="sxs-lookup"><span data-stu-id="a74ec-117">Service providers can use named properties to expose unique features of their messaging systems.</span></span> <span data-ttu-id="a74ec-118">Sin embargo, otro uso de las propiedades con nombre es proporcionar una forma alternativa de hacer referencia a las propiedades con identificadores inferiores a 0x8000.</span><span class="sxs-lookup"><span data-stu-id="a74ec-118">Yet another use for named properties is to provide an alternate way of referring to properties with identifiers below 0x8000.</span></span> 
  
<span data-ttu-id="a74ec-119">Por ejemplo, un cliente puede usar código similar al código siguiente para recuperar los nombres de todas las propiedades con nombre de un objeto:</span><span class="sxs-lookup"><span data-stu-id="a74ec-119">For example, a client could use code similar to the following code to retrieve the names for all of an object's named properties:</span></span>
  
```cpp
LPSPropTagArray FAR *    lppPropTags = NULL;
LPGUID                   lpPropSetGuid = NULL;
ULONG FAR *              lpcPropNames;
LPMAPINAMEID FAR * FAR * lpppPropNames;
lpMAPIProp->GetNamesFromIDs (lppPropTags,
                             lpPropSetGuid,
                             0,
                             lpcPropNames,
                             lpppPropNames);
 
```

<span data-ttu-id="a74ec-120">Para solicitar todos los nombres del conjunto de propiedades PS_PUBLIC_STRINGS, un cliente podría reemplazar el valor NULL del parámetro set de la propiedad a PS_PUBLIC_STRINGS de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="a74ec-120">To request all names from the PS_PUBLIC_STRINGS property set, a client would replace the NULL in the property set parameter to PS_PUBLIC_STRINGS as follows:</span></span> 
  
```cpp
LPSPropTagArray FAR *    lppPropTags = NULL;
LPGUID                   lpPropSetGuid = &PS_PUBLIC_STRINGS;
ULONG FAR *              lpcPropNames;
LPMAPINAMEID FAR * FAR * lpppPropNames;
lpMAPIProp->GetNamesFromIDs (lppPropTags,
                             lpPropSetGuid,
                             0,
                             lpcPropNames,
                             lpppPropNames);
 
```

## <a name="see-also"></a><span data-ttu-id="a74ec-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="a74ec-121">See also</span></span>

- [<span data-ttu-id="a74ec-122">Información general sobre MAPI (propiedad)</span><span class="sxs-lookup"><span data-stu-id="a74ec-122">MAPI Property Overview</span></span>](mapi-property-overview.md)

