---
title: 'IMAPIWaitResult : IUnknown'
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
ms.assetid: d7157f57-709d-4e53-973b-176954e2bb73
description: IMAPIWaitResult
Last modified: April 26, 2021
ms.openlocfilehash: 67a0fffdd0ab6d4989c12568f4d89808ba5adc7a
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062043"
---
# <a name="imapiwaitresult--iunknown"></a>IMAPIWaitResult : IUnknown
  
**Se aplica a**: Outlook 2013 | Outlook 2016 | Outlook 2019

Los consumidores de IMAPIInitMonitor usan esta interfaz para controlar dónde se produce la espera. Les permite crear el objeto en un subproceso y moverlo a otro subproceso para realizar la espera real.

## <a name="vtable-order"></a>Orden de Vtable

| function | description |
|:-----|:-----|
|[HRESULT IMAPIWaitResult::End()](imapiwaitresult-end.md)|Se llama para iniciar la espera de bloqueo en el subproceso al que se llama, que no necesita ser el mismo subproceso que llamó *a IMAPIInitMonitor::BeginWait*.|

| información rápida | result |
|:-----|:-----|
|Hereda de:  <br/> |IUnknown  <br/> |
|Implementado por:  <br/> |  OLMAPI32.DLL<br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIWaitResult  <br/> |

## <a name="see-also"></a>Vea también

[IMAPIInitMonitor](imapiinitmonitoriunknown.md)

[IMAPIInitMonitor::BeginWait](imapiinitmonitor-beginwait.md)

[IMAPIInitMonitor : IUnknown](imapiinitmonitoriunknown.md)

[CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md)
