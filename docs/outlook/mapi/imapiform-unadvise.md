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
  
Cancela un registro de notificaciones con un visor de formulario establecido anteriormente llamando a [IMAPIForm::Advise](imapiform-advise.md).
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Parámetros

 _ulConnection_
  
> [entrada] Número de conexión que identifica el registro de notificación que se va a cancelar.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se canceló el registro.
    
E_INVALIDARG 
  
> El número de conexión pasado en  _el parámetro ulConnection_ no representa un registro válido. 
    
## <a name="remarks"></a>Comentarios

Los visores de formularios llaman al método **IMAPIForm::Unadvise** para cancelar un registro de notificación que establecieron por primera vez llamando al método **IMAPIForm::Advise.** 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Descarte el puntero que está manteniendo en el receptor de avisos de vista del visor de formularios llamando a su [método IUnknown::Release.](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) Por lo general, se llama a **Release** durante la **llamada Unadvise.** Sin embargo, si otro subproceso está en proceso de llamar a uno de los métodos [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) para el receptor de aviso de vista, retrase la llamada **release** hasta que el método **IMAPIViewAdviseSink** vuelva. 
  
## <a name="see-also"></a>Consulte también



[IMAPIForm::Advise](imapiform-advise.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)

