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
ms.openlocfilehash: 989c6872e78ef78e5e0b18149a186d4f920ca603
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563467"
---
# <a name="itabledatahrdeleterow"></a>ITableData::HrDeleteRow

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Elimina una fila de tabla.
  
```cpp
HRESULT HrDeleteRow(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>Parámetros

 _lpSPropValue_
  
> [entrada] Un puntero a una estructura de valor de propiedad que describe la columna de índice de la fila que se va a eliminar. El miembro **ulPropTag** de la estructura del valor de propiedad debe contener la misma etiqueta de propiedad como el parámetro _ulPropTagIndexColumn_ de la llamada a la función [CreateTable](createtable.md) . 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La fila se eliminó correctamente.
    
MAPI_E_NOT_FOUND 
  
> La propiedad indicada por el parámetro _lpSPropValue_ no identifica una fila en la tabla. 
    
## <a name="remarks"></a>Comentarios

El método **ITableData::HrDeleteRow** quita la fila de tabla que contiene la columna que coincide con la propiedad indicada por el parámetro _lpSPropValue_ . Se eliminan los datos de la fila y la fila se quita de todas las vistas abiertas. 
  
Después de que se elimina la fila, se envían a todos los clientes o proveedores de servicios que tienen una vista de la tabla y que ha llamado [IMAPITable::Advise](imapitable-advise.md) (método) de la tabla para registrar para las notificaciones. 
  
Eliminación de una fila no reduce el conjunto de columna que está disponible para las vistas existentes o vuelven a abrir vistas, incluso si la fila eliminada es la última fila que tenga un valor para una columna específica.
  
## <a name="see-also"></a>Recursos adicionales



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRows](itabledata-hrdeleterows.md)
  
[ITableData::HrModifyRow](itabledata-hrmodifyrow.md)
  
[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

