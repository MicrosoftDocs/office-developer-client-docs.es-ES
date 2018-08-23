---
title: IOSTXGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.GetLastError
api_type:
- COM
ms.assetid: b25c9288-b391-6303-3643-5a5b66b75c48
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 78ae0f78e154c17f774817238b2083d98a8fb809
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584684"
---
# <a name="iostxgetlasterror"></a>IOSTX::GetLastError

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Obtiene información sobre el último error ampliada.
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a>Parámetros

 _hResult_
  
>  [entrada] Código de error. 
    
 _ulFlags_
  
>  [entrada] Marcadores para modificar el comportamiento. Esto debe ser 0. 
    
 _lppMAPIError_
  
>  [out] Puntero a la estructura **MAPIERROR** que contiene la información extendida para el error. Vea mapidefs.h para la definición de tipo de **LPMAPIERROR**. 
    
## <a name="see-also"></a>Recursos adicionales



[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes MAPI](mapi-constants.md)

