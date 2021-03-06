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
ms.openlocfilehash: 1b361e025b631418eb63c5c74da264beadec2974
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439565"
---
# <a name="short-term-entry-identifiers"></a>Identificadores de entrada a corto plazo

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un proveedor de servicios asigna un identificador de entrada a corto plazo a un objeto cuando el identificador debe construirse rápidamente y no es necesario que dure con el tiempo o la distancia. La singularidad de un identificador de entrada a corto plazo solo se garantiza durante la vida de la sesión actual en la estación de trabajo actual. Normalmente, un identificador de entrada a corto plazo solo es válido hasta que se libera el objeto que representa. 
  
Los identificadores de entrada a corto plazo se asignan a las filas de las tablas y a las entradas de los cuadros de diálogo, donde es necesario proporcionar datos rápidamente para la exploración. Por ejemplo, los proveedores de almacenes de mensajes asignan identificadores de entrada a corto plazo a filas de mensajes de una tabla de contenido y a destinatarios de una tabla de destinatarios. 

Los clientes pueden usar estos identificadores de entrada a corto plazo para abrir los objetos representados por las filas de tabla. Sin embargo, a diferencia de los identificadores de entrada a largo plazo que se pueden usar con cualquiera de los métodos **OpenEntry,** los identificadores de entrada a corto plazo deben usarse con el método **OpenEntry del** contenedor. 
  
## <a name="implementing-short-term-entry-identifiers"></a>Implementación de identificadores de entrada a corto plazo

Las formas más comunes de implementar identificadores de entrada a corto plazo son las siguientes:
  
- Hacer que los identificadores de entrada a corto plazo sea igual que los identificadores a largo plazo, dejando todas las marcas sin marcar. 
    
- Hacer que los identificadores de entrada a corto plazo se diferencian de los identificadores a largo plazo, estableciendo todas las marcas. 
    
Los clientes pueden identificar un identificador de entrada a corto plazo del segundo tipo examinando su **miembro abFlags** de la siguiente manera: 
  
```cpp
abFlags[0] = 0xFF;
 
```

Algunos proveedores de servicios borran una o más marcas para crear identificadores de entrada a corto plazo con mayor validez. Por ejemplo, los siguientes **miembros abFlags** representan identificadores de entrada a corto plazo que se pueden usar durante varios días o para varias sesiones: 
  
```cpp
abFlags[0] = 0xFF & ~MAPI_NOW;
abFlags[0] = 0xFF & ~MAPI_THISSESSION;
 
```

Los clientes adquieren, usan y descartan rápidamente identificadores de entrada a corto plazo. En su mayoría, se pueden usar de la misma manera que los identificadores de entrada a largo plazo. Se pueden recuperar de una tabla, pasar al método **OpenEntry** y compararlos con el **método CompareEntryIDs.** La única excepción es que nunca se devuelven desde el [método IMAPIProp::GetProps.](imapiprop-getprops.md) Las propiedades **devueltas de GetProps** siempre son identificadores de entrada a largo plazo. 
  
## <a name="see-also"></a>Vea también

- [Identificadores de entrada MAPI](mapi-entry-identifiers.md)

