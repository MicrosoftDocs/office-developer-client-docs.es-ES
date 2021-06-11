---
title: Restricciones de libreta de direcciones
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
# <a name="address-book-restrictions"></a>Restricciones de libreta de direcciones

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los proveedores de libreta de direcciones deben admitir tres tipos de restricciones en las tablas de contenido de sus contenedores:
  
- Restricciones de propiedad de nombre ambiguo
    
- Restricciones de propiedades clave de instancia
    
- Restricciones de contenido de nombre para mostrar con prefijo
    
Las restricciones de nombres ambiguos son restricciones de propiedad que usan la propiedad **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) para hacer coincidir los nombres de los destinatarios con las entradas de los contenedores de libreta de direcciones. La **PR_ANR** propiedad es un tipo de búsqueda de "mejor conjetura" por el que los proveedores de libreta de direcciones pueden elegir la propiedad que coincida mejor para su contenedor. Por ejemplo, un proveedor de libreta de direcciones podría implementar la restricción **de PR_ANR** al coincidir los nombres de destinatarios con la propiedad **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) de cada entrada contenedora, mientras que otro proveedor podría usar **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).
  
MAPI recomienda que las implementaciones de la **restricción PR_ANR** equilibrio entre el rendimiento adecuado y la satisfacción del usuario. La satisfacción del usuario puede verse comprometida cuando un proveedor de libreta de direcciones implementa la restricción de forma que se encuentran demasiadas coincidencias o demasiadas. Algunos proveedores de libreta de direcciones admiten lo que se conoce como un nombre distintivo o común que no se puede mostrar en un cuadro de diálogo, pero que puede coincidir con una restricción de nombre ambigua. 
  
Una implementación típica puede ser analizar el nombre para mostrar del destinatario en palabras, que coincida con cualquier entrada que contenga todas las palabras. Atención a detalles como la confidencialidad de la posición de la palabra, si se coinciden palabras no coincidentes y la elección de caracteres separadores puede variar. Por ejemplo, si el nombre que se va  a resolver es "Bill L", una restricción de PR_ANR típica seleccionaría las siguientes entradas como coincidencia: 
  
- Billy Larson
    
- Bill Lee
    
- Bill Logan Jr. 
    
- Sam Bill Lee
    
Las restricciones de clave de instancia **o PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) se usan en la implementación de cuadros de lista que se usan en aplicaciones cliente para ver tablas MAPI. Algunas implementaciones de cuadro de lista permiten a los usuarios realizar varias selecciones, desplazarse hacia arriba o hacia abajo y volver al primer elemento seleccionado. Para implementar este comportamiento, los clientes llaman a [IMAPITable::FindRow](imapitable-findrow.md), pasando una restricción de propiedad en la propiedad **PR_INSTANCE_KEY** al método. Los proveedores de libreta de direcciones son necesarios para admitir esta restricción. 
  
Otra característica de los cuadros de lista usados para la visualización de tablas es la capacidad de colocar el cursor en función de un conjunto de caracteres de prefijo. A medida que el usuario empieza a escribir caracteres de prefijo, el cliente mueve el cursor al primer elemento que comienza con estos caracteres. Los clientes implementan esta característica con una restricción de contenido basada en la **propiedad PR_DISPLAY_NAME** y el FL_PREFIX nivel difuso. 
  
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

