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
ms.openlocfilehash: 2f0f1fb94ea36512bbc40df8a4877e89d2613a25
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309985"
---
# <a name="imsgserviceadminrenamemsgservice"></a>IMsgServiceAdmin::RenameMsgService

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
En desuso. Asigna un nombre nuevo a un servicio de mensajes. 
  
```cpp
HRESULT RenameMsgService(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPSTR lpszDisplayName
);
```

## <a name="parameters"></a>Parameters

 _lpUID_
  
> a Un puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único del servicio de mensajes que se va a cambiar de nombre. 
    
 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lpszDisplayName_
  
> a Un puntero al nuevo nombre del servicio de mensajes.
    
## <a name="return-value"></a>Valor devuelto

MAPI_E_NO_SUPPORT 
  
> MAPI no admite el cambio de nombre de este servicio de mensajes. **RenameMsgService** siempre devuelve este valor. 
    
## <a name="remarks"></a>Comentarios

Para asignar un nuevo nombre a un servicio de mensajes, los clientes deben usar la propiedad **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) del servicio de mensajes. Los nombres de los proveedores de servicios de un servicio de mensajes se almacenan en sus propiedades **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). 
  
## <a name="see-also"></a>Vea también



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

