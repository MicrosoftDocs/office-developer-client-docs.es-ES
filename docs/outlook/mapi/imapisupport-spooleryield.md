---
title: IMAPISupportSpoolerYield
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SpoolerYield
api_type:
- COM
ms.assetid: f5c6ba8f-4ef5-4d60-b4e6-5b9160ec4e99
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d90f502e2cd7f97ac273ebecedbd0363097b1d60
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584957"
---
# <a name="imapisupportspooleryield"></a>IMAPISupport::SpoolerYield

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Proporciona control de la CPU a la cola de MAPI para que pueda realizar las tareas que considere necesarias.
  
```cpp
HRESULT SpoolerYield(
ULONG ulFlags
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> Reservado; debe ser cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El proveedor de transporte había publicado correctamente la CPU.
    
MAPI_W_CANCEL_MESSAGE 
  
> Indica el proveedor de transporte para detener la entrega del mensaje a los destinatarios que aún no la ha recibido.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport::SpoolerYield** se implementa para los objetos de soporte técnico del proveedor de transporte. Los proveedores de transporte llame a **SpoolerYield** para permitir que la cola MAPI realizar cualquier procesamiento necesario. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Llame a **SpoolerYield** al realizar las operaciones largas que pueden poner en pausa. Esto permite a las aplicaciones de primer plano para que se ejecute durante una operación larga, como la entrega a una lista de destinatarios grandes en una red ocupada. 
  
Si **SpoolerYield** devuelve con MAPI_W_CANCEL_MESSAGE, la cola MAPI ha determinado que ya no se debe enviar el mensaje. Devolver MAPI_E_USER_CANCEL a su proceso de llamada y exit, si es posible. 
  
Para obtener más información acerca de la obtención de la cola MAPI, consulte [interactuar con la cola de MAPI](interacting-with-the-mapi-spooler.md).
  
## <a name="see-also"></a>Vea también



[IMAPISupport: IUnknown](imapisupportiunknown.md)

