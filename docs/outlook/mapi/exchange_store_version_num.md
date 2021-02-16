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
# <a name="exchange_store_version_num"></a>EXCHANGE_STORE_VERSION_NUM

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Almacena información de versión para el Microsoft Exchange Server al que están conectadas las Microsoft Office Outlook de un perfil.
  
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
  
- Número de versión principal que generalmente se incrementa cuando una versión contiene nuevas características y cambios significativos en la funcionalidad.
    
 _wMinorVersion_
  
- Número de versión secundaria que corresponde a un número de versión principal específico y que generalmente se incrementa cuando una versión contiene nuevas características secundarias o correcciones significativas.
    
 _wBuild_
  
- Número de compilación principal que corresponde a números de versión principales y secundarias específicos y que generalmente se incrementa en una versión interna que contiene nuevas características o correcciones. Este valor también se incrementa cuando la versión es una rama o hito de código interno importante, como un candidato de versión.
    
 _wMinorBuild_
  
- Número de compilación secundaria que generalmente se incrementa en una versión interna que contiene nuevas características o correcciones correspondientes a una compilación principal específica que denota una rama o hito de código principal.
    
## <a name="see-also"></a>Vea también



[Acerca de las adiciones de MAPI](about-mapi-additions.md)
  
[Propiedad canónica PidTagProfileServerFullVersion](pidtagprofileserverfullversion-canonical-property.md)

