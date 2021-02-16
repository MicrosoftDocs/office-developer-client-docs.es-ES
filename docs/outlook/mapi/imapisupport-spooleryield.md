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
ms.openlocfilehash: f6cdebf82d8b84ada3d029865867c5192af90b0d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409912"
---
# <a name="imapisupportspooleryield"></a>IMAPISupport::SpoolerYield

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona control de la CPU a la cola MAPI para que pueda realizar las tareas que considere necesarias.
  
```cpp
HRESULT SpoolerYield(
ULONG ulFlags
);
```

## <a name="parameters"></a>Parámetros

 _ulFlags_
  
> Reservado; debe ser cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El proveedor de transporte publicó correctamente la CPU.
    
MAPI_W_CANCEL_MESSAGE 
  
> Indica al proveedor de transporte que detenga la entrega del mensaje a los destinatarios que aún no lo han recibido.
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::SpoolerYield** se implementa para objetos de compatibilidad del proveedor de transporte. Los proveedores de transporte **llaman a SpoolerYield para** permitir que la cola MAPI pueda realizar cualquier procesamiento necesario. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Llame **a SpoolerYield** cuando realice operaciones largas que se puedan pausar. Esto permite que las aplicaciones en primer plano se ejecuten durante una operación larga, como la entrega a una lista de destinatarios de gran tamaño a través de una red ocupada. 
  
Si **SpoolerYield** vuelve con MAPI_W_CANCEL_MESSAGE, la cola MAPI ha determinado que el mensaje ya no se debe enviar. Vuelva MAPI_E_USER_CANCEL al proceso de llamada y salga, si es posible. 
  
Para obtener más información acerca del rendimiento de la cola MAPI, vea [Interactuar con la cola MAPI.](interacting-with-the-mapi-spooler.md)
  
## <a name="see-also"></a>Consulte también



[IMAPISupport: IUnknown](imapisupportiunknown.md)

