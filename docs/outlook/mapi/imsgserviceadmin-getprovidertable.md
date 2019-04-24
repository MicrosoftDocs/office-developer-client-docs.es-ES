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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317384"
---
# <a name="imsgserviceadmingetprovidertable"></a>IMsgServiceAdmin::GetProviderTable

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona acceso a la tabla de proveedores, una lista de los proveedores de servicios del perfil.
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> a Siempre NULL.
    
 _lppTable_
  
> contempla Un puntero a un puntero a la tabla del proveedor.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La tabla de proveedores se devolvió correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMsgServiceAdmin:: GetProviderTable** proporciona acceso a la tabla de proveedores de MAPI, una tabla que enumera todos los proveedores de libreta de direcciones, de almacén de mensajes y de transporte instalados actualmente en el perfil. 
  
A diferencia de la tabla Provider devuelta a través del método [IProviderAdmin:: GetProviderTable](iprovideradmin-getprovidertable.md) , la tabla de proveedores devuelta por **IMsgServiceAdmin:: GetProviderTable** no puede incluir más filas que representen la información asociada con uno o más proveedores de servicios en el perfil. 
  
Los proveedores que se han eliminado o están en uso pero están marcados para su eliminación no se incluyen en la tabla de proveedores. Las tablas de proveedor son estáticas, lo que significa que las adiciones o eliminaciones posteriores del perfil no se reflejan en la tabla. 
  
Si el perfil no tiene proveedores, **GetProviderTable** devuelve una tabla con cero filas y el valor devuelto S_OK. 
  
Para obtener una lista completa de las columnas de la tabla de proveedores, consulte [TABLE Provider](provider-tables.md). 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para recuperar las filas de una tabla de proveedores en el orden de transporte, use el procedimiento siguiente:
  
1. Llame al método [IMAPITable:: Restrict](imapitable-restrict.md) para imponer una restricción de propiedad que coincida con la propiedad **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) con MAPI_TRANSPORT_PROVIDER.
    
2. Llame al método [IMAPITable:: SortTable](imapitable-sorttable.md) para ordenar la tabla por la columna **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)). 
    
3. Llame al método [IMAPITable:: QueryRows](imapitable-queryrows.md) para obtener las filas de la tabla. 
    
Una alternativa a estas llamadas es realizar una única llamada a la función [HrQueryAllRows](hrqueryallrows.md) con todas las estructuras de datos adecuadas que se pasan. 
  
Si recupera las columnas **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) en cada una de las filas, puede usar esta matriz de estructuras **MAPIUID** para establecer el orden de transporte en una llamada a [IMsgServiceAdmin:: MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).
  
La configuración de la marca MAPI_UNICODE en el parámetro _ulFlags_ hace lo siguiente: 
  
- Establece el tipo de cadena en Unicode para los datos devueltos por el método [IMAPITable:: QueryColumns](imapitable-querycolumns.md) para las columnas activas iniciales de la tabla del proveedor. Las columnas activas iniciales de una tabla de proveedor son las columnas que el método **QueryColumns** devuelve antes de que el proveedor que contiene la tabla llame al método [IMAPITable:: SetColumns](imapitable-setcolumns.md) . 
    
- Establece el tipo de cadena en Unicode para los datos devueltos por las filas activas iniciales de la tabla de proveedores mediante **QueryRows**. Las filas activas iniciales de una tabla Provider son las filas **QueryRows** devuelven antes de que el proveedor que contiene la tabla llame a **SetColumns**. 
    
- Controla los tipos de propiedades del criterio de ordenación devuelto por el método [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) antes de que el cliente que contiene la tabla de proveedores llame al método [IMAPITable:: SortTable](imapitable-sorttable.md) . 
    
## <a name="see-also"></a>Vea también



[IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md)
  
[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)
  
[IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

