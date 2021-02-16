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
ms.openlocfilehash: 2ed8bace97dee3842243ed835769e80e8aaf6b03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329487"
---
# <a name="imapiformadvise"></a>IMAPIForm::Advise

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Registra un visor de formulario para notificaciones sobre eventos que afectan al formulario.
  
```cpp
HRESULT Advise(
  LPMAPIVIEWADVISESINK pAdvise,
  ULONG FAR * pulConnection
);
```

## <a name="parameters"></a>Parámetros

 _pAdvise_
  
> [entrada] Un puntero a un objeto receptor de aviso de vista para recibir las notificaciones posteriores. 
    
 _pulConnection_
  
> [salida] Puntero a un valor distinto de cero que representa un registro de notificación correcto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El registro se ha realizado correctamente.
    
E_OUTOFMEMORY 
  
> El registro no se ha hecho correctamente debido a la memoria insuficiente.
    
## <a name="remarks"></a>Comentarios

Los visores de formularios llaman al método **IMAPIForm::Advise** de un formulario para registrarse para recibir notificaciones cuando se producen cambios en el formulario. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Mantenga una copia del puntero receptor de aviso de vista pasado en el parámetro  _pAdvise_ para que pueda usarlo para llamar al método [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) adecuado cuando se produzca un evento. Llama al método [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) del receptor del aviso de vista para conservar el puntero hasta que se cancele el registro de notificaciones. Establezca el contenido del  _parámetro pulConnection_ en un número distinto de cero. 
  
Muchos formularios implementan un objeto auxiliar para controlar el registro y la notificación subsiguiente de eventos. 
  
Para obtener más información sobre el proceso de notificación en general, vea [Notificación de eventos en MAPI](event-notification-in-mapi.md). 
  
Para obtener más información acerca de las notificaciones y los [formularios, vea Enviar y recibir notificaciones de formularios.](sending-and-receiving-form-notifications.md)
  
## <a name="see-also"></a>Consulte también



[IMAPIForm::Unadvise](imapiform-unadvise.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[Notificación de eventos en MAPI](event-notification-in-mapi.md)
  
[Enviar y recibir notificaciones de formularios](sending-and-receiving-form-notifications.md)

