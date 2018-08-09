---
title: FBStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f2d6a11e-847d-6bbe-cd77-e78ee961cb12
description: Una enumeración para el estado libre/ocupado de bloques de libre/ocupado.
ms.openlocfilehash: 67d710f82856dc8ff4839c926018eef88d355f73
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/21/2018
ms.locfileid: "19816070"
---
# <a name="fbstatus"></a>FBStatus

Una enumeración para el estado libre/ocupado de bloques de libre/ocupado.
  
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

El estado de disponibilidad de un bloque de tiempo determina cómo se muestra en un calendario: **libre**, **ocupado**, **provisional**o **Fuera de la oficina**. 
  
## <a name="see-also"></a>Vea también

- [FBBlock_1](fbblock_1.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)

