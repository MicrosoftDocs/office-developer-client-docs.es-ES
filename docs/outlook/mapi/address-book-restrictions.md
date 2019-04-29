---
title: Restricciones de la libreta de direcciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ace8c03-45a7-484b-8c12-516ac0e40dc2
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7419c174c1f68653794c2dbd836577e8dd3e596e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432803"
---
# <a name="address-book-restrictions"></a>Restricciones de la libreta de direcciones

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los proveedores de libreta de direcciones deben admitir tres tipos de restricciones en las tablas de contenido de sus contenedores:
  
- Restricciones de propiedad de nombre ambiguo
    
- Restricciones de propiedad de clave de instancia
    
- Restricciones de contenido de nombre para mostrar con prefijo
    
Las restricciones de nombre ambiguo son restricciones de propiedad que usan la propiedad **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) para hacer coincidir los nombres de los destinatarios con las entradas de los contenedores de la libreta de direcciones. La restricción de propiedad **PR_ANR** es un tipo de "mejor estimación" de la búsqueda, en la que los proveedores de libreta de direcciones pueden elegir la propiedad correspondiente que funciona mejor para su contenedor. Por ejemplo, un proveedor de la libreta de direcciones puede implementar la restricción **PR_ANR** al hacer coincidir los nombres de los destinatarios con la propiedad **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) de cada entrada de contenedor, mientras que otro proveedor puede usar **PR_DISPLAY _NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).
  
MAPI recomienda que las implementaciones de la restricción **PR_ANR** se ajusten a un equilibrio entre el rendimiento y la satisfacción del usuario adecuados. La satisfacción del usuario se puede ver comprometida cuando un proveedor de la libreta de direcciones implementa la restricción de manera que se encuentran muy pocas o demasiadas coincidencias. Algunos proveedores de libretas de direcciones admiten lo que se conoce como un nombre completo, o común, que no se puede reproducir en un cuadro de diálogo, pero que puede coincidir con una restricción de nombre ambiguo. 
  
Una implementación típica podría ser analizar el nombre para mostrar del destinatario en palabras, haciendo coincidir cualquier entrada que contenga todas las palabras. Atención a los detalles, como la sensibilidad a la posición de la palabra, si las palabras no consecutivas coinciden y la elección de caracteres separadores puede variar. Por ejemplo, si el nombre que se va a resolver es "Bill L", una restricción **PR_ANR** típica seleccionaría las siguientes entradas como coincidencia: 
  
- Billy Larson
    
- Bill Lucas
    
- Bill Logan Jr. 
    
- Bill Lucas de Sam
    
Las restricciones de clave de instancia o las restricciones de propiedad **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) se usan en la implementación de cuadros de lista que se usan en aplicaciones cliente para ver tablas MAPI. Algunas implementaciones de cuadros de lista permiten a los usuarios realizar selecciones múltiples, desplazarse hacia arriba o hacia abajo y volver al primer elemento seleccionado. Para implementar este comportamiento, los clientes llaman a [IMAPITable:: FindRow](imapitable-findrow.md), pasando una restricción de propiedad en la propiedad **PR_INSTANCE_KEY** al método. Es necesario que los proveedores de libreta de direcciones admitan esta restricción. 
  
Otra característica de los cuadros de lista usados para la visualización de tablas es la capacidad de colocar el cursor en función de un conjunto de caracteres de prefijo. A medida que el usuario empieza a escribir los caracteres de prefijo, el cliente mueve el cursor al primer elemento que comienza con estos caracteres. Los clientes implementan esta característica con una restricción de contenido basada en la propiedad **PR_DISPLAY_NAME** y el nivel de aproximación FL_PREFIX. 
  
## <a name="see-also"></a>Ver también



[Tablas MAPI](mapi-tables.md)

