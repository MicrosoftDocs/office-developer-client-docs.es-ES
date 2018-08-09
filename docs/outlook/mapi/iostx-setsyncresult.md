---
title: IOSTXSetSyncResult
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SetSyncResult
api_type:
- COM
ms.assetid: 7f083ee0-bf36-0059-1589-66e454fe0098
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 74a4e299da6c0637c3da70c329569266d43dbd9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817840"
---
# <a name="iostxsetsyncresult"></a>IOSTX::SetSyncResult

  
  
**Hace referencia a**: Outlook 
  
Establece el resultado de la sincronización.
  
```cpp
HRESULT SetSyncResult( 
    HRESULT hrSync 
);
```

## <a name="parameters"></a>Parámetros

 _hrSync_
  
>  [entrada] El resultado de la sincronización. 
    
## <a name="remarks"></a>Comentarios

Llame a **IOSTX::SetSyncResult** antes de llamar a **IOSTX::SyncEnd** para informar el almacén local del resultado de la sincronización. 
  
## <a name="see-also"></a>Vea también



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)


[Constantes MAPI](mapi-constants.md)

