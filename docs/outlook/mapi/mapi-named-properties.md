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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345867"
---
# <a name="mapi-named-properties"></a>Propiedades con nombre MAPI
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI proporciona una función para asignar nombres a las propiedades, para asignar estos nombres a identificadores únicos y para que esta asignación sea persistente. El nombre persistente para la asignación de identificadores garantiza que los nombres de propiedad sigan siendo válidos en todas las sesiones.
  
Para definir una propiedad con nombre, un cliente o un proveedor de servicios constituye un nombre y lo almacena en una estructura [MAPINAMEID](mapinameid.md) . Dado que los nombres se componen de un identificador único global (GUID) de 32 bits, y una cadena de caracteres Unicode o un valor numérico, los creadores de propiedades con nombre pueden crear nombres significativos sin temor a la duplicación. Los nombres son únicos y se pueden usar sin tener en cuenta el valor de sus identificadores. 
  
Para admitir propiedades con nombre, un proveedor de servicios implementa dos métodos ( [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) y [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md) ) para traducir entre nombres e identificadores y permitir su [IMAPIProp:: GetProps](imapiprop-getprops.md) [ IMAPIProp:: SetProps](imapiprop-setprops.md) métodos para recuperar y modificar propiedades con identificadores en el intervalo de propiedades con nombre. El intervalo para los identificadores de propiedad con nombre está comprendido entre 0x8000 y 0xFFFE. 
  
Cualquier objeto que implemente la interfaz **IMAPIProp** puede admitir propiedades con nombre. Los proveedores de libretas de direcciones que permiten que las entradas de otros proveedores se copien en sus contenedores y los proveedores de almacenamiento de mensajes que se pueden usar para crear tipos de mensaje arbitrarios son necesarios para proporcionar esta compatibilidad. Es una opción para todos los demás proveedores de servicios. Los proveedores que no admiten propiedades con nombre devuelven MAPI_E_NO_SUPPORT desde los métodos **GetIDsFromNames** y **GetNamesFromIDs** y deniegan el establecimiento de las propiedades con identificadores de 0x8000 o superior, y devuelven MAPI_E_UNEXPECTED en el ** SPropProblemarray**.
  
La creación de nombres para las propiedades es una forma de que los clientes definan nuevas propiedades para las clases de mensaje personalizadas o existentes. Los proveedores de servicios pueden usar propiedades con nombre para exponer características únicas de sus sistemas de mensajería. Sin embargo, otro uso de las propiedades con nombre es proporcionar una forma alternativa de hacer referencia a las propiedades con identificadores inferiores a 0x8000. 
  
Por ejemplo, un cliente puede usar código similar al código siguiente para recuperar los nombres de todas las propiedades con nombre de un objeto:
  
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

Para solicitar todos los nombres del conjunto de propiedades PS_PUBLIC_STRINGS, un cliente podría reemplazar el valor NULL del parámetro set de la propiedad a PS_PUBLIC_STRINGS de la siguiente manera: 
  
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

## <a name="see-also"></a>Vea también

- [Información general sobre MAPI (propiedad)](mapi-property-overview.md)

