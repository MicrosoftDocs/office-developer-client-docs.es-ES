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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390474"
---
# <a name="imapiformunadvise"></a>IMAPIForm::Unadvise

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Cancela un registro para las notificaciones con un visor de formulario que se ha establecido previamente mediante una llamada a [IMAPIForm::Advise](imapiform-advise.md).
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Parámetros

 _ulConnection_
  
> [entrada] Un número de conexión que identifica el registro de notificación que se cancelen.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se canceló el registro.
    
E_INVALIDARG 
  
> El número de conexión que se pasa en el parámetro _ulConnection_ no representan un registro válido. 
    
## <a name="remarks"></a>Comentarios

Visores de formulario llamar al método **IMAPIForm::Unadvise** para cancelar un registro de notificación que estableció por primera vez llamando al método **IMAPIForm::Advise** . 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Descartar el puntero que se mantiene a la vista del Visor de formulario de aviso receptor llamando a su método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) . Por lo general, se llama a **versión** durante la llamada **Unadvise** . Sin embargo, si otro subproceso está en el proceso de una llamada a uno de los métodos [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) para la vista de aviso receptor, retrasar la llamada **versión** hasta que el método **IMAPIViewAdviseSink** devuelve. 
  
## <a name="see-also"></a>Vea también



[IMAPIForm::Advise](imapiform-advise.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)

