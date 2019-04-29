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
ms.openlocfilehash: aa2170bf4bedfb441ad4808f774f6f71d5caf85e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413272"
---
# <a name="itabledatahrnotify"></a>ITableData::HrNotify

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Envía una notificación para una fila de tabla.
  
```cpp
HRESULT HrNotify(
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _cValues_
  
> a El número de valores de propiedad en la estructura [SPropValue](spropvalue.md) apuntado por el parámetro _lpSPropValue_ . 
    
 _lpSPropValue_
  
> a Un puntero a una estructura **SPropValue** que describe los valores de las columnas en la fila de destino. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

El método **ITableData:: HrNotify** envía una notificación de TABLE_ROW_MODIFIED para la fila que coincide con la fila descrita por las propiedades a las que apunta el parámetro _lpSPropValue_ . **HrNotify** envía la notificación independientemente de si se han producido cambios en la fila. Todos los clientes y proveedores de servicios que tienen vistas de la tabla y han llamado a [IMAPITable:: Advise](imapitable-advise.md) para registrarse en las notificaciones en sus vistas reciben esta notificación. 
  
## <a name="see-also"></a>Ver también



[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

