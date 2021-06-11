---
title: IEnumFBBlockNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b46358c-bcab-f097-8746-fabfd4722b3c
description: Obtiene el siguiente número especificado de bloques de datos de disponibilidad en una enumeración.
ms.openlocfilehash: f6ec49a9bac6bcf4fff67991d55c7656f6c8cce2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422141"
---
# <a name="ienumfbblocknext"></a><span data-ttu-id="cc8f6-103">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="cc8f6-103">IEnumFBBlock::Next</span></span>

<span data-ttu-id="cc8f6-104">Obtiene el siguiente número especificado de bloques de datos de disponibilidad en una enumeración.</span><span class="sxs-lookup"><span data-stu-id="cc8f6-104">Gets the next specified number of blocks of free/busy data in an enumeration.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="cc8f6-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="cc8f6-105">Quick info</span></span>

<span data-ttu-id="cc8f6-106">Vea [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="cc8f6-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Next(  
        LONG celt,
        FBBlock_1 *pblk,
        LONG *pcfetch
);
```

## <a name="parameters"></a><span data-ttu-id="cc8f6-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="cc8f6-107">Parameters</span></span>

<span data-ttu-id="cc8f6-108">_celta_</span><span class="sxs-lookup"><span data-stu-id="cc8f6-108">_celt_</span></span>
  
> <span data-ttu-id="cc8f6-109">[in] Número de bloques de datos de disponibilidad en  *pblk*  que se recuperarán.</span><span class="sxs-lookup"><span data-stu-id="cc8f6-109">[in] The number of free/busy data blocks in  *pblk*  to retrieve.</span></span> 
    
<span data-ttu-id="cc8f6-110">_pblk_</span><span class="sxs-lookup"><span data-stu-id="cc8f6-110">_pblk_</span></span>
  
> <span data-ttu-id="cc8f6-111">[in] Puntero a una matriz de bloques de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="cc8f6-111">[in] A pointer to an array of free/busy blocks.</span></span> <span data-ttu-id="cc8f6-112">A la matriz se le asigna un tamaño de *celta.*</span><span class="sxs-lookup"><span data-stu-id="cc8f6-112">The array is allocated a size of  *celt*  .</span></span> <span data-ttu-id="cc8f6-113">Los bloques de disponibilidad solicitados se devuelven en esta matriz.</span><span class="sxs-lookup"><span data-stu-id="cc8f6-113">The requested free/busy blocks are returned in this array.</span></span> 
    
<span data-ttu-id="cc8f6-114">_pcfetch_</span><span class="sxs-lookup"><span data-stu-id="cc8f6-114">_pcfetch_</span></span>
  
> <span data-ttu-id="cc8f6-115">[salida] El número de bloques de disponibilidad devueltos realmente en  *pblk*  .</span><span class="sxs-lookup"><span data-stu-id="cc8f6-115">[out] The number of free/busy blocks actually returned in  *pblk*  .</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="cc8f6-116">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="cc8f6-116">Return values</span></span>

|<span data-ttu-id="cc8f6-117">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="cc8f6-117">**HRESULT**</span></span>|<span data-ttu-id="cc8f6-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="cc8f6-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cc8f6-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="cc8f6-119">S_OK</span></span>  <br/> |<span data-ttu-id="cc8f6-120">Se ha devuelto el número de bloques solicitado.</span><span class="sxs-lookup"><span data-stu-id="cc8f6-120">The requested number of blocks has been returned.</span></span>  <br/> |
|<span data-ttu-id="cc8f6-121">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="cc8f6-121">S_FALSE</span></span>  <br/> |<span data-ttu-id="cc8f6-122">No se ha devuelto el número de bloques solicitado.</span><span class="sxs-lookup"><span data-stu-id="cc8f6-122">The requested number of blocks has not been returned.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cc8f6-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc8f6-123">See also</span></span>

- [<span data-ttu-id="cc8f6-124">Constantes (API de disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="cc8f6-124">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)  
- [<span data-ttu-id="cc8f6-125">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="cc8f6-125">FBBlock_1</span></span>](fbblock_1.md)  
- [<span data-ttu-id="cc8f6-126">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="cc8f6-126">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="cc8f6-127">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="cc8f6-127">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="cc8f6-128">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="cc8f6-128">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)  
- [<span data-ttu-id="cc8f6-129">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="cc8f6-129">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)

