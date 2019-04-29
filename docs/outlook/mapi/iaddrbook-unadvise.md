---
title: IAddrBookUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Unadvise
api_type:
- COM
ms.assetid: e0db9e86-9528-43de-b8ba-a5af8b7bda4b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2988f1fc149bbfc2d724b62b12bd12ae4f4664a6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436156"
---
# <a name="iaddrbookunadvise"></a>IAddrBook::Unadvise

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cancela un registro de notificaciones previamente establecido para una entrada de la libreta de direcciones.
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Parameters

 _ulConnection_
  
> a Un número de conexión que representa el registro que se va a cancelar. El parámetro _ulConnection_ debe contener un valor devuelto por una llamada anterior al método [IAddrBook:: Advise](iaddrbook-advise.md) . 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El registro se canceló correctamente.
    
## <a name="remarks"></a>Comentarios

Los clientes llaman al método **Unadvise** para dejar de recibir notificaciones sobre los cambios realizados en una determinada entrada de la libreta de direcciones. Cuando se cancela un registro de notificación, el proveedor de la libreta de direcciones libera su puntero al receptor de notificaciones del autor de la llamada. Sin embargo, la liberación se puede producir durante la llamada a **Unadvise** o en algún momento posterior si hay otro subproceso en el proceso de llamada al método [IMAPIAdviseSink:: NotifyTo](imapiadvisesink-onnotify.md) . Cuando hay una notificación en curso, la liberación se retrasa hasta que se devuelva el método **BENOTIFY** . 
  
## <a name="see-also"></a>Ver también



[IAddrBook::Advise](iaddrbook-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

