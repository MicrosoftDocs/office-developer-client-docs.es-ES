---
title: ITableDataHrModifyRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrModifyRow
api_type:
- COM
ms.assetid: 9e255b3e-dd17-4528-ba4e-c3a1aef32b04
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 44ecf095ad24dd266dc5f603ace9c7b9f21c1b41
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409002"
---
# <a name="itabledatahrmodifyrow"></a>ITableData::HrModifyRow

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Inserta una fila de tabla nueva, posiblemente reemplazando una fila existente.
  
```cpp
HRESULT HrModifyRow(
  LPSRow lpSRow
);
```

## <a name="parameters"></a>Parameters

 _lpSRow_
  
> [in] Puntero a una [estructura SRow](srow.md) que describe la fila que se va a agregar o para reemplazar una fila existente. Una de las estructuras de valor de propiedad a las que apunta el miembro **lpProps** de la estructura **SRow** debe contener la columna de índice, el mismo valor que se especificó en el parámetro _ulPropTagIndexColumn_ en la llamada a la función [CreateTable.](createtable.md) 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La fila se insertó o modificó correctamente.
    
MAPI_E_INVALID_PARAMETER 
  
> La fila pasada no tiene una columna de índice.
    
## <a name="remarks"></a>Comentarios

El **método ITableData::HrModifyRow** inserta la fila descrita por la estructura **SRow** señalada por el _parámetro lpSRow._ Si una fila que tiene el mismo valor para su columna de índice que la fila a la que  _lpSRow_ apunta ya existe en la tabla, se reemplaza la fila existente. Si no existe ninguna fila que coincida con la incluida en la estructura **SRow,** **HrModifyRow** agrega la fila al final de la tabla. 
  
Todas las vistas de la tabla se modifican para incluir la fila apuntada por  _lpSRow_. Sin embargo, si una vista tiene una restricción que excluye la fila, puede que no sea visible para el usuario. 
  
Las columnas de la fila apuntadas por  _lpSRow_ no tienen que estar en el mismo orden que las columnas de la tabla. El autor de la llamada también puede incluir como columnas propiedades que no están actualmente en la tabla. Para las vistas existentes, **HrModifyRow** hace que estas nuevas columnas estén disponibles, pero no las incluye en el conjunto de columnas actual. Para vistas futuras, **HrModifyRow** incluye las nuevas columnas del conjunto de columnas. 
  
Después **de que HrModifyRow** agrega la fila, las notificaciones se envían a todos los clientes o proveedores de servicios que tienen una vista de la tabla y que han llamado al método [IMAPITable::Advise](imapitable-advise.md) de la tabla para registrar las notificaciones. 
  
## <a name="see-also"></a>Vea también



[SRow](srow.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

