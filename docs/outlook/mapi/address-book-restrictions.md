---
title: Restricciones de la libreta de direcciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ace8c03-45a7-484b-8c12-516ac0e40dc2
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: b8ad765a2bbd3aafd87a7eff79993978816729b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816402"
---
# <a name="address-book-restrictions"></a>Restricciones de la libreta de direcciones

  
  
**Se aplica a**: Outlook 
  
Los proveedores de la libreta de direcciones son necesarios para admitir tres tipos de restricciones en las tablas de contenido de sus contenedores:
  
- Restricciones de nombre ambiguo (propiedad)
    
- Restricciones de propiedad de clave de instancia
    
- Restricciones de contenido de nombre para mostrar con prefijo
    
Restricciones de nombre ambiguo son restricciones de propiedad con la propiedad **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) para que coincida con los nombres de los destinatarios con las entradas de los contenedores de la libreta de direcciones. La restricción de propiedad **PR_ANR** es un tipo "mejor adivinar" de búsqueda mediante el cual los proveedores de la libreta de direcciones pueden elegir la propiedad coincidente que funciona mejor para su contenedor. Por ejemplo, un proveedor de libreta de direcciones podría implementar la restricción **PR_ANR** por nombres de los destinatarios que coinciden con respecto a la propiedad **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) de cada entrada de contenedor mientras que otro proveedor puede usar **PR_DISPLAY _NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).
  
MAPI, se recomienda que las implementaciones de la restricción de **PR_ANR** alcanzar un equilibrio entre la satisfacción del usuario y un rendimiento adecuado. Se puede reducir la satisfacción de los usuarios cuando un proveedor de la libreta de direcciones implementa la restricción de tal forma que se encuentran muy pocas o demasiadas coincidencias. Algunos proveedores de libreta de direcciones compatible con lo que se conoce como un nombre distintivo (DN) o comunes, que no es que se pueden mostrar en un cuadro de diálogo pero puede coincidir con una restricción de nombre ambiguo. 
  
Es posible una implementación típica analizar el nombre para mostrar del destinatario en palabras, que coinciden con cualquier entrada que contiene todas las palabras. Atención a detalles como sensibilidad a la posición de word, si se hacen coincidir las palabras no consecutivos y la elección de los caracteres separadores pueden variar. Por ejemplo, si el nombre que se va a resolver es "Bill L", una restricción **PR_ANR** típica seleccionar las siguientes entradas como coincidentes: 
  
- Billy Larson
    
- Bill Lee
    
- Bill Logan Jr. 
    
- Sam Bill Lee
    
Restricciones de clave de instancia o restricciones de propiedad **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), se utilizan en la implementación de cuadros de lista que se usan en las aplicaciones cliente para ver las tablas MAPI. Algunas implementaciones de cuadro de lista permiten a los usuarios realizar varias selecciones, desplazarse hacia arriba o hacia abajo y devolución para el primer elemento seleccionan. Para implementar este comportamiento, los clientes llaman [IMAPITable:: FindRow](imapitable-findrow.md), pasando una restricción de propiedad en la propiedad **PR_INSTANCE_KEY** al método. Los proveedores de la libreta de direcciones son necesarios para admitir esta restricción. 
  
Otra característica de cuadros de lista que se usa para la visualización de la tabla es la capacidad para colocar el cursor en función de un conjunto de caracteres de prefijo. Como el usuario empieza a escribir caracteres de prefijo, el cliente mueve el cursor al primer elemento que comienza con estos caracteres. Los clientes de implementan esta característica con una restricción de contenido en función de la propiedad **PR_DISPLAY_NAME** y el nivel de aproximada de FL_PREFIX. 
  
## <a name="see-also"></a>Ver también



[Tablas MAPI](mapi-tables.md)

