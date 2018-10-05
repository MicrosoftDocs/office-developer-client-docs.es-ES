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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387638"
---
# <a name="imslogonunadvise"></a>IMSLogon::Unadvise

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Quita el registro de un objeto de notificación de cambios del almacén de mensajes ha establecido previamente mediante una llamada al método [IMSLogon::Advise](imslogon-advise.md) . 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Parámetros

 _ulConnection_
  
> [entrada] El número de la conexión de registro devuelto por una llamada a **IMSLogon::Advise**.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Almacén de mensajes implementan los proveedores el método **IMSLogon::Unadvise** para liberar el puntero al objeto receptor advise pasado en el parámetro _lpAdviseSink_ en la llamada anterior a **IMSLogon::Advise**, con lo que se cancela una notificación en el registro. Como parte de descartar el puntero al objeto receptor advise, se llama al método del objeto [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) . Por lo general, se llama a **versión** durante la llamada **Unadvise** . Sin embargo, si otro subproceso está en proceso de llamar al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para el objeto de receptor advise, la llamada de la **versión** se retrasa hasta que el método **OnNotify** devuelve. 
  
## <a name="see-also"></a>Vea también



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMSLogon::Advise](imslogon-advise.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

