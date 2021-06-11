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
ms.openlocfilehash: c68e4fbda661a119416918a2c35d1780f1deccda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321369"
---
# <a name="imapimessagesitemovemessage"></a>IMAPIMessageSite::MoveMessage

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Mueve el mensaje actual a una carpeta.
  
```cpp
HRESULT MoveMessage(
  LPFOLDER pFolderDestination,
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a>Parameters

 _pFolderDestination_
  
> [in] Puntero a la carpeta donde se va a mover el mensaje.
    
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

Los objetos Form llaman **al método IMAPIMessageSite::MoveMessage** para mover el mensaje actual a una nueva carpeta. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

La implementación de **MoveMessage** de un visor de formulario debe llamar al método [IMAPIViewContext::ActivateNext,](imapiviewcontext-activatenext.md) pasando la marca VCDIR_MOVE, antes de mover realmente el mensaje a una carpeta nueva. Para obtener la **estructura RECT** usada por la ventana de un formulario, llame a la Windows [función GetWindowRect.](https://msdn.microsoft.com/library/ms633519) 
  
Para obtener una lista de interfaces relacionadas con servidores de formulario, vea [Interfaces de formulario MAPI](mapi-form-interfaces.md).
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Tras la devolución de **MoveMessage,** los formularios deben buscar un mensaje actual y, a continuación, descartarse si no existe ninguno. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::MoveMessage  <br/> |No implementado.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulario MAPI](mapi-form-interfaces.md)

