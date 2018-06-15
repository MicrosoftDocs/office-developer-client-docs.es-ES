---
title: MSCAP_SELECTOR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f28ac144-f5ac-fd83-2b72-8d6e5fd74b6e
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 420b2661e766ecf97a5e9e488e9c18f29cd91329
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19818399"
---
# <a name="mscapselector"></a>MSCAP_SELECTOR

  
  
**Se aplica a**: Outlook 
  
Especifica las funciones que se devuelven en un almacén.
  
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
  
> Este miembro está reservado para el uso interno de Outlook y no se admite. 
    
 *MSCAP_SEL_RESERVED2* 
  
> Este miembro está reservado para el uso interno de Outlook y no se admite. 
    
 *MSCAP_SEL_FOLDER* 
  
> Capacidades de acerca de la compatibilidad de las carpetas en un almacén.
    
 *MSCAP_SEL_RESERVED3* 
  
> Este miembro está reservado para el uso interno de Outlook y no se admite. 
    
 *MSCAP_SEL_RESTRICTION* 
  
> Capacidades de acerca de la compatibilidad de las restricciones en un almacén.
    

