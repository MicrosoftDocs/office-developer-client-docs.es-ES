---
title: IXPLogonEndMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.EndMessage
api_type:
- COM
ms.assetid: bb29e6a0-7a92-46eb-bbeb-6f2df6ac6d21
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 03eccfe27c6f93e42ee01a34fbf5df766c145cf1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414161"
---
# <a name="ixplogonendmessage"></a>IXPLogon::EndMessage

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Informa al proveedor de transporte que la cola MAPI completó el procesamiento en un mensaje saliente.
  
```cpp
HRESULT EndMessage(
  ULONG ulMsgRef,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameters

 _ulMsgRef_
  
> a Un valor de referencia específico del mensaje que se obtuvo en una llamada anterior al método [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md) . 
    
 _lpulFlags_
  
> contempla Máscara de máscara de marcadores que indica a la cola MAPI lo que debe hacer con el mensaje. Si no se establece ningún marcador, se ha enviado el mensaje. Se pueden establecer los siguientes indicadores:
    
END_DONT_RESEND 
  
> El proveedor de transporte tiene toda la información que necesita sobre este mensaje en este momento. Cuando el proveedor de transporte requiere más información o cuando envía el mensaje, notifica a la cola MAPI llamando al método [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) con la marca NOTIFY_SENTDEFERRED y pasando el identificador de entrada del mensaje. 
    
END_RESEND_LATER 
  
> El proveedor de transporte no envía el mensaje en el momento actual por motivos que no son condiciones de error. Se debe llamar al proveedor de transporte más adelante para enviar el mensaje.
    
END_RESEND_NOW 
  
> El proveedor de transporte debe reiniciar el mensaje que se le pasó en una llamada al método [IMessage:: SubmitMessage](imessage-submitmessage.md) . 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y ha devuelto el valor o los valores esperados.
    
## <a name="remarks"></a>Comentarios

La cola MAPI llama al método **IXPLogon:: EndMessage** después de completar el procesamiento implicado en proporcionar la información de entrega ampliada o no entregada. 
  
Una vez que se devuelve esta llamada, el valor del parámetro _ulMsgRef_ ya no es válido para este mensaje. El proveedor de transporte puede reutilizar el mismo valor en un mensaje futuro. 
  
Todos los objetos que el proveedor de transporte abre durante la transferencia de un mensaje debe liberarse antes de que se devuelva la llamada a **EndMessage** , con la excepción del objeto Message que la cola MAPI pasa al proveedor de transporte. El objeto de mensaje que pasa la cola MAPI no es válido después de la llamada **EndMessage** . 
  
## <a name="see-also"></a>Ver también



[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

