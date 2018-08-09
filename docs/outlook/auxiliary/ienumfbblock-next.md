---
title: IEnumFBBlockNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b46358c-bcab-f097-8746-fabfd4722b3c
description: Obtiene el siguiente número especificado de bloques de datos de disponibilidad en una enumeración.
ms.openlocfilehash: ec366cf102d3c75487f9485cfae7764d68695f10
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816088"
---
# <a name="ienumfbblocknext"></a><span data-ttu-id="4305f-103">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="4305f-103">IEnumFBBlock::Next</span></span>

<span data-ttu-id="4305f-104">Obtiene el siguiente número especificado de bloques de datos de disponibilidad en una enumeración.</span><span class="sxs-lookup"><span data-stu-id="4305f-104">Gets the next specified number of blocks of free/busy data in an enumeration.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4305f-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="4305f-105">Quick info</span></span>

<span data-ttu-id="4305f-106">Vea [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="4305f-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Next(  
        LONG celt,
        FBBlock_1 *pblk,
        LONG *pcfetch
);
```

## <a name="parameters"></a><span data-ttu-id="4305f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4305f-107">Parameters</span></span>

<span data-ttu-id="4305f-108">_celt_</span><span class="sxs-lookup"><span data-stu-id="4305f-108">_celt_</span></span>
  
> <span data-ttu-id="4305f-109">[entrada] El número de datos de disponibilidad se bloquea en *pblk* para recuperar.</span><span class="sxs-lookup"><span data-stu-id="4305f-109">[in] The number of free/busy data blocks in  *pblk*  to retrieve.</span></span> 
    
<span data-ttu-id="4305f-110">_PBLK_</span><span class="sxs-lookup"><span data-stu-id="4305f-110">_pblk_</span></span>
  
> <span data-ttu-id="4305f-111">[entrada] Un puntero a una matriz de bloques de libre/ocupado.</span><span class="sxs-lookup"><span data-stu-id="4305f-111">[in] A pointer to an array of free/busy blocks.</span></span> <span data-ttu-id="4305f-112">La matriz se asigna un tamaño de *celt* .</span><span class="sxs-lookup"><span data-stu-id="4305f-112">The array is allocated a size of  *celt*  .</span></span> <span data-ttu-id="4305f-113">Los bloques de libre/ocupado solicitados se devuelven en esta matriz.</span><span class="sxs-lookup"><span data-stu-id="4305f-113">The requested free/busy blocks are returned in this array.</span></span> 
    
<span data-ttu-id="4305f-114">_pcfetch_</span><span class="sxs-lookup"><span data-stu-id="4305f-114">_pcfetch_</span></span>
  
> <span data-ttu-id="4305f-115">[out] El número de bloques de libre/ocupado devueltos realmente en *pblk* .</span><span class="sxs-lookup"><span data-stu-id="4305f-115">[out] The number of free/busy blocks actually returned in  *pblk*  .</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="4305f-116">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="4305f-116">Return values</span></span>

|<span data-ttu-id="4305f-117">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="4305f-117">**HRESULT**</span></span>|<span data-ttu-id="4305f-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="4305f-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4305f-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="4305f-119">S_OK</span></span>  <br/> |<span data-ttu-id="4305f-120">Ha devuelto el número solicitado de bloques.</span><span class="sxs-lookup"><span data-stu-id="4305f-120">The requested number of blocks has been returned.</span></span>  <br/> |
|<span data-ttu-id="4305f-121">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="4305f-121">S_FALSE</span></span>  <br/> |<span data-ttu-id="4305f-122">El número de bloques de solicitado no ha devuelto.</span><span class="sxs-lookup"><span data-stu-id="4305f-122">The requested number of blocks has not been returned.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4305f-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="4305f-123">See also</span></span>

- [<span data-ttu-id="4305f-124">Constantes (API de libre/ocupado)</span><span class="sxs-lookup"><span data-stu-id="4305f-124">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)  
- [<span data-ttu-id="4305f-125">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="4305f-125">FBBlock_1</span></span>](fbblock_1.md)  
- [<span data-ttu-id="4305f-126">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="4305f-126">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="4305f-127">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="4305f-127">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="4305f-128">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="4305f-128">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)  
- [<span data-ttu-id="4305f-129">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="4305f-129">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)

