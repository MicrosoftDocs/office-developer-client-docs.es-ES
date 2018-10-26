---
title: ITableDataHrNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrNotify
api_type:
- COM
ms.assetid: 98548b50-342e-434a-9ad3-c37ba418c5ce
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 20831901567f177ada70a6cea94db0537786db94
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571440"
---
# <a name="itabledatahrnotify"></a>ITableData::HrNotify

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Envía una notificación para una fila de tabla.
  
```cpp
HRESULT HrNotify(
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _cValues_
  
> [entrada] El recuento de valores de propiedad en la estructura [SPropValue](spropvalue.md) indicada por el parámetro _lpSPropValue_ . 
    
 _lpSPropValue_
  
> [entrada] Un puntero a una estructura **SPropValue** que se describe los valores de las columnas de la fila de destino. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

El método **ITableData::HrNotify** envía una notificación de TABLE_ROW_MODIFIED para la fila que coincide con la fila que se describen las propiedades que apunta el parámetro _lpSPropValue_ . **HrNotify** envía la notificación, independientemente de si se han producido cambios en la fila. Todos los clientes y proveedores de servicios que tienen las vistas de la tabla y han llamado [IMAPITable::Advise](imapitable-advise.md) para registrar las notificaciones en las vistas de reciben esta notificación. 
  
## <a name="see-also"></a>Vea también



[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

