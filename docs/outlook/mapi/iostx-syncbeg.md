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
ms.openlocfilehash: ddc61aa42b1087ed5f0ecb7986125ceef27cddce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817839"
---
# <a name="iostxsyncbeg"></a>IOSTX::SyncBeg

  
  
**Hace referencia a**: Outlook 
  
Prepara el almacén local para la sincronización en un estado determinado y recupera la información necesaria para replicar.
  
```cpp
HRESULT SyncBeg( 
    UINT uiSync, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a>Parámetros

 _uiSync_
  
>  [entrada] El estado que se especifique el almacén local. La siguiente es una lista de identificadores de estado: 
    
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
  
>  [en] / [salida] puntero a la estructura de datos correspondiente al estado para escribir. 
    
[DNHIER](dnhier.md)
  
> 
    
[DNTBL](dntbl.md)
  
> 
    
[DNTBL](dntbl.md)
  
> 
    
[SYNC](sync.md)
  
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

El cliente llama a **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** para establecer el resultado de la sincronización y, a continuación, llama a **[IOSTX::SyncEnd](iostx-syncend.md)** para finalizar ese estado. El cliente debe llamar a **[IOSTX::SyncEnd](iostx-syncend.md)** para que cada llamada a **IOSTX::SyncBeg** con el fin de determinar si el estado se ha replicado correctamente. Una vez que se ha determinado, Outlook puede empezar a limpiar su estado interno. 
  
La mayoría de estas estructuras contienen [out] o [in] información, lo que permite a Outlook pasar información para el cliente y el cliente para pasar información a Outlook. Cuando el cliente llama a **IOSTX::SyncBeg**, Outlook asigna la estructura de datos para un estado determinado y lo inicializa con información de ese estado. Se trata de la información [out]. Mientras está en un estado, el cliente actualiza la estructura de datos correspondiente para ese estado. Este es el [de] información. 
  
## <a name="see-also"></a>Vea también



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes MAPI](mapi-constants.md)

