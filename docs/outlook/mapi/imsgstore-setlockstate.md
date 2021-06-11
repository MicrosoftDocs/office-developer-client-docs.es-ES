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
ms.openlocfilehash: 9eeede2a430f5186daf429dd6ed59f312ae334be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423632"
---
# <a name="imsgstoresetlockstate"></a>IMsgStore::SetLockState

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Bloquea o desbloquea un mensaje. Se llama a este m�todo s�lo por la cola MAPI.
  
```cpp
HRESULT SetLockState(
  LPMESSAGE lpMessage,
  ULONG ulLockState  
);
```

## <a name="parameters"></a>Parameters

 _lpMessage_
  
> [in] Puntero al mensaje para bloquear o desbloquear.
    
 _ulLockState_
  
> [in] Valor que indica si el mensaje debe bloquearse o desbloquearse. Uno de los siguientes valores es válido:
    
MSG_LOCKED 
  
> El mensaje debe estar bloqueado. 
    
MSG_UNLOCKED 
  
> El mensaje debe estar desbloqueado.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El estado de bloqueo del mensaje se estableció correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IMsgStore::SetLockState** bloquea o desbloquea un mensaje. **SetLockState** solo se puede llamar mediante la cola MAPI mientras envía el mensaje. 
  
Normalmente, cuando la cola MAPI llama a **SetLockState** para bloquear un mensaje, solo bloquea el mensaje más antiguo (es decir, el siguiente mensaje en cola para que la cola MAPI envíe). Si el mensaje más antiguo de la cola está esperando un proveedor de transporte temporalmente no disponible y el siguiente mensaje de la cola usa un proveedor de transporte diferente, la cola MAPI puede comenzar a procesar el mensaje posterior. Se inicia el procesamiento bloqueando ese mensaje mediante **SetLockState**.
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Después de que la cola MAPI haya llamado **a SetLockState** con el parámetro  _ulLockState_ establecido en MSG_LOCKED, las llamadas al método [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) para cancelar la transmisión del mensaje deben producir un error. 
  
Llame al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) del mensaje en la implementación **SetLockState** para que se guarden los cambios realizados en el mensaje antes de recibir la llamada **SetLockState.** 
  
## <a name="see-also"></a>Vea también



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

