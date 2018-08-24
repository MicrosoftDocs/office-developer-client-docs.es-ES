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
ms.openlocfilehash: 079b54757cfcd5c9b38365abc5a6d901e2b06724
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580722"
---
# <a name="ipstxemulatespooler"></a>IPSTX::EmulateSpooler

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Establece un almacén local para emular al administrador de protocolos de Outlook para poner en cola los mensajes salientes a un servidor.
  
```cpp
HRESULT EmulateSpooler( 
    BOOL fEmulate 
);
```

 _fEmulate_
  
>  [entrada] Establezca este parámetro en True si el almacén local debe emular la cola de impresión; establézcalo en False si no. 
    
## <a name="remarks"></a>Comentarios

Un almacén local llama a **IPSTX::EmulateSpooler** para que actúe como un Outlook protocolo administrador, los mensajes de la cola de impresión en la cola de salida para el servidor back-end (por ejemplo, el servidor MSN o AOL) para el procesamiento. El almacén de emula un administrador de cola durante la sincronización, a continuación, llama a estos dos métodos: 
  
1. **[IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** para obtener la cola de mensajes saliente en el almacén. Este método se ejecuta correctamente sólo si el almacén de emula al administrador de protocolos de Outlook. 
    
2. **[IMsgStore::SetLockState](imsgstore-setlockstate.md)** para proteger el acceso exclusivo a un mensaje en la cola de salida justo antes de enviar al servidor. Este método se ejecuta correctamente sólo si el almacén de emula al administrador de protocolos de Outlook. Después de enviar el mensaje, el almacén de llama a este método nuevo para liberar el único acceso a ella. 
    
> [!NOTE]
> Con respecto a Outlook 2002, el Administrador de protocolos de Outlook reemplaza a la cola MAPI y se convirtió en responsable para los mensajes salientes de puesta en cola de los servidores back-end. 
  
## <a name="see-also"></a>Vea también



[IPSTX::GetLastError](ipstx-getlasterror.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)

