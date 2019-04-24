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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338678"
---
# <a name="mscapselector"></a>MSCAP_SELECTOR

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica las funciones que se van a devolver para un almacén.
  
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
  
> Este miembro está reservado para uso interno de Outlook y no es compatible. 
    
 *MSCAP_SEL_RESERVED2* 
  
> Este miembro está reservado para uso interno de Outlook y no es compatible. 
    
 *MSCAP_SEL_FOLDER* 
  
> Funcionalidades sobre carpetas auxiliares en un almacén.
    
 *MSCAP_SEL_RESERVED3* 
  
> Este miembro está reservado para uso interno de Outlook y no es compatible. 
    
 *MSCAP_SEL_RESTRICTION* 
  
> Capacidades para admitir restricciones en un almacén.
    

