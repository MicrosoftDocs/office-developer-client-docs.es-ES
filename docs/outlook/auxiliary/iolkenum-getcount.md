---
title: IOlkEnumGetCount
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dd7a7e62-4cf2-bdd3-8a00-4fff5ac575d3
description: Obtiene el número de cuentas en el enumerador.
ms.openlocfilehash: dd4152a898bdaa96883bcd27ab3ec0d94e80fd90
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816247"
---
# <a name="iolkenumgetcount"></a><span data-ttu-id="d9c30-103">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="d9c30-103">IOlkEnum::GetCount</span></span>

<span data-ttu-id="d9c30-104">Obtiene el número de cuentas en el enumerador.</span><span class="sxs-lookup"><span data-stu-id="d9c30-104">Gets the number of accounts in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d9c30-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="d9c30-105">Quick info</span></span>

<span data-ttu-id="d9c30-106">Vea [IOlkEnum](iolkenum.md).</span><span class="sxs-lookup"><span data-stu-id="d9c30-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum::GetCount ( 
    DWORD *pulCount 
);

```

## <a name="parameters"></a><span data-ttu-id="d9c30-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d9c30-107">Parameters</span></span>

<span data-ttu-id="d9c30-108">_pulCount_</span><span class="sxs-lookup"><span data-stu-id="d9c30-108">_pulCount_</span></span>
  
> <span data-ttu-id="d9c30-109">[out] Un puntero para el número de objetos que se enumeran.</span><span class="sxs-lookup"><span data-stu-id="d9c30-109">[out] A pointer to the number of objects being enumerated.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="d9c30-110">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="d9c30-110">Return values</span></span>

<span data-ttu-id="d9c30-111">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="d9c30-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d9c30-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9c30-112">See also</span></span>

- [<span data-ttu-id="d9c30-113">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="d9c30-113">IOlkEnum::GetNext</span></span>](iolkenum-getnext.md)  
- [<span data-ttu-id="d9c30-114">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="d9c30-114">IOlkEnum::Reset</span></span>](iolkenum-reset.md) 
- [<span data-ttu-id="d9c30-115">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="d9c30-115">IOlkEnum::Skip</span></span>](iolkenum-skip.md)

