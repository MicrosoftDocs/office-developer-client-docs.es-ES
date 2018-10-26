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
ms.openlocfilehash: 6613e4168fea6536b1df873da12f2c215be515bf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588506"
---
# <a name="imapiviewcontextactivatenext"></a>IMAPIViewContext::ActivateNext

**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Activa el mensaje siguiente o anterior en el orden de la vista. 
  
```cpp
HRESULT ActivateNext(
ULONG ulDir,
LPCRECT prcPosRect
);
```

## <a name="parameters"></a>Parámetros

_ulDir_
  
> [entrada] Indicadores de estado que proporciona información acerca del mensaje que se va a activar. Valores de indicador válidos son:
    
  - VCDIR_CATEGORY: El Visor debe activar un mensaje en otra categoría de la vista. El mensaje que se va a activar es: 
        
    - El primer mensaje de la categoría vista siguiente si este marcador es ed **o**con VCDIR_NEXT. 
        
    - Se expande el último mensaje de la categoría de la vista anterior, si este marcador es **OR**ed con VCDIR_PREV y la categoría anterior. 
        
    - No se expande el primer mensaje de la categoría de la vista anterior, si este marcador es **OR**ed con VCDIR_PREV y la categoría anterior. En este caso la categoría anterior se somete a la expansión automática. 
        
  - VCDIR_DELETE: El Visor debe activar el mensaje siguiente o anterior porque se ha eliminado el mensaje actual. 
        
  - VCDIR_MOVE: El Visor debe activar el mensaje siguiente o anterior porque se ha movido el mensaje actual. 
        
  - VCDIR_NEXT: El Visor debe activar el mensaje siguiente en el orden de la vista. 
        
  - VCDIR_PREV: El Visor debe activar el mensaje anterior en el orden de la vista. 
        
  - VCDIR_UNREAD: El Visor debe activar el mensaje no leído siguiente o anterior en el orden de la vista. 
    
_prcPosRect_
  
> [entrada] Puntero a un **rectángulo** de Windows estructura que contiene el tamaño y la posición de la ventana que se usará para mostrar el mensaje activado. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El mensaje se ha activado correctamente. 
    
S_FALSE 
  
> El mensaje se ha activado correctamente, pero se abrió un tipo diferente del formulario en el proceso.
    
## <a name="remarks"></a>Comentarios

Objetos de formulario llamar al método **IMAPIViewContext::ActivateNext** para cambiar qué mensaje se muestra al usuario. El valor que se pasa en el parámetro _ulDir_ indica qué mensaje debe estar activado y, en algunos casos, por qué. Los indicadores VCDIR_NEXT y VCDIR_PREVIOUS corresponden a los usuarios elegir el comando **siguiente** o **anterior** en una vista, respectivamente. Estas operaciones normalmente corresponden a moverse hacia arriba o hacia abajo de un mensaje en la lista del Visor de formulario de mensajes. 
  
Los indicadores VCDIR_DELETE y VCDIR_MOVE se establecen por el [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) y los métodos [IMAPIMessageSite::MoveMessage](imapimessagesite-movemessage.md) , respectivamente. Implementaciones de estos métodos llame al método **ActivateNext** con la dirección apropiada y, a continuación, realizan la operación solicitada en el mensaje si la llamada **ActivateNext** no produjo un error. Visores de formulario normalmente permiten a los usuarios especificar la dirección que desea mover en la lista de mensajes. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

La implementación de [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) hace que el mensaje siguiente o anterior en la carpeta, según el valor de _ulDir_, el mensaje actual. Una vez **ActivateNext** devuelve, llame a [IMAPIMessageSite::GetMessage](imapimessagesite-getmessage.md) para obtener un puntero al mensaje recién activado. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Si **ActivateNext** devuelve S_FALSE, o si no está presente un mensaje actual, realice el procedimiento de cierre normal que debe incluir una llamada a método de [IMAPIForm::ShutdownForm](imapiform-shutdownform.md) del formulario. Si se muestra un mensaje siguiente o anterior, utilice el rectángulo de ventana que se pasa en el parámetro _prcPosRect_ para que se muestre. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::ActivateNext  <br/> |MFCMAPI implementa el método **IMAPIViewContext::ActivateNext** en esta función.  <br/> |
   
## <a name="see-also"></a>Vea también

- [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
- [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
- [MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

