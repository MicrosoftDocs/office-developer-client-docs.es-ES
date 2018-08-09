---
title: IEnumFBBlockSkip
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 70fbdb41-46ea-d016-25a2-37e94962095d
description: Omite un número especificado de bloques de datos de disponibilidad.
ms.openlocfilehash: 63f699d09e143a879702e8dc76beb8a969a77b82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816081"
---
# <a name="ienumfbblockskip"></a><span data-ttu-id="f9292-103">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="f9292-103">IEnumFBBlock::Skip</span></span>

<span data-ttu-id="f9292-104">Omite un número especificado de bloques de datos de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="f9292-104">Skips a specified number of blocks of free/busy data.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f9292-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="f9292-105">Quick info</span></span>

<span data-ttu-id="f9292-106">Vea [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="f9292-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Skip(  
    LONG celt 
);
```

## <a name="parameters"></a><span data-ttu-id="f9292-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f9292-107">Parameters</span></span>

<span data-ttu-id="f9292-108">_celt_</span><span class="sxs-lookup"><span data-stu-id="f9292-108">_celt_</span></span>
  
>  <span data-ttu-id="f9292-109">[entrada] El número de bloques de libre/ocupado para omitir.</span><span class="sxs-lookup"><span data-stu-id="f9292-109">[in] The number of free/busy blocks to skip.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="f9292-110">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="f9292-110">Return values</span></span>

<span data-ttu-id="f9292-111">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="f9292-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f9292-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9292-112">See also</span></span>

- [<span data-ttu-id="f9292-113">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="f9292-113">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="f9292-114">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="f9292-114">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="f9292-115">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="f9292-115">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="f9292-116">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="f9292-116">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)

