---
title: ITableDataHrModifyRows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrModifyRows
api_type:
- COM
ms.assetid: d295c896-9882-4d6f-9689-5cf40db208c0
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d0074dd006fda6d44252011d0b979169e0c3d4cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405362"
---
# <a name="itabledatahrmodifyrows"></a>ITableData::HrModifyRows

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Inserta varias filas de tabla, posiblemente reemplazando las filas existentes.
  
```cpp
HRESULT HrModifyRows(
  ULONG ulFlags,
  LPSRowSet lpSRowSet
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lpSRowSet_
  
> [in] Puntero a una [estructura SRowSet](srowset.md) que contiene el conjunto de filas que se van a agregar, reemplazando las filas existentes si es necesario. Una de las estructuras de valor de propiedad a las que apunta el miembro **lpProps** de cada estructura [SRow](srow.md) del conjunto de filas debe contener la columna de índice, el mismo valor que se especificó en el parámetro _ulPropTagIndexColumn_ en la llamada a la [función CreateTable.](createtable.md) 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Las filas se insertaron o modificaron correctamente.
    
MAPI_E_INVALID_PARAMETER 
  
> Una o varias de las filas pasadas no tiene una columna de índice. Si se devuelve este error, no se cambia ninguna fila.
    
## <a name="remarks"></a>Comentarios

El **método ITableData::HrModifyRows** inserta las filas descritas por la estructura [SRowSet](srowset.md) a las que apunta el _parámetro lpSRowSet._ Si el valor de columna de índice de una fila del conjunto de filas coincide con el valor de una fila existente en la tabla, se reemplaza la fila existente. Si no existe ninguna fila que coincida con la incluida en la estructura **SRowSet,** **HrModifyRows** agrega la fila al final de la tabla. 
  
Todas las vistas de la tabla se modifican para incluir las filas apuntadas por  _lpSRowSet_. Sin embargo, si una vista tiene una restricción que excluye una fila, puede que no sea visible para el usuario. 
  
Las columnas de las filas apuntadas por  _lpSRowSet_ no tienen que estar en el mismo orden que las columnas de la tabla. El autor de la llamada también puede incluir como columnas propiedades que no están actualmente en la tabla. Para las vistas **existentes, HrModifyRows** hace que estas nuevas columnas estén disponibles, pero no las incluye en el conjunto de columnas actual. Para vistas futuras, **HrModifyRows** incluye las nuevas columnas del conjunto de columnas. 
  
Después de que **HrModifyRows** haya agregado las filas, las notificaciones se envían a todos los clientes o proveedores de servicios que tienen una vista de la tabla y que han llamado al método [IMAPITable::Advise](imapitable-advise.md) de la tabla para registrar las notificaciones. MAPI envía TABLE_ROW_ADDED o TABLE_ROW_MODIFIED notificaciones para cada fila, hasta ocho filas. Si la llamada **de HrModifyRows** afecta a más de ocho filas, MAPI envía una única notificación TABLE_CHANGED en su lugar. 
  
## <a name="see-also"></a>Vea también



[SRowSet](srowset.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

