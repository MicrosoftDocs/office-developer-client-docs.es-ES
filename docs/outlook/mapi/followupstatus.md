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
ms.openlocfilehash: 2280ae9271ca73af33f395bf9e41a9ee8fa62f96
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418333"
---
# <a name="followupstatus"></a>FollowUpStatus

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica los distintos Estados de seguimiento de un mensaje.
  
## <a name="quick-info"></a>Información rápida

```cpp
enum FollowUpStatus { 
    flwupNone = 0, 
    flwupComplete, 
    flwupMarked, 
    flwupMAX}; 

```

## <a name="members"></a>Miembros

 _flwupNone_
  
> No se ha especificado ningún seguimiento.
    
 _flwupComplete_
  
> El mensaje se ha completado.
    
 _flwupMarked_
  
> El mensaje se marca para seguimiento.
    
 _flwupMAX_
  
> El número de diferentes Estados admitidos para el seguimiento.
    
## <a name="see-also"></a>Ver también



[Propiedad canónica PidTagFlagStatus](pidtagflagstatus-canonical-property.md)

