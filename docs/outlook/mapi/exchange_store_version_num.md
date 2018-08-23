---
title: EXCHANGE_STORE_VERSION_NUM
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 88950eda-85ae-ad7a-46c6-0e1933d35e04
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 152afd68bea44f3485b2cc566f3f0d2768590704
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594477"
---
# <a name="exchangestoreversionnum"></a>EXCHANGE_STORE_VERSION_NUM

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Almacena información de versión de Microsoft Exchange Server conectados a cuentas en un perfil de Microsoft Office Outlook.
  
## <a name="quick-info"></a>Información rápida

```cpp
typedef struct { 
    WORD wMajorVersion; 
    WORD wMinorVersion; 
    WORD wBuild; 
    WORD wMinorBuild; 
} EXCHANGE_STORE_VERSION_NUM; 

```

## <a name="members"></a>Members

 _wMajorVersion_
  
- Número de versión principal que generalmente se incrementa cuando una versión contiene importantes nuevas características y cambios en la funcionalidad.
    
 _wMinorVersion_
  
- Número de versión secundaria que corresponde a un número específico de versión principal y que generalmente se incrementa cuando una versión contiene nuevas características secundarias o revisiones importantes.
    
 _wBuild_
  
- Número de compilación principal que corresponde a los números de versión principal y secundaria específica y que generalmente se incrementa en una versión interna que contiene las nuevas características o revisiones. Este valor también se incrementa cuando la versión es una bifurcación de código interno principales o hito, como un candidato de versión comercial.
    
 _wMinorBuild_
  
- Número de compilación secundaria que generalmente se incrementa en una versión interna que contiene las nuevas características o corrige correspondiente a una compilación principal específica que indica un hito o una sucursal de código principal.
    
## <a name="see-also"></a>Recursos adicionales



[Información sobre las adiciones de MAPI](about-mapi-additions.md)
  
[Propiedad canónica PidTagProfileServerFullVersion](pidtagprofileserverfullversion-canonical-property.md)

