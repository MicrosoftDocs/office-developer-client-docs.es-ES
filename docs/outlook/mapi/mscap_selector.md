---
title: MSCAP_SELECTOR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f28ac144-f5ac-fd83-2b72-8d6e5fd74b6e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9c5d8ab5bbac91250f3b8c552ad891c62134526e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417206"
---
# <a name="mscap_selector"></a>MSCAP_SELECTOR

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica las capacidades que se devolverán para un almacén.
  
## <a name="quick-info"></a>Información rápida

```cpp
typedef enum 
{ 
    MSCAP_SEL_RESERVED1 = 0, 
    MSCAP_SEL_RESERVED2, 
    MSCAP_SEL_FOLDER, 
    MSCAP_SEL_RESERVED3, 
    MSCAP_SEL_RESTRICTION, 
} MSCAP_SELECTOR;
```

## <a name="members"></a>Miembros

 *MSCAP_SEL_RESERVED1* 
  
> Este miembro está reservado para el uso interno de Outlook y no es compatible. 
    
 *MSCAP_SEL_RESERVED2* 
  
> Este miembro está reservado para el uso interno de Outlook y no es compatible. 
    
 *MSCAP_SEL_FOLDER* 
  
> Funcionalidades sobre la compatibilidad de carpetas en un almacén.
    
 *MSCAP_SEL_RESERVED3* 
  
> Este miembro está reservado para el uso interno de Outlook y no es compatible. 
    
 *MSCAP_SEL_RESTRICTION* 
  
> Funcionalidades sobre cómo admitir restricciones en un almacén.
    

