---
title: IOSTXSyncBeg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncBeg
api_type:
- COM
ms.assetid: 4a935df3-98c4-2742-206e-4e16eda7b9bc
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ae4497295328155780fc5208d1699169698e02d8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317174"
---
# <a name="iostxsyncbeg"></a>IOSTX::SyncBeg

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Prepara el almacén local para la sincronización en un estado concreto y recupera la información necesaria para replicar.
  
```cpp
HRESULT SyncBeg( 
    UINT uiSync, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a>Parameters

 _uiSync_
  
>  a El estado que escribirá el almacén local. A continuación se muestra una lista de los identificadores de estado: 
    
LR_SYNC_IDLE
  
> 
    
LR_SYNC
  
> 
    
LR_SYNC_UPLOAD_HIERARCHY
  
> 
    
LR_SYNC_UPLOAD_FOLDER
  
> 
    
LR_SYNC_CONTENTS
  
> 
    
LR_SYNC_UPLOAD_TABLE
  
> 
    
LR_SYNC_UPLOAD_MESSAGE
  
> 
    
LR_SYNC_UPLOAD_MESSAGE_READ
  
> 
    
LR_SYNC_UPLOAD_MESSAGE_DEL
  
> 
    
LR_SYNC_DOWNLOAD_HIERARCHY
  
> 
    
LR_SYNC_DOWNLOAD_TABLE
  
> 
    
 _PPV_
  
>  [entrada]/[salida] puntero a la estructura de datos correspondiente al estado que se va a escribir. 
    
[DNHIER](dnhier.md)
  
> 
    
[DNTBL](dntbl.md)
  
> 
    
[DNTBL](dntbl.md)
  
> 
    
[SINCRONIZÁNDOSE](sync.md)
  
> 
    
[SYNCCONT](synccont.md)
  
> 
    
[UPDEL](updel.md)
  
> 
    
[UPDELE](updele.md)
  
> 
    
[UPFLD](upfld.md)
  
> 
    
[UPHIER](uphier.md)
  
> 
    
[UPMOV](upmov.md)
  
> 
    
[UPMSG](upmsg.md)
  
> 
    
[UPREAD](upread.md)
  
> 
    
[UPREADE](upreade.md)
  
> 
    
[UPTBL](uptbl.md)
  
> 
    
[UPTBLE](uptble.md)
  
> 
    
## <a name="remarks"></a>Comentarios

El cliente llama a **[IOSTX:: SetSyncResult](iostx-setsyncresult.md)** para establecer el resultado de la sincronización y, a continuación, llama a **[IOSTX:: SyncEnd](iostx-syncend.md)** para finalizar ese estado. El cliente debe llamar a **[IOSTX:: SyncEnd](iostx-syncend.md)** para cada llamada a **IOSTX:: SyncBeg** con el fin de determinar si el estado se ha replicado correctamente. Una vez que se haya determinado esto, Outlook puede empezar a limpiar su estado interno. 
  
La mayoría de estas estructuras contienen información [out]/[in], lo que permite a Outlook pasar información al cliente y al cliente pasar información a Outlook. Cuando el cliente llama a **IOSTX:: SyncBeg**, Outlook asigna la estructura de datos para un estado determinado y lo inicializa con información para ese estado. Esta es la información de [salida]. Mientras se está en un estado, el cliente actualiza la estructura de datos correspondiente a ese estado. Esta es la información de [in]. 
  
## <a name="see-also"></a>Vea también



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes MAPI](mapi-constants.md)

