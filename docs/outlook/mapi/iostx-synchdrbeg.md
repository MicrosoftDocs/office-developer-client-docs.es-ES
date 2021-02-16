---
title: IOSTXSyncHdrBeg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncHdrBeg
api_type:
- COM
ms.assetid: 7f8ca7cf-ac0b-9b77-c1dd-9f1d0871d603
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 49ef9862d5156a1bed242652df32baab9a0123fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405096"
---
# <a name="iostxsynchdrbeg"></a>IOSTX::SyncHdrBeg

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Inicia la sincronización de un encabezado de mensaje.
  
```cpp
HRESULT SyncHdrBeg( 
    ULONG cbeid, 
    LPENTRYID lpeid, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a>Parámetros

 _cgnid_
  
> [entrada] El número de bytes del identificador de entrada del mensaje.
    
 _lpeid_
  
> [entrada] Identificador de entrada del mensaje.
    
 _ppv_
  
>  [entrada]/[salida] Puntero a la estructura **[HDRSYNC](hdrsync.md)** del encabezado del mensaje. 
    
## <a name="remarks"></a>Comentarios

En **IOSTX::SyncHdrBeg,** el almacén local pasa al estado de encabezado [del mensaje de descarga.](download-message-header-state.md) Outlook inicializa para el cliente la estructura **HDRSYNC** con la representación actual del encabezado del mensaje en el almacén y la carpeta principal. A continuación, el cliente debe descargar un elemento de mensaje completo  *(como pmsgFull*  en **HDRSYNC** ). Si se ha realizado correctamente, el cliente también establece  *ulFlags*  en **HDRSYNC** **como HSF_OK**. En **[IOSTX::SyncHdrEnd,](iostx-synchdrend.md)** Outlook comprueba el resultado en **HDRSYNC** y usa la información de **HDRSYNC** para actualizar el encabezado del mensaje local. 
  
## <a name="see-also"></a>Consulte también



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes MAPI](mapi-constants.md)

