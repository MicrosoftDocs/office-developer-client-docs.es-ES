---
title: ACCT_BIN
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5b57296c-61d7-e517-7ab7-44a9cc1f7ffc
description: Una variable de este tipo de datos contiene un valor binario.
ms.openlocfilehash: 3dcaaf73a04ddc608e68ca7bd1f801d0a5d99bb6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316915"
---
# <a name="acctbin"></a><span data-ttu-id="8f546-103">ACCT_BIN</span><span class="sxs-lookup"><span data-stu-id="8f546-103">ACCT_BIN</span></span>

<span data-ttu-id="8f546-104">Una variable de este tipo de datos contiene un valor binario.</span><span class="sxs-lookup"><span data-stu-id="8f546-104">A variable of this data type holds a binary value.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8f546-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="8f546-105">Quick info</span></span>

```cpp
typedef struct { 
    DWORDcb; 
    BYTE * pb; 
} ACCT_BIN; 

```

## <a name="members"></a><span data-ttu-id="8f546-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="8f546-106">Members</span></span>

<span data-ttu-id="8f546-107">_cb_</span><span class="sxs-lookup"><span data-stu-id="8f546-107">_cb_</span></span>
  
> <span data-ttu-id="8f546-108">Número de bytes que apunta a _PB_ .</span><span class="sxs-lookup"><span data-stu-id="8f546-108">Number of bytes that  _pb_ points to.</span></span> 
    
<span data-ttu-id="8f546-109">_pb_</span><span class="sxs-lookup"><span data-stu-id="8f546-109">_pb_</span></span>
  
> <span data-ttu-id="8f546-110">Puntero a información binaria.</span><span class="sxs-lookup"><span data-stu-id="8f546-110">Pointer to binary information.</span></span>
    

