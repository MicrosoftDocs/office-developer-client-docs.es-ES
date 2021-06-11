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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7b2761e20444c51d08380aee01c41eee797733eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321416"
---
# <a name="imapimessagesitedeletemessage"></a>IMAPIMessageSite::DeleteMessage

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Elimina el mensaje actual.
  
```cpp
HRESULT DeleteMessage(
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a>Parameters

 _pViewContext_
  
> [in] Puntero a un objeto de contexto de vista.
    
 _prcPosRect_
  
> [in] Puntero a una [estructura RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) que contiene el tamaño y la posición de la ventana del formulario actual. El siguiente formulario que se muestra también usa este rectángulo de ventana. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_NO_SUPPORT 
  
> Este sitio de mensaje no admite la operación.
    
## <a name="remarks"></a>Comentarios

Un objeto form llama al método **IMAPIMessageSite::D eleteMessage** para eliminar el mensaje que el formulario está mostrando actualmente. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Tras la devolución de **DeleteMessage,** los objetos de formulario deben buscar un nuevo mensaje y, a continuación, descartarse si no existe ninguno. Para determinar si el mensaje **DeleteMessage** en el que se actuó se eliminó o se movió a una carpeta **Elementos** eliminados, un objeto de formulario puede llamar al método [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) para determinar si se ha devuelto la marca DELETE_IS_MOVE. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Si la implementación del método **DeleteMessage** de un visor de formularios se mueve al siguiente mensaje después de eliminar un mensaje, la implementación debe llamar al método [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) y pasar la marca VCDIR_DELETE antes de realizar la eliminación real. Si la implementación de **DeleteMessage** de un visor de formulario mueve el mensaje eliminado (por ejemplo, a una carpeta **Elementos** eliminados), la implementación debe guardar los cambios en el mensaje si se modificó el mensaje. 
  
Una implementación típica de **DeleteMessage** realiza las siguientes tareas: 
  
1. Si la implementación mueve el mensaje, llama al método [IPersistMessage::Save,](ipersistmessage-save.md) pasando **null** en el _parámetro pMessage_ y **true** en el parámetro _fSameAsLoad._ 
    
2. Llama al método **IMAPIViewContext::ActivateNext,** pasando la marca VCDIR_DELETE en el _parámetro ulDir._ 
    
3. Si se produce un error en la llamada **ActivateNext,** devuelve. Si **ActivateNext** devuelve S_FALSE, llama al [método IPersistMessage::HandsOffMessage.](ipersistmessage-handsoffmessage.md) 
    
4. Elimina o mueve el mensaje.
    
Para obtener la **estructura RECT** usada por la ventana de un formulario, llame a la Windows [función GetWindowRect.](https://msdn.microsoft.com/library/ms633519) 
  
Para obtener una lista de interfaces relacionadas con servidores de formulario, vea [Interfaces de formulario MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::D eleteMessage  <br/> |No implementado.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IPersistMessage::Save](ipersistmessage-save.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulario MAPI](mapi-form-interfaces.md)

