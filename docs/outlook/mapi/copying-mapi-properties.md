---
title: Copia de las propiedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a52f4bcd-6e17-4623-a469-53be1f2758b1
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ae8e553cf2e19ae1ba06ca09aad84eae9f7d1238
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333078"
---
# <a name="copying-mapi-properties"></a>Copia de las propiedades MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los clientes y los proveedores de servicios pueden copiar una o varias de las propiedades de un objeto con los siguientes métodos de **IMAPIProp** y funciones API: 
  
- El método [IMAPIProp:: CopyTo](imapiprop-copyto.md) copia todas las propiedades de un objeto en otro objeto, opcionalmente excluyendo las propiedades seleccionadas. **CopyTo** se usa para copiar o mover cualquier tipo de objeto. 
    
- El método [IMAPIProp:: CopyProps](imapiprop-copyprops.md) copia las propiedades seleccionadas de un objeto. **CopyProps** se usa principalmente con mensajes. Cuando un cliente crea una copia reenviada de un mensaje o una respuesta, **CopyProps** controla la copia de las propiedades adecuadas del mensaje original. 
    
- La función [PropCopyMore](propcopymore.md) copia un único valor de propiedad de una ubicación a otra. Use **PropCopyMore** con cuidado. Es posible, cuando se copia un valor cada vez, para asignar muchos bloques de memoria pequeños y hacer que la memoria se fragmente. 
    
- La función [ScCopyProps](sccopyprops.md) copia los valores de propiedad en masa. **ScCopyProps** puede copiar los valores de propiedad que se han generado desde bloques de memoria inconexos. Devuelve una nueva matriz de propiedades. 
    
- Si la matriz de propiedades devuelta por **ScCopyProps** se va a almacenar en el disco, use la función [ScRelocProps](screlocprops.md) para ajustar los punteros. Se debe llamar dos veces a **ScRelocProps** ; una vez para ajustar las direcciones antes de escribir la operación de datos y de nuevo durante la operación de lectura. La función **ScRelocProps** presupone que la matriz de valores de propiedad se asignó originalmente en una única asignación. 
    
Las funciones de la API descritas en la lista anterior copian las propiedades de la memoria en lugar de hacerlo de un objeto a otro objeto. Actualmente, estas funciones se admiten, pero es posible que no se admitan en una versión futura.
  
## <a name="see-also"></a>Vea también



[Información general sobre MAPI (propiedad)](mapi-property-overview.md)

