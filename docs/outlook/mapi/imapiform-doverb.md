---
title: IMAPIFormDoVerb
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.DoVerb
api_type:
- COM
ms.assetid: 8b582571-b448-4476-91d9-4cc94dbec710
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 60a8c89afe0d70a1737c6ce694c66359fd6aae4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329465"
---
# <a name="imapiformdoverb"></a>IMAPIForm::DoVerb

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Solicita que el formulario realice las tareas que asocie con un verbo específico.
  
```cpp
HRESULT DoVerb(
  LONG iVerb,
  LPMAPIVIEWCONTEXT lpViewContext,
  ULONG_PTR hwndParent,
  LPCRECT lprcPosRect
);
```

## <a name="parameters"></a>Parameters

 _iVerb_
  
> [in] Número asociado a uno de los verbos del formulario.
    
 _lpViewContext_
  
> [in] Puntero a un objeto de contexto de vista. El  _parámetro lpViewContext_ puede ser **null**.
    
 _hwndParent_
  
> [in] Un identificador de la ventana principal de cualquier cuadro de diálogo o ventana que muestre este método. El  _parámetro hwndParent_ debe ser **null** si el cuadro de diálogo o la ventana no son modales. 
    
 _lprcPosRect_
  
> [in] Puntero a una estructura [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) de Win32 que contiene el tamaño y la posición de la ventana del formulario. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El verbo se invocó correctamente.
    
OLEOBJ_S_CANNOT_DOVERB_NOW 
  
> El verbo representado por el  _parámetro iVerb_ es válido, pero el formulario no puede realizar las operaciones asociadas actualmente con él. 
    
## <a name="remarks"></a>Comentarios

Los visores de formularios llaman al método **IMAPIForm::D oVerb** para solicitar que el formulario realice las tareas que asocia con cada verbo compatible con el formulario. 
  
Cada uno de los verbos admitidos se identifica mediante un valor numérico, que se pasa a **DoVerb** en el _parámetro iVerb._ Las implementaciones típicas de **DoVerb** contienen una **instrucción switch** que prueba los valores válidos para el parámetro  _iVerb_ del formulario. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Si el visor de formulario especifica un contexto de vista en el parámetro _lpViewContext,_ úselo en la implementación de **DoVerb** en lugar del contexto de vista pasado en una llamada anterior al método [IMAPIForm::SetViewContext.](imapiform-setviewcontext.md) Realice los cambios necesarios en las estructuras de datos internas y no guarde el contexto de vista. 
  
Realice las siguientes tareas en la **implementación de DoVerb:** 
  
- Ejecute el código que sea necesario para el verbo concreto asociado al _parámetro iVerb._ 
    
- Si es necesario, restaure el contexto de vista original.
    
- Si se ha pasado un número de verbo desconocido, MAPI_E_NO_SUPPORT. De lo contrario, devuelve un resultado basado en el éxito o error de cualquier verbo que se haya ejecutado.
    
- Cierre el formulario. Siempre es su responsabilidad cerrar el formulario una vez completada una llamada a **DoVerb.** 
    
Algunos verbos, como Print, deben ser modales con respecto a la llamada **a DoVerb;** es decir, la operación indicada debe finalizar antes de que la llamada **DoVerb** devuelva. 
  
Para obtener la **estructura RECT** usada por la ventana de un formulario, llame a la [función GetWindowRect.](https://msdn.microsoft.com/library/ms633519) 
  
No guarde el controlador en el  _parámetro hwndParent_ porque, aunque normalmente permanece válido hasta la finalización de **DoVerb,** puede destruirse inmediatamente después de la devolución de la llamada.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede hacer que los verbos no modales actúen como verbos modales _señalando lpViewContext_ a una implementación de contexto de vista que devuelve la marca VCSTATUS_MODAL de su método [IMAPIViewContext::GetViewStatus.](imapiviewcontext-getviewstatus.md) 
  
Para obtener más información acerca de los verbos en MAPI, vea [Verbos de formulario](form-verbs.md). Para obtener más información acerca de cómo se controlan los verbos en OLE, vea [OLE y Transferencia de datos](https://msdn.microsoft.com/library/ms693425%28VS.85%29.aspx).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::CallDoVerb  <br/> |MFCMAPI usa el **método IMAPIForm::D oVerb** para invocar un verbo en un formulario.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIForm::SetViewContext](imapiform-setviewcontext.md)
  
[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
  
[Verbos de formulario](form-verbs.md)

