---
title: IMAPIWaitResult::End
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIWaitResult.End
api_type:
- COM
ms.assetid: 7463c9e8-d065-4cc3-ac01-d428b57bbc88
description: IMAPIWaitResult::End
Last modified: April 26, 2021
ms.openlocfilehash: 3432bf3b71fa7e15cb4621d461a8d4bbe962f1ba
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062035"
---
# <a name="imapiwaitresultend"></a>IMAPIWaitResult::End
  
**Se aplica a**: Outlook 2013 | Outlook 2016 | 2019

Inicia una llamada BLOCKING en este subproceso, que devolverá cuando haya transcurrido el número especificado de milisegundos o cuando se haya inicializado MAPI. INFINITE se puede usar para una espera infinita.

```cpp
HRESULT IMAPIWaitResult::End(DWORD timeout)
```

## <a name="parameters"></a>Parámetros

_tiempo de espera_
> [in] El número de milisegundos para esperar a que se inicialice MAPI, puede pasar INFINITE (0xFFFFFFFF) para esperar para siempre.

## <a name="return-value"></a>Valor devuelto

S_OK
> MAPI se ha inicializado correctamente

HRESULT_FROM_WIN32(ERROR_TIMEOUT)
> Cuando se le da un tiempo de espera no infinito, esto indica que MAPI no se inicializó durante ese período.

## <a name="remarks"></a>Comentarios
Esta API se comporta exactamente igual que [IMAPInitMonitor::Wait](imapiinitmonitor-wait.md).
  
## <a name="see-also"></a>Vea también

[IMAPIInitMonitor::IsInitialized](imapiinitmonitor-isinitialized.md)

[IMAPIInitMonitor::BeginWait](imapiinitmonitor-beginwait.md)

[CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md)

[IMAPIWaitResult](imapiwaitresultiunknown.md)
