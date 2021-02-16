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
  
El **método IMAPITable::SortTable** ordena las filas de la tabla, según los criterios de ordenación. 
  
```cpp
HRESULT SortTable(
LPSSortOrderSet lpSortCriteria,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parámetros

_lpSortCriteria_
  
> [entrada] Puntero a una [estructura SSortOrderSet](ssortorderset.md) que contiene los criterios de ordenación que se aplicarán. Pasar una **estructura SSortOrderSet** que contiene cero columnas indica que no es necesario ordenar la tabla en ningún orden determinado. 
    
_ulFlags_
  
> [entrada] Máscara de bits de marcas que controla el tiempo de la **operación IMAPITable::SortTable.** Se pueden establecer las siguientes marcas: 
    
TBL_ASYNC 
  
> Inicia la operación de forma asincrónica y vuelve antes de que finalice la operación.
    
TBL_BATCH 
  
> Aplaza la finalización de la ordenación hasta que se requieran los datos de la tabla.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La operación de ordenación se ha realizado correctamente.
    
MAPI_E_BUSY 
  
> Hay otra operación en curso que impide que se inicie la operación de ordenación. La operación en curso debe poder completarse o debe detenerse.
    
MAPI_E_NO_SUPPORT 
  
> La tabla no admite el tipo de ordenación solicitada.
    
MAPI_E_TOO_COMPLEX 
  
> La tabla no puede realizar la operación porque el criterio de ordenación determinado al que apunta el parámetro  _lpSortCriteria_ es demasiado complejo. **SortTable** puede devolver MAPI_E_TOO_COMPLEX en las siguientes condiciones. 
    
   - Se solicita una operación de ordenación para una columna de propiedad que la implementación no puede ordenar.
    
   - La implementación no admite el criterio de ordenación solicitado en el **miembro ulOrder** de la **estructura SSortOrderSet.** 
    
   - El número de columnas que se va a ordenar, como se especifica en el miembro **cSorts** en **SSortOrderSet**, es mayor de lo que puede controlar la implementación.
    
   - Se solicita una operación de ordenación, como se indica mediante una etiqueta de propiedad en **SSortOrderSet**, basada en una propiedad que no está en el conjunto disponible o activo y la implementación no admite la ordenación de propiedades que no están en el conjunto disponible.
    
   - Una propiedad se especifica varias veces en un conjunto de criterio de ordenación, como indican varias instancias de la misma etiqueta de propiedad, y la implementación no puede realizar dicha operación de ordenación.
    
   - Se solicita una operación de ordenación basada en columnas de propiedad multivalor mediante MVI_FLAG y la implementación no admite la ordenación de propiedades multivalor. 
    
   - Una etiqueta de propiedad para una propiedad en **SSortOrderSet** especifica una propiedad o tipo que la implementación no admite. 
    
   - Una operación de ordenación que no sea una que continúe a través de la tabla desde la propiedad **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) se especifica sólo para una tabla de datos adjuntos que admite este tipo de ordenación.
    
## <a name="remarks"></a>Comentarios

El **método IMAPITable::SortTable** ordena las filas de una vista de tabla. Mientras que algunas tablas admiten la ordenación estándar y por categorías en varias columnas de clave de ordenación, otras tablas son más limitadas en su compatibilidad. Normalmente, los proveedores de libretas de direcciones no admiten la ordenación de tablas. Los proveedores de almacenamiento de mensajes normalmente admiten la ordenación en la medida en que mantienen el criterio de ordenación de las carpetas que se produce cuando se ordena una tabla completa (una tabla sin restricciones). 
  
Algunas tablas permiten ordenar en cualquier columna de tabla. Otras tablas no lo hacen; las columnas que no se incluyen en la vista de tabla no se ven afectadas por una **llamada a SortTable.** Algunas tablas requieren que las claves de ordenación se puedan crear solo con columnas del conjunto de columnas actual de la tabla. 
  
Una tabla puede devolver MAPI_E_NO_SUPPORT o MAPI_E_TOO_COMPLEX de **SortTable** cuando no puede completar una operación de ordenación. Además, no se garantiza que los proveedores de almacén respetarán el conjunto de criterio de ordenación especificado para las tablas de jerarquía. 
  
Cuando hay cero columnas en la estructura [SSortOrderSet](ssortorderset.md) a las que apunta el parámetro  _lpSortCriteria,_ la tabla devuelve el conjunto de columnas actual. El criterio de ordenación actual se puede recuperar llamando al método [IMAPITable::QuerySortOrder de](imapitable-querysortorder.md) la tabla. 
  
Todos los marcadores de una tabla se invalidan y deben eliminarse cuando se realiza una llamada a **SortTable,** y el marcador BOOKMARK_CURRENT que indica la posición actual del cursor debe establecerse al principio de la tabla. 
  
Si se ordena en una columna que contiene una propiedad multivalor sin la marca MVI_FLAG establecida, los valores de la columna se tratan como una tupla completamente ordenada. Una comparación de dos columnas multivalor compara los elementos de columna en orden, informando de la relación de las columnas en la primera diferencia y devuelve la igualdad sólo si las columnas que se comparan contienen los mismos valores en el mismo orden. Si una columna tiene menos valores que la otra, la relación notificada es la de un valor nulo con el otro valor.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

**SortTable** funciona de forma sincrónica a menos que establezcas una de las marcas. Si establece la marca TBL_BATCH, **SortTable** pospone la operación de ordenación a menos que solicite los datos. Si se TBL_ASYNC marca, **SortTable** funciona de forma asincrónica, lo que puede devolverse antes de que finalice la operación. 
  
Llame al [método IMAPITable::Abort](imapitable-abort.md) para detener una operación asincrónica en curso si la ordenación debe realizarse inmediatamente. Si **SortTable** no puede continuar porque una o varias operaciones asincrónicas de la tabla están en curso, devuelve MAPI_E_BUSY. 
  
Para obtener un mejor rendimiento, llame a **SetColumns** para personalizar el conjunto de columnas de la tabla y Restrinja para limitar el número de filas de la tabla antes de llamar a  **SortTable** para realizar la ordenación. 
  
Siempre que se produce un error en **SortTable,** el criterio de ordenación que estaba en vigor antes del error sigue en vigor. 
  
## <a name="see-also"></a>Consulte también

- [IMAPITable::Abort](imapitable-abort.md)
- [IMAPITable::GetRowCount](imapitable-getrowcount.md)
- [IMAPITable::QueryColumns](imapitable-querycolumns.md)
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
- [IMAPITable::SetColumns](imapitable-setcolumns.md)
- [SSortOrderSet](ssortorderset.md)
- [IMAPITable : IUnknown](imapitableiunknown.md)

