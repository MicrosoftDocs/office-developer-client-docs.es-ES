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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315095"
---
# <a name="ipstxemulatespooler"></a>IPSTX::EmulateSpooler

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Establece un almacén local para emular el administrador de protocolos de Outlook para poner en cola los mensajes salientes a un servidor.
  
```cpp
HRESULT EmulateSpooler( 
    BOOL fEmulate 
);
```

 _fEmulate_
  
>  a Establezca este parámetro en true si el almacén local debe emular la cola de impresión; de lo contrario, establézcalo en false. 
    
## <a name="remarks"></a>Comentarios

Un almacén local llama a **IPSTX:: EmulateSpooler** para actuar como administrador de protocolos de Outlook, poniendo en cola los mensajes de la cola de salida en el servidor back-end (por ejemplo, MSN Server o AOL Server) para su procesamiento. Emular una cola de impresión durante la sincronización, el almacén llama a estos dos métodos: 
  
1. **[IMsgStore:: GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** para obtener la cola de salida de mensajes en el almacén. Este método se ejecuta correctamente sólo si el almacén está emulando el administrador de protocolos de Outlook. 
    
2. **[IMsgStore:: SetLockState](imsgstore-setlockstate.md)** para proteger el acceso único a un mensaje en la cola de salida justo antes de enviarlo al servidor. Este método se ejecuta correctamente sólo si el almacén está emulando el administrador de protocolos de Outlook. Después de enviar el mensaje, el almacén llama de nuevo a este método para liberar el acceso único al mismo. 
    
> [!NOTE]
> Desde Outlook 2002, el administrador de protocolos de Outlook reemplazó la cola de espera de MAPI y se convirtió en poner en cola los mensajes salientes a los servidores back-end. 
  
## <a name="see-also"></a>Vea también



[IPSTX::GetLastError](ipstx-getlasterror.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)

