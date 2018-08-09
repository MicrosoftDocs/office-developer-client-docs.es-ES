---
title: FollowUpStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c3d0f6c4-4597-784f-8d44-6e5d905895b4
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e59c0ba7810741943883b9e86e84c6fe141f3050
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816838"
---
# <a name="followupstatus"></a>FollowUpStatus

  
  
**Hace referencia a**: Outlook 
  
Especifica los diferentes Estados de seguimiento para un mensaje.
  
## <a name="quick-info"></a>Información rápida

```cpp
enum FollowUpStatus { 
    flwupNone = 0, 
    flwupComplete, 
    flwupMarked, 
    flwupMAX}; 

```

## <a name="members"></a>Members

 _flwupNone_
  
> No se ha especificado ningún seguimiento.
    
 _flwupComplete_
  
> El mensaje está completado.
    
 _flwupMarked_
  
> El mensaje está marcado para su seguimiento.
    
 _flwupMAX_
  
> El número de diferentes estados compatibles para su seguimiento.
    
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagFlagStatus](pidtagflagstatus-canonical-property.md)

