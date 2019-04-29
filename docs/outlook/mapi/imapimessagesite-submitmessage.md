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
ms.openlocfilehash: 496732e334d2d39672048dd1a02346aaee4b70e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417031"
---
# <a name="imapimessagesitesubmitmessage"></a>IMAPIMessageSite::SubmitMessage

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Solicita que el mensaje actual se ponga en cola para su entrega.
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> a Una máscara de máscara de marcadores que controla cómo se envía un mensaje. Se puede establecer la siguiente marca:
    
FORCE_SUBMIT 
  
> MAPI debe enviar el mensaje incluso si es posible que no se envíe inmediatamente.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Los objetos de formulario llaman al método **IMAPIMessageSite:: SubmitMessage** para solicitar que un mensaje se ponga en la cola para su entrega. El sitio del mensaje debe llamar al método [IPersistMessage:: HandsOffMessage](ipersistmessage-handsoffmessage.md) antes de enviar el mensaje. No es necesario que el mensaje se haya guardado previamente porque **SubmitMessage** debe hacer que se guarde el mensaje si se ha modificado el mensaje. Después de la devolución de **SubmitMessage**, el formulario debe comprobar un mensaje actual y, a continuación, descartarse si no hay ninguno. 
  
Para obtener una lista de las interfaces relacionadas con los servidores de formularios, consulte [MAPI Form interfaces](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer:: SubmitMessage  <br/> |MFCMAPI usa el método **IMAPIMessageSite:: SubmitMessage** para guardar el mensaje. En primer lugar, llama al método **IPersistMessage:: HandsOffMessage** y, a continuación, llama a **SubmitMessage**.  <br/> |
   
## <a name="see-also"></a>Ver también



[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulario de MAPI](mapi-form-interfaces.md)

