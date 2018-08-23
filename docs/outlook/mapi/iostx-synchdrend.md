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
ms.openlocfilehash: a40d4e62a930219a738c7b431f3d2192007c3d9d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591334"
---
# <a name="iostxsynchdrend"></a>IOSTX::SyncHdrEnd

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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
  
## <a name="see-also"></a>Recursos adicionales



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes MAPI](mapi-constants.md)

