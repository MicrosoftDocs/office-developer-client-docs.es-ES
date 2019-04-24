---
title: NOTIFCALLBACK
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFCALLBACK
api_type:
- COM
ms.assetid: 416008b4-13aa-4387-8c12-f8f2ca252391
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0e2a1a582894e082722d73422fc8bafe34c4230c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334478"
---
# <a name="notifcallback"></a>NOTIFCALLBACK

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Define una función de devolución de llamada a la que MAPI llama para enviar una notificación de evento. Esta función de devolución de llamada solo se puede usar cuando se incluye en un objeto Sink de notificaciones creado llamando a la función [HrAllocAdviseSink](hrallocadvisesink.md) . 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
|Función definida implementada por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
|Función definida llamada por:  <br/> |MAPI  <br/> |
   
```cpp
ULONG (STDAPICALLTYPE NOTIFCALLBACK)(
  LPVOID lpvContext,
  ULONG cNotification,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a>Parameters

 _lpvContext_
  
> a Puntero a un valor arbitrario que se pasa a la función de devolución de llamada cuando MAPI la llama. Este valor puede representar una dirección de importancia para la aplicación cliente o el proveedor de servicios. Normalmente, para código de C++, el parámetro _lpvContext_ representa un puntero a un objeto de c++. 
    
 _cNotification_
  
> a Número de notificaciones de eventos en la matriz indicada por el parámetro _lpNotifications_ . 
    
 _lpNotifications_
  
> contempla Puntero a la ubicación en la que esta función escribe una matriz de estructuras de [notificación](notification.md) que contiene las notificaciones de eventos. 
    
## <a name="return-value"></a>Valor devuelto

El conjunto de valores de devolución válidos para el prototipo de función **NOTIFCALLBACK** depende de si la función la implementa una aplicación cliente o un proveedor de servicios. Los clientes siempre deben devolver S_OK. Los proveedores pueden devolver S_OK o CALLBACK_DISCONTINUE. 
  
## <a name="remarks"></a>Comentarios

CALLBACK_DISCONTINUE es un valor devuelto válido solo para las funciones de devolución de llamada sincrónica; solicita que MAPI deje inmediatamente de procesar las devoluciones de llamada de esta notificación. Cuando se devuelve CALLBACK_DISCONTINUE, MAPI establece el parámetro _lpUlFlags_ en NOTIFY_CANCELED cuando devuelve de [IMAPISupport:: Notify](imapisupport-notify.md). 
  
A continuación se indican las limitaciones que puede realizar una función de devolución de llamada sincrónica:
  
- No puede provocar que se genere otra notificación sincrónica.
    
- No puede mostrar una interfaz de usuario.
    
## <a name="see-also"></a>Vea también



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)

