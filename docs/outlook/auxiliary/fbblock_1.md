---
title: FBBlock_1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: da67171d-d25f-3424-1409-33189ac63a12
description: Define un bloque libre/ocupado de datos. Esto es un elemento en un calendario representado por una convocatoria de reunión o cita.
ms.openlocfilehash: 93418e3777e9d9f0a016822ea5897b8fccc37ac3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816059"
---
# <a name="fbblock1"></a>FBBlock_1

Define un bloque libre/ocupado de datos. Esto es un elemento en un calendario representado por una convocatoria de reunión o cita.
  
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
  
> La hora de inicio para el bloque, expresado en hora relativa. Para obtener más información, vea [usar la hora relativa para tener acceso a datos de disponibilidad](how-to-use-relative-time-to-access-free-busy-data.md).
    
_m_tmEnd_
  
> La hora de finalización para el bloque, expresado en hora relativa.
    
_m_fbStatus_
  
> El estado de disponibilidad de este bloque, que indica si el usuario está fuera de la oficina, ocupado, provisional o libre, durante el período de tiempo entre _m_tmStart_ y _m_tmEnd_.
    
## <a name="see-also"></a>Ver también

- [FBStatus](fbstatus.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)
- [Usar tiempo relativa a los datos de libre/ocupado de access](how-to-use-relative-time-to-access-free-busy-data.md)

