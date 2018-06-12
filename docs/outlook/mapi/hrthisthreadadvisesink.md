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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 744d9a7588bff89e9d306e516a24da2db3038d4d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817098"
---
# <a name="hrthisthreadadvisesink"></a>HrThisThreadAdviseSink

  
  
**Se aplica a**: Outlook 
  
Crea un receptor de notificaciones que se ajusta un receptor de notificaciones existentes seguridad para subprocesos. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
   
```cpp
HrThisThreadAdviseSink(
  LPMAPIADVISESINK lpAdviseSink,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a>Sintaxis

 _lpAdviseSink_
  
> [entrada] Puntero para el receptor de notificaciones que se ajustarán. 
    
 _lppAdviseSink_
  
> [out] Puntero a un puntero a un nuevo receptor de notificaciones que se ajusta el receptor de notificaciones que señala el parámetro _lpAdviseSink_ . 
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Observaciones

El propósito del contenedor es asegurarse de que la notificación se denomina en el mismo subproceso que llamó a la función **HrThisThreadAdviseSink** . Esta función se usa para proteger las devoluciones de llamada de notificación que se deben ejecutar en un subproceso concreto. 
  
Aplicaciones cliente deben usar **HrThisThreadAdviseSink** para restringir cuando se generan notificaciones, es decir, cuando se realizan llamadas al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) del objeto receptor advise que se pasan por el cliente en un **anterior Advise **de llamadas. Si se permiten las notificaciones que se genere arbitrariamente, una implementación de notificación podría forzar a un cliente en funcionamiento multiproceso cuando que no sería adecuado. Por ejemplo, un cliente puede usar una biblioteca, como una de las bibliotecas de clases de Microsoft Foundation, que no admite llamadas multiproceso. Notificación en un subproceso diferente haría que este tipo de cliente difícil probar y propensas a errores. 
  
 **HrThisThreadAdviseSink** se asegura de que las llamadas de **OnNotify** se producen sólo en estos momentos adecuados: 
  
- Durante el procesamiento de una llamada a cualquier método de MAPI. 
    
- Durante el procesamiento de los mensajes de Windows. 
    
Cuando se implementa **HrThisThreadAdviseSink** , las llamadas al método de **OnNotify** del receptor de notificaciones nuevas en cualquier subproceso que el método de notificación original que se debe ejecutar en el subproceso en el que se llamó a **HrThisThreadAdviseSink** . 
  
Para obtener más información acerca de la notificación y receptores de notificaciones, vea la [Notificación de eventos en MAPI](event-notification-in-mapi.md) y la [implementación de un objeto de receptor de aviso](implementing-an-advise-sink-object.md). 
  

