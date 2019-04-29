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
  
Crea un receptor de notificaciones que encapsula un receptor de notificaciones existente para la seguridad de subprocesos. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
   
```cpp
HrThisThreadAdviseSink(
  LPMAPIADVISESINK lpAdviseSink,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a>Parameters

 _lpAdviseSink_
  
> a Puntero al receptor de notificaciones que se va a ajustar. 
    
 _lppAdviseSink_
  
> contempla Puntero a un puntero a un nuevo receptor de notificaciones que encapsula el receptor de notificaciones al que apunta el parámetro _lpAdviseSink_ . 
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El propósito del contenedor es asegurarse de que se llama a la notificación en el mismo subproceso que llamó a la función **HrThisThreadAdviseSink** . Esta función se usa para proteger las devoluciones de llamada de notificaciones que se deben ejecutar en un subproceso en particular. 
  
Las aplicaciones cliente deben usar **HrThisThreadAdviseSink** para restringir Cuándo se generan las notificaciones, es decir, cuando se realizan llamadas al método [IMAPIAdviseSink:: método Notify](imapiadvisesink-onnotify.md) del objeto de notificación de notificaciones que pasa el cliente en una **notificación anterior **llamar. Si se permite generar arbitrariamente las notificaciones, una implementación de notificaciones puede forzar a un cliente en una operación multiproceso cuando no sería adecuada. Por ejemplo, un cliente podría usar una biblioteca, como una de las bibliotecas de Microsoft Foundation Class, que no es compatible con llamadas multiproceso. La notificación en un subproceso diferente haría que un cliente de este tipo sería difícil de probar y propenso a errores. 
  
 **HrThisThreadAdviseSink** asegura que las llamadas a **Notify** solo se producen en las siguientes horas adecuadas: 
  
- Durante el procesamiento de una llamada a cualquier método de MAPI. 
    
- Durante el procesamiento de los mensajes de Windows. 
    
Cuando se implementa **HrThisThreadAdviseSink** , cualquier llamada al método de **Notify** del receptor de notificación nuevo en cualquier subproceso causa el método de notificación original que se ejecuta en el subproceso en el que se llamó a **HrThisThreadAdviseSink** . 
  
Para obtener más información acerca de los receptores de notificaciones y avisos, vea [notificación de eventos en MAPI](event-notification-in-mapi.md) e [implementación de un objeto](implementing-an-advise-sink-object.md)de notificación de aviso. 
  

