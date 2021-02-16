---
title: IMAPISupportStatusRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.StatusRecips
api_type:
- COM
ms.assetid: 9c34538e-5ba4-47c8-8002-85afa9d6c067
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 39d8786bf558ade4599d69e0a764f87fe60d99f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408771"
---
# <a name="imapisupportstatusrecips"></a>IMAPISupport::StatusRecips

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Genera informes de entrega y no entrega.
  
```cpp
HRESULT StatusRecips(
LPMESSAGE lpMessage,
LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>Parámetros

 _lpMessage_
  
> [entrada] Puntero al mensaje para el que se debe generar el informe.
    
 _lpRecipList_
  
> [entrada] Puntero a una [estructura ADRLIST](adrlist.md) que describe los destinatarios del mensaje que apunta  _lpMessage_.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El informe se generó correctamente.
    
MAPI_W_ERRORS_RETURNED 
  
> La llamada se ha hecho correctamente en general, pero no hay opciones de destinatario para este tipo de destinatario. Cuando se devuelve esta advertencia, la llamada debe tratarse como correcta. Para probar esta advertencia, use la **macro HR_FAILED** datos. Para obtener más información, vea [Usar macros para el control de errores.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::StatusRecips** se implementa para objetos de compatibilidad del proveedor de transporte. Los proveedores de transporte llaman a **StatusRecips** para solicitar que MAPI envíe un informe de entrega o no entrega a un conjunto de uno o varios de los destinatarios de un mensaje. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede llamar a **StatusRecips varias** veces durante el procesamiento de un mensaje. Sin embargo, si llama a **StatusRecips** para un mensaje abierto, haga todo lo posible para recopilar toda la información de entrega y no entrega para los destinatarios del mensaje y llamar a **StatusRecips** para esa lista de destinatarios. Un único punto de recopilación es importante, ya que varias **llamadas StatusRecips** para un destinatario pueden dar como resultado que se envíen varios informes idénticos. 
  
Almacene las propiedades relacionadas con la entrega de mensajes o nondelivery en la estructura **ADRLIST** indicada por el parámetro _lpRecipList._ Para obtener una lista completa de propiedades obligatorias y opcionales para informes de entrega e informes de no entrega, vea Propiedades de mensaje de informe requeridas y Propiedades opcionales [del mensaje de informe.](optional-report-message-properties.md) [](required-report-message-properties.md) 
  
Asigne memoria para la **estructura ADRLIST** _en lpRecipList_ mediante las [funciones MAPIAllocateBuffer](mapiallocatebuffer.md) y [MAPIAllocateMore.](mapiallocatemore.md) MAPI libera la memoria llamando a la [función MAPIFreeBuffer](mapifreebuffer.md) solo si **StatusRecips se realiza** correctamente. 
  
Para obtener información general sobre los informes de entrega y no entrega, vea [mensajes de informe MAPI](mapi-report-messages.md).
  
## <a name="see-also"></a>Consulte también



[ADRLIST](adrlist.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IXPLogon::EndMessage](ixplogon-endmessage.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

