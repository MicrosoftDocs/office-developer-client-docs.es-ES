---
title: SSortOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSortOrder
api_type:
- COM
ms.assetid: fe181b9a-5903-4cc0-bcd5-2061b440b5b1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 331dc05b30390bb803d186f157e0fe9edb779ab0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571671"
---
# <a name="ssortorder"></a>SSortOrder
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Define cómo se ordenan las filas de una tabla, ¿qué columna para usar como el criterio de ordenación y la dirección de la ordenación. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SSortOrder
{
  ULONG ulPropTag;
  ULONG ulOrder;
} SSortOrder, FAR *LPSSortOrder;

```

## <a name="members"></a>Members

**ulPropTag**
  
> Etiqueta de la propiedad que identifica el criterio de ordenación clave o, para una ordenación por categorías, la columna categoría.
    
**ulOrder**
  
> El orden en que los datos están que se deben ordenar. Los valores posibles son los siguientes:
    
  - TABLE_SORT_ASCEND: La tabla se debe ordenar en orden ascendente.
      
  - TABLE_SORT_COMBINE: La operación de ordenación debe crear una categoría que combina la propiedad identificada como la columna de clave de ordenación en el miembro **ulPropTag** con la columna de clave de ordenación especificada en la estructura de **SSortOrder** anterior. 
      
    Sólo se puede usar TABLE_SORT_COMBINE cuando se utiliza la estructura **SSortOrder** como una entrada en una estructura de [SSortOrderSet](ssortorderset.md) para especificar varios criterios de ordenación para una ordenación por categorías. TABLE_SORT_COMBINE no se puede usar en la primera estructura **SSortOrder** en una estructura **SSortOrderSet** . 
      
  - TABLE_SORT_DESCEND: La tabla se debe ordenar en orden descendente.
      
  - TABLE_SORT_CATEG_MAX: Se debe ordenar la tabla en el valor máximo del miembro **ulPropTag** para las filas de datos en las categorías especificadas por el criterio de ordenación anterior en la estructura **SSortOrderSet** . 
      
  - TABLE_SORT_CATEG_MIN: En el valor mínimo del miembro **ulPropTag** para las filas de datos en las categorías especificadas por el criterio de ordenación anterior en la estructura de **SSortOrderSet** en la que se debe ordenar la tabla. 
    
## <a name="remarks"></a>Comentarios

Una estructura de **SSortOrder** se usa para describir cómo se realiza una operación de ordenación estándar o una operación de ordenación por categorías. Estructuras **SSortOrder** normalmente se combinan en una estructura **SSortOrderSet** para describir varios criterios de ordenación y las instrucciones de activación. Estructuras de **SSortOrderSet** se usan en los métodos de interfaz y las funciones siguientes: 
  
- [ITableData::HrGetView](itabledata-hrgetview.md)
    
- [IMAPIFolder::SaveContentsSort](imapifolder-savecontentssort.md)
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
    
- [IMAPITable::SortTable](imapitable-sorttable.md)
    
- [FBadSortOrderSet](fbadsortorderset.md)
    
- [HrQueryAllRows](hrqueryallrows.md)
    
El rango de columnas permitidos en una tabla que se pueden usar como una clave de ordenación depende del proveedor. Las columnas que forman parte del conjunto de columna actual siempre se pueden usar como claves de ordenación. Sin embargo, cada proveedor determina si las claves de ordenación se pueden definir mediante el uso de columnas disponibles que no están en la columna actual conjunto. Una columna disponible es una columna que se devuelve desde [IMAPITable::QueryColumns](imapitable-querycolumns.md) cuando se establece la marca TBL_ALL_COLUMNS. 
  
El miembro **ulOrder** indica orden direccional y la información de categorización, por ejemplo, por conversación ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)), es decir, conversación subproceso, que es una serie de mensajes y respuestas. Las filas se pueden ordenar en orden ascendente o descendente secuencia con todas las entradas NULL situadas por última vez. 
  
El valor TABLE_SORT_COMBINE indica que la columna especificada en **ulPropTag** se debe combinar con la columna de categoría anterior para formar una categoría compuesta. Es decir, en lugar de clasificar en valores únicos de las columnas individuales, permite TABLE_SORT_COMBINE para la categorización de valores únicos de una combinación de columnas. Por ejemplo, se podría definir una única categoría para agrupar mensajes procedentes de un remitente determinado en un tema concreto. Si se establece el valor en TABLE_SORT_COMBINE, reduce el número de filas de categoría que se muestran. 
  
Todo el mundo no se admite la ordenación en columnas con varios valores por todas las implementaciones de la tabla. Si se admite, aplicar el MV_FLAG mediante la macro MVI_PROP a la etiqueta de propiedad en el miembro **ulPropTag** para identificar el criterio de ordenación como una columna multivalor. Ordenación en una columna multivalor se basa en el uso de los valores individuales. 
  
> [!IMPORTANT]
> Los valores de miembro **ulOrder** TABLE_SORT_CATEG_MAX y TABLE_SORT_CATEG_MIN no pueden definirse en el archivo de encabezado que se pueden descargar tiene actualmente, en cuyo caso se puede agregar a su código con los siguientes valores: >`#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`
  
Para obtener más información acerca de la ordenación estándar y organizados por categorías, vea [Ordenar y la categorización](sorting-and-categorization.md). 
  
## <a name="see-also"></a>Recursos adicionales

- [SSortOrderSet](ssortorderset.md)
- [Estructuras MAPI](mapi-structures.md)

