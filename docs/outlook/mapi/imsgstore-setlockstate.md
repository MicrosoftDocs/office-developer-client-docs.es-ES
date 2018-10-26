---
title: IMsgStoreSetLockState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.SetLockState
api_type:
- COM
ms.assetid: 4b1176ec-4126-43f5-856d-cbab8d622825
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2efee531e277b6295b7d4bc299eefc789a805d34
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571090"
---
# <a name="imsgstoresetlockstate"></a>IMsgStore::SetLockState

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Bloquea o desbloquea un mensaje. Se llama a este m�todo s�lo por la cola MAPI.
  
```cpp
HRESULT SetLockState(
  LPMESSAGE lpMessage,
  ULONG ulLockState  
);
```

## <a name="parameters"></a>Par�metros

 _lpMessage_
  
> [entrada] Un puntero al mensaje que se va a bloquear o desbloquear.
    
 _ulLockState_
  
> [entrada] Un valor que indica si el mensaje debe ser bloqueado o desbloqueado. Uno de los valores siguientes es válida:
    
MSG_LOCKED 
  
> Debe ser bloqueado el mensaje. 
    
MSG_UNLOCKED 
  
> El mensaje debe ser desbloqueado.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El estado de bloqueo del mensaje se estableció correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMsgStore::SetLockState** se bloquea o desbloquea un mensaje. **SetLockState** se puede llamar sólo por la cola MAPI mientras está enviando el mensaje. 
  
Normalmente, cuando la cola MAPI llama a **SetLockState** para bloquear un mensaje, bloquea sólo el mensaje más antiguo (es decir, el siguiente mensaje en cola para que la cola MAPI enviar). Si el mensaje más antiguo en la cola está esperando para un proveedor de transporte disponible temporalmente, y el siguiente mensaje en la cola usa un proveedor de transporte diferentes, la cola MAPI puede empezar a procesar el mensaje posterior. Comienza el procesamiento bloqueando ese mensaje mediante el uso de **SetLockState**.
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Después de la cola MAPI ha llamado **SetLockState** con el parámetro _ulLockState_ establecido en MSG_LOCKED, se deben producir un error en las llamadas al método [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) para cancelar la transmisión del mensaje. 
  
Llamar al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) del mensaje en su implementación de **SetLockState** para que se guarden los cambios realizados en el mensaje antes de que se recibió la llamada **SetLockState** . 
  
## <a name="see-also"></a>Vea también



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

