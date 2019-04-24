---
title: IMAPIViewContextActivateNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.ActivateNext
api_type:
- COM
ms.assetid: 25ce90ac-526e-48a0-9edb-bd266375d4f4
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5b10f744e3033aab63820e4cd5e414f4c01c27cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351159"
---
# <a name="imapiviewcontextactivatenext"></a>IMAPIViewContext::ActivateNext

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Activa el mensaje siguiente o anterior en el orden de vista. 
  
```cpp
HRESULT ActivateNext(
ULONG ulDir,
LPCRECT prcPosRect
);
```

## <a name="parameters"></a>Parameters

_ulDir_
  
> a Indicadores de estado que proporcionan información sobre el mensaje que se va a activar. La configuración válida del indicador es la siguiente:
    
  - VCDIR_CATEGORY: el visor debe activar un mensaje en otra categoría de la vista. El mensaje que se va a activar es: 
        
    - El primer mensaje de la siguiente categoría de vista si esta marca es **o**Ed con VCDIR_NEXT. 
        
    - Último mensaje de la categoría de vista anterior si este indicador es **o**Ed con VCDIR_PREV y se expande la categoría anterior. 
        
    - El primer mensaje de la categoría de vista anterior si esta marca es **o**Ed con VCDIR_PREV y la categoría anterior no se expande. En este caso, la categoría anterior sufre una expansión automática. 
        
  - VCDIR_DELETE: el visor debe activar el mensaje siguiente o anterior porque se ha eliminado el mensaje actual. 
        
  - VCDIR_MOVE: el visor debe activar el mensaje siguiente o anterior porque el mensaje actual se ha movido. 
        
  - VCDIR_NEXT: el visor debe activar el siguiente mensaje en el orden de vista. 
        
  - VCDIR_PREV: el visor debe activar el mensaje anterior en el orden de la vista. 
        
  - VCDIR_UNREAD: el visor debe activar el mensaje no leído siguiente o anterior en el orden de vista. 
    
_prcPosRect_
  
> a Puntero a una estructura de Windows **Rect** que contiene el tamaño y la posición de la ventana que se va a usar para mostrar el mensaje activado. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El mensaje se activó correctamente. 
    
S_FALSE 
  
> El mensaje se activó correctamente, pero se abrió un tipo diferente de formulario en el proceso.
    
## <a name="remarks"></a>Comentarios

Los objetos de formulario llaman al método **IMAPIViewContext:: ActivateNext** para cambiar el mensaje que se muestra al usuario. El valor que se pasa en el parámetro _ulDir_ indica qué mensaje debe activarse y, en algunos casos, por qué. Los indicadores VCDIR_NEXT y VCDIR_PREVIOUS corresponden a los usuarios que eligen el comando **siguiente** o **anterior** en una vista, respectivamente. Estas operaciones suelen corresponderse para subir o bajar un mensaje en la lista de mensajes del visor de formulario. 
  
Los indicadores VCDIR_DELETE y VCDIR_MOVE los establecen los métodos [IMAPIMessageSite::D eletemessage](imapimessagesite-deletemessage.md) y [IMAPIMessageSite:: MoveMessage](imapimessagesite-movemessage.md) , respectivamente. Las implementaciones de estos métodos llaman a **ActivateNext** con la dirección adecuada y, a continuación, realizan la operación solicitada en el mensaje si la llamada **ActivateNext** no se ha realizado correctamente. Los visores de formularios normalmente permiten a los usuarios especificar la dirección que se va a mover en la lista de mensajes. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

La implementación de [IMAPIViewContext:: ActivateNext](imapiviewcontext-activatenext.md) hace que el mensaje siguiente o anterior de la carpeta, según el valor de _ulDir_, el mensaje actual. Una vez que **ActivateNext** devuelve un, llame a [IMAPIMessageSite:: GetMessage](imapimessagesite-getmessage.md) para obtener un puntero al mensaje recién activado. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Si **ActivateNext** devuelve S_FALSE, o si no hay un mensaje actual, realice el procedimiento de cierre normal que deba incluir una llamada al método [IMAPIForm:: ShutdownForm](imapiform-shutdownform.md) del formulario. Si se muestra un mensaje próximo o anterior, use el rectángulo de la ventana que se pasa en el parámetro _prcPosRect_ para mostrarlo. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer:: ActivateNext  <br/> |MFCMAPI implementa el método **IMAPIViewContext:: ActivateNext** en esta función.  <br/> |
   
## <a name="see-also"></a>Vea también

- [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
- [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
- [MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

