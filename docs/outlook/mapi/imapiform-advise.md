---
title: IMAPIFormAdvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.Advise
api_type:
- COM
ms.assetid: 961318d6-bebe-4f4b-98ff-921cafc68d24
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b5347205e10b44d62a7e11cbe2f4179970f1bd64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817252"
---
# <a name="imapiformadvise"></a>IMAPIForm::Advise

  
  
**Hace referencia a**: Outlook 
  
Registra un visor de formulario para las notificaciones sobre los eventos que afectan a la forma.
  
```cpp
HRESULT Advise(
  LPMAPIVIEWADVISESINK pAdvise,
  ULONG FAR * pulConnection
);
```

## <a name="parameters"></a>Parámetros

 _pAdvise_
  
> [entrada] Un puntero a una vista de aviso objeto receptor para recibir las notificaciones posteriores. 
    
 _pulConnection_
  
> [out] Un puntero a un valor distinto de cero que representa un registro de la notificación realizada correctamente.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El registro se realizó correctamente.
    
E_OUTOFMEMORY 
  
> El registro no tuvo éxito debido a memoria insuficiente.
    
## <a name="remarks"></a>Comentarios

Visores de formulario llame al método de **IMAPIForm::Advise** de un formulario para registrarse para la notificación cuando se producen cambios al formulario. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Mantener una copia de la vista de aviso puntero receptor pasa en el parámetro _pAdvise_ de forma que puede usar para llamar al método apropiado de [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) cuando se produce un evento. Método de [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) del receptor para conservar el puntero hasta que se cancele el registro de la notificación de aviso de llamada de la vista. Establecer el contenido del parámetro _pulConnection_ a un número distinto de cero. 
  
Muchas formas implementan un objeto auxiliar para controlar el registro y la notificación posterior de eventos. 
  
Para obtener más información sobre el proceso de notificación en general, vea [Notificación de evento de MAPI](event-notification-in-mapi.md). 
  
Para obtener más información acerca de la notificación y formularios, vea [Enviar y recibir notificaciones de formulario](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Vea también



[IMAPIForm::Unadvise](imapiform-unadvise.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[Notificación de eventos de MAPI](event-notification-in-mapi.md)
  
[Enviar y recibir notificaciones de formulario](sending-and-receiving-form-notifications.md)

