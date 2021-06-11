---
title: CreateMAPIInitializationMonitor
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIWAITRESULT
api_type:
- COM
ms.assetid: 32a9758a-395d-4526-9610-3e4eeaf78c96
description: Monitor de inicialización MAPI
Last modified: April 26, 2021
ms.openlocfilehash: da7c48a6b026ccd4cbe4cbac192a1a0760202835
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062056"
---
# <a name="createmapiinitializationmonitor"></a>CreateMAPIInitializationMonitor

**Se aplica a**: Outlook 2016 | Outlook 2019
  
## <a name="mapi-initialization-monitor"></a>Monitor de inicialización MAPI

Hay ocasiones en las que una aplicación que consume MAPI puede querer saber cuándo se completa la inicialización. Por ejemplo, tiene varios subprocesos que podrían inicializar MAPI, o en respuesta a MAPI que se inicializa la aplicación le gustaría realizar algún trabajo, pero no quiere girar siempre la pila MAPI. El monitor de inicialización proporciona esta funcionalidad a través de una función (exportada desde OLMAPI32.DLL) y un par de interfaces sencillas que se describen a continuación.

Este es el punto de entrada exportado desde OLMAPI32.DLL esto permite al autor de la llamada recuperar una interfaz para consultar el estado de inicialización actual, configurar una devolución de llamada para la finalización de inicialización o bloquear el subproceso actual hasta que se haya completado. El objeto devuelto de esta API es reutilizable y seguro para subprocesos y se puede invocar desde cualquier subproceso, no solo desde el subproceso que la recuperó. Además, a diferencia de otros objetos expuestos desde MAPI, este objeto es válido siempre que se cargue la DLL, se puede volver a usar en las sesiones de inicialización y se puede consumir antes o después de llamar a MAPIInitialize. Devuelve éxito o error a través de un HRESULT estándar COM y asigna un parámetro de salida a una instancia de IMAPIInitMonitor.

```cpp
HRESULT CreateMAPIInitializationMonitor(IMAPIInitMonitor** ppInitMonitor); 
```
#### <a name="hresult-stdapicalltype-createmapiinitializationmonitorimapiinitmonitor-ppinitmonitor"></a>HRESULT STDAPICALLTYPE CreateMapiInitializationMonitor(IMAPIInitMonitor ppInitMonitor)

Este punto de entrada exportado desde OLMAPI32.DLL permite al autor de la llamada recuperar una interfaz para consultar el estado de inicialización actual, configurar una devolución de llamada para la finalización de la inicialización o bloquear el subproceso actual hasta que se haya completado. El objeto devuelto de esta API es reutilizable y seguro para subprocesos y se puede invocar desde cualquier subproceso, no solo desde el subproceso que la recuperó. Además, a diferencia de otros objetos expuestos desde MAPI, este objeto es válido siempre que se cargue la DLL, se puede volver a usar en las sesiones de inicialización y se puede consumir antes o después de llamar a MAPIInitialize. Devuelve éxito o error a través de un HRESULT estándar COM y asigna un parámetro de salida a una instancia de IMAPIInitMonitor.
  
## <a name="quick-info"></a>Información rápida

| identificador | result |
|:-----|:-----|
|Exportada por:  <br/> |olmapi32.dll  <br/> |
|Llamado por:  <br/> |Cliente  <br/> |
|Implementado por:  <br/> |Outlook  <br/> |

## <a name="parameters"></a>Parameters
  
 _ppInitMonitor_
> [salida] Puntero para recibir la instancia recién creada del monitor de inicialización MAPI.
  
## <a name="return-values"></a>Valores devueltos

S_OK
> Se creó correctamente una nueva instancia del monitor de inicialización.

E_OUTOFMEMORY
> No había suficiente memoria para crear un nuevo objeto.

## <a name="see-also"></a>Vea también
[IMAPIInitMonitor](imapiinitmonitoriunknown.md)

[IMAPIWaitResult](imapiwaitresultiunknown.md)
