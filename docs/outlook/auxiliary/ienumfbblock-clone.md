---
title: IEnumFBBlockClone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5af36a87-e782-df63-4190-a608758fef50
description: Crea una copia del enumerador, utilizando la misma restricción de tiempo, pero estableciendo el cursor en el principio del enumerador.
ms.openlocfilehash: 1a279430bf6a29611fa223bebbf8023c34967139
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317601"
---
# <a name="ienumfbblockclone"></a><span data-ttu-id="33ad5-103">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="33ad5-103">IEnumFBBlock::Clone</span></span>

<span data-ttu-id="33ad5-104">Crea una copia del enumerador, utilizando la misma restricción de tiempo, pero estableciendo el cursor en el principio del enumerador.</span><span class="sxs-lookup"><span data-stu-id="33ad5-104">Creates a copy of the enumerator, using the same time restriction but setting the cursor to the beginning of the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="33ad5-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="33ad5-105">Quick info</span></span>

<span data-ttu-id="33ad5-106">Consulte [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="33ad5-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Clone(  
     IEnumFBBlock **ppclone 
); 
```

## <a name="parameters"></a><span data-ttu-id="33ad5-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="33ad5-107">Parameters</span></span>

<span data-ttu-id="33ad5-108">_ppclone_</span><span class="sxs-lookup"><span data-stu-id="33ad5-108">_ppclone_</span></span>
  
> <span data-ttu-id="33ad5-109">contempla Un puntero a puntero a la copia de la interfaz de [IEnumFBBlock](ienumfbblock.md) .</span><span class="sxs-lookup"><span data-stu-id="33ad5-109">[out] A pointer to pointer to the copy of [IEnumFBBlock](ienumfbblock.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="33ad5-110">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="33ad5-110">Return values</span></span>

|<span data-ttu-id="33ad5-111">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="33ad5-111">**HRESULT**</span></span>|<span data-ttu-id="33ad5-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="33ad5-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="33ad5-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="33ad5-113">S_OK</span></span>  <br/> |<span data-ttu-id="33ad5-114">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="33ad5-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="33ad5-115">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="33ad5-115">E_OUTOFMEMORY</span></span>  <br/> |<span data-ttu-id="33ad5-116">Memoria insuficiente para realizar la copia.</span><span class="sxs-lookup"><span data-stu-id="33ad5-116">There is insufficient memory for making the copy.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="33ad5-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="33ad5-117">See also</span></span>

- [<span data-ttu-id="33ad5-118">Constantes (API de disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="33ad5-118">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)
- [<span data-ttu-id="33ad5-119">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="33ad5-119">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="33ad5-120">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="33ad5-120">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="33ad5-121">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="33ad5-121">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)  
- [<span data-ttu-id="33ad5-122">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="33ad5-122">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)

