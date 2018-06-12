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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 66542d2cc7600ecbcd8de9043b6b40559744c2ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817849"
---
# <a name="iostxsyncend"></a>IOSTX::SyncEnd

  
  
**Se aplica a**: Outlook 
  
Finaliza la sincronización en el estado actual y sale de ese estado.
  
```cpp
HRESULT SyncEnd();
```

## <a name="remarks"></a>Notas

El cliente debe llamar a **IOSTX::SyncEnd** para cada llamada a [IOSTX::SyncBeg](iostx-syncbeg.md). La estructura de datos correspondiente contiene información para indicar si el cliente ha completado correctamente el estado actual para que Outlook puede limpiar su estado interno.
  
## <a name="see-also"></a>Ver también



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::Initsync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX: IUnknown](iostxiunknown.md)


[Constantes MAPI](mapi-constants.md)

