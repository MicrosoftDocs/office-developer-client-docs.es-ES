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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350949"
---
# <a name="imapiformsetviewcontext"></a>IMAPIForm::SetViewContext

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Establece un contexto de vista para el formulario. 
  
```cpp
HRESULT SetViewContext(
  LPMAPIVIEWCONTEXT pViewContext
);
```

## <a name="parameters"></a>Parameters

 _pViewContext_
  
> [in] Puntero al nuevo contexto de vista del formulario.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El contexto de vista se estableció correctamente.
    
## <a name="remarks"></a>Comentarios

Los visores de formularios llaman **al método IMAPIForm::SetViewContext** para establecer un contexto de vista de formulario determinado como actual. Un formulario solo puede tener un contexto de vista a la vez. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

La mayoría de los servidores **de formulario implementan SetViewContext** mediante el siguiente algoritmo: 
  
- Si ya existe un contexto de vista para el formulario, cancele el registro del formulario llamando al método [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) con **null** en el  _parámetro pmnvs_ y, a continuación, llame al método [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) del contexto de vista para disminuir su recuento de referencias. 
    
- Si el nuevo contexto de vista no es **nulo,** llama a **IMAPIViewContext::SetAdviseSink** mediante el parámetro  _pViewContext_ para configurar un receptor de aviso de vista nuevo. 
    
- Si el nuevo contexto de vista no es **nulo,** llama al método [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) para determinar qué marcas de estado se han establecido. 
    
- Si el nuevo contexto de vista no es **nulo,** guárdalo y llame a su [método IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) para incrementar su recuento de referencias. 
    
- Actualice los elementos de la interfaz de usuario que dependan del contexto de vista. 
    
Según las marcas de estado devueltas de **IMAPIViewContext::GetViewStatus,** **SetViewContext** también puede realizar otras acciones. Por ejemplo, si se devuelven VCSTATUS_NEXT y VCSTATUS_PREV, **SetViewContext** puede habilitar  los botones **Siguiente** y Anterior para el nuevo contexto de vista. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CreateAndDisplayNewMailInFolder  <br/> |MFCMAPI usa el **método IMAPIForm::SetViewContext** para establecer el contexto de vista de MFCMAPI en el formulario antes de que se muestre el formulario.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
  
[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

