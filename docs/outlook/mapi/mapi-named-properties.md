---
title: Con el nombre de las propiedades de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 464b1297-9d90-47bd-afc4-3dc63b106cb7
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e755c18ef3cc32f9a00169f19cf336eace447a32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818156"
---
# <a name="mapi-named-properties"></a><span data-ttu-id="f7dd0-103">Con el nombre de las propiedades de MAPI</span><span class="sxs-lookup"><span data-stu-id="f7dd0-103">MAPI Named Properties</span></span>
 
<span data-ttu-id="f7dd0-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f7dd0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f7dd0-105">MAPI proporciona una utilidad para asignar nombres a las propiedades, para asignar estos nombres a los identificadores únicos y para realizar esta asignación persistente.</span><span class="sxs-lookup"><span data-stu-id="f7dd0-105">MAPI provides a facility for assigning names to properties, for mapping these names to unique identifiers, and for making this mapping persistent.</span></span> <span data-ttu-id="f7dd0-106">Persistent asignación de nombre a identificador se asegura de que los nombres de propiedad siguen siendo válidos en todas las sesiones.</span><span class="sxs-lookup"><span data-stu-id="f7dd0-106">Persistent name to identifier mapping ensures that property names remain valid across sessions.</span></span>
  
<span data-ttu-id="f7dd0-107">Para definir una propiedad con nombre, un proveedor de servicio o cliente realiza un nombre y lo almacena en una estructura [MAPINAMEID](mapinameid.md) .</span><span class="sxs-lookup"><span data-stu-id="f7dd0-107">To define a named property, a client or service provider makes up a name and stores it in a [MAPINAMEID](mapinameid.md) structure.</span></span> <span data-ttu-id="f7dd0-108">Debido a que los nombres se componen de un identificador único global de 32 bits, o GUID y puede ser una cadena o numérico valor de carácter Unicode, los creadores de propiedades con nombre pueden crear nombres descriptivos sin miedo de duplicación.</span><span class="sxs-lookup"><span data-stu-id="f7dd0-108">Because names are made up of a 32-bit globally unique identifier, or GUID, and either a Unicode character string or numeric value, creators of named properties can create meaningful names without fear of duplication.</span></span> <span data-ttu-id="f7dd0-109">Los nombres son únicos y se pueden usar sin tener en cuenta el valor de sus identificadores.</span><span class="sxs-lookup"><span data-stu-id="f7dd0-109">Names are unique and they can be used without regard to the value of their identifiers.</span></span> 
  
<span data-ttu-id="f7dd0-110">Para admitir las propiedades con nombre, un proveedor de servicios implementa dos métodos: [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) y [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) — para traducir entre los nombres y los identificadores y permitir su [IMAPIProp::GetProps](imapiprop-getprops.md) [ IMAPIProp::SetProps](imapiprop-setprops.md) métodos para recuperar y modificar las propiedades con los identificadores en el intervalo de la propiedad con nombre.</span><span class="sxs-lookup"><span data-stu-id="f7dd0-110">To support named properties, a service provider implements two methods — [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) and [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) — to translate between names and identifiers and to allow its [IMAPIProp::GetProps](imapiprop-getprops.md)[IMAPIProp::SetProps](imapiprop-setprops.md) methods to retrieve and modify properties with identifiers in the named property range.</span></span> <span data-ttu-id="f7dd0-111">El intervalo para los identificadores de propiedad con nombre se encuentra entre 0 x 8000 y 0xFFFE.</span><span class="sxs-lookup"><span data-stu-id="f7dd0-111">The range for named property identifiers is between 0x8000 and 0xFFFE.</span></span> 
  
<span data-ttu-id="f7dd0-112">Cualquier objeto que implementa la interfaz **IMAPIProp** puede admitir propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="f7dd0-112">Any object that implements the **IMAPIProp** interface can support named properties.</span></span> <span data-ttu-id="f7dd0-113">Los proveedores de la libreta de direcciones que permiten las entradas de otros proveedores que se copiarán a sus contenedores y mensaje almacenan proveedores que se pueden usar para crear tipos de mensaje arbitrario se necesitan para proporcionar este soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="f7dd0-113">Address book providers that allow entries from other providers to be copied into their containers and message store providers that can be used to create arbitrary message types are required to supply this support.</span></span> <span data-ttu-id="f7dd0-114">Es una opción para todos los demás proveedores de servicio.</span><span class="sxs-lookup"><span data-stu-id="f7dd0-114">It is an option for all other service providers.</span></span> <span data-ttu-id="f7dd0-115">Los proveedores que no admiten las propiedades con nombre devuelven MAPI_E_NO_SUPPORT de los métodos **a GetIDsFromNames** y **GetNamesFromIDs** y denegación establecer las propiedades con identificadores de 0 x 8000 o mayor, devolución MAPI_E_UNEXPECTED en la ** SPropProblemarray**.</span><span class="sxs-lookup"><span data-stu-id="f7dd0-115">Providers that do not support named properties return MAPI_E_NO_SUPPORT from the **GetIDsFromNames** and **GetNamesFromIDs** methods and refuse to set any properties with identifiers of 0x8000 or greater, returning MAPI_E_UNEXPECTED in the **SPropProblemarray**.</span></span>
  
<span data-ttu-id="f7dd0-116">Creación de nombres de propiedades es una forma para que los clientes definir nuevas propiedades para las clases de mensajes existente o personalizado.</span><span class="sxs-lookup"><span data-stu-id="f7dd0-116">Creating names for properties is one way for clients to define new properties for existing or custom message classes.</span></span> <span data-ttu-id="f7dd0-117">Proveedores de servicios pueden usar propiedades con nombre para exponer características exclusivas de los sistemas de mensajería.</span><span class="sxs-lookup"><span data-stu-id="f7dd0-117">Service providers can use named properties to expose unique features of their messaging systems.</span></span> <span data-ttu-id="f7dd0-118">Aún otro uso de las propiedades con nombre consiste en proporcionar una forma alternativa de hacer referencia a las propiedades con identificadores por debajo de 0 x 8000.</span><span class="sxs-lookup"><span data-stu-id="f7dd0-118">Yet another use for named properties is to provide an alternate way of referring to properties with identifiers below 0x8000.</span></span> 
  
<span data-ttu-id="f7dd0-119">Por ejemplo, un cliente podría utilizar código similar al siguiente código para recuperar los nombres de todas las propiedades de un objeto con nombre:</span><span class="sxs-lookup"><span data-stu-id="f7dd0-119">For example, a client could use code similar to the following code to retrieve the names for all of an object's named properties:</span></span>
  
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

<span data-ttu-id="f7dd0-120">Para solicitar todos los nombres desde el conjunto de propiedades PS_PUBLIC_STRINGS, un cliente podría reemplazar el valor NULL en el parámetro del conjunto de propiedad a PS_PUBLIC_STRINGS como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="f7dd0-120">To request all names from the PS_PUBLIC_STRINGS property set, a client would replace the NULL in the property set parameter to PS_PUBLIC_STRINGS as follows:</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="f7dd0-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="f7dd0-121">See also</span></span>

- [<span data-ttu-id="f7dd0-122">Información general sobre MAPI (propiedad)</span><span class="sxs-lookup"><span data-stu-id="f7dd0-122">MAPI Property Overview</span></span>](mapi-property-overview.md)

