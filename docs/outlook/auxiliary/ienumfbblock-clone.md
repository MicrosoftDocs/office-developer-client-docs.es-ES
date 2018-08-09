---
title: IEnumFBBlockClone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5af36a87-e782-df63-4190-a608758fef50
description: Crea una copia del enumerador, utilizando la misma restricción de tiempo pero establecer el cursor al principio del enumerador.
ms.openlocfilehash: 51503be2091fa01da6f636bf6944274068617f05
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816082"
---
# <a name="ienumfbblockclone"></a><span data-ttu-id="8cf32-103">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="8cf32-103">IEnumFBBlock::Clone</span></span>

<span data-ttu-id="8cf32-104">Crea una copia del enumerador, utilizando la misma restricción de tiempo pero establecer el cursor al principio del enumerador.</span><span class="sxs-lookup"><span data-stu-id="8cf32-104">Creates a copy of the enumerator, using the same time restriction but setting the cursor to the beginning of the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8cf32-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="8cf32-105">Quick info</span></span>

<span data-ttu-id="8cf32-106">Vea [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="8cf32-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Clone(  
     IEnumFBBlock **ppclone 
); 
```

## <a name="parameters"></a><span data-ttu-id="8cf32-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8cf32-107">Parameters</span></span>

<span data-ttu-id="8cf32-108">_ppclone_</span><span class="sxs-lookup"><span data-stu-id="8cf32-108">_ppclone_</span></span>
  
> <span data-ttu-id="8cf32-109">[out] Un puntero a un puntero a la copia de la interfaz de [IEnumFBBlock](ienumfbblock.md) .</span><span class="sxs-lookup"><span data-stu-id="8cf32-109">[out] A pointer to pointer to the copy of [IEnumFBBlock](ienumfbblock.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="8cf32-110">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="8cf32-110">Return values</span></span>

|<span data-ttu-id="8cf32-111">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="8cf32-111">**HRESULT**</span></span>|<span data-ttu-id="8cf32-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="8cf32-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8cf32-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="8cf32-113">S_OK</span></span>  <br/> |<span data-ttu-id="8cf32-114">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="8cf32-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="8cf32-115">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="8cf32-115">E_OUTOFMEMORY</span></span>  <br/> |<span data-ttu-id="8cf32-116">Hay suficiente memoria para realizar la copia.</span><span class="sxs-lookup"><span data-stu-id="8cf32-116">There is insufficient memory for making the copy.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8cf32-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="8cf32-117">See also</span></span>

- [<span data-ttu-id="8cf32-118">Constantes (API de libre/ocupado)</span><span class="sxs-lookup"><span data-stu-id="8cf32-118">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)
- [<span data-ttu-id="8cf32-119">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="8cf32-119">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="8cf32-120">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="8cf32-120">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="8cf32-121">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="8cf32-121">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)  
- [<span data-ttu-id="8cf32-122">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="8cf32-122">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)

