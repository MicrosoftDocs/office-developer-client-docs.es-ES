---
title: HrDispatchNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDispatchNotifications
api_type:
- COM
ms.assetid: 42ec4266-67b9-416e-8b9b-163c95011626
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 28afa338b37e747ed441a8767981b7e63808e741
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817049"
---
# <a name="hrdispatchnotifications"></a>HrDispatchNotifications

  
  
**Hace referencia a**: Outlook 
  
Envío de fuerza de todas las notificaciones en la cola. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
HRESULT HrDispatchNotifications(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Reservado; debe ser cero. 
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> Todas las notificaciones en cola se ha distribuido.
    
MAPI_E_USER_CANCEL
  
> Se ha recibido WM_QUIT, mensaje WM_QUERYENDSESSION o WM_ENDSESSION.
    
MAPI_E_NOT_INITIALIZED
  
> MAPI no se ha inicializado.
    
## <a name="remarks"></a>Comentarios

La función **HrDispatchNotifications** hace que MAPI enviar todas las notificaciones que están actualmente en cola en el motor de notificación de MAPI sin tener que esperar un envío de mensaje. Esto puede tener un efecto beneficioso en el uso de memoria. Para obtener más información, vea [forzar una notificación](forcing-a-notification.md). 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Algunas aplicaciones de esperen un mensaje de notificación en un bucle de tiempo de espera mediante las funciones de [DispatchMessage](http://msdn.microsoft.com/en-us/library/ms644934.aspx) y Windows [PeekMessage](http://msdn.microsoft.com/en-us/library/ms644943.aspx) . En todos los pero las plataformas más rápidas, dichas aplicaciones podrían experimentar un rendimiento deficiente o incluso bloqueo de notificaciones. Uso de **HrDispatchNotifications** no sólo reduce el código pero mejora el rendimiento. 
  

