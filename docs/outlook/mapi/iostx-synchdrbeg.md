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
ms.openlocfilehash: 2d05592d1fdcdcd53c8b7879f9cdcd432df1a3f7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579469"
---
# <a name="iostxsynchdrbeg"></a>IOSTX::SyncHdrBeg

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Inicia la sincronización para un encabezado de mensaje.
  
```cpp
HRESULT SyncHdrBeg( 
    ULONG cbeid, 
    LPENTRYID lpeid, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a>Parámetros

 _cbeid_
  
> [entrada] El número de bytes en el identificador de entrada para el mensaje.
    
 _lpeid_
  
> [entrada] El identificador de entrada para el mensaje.
    
 _PPV_
  
>  [en] / [salida] puntero a la estructura **[HDRSYNC](hdrsync.md)** para el encabezado del mensaje. 
    
## <a name="remarks"></a>Comentarios

Una vez **IOSTX::SyncHdrBeg**, local almacenar transiciones para el [estado del encabezado de mensaje de descarga](download-message-header-state.md). Outlook inicializa para el cliente de la estructura **HDRSYNC** con la representación del encabezado del mensaje en el almacén y la carpeta primaria. El cliente, a continuación, debe descargar un elemento de mensaje completa (como *pmsgFull* en **HDRSYNC** ). Si se ha realizado correctamente, el cliente también establece *ulFlags* de **HDRSYNC** como **HSF_OK**. Una vez **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)**, Outlook comprueba el resultado en **HDRSYNC** y utiliza la información de **HDRSYNC** para actualizar el encabezado del mensaje local. 
  
## <a name="see-also"></a>Recursos adicionales



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes MAPI](mapi-constants.md)

