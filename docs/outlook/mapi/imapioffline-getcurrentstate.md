---
title: IMAPIOfflineGetCurrentState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline.GetCurrentState
api_type:
- COM
ms.assetid: f3769e83-d678-1087-fc0f-b4f156386333
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f5170ceb443dcde075440bf84d29000afe4680c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419873"
---
# <a name="imapiofflinegetcurrentstate"></a>IMAPIOffline::GetCurrentState

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Obtiene el estado actual en línea o sin conexión de un objeto sin conexión.
  
```cpp
HRESULT GetCurrentState( 
    ULONG* pulState 
);
```

## <a name="parameters"></a>Parameters

 _pulState_
  
> [salida] El estado actual en línea o sin conexión de un objeto sin conexión. Debe ser uno de estos dos valores:
    
MAPIOFFLINE_STATE_ONLINE
  
> 
    
MAPIOFFLINE_STATE_OFFLINE
  
> 
    
## <a name="see-also"></a>Vea también



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOffline::SetCurrentState](imapioffline-setcurrentstate.md)


[Constantes MAPI](mapi-constants.md)

