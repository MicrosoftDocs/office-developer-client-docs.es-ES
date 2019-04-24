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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341772"
---
# <a name="imapisupportstatusrecips"></a>IMAPISupport::StatusRecips

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Genera informes de entrega y de no entrega.
  
```cpp
HRESULT StatusRecips(
LPMESSAGE lpMessage,
LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>Parameters

 _lpMessage_
  
> a Un puntero al mensaje para el que se debe generar el informe.
    
 _lpRecipList_
  
> a Un puntero a una estructura [ADRLIST](adrlist.md) que describe los destinatarios del mensaje al que señala _lpMessage_.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El informe se generó correctamente.
    
MAPI_W_ERRORS_RETURNED 
  
> La llamada se realizó en general, pero no hay opciones de destinatarios para este tipo de destinatario. Cuando se devuelve esta advertencia, la llamada se debe administrar como correcta. Para probar esta advertencia, use la macro **HR_FAILED** . Para obtener más información, consulte [usar macros para el control de errores](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport:: StatusRecips** se implementa para los objetos de soporte del proveedor de transporte. Los proveedores de transporte llaman a **StatusRecips** para solicitar que MAPI envíe un informe de entrega o de no entrega a un conjunto de uno o varios de los destinatarios de un mensaje. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede llamar a **StatusRecips** varias veces durante el procesamiento de un mensaje. Sin embargo, si llama a **StatusRecips** para un mensaje abierto, haga lo mejor para recopilar toda la información de entrega y de no entrega para los destinatarios del mensaje y llamar a **StatusRecips** para la lista de destinatarios. Un único punto de recopilación es importante, ya que varias llamadas de **StatusRecips** para un destinatario pueden dar lugar a que se envíen varios informes idénticos. 
  
Almacene las propiedades relacionadas con la entrega de mensajes o no entrega en la estructura **ADRLIST** indicada por el parámetro _lpRecipList_ . Para obtener una lista completa de las propiedades necesarias y opcionales para los informes de entrega y los informes de no entrega, consulte reQuired [Report Message Properties](required-report-message-properties.md) y [Optional Report Message Properties](optional-report-message-properties.md). 
  
Asigne memoria para la estructura **ADRLIST** en _lpRecipList_ mediante las funciones [MAPIAllocateBuffer](mapiallocatebuffer.md) y [MAPIAllocateMore](mapiallocatemore.md) . MAPI libera la memoria al llamar a la función [MAPIFreeBuffer](mapifreebuffer.md) solo si **StatusRecips** se ejecuta correctamente. 
  
Para obtener información general sobre los informes de entrega y de no entrega, consulte [MAPI Report messages](mapi-report-messages.md).
  
## <a name="see-also"></a>Vea también



[ADRLIST](adrlist.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IXPLogon::EndMessage](ixplogon-endmessage.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

