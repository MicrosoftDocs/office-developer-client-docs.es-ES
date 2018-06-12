---
title: EXCHANGE_STORE_VERSION_NUM
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 88950eda-85ae-ad7a-46c6-0e1933d35e04
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 00d92f8e2ec3af766d5b241d1a911be304b346d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816771"
---
# <a name="exchangestoreversionnum"></a>EXCHANGE_STORE_VERSION_NUM

  
  
**Se aplica a**: Outlook 
  
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

## <a name="members"></a>Miembros

 _wMajorVersion_
  
- Número de versión principal que generalmente se incrementa cuando una versión contiene importantes nuevas características y cambios en la funcionalidad.
    
 _wMinorVersion_
  
- Número de versión secundaria que corresponde a un número específico de versión principal y que generalmente se incrementa cuando una versión contiene nuevas características secundarias o revisiones importantes.
    
 _wBuild_
  
- Número de compilación principal que corresponde a los números de versión principal y secundaria específica y que generalmente se incrementa en una versión interna que contiene las nuevas características o revisiones. Este valor también se incrementa cuando la versión es una bifurcación de código interno principales o hito, como un candidato de versión comercial.
    
 _wMinorBuild_
  
- Número de compilación secundaria que generalmente se incrementa en una versión interna que contiene las nuevas características o corrige correspondiente a una compilación principal específica que indica un hito o una sucursal de código principal.
    
## <a name="see-also"></a>Ver también



[Acerca de las adiciones de MAPI](about-mapi-additions.md)
  
[Propiedad canónico PidTagProfileServerFullVersion](pidtagprofileserverfullversion-canonical-property.md)

