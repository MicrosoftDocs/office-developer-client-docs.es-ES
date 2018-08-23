---
title: SSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSortOrderSet
api_type:
- COM
ms.assetid: e7f9be6a-92e7-44a8-93ee-b087713a31df
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e8d85ba55c5aa2f3780ad8e04cf1326cd7c35865
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575941"
---
# <a name="ssortorderset"></a>SSortOrderSet

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Define una colección de claves de ordenación para una tabla que se usa para la ordenación por categorías o estándar.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Macros relacionadas:  <br/> |[CbNewSSortOrderSet](cbnewssortorderset.md), [CbSSortOrderSet](cbssortorderset.md), [SizedSSortOrderSet](sizedssortorderset.md) <br/> |
   
```cpp
typedef struct _SSortOrderSet
{
  ULONG cSorts;
  ULONG cCategories;
  ULONG cExpanded;
  SSortOrder aSort[MAPI_DIM];
} SSortOrderSet, FAR *LPSSortOrderSet;

```

## <a name="members"></a>Members

 **cSorts**
  
> Recuento de las estructuras de [SSortOrder](ssortorder.md) que se incluyen en el miembro **aSort** . 
    
 **cCategories**
  
> Número de columnas que se designan como columnas de la categoría. Intervalo de valores posibles desde cero, lo que indica a una ordenación que no sean clasificar o estándar, con el número indicado por el miembro **cSorts** . 
    
 **cExpanded**
  
> Número de categorías que se inician en un estado expandido, donde todas las filas que se aplican a la categoría son visibles en la vista de tabla. Intervalo de valores posibles entre 0 y el número indicado por **cCategories**.
    
 **aSort**
  
> Matriz de estructuras **SSortOrder** , cada definición de un criterio de ordenación. 
    
## <a name="remarks"></a>Comentarios

Una estructura **SSortOrderSet** se usa para definir varios criterios de ordenación para la ordenación estándar y organizados por categorías. 
  
Cada estructura **SSortOrderSet** contiene al menos una estructura **SSortOrder** definir la dirección de la ordenación y la columna que se utilizará como el criterio de ordenación. Para la ordenación por categorías, esta columna se usa como la categoría. Cuando el valor del miembro **cSorts** supera el valor del miembro **cCategories** , hay más claves de ordenación que las categorías y categorías se crean a partir de las columnas que aparecen primeros en la matriz **SSortOrder** . 
  
Por ejemplo, si **cSorts** se establece en 3 y **cCategories** está establecido en 2, se utilizan las columnas descritas por el miembro **ulPropTag** de las dos primeras entradas de la matriz **SSortOrder** como las columnas de la categoría. La primera entrada sirve como la categoría de nivel superior de agrupación; la segunda entrada como la agrupación secundaria. Todas las filas que coinciden con las columnas de dos categorías se ordenan mediante el uso de la clave de ordenación definida en la tercera entrada. 
  
El miembro **cExpanded** especifica el número de categorías que expandió en primer lugar. Cuando hay varias categorías, la implementación de la tabla comienza con la primera columna que se designarán como una categoría y continúa en orden secuencial con las columnas de la categoría subsiguientes hasta que se ha superado el número de **cCategories** . Si hay más columnas de la categoría de las columnas expandida, las columnas de categoría están contraídas. Si **cExpanded** es igual a cero, está disponible para el usuario de la tabla para mostrar sólo la fila de encabezado de nivel superior. Si **cExpanded** es igual a uno menor que el número de categorías, a continuación, todas las filas de encabezado y ninguna de las filas de la hoja están disponible. Si **cExpanded** es igual que el número de categorías, a continuación, en la tabla se expande por completo. 
  
Para obtener más información acerca de la ordenación estándar y organizados por categorías, vea [Ordenar y la categorización](sorting-and-categorization.md).
  
## <a name="see-also"></a>Recursos adicionales



[SSortOrder](ssortorder.md)
  
[IMAPITable::ExpandRow](imapitable-expandrow.md)
  
[IMAPITable::CollapseRow](imapitable-collapserow.md)


[Estructuras MAPI](mapi-structures.md)

