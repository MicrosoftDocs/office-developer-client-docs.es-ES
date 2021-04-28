---
title: 'IMAPIInitMonitor : IUnknown'
manager: lindalu
26ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIInitMonitor
api_type:
- COM
ms.assetid: ad71ea65-394d-4be2-a9da-cd23099bc2cc
description: IMAPIInitMonitor
Last modified: April 26, 2021
ms.openlocfilehash: dd17d50b04755d9d9c2a10a9b02cd821faf1f7ec
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062049"
---
# <a name="imapiinitmonitor--iunknown"></a>IMAPIInitMonitor : IUnknown

**Se aplica a**: Outlook 2013 | Outlook 2016 | Outlook 2019

Hay ocasiones en las que una aplicación que consume MAPI puede querer saber cuándo se completa la inicialización. Por ejemplo, tiene varios subprocesos que podrían inicializar MAPI, o en respuesta a MAPI que se inicializa la aplicación le gustaría realizar algún trabajo, pero no quiere girar siempre la pila MAPI. El monitor de inicialización proporciona esta funcionalidad a través [de un objeto CreateMAPIInitializationMonitor.](createmapiinitializationmonitor.md)

| información rápida | result |
|:-----|:-----|
|Hereda de:  <br/> |IUnknown  <br/> |
|Implementado por:  <br/> | OLMAPI32.DLL <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIInitMonitor  <br/> |

## <a name="vtable-order"></a>Orden de Vtable

| function | description |
|:-----|:-----|
|[IMAPIInitMonitor::IsInitialized](imapiinitmonitor-isinitialized.md) <br/> |Devuelve el estado actual de inicialización MAPI.  <br/> |
|[IMAPIInitMonitor::Wait](imapiinitmonitor-wait.md) <br/> |Inicia una llamada BLOCKING en este subproceso, que devolverá cuando haya transcurrido el número especificado de milisegundos o cuando se haya inicializado MAPI.  INFINITE se puede usar para una espera infinita.  <br/> |
|[IMAPIInitMonitor::BeginWait](imapiinitmonitor-beginwait.md) <br/> |Inicie una espera para que transcurra la inicialización MAPI o el número especificado de milisegundos. Esto devuelve una interfaz IMAPIWaitResult que debería tener "End" llamado para comenzar la espera.  Esto permite al autor de la llamada controlar qué subproceso está bloqueado mientras estamos esperando. <br/> |
