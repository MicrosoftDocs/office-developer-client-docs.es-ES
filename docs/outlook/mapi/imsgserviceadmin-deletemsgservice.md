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
ms.openlocfilehash: 6cef03e33abab81a407698b73a007f247ef88194
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407385"
---
# <a name="imsgserviceadmindeletemsgservice"></a>IMsgServiceAdmin::DeleteMsgService

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Elimina un servicio de mensajes de un perfil.
  
```cpp
HRESULT DeleteMsgService(
  LPMAPIUID lpuid
);
```

## <a name="parameters"></a>Parameters

 _lpuid_
  
> a Un puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único del servicio de mensajes que se va a eliminar. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se ha eliminado el servicio de mensajes.
    
MAPI_E_NOT_FOUND 
  
> La **MAPIUID** a la que apunta _lpuid_ no coincide con un servicio de mensajes existente. 
    
## <a name="remarks"></a>Comentarios

El método **IMsgServiceAdmin::D eletemsgservice** elimina un servicio de mensajes de un perfil. **DeleteMsgService** quita todas las secciones de perfil relacionadas con el servicio de mensajes. 
  
 **DeleteMsgService** realiza los siguientes pasos para eliminar el servicio de mensajes: 
  
1. Llama a la función de punto de entrada del servicio de mensajes con el parámetro _ulContext_ establecido en MSG_SERVICE_DELETE antes de quitar las secciones de perfil. Esto permite que el servicio realice cualquier tarea específica del servicio. 
    
2. Elimina el servicio de mensajes.
    
3. Elimina la sección de perfil del servicio de mensajes.
    
No se llama de nuevo a la función de punto de entrada del servicio de mensajes después de que se haya eliminado el servicio.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para recuperar la estructura **MAPIUID** del servicio de mensajes que se va a eliminar, recupere la columna de propiedad **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) de la fila del servicio de mensajes en la tabla de servicios de mensajes. Para obtener más información, vea el procedimiento descrito en el método [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) . 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MsgServiceTableDlg. cpp  <br/> |CMsgServiceTableDlg:: OnDeleteSelectedItem  <br/> |MFCMAPI usa el método **IMsgServiceAdmin::D eletemsgservice** para eliminar el servicio seleccionado.  <br/> |
   
## <a name="see-also"></a>Ver también



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

