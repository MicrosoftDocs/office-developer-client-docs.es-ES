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
ms.openlocfilehash: 6b7360995a781824b50ff02b5d2dec8e481e7ba7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422764"
---
# <a name="imsgserviceadminadminproviders"></a>IMsgServiceAdmin::AdminProviders

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve un puntero que proporciona acceso a un objeto de administración del proveedor.
  
```cpp
HRESULT AdminProviders(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPPROVIDERADMIN FAR * lppProviderAdmin
);
```

## <a name="parameters"></a>Parameters

 _lpUID_
  
> [in] Puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único del servicio de mensajes que se va a administrar. 
    
 _ulFlags_
  
> [in] Siempre NULL. 
    
 _lppProviderAdmin_
  
> [salida] Puntero a un puntero a un objeto de administración del proveedor.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El objeto de administración del proveedor se devolvió correctamente.
    
MAPI_E_NOT_FOUND 
  
> El **MAPIUID señalado** por  _lpUID_ no existe. 
    
## <a name="remarks"></a>Comentarios

El **método IMsgServiceAdmin::AdminProviders** proporciona acceso a un objeto de administración del proveedor. Una administración de proveedor es un objeto que admite la [interfaz IProviderAdmin](iprovideradminiunknown.md) y permite a los clientes hacer lo siguiente: 
  
- Agregar proveedores de servicios a un servicio de mensajes.
    
- Eliminar proveedores de servicios de un servicio de mensajes.
    
- Abra secciones de perfil.
    
- Obtenga acceso a la tabla del proveedor de servicios de mensajes.
    
Los tipos de cambios que realmente se pueden realizar en un servicio de mensajes mientras el perfil está en uso dependen del servicio de mensajes. Sin embargo, la mayoría de los servicios de mensajes no admiten cambios como agregar y eliminar proveedores mientras el perfil está en uso.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para recuperar la estructura **MAPIUID** del servicio de mensajes que se va a administrar, recupere la columna de propiedad **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) de la fila del servicio de mensajes de la tabla de servicio de mensajes. Para obtener más información, vea el procedimiento descrito en el [método IMsgServiceAdmin::CreateMsgService.](imsgserviceadmin-createmsgservice.md) 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDisplayItem  <br/> |MFCMAPI usa el **método IMsgServiceAdmin::AdminProviders** para abrir un objeto de administración de proveedor para un servicio.  <br/> |
   
## <a name="see-also"></a>Vea también



[IProviderAdmin : IUnknown](iprovideradminiunknown.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

