---
title: imapiinitmonitor-beginwait
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIINITMONITOR.BeginWait
api_type:
- COM
ms.assetid: 71f565a9-651c-42b5-9102-91b728b681ae
description: IMAPIInitMonitor::BeginWait"
Last modified: April 26, 2021
ms.openlocfilehash: 43a88507cbfc23b3b842f51e69eb4bd791bcfda8
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062021"
---
# <a name="imapiinitmonitorbeginwait"></a>IMAPIInitMonitor::BeginWait
  
**Se aplica a**: Outlook 2016 | 2019
  
Inicie una espera para que transcurra la inicialización MAPI o el número especificado de milisegundos. Esto devuelve una interfaz IMAPIWaitResult que debería llamar a **IMAPIWaitResult::End** para iniciar la espera. Esto permite al autor de la llamada controlar qué subproceso está bloqueado mientras estamos esperando.

```cpp
HRESULT IMAPIInitMonitor::BeginWait(DWORD timeout, IMAPIWaitResult** ppResult)
```

## <a name="parameters"></a>Parameters
_tiempo de espera_
>[in] El número de milisegundos que se esperará a la inicialización MAPI, esto puede establecerse en INFINITE para esperar para siempre a que se pueda producir la inicialización.

_ppResult_
>[salida] Puntero para recibir la interfaz de espera recién creada.

## <a name="return-value"></a>Valor devuelto
S_OK
>Se ha iniciado correctamente una operación de espera.

E_OUTOFMEMORY
>No había suficiente memoria para crear un nuevo objeto

## <a name="remarks"></a>Comentarios
Esta API proporcionaba al autor de la llamada una interfaz (que es segura para subprocesos) que se puede usar para iniciar una espera de bloqueo para la inicialización mapi. Esto permite al consumidor degradar la mejor espera para esperar a su aplicación.   El comportamiento de llamar a IMAPIWaitResult::End es idéntico a llamar a IMAPIInitMonitor::Wait.

## <a name="see-also"></a>Vea también

[IMAPIInitMonitor](imapiinitmonitoriunknown.md)

[IMAPIInitMonitor::IsInitialized](imapiinitmonitor-isinitialized.md)

[IMAPIInitMonitor::Wait](imapiinitmonitor-wait.md)

[CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md)

[IMAPIWaitResult](imapiwaitresultiunknown.md)
