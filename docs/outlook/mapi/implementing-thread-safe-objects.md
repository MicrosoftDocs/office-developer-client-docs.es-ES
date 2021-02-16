---
title: Implementación de Thread-Safe objetos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3c911694-b953-4d35-9a3a-22c17cfd79bc
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9160136542c7960bad0be2423872171b17d99fe3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413531"
---
# <a name="implementing-thread-safe-objects"></a>Implementación de Thread-Safe objetos

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Con objetos que se devuelven directamente desde llamadas a métodos de interfaz, es responsabilidad del proveedor garantizar la seguridad de subprocesos. Con los objetos de devolución de llamada, es responsabilidad de la aplicación cliente.
  
Un cliente puede implementar una devolución de llamada de notificación segura para subprocesos llamando a la utilidad MAPI [HrThisThreadAdviseSink](hrthisthreadadvisesink.md). **HrThisThreadAdviseSink** transforma un receptor de aviso no seguro para subprocesos en uno seguro para subprocesos. Para las devoluciones de llamada de progreso, no existe dicha utilidad. Un cliente puede elegir usar el objeto de progreso seguro para subprocesos MAPI o crear uno manualmente. 
  
Un objeto seguro para subprocesos también puede o no ser consciente de subprocesos. Un objeto para subprocesos mantiene un contexto independiente para cada subproceso que lo está usando. Los proveedores de servicios no son necesarios para admitir el reconocimiento de subprocesos en sus objetos seguros para subprocesos, aunque la compatibilidad con el reconocimiento de subprocesos puede ser útil en algunas situaciones. Dos tablas MAPI siempre proporcionan su propio contexto por definición. Una tabla usada en subprocesos diferentes no proporciona ni debe proporcionar un contexto único.
  
Un cliente puede elegir entre recibir notificaciones en el mismo subproceso que se usó para la llamada **MAPIInitialize,** en el mismo subproceso que se usó para la llamada **Advise** o en un subproceso independiente propiedad de MAPI. Para asegurarse de que las notificaciones lleguen al mismo subproceso que se usó para llamar a **MAPIInitialize,** un cliente llama a [MAPIInitialize](mapiinitialize.md) y pasa cero en el miembro **ulFlags** de la [estructura MAPIINIT_0](mapiinit_0.md) web. A continuación, las notificaciones se entregan durante el bucle de mensajes principal. 
  
Para recibir notificaciones en el subproceso propiedad de MAPI, un cliente llama a **MAPIInitialize** con el **miembro ulFlags** de la estructura **MAPIINIT_0** establecida en MAPI_MULTITHREAD_NOTIFICATIONS. La **llamada advise** se realiza con el objeto receptor de aviso del cliente en lugar de una versión ajustada. 
  
Para asegurarse de que las notificaciones lleguen al mismo subproceso que se usó para llamar a **Advise**, un cliente llama a [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) y pasa el receptor de avisos ajustado recién creado a **Advise** en lugar del receptor de avisos original. **Se puede llamar a MAPIInitialize** con cualquier valor de marca. 
  

