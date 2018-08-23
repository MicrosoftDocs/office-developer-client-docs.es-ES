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
ms.openlocfilehash: e06f78317a1e98d47a37cb7059042b254567fe8b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573687"
---
# <a name="iaddrbookunadvise"></a>IAddrBook::Unadvise

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cancela un registro de notificación establecido anteriormente para una entrada de la libreta de direcciones.
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Parámetros

 _ulConnection_
  
> [entrada] Un número de conexión que representa el registro que se cancelen. El parámetro _ulConnection_ debe contener un valor devuelto por una llamada anterior al método [IAddrBook::Advise](iaddrbook-advise.md) . 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El registro se canceló correctamente.
    
## <a name="remarks"></a>Comentarios

Los clientes de llaman al método **Unadvise** para dejar de recibir notificaciones sobre los cambios realizados en una entrada de la libreta de direcciones determinada. Cuando se cancela un registro de la notificación, las versiones de proveedor de la libreta de direcciones su puntero al autor de la llamada del aviso receptor. Sin embargo, la versión puede producirse durante la llamada **Unadvise** o en algún momento posterior, si es otro subproceso en el proceso de llamar al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) . Cuando una notificación está en progreso, la versión se retrasa hasta que el método **OnNotify** devuelve. 
  
## <a name="see-also"></a>Recursos adicionales



[IAddrBook::Advise](iaddrbook-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

