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
ms.openlocfilehash: 6b57ed45e067ce2debd40e033d386ad2b5ae895a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568521"
---
# <a name="followupstatus"></a>FollowUpStatus

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="see-also"></a>Recursos adicionales



[Propiedad canónica PidTagFlagStatus](pidtagflagstatus-canonical-property.md)

