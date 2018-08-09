---
title: IMAPIMessageSiteSubmitMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.SubmitMessage
api_type:
- COM
ms.assetid: 6b14c383-8bc6-4e86-bd92-0500272af40d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 694ee8b12b9918502e60c0c6ea92992cc1062945
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817360"
---
# <a name="imapimessagesitesubmitmessage"></a>IMAPIMessageSite::SubmitMessage

  
  
**Hace referencia a**: Outlook 
  
Solicitudes que se ponen en cola en el mensaje actual para la entrega.
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se envía un mensaje. Se puede establecer la marca siguiente:
    
FORCE_SUBMIT 
  
> MAPI debe enviar el mensaje, incluso si es posible que no se enviarán inmediatamente.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Objetos de formulario llamar al método **IMAPIMessageSite::SubmitMessage** para solicitar que un mensaje se ponen en cola para la entrega. El sitio de mensaje debe llamar al método [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) antes de enviar el mensaje. El mensaje no es necesario que se han guardado anteriormente, debido a que **SubmitMessage** debe producir el mensaje que se guarde si se ha modificado el mensaje. Después de la devolución de **SubmitMessage**, el formulario debe comprobar si un mensaje actual y descartar propio si no existe ninguno. 
  
Para obtener una lista de las interfaces relacionadas con los servidores de formulario, vea [Interfaces de formulario MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::SubmitMessage  <br/> |MFCMAPI utiliza el método **IMAPIMessageSite::SubmitMessage** para guardar el mensaje. En primer lugar, llama al método **IPersistMessage::HandsOffMessage** y, a continuación, se llama **SubmitMessage**.  <br/> |
   
## <a name="see-also"></a>Vea también



[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulario de MAPI](mapi-form-interfaces.md)

