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
# <a name="mapi-named-properties"></a>Propiedades con nombre MAPI
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI proporciona una función para asignar nombres a propiedades, para asignar estos nombres a identificadores únicos y para hacer que esta asignación sea persistente. La asignación de nombre persistente a identificador garantiza que los nombres de propiedad sigan siendo válidos en todas las sesiones.
  
Para definir una propiedad con nombre, un cliente o proveedor de servicios forma un nombre y lo almacena en una [estructura MAPINAMEID.](mapinameid.md) Dado que los nombres están hechos de un identificador único global de 32 bits, o GUID, y una cadena de caracteres Unicode o un valor numérico, los creadores de propiedades con nombre pueden crear nombres significativos sin miedo a la duplicación. Los nombres son únicos y se pueden usar sin tener en cuenta el valor de sus identificadores. 
  
Para admitir propiedades con nombre, un proveedor de servicios implementa dos métodos [(IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) e [IMAPIProp::GetNamesFromIDs)](imapiprop-getnamesfromids.md) para traducir entre nombres e identificadores y para permitir que sus métodos [IMAPIProp::GetProps](imapiprop-getprops.md)[IMAPIProp::SetProps](imapiprop-setprops.md) recuperen y modifiquen propiedades con identificadores en el intervalo de propiedades con nombre. El intervalo de identificadores de propiedad con nombre está entre 0x8000 y 0xFFFE. 
  
Cualquier objeto que implemente la **interfaz IMAPIProp** puede admitir propiedades con nombre. Los proveedores de libretas de direcciones que permiten que las entradas de otros proveedores se copien en sus contenedores y proveedores de almacenamiento de mensajes que se pueden usar para crear tipos de mensajes arbitrarios son necesarios para proporcionar esta compatibilidad. Es una opción para todos los demás proveedores de servicios. Los proveedores que no admiten propiedades con nombre devuelven MAPI_E_NO_SUPPORT de los **métodos GetIDsFromNames** y **GetNamesFromIDs** y no establecen ninguna propiedad con identificadores de 0x8000 o superior, devolviendo MAPI_E_UNEXPECTED en **el SPropProblemarray**.
  
La creación de nombres para propiedades es una forma de que los clientes definan nuevas propiedades para las clases de mensajes existentes o personalizadas. Los proveedores de servicios pueden usar propiedades con nombre para exponer características únicas de sus sistemas de mensajería. Otro uso para las propiedades con nombre es proporcionar una forma alternativa de hacer referencia a propiedades con identificadores por debajo de 0x8000. 
  
Por ejemplo, un cliente podría usar código similar al siguiente código para recuperar los nombres de todas las propiedades con nombre de un objeto:
  
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

Para solicitar todos los nombres del conjunto PS_PUBLIC_STRINGS propiedades, un cliente reemplazaría el valor NULL en el parámetro del conjunto de propiedades en PS_PUBLIC_STRINGS como se muestra a continuación: 
  
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

