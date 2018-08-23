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
ms.openlocfilehash: 78f6083cf17bb21152df1a7ea09825f3be7f0e37
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572945"
---
# <a name="working-with-multivalued-columns"></a>Trabajar con columnas multivalor

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una columna multivalor contiene los datos de una propiedad multivalor, que es una propiedad que tiene una matriz de valores del tipo base en lugar de un solo valor. Debido a que ninguna de las tablas incluyen propiedades multivalor en sus conjuntos de columnas predeterminados, se incluyen propiedades multivalor en una tabla sólo si lo solicita el usuario de la tabla. 
  
Columnas con varios valores se pueden mostrar en las tablas:
  
- En una sola fila, con todos los valores de propiedad que aparecen en la instancia de una sola columna. Esto es el valor predeterminado.
    
    - O bien -
    
- En una serie de filas, con una fila para cada uno de los valores de propiedad. Cada valor único aparece en la columna en su propia fila con allí es como número de filas como allí es valores de la propiedad multivalor. Cada fila tiene un valor único para la propiedad **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), pero los mismos valores para las demás columnas. Si una fila contiene más de una columna con varios valores, por ejemplo, dos columnas con _M_ y _N_ valores respectivamente, a continuación, _M\*N_ instancias de la fila que aparecen en la tabla. 
    
Un usuario de la tabla solicita el tipo que no sean predeterminadas de presentación llamando al método [IMAPITable::SetColumns](imapitable-setcolumns.md) con el indicador MVI_FLAG establecido en el tipo de propiedad de la columna multivalor. El indicador MVI_FLAG es una constante definida como resultado de la combinación de los indicadores MV_FLAG y MV_INSTANCE con una operación **OR** lógica. Además de su uso en **SetColumns**, MVI_FLAG también se pueden pasar a [SortTable](imapitable-sorttable.md) en el parámetro _lpSortCriteria_ e [IMAPITable:: Restrict](imapitable-restrict.md) en el miembro **ulPropTag** de la _lpRestriction_ parámetro. Cuando se pasa el MVI_FLAG, **SortTable** realiza de forma similar a **SetColumns**, adición de una fila por cada valor en la columna multivalor y ordenar según los valores de las instancias de único. Se agrega una fila para cada valor. 
  
 **Restrict**, sin embargo, no se expande la columna multivalor en filas calculadas adicionales. Una columna multivalor con el conjunto MVI_FLAG indica que el proveedor de servicios para usar esa columna en la restricción a la tabla. Si hay un valor de propiedad en la restricción, debe ser una etiqueta de propiedad de valor único idéntica al que devolvería [IMAPITable:: QueryRows](imapitable-queryrows.md) para la columna. 
  
Tabla sólo son necesarios para admitir el tipo de presentación predeterminado e implementadores pueden devolver el valor MAPI_E_TOO_COMPLEX cuando un llamador solicita la otra alternativa. La capacidad para admitir ambos tipos de presentación es más importante para los proveedores de almacén de mensaje que se implementan las tablas de contenido de carpeta. 
  
## <a name="see-also"></a>Recursos adicionales



[Tablas MAPI](mapi-tables.md)

