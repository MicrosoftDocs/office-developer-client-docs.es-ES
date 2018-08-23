---
title: Identificadores de entrada a corto plazo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 948e007a-ad68-4abd-9720-204c6584beb5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 03352b55589138d406ad3e4ee0756fc44bca8c78
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580617"
---
# <a name="short-term-entry-identifiers"></a>Identificadores de entrada a corto plazo

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cuando el identificador debe crearse rápidamente y no es necesario que por última vez a través de tiempo o distancia, se asigna un identificador de entrada a corto plazo por un proveedor de servicios a un objeto. Se garantiza que la exclusividad de un identificador de entrada a corto plazo sólo a través de la vida de la sesión actual en la estación de trabajo actual. Normalmente, un identificador de entrada a corto plazo es válido sólo hasta que se libera el objeto que lo representa. 
  
Los identificadores de entrada a corto plazo se asignan a las filas en las tablas y las entradas de los cuadros de diálogo, cuando sea necesario proporcionar rápidamente los datos para la exploración. Por ejemplo, los proveedores de almacén de mensajes asignan los identificadores de entrada a corto plazo a las filas de los mensajes en una tabla de contenido a los destinatarios en una tabla de destinatarios. 

Los clientes pueden usar estos identificadores de entrada a corto plazo para abrir los objetos representados por las filas de tabla. Sin embargo, a diferencia de los identificadores de entrada a largo plazo que pueden usarse con cualquiera de los métodos de **OpenEntry** , los identificadores de entrada a corto plazo deben usarse con el método de **OpenEntry** del contenedor. 
  
## <a name="implementing-short-term-entry-identifiers"></a>Implementación de los identificadores de entrada a corto plazo

Las formas más comunes para implementar los identificadores de entrada a corto plazo son las siguientes:
  
- Hacer que los identificadores de entrada a corto plazo la misma que los identificadores a largo plazo, dejando todas las marcas no definidas. 
    
- Hacer que los identificadores de entrada a corto plazo distintos de los identificadores a largo plazo, configuración de todas las marcas. 
    
Los clientes pueden identificar un identificador de entrada a corto plazo del segundo tipo examinando su miembro **abFlags** como se indica a continuación: 
  
```cpp
abFlags[0] = 0xFF;
 
```

Algunos proveedores de servicios desactive uno o más indicadores para crear los identificadores de entrada a corto plazo que tienen validez mayor. Por ejemplo, los siguientes miembros **abFlags** representan los identificadores de entrada a corto plazo que se pueden usar para varios días o para varias sesiones: 
  
```cpp
abFlags[0] = 0xFF & ~MAPI_NOW;
abFlags[0] = 0xFF & ~MAPI_THISSESSION;
 
```

Los clientes rápidamente adquieren, usarán y descartar los identificadores de entrada a corto plazo. La mayor parte, se pueden usar en la misma manera que los identificadores de entrada a largo plazo. Se puedan recuperar de una tabla, se pasan al método **OpenEntry** y, en comparación con el método **CompareEntryIDs** . La única excepción es que nunca se devuelven desde el método [IMAPIProp::GetProps](imapiprop-getprops.md) . Las propiedades devueltas desde **GetProps** siempre son identificadores de entrada a largo plazo. 
  
## <a name="see-also"></a>Recursos adicionales

- [Identificadores de entrada MAPI](mapi-entry-identifiers.md)

