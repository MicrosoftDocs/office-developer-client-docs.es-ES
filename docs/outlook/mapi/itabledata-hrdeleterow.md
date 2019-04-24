---
title: ITableDataHrDeleteRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrDeleteRow
api_type:
- COM
ms.assetid: 670c2291-d5b6-4dcf-9046-9125272dd8f8
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b187cccc4505256b7ab4d580c30eeb2e15ebf574
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278865"
---
# <a name="itabledatahrdeleterow"></a>ITableData::HrDeleteRow

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Elimina una fila de tabla.
  
```cpp
HRESULT HrDeleteRow(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>Parameters

 _lpSPropValue_
  
> a Un puntero a una estructura de valores de propiedad que describe la columna de índice de la fila que se va a eliminar. El miembro **ulPropTag** de la estructura del valor de la propiedad debe contener la misma etiqueta de propiedad que el parámetro _ulPropTagIndexColumn_ desde la llamada a la función [createTable](createtable.md) . 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La fila se eliminó correctamente.
    
MAPI_E_NOT_FOUND 
  
> La propiedad a la que señala el parámetro _lpSPropValue_ no identifica una fila de la tabla. 
    
## <a name="remarks"></a>Comentarios

El método **ITableData:: HrDeleteRow** quita la fila de la tabla que contiene la columna que coincide con la propiedad a la que señala el parámetro _lpSPropValue_ . Los datos de la fila se eliminan y la fila se quita de todas las vistas abiertas. 
  
Después de eliminar la fila, se envían notificaciones a todos los clientes o proveedores de servicios que tienen una vista de la tabla y que han llamado al método [IMAPITable:: Advise](imapitable-advise.md) para registrarse para las notificaciones. 
  
La eliminación de una fila no reduce el conjunto de columnas que está disponible para vistas existentes o vistas abiertas posteriormente, incluso si la fila eliminada es la última que tiene un valor para una columna específica.
  
## <a name="see-also"></a>Vea también



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRows](itabledata-hrdeleterows.md)
  
[ITableData::HrModifyRow](itabledata-hrmodifyrow.md)
  
[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

