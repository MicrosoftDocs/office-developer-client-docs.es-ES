---
title: IMAPISupportGetSvcConfigSupportObj
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetSvcConfigSupportObj
api_type:
- COM
ms.assetid: 56c3bdae-a3a8-4334-b6d2-a89c6820d72e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6de0fed4df9d23e67c3520ffb019a961b890f988
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411312"
---
# <a name="imapisupportgetsvcconfigsupportobj"></a>IMAPISupport::GetSvcConfigSupportObj

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea un objeto de soporte técnico del servicio de mensajes.
  
```cpp
HRESULT GetSvcConfigSupportObj(
  ULONG ulFlags,
  LPMAPISUP FAR * lppSvcSupport
);
```

## <a name="parameters"></a>Parámetros

 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lppSvcSupport_
  
> [salida] Puntero a un puntero al nuevo objeto de soporte del servicio de mensajes.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El objeto de compatibilidad con la configuración se creó correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::GetSvcConfigSupportObj** se implementa para todos los objetos de compatibilidad. Los proveedores de servicios llaman a **GetSvcConfigSupportObj para** crear un objeto de compatibilidad de configuración para pasar a una función de punto de entrada del servicio de mensajes. 
  
Una función de punto de entrada del servicio de mensajes se basa en el prototipo [MSGSERVICEENTRY](msgserviceentry.md) y la llaman los métodos de la [interfaz IMsgServiceAdmin.](imsgserviceadminiunknown.md) Una función de punto de entrada del servicio de mensajes permite que los servicios de mensajes se configuren a sí mismos o realicen otras acciones cuando se cambia el perfil. Las funciones de punto de entrada del servicio de mensajes pueden admitir cambios de configuración mostrando una hoja de propiedades o a través de una matriz de valores de propiedad pasada al método [IMsgServiceAdmin::ConfigureMsgService.](imsgserviceadmin-configuremsgservice.md) 
  
## <a name="see-also"></a>Consulte también



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)
  
[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

