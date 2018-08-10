---
title: IMAPIMessageSiteGetMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetMessage
api_type:
- COM
ms.assetid: 49d12c49-84f8-44ac-bc4a-2ee44a46f8c1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b3cdd9994de3e2a02a5302068881abce57a632a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817340"
---
# <a name="imapimessagesitegetmessage"></a>IMAPIMessageSite::GetMessage

  
  
**Hace referencia a**: Outlook 
  
Devuelve el mensaje actual.
  
```cpp
HRESULT GetMessage(
  LPMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a>Parámetros

 _ppmsg_
  
> [out] Un puntero a un puntero a la interfaz devuelta para el mensaje.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
S_FALSE 
  
> Actualmente no existe ningún mensaje para el formulario de llamada.
    
## <a name="remarks"></a>Comentarios

Formularios de llamar al método **IMAPIMessageSite::GetMessage** para obtener una interfaz de mensaje para el mensaje actual. El mensaje actual es el mismo mensaje tal y como se pasó anteriormente en el método [IPersistMessage::InitNew](ipersistmessage-initnew.md), [IPersistMessage::Load](ipersistmessage-load.md)o [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) . 
  
 **GetMessage** devuelve S_FALSE si actualmente no existe ningún mensaje. Este estado puede producirse después de las llamadas al método [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) o antes de la siguiente llamada a **IPersistMessage::Load** o **IPersistMessage::SaveCompleted** se realiza. 
  
Para obtener una lista de las interfaces relacionadas con los servidores de formulario, vea [Interfaces de formulario MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetSession  <br/> |MFCMAPI usa el método **IMAPIMessageSite::GetMessage** para devolver el puntero de mensaje actualmente en caché, si está disponible.  <br/> |
   
## <a name="see-also"></a>Vea también



[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IPersistMessage::InitNew](ipersistmessage-initnew.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulario de MAPI](mapi-form-interfaces.md)

