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
ms.openlocfilehash: f3642c890c3922611d57dea6f03aca5606876864
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817569"
---
# <a name="imapisupportstatusrecips"></a>IMAPISupport::StatusRecips

  
  
**Hace referencia a**: Outlook 
  
Genera informes de entrega y no entrega.
  
```cpp
HRESULT StatusRecips(
LPMESSAGE lpMessage,
LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>Parámetros

 _lpMessage_
  
> [entrada] Un puntero al mensaje para el que se debe generar el informe.
    
 _lpRecipList_
  
> [entrada] Un puntero a una estructura [ADRLIST](adrlist.md) que describe a los destinatarios del mensaje que apunta _lpMessage_.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El informe se ha generado correctamente.
    
MAPI_W_ERRORS_RETURNED 
  
> La llamada satisfactoria, pero no hay ningún destinatarios opciones para este tipo de destinatario. Cuando se devuelve esta advertencia, la llamada se debe controlarse como correcta. Para probar esta advertencia, utilice la macro **HR_FAILED** . Para obtener más información, vea [Uso de Macros para el control de errores](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport::StatusRecips** se implementa para los objetos de soporte técnico del proveedor de transporte. Los proveedores de transporte llame a **StatusRecips** para solicitar que envían MAPI un informe de entrega o de no entrega a un conjunto de uno o varios de los destinatarios de un mensaje. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede llamar varias veces a **StatusRecips** durante el procesamiento de un mensaje. Sin embargo, si se llama a **StatusRecips** para abrir el mensaje, realice los procedimientos para recopilar toda la información de entrega y no entrega de los destinatarios del mensaje y llamar a **StatusRecips** para esa lista de destinatarios. Un único punto de colección es importante, porque pueden producir varias llamadas **StatusRecips** para un destinatario en varios informes idénticos que se está enviados. 
  
Almacenar propiedades relacionadas con la entrega del mensaje o no entrega en la estructura **ADRLIST** indicada por el parámetro _lpRecipList_ . Para obtener una lista completa de las propiedades opcionales y obligatorios para informes de entrega e informes de no entrega, vea [Propiedades de mensaje de informe necesarias](required-report-message-properties.md) y [Propiedades de mensaje de informe opcionales](optional-report-message-properties.md). 
  
Asignar memoria para la estructura **ADRLIST** en _lpRecipList_ mediante el uso de las funciones [MAPIAllocateBuffer](mapiallocatebuffer.md) y [MAPIAllocateMore](mapiallocatemore.md) . MAPI libera la memoria mediante una llamada a la función [MAPIFreeBuffer](mapifreebuffer.md) sólo si **StatusRecips** se realiza correctamente. 
  
Para obtener información general de informes de entrega y no entrega, vea [Los mensajes de informe de MAPI](mapi-report-messages.md).
  
## <a name="see-also"></a>Vea también



[ADRLIST](adrlist.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IXPLogon::EndMessage](ixplogon-endmessage.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

