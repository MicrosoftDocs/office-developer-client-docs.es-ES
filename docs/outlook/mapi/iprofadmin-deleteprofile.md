---
title: IProfAdminDeleteProfile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.DeleteProfile
api_type:
- COM
ms.assetid: 730af2da-4c4a-42a7-9d52-56d914107d64
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8aafb849a98028efb37646752a7b49fa5e6ef2ff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419593"
---
# <a name="iprofadmindeleteprofile"></a>IProfAdmin::DeleteProfile

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Elimina un perfil.
  
```cpp
HRESULT DeleteProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpszProfileName_
  
> [in] Puntero al nombre del perfil que se va a eliminar.
    
 _ulFlags_
  
> [in] Siempre NULL. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El perfil se eliminó correctamente.
    
MAPI_E_NOT_FOUND 
  
> El perfil especificado no existe.
    
## <a name="remarks"></a>Comentarios

El **método IProfAdmin::D eleteProfile** elimina un perfil. Si el perfil que se va a eliminar está en uso cuando se llama **a DeleteProfile,** **DeleteProfile** devuelve S_OK pero no elimina el perfil inmediatamente. En su lugar, **DeleteProfile** marca el perfil para su eliminación y lo elimina después de que ya no se esté utilizando, cuando todas sus sesiones activas han finalizado. 
  
Se llama a la función de punto de entrada para cada servicio de mensajes del perfil con el valor MSG_SERVICE_DELETE establecido en _el parámetro ulContext._ En primer lugar, la función elimina el servicio y, a continuación, elimina la sección de perfil del servicio. No se vuelve a llamar a la función de punto de entrada del servicio de mensajes después de eliminar el servicio. 
  
No se requiere ninguna contraseña para eliminar un perfil.
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |HrRemoveProfile  <br/> |MFCMAPI usa el **método IProfAdmin::D eleteProfile** para eliminar el perfil seleccionado.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

