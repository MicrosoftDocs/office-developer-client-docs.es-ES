---
title: Implementación de objetos MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b1ee2533-8077-4976-846b-d42d148bf8c6
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c0d67d10d54591de926724cbf594a44f17e9ea14
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310174"
---
# <a name="implementing-mapi-objects"></a>Implementación de objetos MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los objetos MAPI se pueden implementar mediante clases de C++ o estructuras de datos C, según el idioma y el conjunto de API que use un cliente o un proveedor de servicios. Los proveedores de servicios pueden escribirse en C o C++ con la interfaz del proveedor de servicios MAPI; las aplicaciones cliente también pueden usar C o C++. Si es posible, los clientes y los proveedores de servicios que usan la interfaz de programación orientada a objetos deben usar C++. 
  
C++ es la opción preferida porque MAPI es una tecnología orientada a objetos y C++ se presta más fácilmente al desarrollo orientado a objetos. El código resultante es más sencillo y más sencillo, lo que facilita el mantenimiento. La documentación de MAPI se ha escrito principalmente para los programadores de C++; todas las descripciones de sintaxis para los métodos de interfaz MAPI de esta referencia están en C++.
  
Los desarrolladores pueden usar las herramientas de desarrollo de Microsoft Visual Studio y de terceros para desarrollar soluciones que llaman a MAPI. Tenga en cuenta que los desarrolladores deben usar C o C++ no administrado, pero no C++ administrado para escribir soluciones MAPI.
  
Cuando se implementa un objeto MAPI, un cliente o proveedor de servicios crea código para todos los métodos de la interfaz, el código para los métodos privados específicos de la implementación y el código para admitir los miembros de datos privados para mantener la información de estado. El código de los métodos de interfaz debe seguir las especificaciones publicadas por MAPI que documentan el comportamiento esperado. 
  
Hay muchas macros en el archivo de encabezado Mapidefs. h y en los archivos de encabezado OLE que los clientes y los proveedores de servicios de cualquiera de los idiomas pueden usar para ayudarles con sus definiciones de objetos MAPI. Por ejemplo, hay una macro para definir los métodos de cada una de las interfaces MAPI. La macro para definir los métodos de la interfaz [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) aparece en Mapidefs. h de la siguiente manera: 
  
```cpp
#define MAPI_IUNKNOWN_METHODS(IPURE)          \
    MAPIMETHOD(QueryInterface)                \
        (THIS_ REFIID riid, LPVOID FAR * ppvObj) IPURE;    \
    MAPIMETHOD_(ULONG,AddRef)  (THIS) IPURE;               \
    MAPIMETHOD_(ULONG,Release) (THIS) IPURE;   \
 
```

## <a name="see-also"></a>Vea también



[Introducción a la interfaz y el objeto MAPI](mapi-object-and-interface-overview.md)

