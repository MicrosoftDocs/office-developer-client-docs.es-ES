---
title: imapiinitmonitor-isinitialized
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIINITMONITOR.IsInitialized
api_type:
- COM
ms.assetid: 1af0bf93-6bcb-4235-ac30-0d00245ec636
description: IMAPIInitMonitor::IsInitialized
Last modified: April 26, 2021
ms.openlocfilehash: 6870c8fa0de51b626662c58b2c8c300c3a4d806e
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062028"
---
# <a name="imapiinitmonitorisinitialized"></a>IMAPIInitMonitor::IsInitialized
  
**Se aplica a**: Outlook 2013 | Outlook 2016 | 2019
  
Consulta MAPI para determinar si se inicializa actualmente en el proceso de llamada.

```cpp
BOOL IMAPIInitMonitor::IsInitialized()  
```

## <a name="parameters"></a>Parámetros
Ninguno

## <a name="return-value"></a>Valor devuelto
Un BOOL que indica el estado actual de inicialización MAPI, un valor de TRUE significa que MAPI se ha inicializado y está disponible para su uso, mientras que un valor de FALSE significa que MAPI no está inicializado y no está listo para usarse.

## <a name="remarks"></a>Comentarios
Esto se puede usar para determinar si MAPI está listo para usarse, por ejemplo, si la aplicación quería hacer algo solo si MAPI ya se ha inicializado, esto podría ser una comprobación útil en una tarea en segundo plano para evitar el costo de girar MAPI para el trabajo opcional.

## <a name="see-also"></a>Vea también

[IMAPIInitMonitor::Wait](imapiinitmonitor-wait.md)

[CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md)
