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
ms.openlocfilehash: 7f81a0c3c9a9ad0a9bcef5c5685aa5b343237f19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817999"
---
# <a name="ixplogonendmessage"></a>IXPLogon::EndMessage

  
  
**Hace referencia a**: Outlook 
  
Informa al proveedor de transporte que la cola MAPI completó su procesamiento en un mensaje de salida.
  
```cpp
HRESULT EndMessage(
  ULONG ulMsgRef,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parámetros

 _ulMsgRef_
  
> [entrada] Un valor de referencia específicas de mensaje que se ha obtenido en una llamada anterior al método [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) . 
    
 _lpulFlags_
  
> [out] Una máscara de bits de marcadores que indica a la cola MAPI, lo que debe hacer con el mensaje. Si no se establecen indicadores, el mensaje se ha enviado. Se pueden establecer los siguientes indicadores:
    
END_DONT_RESEND 
  
> El proveedor de transporte tiene toda la información que necesita acerca de este mensaje por ahora. Cuando el proveedor de transporte requiere más información o cuando ha enviado el mensaje, se lo comunica a la cola MAPI llamando al método [SpoolerNotify](imapisupport-spoolernotify.md) con el indicador NOTIFY_SENTDEFERRED y pasando el identificador de entrada del mensaje. 
    
END_RESEND_LATER 
  
> El proveedor de transporte no está enviando el mensaje en el tiempo actual por motivos que no sean las condiciones de error. El proveedor de transporte debe se vuelva a llamar más tarde para enviar el mensaje.
    
END_RESEND_NOW 
  
> El proveedor de transporte es necesario reiniciar el mensaje que se pasa a ella en una llamada al método [IMessage::SubmitMessage](imessage-submitmessage.md) . 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelve el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

La cola MAPI llama al método de **IXPLogon::EndMessage** después de que finalice el procesamiento necesarios para proporcionar información de no entrega o entrega extendida. 
  
Una vez que devuelve esta llamada, el valor en el parámetro _ulMsgRef_ ya no es válido para este mensaje. El proveedor de transporte puede volver a usar el mismo valor en un mensaje futuro. 
  
Todos los objetos que se abre el proveedor de transporte durante la transferencia de un mensaje deben liberarse antes de la devolución de llamada **EndMessage** , excepto el objeto de mensaje que la cola MAPI se pasa al proveedor de transporte. El objeto de mensaje pasado por la cola MAPI no es válido después de la llamada **EndMessage** . 
  
## <a name="see-also"></a>Vea también



[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

