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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: ff748827950c79c3c94e9f70ce8b0bb335884290
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817736"
---
# <a name="imsgserviceadminrenamemsgservice"></a>IMsgServiceAdmin::RenameMsgService

  
  
**Se aplica a**: Outlook 
  
En desuso. Asigna un nombre nuevo a un servicio de mensajes. 
  
```cpp
HRESULT RenameMsgService(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPSTR lpszDisplayName
);
```

## <a name="parameters"></a>Sintaxis

 _lpUID_
  
> [entrada] Un puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único para el servicio de mensajes cambiar el nombre. 
    
 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lpszDisplayName_
  
> [entrada] Un puntero al nuevo nombre para el servicio de mensajes.
    
## <a name="return-value"></a>Valor devuelto

MAPI_E_NO_SUPPORT 
  
> MAPI no es compatible con el cambio de nombre de este servicio de mensajes. **RenameMsgService** siempre devuelve este valor. 
    
## <a name="remarks"></a>Notas

Para asignar un nombre nuevo a un servicio de mensajes, los clientes deben usar la propiedad **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) del servicio de mensajes. Los nombres de los proveedores de servicios en un servicio de mensajes se almacenan en sus propiedades **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). 
  
## <a name="see-also"></a>Ver también



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin: IUnknown](imsgserviceadminiunknown.md)

