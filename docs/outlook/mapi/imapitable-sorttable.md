---
title: IMAPITableSortTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SortTable
api_type:
- COM
ms.assetid: ff5f78ac-06cf-46fb-93da-5f4a3a5d1b22
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 46a87a6eb5c80244c04ae6257cd4441b8797ba36
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817611"
---
# <a name="imapitablesorttable"></a>IMAPITable::SortTable

**Hace referencia a**: Outlook 
  
El método **SortTable** ordena las filas de la tabla, según la ordenación criterios. 
  
```cpp
HRESULT SortTable(
LPSSortOrderSet lpSortCriteria,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parámetros

_lpSortCriteria_
  
> [entrada] Puntero a una estructura [SSortOrderSet](ssortorderset.md) que contiene los criterios de ordenación que se debe aplicar. Pasando una estructura **SSortOrderSet** que contiene cero columnas indica que no dispone de la tabla que se deben ordenar en un orden determinado. 
    
_ulFlags_
  
> [entrada] Máscara de bits de indicadores que controla la sincronización de la operación de **SortTable** . Se pueden establecer los siguientes indicadores: 
    
TBL_ASYNC 
  
> Inicia la operación de forma asincrónica y devuelve antes de completar la operación.
    
TBL_BATCH 
  
> Aplaza la finalización de la ordenación hasta que los datos de la tabla están necesarios.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La operación de ordenación fue correcta.
    
MAPI_E_BUSY 
  
> Otra operación está en curso que impide que la operación de ordenación de inicio. Debe ser permite la operación en curso para llevar a cabo o se debe detener.
    
MAPI_E_NO_SUPPORT 
  
> La tabla no es compatible con el tipo de ordenación solicitado.
    
MAPI_E_TOO_COMPLEX 
  
> La tabla no puede realizar la operación porque el criterio de ordenación determinado indicado por el parámetro _lpSortCriteria_ es demasiado compleja. **SortTable** puede devolver MAPI_E_TOO_COMPLEX en las siguientes condiciones. 
    
   - Se solicita una operación de ordenación para una columna de propiedad que no se puede ordenar la implementación.
    
   - La implementación no es compatible con el criterio de ordenación solicitado en el miembro **ulOrder** de la estructura **SSortOrderSet** . 
    
   - El número de columnas que se deben ordenar, tal como se especifica en el miembro **cSorts** en **SSortOrderSet**, es mayor que la implementación puede tratar.
    
   - Se solicita una operación de ordenación, indicada por una etiqueta de propiedad en **SSortOrderSet**, en función de una propiedad que no está en el conjunto disponible o activo y la implementación no admite la ordenación en las propiedades no en el conjunto disponible.
    
   - Una propiedad se especifica varias veces en un conjunto de criterio de ordenación, como se indica en varias instancias de la misma etiqueta de propiedad, y la implementación no puede realizar como una operación de ordenación.
    
   - Se solicita una operación de ordenación en función de las columnas de propiedad multivalor con MVI_FLAG y la implementación no admite la ordenación en las propiedades multivalores. 
    
   - Una etiqueta de propiedad para una propiedad en **SSortOrderSet** especifica una propiedad o un tipo que no es compatible con la implementación. 
    
   - Una operación de ordenación distinto del que se realiza a través de la tabla de la propiedad **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) desviar sólo se especifica para una tabla de datos adjuntos que admite este tipo de ordenación.
    
## <a name="remarks"></a>Comentarios

El método **SortTable** pedidos las filas en una vista de tabla. Mientras que algunas tablas admiten la ordenación estándar y ordenadas por categorías en varias columnas de clave de ordenación, otras tablas son más limitados en las admite. Los proveedores de la libreta de direcciones normalmente no admiten la ordenación de tablas. Los proveedores de almacén de mensajes normalmente admiten la ordenación en la medida en que mantienen el criterio de ordenación de las carpetas que se produce cuando se ordena una tabla completa (una tabla sin restricciones). 
  
Algunas tablas permiten ordenación que debe realizarse en cualquier columna de la tabla. Otras tablas no; las columnas no incluidas en la vista de tabla no se ven afectadas por una llamada de **SortTable** . Algunas tablas requieren que las claves de ordenación se generan sólo con columnas en el conjunto actual de columna de la tabla. 
  
Una tabla puede devolver MAPI_E_NO_SUPPORT o MAPI_E_TOO_COMPLEX de **SortTable** cuando no puede completar una operación de ordenación. Además, no se garantiza que los proveedores de almacén para respetar el criterio de ordenación especificado para tablas de jerarquía. 
  
Cuando hay cero columnas en la estructura de [SSortOrderSet](ssortorderset.md) indicada por el parámetro _lpSortCriteria_ , en la tabla devuelve el conjunto actual de la columna. El criterio de ordenación actual se puede recuperar al llamar al método [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) de la tabla. 
  
Todos los marcadores de una tabla se invalidan y se deben eliminar cuando se realiza una llamada a **SortTable** , y debe establecerse el marcador BOOKMARK_CURRENT que indica la posición actual del cursor, al principio de la tabla. 
  
Si realiza una ordenación en una columna que contiene una propiedad multivalor sin establecer el indicador MVI_FLAG, los valores de la columna se tratan como una tupla ordenada por completo. Una comparación de dos columnas con varios valores compara los elementos de columna en orden, informes de la relación de las columnas en la primera desigualdad y devuelve la igualdad sólo si las columnas que se comparan contienen los mismos valores en el mismo orden. Si una columna tiene menos valores que el otro, la relación conocida es un valor nulo en el otro valor.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

**SortTable** funciona de forma sincrónica a menos que establezca uno de los indicadores. Si se establece la marca TBL_BATCH, **SortTable** pospone la operación de ordenación a menos que solicitar los datos. Si se establece la marca TBL_ASYNC, **SortTable** funciona de forma asincrónica, potencialmente devolver antes de la finalización de la operación. 
  
Llame al método [IMAPITable::Abort](imapitable-abort.md) para detener una operación asincrónica en curso si la ordenación debe llevarse a cabo inmediatamente. Si no se puede continuar **SortTable** debido a que una o varias operaciones asincrónicas en la tabla están en curso, devuelve MAPI_E_BUSY. 
  
Para obtener el mejor rendimiento, llame a **SetColumns** para personalizar el conjunto de columnas de la tabla y **Restrict** para limitar el número de filas en la tabla antes de llamar a **SortTable** para llevar a cabo a la ordenación. 
  
Cada vez que se produce un error de **SortTable** , el criterio de ordenación que estaba en vigor antes del error todavía está en efecto. 
  
## <a name="see-also"></a>Vea también

- [IMAPITable::Abort](imapitable-abort.md)
- [IMAPITable::GetRowCount](imapitable-getrowcount.md)
- [IMAPITable::QueryColumns](imapitable-querycolumns.md)
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
- [IMAPITable::SetColumns](imapitable-setcolumns.md)
- [SSortOrderSet](ssortorderset.md)
- [IMAPITable : IUnknown](imapitableiunknown.md)

