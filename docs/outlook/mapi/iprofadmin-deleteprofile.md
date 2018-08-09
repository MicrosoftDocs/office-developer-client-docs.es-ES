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
ms.openlocfilehash: 249d2dcf3a298abde85bdc53620680146d43c168
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817898"
---
# <a name="iprofadmindeleteprofile"></a>IProfAdmin::DeleteProfile

  
  
**Hace referencia a**: Outlook 
  
Elimina un perfil.
  
```cpp
HRESULT DeleteProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parámetros

 _lpszProfileName_
  
> [entrada] Un puntero al nombre del perfil que se va a eliminar.
    
 _ulFlags_
  
> [entrada] Siempre es NULL. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El perfil se eliminó correctamente.
    
MAPI_E_NOT_FOUND 
  
> No existe el perfil especificado.
    
## <a name="remarks"></a>Comentarios

El método **IProfAdmin::DeleteProfile** elimina un perfil. Si el perfil que desea eliminar está en uso cuando se llama a **DeleteProfile** , **DeleteProfile** devuelve S_OK, pero no se elimina inmediatamente el perfil. En su lugar, **DeleteProfile** marca el perfil para su eliminación y se elimina después de ya no se usa, cuando todos sus sesiones activas han finalizado. 
  
La función de punto de entrada para cada servicio de mensajes en el perfil se llama con el valor MSG_SERVICE_DELETE establecido en el parámetro _ulContext_ . En primer lugar, la función elimina el servicio y, a continuación, elimina la sección de perfil del servicio. La función de punto de entrada de servicio de mensajes no se llama de nuevo después de que se ha eliminado el servicio. 
  
Para eliminar un perfil no se requiere ninguna contraseña.
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |HrRemoveProfile  <br/> |MFCMAPI usa el método **IProfAdmin::DeleteProfile** para eliminar el perfil seleccionado.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

