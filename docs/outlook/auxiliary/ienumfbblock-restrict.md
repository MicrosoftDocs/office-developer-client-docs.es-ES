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
# <a name="ienumfbblockrestrict"></a><span data-ttu-id="4cc6f-103">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="4cc6f-103">IEnumFBBlock::Restrict</span></span>

<span data-ttu-id="4cc6f-104">Restringe la enumeración a un período de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="4cc6f-104">Restricts the enumeration to a specified time period.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4cc6f-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="4cc6f-105">Quick info</span></span>

<span data-ttu-id="4cc6f-106">Consulta [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="4cc6f-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Restrict(  
    FILETIME ftmStart, 
    FILETIME ftmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="4cc6f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4cc6f-107">Parameters</span></span>

<span data-ttu-id="4cc6f-108">_ftmStart_</span><span class="sxs-lookup"><span data-stu-id="4cc6f-108">_ftmStart_</span></span>
  
>  <span data-ttu-id="4cc6f-109">[entrada] Hora de inicio para restringir la enumeración.</span><span class="sxs-lookup"><span data-stu-id="4cc6f-109">[in] The start time to restrict the enumeration.</span></span> 
    
<span data-ttu-id="4cc6f-110">_ftmEnd_</span><span class="sxs-lookup"><span data-stu-id="4cc6f-110">_ftmEnd_</span></span>
  
> <span data-ttu-id="4cc6f-111">[entrada] Hora de finalización para restringir la enumeración.</span><span class="sxs-lookup"><span data-stu-id="4cc6f-111">[in] The end time to restrict the enumeration.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="4cc6f-112">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="4cc6f-112">Return values</span></span>

<span data-ttu-id="4cc6f-113">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="4cc6f-113">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4cc6f-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4cc6f-114">Remarks</span></span>

<span data-ttu-id="4cc6f-115">Este método también restablece la enumeración.</span><span class="sxs-lookup"><span data-stu-id="4cc6f-115">This method also resets the enumeration.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4cc6f-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4cc6f-116">See also</span></span>

- [<span data-ttu-id="4cc6f-117">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="4cc6f-117">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="4cc6f-118">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="4cc6f-118">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="4cc6f-119">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="4cc6f-119">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="4cc6f-120">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="4cc6f-120">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)  
- [<span data-ttu-id="4cc6f-121">Utilizar un tiempo relativo a los datos de disponibilidad de acceso</span><span class="sxs-lookup"><span data-stu-id="4cc6f-121">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

