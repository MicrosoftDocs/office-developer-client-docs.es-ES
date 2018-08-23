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
ms.openlocfilehash: f45b070464fe1b3c177088ff6aa3295f961d45f6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592594"
---
# <a name="ipstxgetlasterror"></a>IPSTX::GetLastError

  
  
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



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)

