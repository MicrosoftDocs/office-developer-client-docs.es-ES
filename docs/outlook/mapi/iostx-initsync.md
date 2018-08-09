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
ms.openlocfilehash: 07305f712fd925b206ce18a32f8f5a24f199ccbf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817838"
---
# <a name="iostxinitsync"></a>IOSTX::InitSync

  
  
**Hace referencia a**: Outlook 
  
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

