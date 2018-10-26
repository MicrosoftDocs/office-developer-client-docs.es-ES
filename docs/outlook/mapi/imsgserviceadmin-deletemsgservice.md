---
title: IMsgServiceAdminDeleteMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.DeleteMsgService
api_type:
- COM
ms.assetid: 3a6b34eb-9d46-488f-8d02-91b27c35de67
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e0d3d669982bee309901f913612ac1fb1622e60a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571147"
---
# <a name="imsgserviceadmindeletemsgservice"></a>IMsgServiceAdmin::DeleteMsgService

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Elimina un servicio de mensajes de un perfil.
  
```cpp
HRESULT DeleteMsgService(
  LPMAPIUID lpuid
);
```

## <a name="parameters"></a>Parámetros

 _lpuid_
  
> [entrada] Un puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único para el servicio de mensajes eliminar. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se ha eliminado el servicio de mensajes.
    
MAPI_E_NOT_FOUND 
  
> El **MAPIUID** que señala _lpuid_ no coincide con un servicio de mensaje existente. 
    
## <a name="remarks"></a>Comentarios

El método **IMsgServiceAdmin::DeleteMsgService** elimina un servicio de mensajes de un perfil. **DeleteMsgService** quita todos los perfiles en las secciones relacionadas con el servicio de mensajes. 
  
 **DeleteMsgService** realiza los siguientes pasos para eliminar el servicio de mensajes: 
  
1. Llamadas de función de punto de entrada del servicio de mensajes con el parámetro de _ulContext_ establecido en MSG_SERVICE_DELETE antes de que se han quitado las secciones del perfil. Esto permite que el servicio realizar las tareas específicas de servicio. 
    
2. Elimina el servicio de mensajes.
    
3. Elimina la sección de perfil de servicio de mensajes.
    
Función de punto de entrada del servicio de mensajes no se llama de nuevo después de que se ha eliminado el servicio.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para recuperar la estructura **MAPIUID** para el servicio de mensajes eliminar, recuperar la columna de propiedad **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) de la fila del servicio de mensajes en la tabla de servicios de mensaje. Para obtener más información, vea el procedimiento descrito en el método [IMsgServiceAdmin::](imsgserviceadmin-createmsgservice.md) . 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDeleteSelectedItem  <br/> |MFCMAPI usa el método **IMsgServiceAdmin::DeleteMsgService** para eliminar el servicio seleccionado.  <br/> |
   
## <a name="see-also"></a>Vea también



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

