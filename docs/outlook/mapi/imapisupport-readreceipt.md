---
title: IMAPISupportReadReceipt
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ReadReceipt
api_type:
- COM
ms.assetid: ef31b61a-93b6-4ae8-bc71-f5ef5caf43f4
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 1915004847fdfd27c97656223866aaab9d3e59c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425326"
---
# <a name="imapisupportreadreceipt"></a>IMAPISupport::ReadReceipt

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Genera un informe leído o no leído para un mensaje.
  
```cpp
HRESULT ReadReceipt(
ULONG ulFlags,
LPMESSAGE lpReadMessage,
LPMESSAGE FAR * lppEmptyMessage
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Máscara de bits de marcas que controla cómo se genera el informe leído o no leído. Se puede establecer la siguiente marca:
    
MAPI_NON_READ 
  
> Se genera un informe no leído. Si MAPI_NON_READ no está establecido, se genera un informe de lectura.
    
 _lpReadMessage_
  
> [in] Puntero al mensaje sobre el que se debe generar el informe.
    
 _lppEmptyMessage_
  
> [in, out] En la entrada,  _lppEmptyMessage_ apunta a un puntero a un mensaje vacío. En el resultado,  _lppEmptyMessage_ apunta a un puntero al mensaje de informe. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El informe se generó correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::ReadReceipt** solo se implementa para objetos de soporte técnico del proveedor del almacén de mensajes. Los proveedores de almacén de mensajes llaman a **ReadReceipt para** indicar a MAPI que genere un informe de lectura o no leído para el mensaje al que apunta el _parámetro lpReadMessage._ 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Llame **a ReadReceipt** cuando se establezca la propiedad **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) y se cumple una de las siguientes condiciones:
  
- El mensaje se ha leído.
    
- El mensaje se ha movido.
    
- El mensaje se ha copiado.
    
- Se ha llamado al [método IMessage::SetReadFlag](imessage-setreadflag.md) del mensaje. 
    
No llame a **ReadReceipt cuando** se elimine un mensaje. 
  
Un informe leído o no leído debe enviarse solo una vez para un mensaje. Realice un seguimiento del estado de lectura de un mensaje y no envíe varios informes para un solo mensaje.
  
Si el parámetro _lppEmptyMessage_ apunta a un mensaje de informe válido cuando MAPI devuelve desde **ReadReceipt**, llame al método [IMessage::SubmitMessage](imessage-submitmessage.md) para enviar el mensaje y, a continuación, libere el puntero llamando a su **método IUnknown:s:Release.** 
  
Si **ReadReceipt produce** un error, el mensaje debe liberarse sin enviarse. Si almacena el estado de lectura del mensaje, puede intentar generar el informe leído o no leído más adelante. 
  
Puede ocultar o mostrar informes leídos y no leídos generados por los almacenes de las carpetas. El almacenamiento de informes leídos y no leídos en carpetas ocultas permite implementar una seguridad más estricta.
  
## <a name="see-also"></a>Vea también



[IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[Propiedad canónica PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

