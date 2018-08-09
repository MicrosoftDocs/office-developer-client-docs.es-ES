---
title: IEnumFBBlockRestrict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 887cea55-8f1c-45ec-3100-d03e1213d7c9
description: Restringe la enumeración a un período de tiempo especificado.
ms.openlocfilehash: 6b07fe52a84d6a808ab7400ff3e8982b1cce51ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816079"
---
# <a name="ienumfbblockrestrict"></a><span data-ttu-id="e5f78-103">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="e5f78-103">IEnumFBBlock::Restrict</span></span>

<span data-ttu-id="e5f78-104">Restringe la enumeración a un período de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="e5f78-104">Restricts the enumeration to a specified time period.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e5f78-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="e5f78-105">Quick info</span></span>

<span data-ttu-id="e5f78-106">Vea [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="e5f78-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Restrict(  
    FILETIME ftmStart, 
    FILETIME ftmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="e5f78-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e5f78-107">Parameters</span></span>

<span data-ttu-id="e5f78-108">_ftmStart_</span><span class="sxs-lookup"><span data-stu-id="e5f78-108">_ftmStart_</span></span>
  
>  <span data-ttu-id="e5f78-109">[entrada] La hora de inicio para restringir la enumeración.</span><span class="sxs-lookup"><span data-stu-id="e5f78-109">[in] The start time to restrict the enumeration.</span></span> 
    
<span data-ttu-id="e5f78-110">_ftmEnd_</span><span class="sxs-lookup"><span data-stu-id="e5f78-110">_ftmEnd_</span></span>
  
> <span data-ttu-id="e5f78-111">[entrada] La hora de finalización para restringir la enumeración.</span><span class="sxs-lookup"><span data-stu-id="e5f78-111">[in] The end time to restrict the enumeration.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="e5f78-112">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="e5f78-112">Return values</span></span>

<span data-ttu-id="e5f78-113">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="e5f78-113">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e5f78-114">Notas</span><span class="sxs-lookup"><span data-stu-id="e5f78-114">Remarks</span></span>

<span data-ttu-id="e5f78-115">Este método también restablece la enumeración.</span><span class="sxs-lookup"><span data-stu-id="e5f78-115">This method also resets the enumeration.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e5f78-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="e5f78-116">See also</span></span>

- [<span data-ttu-id="e5f78-117">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="e5f78-117">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="e5f78-118">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="e5f78-118">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="e5f78-119">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="e5f78-119">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="e5f78-120">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="e5f78-120">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)  
- [<span data-ttu-id="e5f78-121">Utilizar un tiempo relativo a los datos de disponibilidad de acceso</span><span class="sxs-lookup"><span data-stu-id="e5f78-121">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

