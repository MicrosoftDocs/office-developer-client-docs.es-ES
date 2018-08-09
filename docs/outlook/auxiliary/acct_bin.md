---
title: ACCT_BIN
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5b57296c-61d7-e517-7ab7-44a9cc1f7ffc
description: Una variable de este tipo de datos contiene un valor binario.
ms.openlocfilehash: 6816fd21a51b86bda97353034e959685f22ff176
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816065"
---
# <a name="acctbin"></a>ACCT_BIN

Una variable de este tipo de datos contiene un valor binario.
  
## <a name="quick-info"></a>Información rápida

```cpp
typedef struct { 
    DWORDcb; 
    BYTE * pb; 
} ACCT_BIN; 

```

## <a name="members"></a>Members

_cb_
  
> Número de bytes que _pb_ apunta a. 
    
_pb_
  
> Puntero a información binaria.
    

