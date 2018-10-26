---
title: IMsgServiceAdminAdminProviders
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.AdminProviders
api_type:
- COM
ms.assetid: 0d605e2c-10db-46e1-95d5-12fabd524baa
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1b03245d7af4c6fb3879e597d8345e5d9888e164
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567212"
---
# <a name="imsgserviceadminadminproviders"></a>IMsgServiceAdmin::AdminProviders

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Devuelve un puntero que proporciona acceso a un objeto de administración del proveedor.
  
```cpp
HRESULT AdminProviders(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPPROVIDERADMIN FAR * lppProviderAdmin
);
```

## <a name="parameters"></a>Parámetros

 _lpUID_
  
> [entrada] Un puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único para el servicio de mensajes que van a administrar. 
    
 _ulFlags_
  
> [entrada] Siempre es NULL. 
    
 _lppProviderAdmin_
  
> [out] Un puntero a un puntero a un objeto de administración del proveedor.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El objeto de proveedor de administración se devolvió correctamente.
    
MAPI_E_NOT_FOUND 
  
> El **MAPIUID** que señala _lpUID_ no existe. 
    
## <a name="remarks"></a>Comentarios

El método **IMsgServiceAdmin::AdminProviders** proporciona acceso a un objeto de administración del proveedor. Administración de un proveedor es un objeto que admite la interfaz [IProviderAdmin](iprovideradminiunknown.md) y permite a los clientes hacer lo siguiente: 
  
- Agregar proveedores de servicios a un servicio de mensajes.
    
- Eliminar proveedores de servicios de un servicio de mensajes.
    
- Abra las secciones del perfil.
    
- Obtener acceso a la tabla de proveedor de servicios de mensaje.
    
Los tipos de cambios que realmente se pueden establecer con un servicio de mensajes mientras el perfil está en uso dependen del servicio de mensajes. Sin embargo, la mayoría de los servicios de mensaje no admiten los cambios, como agregar y eliminar proveedores mientras el perfil está en uso.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para recuperar la estructura **MAPIUID** para el servicio de mensajes administrar, recuperar la columna de propiedad **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) de la fila del servicio de mensajes en la tabla de servicios de mensaje. Para obtener más información, vea el procedimiento descrito en el método [IMsgServiceAdmin::](imsgserviceadmin-createmsgservice.md) . 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDisplayItem  <br/> |MFCMAPI utiliza el método **IMsgServiceAdmin::AdminProviders** para abrir un objeto de administración del proveedor para un servicio.  <br/> |
   
## <a name="see-also"></a>Vea también



[IProviderAdmin : IUnknown](iprovideradminiunknown.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

