---
title: IMAPISessionAdminServices
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.AdminServices
api_type:
- COM
ms.assetid: 487fab39-5c2c-4e1a-9f90-4da64f5e198b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 850d4d952102e11d11234fa3184b88e280a98c21
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817456"
---
# <a name="imapisessionadminservices"></a>IMAPISession::AdminServices

  
  
**Hace referencia a**: Outlook 
  
Devuelve un puntero [IMsgServiceAdmin](imsgserviceadminiunknown.md) para realizar cambios en los servicios de mensajes. 
  
```cpp
HRESULT AdminServices(
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lppServiceAdmin_
  
> [out] Un puntero a un puntero a un objeto de administración del servicio de mensajes.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Un puntero a un objeto de administración del servicio de mensajes se devolvió correctamente.
    
## <a name="notes-to-callers"></a>Notas para los llamadores

El método **IMAPISession::AdminServices** crea un objeto de administración de servicio de mensaje, un objeto que admite la interfaz **IMsgServiceAdmin** y devuelve un puntero. Mediante el uso de este puntero, puede llamar a métodos **IMsgServiceAdmin** para cambiar cualquiera de los servicios de mensaje en el perfil de sesión. Tenga en cuenta que estos cambios no tendrán efecto hasta la siguiente sesión; la sesión actual no se ve afectada. 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |GetServerName  <br/> |MFCMAPI usa el método **IMAPISession::AdminServices** para tener acceso a los perfiles para leer el nombre del servidor.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)
  
[IProfAdmin::AdminServices](iprofadmin-adminservices.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

