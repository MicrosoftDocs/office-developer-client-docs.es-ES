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
ms.openlocfilehash: a1388545597cf0000f270bf693c93f9349fb6426
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817993"
---
# <a name="itabledatahrmodifyrow"></a>ITableData::HrModifyRow

  
  
**Hace referencia a**: Outlook 
  
Inserta una nueva fila de tabla, posiblemente reemplazando una fila existente.
  
```cpp
HRESULT HrModifyRow(
  LPSRow lpSRow
);
```

## <a name="parameters"></a>Parámetros

 _lpSRow_
  
> [entrada] Un puntero a una estructura [SRow](srow.md) que describe la fila que se va a agregar o reemplazar una fila existente. Una de las estructuras de valor de la propiedad indicadas por el miembro **lpProps** de la estructura **SRow** debe contener la columna de índice, el mismo valor que se especificó en el parámetro _ulPropTagIndexColumn_ en la llamada a la [CreateTable ](createtable.md)(función). 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La fila se inserta o se modificó correctamente.
    
MAPI_E_INVALID_PARAMETER 
  
> La fila se pasan en no tiene una columna de índice.
    
## <a name="remarks"></a>Comentarios

El método **ITableData::HrModifyRow** inserta la fila descrita por la estructura de **SRow** indicada por el parámetro _lpSRow_ . Si una fila que tiene el mismo valor para su columna de índice que la fila que señala _lpSRow_ ya existe en la tabla, se reemplaza la fila existente. Si no hay ninguna fila que coincida con el incluido en la estructura de **SRow** , **HrModifyRow** agrega la fila al final de la tabla. 
  
Todas las vistas de la tabla se modifican para incluir la fila indicada por _lpSRow_. Sin embargo, si una vista tiene una restricción en el lugar que excluye la fila, pueden no ser visible para el usuario. 
  
Las columnas de la fila que señala _lpSRow_ no es necesario estar en el mismo orden que las columnas de la tabla. También puede incluir el autor de la llamada como propiedades de las columnas que no están actualmente en la tabla. Para las vistas existentes, **HrModifyRow** realiza estas nuevas columnas disponibles, pero no se incluye en el conjunto actual de la columna. Para las futuras vistas, **HrModifyRow** incluye las nuevas columnas en el conjunto de columnas. 
  
Una vez que **HrModifyRow** se agrega la fila, se envían a todos los clientes o proveedores de servicios que tienen una vista de la tabla y que ha llamado [IMAPITable::Advise](imapitable-advise.md) (método) de la tabla para registrar para las notificaciones. 
  
## <a name="see-also"></a>Vea también



[SRow](srow.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

