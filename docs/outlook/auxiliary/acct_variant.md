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
# <a name="acctvariant"></a><span data-ttu-id="0cba9-103">ACCT_VARIANT</span><span class="sxs-lookup"><span data-stu-id="0cba9-103">ACCT_VARIANT</span></span>

<span data-ttu-id="0cba9-104">Una variable de este tipo de datos contiene el valor de una propiedad, que es un tipo de datos Variant.</span><span class="sxs-lookup"><span data-stu-id="0cba9-104">A variable of this data type holds the value of a property, which is of a variant data type.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="0cba9-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="0cba9-105">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="0cba9-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="0cba9-106">Members</span></span>

<span data-ttu-id="0cba9-107">_dwType_</span><span class="sxs-lookup"><span data-stu-id="0cba9-107">_dwType_</span></span>
  
> <span data-ttu-id="0cba9-108">Tipo de variante:</span><span class="sxs-lookup"><span data-stu-id="0cba9-108">Type of variant:</span></span>
    
    - <span data-ttu-id="0cba9-109">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0cba9-109">PT_LONG</span></span>
    
    - <span data-ttu-id="0cba9-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0cba9-110">PT_UNICODE</span></span>
    
    - <span data-ttu-id="0cba9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0cba9-111">PT_BINARY</span></span>
    
<span data-ttu-id="0cba9-112">_DW_</span><span class="sxs-lookup"><span data-stu-id="0cba9-112">_dw_</span></span>
  
> <span data-ttu-id="0cba9-113">Valor DWORD de Variant.</span><span class="sxs-lookup"><span data-stu-id="0cba9-113">DWORD value of variant.</span></span>
    
<span data-ttu-id="0cba9-114">_pwsz_</span><span class="sxs-lookup"><span data-stu-id="0cba9-114">_pwsz_</span></span>
  
> <span data-ttu-id="0cba9-115">Valor de cadena de Variant.</span><span class="sxs-lookup"><span data-stu-id="0cba9-115">String value of variant.</span></span>
    
<span data-ttu-id="0cba9-116">_definido_</span><span class="sxs-lookup"><span data-stu-id="0cba9-116">_bin_</span></span>
  
> <span data-ttu-id="0cba9-117">Valor binario de Variant.</span><span class="sxs-lookup"><span data-stu-id="0cba9-117">Binary value of the variant.</span></span>
    

