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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408127"
---
# <a name="acct_bin"></a><span data-ttu-id="0911b-103">ACCT_BIN</span><span class="sxs-lookup"><span data-stu-id="0911b-103">ACCT_BIN</span></span>

<span data-ttu-id="0911b-104">Una variable de este tipo de datos contiene un valor binario.</span><span class="sxs-lookup"><span data-stu-id="0911b-104">A variable of this data type holds a binary value.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="0911b-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="0911b-105">Quick info</span></span>

```cpp
typedef struct { 
    DWORDcb; 
    BYTE * pb; 
} ACCT_BIN; 

```

## <a name="members"></a><span data-ttu-id="0911b-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="0911b-106">Members</span></span>

<span data-ttu-id="0911b-107">_cb_</span><span class="sxs-lookup"><span data-stu-id="0911b-107">_cb_</span></span>
  
> <span data-ttu-id="0911b-108">Número de bytes a los _que apunta pb._</span><span class="sxs-lookup"><span data-stu-id="0911b-108">Number of bytes that  _pb_ points to.</span></span> 
    
<span data-ttu-id="0911b-109">_pb_</span><span class="sxs-lookup"><span data-stu-id="0911b-109">_pb_</span></span>
  
> <span data-ttu-id="0911b-110">Puntero a la información binaria.</span><span class="sxs-lookup"><span data-stu-id="0911b-110">Pointer to binary information.</span></span>
    

