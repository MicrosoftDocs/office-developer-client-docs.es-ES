---
title: Implementar objetos seguros para subprocesos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3c911694-b953-4d35-9a3a-22c17cfd79bc
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 8c8c89f3626d54f04896ad54de5d7e480dd9b568
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817722"
---
# <a name="implementing-thread-safe-objects"></a>Implementar objetos seguros para subprocesos

  
  
**Hace referencia a**: Outlook 
  
Con los objetos que se devuelven desde la interfaz llamadas al método directamente, es responsabilidad del proveedor para garantizar la seguridad para subprocesos. Con los objetos de devolución de llamada, es responsabilidad de la aplicación cliente.
  
Un cliente puede implementar una devolución de llamada de notificación de subprocesos mediante una llamada a la utilidad MAPI [HrThisThreadAdviseSink](hrthisthreadadvisesink.md). **HrThisThreadAdviseSink** transforma un receptor de notificaciones de que no son seguros para subprocesos en uno de los subprocesos. Para realizar devoluciones de llamadas de progreso, no hay ningún dicha utilidad. Un cliente puede optar por usar el objeto de progreso de subprocesos MAPI o crear uno de forma manual. 
  
Un objeto de seguros para subprocesos podría o no también pueden tener en cuenta de subproceso. Un objeto de subproceso mantiene un contexto independiente para cada subproceso que lo está utilizando. Proveedores de servicios no necesarios para admitir el reconocimiento de subproceso en sus objetos seguros para subprocesos, aunque apoyo del conocimiento de subproceso puede ser útil en algunas situaciones. Dos tablas MAPI siempre proporcionan su propio contexto por definición. Una tabla que se usan en distintos subprocesos no lo hace y no debe proporcionar contexto único.
  
Un cliente puede elegir entre recibir notificaciones en el mismo subproceso que se usó para la **MAPIInitialize** llamar, en el mismo subproceso que se usó para la llamada **Advise** , o en un subproceso separado que pertenecen a MAPI. Para asegurarse de que reciben notificaciones en el mismo subproceso que se usó para llamar **MAPIInitialize**, un cliente llama [MAPIInitialize](mapiinitialize.md) y pasa cero en el miembro **ulFlags** de la estructura [MAPIINIT_0](mapiinit_0.md) . A continuación, se entregan las notificaciones durante el bucle de mensajes principal. 
  
Para recibir notificaciones en el subproceso de propiedad MAPI, un cliente llama **MAPIInitialize** con el miembro **ulFlags** de la estructura **MAPIINIT_0** establecido en MAPI_MULTITHREAD_NOTIFICATIONS. Se realiza la llamada **Advise** con el cliente de aviso objeto receptor en lugar de una versión ajustada. 
  
Para asegurarse de que reciben notificaciones en el mismo subproceso que se usó para llamar **Advise**, un cliente llama a [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) y pasa ajustada recién creada de aviso receptor para **Advise** en lugar de la original receptor de notificaciones. **MAPIInitialize** puede llamarse con cualquier valor de marca. 
  

