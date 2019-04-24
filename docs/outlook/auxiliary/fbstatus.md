---
title: FBStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f2d6a11e-847d-6bbe-cd77-e78ee961cb12
description: Enumeración para el estado de disponibilidad de los bloques de disponibilidad.
ms.openlocfilehash: 2a08ef142f9baddd453166c0ebcb989e69a51ceb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319729"
---
# <a name="fbstatus"></a>FBStatus

Enumeración para el estado de disponibilidad de los bloques de disponibilidad.
  
## <a name="quick-info"></a>Información rápida

```cpp
enum  
    { 
      fbFree      = 0, 
      fbTentative = fbFree + 1, 
      fbBusy      = fbTentative + 1, 
      fbOutOfOffice = fbBusy + 1 
    }

```

## <a name="remarks"></a>Comentarios

El estado de disponibilidad de un bloque de tiempo determina cómo se muestra en un calendario: **libre**, **ocupado**, **provisional**o **fuera de la oficina**. 
  
## <a name="see-also"></a>Vea también

- [FBBlock_1](fbblock_1.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)

