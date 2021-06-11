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
  
> [in] Valor que controla cómo o si los datos del formulario se guardan antes de cerrar el formulario. Puede establecer uno de los siguientes indicadores:
    
SAVEOPTS_NOSAVE 
  
> Los datos del formulario no deben guardarse.
    
SAVEOPTS_PROMPTSAVE 
  
> Se debe pedir al usuario que guarde los datos modificados en el formulario.
    
SAVEOPTS_SAVEIFDIRTY 
  
> Los datos del formulario deben guardarse si han cambiado desde el último guardado. Si no se muestra ninguna interfaz de usuario, el formulario puede cambiar opcionalmente al uso de la funcionalidad para la SAVEOPTS_NOSAVE usuario.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El formulario se ha cerrado.
    
E_UNEXPECTED 
  
> El formulario ya estaba cerrado mediante una llamada anterior a **ShutdownForm**.
    
## <a name="remarks"></a>Comentarios

Los visores de formularios llaman **al método IMAPIForm::ShutdownForm** para cerrar un formulario. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Realice las siguientes tareas en la implementación de **ShutdownForm**:
  
1. Compruebe que un visor no haya llamado **a ShutdownForm** y devuelva E_UNEXPECTED si lo ha hecho. Aunque esto es poco probable, debe comprobarlo.
    
2. Llama al método [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) del formulario para que el almacenamiento del formulario y las estructuras de datos internas permanezcan disponibles hasta que finalice el procesamiento. 
    
3. Determine si hay cambios no guardados en los datos del formulario. Guarde los datos sin guardar según cómo se establece el parámetro  _ulSaveOptions_ llamando al método [IMAPIMessageSite::SaveMessage del](imapimessagesite-savemessage.md) visor. 
    
4. Destruir la ventana de la interfaz de usuario del formulario.
    
5. Libere los objetos de sitio de mensaje y mensaje del formulario llamando a sus [métodos IUnknown::Release.](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) 
    
6. Notifique a todos los visores registrados del cierre pendiente llamando a sus [métodos IMAPIViewAdviseSink::OnShutdown.](imapiviewadvisesink-onshutdown.md) 
    
7. Llame al [método IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) para cancelar el registro del formulario para la notificación estableciendo el puntero del receptor de notificaciones en **null**.
    
8. Llama a [la función MAPIFreeBuffer](mapifreebuffer.md) para liberar la memoria de las propiedades del formulario. 
    
9. Llama al método **IUnknown::Release** del formulario y coincide con la **llamada AddRef** realizada en el paso 2. 
    
10. Devuelve S_OK.
    
> [!NOTE]
> Una vez completadas estas acciones, los únicos métodos válidos en el objeto de formulario al que se puede llamar son los de la [interfaz IUnknown.](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Cuando **ShutdownForm** devuelve, independientemente de si devuelve un error, libere el formulario llamando a su **método IUnknown::Release.** Puede omitir de forma segura los errores devueltos **por ShutdownForm**.
  
## <a name="see-also"></a>Vea también



[IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md)
  
[IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md)
  
[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)

