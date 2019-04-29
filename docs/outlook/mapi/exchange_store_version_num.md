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
ms.openlocfilehash: bf60b12a6e4575d3504a112aa2b54fb8c4ae23c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433727"
---
# <a name="exchangestoreversionnum"></a>EXCHANGE_STORE_VERSION_NUM

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Almacena la información de versión del servidor de Microsoft Exchange al que están conectadas las cuentas de un perfil de Microsoft Office Outlook.
  
## <a name="quick-info"></a>Información rápida

```cpp
typedef struct { 
    WORD wMajorVersion; 
    WORD wMinorVersion; 
    WORD wBuild; 
    WORD wMinorBuild; 
} EXCHANGE_STORE_VERSION_NUM; 

```

## <a name="members"></a>Miembros

 _wMajorVersion_
  
- Número de versión principal que se suele incrementar cuando una versión contiene nuevas características importantes y cambios de funcionalidad.
    
 _wMinorVersion_
  
- Número de versión secundaria que corresponde a un número de versión principal específico y que, por lo general, se incrementa cuando una versión contiene nuevas características secundarias o correcciones significativas.
    
 _wBuild_
  
- Número de compilación principal que corresponde a números de versiones principales y secundarias específicas y que, por lo general, se incrementa en una versión interna que contiene nuevas características o correcciones. Este valor también se incrementa cuando el lanzamiento es una bifurcación de código interno principal o un hito como, por ejemplo, Release Candidate.
    
 _wMinorBuild_
  
- Número de compilación secundaria que suele incrementarse en una versión interna que contiene nuevas características o revisiones correspondientes a una compilación principal específica que denota una bifurcación de código principal o un hito.
    
## <a name="see-also"></a>Vea también



[Acerca de las adiciones de MAPI](about-mapi-additions.md)
  
[Propiedad canónica PidTagProfileServerFullVersion](pidtagprofileserverfullversion-canonical-property.md)

