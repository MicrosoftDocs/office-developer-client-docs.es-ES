---
title: IOlkEnumGetCount
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dd7a7e62-4cf2-bdd3-8a00-4fff5ac575d3
description: Obtiene el número de cuentas del enumerador.
ms.openlocfilehash: 8571d5ff01501d980c8b6543607a658ad99085ca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421826"
---
# <a name="iolkenumgetcount"></a><span data-ttu-id="344f8-103">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="344f8-103">IOlkEnum::GetCount</span></span>

<span data-ttu-id="344f8-104">Obtiene el número de cuentas del enumerador.</span><span class="sxs-lookup"><span data-stu-id="344f8-104">Gets the number of accounts in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="344f8-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="344f8-105">Quick info</span></span>

<span data-ttu-id="344f8-106">Vea [IOlkEnum](iolkenum.md).</span><span class="sxs-lookup"><span data-stu-id="344f8-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum::GetCount ( 
    DWORD *pulCount 
);

```

## <a name="parameters"></a><span data-ttu-id="344f8-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="344f8-107">Parameters</span></span>

<span data-ttu-id="344f8-108">_pulCount_</span><span class="sxs-lookup"><span data-stu-id="344f8-108">_pulCount_</span></span>
  
> <span data-ttu-id="344f8-109">[salida] Puntero al número de objetos que se enumeran.</span><span class="sxs-lookup"><span data-stu-id="344f8-109">[out] A pointer to the number of objects being enumerated.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="344f8-110">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="344f8-110">Return values</span></span>

<span data-ttu-id="344f8-111">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="344f8-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="344f8-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="344f8-112">See also</span></span>

- [<span data-ttu-id="344f8-113">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="344f8-113">IOlkEnum::GetNext</span></span>](iolkenum-getnext.md)  
- [<span data-ttu-id="344f8-114">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="344f8-114">IOlkEnum::Reset</span></span>](iolkenum-reset.md) 
- [<span data-ttu-id="344f8-115">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="344f8-115">IOlkEnum::Skip</span></span>](iolkenum-skip.md)

