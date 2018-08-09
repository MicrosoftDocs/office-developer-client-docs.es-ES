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
ms.openlocfilehash: e061808c57f25f881cc17fa5251e46ed5d524acd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817953"
---
# <a name="ipstxgetlasterror"></a>IPSTX::GetLastError

  
  
**Hace referencia a**: Outlook 
  
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
    
## <a name="see-also"></a>Vea también



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)

