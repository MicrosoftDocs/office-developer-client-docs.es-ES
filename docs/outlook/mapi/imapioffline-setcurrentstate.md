---
title: IMAPIOfflineSetCurrentState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline.SetCurrentState
api_type:
- COM
ms.assetid: c0aa0df2-79f9-2558-7eb6-accae9bef4b2
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 13a4cf401cf51241a52401668eef008d65aa5459
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567142"
---
# <a name="imapiofflinesetcurrentstate"></a>IMAPIOffline::SetCurrentState

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Establece el estado actual de un objeto sin conexión a en línea o sin conexión.
  
```cpp
HRESULT SetCurrentState( 
    ULONG ulFlags, 
    ULONG ulMask, 
    ULONG ulState, 
    void* pReserved 
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Modifica el comportamiento de esta llamada. Los valores admitidos son:
    
MAPIOFFLINE_FLAG_BLOCK
  
> Al establecer _ulFlags_ en este valor se bloqueará la llamada **SetCurrentState** hasta que se complete el cambio de estado. De forma predeterminada la transición tiene lugar de forma asincrónica. Cuando la transición se está deshaciendo la desprotección de forma asincrónica, todas las llamadas de **SetCurrentState** devolverá **E_PENDING** hasta que se complete el cambio. 
    
MAPIOFFLINE_FLAG_DEFAULT
  
> Establece el estado actual sin bloquear.
    
 _ulMask_
  
> [entrada] La parte de que cambie el estado. El único valor admitido es MAPIOFFLINE_STATE_OFFLINE_MASK.
    
 _ulState_
  
> [entrada] El estado para cambiar a. Debe ser uno de estos dos valores:
    
MAPIOFFLINE_STATE_ONLINE
  
> 
    
MAPIOFFLINE_STATE_OFFLINE
  
> 
    
 _Conserva_
  
> Este parámetro está reservado para uso interno de Outlook y no se admite. 
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> Se cambió correctamente el estado del objeto sin conexión.
    
E_PENDING
  
> Esto indica que el estado del objeto sin conexión está cambiando de forma asincrónica. Esto se produce cuando _ulFlags_ está establecida en MAPIOFFLINE_FLAG_BLOCK en una anterior llamada **SetCurrentState** , y cualquier llamada **SetCurrentState** subsiguiente devolverá este valor hasta que se complete el cambio de estado asincrónico. 
    
## <a name="see-also"></a>Vea también



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOffline::GetCurrentState](imapioffline-getcurrentstate.md)


[Constantes MAPI](mapi-constants.md)

