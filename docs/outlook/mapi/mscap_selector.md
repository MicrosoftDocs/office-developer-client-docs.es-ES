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
ms.openlocfilehash: 8c23788d64fe3703c7c46998cade0bd40d2f3dd2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588128"
---
# <a name="mscapselector"></a>MSCAP_SELECTOR

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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

## <a name="members"></a>Members

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
    

