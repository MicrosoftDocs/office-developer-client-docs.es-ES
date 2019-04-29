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
ms.openlocfilehash: f16ba9164d55fdb7bd688d4068f99dc4407e5413
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432369"
---
# <a name="imapitablesorttable"></a>IMAPITable::SortTable

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El método **IMAPITable:: SortTable** ordena las filas de la tabla, en función de los criterios de ordenación. 
  
```cpp
HRESULT SortTable(
LPSSortOrderSet lpSortCriteria,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

_lpSortCriteria_
  
> a Puntero a una estructura [SSortOrderSet](ssortorderset.md) que contiene los criterios de ordenación que se van a aplicar. Si se pasa una estructura **SSortOrderSet** que contiene cero columnas, indica que no es necesario ordenar la tabla en un orden determinado. 
    
_ulFlags_
  
> a Máscara de máscara de marcadores que controla la temporización de la operación **IMAPITable:: SortTable** . Se pueden establecer los siguientes indicadores: 
    
TBL_ASYNC 
  
> Inicia la operación de forma asincrónica y regresa antes de que se complete la operación.
    
TBL_BATCH 
  
> Pospone la finalización de la ordenación hasta que se necesiten los datos de la tabla.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La operación de ordenación se realizó correctamente.
    
MAPI_E_BUSY 
  
> Hay otra operación en curso que evita que se inicie la operación de ordenación. Debe permitirse que la operación en curso se complete o que deba detenerse.
    
MAPI_E_NO_SUPPORT 
  
> La tabla no admite el tipo de ordenación solicitada.
    
MAPI_E_TOO_COMPLEX 
  
> La tabla no puede realizar la operación porque los criterios de ordenación señalados por el parámetro _lpSortCriteria_ son demasiado complejos. **SortTable** puede devolver MAPI_E_TOO_COMPLEX en las siguientes condiciones. 
    
   - Se ha solicitado una operación de ordenación para una columna de propiedad que la implementación no puede ordenar.
    
   - La implementación no admite el criterio de ordenación solicitado en el miembro **ulOrder** de la estructura **SSortOrderSet** . 
    
   - El número de columnas que se van a ordenar, como se especifica en el miembro **cSorts** en **SSortOrderSet**, es mayor que el que puede controlar la implementación.
    
   - Se solicita una operación de ordenación, tal como indica una etiqueta de propiedad en **SSortOrderSet**, basada en una propiedad que no está en el conjunto disponible o activo y la implementación no admite la ordenación en propiedades que no están en el conjunto disponible.
    
   - Una propiedad se especifica varias veces en un conjunto de ordenación, como se indica en varias instancias de la misma etiqueta de propiedad, y la implementación no puede realizar dicha operación de ordenación.
    
   - Se solicita una operación de ordenación basada en columnas de propiedades multivalor mediante MVI_FLAG y la implementación no admite la ordenación de propiedades multivalor. 
    
   - Una etiqueta de propiedad de una propiedad en **SSortOrderSet** especifica una propiedad o un tipo que no es compatible con la implementación. 
    
   - Una operación de ordenación distinta de la que pasa por la tabla de la propiedad **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) forward se especifica sólo para una tabla de datos adjuntos que admita este tipo de ordenación.
    
## <a name="remarks"></a>Comentarios

El método **IMAPITable:: SortTable** ordena las filas en una vista de tabla. Mientras que algunas tablas admiten la ordenación estándar y por categorías en varias columnas de clave de ordenación, otras tablas están más limitadas en su compatibilidad. Normalmente, los proveedores de libretas de direcciones no admiten la ordenación de tablas. Los proveedores de almacenamiento de mensajes normalmente admiten la ordenación en la medida que conservan el criterio de ordenación de las carpetas que se produce cuando se ordena una tabla completa (una tabla sin restricciones). 
  
Algunas tablas permiten la ordenación que se va a realizar en cualquier columna de la tabla. Otras tablas no; las columnas que no se incluyen en la vista de tabla no se ven afectadas por una llamada de **SortTable** . Algunas tablas requieren que las claves de ordenación se generen sólo con las columnas del conjunto de columnas actual de la tabla. 
  
Una tabla puede devolver MAPI_E_NO_SUPPORT o MAPI_E_TOO_COMPLEX de **SortTable** cuando no puede completar una operación de ordenación. Además, no se garantiza que los proveedores de almacenamiento respeten el conjunto de criterios de ordenación especificado para las tablas de jerarquía. 
  
Cuando hay cero columnas en la estructura [SSortOrderSet](ssortorderset.md) apuntado por el parámetro _lpSortCriteria_ , la tabla devuelve el conjunto de columnas actual. El criterio de ordenación actual puede recuperarse llamando al método [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) de la tabla. 
  
Todos los marcadores de una tabla están invalidados y deben eliminarse cuando se realiza una llamada a **SortTable** y el marcador BOOKMARK_CURRENT que indica la posición actual del cursor debe establecerse en el principio de la tabla. 
  
Si ordena por una columna que contiene una propiedad con varios valores sin la marca MVI_FLAG establecida, los valores de la columna se tratan como una tupla completamente ordenada. Una comparación de dos columnas con varios valores compara los elementos de columna en orden, informa de la relación de las columnas en la primera desigualdad y devuelve la igualdad sólo si las columnas que se comparan contienen los mismos valores en el mismo orden. Si una columna tiene menos valores que el otro, la relación notificada es la de un valor null en el otro valor.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

**SortTable** funciona de forma sincrónica a menos que establezca una de las marcas. Si establece la marca TBL_BATCH, **SortTable** pospone la operación de ordenación a menos que solicite los datos. Si se establece la marca TBL_ASYNC, **SortTable** funciona de forma asincrónica, lo que puede devolverse antes de la finalización de la operación. 
  
Llame al método [IMAPITable:: ABORT](imapitable-abort.md) para detener una operación asincrónica en curso si la ordenación debe realizarse inmediatamente. Si **SortTable** no puede continuar porque una o más operaciones asincrónicas en la tabla están en curso, devuelve MAPI_E_BUSY. 
  
Para obtener el mejor rendimiento, llame a **SetColumns** para personalizar el conjunto de columnas de la tabla y **Restrict** para limitar el número de filas de la tabla antes de llamar a **SortTable** para realizar la ordenación. 
  
Cuando se produce un error en **SortTable** , el criterio de ordenación que estaba en vigor antes del error todavía está en vigor. 
  
## <a name="see-also"></a>Ver también

- [IMAPITable::Abort](imapitable-abort.md)
- [IMAPITable::GetRowCount](imapitable-getrowcount.md)
- [IMAPITable::QueryColumns](imapitable-querycolumns.md)
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
- [IMAPITable::SetColumns](imapitable-setcolumns.md)
- [SSortOrderSet](ssortorderset.md)
- [IMAPITable : IUnknown](imapitableiunknown.md)

