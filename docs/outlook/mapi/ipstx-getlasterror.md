---
title: IPSTXGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX.GetLastError
api_type:
- COM
ms.assetid: 68dc0ecc-881e-de69-faaa-90acb9857031
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 1d0fb16ba63548a44dba3920670c0e65f8c700a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414980"
---
# <a name="ipstxgetlasterror"></a>IPSTX::GetLastError

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Obtiene información extendida sobre el último error.
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a>Parameters

 _hResult_
  
>  [in] Código de error. 
    
 _ulFlags_
  
>  [entrada] Marcadores para modificar el comportamiento. Debe ser 0. 
    
 _lppMAPIError_
  
>  [salida] Puntero a la **estructura MAPIERROR** que contiene la información extendida del error. Vea mapidefs.h para obtener la definición de tipo **de LPMAPIERROR**. 
    
## <a name="see-also"></a>Vea también



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)

