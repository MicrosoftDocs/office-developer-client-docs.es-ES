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
ms.openlocfilehash: 0b6837b51b09ecd9a60630c613e1806cb10c1d87
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421742"
---
# <a name="imapiofflinesetcurrentstate"></a>IMAPIOffline::SetCurrentState

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Establece el estado actual de un objeto sin conexión en en línea o sin conexión.
  
```cpp
HRESULT SetCurrentState( 
    ULONG ulFlags, 
    ULONG ulMask, 
    ULONG ulState, 
    void* pReserved 
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> a Modifica el comportamiento de esta llamada. Los valores admitidos son:
    
MAPIOFFLINE_FLAG_BLOCK
  
> Si se establece _ulFlags_ en este valor, se bloqueará la llamada **SetCurrentState** hasta que se complete el cambio de estado. De forma predeterminada, la transición se lleva a cabo de forma asincrónica. Cuando la transición se produce asincrónicamente, todas las llamadas **SetCurrentState** devolverán **E_PENDING** hasta que el cambio se complete. 
    
MAPIOFFLINE_FLAG_DEFAULT
  
> Establece el estado actual sin bloquearse.
    
 _ulMask_
  
> a Parte del estado que se va a cambiar. El único valor admitido es MAPIOFFLINE_STATE_OFFLINE_MASK.
    
 _ulState_
  
> a Estado al que se va a cambiar. Debe ser uno de estos dos valores:
    
MAPIOFFLINE_STATE_ONLINE
  
> 
    
MAPIOFFLINE_STATE_OFFLINE
  
> 
    
 _Preserva_
  
> Este parámetro está reservado para uso interno de Outlook y no es compatible. 
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> El estado del objeto sin conexión se ha cambiado correctamente.
    
E_PENDING
  
> Esto indica que el estado del objeto sin conexión cambia de forma asincrónica. Esto ocurre cuando _ulFlags_ se establece en MAPIOFFLINE_FLAG_BLOCK en una llamada a **SetCurrentState** anterior, y cualquier llamada subsiguiente a **SetCurrentState** devolverá este valor hasta que se complete el cambio de estado asincrónico. 
    
## <a name="see-also"></a>Ver también



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOffline::GetCurrentState](imapioffline-getcurrentstate.md)


[Constantes MAPI](mapi-constants.md)

