---
title: IMsgStoreUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.Unadvise
api_type:
- COM
ms.assetid: 1394039b-d509-49a5-8421-b7362d906879
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f85b662b7fe710c66a2e69dd3cd3db22e3283ddb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309726"
---
# <a name="imsgstoreunadvise"></a>IMsgStore::Unadvise

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cancela el envío de notificaciones configuradas anteriormente con una llamada al [método IMsgStore::Advise.](imsgstore-advise.md) 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Parameters

 _ulConnection_
  
> [in] Número de conexión asociado a un registro de notificación activo. El valor de _ulConnection_ debe haber sido devuelto por una llamada anterior al **método IMsgStore::Advise.** 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El registro se canceló correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IMsgStore::Unadvise** cancela un registro para la notificación. **Unadvise** libera su puntero al receptor de avisos del autor de la llamada, que recibió en la **llamada Advise** usada para el registro. 
  
Por lo general, **Unadvise** llama al método [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) del receptor de aviso durante la **llamada Unadvise.** Sin embargo, si otro subproceso está en proceso de llamar al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) del receptor de aviso, la llamada **Release** se retrasa hasta que el método **OnNotify** devuelve. 
  
## <a name="see-also"></a>Vea también



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMsgStore::Advise](imsgstore-advise.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

