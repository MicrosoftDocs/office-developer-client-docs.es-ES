---
title: IOSTXInitSync
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.InitSync
api_type:
- COM
ms.assetid: e22244a2-ac5f-910a-501f-4483ea0667c2
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5a0632ffd892c08fdf19de2c9b34607c27534f19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594043"
---
# <a name="iostxinitsync"></a>IOSTX::InitSync

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Informa que el almacén de mensajes local que sincronización está a punto de inicio.
  
```cpp
HRESULT InitSync( 
    ULONG ulFlags 
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Marcas para determinar el comportamiento adecuado durante la sincronización. Outlook utiliza estos marcadores en cada estado de la máquina de estado de replicación para determinar la información que debe suministrar para el cliente. Por ejemplo, si el cliente pasa **SYNC_ONLY_ASSOCIATED**, Outlook solo devuelven información relacionada con los elementos asociados (u ocultos). 
    
## <a name="see-also"></a>Vea también



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes MAPI](mapi-constants.md)

