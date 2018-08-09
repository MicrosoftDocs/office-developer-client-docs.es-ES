---
title: IOSTXSyncHdrEnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncHdrEnd
api_type:
- COM
ms.assetid: a0beb6eb-7978-c64e-dba1-89f0caf2090e
description: 'Última modificación: 03 de julio de 2012'
ms.openlocfilehash: ee68052f330bf3239cd12139ffbd77f5a180f6cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817844"
---
# <a name="iostxsynchdrend"></a>IOSTX::SyncHdrEnd

 
  
**Hace referencia a**: Outlook 
  
Finaliza la sincronización para un encabezado de mensaje.
  
```cpp
HRESULT SyncHdrEnd( 
    LPMAPIPROGRESS pprog 
);
```

## <a name="parameters"></a>Parámetros

 _pprog_
  
> [entrada] Interfaz **[IMAPIProgress](imapiprogressiunknown.md)** para la sincronización de mover o copia mensajes. Vea mapidefs.h para la definición de tipo de **LPMAPIPROGRESS**. 
    
## <a name="remarks"></a>Comentarios

Una vez **[IOSTX::SyncBeg](iostx-syncbeg.md)**, el almacén local entra en el [estado del encabezado de mensaje de descarga](download-message-header-state.md). El cliente descarga un elemento de mensaje completa (como *pmsgFull* en **[HDRSYNC](hdrsync.md)** ). Si esto se realiza correctamente, el cliente establece también *ulFlags* en **HDRSYNC** como **HSF_OK**. Una vez **IOSTX::SyncHdrEnd**, Outlook comprueba el resultado en **HDRSYNC** y usa *pprog* y la información en **HDRSYNC** para actualizar el encabezado del mensaje local. 
  
El almacén local se devuelve al estado que tenía antes de la anterior **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)**. 
  
## <a name="see-also"></a>Vea también



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes MAPI](mapi-constants.md)

