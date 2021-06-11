---
title: IPSTX2SetSpoolSuspendState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX2.SetSpoolSuspendState
api_type:
- COM
ms.assetid: 396db029-1d4a-203d-2256-3353d03c6767
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e988114e8e71ad1f80d20ab0d5a30c37425f5952
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407518"
---
# <a name="ipstx2setspoolsuspendstate"></a>IPSTX2::SetSpoolSuspendState

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Establece el estado suspendido en la cola.
  
```cpp
void SetSpoolSuspendState( 
    ULONG ulState 
);
```

## <a name="parameters"></a>Parameters

 _ulState_
  
> [in] Estado en el que se va a establecer la cola. Debe ser uno de los siguientes valores:
    
 **SS_ACTIVE**
  
> 
    
 **SS_SUSPENDED**
  
> 
    
## <a name="see-also"></a>Vea también



[Constantes MAPI](mapi-constants.md)

