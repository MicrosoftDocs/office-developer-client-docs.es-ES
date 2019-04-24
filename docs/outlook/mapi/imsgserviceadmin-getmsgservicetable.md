---
title: IMsgServiceAdminGetMsgServiceTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.GetMsgServiceTable
api_type:
- COM
ms.assetid: 064dd5ca-0108-4045-b17b-0bb29cb93346
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fcaebb96d4dca4e6bfbee7491dabeafcbd93a2eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309978"
---
# <a name="imsgserviceadmingetmsgservicetable"></a>IMsgServiceAdmin::GetMsgServiceTable

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona acceso a la tabla servicio de mensajes, una lista de los servicios de mensajes del perfil.
  
```cpp
HRESULT GetMsgServiceTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> a Siempre NULL.
    
 _lppTable_
  
> contempla Un puntero a un puntero a la tabla de servicio de mensajes.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La tabla de servicio de mensajes se devolvió correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMsgServiceAdmin:: GetMsgServiceTable** proporciona acceso a la tabla de servicio de mensajes, una tabla que MAPI mantiene y enumera los servicios de mensajes instalados actualmente en el perfil de sesión. Para obtener una lista completa de las columnas de la tabla servicio de mensajes, vea [Message Service Table](message-service-tables.md).
  
La tabla de servicio de mensajes es estática. Una vez que se ha concedido acceso a un cliente, las adiciones o eliminaciones de servicios de mensajes posteriores no lo afectarán. Si no hay ningún servicio de mensajes en el perfil actual, **GetMsgServiceTable** devuelve una tabla con cero filas. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MsgServiceTableDlg. cpp  <br/> |CMsgServiceTableDlg:: OnRefreshView  <br/> |MFCMAPI usa el método **IMsgServiceAdmin:: GetMsgServiceTable** para cargar la tabla de servicios en un perfil para representarlo en la vista.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

