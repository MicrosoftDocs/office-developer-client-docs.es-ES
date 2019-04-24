---
title: IMAPISessionUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Unadvise
api_type:
- COM
ms.assetid: 5e608cb0-808d-4418-8521-71dcbce8cdff
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 98a5faca00f5877eb10110406875b46a69244d94
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335707"
---
# <a name="imapisessionunadvise"></a>IMAPISession::Unadvise

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cancela el envío de notificaciones previamente configurado con una llamada al método [IMAPISession:: Advise](imapisession-advise.md) . 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Parameters

 _ulConnection_
  
> a Un número de conexión asociado con un registro de notificación activo. El valor de _ulConnection_ debe haber sido devuelto por una llamada anterior a **IMAPISession:: Advise**.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El registro se canceló correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISession:: Unadvise** cancela un registro para la notificación. No **aconseja** liberar su puntero al receptor de notificaciones del autor de la llamada, que recibió en la llamada de **aviso** utilizada para el registro. 
  
Generalmente, **Unadvise** llama al método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) del receptor de notificaciones durante **** la llamada a Unadvise. Sin embargo, si hay otro subproceso en proceso de llamar al método [IMAPIAdviseSink:: NotifyTo](imapiadvisesink-onnotify.md) del receptor de notificación, la llamada de **liberación** se retrasa hasta que se devuelva el método **BENOTIFY** . 
  
## <a name="see-also"></a>Vea también



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISession::Advise](imapisession-advise.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)

