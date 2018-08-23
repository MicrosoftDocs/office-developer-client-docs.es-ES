---
title: ITableDataHrInsertRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrInsertRow
api_type:
- COM
ms.assetid: e5ae37ea-81a5-49c7-9ad0-0bfac518426c
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9aa038958e26652ae7ead728ab15d068e080dc69
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579889"
---
# <a name="itabledatahrinsertrow"></a>ITableData::HrInsertRow

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Inserta una fila de tabla. 
  
```cpp
HRESULT HrInsertRow(
  ULONG uliRow,
  LPSRow lpSRow
);
```

## <a name="parameters"></a>Parámetros

 _uliRow_
  
> [entrada] Un número de fila secuencial que representa una fila concreta. Después de la fila que indica el número se colocará la nueva fila. El parámetro _uliRow_ puede contener los números de filas de n a 0, donde n es el número total de filas de la tabla. Pasando n _uliRow_ , la fila anexa al final de la tabla. 
    
 _lpSRow_
  
> [entrada] Un puntero a una estructura [SRow](srow.md) que describe la fila que se va a insertar. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La fila se insertó correctamente.
    
MAPI_E_INVALID_PARAMETER 
  
> Una fila que tiene el mismo valor para su columna de índice, como la fila que va a insertarse ya existe en la tabla.
    
## <a name="remarks"></a>Comentarios

El método **ITableData::HrInsertRow** , inserta una fila en una tabla en una posición determinada. La nueva fila se inserta después de la fila que se encuentra en la posición especificada por el parámetro _uliRow_ . 
  
Si _uliRow_ se establece en el número de filas en la tabla, la nueva fila se anexa al final de la tabla. 
  
La propiedad que actúa como la columna de índice para la tabla debe incluirse en el miembro **lpProps** de la estructura [SRow](srow.md) indicada por el parámetro _lpSRow_ . Esta propiedad de índice, normalmente **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), se usa para identificar de forma exclusiva la fila de tareas de mantenimiento futuros.
  
Las columnas de propiedad de la estructura de **SRow** no es necesario estar en el mismo orden que las columnas de propiedad en la tabla. 
  
Después de que se inserte la fila, se envían a todos los clientes o proveedores de servicios que tienen una vista de la tabla y que ha llamado [IMAPITable::Advise](imapitable-advise.md) (método) de la tabla para registrar para las notificaciones. Si la fila insertada no está incluida en la vista debido a una restricción, se envía ninguna notificación. 
  
## <a name="see-also"></a>Recursos adicionales



[SRow](srow.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

