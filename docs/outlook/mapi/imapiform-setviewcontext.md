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
ms.openlocfilehash: 81d99b2bbe6ef7914a4b7d253a3472026872260d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384314"
---
# <a name="imapiformsetviewcontext"></a>IMAPIForm::SetViewContext

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
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
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

La mayoría de los servidores de formulario implementan **SetViewContext** mediante el siguiente algoritmo: 
  
- Si ya existe un contexto de vista para el formulario, cancelar el registro del formulario llamando al método [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) con **null** en el parámetro _pmnvs_ y, a continuación, llamar [IUnknown:: Release al contexto la vista](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) método para reducir su recuento de referencia. 
    
- Si el contexto de vista nueva no es **null**, llamada **IMAPIViewContext::SetAdviseSink** mediante el parámetro _pViewContext_ para configurar una nueva vista de aviso receptor. 
    
- Si el contexto de vista nueva no es **null**, llame al método [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) para determinar qué indicadores de estado se hayan establecido. 
    
- Si el contexto de vista nueva no es **null**, guárdelo y llamar al método [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) para incrementar su recuento de referencia. 
    
- Actualizar todos los elementos de interfaz de usuario que dependen del contexto de la vista. 
    
Dependiendo de los indicadores de estado devueltos desde **IMAPIViewContext::GetViewStatus**, **SetViewContext** también pueden realizar otras acciones. Por ejemplo, si se devuelven los indicadores VCSTATUS_NEXT y VCSTATUS_PREV, **SetViewContext** puede habilitar los botones **siguiente** y **anterior** para el contexto de vista nueva. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CreateAndDisplayNewMailInFolder  <br/> |MFCMAPI usa el método **IMAPIForm::SetViewContext** para establecer el contexto de vista del MFCMAPI en el formulario antes de que se muestre el formulario.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
  
[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

