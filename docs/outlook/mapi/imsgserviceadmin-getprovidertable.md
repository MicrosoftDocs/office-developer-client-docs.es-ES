---
title: IMsgServiceAdminGetProviderTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.GetProviderTable
api_type:
- COM
ms.assetid: 7180bff2-91ad-4e11-923e-2a9acefa3215
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 1185a35df471fc3f85cbf50fd8ad3baa3927e72b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428770"
---
# <a name="imsgserviceadmingetprovidertable"></a>IMsgServiceAdmin::GetProviderTable

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona acceso a la tabla del proveedor, una lista de los proveedores de servicios en el perfil.
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parámetros

 _ulFlags_
  
> [entrada] Siempre NULL.
    
 _lppTable_
  
> [salida] Puntero a un puntero a la tabla del proveedor.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La tabla del proveedor se devolvió correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IMsgServiceAdmin::GetProviderTable** proporciona acceso a la tabla del proveedor MAPI, una tabla que enumera todos los proveedores de libreta de direcciones, almacén de mensajes y transporte instalados actualmente en el perfil. 
  
A diferencia de la tabla de proveedor devuelta a través del método [IProviderAdmin::GetProviderTable,](iprovideradmin-getprovidertable.md) la tabla de proveedor devuelta a través de **IMsgServiceAdmin::GetProviderTable** no puede incluir filas adicionales que representen información asociada a uno o más proveedores de servicios en el perfil. 
  
Los proveedores que se han eliminado o que están en uso pero que se han marcado para su eliminación no se incluyen en la tabla del proveedor. Las tablas de proveedor son estáticas, lo que significa que las adiciones o eliminaciones posteriores del perfil no se reflejan en la tabla. 
  
Si el perfil no tiene proveedores, **GetProviderTable** devuelve una tabla con cero filas y S_OK valor devuelto. 
  
Para obtener una lista completa de las columnas de la tabla de proveedor, vea [Tabla de proveedor](provider-tables.md). 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para recuperar las filas de una tabla de proveedor en orden de transporte, use el siguiente procedimiento:
  
1. Llame al [método IMAPITable::Restrict](imapitable-restrict.md) para imponer una restricción de propiedad que coincida con la propiedad **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) con MAPI_TRANSPORT_PROVIDER.
    
2. Llame al [método IMAPITable::SortTable](imapitable-sorttable.md) para ordenar la tabla por la **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)). 
    
3. Llame al [método IMAPITable::QueryRows](imapitable-queryrows.md) para obtener las filas de la tabla. 
    
Una alternativa a estas llamadas es realizar una sola llamada a la función [HrQueryAllRows](hrqueryallrows.md) con todas las estructuras de datos apropiadas pasadas. 
  
Si recupera las columnas **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) en cada una de las filas, puede usar esta matriz de estructuras **MAPIUID** para establecer el orden de transporte en una llamada a [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).
  
Al establecer MAPI_UNICODE marca en  _el parámetro ulFlags,_ se hace lo siguiente: 
  
- Establece el tipo de cadena en Unicode para los datos devueltos para las columnas activas iniciales de la tabla de proveedor por el método [IMAPITable::QueryColumns.](imapitable-querycolumns.md) Las columnas activas iniciales de una tabla de proveedor son aquellas columnas que devuelve el método **QueryColumns** antes de que el proveedor que contiene la tabla llame al método [IMAPITable::SetColumns.](imapitable-setcolumns.md) 
    
- Establece el tipo de cadena en Unicode para los datos devueltos por **QueryRows** para las filas activas iniciales de la tabla del proveedor. Las filas activas iniciales de una tabla de proveedor son aquellas filas que **QueryRows** devuelve antes de que el proveedor que contiene la tabla llame a **SetColumns**. 
    
- Controla los tipos de propiedades del criterio de ordenación devuelto por el método [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) antes de que el cliente que contiene la tabla del proveedor llame al método [IMAPITable::SortTable.](imapitable-sorttable.md) 
    
## <a name="see-also"></a>Consulte también



[IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md)
  
[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)
  
[IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

