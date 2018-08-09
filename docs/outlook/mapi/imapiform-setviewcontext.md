---
title: IMAPIFormSetViewContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.SetViewContext
api_type:
- COM
ms.assetid: a7b10007-42d8-4755-8362-f8ad9a8dad68
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c1ba49ba1b4deacb684da1411d86ebd4dd19e63f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817267"
---
# <a name="imapiformsetviewcontext"></a>IMAPIForm::SetViewContext

  
  
**Hace referencia a**: Outlook 
  
Establece un contexto de vista para el formulario. 
  
```cpp
HRESULT SetViewContext(
  LPMAPIVIEWCONTEXT pViewContext
);
```

## <a name="parameters"></a>Parámetros

 _pViewContext_
  
> [entrada] Un puntero al nuevo contexto de vista para el formulario.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se estableció correctamente en el contexto de vista.
    
## <a name="remarks"></a>Comentarios

Visores de formulario llamar al método **IMAPIForm::SetViewContext** para establecer un contexto de vista de formulario en particular como actual. Un formulario puede tener solo un contexto de vista a la vez. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

La mayoría de los servidores de formulario implementan **SetViewContext** mediante el siguiente algoritmo: 
  
- Si ya existe un contexto de vista para el formulario, cancelar el registro del formulario llamando al método [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) con **null** en el parámetro _pmnvs_ y, a continuación, llamar [IUnknown:: Release al contexto la vista](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) método para reducir su recuento de referencia. 
    
- Si el contexto de vista nueva no es **null**, llamada **IMAPIViewContext::SetAdviseSink** mediante el parámetro _pViewContext_ para configurar una nueva vista de aviso receptor. 
    
- Si el contexto de vista nueva no es **null**, llame al método [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) para determinar qué indicadores de estado se hayan establecido. 
    
- Si el contexto de vista nueva no es **null**, guárdelo y llamar al método [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) para incrementar su recuento de referencia. 
    
- Actualizar todos los elementos de interfaz de usuario que dependen del contexto de la vista. 
    
Dependiendo de los indicadores de estado devueltos desde **IMAPIViewContext::GetViewStatus**, **SetViewContext** también pueden realizar otras acciones. Por ejemplo, si se devuelven los indicadores VCSTATUS_NEXT y VCSTATUS_PREV, **SetViewContext** puede habilitar los botones **siguiente** y **anterior** para el contexto de vista nueva. 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CreateAndDisplayNewMailInFolder  <br/> |MFCMAPI usa el método **IMAPIForm::SetViewContext** para establecer el contexto de vista del MFCMAPI en el formulario antes de que se muestre el formulario.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
  
[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

