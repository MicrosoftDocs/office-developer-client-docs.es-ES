---
title: IMAPIMessageSiteDeleteMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.DeleteMessage
api_type:
- COM
ms.assetid: 09955996-b904-4c0d-8ba5-954a8875c055
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: da6de94342c8d8bbd378a3cde2fb065c97632291
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817336"
---
# <a name="imapimessagesitedeletemessage"></a>IMAPIMessageSite::DeleteMessage

  
  
**Se aplica a**: Outlook 
  
Elimina el mensaje actual.
  
```cpp
HRESULT DeleteMessage(
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a>Sintaxis

 _pViewContext_
  
> [entrada] Un puntero a un objeto de contexto de la vista.
    
 _prcPosRect_
  
> [entrada] Un puntero a una estructura de [rectángulo](http://msdn.microsoft.com/en-us/library/dd162897%28VS.85%29.aspx) que contiene el tamaño de la ventana y la posición del formulario actual. El siguiente formulario que muestra también usa este rectángulo de la ventana. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_NO_SUPPORT 
  
> La operación no es compatible con este sitio de mensaje.
    
## <a name="remarks"></a>Notas

Un objeto de formulario llama al método de **IMAPIMessageSite::DeleteMessage** para eliminar el mensaje que el formulario se muestra actualmente. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Después de la devolución de **DeleteMessage**, objetos de formulario deben comprobar para un nuevo mensaje y descartar a sí mismos si no existe ninguno. Para determinar si el mensaje **en que deletemessage** actúa fue eliminado o movido a una carpeta de **Elementos eliminados** , un objeto de formulario puede llamar al método de [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) para determinar si se ha devuelto la marca DELETE_IS_MOVE. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Si la implementación del Visor de un formulario del método **DeleteMessage** se mueve hasta el siguiente mensaje después de que elimina un mensaje, la implementación debe llamar al método [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) y pase el indicador VCDIR_DELETE antes de realizar la eliminación real. Si la implementación de un visor formulario de **DeleteMessage** mueve el mensaje eliminado (por ejemplo, en una carpeta de **Elementos eliminados** ), la implementación debe guardar cambios en el mensaje, si se modificó el mensaje. 
  
Una implementación típica de **DeleteMessage** realiza las tareas siguientes: 
  
1. Si la implementación traslada el mensaje, se llama al método [IPersistMessage::Save](ipersistmessage-save.md) , pasando **null** en el parámetro _pMessage_ y **true** en el parámetro _fSameAsLoad_ . 
    
2. Llama al método **IMAPIViewContext::ActivateNext** , pasando el indicador VCDIR_DELETE en el parámetro _ulDir_ . 
    
3. Si se produce un error en la llamada **ActivateNext** , devuelve. Si **ActivateNext** devuelve S_FALSE, llama al método [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) . 
    
4. Elimina o se mueve el mensaje.
    
Para obtener la estructura de **rectángulo** usada por la ventana de un formulario, llame a la función de Windows [GetWindowRect](http://msdn.microsoft.com/en-us/library/ms633519) . 
  
Para obtener una lista de las interfaces relacionadas con los servidores de formulario, vea [Interfaces de formulario MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::DeleteMessage  <br/> |No se ha implementado.  <br/> |
   
## <a name="see-also"></a>Ver también



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IPersistMessage::Save](ipersistmessage-save.md)
  
[IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulario MAPI](mapi-form-interfaces.md)

