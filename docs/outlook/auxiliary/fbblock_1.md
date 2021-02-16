---
title: FBBlock_1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: da67171d-d25f-3424-1409-33189ac63a12
description: Define un bloque de datos de disponibilidad. Se trata de un elemento de un calendario representado por una cita o una solicitud de reunión.
ms.openlocfilehash: 60d2ff50081a8950a397df6f2f6bbfd37d3bdb61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413202"
---
# <a name="fbblock_1"></a>FBBlock_1

Define un bloque de datos de disponibilidad. Se trata de un elemento de un calendario representado por una cita o una solicitud de reunión.
  
## <a name="quick-info"></a>Información rápida

```cpp
typedef struct  tagFBBlock_1 
    { 
    long m_tmStart; 
    long m_tmEnd; 
    FBStatus m_fbstatus; 
    }FBBlock_1; 

```

## <a name="members"></a>Miembros

_m_tmStart_
  
> La hora de inicio del bloque, expresada en tiempo relativo. Para obtener más información, vea [Usar tiempo relativo para obtener acceso a los datos de disponibilidad.](how-to-use-relative-time-to-access-free-busy-data.md)
    
_m_tmEnd_
  
> La hora de finalización del bloque, expresada en tiempo relativo.
    
_m_fbStatus_
  
> El estado de disponibilidad de este bloque, que indica si el usuario está fuera de la oficina, ocupado, provisional o libre, durante el período de tiempo entre  _m_tmStart_ y  _m_tmEnd_.
    
## <a name="see-also"></a>Consulte también

- [FBStatus](fbstatus.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)
- [Utilizar un tiempo relativo a los datos de disponibilidad de acceso](how-to-use-relative-time-to-access-free-busy-data.md)

