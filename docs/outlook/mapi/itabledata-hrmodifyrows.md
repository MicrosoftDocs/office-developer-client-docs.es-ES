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
ms.openlocfilehash: 15d98183548d4b73c35368d690ef63d5c3dfd9af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817987"
---
# <a name="itabledatahrmodifyrows"></a>ITableData::HrModifyRows

  
  
**Hace referencia a**: Outlook 
  
Inserta varias filas de tabla, posiblemente reemplazando las filas existentes.
  
```cpp
HRESULT HrModifyRows(
  ULONG ulFlags,
  LPSRowSet lpSRowSet
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lpSRowSet_
  
> [entrada] Un puntero a una estructura [SRowSet](srowset.md) que contiene el conjunto de filas que se va a agregar, reemplazar las filas existentes, si es necesario. Una de las estructuras de valor de la propiedad apuntadas establece el miembro **lpProps** de cada estructura de [SRow](srow.md) en la fila debe contener la columna de índice, el mismo valor que se especificó en el parámetro _ulPropTagIndexColumn_ en la llamada a la [ CreateTable](createtable.md) (función). 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Las filas insertadas o modificadas correctamente.
    
MAPI_E_INVALID_PARAMETER 
  
> Una o varias de las filas que se pasan en no tienen una columna de índice. Si se devuelve este error, no se cambiarán ninguna fila.
    
## <a name="remarks"></a>Comentarios

El método **ITableData::HrModifyRows** inserta las filas descritas por la estructura de [SRowSet](srowset.md) indicada por el parámetro _lpSRowSet_ . Si el valor de la columna de índice de una fila en el conjunto de filas coincide con el valor de una fila existente en la tabla, se reemplaza la fila existente. Si no hay ninguna fila que coincida con el incluido en la estructura de **SRowSet** , **HrModifyRows** agrega la fila al final de la tabla. 
  
Todas las vistas de la tabla se modifican para incluir las filas que señala _lpSRowSet_. Sin embargo, si una vista tiene una restricción en el lugar que excluye una fila, pueden no ser visible para el usuario. 
  
Las columnas de las filas que señala _lpSRowSet_ no es necesario estar en el mismo orden que las columnas de la tabla. También puede incluir el autor de la llamada como propiedades de las columnas que no están actualmente en la tabla. Para las vistas existentes, **HrModifyRows** realiza estas nuevas columnas disponibles, pero no se incluye en el conjunto actual de la columna. Para las futuras vistas, **HrModifyRows** incluye las nuevas columnas en el conjunto de columnas. 
  
Después de **HrModifyRows** que agrega las filas, las notificaciones se envían a todos los clientes o proveedores de servicios que tienen una vista de la tabla y que ha llamado [IMAPITable::Advise](imapitable-advise.md) (método) de la tabla para registrar para las notificaciones. MAPI envía notificaciones TABLE_ROW_ADDED o TABLE_ROW_MODIFIED para cada fila, hasta ocho filas. Si más de ocho filas se ven afectadas por la llamada **HrModifyRows** , MAPI envía una única notificación TABLE_CHANGED en su lugar. 
  
## <a name="see-also"></a>Vea también



[SRowSet](srowset.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

