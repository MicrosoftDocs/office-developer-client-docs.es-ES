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
  
Define una colección de claves de ordenación para una tabla que se usa para la ordenación estándar o categorizada.
  
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
  
> Recuento de [estructuras SSortOrder](ssortorder.md) que se incluyen en el **miembro de aSort.** 
    
 **cCategories**
  
> Recuento de columnas designadas como columnas de categoría. Los valores posibles oscilan entre cero, que indica una ordenación estándar o no categorizada, hasta el número indicado por el miembro **cSorts.** 
    
 **cExpanded**
  
> Recuento de categorías que comienzan en un estado expandido, donde todas las filas que se aplican a la categoría están visibles en la vista de tabla. Los valores posibles oscilan entre 0 y el número indicado por **cCategories**.
    
 **aSort**
  
> Matriz de **estructuras SSortOrder,** cada una definiendo un criterio de ordenación. 
    
## <a name="remarks"></a>Comentarios

Se **usa una estructura SSortOrderSet** para definir varios pedidos de ordenación para la ordenación estándar y categorizada. 
  
Cada **estructura SSortOrderSet** contiene al menos una estructura **SSortOrder** que define la dirección del ordenación y la columna que se usará como clave de ordenación. Para la ordenación categorizada, esta columna se usa como categoría. Cuando el valor del miembro **cSorts** supera el valor del miembro **cCategories,** hay más claves de ordenación que categorías y las categorías se crean a partir de las columnas que aparecen primero en la matriz **SSortOrder.** 
  
Por ejemplo, si **cSorts** se establece en 3 y **cCategories** se establece en 2, las columnas descritas por el **miembro ulPropTag** de las dos primeras entradas de la matriz **SSortOrder** se usan como columnas de categoría. La primera entrada sirve como agrupación de categorías de nivel superior; la segunda entrada como agrupación secundaria. Todas las filas que coinciden con las dos columnas de categoría se ordenan mediante la clave de ordenación definida en la tercera entrada. 
  
El **miembro cExpanded** especifica el número de categorías que se expanden al principio. Cuando hay varias categorías, la implementación de la tabla comienza con la primera columna que se designará como categoría y continúa en orden secuencial con las columnas de categorías subsiguientes hasta que se supere el número de **cCategories.** Si hay más columnas de categoría de las que hay expandida, las columnas de categoría se contraen. Si **cExpanded** es igual a cero, solo la fila de título de nivel superior está disponible para que se muestre el usuario de la tabla. Si **cExpanded** es igual a uno menos que el número de categorías, todas las filas de encabezado y ninguna de las filas hoja están disponibles. Si **cExpanded** es igual al número de categorías, la tabla se expande por completo. 
  
Para obtener más información acerca de la ordenación estándar y categorizada, vea [Ordenación y categorización](sorting-and-categorization.md).
  
## <a name="see-also"></a>Vea también



[SSortOrder](ssortorder.md)
  
[IMAPITable::ExpandRow](imapitable-expandrow.md)
  
[IMAPITable::CollapseRow](imapitable-collapserow.md)


[Estructuras MAPI](mapi-structures.md)

