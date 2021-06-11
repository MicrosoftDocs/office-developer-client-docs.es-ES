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
ms.openlocfilehash: c639523a02047bf00c378dafd7bc698d7d4e5fff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405908"
---
# <a name="imapisessionadminservices"></a>IMAPISession::AdminServices

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve un [puntero IMsgServiceAdmin](imsgserviceadminiunknown.md) para realizar cambios en los servicios de mensajes. 
  
```cpp
HRESULT AdminServices(
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lppServiceAdmin_
  
> [salida] Puntero a un puntero a un objeto de administración del servicio de mensajes.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se ha devuelto correctamente un puntero a un objeto de administración del servicio de mensajes.
    
## <a name="notes-to-callers"></a>Notas para los llamadores

El **método IMAPISession::AdminServices** crea un objeto de administración del servicio de mensajes, un objeto que admite la interfaz **IMsgServiceAdmin** y devuelve un puntero. Con este puntero, puede llamar a **los métodos IMsgServiceAdmin** para cambiar cualquiera de los servicios de mensajes del perfil de sesión. Tenga en cuenta que estos cambios no tienen efecto hasta la siguiente sesión; la sesión actual no se ha afectado. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |GetServerName  <br/> |MFCMAPI usa el **método IMAPISession::AdminServices** para obtener acceso al perfil para leer el nombre del servidor.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)
  
[IProfAdmin::AdminServices](iprofadmin-adminservices.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

