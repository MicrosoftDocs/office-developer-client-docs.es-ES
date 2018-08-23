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
ms.openlocfilehash: 5a6ba7af5e497ba59b43e9b80cfc9595961ed10e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579546"
---
# <a name="mapi-named-properties"></a>Con el nombre de las propiedades de MAPI
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI proporciona una utilidad para asignar nombres a las propiedades, para asignar estos nombres a los identificadores únicos y para realizar esta asignación persistente. Persistent asignación de nombre a identificador se asegura de que los nombres de propiedad siguen siendo válidos en todas las sesiones.
  
Para definir una propiedad con nombre, un proveedor de servicio o cliente realiza un nombre y lo almacena en una estructura [MAPINAMEID](mapinameid.md) . Debido a que los nombres se componen de un identificador único global de 32 bits, o GUID y puede ser una cadena o numérico valor de carácter Unicode, los creadores de propiedades con nombre pueden crear nombres descriptivos sin miedo de duplicación. Los nombres son únicos y se pueden usar sin tener en cuenta el valor de sus identificadores. 
  
Para admitir las propiedades con nombre, un proveedor de servicios implementa dos métodos: [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) y [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) — para traducir entre los nombres y los identificadores y permitir su [IMAPIProp::GetProps](imapiprop-getprops.md) [ IMAPIProp::SetProps](imapiprop-setprops.md) métodos para recuperar y modificar las propiedades con los identificadores en el intervalo de la propiedad con nombre. El intervalo para los identificadores de propiedad con nombre se encuentra entre 0 x 8000 y 0xFFFE. 
  
Cualquier objeto que implementa la interfaz **IMAPIProp** puede admitir propiedades con nombre. Los proveedores de la libreta de direcciones que permiten las entradas de otros proveedores que se copiarán a sus contenedores y mensaje almacenan proveedores que se pueden usar para crear tipos de mensaje arbitrario se necesitan para proporcionar este soporte técnico. Es una opción para todos los demás proveedores de servicio. Los proveedores que no admiten las propiedades con nombre devuelven MAPI_E_NO_SUPPORT de los métodos **a GetIDsFromNames** y **GetNamesFromIDs** y denegación establecer las propiedades con identificadores de 0 x 8000 o mayor, devolución MAPI_E_UNEXPECTED en la ** SPropProblemarray**.
  
Creación de nombres de propiedades es una forma para que los clientes definir nuevas propiedades para las clases de mensajes existente o personalizado. Proveedores de servicios pueden usar propiedades con nombre para exponer características exclusivas de los sistemas de mensajería. Aún otro uso de las propiedades con nombre consiste en proporcionar una forma alternativa de hacer referencia a las propiedades con identificadores por debajo de 0 x 8000. 
  
Por ejemplo, un cliente podría utilizar código similar al siguiente código para recuperar los nombres de todas las propiedades de un objeto con nombre:
  
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

Para solicitar todos los nombres desde el conjunto de propiedades PS_PUBLIC_STRINGS, un cliente podría reemplazar el valor NULL en el parámetro del conjunto de propiedad a PS_PUBLIC_STRINGS como se indica a continuación: 
  
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

