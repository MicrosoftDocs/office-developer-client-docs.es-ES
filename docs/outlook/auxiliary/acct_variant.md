---
title: ACCT_VARIANT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4664df83-cf81-36d4-189d-4a09be371638
description: Una variable de este tipo de datos contiene el valor de una propiedad, que es un tipo de datos Variant.
ms.openlocfilehash: 124cfaef40e63d60e2e9c6681884bfb57a043dde
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316922"
---
# <a name="acctvariant"></a>ACCT_VARIANT

Una variable de este tipo de datos contiene el valor de una propiedad, que es un tipo de datos Variant.
  
## <a name="quick-info"></a>Información rápida

```cpp
typedef struct 
    { 
        DWORD dwType; 
        union  
            { 
            DWORD dw; 
            WCHAR *pwsz; 
            ACCT_BIN bin; 
            } Val; 
    } ACCT_VARIANT; 

```

## <a name="members"></a>Miembros

_dwType_
  
> Tipo de variante:
    
    - PT_LONG
    
    - PT_UNICODE
    
    - PT_BINARY
    
_DW_
  
> Valor DWORD de Variant.
    
_pwsz_
  
> Valor de cadena de Variant.
    
_definido_
  
> Valor binario de Variant.
    

