---
title: IEnumFBBlockClone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5af36a87-e782-df63-4190-a608758fef50
description: Crea una copia del enumerador, con la misma restricción de tiempo pero estableciendo el cursor al principio del enumerador.
ms.openlocfilehash: 1a279430bf6a29611fa223bebbf8023c34967139
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413405"
---
# <a name="ienumfbblockclone"></a><span data-ttu-id="cf7d0-103">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="cf7d0-103">IEnumFBBlock::Clone</span></span>

<span data-ttu-id="cf7d0-104">Crea una copia del enumerador, con la misma restricción de tiempo pero estableciendo el cursor al principio del enumerador.</span><span class="sxs-lookup"><span data-stu-id="cf7d0-104">Creates a copy of the enumerator, using the same time restriction but setting the cursor to the beginning of the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="cf7d0-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="cf7d0-105">Quick info</span></span>

<span data-ttu-id="cf7d0-106">Consulta [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="cf7d0-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Clone(  
     IEnumFBBlock **ppclone 
); 
```

## <a name="parameters"></a><span data-ttu-id="cf7d0-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cf7d0-107">Parameters</span></span>

<span data-ttu-id="cf7d0-108">_ppclone_</span><span class="sxs-lookup"><span data-stu-id="cf7d0-108">_ppclone_</span></span>
  
> <span data-ttu-id="cf7d0-109">[salida] Puntero a la copia de la interfaz [IEnumFBBlock.](ienumfbblock.md)</span><span class="sxs-lookup"><span data-stu-id="cf7d0-109">[out] A pointer to pointer to the copy of [IEnumFBBlock](ienumfbblock.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="cf7d0-110">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="cf7d0-110">Return values</span></span>

|<span data-ttu-id="cf7d0-111">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="cf7d0-111">**HRESULT**</span></span>|<span data-ttu-id="cf7d0-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="cf7d0-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cf7d0-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="cf7d0-113">S_OK</span></span>  <br/> |<span data-ttu-id="cf7d0-114">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="cf7d0-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="cf7d0-115">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="cf7d0-115">E_OUTOFMEMORY</span></span>  <br/> |<span data-ttu-id="cf7d0-116">No hay memoria suficiente para realizar la copia.</span><span class="sxs-lookup"><span data-stu-id="cf7d0-116">There is insufficient memory for making the copy.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cf7d0-117">Consulte también</span><span class="sxs-lookup"><span data-stu-id="cf7d0-117">See also</span></span>

- [<span data-ttu-id="cf7d0-118">Constantes (API de disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="cf7d0-118">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)
- [<span data-ttu-id="cf7d0-119">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="cf7d0-119">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="cf7d0-120">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="cf7d0-120">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="cf7d0-121">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="cf7d0-121">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)  
- [<span data-ttu-id="cf7d0-122">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="cf7d0-122">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)

