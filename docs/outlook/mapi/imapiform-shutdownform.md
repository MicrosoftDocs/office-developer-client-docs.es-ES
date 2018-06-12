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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 9a6ab96a70bce622f44de6576e7b77861302de4f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817259"
---
# <a name="imapiformshutdownform"></a>IMAPIForm::ShutdownForm

  
  
**Se aplica a**: Outlook 
  
Cierra el formulario.
  
```cpp
HRESULT ShutdownForm(
  ULONG ulSaveOptions
);
```

## <a name="parameters"></a>Sintaxis

 _ulSaveOptions_
  
> [entrada] Un valor que controla cómo o si se guardan los datos en el formulario antes de cerrar el formulario. Puede establecer uno de los siguientes indicadores:
    
SAVEOPTS_NOSAVE 
  
> No se deben guardar los datos del formulario.
    
SAVEOPTS_PROMPTSAVE 
  
> El usuario se debe pedir para guardar los datos modificados en el formulario.
    
SAVEOPTS_SAVEIFDIRTY 
  
> Si ha cambiado desde la última vez que se guardó, se deben guardar datos de formulario. Si no se muestra ninguna interfaz de usuario, el formulario, opcionalmente, puede pasar a usar la funcionalidad para la opción SAVEOPTS_NOSAVE.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se ha cerrado el formulario.
    
E_UNEXPECTED 
  
> El formulario ya se ha cerrado por una llamada anterior a **ShutdownForm**.
    
## <a name="remarks"></a>Notas

Visores de formulario llamar al método **IMAPIForm::ShutdownForm** para cerrar un formulario. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Realizar las siguientes tareas en su implementación de **ShutdownForm**:
  
1. Comprobar que un visor ya no llamado **ShutdownForm**y devolver E_UNEXPECTED si lo tiene. Aunque es poco probable, se debe comprobar.
    
2. Llamar al método [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) de su formulario para que el almacenamiento de información para el formulario y las estructuras de datos internos permanecen disponibles hasta que haya terminado el procesamiento. 
    
3. Determinar si hay cambios no guardados para los datos del formulario. Guarde los datos no guardados según cómo se establece el parámetro _ulSaveOptions_ al llamar al método de [IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md) del Visor. 
    
4. Destruir la ventana de interfaz de usuario de su formulario.
    
5. Liberar el formulario mensaje y objetos de sitio de mensaje llamando a sus métodos [IUnknown:: Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) . 
    
6. Notificar a todos los visores del cierre pendiente llamando a sus métodos [IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md) . 
    
7. Llame al método [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) para cancelar el registro de su formulario para notificación estableciendo el puntero de receptor advise en **null**.
    
8. Llame a la función [MAPIFreeBuffer](mapifreebuffer.md) para liberar la memoria para las propiedades del formulario. 
    
9. Llamar al método **IUnknown:: Release** de su formulario, que coincidan con la llamada de **AddRef** realizada en el paso 2. 
    
10. Devuelve S_OK.
    
> [!NOTE]
> Después de que se hayan completado estas acciones, los métodos solo es válidos en el objeto de formulario que se puede llamar son los de la interfaz [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) . 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Cuando se devuelve **ShutdownForm** , independientemente de si devuelve un error, la versión del formulario llamando a su método **IUnknown:: Release** . Puede omitir sin ningún riesgo los errores devueltos por **ShutdownForm**.
  
## <a name="see-also"></a>Ver también



[IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md)
  
[IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md)
  
[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIForm: IUnknown](imapiformiunknown.md)

