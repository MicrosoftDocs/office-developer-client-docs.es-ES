---
title: IMAPIFormUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.Unadvise
api_type:
- COM
ms.assetid: fdda45e2-631d-404c-8af4-bce68df0968b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 770ceb7af98f5271baad65043e013feb353d231a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329473"
---
# <a name="imapiformunadvise"></a>IMAPIForm::Unadvise

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cancela un registro de notificaciones con un visor de formularios establecido previamente mediante una llamada a [IMAPIForm:: Advise](imapiform-advise.md).
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Parameters

 _ulConnection_
  
> a Un número de conexión que identifica el registro de notificaciones que se va a cancelar.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se canceló el registro.
    
E_INVALIDARG 
  
> El número de conexión pasado en el parámetro _ulConnection_ no representa un registro válido. 
    
## <a name="remarks"></a>Comentarios

Los visores de formularios llaman al método **IMAPIForm:: Unadvise** para cancelar un registro para la notificación que se estableció por primera vez mediante una llamada al método **IMAPIForm:: Advise** . 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

DesCartar el puntero que está reteniendo al receptor de la vista de notificar del formulario del visor llamando a su método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) . Por lo general, se llama a **Release** durante la llamada a **Unadvise** . Sin embargo, si hay otro subproceso que llama a uno de los métodos [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) para el receptor View Advise, retrase la llamada a **Release** hasta que se devuelva el método **IMAPIViewAdviseSink** . 
  
## <a name="see-also"></a>Vea también



[IMAPIForm::Advise](imapiform-advise.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)

