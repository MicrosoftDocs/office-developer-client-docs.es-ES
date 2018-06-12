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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: b14529e987b85d1dcbe3689d4e852a9efd39a396
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818418"
---
# <a name="notifcallback"></a>NOTIFCALLBACK

  
  
**Se aplica a**: Outlook 
  
Define una función de devolución de llamada que llama MAPI para enviar una notificación de eventos. Sólo se puede usar esta función de devolución de llamada cuando se ajusta en un objeto de receptor advise creado mediante una llamada a la función [HrAllocAdviseSink](hrallocadvisesink.md) . 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Función definido implementada por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
|Llamado por una función definida:  <br/> |MAPI  <br/> |
   
```cpp
ULONG (STDAPICALLTYPE NOTIFCALLBACK)(
  LPVOID lpvContext,
  ULONG cNotification,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a>Sintaxis

 _lpvContext_
  
> [entrada] Puntero a un valor arbitrario se pasa a la función de devolución de llamada cuando llama a MAPI. Este valor puede representar una dirección de importancia a la aplicación de cliente o un proveedor de servicios. Normalmente, para el código de C++, el parámetro _lpvContext_ representa un puntero a un objeto de C++. 
    
 _cNotification_
  
> [entrada] Recuento de las notificaciones de eventos en la matriz indicada por el parámetro _lpNotifications_ . 
    
 _lpNotifications_
  
> [out] Puntero a la ubicación donde esta función escribe una matriz de estructuras de [notificación](notification.md) que contiene las notificaciones de eventos. 
    
## <a name="return-value"></a>Valor devuelto

El conjunto de valores devueltos válidos para el prototipo de función **NOTIFCALLBACK** depende de si se implementa la función por una aplicación de cliente o un proveedor de servicios. Los clientes siempre deben devolver S_OK. Proveedores pueden devolver S_OK o CALLBACK_DISCONTINUE. 
  
## <a name="remarks"></a>Notas

CALLBACK_DISCONTINUE es un valor devuelto válido para las funciones de devolución de llamada sincrónica solamente; solicita que MAPI detener inmediatamente el procesamiento de las devoluciones de llamada para esta notificación. Cuando se devuelve CALLBACK_DISCONTINUE, MAPI establece el parámetro _lpUlFlags_ a NOTIFY_CANCELED cuando se devuelve desde [IMAPISupport::Notify](imapisupport-notify.md). 
  
Las siguientes son limitaciones en lo que puede hacer una función de devolución de llamada sincrónica:
  
- No puede provocar otra notificación sincrónica que se genere.
    
- No puede mostrar una interfaz de usuario.
    
## <a name="see-also"></a>Ver también



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)

