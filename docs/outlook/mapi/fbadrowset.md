---
title: FBadRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRowSet
api_type:
- COM
ms.assetid: 3890dd50-e6ca-4859-bada-f6752ab61d41
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 49e6c8254cbd527635685c3f974da57ee3ac82a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341023"
---
# <a name="fbadrowset"></a><span data-ttu-id="c8246-103">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="c8246-103">FBadRowSet</span></span>

  
  
<span data-ttu-id="c8246-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8246-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8246-105">Valida todas las filas de tabla incluidas en un conjunto de filas de tabla.</span><span class="sxs-lookup"><span data-stu-id="c8246-105">Validates all table rows included in a set of table rows.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c8246-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="c8246-106">Header file:</span></span>  <br/> |<span data-ttu-id="c8246-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="c8246-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="c8246-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="c8246-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c8246-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c8246-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c8246-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="c8246-110">Called by:</span></span>  <br/> |<span data-ttu-id="c8246-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="c8246-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRowSet(
  LPSRowSet lpRowSet
);
```

## <a name="parameters"></a><span data-ttu-id="c8246-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8246-112">Parameters</span></span>

 <span data-ttu-id="c8246-113">_lpRowSet_</span><span class="sxs-lookup"><span data-stu-id="c8246-113">_lpRowSet_</span></span>
  
> <span data-ttu-id="c8246-114">a Puntero a una estructura [SRowSet](srowset.md) que identifica el conjunto de filas que se va a validar.</span><span class="sxs-lookup"><span data-stu-id="c8246-114">[in] Pointer to an [SRowSet](srowset.md) structure identifying the row set to be validated.</span></span> <span data-ttu-id="c8246-115">Si el puntero es NULL, la estructura no es válida.</span><span class="sxs-lookup"><span data-stu-id="c8246-115">If the pointer is NULL, the structure is invalid.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c8246-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8246-116">Return value</span></span>

<span data-ttu-id="c8246-117">TRUE</span><span class="sxs-lookup"><span data-stu-id="c8246-117">TRUE</span></span> 
  
> <span data-ttu-id="c8246-118">Una fila del conjunto de filas especificado no es válida o el conjunto de filas en sí no es válido.</span><span class="sxs-lookup"><span data-stu-id="c8246-118">A row of the specified row set is invalid, or the row set itself is invalid.</span></span> 
    
<span data-ttu-id="c8246-119">FALSE</span><span class="sxs-lookup"><span data-stu-id="c8246-119">FALSE</span></span> 
  
> <span data-ttu-id="c8246-120">Las filas del conjunto de filas especificado y el conjunto de filas son válidas.</span><span class="sxs-lookup"><span data-stu-id="c8246-120">The rows of the specified row set and the row set itself are all valid.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c8246-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8246-121">See also</span></span>



[<span data-ttu-id="c8246-122">FBadRow</span><span class="sxs-lookup"><span data-stu-id="c8246-122">FBadRow</span></span>](fbadrow.md)

