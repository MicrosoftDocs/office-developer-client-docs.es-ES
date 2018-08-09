---
title: IOlkEnumSkip
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e83e409c-f201-df9d-5e30-879adf15318d
description: Omite un número especificado de cuentas en el enumerador.
ms.openlocfilehash: 2791f1204cedf5e91d13923e50dfc45b981b7e26
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816240"
---
# <a name="iolkenumskip"></a><span data-ttu-id="4bcae-103">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="4bcae-103">IOlkEnum::Skip</span></span>

<span data-ttu-id="4bcae-104">Omite un número especificado de cuentas en el enumerador.</span><span class="sxs-lookup"><span data-stu-id="4bcae-104">Skips a specified number of accounts in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4bcae-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="4bcae-105">Quick info</span></span>

<span data-ttu-id="4bcae-106">Vea [IOlkEnum](iolkenum.md).</span><span class="sxs-lookup"><span data-stu-id="4bcae-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum::Skip(  
    DWORD cSkip 
);
```

## <a name="parameters"></a><span data-ttu-id="4bcae-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4bcae-107">Parameters</span></span>

<span data-ttu-id="4bcae-108">_cSkip_</span><span class="sxs-lookup"><span data-stu-id="4bcae-108">_cSkip_</span></span>
  
> <span data-ttu-id="4bcae-109">[entrada] El número de cuentas que se pasan por alto.</span><span class="sxs-lookup"><span data-stu-id="4bcae-109">[in] The number of accounts to be skipped.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="4bcae-110">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="4bcae-110">Return values</span></span>

<span data-ttu-id="4bcae-111">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="4bcae-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4bcae-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="4bcae-112">See also</span></span>

- [<span data-ttu-id="4bcae-113">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="4bcae-113">IOlkEnum::GetCount</span></span>](iolkenum-getcount.md) 
- [<span data-ttu-id="4bcae-114">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="4bcae-114">IOlkEnum::GetNext</span></span>](iolkenum-getnext.md)  
- [<span data-ttu-id="4bcae-115">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="4bcae-115">IOlkEnum::Reset</span></span>](iolkenum-reset.md)

