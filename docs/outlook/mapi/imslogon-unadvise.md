---
title: IMSLogonUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Unadvise
api_type:
- COM
ms.assetid: 440d61c4-b69a-4010-a22b-0c9c5c376fbc
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9172d4956e78ac31cd15d69e70d05c127a474ca5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317279"
---
# <a name="imslogonunadvise"></a>IMSLogon::Unadvise

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Quita el registro de un objeto para notificaciones de cambios del almacén de mensajes previamente establecidos mediante una llamada al método [IMSLogon:: Advise](imslogon-advise.md) . 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Parameters

 _ulConnection_
  
> a El número de la conexión de registro devuelta por una llamada a **IMSLogon:: Advise**.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Los proveedores de almacenamiento de mensajes implementan el método **IMSLogon:: Unadvise** para liberar el puntero al objeto del receptor de notificaciones que se pasa en el parámetro _lpAdviseSink_ en la llamada anterior a **IMSLogon:: Advise**, con lo que se cancela una notificación. registro. Como parte de la descartar el puntero al objeto de receptor de notificaciones, se llama al método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) del objeto. Por lo general, se llama a **Release** durante la llamada a **Unadvise** . Sin embargo, si hay otro subproceso que llama al método [IMAPIAdviseSink:: método Notify](imapiadvisesink-onnotify.md) para el objeto Asesor de notificaciones, la llamada de **liberación** se retrasa hasta que se devuelva el método **BENOTIFY** . 
  
## <a name="see-also"></a>Vea también



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMSLogon::Advise](imslogon-advise.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

