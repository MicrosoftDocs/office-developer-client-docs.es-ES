---
title: ACCT_VARIANT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4664df83-cf81-36d4-189d-4a09be371638
description: Una variable de este tipo de datos contiene el valor de una propiedad, que es de un tipo de datos variant.
ms.openlocfilehash: c85af4bd4fefffb4fadf671bb7cf5b7f072d5e95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816057"
---
# <a name="acctvariant"></a>ACCT_VARIANT

Una variable de este tipo de datos contiene el valor de una propiedad, que es de un tipo de datos variant.
  
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

## <a name="members"></a>Members

_dwType_
  
> Tipo de variante:
    
    - PT_LONG
    
    - PT_UNICODE
    
    - PT_BINARY
    
_DW_
  
> Valor DWORD de variante.
    
_pwsz_
  
> Valor de tipo variant de cadena.
    
_Papelera de_
  
> Valor binario de la variante.
    

