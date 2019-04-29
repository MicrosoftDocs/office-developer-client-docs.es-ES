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
  
> a Un puntero al mensaje que se va a bloquear o desbloquear.
    
 _ulLockState_
  
> a Un valor que indica si el mensaje debe estar bloqueado o desbloqueado. Uno de los siguientes valores es válido:
    
MSG_LOCKED 
  
> El mensaje debe estar bloqueado. 
    
MSG_UNLOCKED 
  
> El mensaje debe estar desbloqueado.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El estado de bloqueo del mensaje se estableció correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMsgStore:: SetLockState** bloquea o desbloquea un mensaje. Solo puede llamar a **SetLockState** la cola MAPI mientras envía el mensaje. 
  
Normalmente, cuando la cola MAPI llama a **SetLockState** para bloquear un mensaje, bloquea sólo el mensaje más antiguo (es decir, el siguiente mensaje que se pone en cola para que lo envíe la cola MAPI). Si el mensaje más antiguo de la cola está esperando a un proveedor de transporte no disponible temporalmente y el siguiente mensaje de la cola usa un proveedor de transporte diferente, la cola MAPI puede empezar a procesar el mensaje posterior. Comienza el procesamiento bloqueando el mensaje mediante **SetLockState**.
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Una vez que la cola MAPI llamó a **SetLockState** con el parámetro _ULLOCKSTATE_ establecido en MSG_LOCKED, las llamadas al método [IMsgStore:: AbortSubmit](imsgstore-abortsubmit.md) para cancelar la transmisión del mensaje deben producir un error. 
  
Llame al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) del mensaje en la implementación de **SetLockState** para que se guarden todos los cambios realizados en el mensaje antes de que se haya recibido la llamada **SetLockState** . 
  
## <a name="see-also"></a>Ver también



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

