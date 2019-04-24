---
title: IOlkEnumSkip
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e83e409c-f201-df9d-5e30-879adf15318d
description: Omite un número de cuentas especificado en el enumerador.
ms.openlocfilehash: d4063b0ff4852e6932cf50789eea3caa81d4d586
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321990"
---
# <a name="iolkenumskip"></a><span data-ttu-id="72cf8-103">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="72cf8-103">IOlkEnum::Skip</span></span>

<span data-ttu-id="72cf8-104">Omite un número de cuentas especificado en el enumerador.</span><span class="sxs-lookup"><span data-stu-id="72cf8-104">Skips a specified number of accounts in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="72cf8-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="72cf8-105">Quick info</span></span>

<span data-ttu-id="72cf8-106">Consulte [IOlkEnum](iolkenum.md).</span><span class="sxs-lookup"><span data-stu-id="72cf8-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum::Skip(  
    DWORD cSkip 
);
```

## <a name="parameters"></a><span data-ttu-id="72cf8-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="72cf8-107">Parameters</span></span>

<span data-ttu-id="72cf8-108">_cSkip_</span><span class="sxs-lookup"><span data-stu-id="72cf8-108">_cSkip_</span></span>
  
> <span data-ttu-id="72cf8-109">a Número de cuentas que se deben omitir.</span><span class="sxs-lookup"><span data-stu-id="72cf8-109">[in] The number of accounts to be skipped.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="72cf8-110">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="72cf8-110">Return values</span></span>

<span data-ttu-id="72cf8-111">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="72cf8-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="72cf8-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="72cf8-112">See also</span></span>

- [<span data-ttu-id="72cf8-113">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="72cf8-113">IOlkEnum::GetCount</span></span>](iolkenum-getcount.md) 
- [<span data-ttu-id="72cf8-114">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="72cf8-114">IOlkEnum::GetNext</span></span>](iolkenum-getnext.md)  
- [<span data-ttu-id="72cf8-115">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="72cf8-115">IOlkEnum::Reset</span></span>](iolkenum-reset.md)

