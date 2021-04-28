---
title: imapiinitmonitor-wait
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIINITMONITOR.Wait
api_type:
- COM
ms.assetid: ed566cae-35a2-4716-817b-54d1ba6825c6
description: IMAPIAMonitor::Wait
Last modified: April 26, 2021
ms.openlocfilehash: ee46a2744e67804c9dfdac8d7512db1d7b07f8ba
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062014"
---
# <a name="imapiinitmonitorwait"></a>IMAPIInitMonitor::Wait
  
**Se aplica a**: Outlook 2013 | Outlook 2016 | 2019
  
Inicia una llamada BLOCKING en este subproceso, que devolverá cuando haya transcurrido el número especificado de milisegundos o cuando se haya inicializado MAPI. INFINITE se puede usar para una espera infinita.

```cpp
HRESULT IMAPIInitMonitor::Wait(DWORD timeout)
```

## <a name="parameters"></a>Parámetros
_tiempo de espera_
> [in] El número de milisegundos que hay que esperar a que se inicialice MAPI, puede pasar INFINITE (0xFFFFFFFF) para esperar para siempre.

## <a name="return-value"></a>Valor devuelto

S_OK
> MAPI se ha inicializado correctamente.

HRESULT_FROM_WIN32(ERROR_TIMEOUT)
> Cuando se le da un tiempo de espera no infinito, esto indica que MAPI no se inicializó durante ese período.

## <a name="remarks"></a>Comentarios
  
## <a name="see-also"></a>Vea también

[IMAPIInitMonitor](imapiinitmonitoriunknown.md)

[IMAPIInitMonitor::IsInitialized](imapiinitmonitor-isinitialized.md)

[IMAPIInitMonitor::BeginWait](imapiinitmonitor-beginwait.md)

[CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md)

[IMAPIWaitResult](imapiwaitresultiunknown.md)
