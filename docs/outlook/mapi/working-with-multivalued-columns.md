---
title: Trabajar con columnas multivalor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 911a41c3-c10f-4473-8853-fafb56b721ba
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 34f19e279c86e0c0856d242cf2aa13d744d46f13
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420188"
---
# <a name="working-with-multivalued-columns"></a>Trabajar con columnas multivalor

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una columna multivalor contiene los datos de una propiedad multivalor, que es una propiedad que tiene una matriz de valores del tipo base en lugar de un valor único. Dado que ninguna de las tablas incluye propiedades multivalor en sus conjuntos de columnas predeterminados, las propiedades multivalor se incluyen en una tabla solo si el usuario de la tabla lo solicita. 
  
Las columnas multivalor se pueden mostrar en tablas:
  
- En una sola fila, con todos los valores de propiedad que aparecen en la instancia de una sola columna. Este valor es predeterminado.
    
    - O bien:
    
- En una serie de filas, con una fila para cada uno de los valores de propiedad. Cada valor único aparece en la columna en su propia fila y hay tantas filas como valores en la propiedad multivalor. Cada fila tiene un valor único para **la propiedad PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), pero los mismos valores para las otras columnas. Si una fila contiene más de una columna con varios valores, por ejemplo, dos columnas con valores  _M_ y  _N_ respectivamente, las instancias  _M \* N_ de la fila aparecen en la tabla. 
    
Un usuario de tabla solicita el tipo de presentación no predeterminado llamando al método [IMAPITable::SetColumns](imapitable-setcolumns.md) con la marca MVI_FLAG establecida en el tipo de propiedad de la columna multivalor. El MVI_FLAG marca es una constante definida como el resultado de combinar las marcas MV_FLAG y MV_INSTANCE con una operación **lógica OR.** Además de usarse en **SetColumns,** MVI_FLAG también se puede pasar a [IMAPITable::SortTable](imapitable-sorttable.md) en el parámetro _lpSortCriteria_ y [IMAPITable::Restrict](imapitable-restrict.md) en el miembro **ulPropTag** del parámetro _lpRestriction._ Cuando se pasa el MVI_FLAG, **SortTable** funciona de forma similar a **SetColumns**, agregando una fila por cada valor de la columna multivalor y ordenando los valores únicos en las instancias. Se agrega una fila por cada valor. 
  
 **Sin** embargo, restringir no expande la columna multivalor en filas calculadas adicionales. Una columna multivalor con el conjunto MVI_FLAG indica al proveedor de servicios que use esa columna para restringir la tabla. Si hay un valor de propiedad en la restricción, debe ser una etiqueta de propiedad de valor único idéntica a la que [devolvería IMAPITable::QueryRows](imapitable-queryrows.md) para la columna. 
  
Los implementadores de tabla solo son necesarios para admitir el tipo predeterminado de presentación y pueden devolver el valor MAPI_E_TOO_COMPLEX cuando un llamador solicita la otra alternativa. La capacidad de admitir ambos tipos de presentación es lo más importante para los proveedores de almacenamiento de mensajes que implementan tablas de contenido de carpetas. 
  
## <a name="see-also"></a>Consulte también



[Tablas MAPI](mapi-tables.md)

