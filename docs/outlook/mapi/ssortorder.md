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
ms.openlocfilehash: f9d38c90fa5795d34f78c61ce0faa5f76d8f740d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439726"
---
# <a name="ssortorder"></a>SSortOrder
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Define cómo se ordenan las filas de una tabla, qué columna se va a usar como clave de ordenación y la dirección de la ordenación. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SSortOrder
{
  ULONG ulPropTag;
  ULONG ulOrder;
} SSortOrder, FAR *LPSSortOrder;

```

## <a name="members"></a>Members

**ulPropTag**
  
> Etiqueta de propiedad que identifica el criterio de ordenación o, en el caso de una ordenación por categorías, la columna categoría.
    
**ulOrder**
  
> Orden en el que se van a ordenar los datos. Los valores posibles son los siguientes:
    
  - TABLE_SORT_ASCEND: la tabla debe ordenarse en orden ascendente.
      
  - TABLE_SORT_COMBINE: la operación de ordenación debe crear una categoría que combine la propiedad identificada como la columna de clave de ordenación en el miembro **ulPropTag** con la columna de clave de ordenación especificada en la estructura **SSortOrder** anterior. 
      
    TABLE_SORT_COMBINE solo se puede usar cuando la estructura **SSortOrder** se usa como una entrada en una estructura [SSortOrderSet](ssortorderset.md) para especificar varios criterios de ordenación para una ordenación por categorías. TABLE_SORT_COMBINE no se puede usar en la primera estructura **SSortOrder** de una estructura **SSortOrderSet** . 
      
  - TABLE_SORT_DESCEND: la tabla debe ordenarse en orden descendente.
      
  - TABLE_SORT_CATEG_MAX: la tabla debe ordenarse por el valor máximo del miembro **ulPropTag** para las filas de datos en las categorías especificadas por el criterio de ordenación anterior en la estructura **SSortOrderSet** . 
      
  - TABLE_SORT_CATEG_MIN: la tabla debe ordenarse por el valor mínimo del miembro **ulPropTag** para las filas de datos en las categorías especificadas por el criterio de ordenación anterior en la estructura de **SSortOrderSet** . 
    
## <a name="remarks"></a>Comentarios

Una estructura **SSortOrder** se utiliza para describir cómo realizar una operación de ordenación estándar o una operación de ordenación por categorías. Las estructuras **SSortOrder** suelen combinarse en una estructura **SSortOrderSet** para describir varios criterios de ordenación y direcciones. Las estructuras **SSortOrderSet** se usan en las siguientes funciones y métodos de interfaz: 
  
- [ITableData::HrGetView](itabledata-hrgetview.md)
    
- [IMAPIFolder::SaveContentsSort](imapifolder-savecontentssort.md)
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
    
- [IMAPITable::SortTable](imapitable-sorttable.md)
    
- [FBadSortOrderSet](fbadsortorderset.md)
    
- [HrQueryAllRows](hrqueryallrows.md)
    
El intervalo de columnas permitidas en una tabla que se puede usar como clave de ordenación depende del proveedor. Las columnas que forman parte del conjunto de columnas actual siempre se pueden usar como claves de ordenación. Sin embargo, cada proveedor determina si las claves de ordenación pueden definirse mediante columnas disponibles que no están en el conjunto de columnas actual. Una columna disponible es una columna que devuelve el [IMAPITable:: QueryColumns](imapitable-querycolumns.md) cuando se establece la marca TBL_ALL_COLUMNS. 
  
El miembro **ulOrder** indica el orden direccional y la información de categorización, por ejemplo, por conversación ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)), es decir, hilo de conversación, que es una serie de mensajes y respuestas. Las filas pueden ordenarse en una secuencia ascendente o descendente con todas las entradas NULAs colocadas en último lugar. 
  
El valor TABLE_SORT_COMBINE indica que la columna especificada en **ulPropTag** debe combinarse con la columna de categoría anterior para formar una categoría compuesta. Es decir, en lugar de categorizar en valores únicos de columnas individuales, TABLE_SORT_COMBINE permite la categorización en valores únicos de una combinación de columnas. Por ejemplo, una única categoría podría definirse para agrupar los mensajes recibidos de un remitente determinado sobre un tema concreto. Si se establece el valor en TABLE_SORT_COMBINE, se reduce el número de filas de categoría que se muestran. 
  
La ordenación por columnas multivalor no es compatible universalmente con todas las implementaciones de tabla. Si se admite, aplique MV_FLAG mediante la macro MVI_PROP a la etiqueta Property del miembro **ulPropTag** para identificar el criterio de ordenación como una columna multivalor. La ordenación en una columna de varios valores se basa en el uso de los valores individuales. 
  
> [!IMPORTANT]
> Los valores TABLE_SORT_CATEG_MAX y TABLE_SORT_CATEG_MIN de los miembros de **ulOrder** podrían no estar definidos en el archivo de encabezado descargable que tiene actualmente, en cuyo caso puede agregarlo al código con los siguientes valores: >`#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`
  
Para obtener más información acerca de la ordenación estándar y clasificada, vea [ordenar y categorizar](sorting-and-categorization.md). 
  
## <a name="see-also"></a>Ver también

- [SSortOrderSet](ssortorderset.md)
- [Estructuras MAPI](mapi-structures.md)

