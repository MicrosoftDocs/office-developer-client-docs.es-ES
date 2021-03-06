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
ms.openlocfilehash: b9086383b45d40d5839284ac785d72438be60e00
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413356"
---
# <a name="iostxinitsync"></a>IOSTX::InitSync

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Informa al almacén de mensajes local de que la sincronización está a punto de iniciarse.
  
```cpp
HRESULT InitSync( 
    ULONG ulFlags 
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Marcas para determinar el comportamiento adecuado durante la sincronización. Outlook usa estas marcas en cada estado de la máquina de estado de replicación para determinar la información que debe proporcionar al cliente. Por ejemplo, si el cliente pasa SYNC_ONLY_ASSOCIATED **,** Outlook solo devolverá información relacionada con elementos asociados (u ocultos). 
    
## <a name="see-also"></a>Vea también



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes MAPI](mapi-constants.md)

