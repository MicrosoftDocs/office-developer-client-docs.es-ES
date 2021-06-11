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
description: 'Last modified: July 03, 2012'
ms.openlocfilehash: 864c2d2dfd17c285b0d8a401d59ce5b7d0463864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432775"
---
# <a name="iostxsynchdrend"></a>IOSTX::SyncHdrEnd

 
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Finaliza la sincronización de un encabezado de mensaje.
  
```cpp
HRESULT SyncHdrEnd( 
    LPMAPIPROGRESS pprog 
);
```

## <a name="parameters"></a>Parameters

 _pprog_
  
> [in] **[Interfaz IMAPIProgress](imapiprogressiunknown.md)** para la sincronización de mensajes movidos o copiados. Vea mapidefs.h para obtener la definición de tipo **de LPMAPIPROGRESS**. 
    
## <a name="remarks"></a>Comentarios

Tras **[IOSTX::SyncBeg,](iostx-syncbeg.md)** el almacén local escribe el estado de encabezado [del mensaje de descarga](download-message-header-state.md). El cliente descarga un elemento de mensaje completo  *(como pmsgFull*  en **[HDRSYNC](hdrsync.md)** ). Si se realiza correctamente, el cliente también establece  *ulFlags*  en **HDRSYNC** como **HSF_OK**. En **IOSTX::SyncHdrEnd,** Outlook comprueba el resultado en **HDRSYNC** y usa *pprog* y la información de **HDRSYNC** para actualizar el encabezado del mensaje local. 
  
El almacén local vuelve al estado en el que estaba antes del **[IOSTX::SyncHdrBeg anterior.](iostx-synchdrbeg.md)** 
  
## <a name="see-also"></a>Vea también



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes MAPI](mapi-constants.md)

