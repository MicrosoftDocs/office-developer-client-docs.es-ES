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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 4272edef5b1b72944d1d27f0e4dd99ee4956aa57
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817729"
---
# <a name="imsgserviceadmingetprovidertable"></a>IMsgServiceAdmin::GetProviderTable

  
  
**Se aplica a**: Outlook 
  
Proporciona acceso a la tabla de proveedor, una lista de los proveedores de servicios en el perfil.
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Siempre es NULL.
    
 _lppTable_
  
> [out] Un puntero a un puntero a la tabla de proveedor.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> En la tabla de proveedor se devolvió correctamente.
    
## <a name="remarks"></a>Notas

El método **IMsgServiceAdmin::GetProviderTable** proporciona acceso a la tabla de proveedor MAPI, una tabla que enumera todos los la libreta de direcciones, almacén de mensajes y proveedores de transporte instalados actualmente en el perfil. 
  
A diferencia de la tabla de proveedor devuelta a través del método [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md) , en la tabla de proveedor devuelta a través de **IMsgServiceAdmin::GetProviderTable** no puede incluir filas adicionales que representan información asociada con uno o más proveedores de servicio en el perfil. 
  
Los proveedores que se han eliminado, o están en uso, se han marcado para su eliminación, pero no se incluyen en la tabla proveedor. Tablas de proveedor son estáticas, lo que significa que adiciones posteriores a o eliminaciones desde el perfil no se reflejan en la tabla. 
  
Si el perfil no tiene ningún proveedor, **GetProviderTable** devuelve un objeto table con cero filas y el valor devuelto de S_OK. 
  
Para obtener una lista completa de las columnas en la tabla de proveedor, vea la [Tabla de proveedor](provider-tables.md). 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para recuperar las filas de una tabla de proveedor en el orden de transporte, utilice el procedimiento siguiente:
  
1. Llame al método [IMAPITable:: Restrict](imapitable-restrict.md) para imponer una restricción de propiedad que coincida con la propiedad **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) con MAPI_TRANSPORT_PROVIDER.
    
2. Llame al método [SortTable](imapitable-sorttable.md) para ordenar la tabla por la columna **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)). 
    
3. Llame al método [IMAPITable:: QueryRows](imapitable-queryrows.md) para obtener las filas de la tabla. 
    
Es una alternativa a estas llamadas realizar una única llamada a la función [HrQueryAllRows](hrqueryallrows.md) con todos los datos adecuados estructuras que se pasan. 
  
Si recupera las columnas **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) en cada una de las filas, puede utilizar esta matriz de las estructuras **MAPIUID** para establecer el orden de transporte en una llamada a [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).
  
Establecer el indicador MAPI_UNICODE en el parámetro _ulFlags_ hace lo siguiente: 
  
- Establece el tipo de cadena a formato Unicode para los datos devueltos para las columnas activas iniciales de la tabla de proveedor por el método [IMAPITable::QueryColumns](imapitable-querycolumns.md) . Las columnas activas iniciales para una tabla de proveedor son aquellas columnas que devuelve el método **QueryColumns** antes el proveedor que contiene el método [IMAPITable::SetColumns](imapitable-setcolumns.md) de las llamadas de la tabla. 
    
- Establece el tipo de cadena a formato Unicode para los datos devueltos para las filas activas iniciales de la tabla proveedor por **QueryRows**. Las filas activas iniciales para una tabla de proveedor son aquellas filas **que QueryRows** devuelve antes el proveedor que contiene las llamadas de tabla **SetColumns**. 
    
- Controles de los tipos de propiedad de devuelto por el método [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) antes de que el cliente que contiene la tabla de proveedor llama al método [SortTable](imapitable-sorttable.md) el criterio de ordenación. 
    
## <a name="see-also"></a>Ver también



[IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md)
  
[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)
  
[IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)
  
[IMsgServiceAdmin: IUnknown](imsgserviceadminiunknown.md)

