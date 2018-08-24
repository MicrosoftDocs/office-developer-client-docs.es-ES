---
title: IMsgServiceAdminRenameMsgService
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.RenameMsgService
api_type:
- COM
ms.assetid: eba0e7f2-03c1-4713-aa36-3d0b398cd197
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a6eba20fb346f53052808abf8fcae8993d423d34
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589563"
---
# <a name="imsgserviceadminrenamemsgservice"></a>IMsgServiceAdmin::RenameMsgService

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
En desuso. Asigna un nombre nuevo a un servicio de mensajes. 
  
```cpp
HRESULT RenameMsgService(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPSTR lpszDisplayName
);
```

## <a name="parameters"></a>Parámetros

 _lpUID_
  
> [entrada] Un puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único para el servicio de mensajes cambiar el nombre. 
    
 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lpszDisplayName_
  
> [entrada] Un puntero al nuevo nombre para el servicio de mensajes.
    
## <a name="return-value"></a>Valor devuelto

MAPI_E_NO_SUPPORT 
  
> MAPI no es compatible con el cambio de nombre de este servicio de mensajes. **RenameMsgService** siempre devuelve este valor. 
    
## <a name="remarks"></a>Comentarios

Para asignar un nombre nuevo a un servicio de mensajes, los clientes deben usar la propiedad **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) del servicio de mensajes. Los nombres de los proveedores de servicios en un servicio de mensajes se almacenan en sus propiedades **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). 
  
## <a name="see-also"></a>Vea también



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

