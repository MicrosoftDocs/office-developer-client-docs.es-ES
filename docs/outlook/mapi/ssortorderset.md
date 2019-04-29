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
ms.openlocfilehash: db19c3908c419b98b8deb71e2a86d0aa6eebe240
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438102"
---
# <a name="ssortorderset"></a>SSortOrderSet

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Define una colección de claves de ordenación para una tabla que se usa para la ordenación estándar o clasificada.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
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
  
> Número de estructuras [SSortOrder](ssortorder.md) incluidas en el miembro **unaordenación** . 
    
 **cCategories**
  
> Número de columnas que se designan como columnas de categoría. Los valores posibles van desde cero, que indica una ordenación no clasificada o estándar, al número indicado por el miembro **cSorts** . 
    
 **cExpanded**
  
> Número de categorías que se inician en un estado expandido, donde todas las filas que se aplican a la categoría están visibles en la vista de tabla. Los valores posibles oscilan entre 0 y el número indicado por **cCategories**.
    
 **Unaordenación**
  
> Matriz de estructuras **SSortOrder** , cada una de las cuales define un criterio de ordenación. 
    
## <a name="remarks"></a>Comentarios

Se usa una estructura **SSortOrderSet** para definir varios criterios de ordenación para la ordenación estándar y por categorías. 
  
Cada estructura **SSortOrderSet** contiene al menos una estructura **SSortOrder** que define la dirección de la ordenación y la columna que se utilizará como clave de ordenación. Para la ordenación por categorías, esta columna se usa como categoría. Cuando el valor del miembro **cSorts** supera el valor del miembro **cCategories** , hay más claves de ordenación que categorías y se crean categorías a partir de las columnas que aparecen primero en la matriz **SSortOrder** . 
  
Por ejemplo, si **cSorts** se establece en 3 y **cCategories** se establece en 2, las columnas descritas por el miembro **ulPropTag** de las dos primeras entradas de la matriz **SSortOrder** se usan como columnas Category. La primera entrada sirve como grupo de categorías de nivel superior; segunda entrada de la agrupación secundaria. Todas las filas que coinciden con las dos columnas Category se ordenan mediante el criterio de ordenación definido en la tercera entrada. 
  
El miembro **cExpanded** especifica el número de categorías que se han expandido por primera vez. Cuando hay varias categorías, la implementación de la tabla comienza con la primera columna que se va a designar como categoría y sigue en orden secuencial con las columnas de categoría siguientes hasta que se haya superado el número de **cCategories** . Si hay más columnas de categorías que las columnas expandidas, las columnas de categoría están contraídas. Si **cExpanded** es igual a cero, sólo la fila de título de nivel superior estará disponible para el usuario de la tabla para la visualización. Si **cExpanded** es igual a uno menos que el número de categorías, todas las filas de título y ninguna de las filas de hoja estarán disponibles. Si **cExpanded** es igual al número de categorías, la tabla se expande completamente. 
  
Para obtener más información acerca de la ordenación estándar y clasificada, vea [ordenar y categorizar](sorting-and-categorization.md).
  
## <a name="see-also"></a>Ver también



[SSortOrder](ssortorder.md)
  
[IMAPITable::ExpandRow](imapitable-expandrow.md)
  
[IMAPITable::CollapseRow](imapitable-collapserow.md)


[Estructuras MAPI](mapi-structures.md)

