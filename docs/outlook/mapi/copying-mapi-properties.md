---
title: Copiar las propiedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a52f4bcd-6e17-4623-a469-53be1f2758b1
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2f9ee7221f523d7c92d91746f5cd719fad821a27
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816596"
---
# <a name="copying-mapi-properties"></a>Copiar las propiedades MAPI

  
  
**Hace referencia a**: Outlook 
  
Los clientes y proveedores de servicios pueden copiar una o varias de las propiedades de un objeto con los siguientes métodos de **IMAPIProp** y funciones de la API: 
  
- El método [IMAPIProp::CopyTo](imapiprop-copyto.md) copia todas las propiedades de un objeto a otro objeto, y, opcionalmente, excluyendo las propiedades seleccionadas. **CopyTo** se usa para copiar o mover cualquier tipo de objeto. 
    
- El método [IMAPIProp::CopyProps](imapiprop-copyprops.md) copia las propiedades seleccionadas de un objeto. **CopyProps** se usa principalmente con los mensajes. Cuando un cliente crea una copia de un mensaje o una respuesta, reenvío controladores **CopyProps** copiar las propiedades adecuadas del mensaje original. 
    
- La función [PropCopyMore](propcopymore.md) copia un valor de propiedad único de una ubicación a otra. Utilice **PropCopyMore** con precaución. Es posible, al copiar un valor en un momento: para asignar muchos bloques pequeños de memoria y hacer que la memoria a fragmentar. 
    
- La función [ScCopyProps](sccopyprops.md) copia valores de propiedad de forma masiva. **ScCopyProps** puede copiar los valores de propiedad que se han generado desde disjuntos bloques de memoria. Devuelve una matriz de propiedad nuevo. 
    
- Si la matriz de propiedad devuelta por **ScCopyProps** es se almacenen en el disco, utilice la función [ScRelocProps](screlocprops.md) para ajustar los punteros. **ScRelocProps** debe llamarse dos veces; una vez para ajustar las direcciones antes de escribir la operación de datos y, a continuación, vuelva a durante la operación de lectura. La función **ScRelocProps** se supone que la matriz de valores de propiedad se ha asignado originalmente en una única asignación. 
    
Las funciones de la API que se describen en las propiedades de copia de lista anterior en la memoria, en lugar de un objeto a otro objeto. Estas funciones se admiten actualmente, pero es posible que no se admite en una futura versión.
  
## <a name="see-also"></a>Vea también



[Información general sobre MAPI (propiedad)](mapi-property-overview.md)

