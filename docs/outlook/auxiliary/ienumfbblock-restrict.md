---
title: IEnumFBBlockRestrict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 887cea55-8f1c-45ec-3100-d03e1213d7c9
description: Restringe la enumeración a un período de tiempo especificado.
ms.openlocfilehash: e7f7a5d846d13422f9ed79ef26f1b9b0008463f6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431949"
---
# <a name="ienumfbblockrestrict"></a><span data-ttu-id="79b22-103">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="79b22-103">IEnumFBBlock::Restrict</span></span>

<span data-ttu-id="79b22-104">Restringe la enumeración a un período de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="79b22-104">Restricts the enumeration to a specified time period.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="79b22-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="79b22-105">Quick info</span></span>

<span data-ttu-id="79b22-106">Vea [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="79b22-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Restrict(  
    FILETIME ftmStart, 
    FILETIME ftmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="79b22-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="79b22-107">Parameters</span></span>

<span data-ttu-id="79b22-108">_ftmStart_</span><span class="sxs-lookup"><span data-stu-id="79b22-108">_ftmStart_</span></span>
  
>  <span data-ttu-id="79b22-109">[in] Hora de inicio para restringir la enumeración.</span><span class="sxs-lookup"><span data-stu-id="79b22-109">[in] The start time to restrict the enumeration.</span></span> 
    
<span data-ttu-id="79b22-110">_ftmEnd_</span><span class="sxs-lookup"><span data-stu-id="79b22-110">_ftmEnd_</span></span>
  
> <span data-ttu-id="79b22-111">[in] Hora de finalización para restringir la enumeración.</span><span class="sxs-lookup"><span data-stu-id="79b22-111">[in] The end time to restrict the enumeration.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="79b22-112">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="79b22-112">Return values</span></span>

<span data-ttu-id="79b22-113">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="79b22-113">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="79b22-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="79b22-114">Remarks</span></span>

<span data-ttu-id="79b22-115">Este método también restablece la enumeración.</span><span class="sxs-lookup"><span data-stu-id="79b22-115">This method also resets the enumeration.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="79b22-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="79b22-116">See also</span></span>

- [<span data-ttu-id="79b22-117">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="79b22-117">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="79b22-118">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="79b22-118">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="79b22-119">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="79b22-119">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="79b22-120">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="79b22-120">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)  
- [<span data-ttu-id="79b22-121">Utilizar un tiempo relativo a los datos de disponibilidad de acceso</span><span class="sxs-lookup"><span data-stu-id="79b22-121">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

