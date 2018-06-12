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
# <a name="acctbin"></a><span data-ttu-id="51d1b-103">ACCT_BIN</span><span class="sxs-lookup"><span data-stu-id="51d1b-103">ACCT_BIN</span></span>

<span data-ttu-id="51d1b-104">Una variable de este tipo de datos contiene un valor binario.</span><span class="sxs-lookup"><span data-stu-id="51d1b-104">A variable of this data type holds a binary value.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="51d1b-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="51d1b-105">Quick info</span></span>

```cpp
typedef struct { 
    DWORDcb; 
    BYTE * pb; 
} ACCT_BIN; 

```

## <a name="members"></a><span data-ttu-id="51d1b-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="51d1b-106">Members</span></span>

<span data-ttu-id="51d1b-107">_cb_</span><span class="sxs-lookup"><span data-stu-id="51d1b-107">_cb_</span></span>
  
> <span data-ttu-id="51d1b-108">Número de bytes que _pb_ apunta a.</span><span class="sxs-lookup"><span data-stu-id="51d1b-108">Number of bytes that  _pb_ points to.</span></span> 
    
<span data-ttu-id="51d1b-109">_pb_</span><span class="sxs-lookup"><span data-stu-id="51d1b-109">_pb_</span></span>
  
> <span data-ttu-id="51d1b-110">Puntero a información binaria.</span><span class="sxs-lookup"><span data-stu-id="51d1b-110">Pointer to binary information.</span></span>
    

