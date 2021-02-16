---
title: HrThisThreadAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrThisThreadAdviseSink
api_type:
- COM
ms.assetid: 12c07302-472f-4e4f-8087-1bdf0dc09a5a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0fb867d662064dfe5ff7759dba4b36a4635a2914
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427733"
---
# <a name="hrthisthreadadvisesink"></a>HrThisThreadAdviseSink

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea un receptor de avisos que encapsula un receptor de avisos existente para la seguridad de subprocesos. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
   
```cpp
HrThisThreadAdviseSink(
  LPMAPIADVISESINK lpAdviseSink,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a>Parámetros

 _lpAdviseSink_
  
> [entrada] Puntero al receptor de aviso que se va a ajustar. 
    
 _lppAdviseSink_
  
> [salida] Puntero a un puntero a un nuevo receptor de avisos que encapsula el receptor de avisos al que apunta el parámetro _lpAdviseSink._ 
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El propósito del contenedor es asegurarse de que se llama a la notificación en el mismo subproceso que llamó a la función **HrThisThreadAdviseSink.** Esta función se usa para proteger las devoluciones de llamada de notificación que deben ejecutarse en un subproceso determinado. 
  
Las aplicaciones cliente deben usar **HrThisThreadAdviseSink** para restringir cuándo se generan las notificaciones, es decir, cuando se realizan llamadas al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) del objeto receptor de aviso pasado por el cliente en una llamada **advise** anterior. Si se permite que las notificaciones se generen de forma arbitraria, una implementación de notificación podría forzar a un cliente a una operación multiproceso cuando no fuera apropiado. Por ejemplo, un cliente puede usar una biblioteca, como una de las bibliotecas de clase de Microsoft Foundation, que no admite llamadas multiproceso. La notificación en un subproceso diferente haría que un cliente de este tipo sea difícil de probar y propensa a errores. 
  
 **HrThisThreadAdviseSink** se asegura de que las llamadas **OnNotify** se produzcan solo en los momentos adecuados: 
  
- Durante el procesamiento de una llamada a cualquier método MAPI. 
    
- Durante el procesamiento de mensajes de Windows. 
    
Cuando se implementa **HrThisThreadAdviseSink,** cualquier llamada al nuevo método **OnNotify** del receptor de avisos en cualquier subproceso hace que el método de notificación original se ejecute en el subproceso en el que se llamó a **HrThisThreadAdviseSink.** 
  
Para obtener más información acerca de los receptores de notificaciones y avisos, vea [notificación de eventos](event-notification-in-mapi.md) en MAPI e implementación de un objeto receptor de [avisos](implementing-an-advise-sink-object.md). 
  

