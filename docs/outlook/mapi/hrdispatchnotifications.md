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
ms.openlocfilehash: f4af3f2fd094942c48e02849c60f3e46acb1a5f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348100"
---
# <a name="hrdispatchnotifications"></a>HrDispatchNotifications

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Fuerza el envío de todas las notificaciones en cola. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
HRESULT HrDispatchNotifications(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [entrada] Reservado; debe ser cero. 
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> Se han enviado todas las notificaciones en cola.
    
MAPI_E_USER_CANCEL
  
> WM_QUIT, WM_QUERYENDSESSION o WM_ENDSESSION se recibió.
    
MAPI_E_NOT_INITIALIZED
  
> MAPI no se inicializó.
    
## <a name="remarks"></a>Comentarios

La **función HrDispatchNotifications** hace que MAPI envíe todas las notificaciones que están actualmente en cola en el motor de notificaciones MAPI sin esperar a que se envíe un mensaje. Esto puede tener un efecto beneficioso en el uso de la memoria. Para obtener más información, [vea Forzar una notificación](forcing-a-notification.md). 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Algunas aplicaciones esperan un mensaje de notificación en un bucle de tiempo de espera mediante las Windows [PeekMessage](https://msdn.microsoft.com/library/ms644943.aspx) y [DispatchMessage.](https://msdn.microsoft.com/library/ms644934.aspx) En todas las plataformas, menos en las más rápidas, estas aplicaciones pueden experimentar un rendimiento deficiente o incluso bloquear las notificaciones. El **uso de HrDispatchNotifications** no solo reduce el código, sino que mejora el rendimiento. 
  

