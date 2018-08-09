---
title: Implementar objetos MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b1ee2533-8077-4976-846b-d42d148bf8c6
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d53304dd74a0e54974d479c66637079cd48b2fc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817685"
---
# <a name="implementing-mapi-objects"></a>Implementar objetos MAPI

  
  
**Hace referencia a**: Outlook 
  
Objetos MAPI se pueden implementar mediante el uso de clases de C++ o C las estructuras de datos, dependiendo del lenguaje y la API de establece a un cliente o está usando el proveedor de servicios. Proveedores de servicios se pueden escribir en C o C++ con la interfaz de proveedor de servicio MAPI; También pueden usar las aplicaciones cliente de C o C++. Si es posible, los clientes y proveedores de servicios que usan la interfaz de programación orientada a objetos deben usar C++. 
  
C++ es la opción preferida porque MAPI es una tecnología orientada a objetos y C++ se presta más fácilmente a desarrollo orientado a objetos. El código resultante es más sencilla y directa, haciendo que sea más fácil de mantener. La documentación de MAPI está escrita principalmente para programadores de C++; todas las descripciones de sintaxis para los métodos de interfaz MAPI en esta referencia se encuentran en C++.
  
Los desarrolladores pueden usar Microsoft Visual Studio y herramientas de desarrollo de aplicaciones de terceros para desarrollar soluciones que llamar a MAPI. Tenga en cuenta que los desarrolladores deben utilizar C o C++ no administrado, pero no administran de C++ para escribir soluciones MAPI.
  
Cuando se implementa un objeto MAPI, un proveedor de servicio o cliente crea código para todos los métodos de la interfaz, el código para los métodos privados que son específicos de la implementación y el código para admitir los miembros de datos privados para el mantenimiento de información de estado. El código para los métodos de interfaz debe seguir las especificaciones publicadas por MAPI que documentar el comportamiento esperado. 
  
Hay muchas macros en el archivo de encabezado Mapidefs.h y los archivos de encabezado OLE que pueden usar los clientes y proveedores de servicio en cualquier idioma para ayudarles con sus definiciones de objetos MAPI. Por ejemplo, hay una macro para definir los métodos de cada una de las interfaces MAPI. La macro para definir los métodos de la interfaz [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) aparece en Mapidefs.h como se indica a continuación: 
  
```cpp
#define MAPI_IUNKNOWN_METHODS(IPURE)          \
    MAPIMETHOD(QueryInterface)                \
        (THIS_ REFIID riid, LPVOID FAR * ppvObj) IPURE;    \
    MAPIMETHOD_(ULONG,AddRef)  (THIS) IPURE;               \
    MAPIMETHOD_(ULONG,Release) (THIS) IPURE;   \
 
```

## <a name="see-also"></a>Vea también



[Objeto MAPI e Introducción a la interfaz](mapi-object-and-interface-overview.md)

