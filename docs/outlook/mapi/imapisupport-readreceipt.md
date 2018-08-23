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
ms.openlocfilehash: e785d42639d51dab154a0bde239f858a92ddd143
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588625"
---
# <a name="imapisupportreadreceipt"></a>IMAPISupport::ReadReceipt

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Genera una lectura o del informe nonread para un mensaje.
  
```cpp
HRESULT ReadReceipt(
ULONG ulFlags,
LPMESSAGE lpReadMessage,
LPMESSAGE FAR * lppEmptyMessage
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se genera la lectura o el informe nonread. Se puede establecer la marca siguiente:
    
MAPI_NON_READ 
  
> Se genera un informe nonread. Si no se establece MAPI_NON_READ, se genera un informe de lectura.
    
 _lpReadMessage_
  
> [entrada] Un puntero al mensaje sobre qué se debe generar el informe.
    
 _lppEmptyMessage_
  
> [entrada, salida] En la entrada, _lppEmptyMessage_ apunta a un puntero a un mensaje vacío. En la salida, _lppEmptyMessage_ apunta a un puntero al mensaje de informe. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El informe se ha generado correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport::ReadReceipt** sólo se implementa para objetos de soporte técnico de proveedor de almacén de mensajes. Los proveedores de almacén de mensajes llamada **ReadReceipt** para indicar a MAPI para generar una lectura o del informe nonread para el mensaje que apunta el parámetro _lpReadMessage_ . 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Llamar a **ReadReceipt** cuando se establece la propiedad **PR_READ_RECEIPT_REQUESTED de MAPI** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) y una de las siguientes condiciones es verdadera:
  
- Lo ha leído el mensaje.
    
- El mensaje se ha movido.
    
- El mensaje se ha copiado.
    
- Se ha llamado al método [IMessage::SetReadFlag](imessage-setreadflag.md) del mensaje. 
    
No llame a **ReadReceipt** cuando se elimina un mensaje. 
  
Una lectura informe nonread se debe enviar o sólo una vez para un mensaje. Realizar un seguimiento de estado de lectura de un mensaje y no enviar varios informes para un solo mensaje.
  
Si el parámetro _lppEmptyMessage_ apunta a un mensaje de informe válido cuando devuelve MAPI desde **ReadReceipt**, llame al método [IMessage::SubmitMessage](imessage-submitmessage.md) para enviar el mensaje y, a continuación, liberar el puntero llamando a su **IUnknown:s:Release **(método). 
  
Si se produce un error en **ReadReceipt** , se debe liberar el mensaje sin que se envía. Si almacena el estado de lectura del mensaje, puede intentar generar la lectura o el informe nonread en un momento posterior. 
  
Puede ocultar o mostrar informes de lectura y nonread generados por almacenes en las carpetas. Almacenamiento de informes de lectura y nonread en las carpetas ocultas le permite implementar una mayor seguridad.
  
## <a name="see-also"></a>Recursos adicionales



[IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[Propiedad canónica PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

