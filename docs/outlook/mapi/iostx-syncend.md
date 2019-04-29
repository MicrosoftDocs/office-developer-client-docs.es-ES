---
title: IOSTXSyncEnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncEnd
api_type:
- COM
ms.assetid: da9de705-bdab-6cb8-35ea-61f03cdc4ff5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 364914df1c5897241dfeb89cce2cc3c62018ce24
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439579"
---
# <a name="iostxsyncend"></a>IOSTX::SyncEnd

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Finaliza la sincronización en el estado actual y sale de ese estado.
  
```cpp
HRESULT SyncEnd();
```

## <a name="remarks"></a>Comentarios

El cliente debe llamar a **IOSTX:: SyncEnd** para cada llamada a [IOSTX:: SyncBeg](iostx-syncbeg.md). La estructura de datos correspondiente retiene información para indicar si el cliente ha completado correctamente el estado actual para que Outlook pueda limpiar su estado interno.
  
## <a name="see-also"></a>Ver también



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes MAPI](mapi-constants.md)

