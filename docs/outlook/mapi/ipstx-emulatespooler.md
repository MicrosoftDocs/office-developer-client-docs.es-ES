---
title: IPSTXEmulateSpooler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX.EmulateSpooler
api_type:
- COM
ms.assetid: aec72e51-1f75-b2c5-76ca-626cd21fbc7d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 024583926b5d0be638b33b1b60c5d4c5dc74d05b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438956"
---
# <a name="ipstxemulatespooler"></a>IPSTX::EmulateSpooler

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Establece un almacén local para emular el Administrador de protocolo de Outlook para colar mensajes salientes en un servidor.
  
```cpp
HRESULT EmulateSpooler( 
    BOOL fEmulate 
);
```

 _fEmulate_
  
>  [entrada] Establezca este parámetro en True si el almacén local debe emular la cola; se establece en False si no es así. 
    
## <a name="remarks"></a>Comentarios

Un almacén local llama a **IPSTX::EmulateSpooler** para que actúe como administrador de protocolo de Outlook, y pone en cola los mensajes de la cola saliente en el servidor back-end (por ejemplo, servidor MSN o servidor AOL) para su procesamiento. Emulando una cola durante la sincronización, el almacén llama a estos dos métodos: 
  
1. **[IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** para obtener la cola saliente de mensajes en el almacén. Este método solo se realiza correctamente si el almacén emula el Administrador de protocolo de Outlook. 
    
2. **[IMsgStore::SetLockState](imsgstore-setlockstate.md)** para proteger el acceso único a un mensaje en la cola saliente justo antes de enviarlo al servidor. Este método solo se realiza correctamente si el almacén emula el Administrador de protocolo de Outlook. Después de enviar el mensaje, el almacén llama de nuevo a este método para liberar el acceso único a él. 
    
> [!NOTE]
> Desde Outlook 2002, el Administrador de protocolo de Outlook reemplazó la cola MAPI y se hizo responsable de poner en cola los mensajes salientes en servidores back-end. 
  
## <a name="see-also"></a>Consulte también



[IPSTX::GetLastError](ipstx-getlasterror.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)

