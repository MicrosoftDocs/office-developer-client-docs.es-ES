---
title: IMAPIFormShutdownForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.ShutdownForm
api_type:
- COM
ms.assetid: f1e2a526-40ad-4a93-908f-8ab9a65928a8
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 073a76766a296d86e7a23809921b832d494a8f1b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329480"
---
# <a name="imapiformshutdownform"></a>IMAPIForm::ShutdownForm

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cierra el formulario.
  
```cpp
HRESULT ShutdownForm(
  ULONG ulSaveOptions
);
```

## <a name="parameters"></a>Parameters

 _ulSaveOptions_
  
> a Un valor que controla cómo se guardan los datos en el formulario o si se guardan antes de cerrar el formulario. Puede establecer uno de los siguientes indicadores:
    
SAVEOPTS_NOSAVE 
  
> No se deben guardar los datos del formulario.
    
SAVEOPTS_PROMPTSAVE 
  
> Se debe pedir al usuario que guarde los datos modificados en el formulario.
    
SAVEOPTS_SAVEIFDIRTY 
  
> Los datos de formulario deben guardarse si han cambiado desde la última vez que guardó. Si no se muestra ninguna interfaz de usuario, el formulario puede cambiar opcionalmente a usar la funcionalidad de la opción SAVEOPTS_NOSAVE.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El formulario se ha cerrado.
    
E_UNEXPECTED 
  
> El formulario ya ha sido cerrado por una llamada anterior a **ShutdownForm**.
    
## <a name="remarks"></a>Comentarios

Los visores de formularios llaman al método **IMAPIForm:: ShutdownForm** para cerrar un formulario. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Realice las siguientes tareas en su implementación de **ShutdownForm**:
  
1. Compruebe que un visor todavía no ha llamado a **ShutdownForm**y devuelva E_UNEXPECTED si lo tiene. Aunque es poco probable, debe comprobar.
    
2. Llamar al método [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) del formulario para que el almacenamiento para el formulario y todas las estructuras de datos internas permanezca disponible hasta que finalice el procesamiento. 
    
3. DeTermine si hay cambios no guardados en los datos del formulario. Guarde los datos no guardados de acuerdo con el modo en que el parámetro _ulSaveOptions_ se establece llamando al método [IMAPIMessageSite:: SaveMessage](imapimessagesite-savemessage.md) del visor. 
    
4. Destruya la ventana de la interfaz de usuario del formulario.
    
5. Libere el mensaje del formulario y los objetos del sitio de mensajes llamando a sus métodos [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) . 
    
6. Notifique a todos los visores registrados del apagado pendiente llamando a sus métodos [IMAPIViewAdviseSink:: alshutdown](imapiviewadvisesink-onshutdown.md) . 
    
7. Llame al método [IMAPIViewContext:: SetAdviseSink](imapiviewcontext-setadvisesink.md) para cancelar el registro del formulario para la notificación; para ello, establezca el puntero notificar al receptor en **null**.
    
8. Llame a la función [MAPIFreeBuffer](mapifreebuffer.md) para liberar la memoria de las propiedades del formulario. 
    
9. Llame al método **IUnknown:: Release** del formulario, que coincide con la llamada **AddRef** realizada en el paso 2. 
    
10. Devuelve S_OK.
    
> [!NOTE]
> Una vez completadas estas acciones, los únicos métodos válidos en el objeto de formulario al que se puede llamar son los de la interfaz [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) . 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Cuando **ShutdownForm** devuelve, independientemente de si devuelve un error, libere el formulario llamando a su método **IUnknown:: Release** . Puede omitir sin problemas todos los errores devueltos por **ShutdownForm**.
  
## <a name="see-also"></a>Vea también



[IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md)
  
[IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md)
  
[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)

