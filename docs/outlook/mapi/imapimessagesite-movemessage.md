---
title: IMAPIMessageSiteMoveMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.MoveMessage
api_type:
- COM
ms.assetid: cd4d7b11-fad0-4f05-a99e-9567abcab45c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0451d8635848705ef912b9a575d6390898251f4f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817351"
---
# <a name="imapimessagesitemovemessage"></a>IMAPIMessageSite::MoveMessage

  
  
**Hace referencia a**: Outlook 
  
Mueve el mensaje actual a una carpeta.
  
```cpp
HRESULT MoveMessage(
  LPFOLDER pFolderDestination,
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a>Parámetros

 _pFolderDestination_
  
> [entrada] Un puntero a la carpeta donde el mensaje se va a mover.
    
 _pViewContext_
  
> [entrada] Un puntero a un objeto de contexto de la vista.
    
 _prcPosRect_
  
> [entrada] Un puntero a una estructura de [rectángulo](http://msdn.microsoft.com/en-us/library/dd162897%28VS.85%29.aspx) que contiene el tamaño de la ventana y la posición del formulario actual. El siguiente formulario que muestra también usa este rectángulo de la ventana. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_NO_SUPPORT 
  
> La operación no es compatible con este sitio de mensaje.
    
## <a name="remarks"></a>Comentarios

Objetos de formulario llamar al método **IMAPIMessageSite::MoveMessage** para mover el mensaje actual a una nueva carpeta. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Implementación del Visor de un formulario de **MoveMessage** debe llamar al método [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) , que se pasa el indicador VCDIR_MOVE, antes de mover realmente el mensaje a una carpeta nueva. Para obtener la estructura de **rectángulo** usada por la ventana de un formulario, llame a la función de Windows [GetWindowRect](http://msdn.microsoft.com/en-us/library/ms633519) . 
  
Para obtener una lista de las interfaces relacionadas con los servidores de formulario, vea [Interfaces de formulario MAPI](mapi-form-interfaces.md).
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Después de la devolución de **MoveMessage**, formularios deben comprobar si un mensaje actual y descartar a sí mismos si no existe ninguno. 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::MoveMessage  <br/> |No se ha implementado.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulario de MAPI](mapi-form-interfaces.md)

