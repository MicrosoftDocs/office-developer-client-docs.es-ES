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
ms.openlocfilehash: cb7fa7bb7dc17a89fc7cc40ae370accc40fa3941
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579846"
---
# <a name="imapisessionadminservices"></a>IMAPISession::AdminServices

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
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
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |GetServerName  <br/> |MFCMAPI usa el método **IMAPISession::AdminServices** para tener acceso a los perfiles para leer el nombre del servidor.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)
  
[IProfAdmin::AdminServices](iprofadmin-adminservices.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

