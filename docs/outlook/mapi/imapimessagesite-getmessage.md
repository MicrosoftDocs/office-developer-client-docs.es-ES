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
ms.openlocfilehash: 03dd0553d0203585850ac5c4f8c91c86ef60236a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409030"
---
# <a name="imapimessagesitegetmessage"></a>IMAPIMessageSite::GetMessage

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve el mensaje actual.
  
```cpp
HRESULT GetMessage(
  LPMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a>Parameters

 _ppmsg_
  
> [salida] Puntero a un puntero a la interfaz devuelta para el mensaje.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
S_FALSE 
  
> Actualmente no existe ningún mensaje para el formulario de llamada.
    
## <a name="remarks"></a>Comentarios

Los formularios llaman **al método IMAPIMessageSite::GetMessage** para obtener una interfaz de mensaje para el mensaje actual. El mensaje actual es el mismo mensaje que se pasó anteriormente en el método [IPersistMessage::InitNew](ipersistmessage-initnew.md), [IPersistMessage::Load](ipersistmessage-load.md)o [IPersistMessage::SaveCompleted.](ipersistmessage-savecompleted.md) 
  
 **GetMessage** devuelve S_FALSE si no existe ningún mensaje actualmente. Este estado puede producirse después de las llamadas al método [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) o antes de realizar la siguiente llamada a **IPersistMessage::Load** o **IPersistMessage::SaveCompleted.** 
  
Para obtener una lista de interfaces relacionadas con servidores de formulario, vea [Interfaces de formulario MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetSession  <br/> |MFCMAPI usa el **método IMAPIMessageSite::GetMessage** para devolver el puntero de mensaje almacenado en caché, si está disponible.  <br/> |
   
## <a name="see-also"></a>Vea también



[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IPersistMessage::InitNew](ipersistmessage-initnew.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulario MAPI](mapi-form-interfaces.md)

