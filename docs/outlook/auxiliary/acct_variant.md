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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424402"
---
# <a name="acctvariant"></a><span data-ttu-id="9658c-103">ACCT_VARIANT</span><span class="sxs-lookup"><span data-stu-id="9658c-103">ACCT_VARIANT</span></span>

<span data-ttu-id="9658c-104">Una variable de este tipo de datos contiene el valor de una propiedad, que es un tipo de datos Variant.</span><span class="sxs-lookup"><span data-stu-id="9658c-104">A variable of this data type holds the value of a property, which is of a variant data type.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9658c-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="9658c-105">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="9658c-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="9658c-106">Members</span></span>

<span data-ttu-id="9658c-107">_dwType_</span><span class="sxs-lookup"><span data-stu-id="9658c-107">_dwType_</span></span>
  
> <span data-ttu-id="9658c-108">Tipo de variante:</span><span class="sxs-lookup"><span data-stu-id="9658c-108">Type of variant:</span></span>
    
    - <span data-ttu-id="9658c-109">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9658c-109">PT_LONG</span></span>
    
    - <span data-ttu-id="9658c-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9658c-110">PT_UNICODE</span></span>
    
    - <span data-ttu-id="9658c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9658c-111">PT_BINARY</span></span>
    
<span data-ttu-id="9658c-112">_DW_</span><span class="sxs-lookup"><span data-stu-id="9658c-112">_dw_</span></span>
  
> <span data-ttu-id="9658c-113">Valor DWORD de Variant.</span><span class="sxs-lookup"><span data-stu-id="9658c-113">DWORD value of variant.</span></span>
    
<span data-ttu-id="9658c-114">_pwsz_</span><span class="sxs-lookup"><span data-stu-id="9658c-114">_pwsz_</span></span>
  
> <span data-ttu-id="9658c-115">Valor de cadena de Variant.</span><span class="sxs-lookup"><span data-stu-id="9658c-115">String value of variant.</span></span>
    
<span data-ttu-id="9658c-116">_definido_</span><span class="sxs-lookup"><span data-stu-id="9658c-116">_bin_</span></span>
  
> <span data-ttu-id="9658c-117">Valor binario de Variant.</span><span class="sxs-lookup"><span data-stu-id="9658c-117">Binary value of the variant.</span></span>
    

