---
title: Copiar propiedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a52f4bcd-6e17-4623-a469-53be1f2758b1
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ae8e553cf2e19ae1ba06ca09aad84eae9f7d1238
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415050"
---
# <a name="copying-mapi-properties"></a>Copiar propiedades MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los clientes y proveedores de servicios pueden copiar una o varias de las propiedades de un objeto con los siguientes métodos **IMAPIProp** y funciones api: 
  
- El [método IMAPIProp::CopyTo](imapiprop-copyto.md) copia todas las propiedades de un objeto en otro objeto, excluyendo opcionalmente las propiedades seleccionadas. **CopyTo** se usa para copiar o mover cualquier tipo de objeto. 
    
- El [método IMAPIProp::CopyProps](imapiprop-copyprops.md) copia las propiedades seleccionadas de un objeto. **CopyProps se** usa principalmente con mensajes. Cuando un cliente crea una copia reenviada de un mensaje o una respuesta, **CopyProps** controla la copia de las propiedades apropiadas del mensaje original. 
    
- La [función PropCopyMore](propcopymore.md) copia un único valor de propiedad de una ubicación a otra. Use **PropCopyMore** con precaución. Es posible, al copiar un valor cada vez, asignar muchos bloques pequeños de memoria y hacer que la memoria se fragmente. 
    
- La [función ScCopyProps](sccopyprops.md) copia los valores de propiedad de forma masiva. **ScCopyProps puede** copiar valores de propiedad creados a partir de bloques de memoria diferentes. Devuelve una nueva matriz de propiedades. 
    
- Si la matriz de propiedades devuelta por **ScCopyProps** se va a almacenar en el disco, use la función [ScRelocProps](screlocprops.md) para ajustar los punteros. Se debe llamar dos veces a **ScRelocProps;** una vez para ajustar las direcciones antes de escribir la operación de datos y, a continuación, otra vez durante la operación de lectura. La **función ScRelocProps** supone que la matriz de valores de propiedad se asignó originalmente en una única asignación. 
    
Las funciones api descritas en la lista anterior copian propiedades en la memoria en lugar de desde un objeto a otro. Actualmente, estas funciones se admiten, pero es posible que no se puedan usar en una versión futura.
  
## <a name="see-also"></a>Vea también



[Información general sobre MAPI (propiedad)](mapi-property-overview.md)

