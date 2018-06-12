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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: e6963fc373f771289e3dbff3a0b41857352b4b9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816821"
---
# <a name="fbadrowset"></a><span data-ttu-id="3e099-103">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="3e099-103">FBadRowSet</span></span>

  
  
<span data-ttu-id="3e099-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3e099-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3e099-105">Valida todas las filas de tabla incluidas en un conjunto de filas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="3e099-105">Validates all table rows included in a set of table rows.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3e099-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="3e099-106">Header file:</span></span>  <br/> |<span data-ttu-id="3e099-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="3e099-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="3e099-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="3e099-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3e099-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3e099-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3e099-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="3e099-110">Called by:</span></span>  <br/> |<span data-ttu-id="3e099-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="3e099-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRowSet(
  LPSRowSet lpRowSet
);
```

## <a name="parameters"></a><span data-ttu-id="3e099-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3e099-112">Parameters</span></span>

 <span data-ttu-id="3e099-113">_lpRowSet_</span><span class="sxs-lookup"><span data-stu-id="3e099-113">_lpRowSet_</span></span>
  
> <span data-ttu-id="3e099-114">[entrada] Puntero a una estructura [SRowSet](srowset.md) que identifica el conjunto que se va a validar de filas.</span><span class="sxs-lookup"><span data-stu-id="3e099-114">[in] Pointer to an [SRowSet](srowset.md) structure identifying the row set to be validated.</span></span> <span data-ttu-id="3e099-115">Si el puntero es NULL, la estructura no es válida.</span><span class="sxs-lookup"><span data-stu-id="3e099-115">If the pointer is NULL, the structure is invalid.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3e099-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3e099-116">Return value</span></span>

<span data-ttu-id="3e099-117">TRUE</span><span class="sxs-lookup"><span data-stu-id="3e099-117">TRUE</span></span> 
  
> <span data-ttu-id="3e099-118">Una fila del conjunto de filas especificado no es válida o el propio conjunto de filas no es válido.</span><span class="sxs-lookup"><span data-stu-id="3e099-118">A row of the specified row set is invalid, or the row set itself is invalid.</span></span> 
    
<span data-ttu-id="3e099-119">FALSE</span><span class="sxs-lookup"><span data-stu-id="3e099-119">FALSE</span></span> 
  
> <span data-ttu-id="3e099-120">Las filas del conjunto de fila especificada y el propio conjunto de filas son válidas.</span><span class="sxs-lookup"><span data-stu-id="3e099-120">The rows of the specified row set and the row set itself are all valid.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3e099-121">Ver también</span><span class="sxs-lookup"><span data-stu-id="3e099-121">See also</span></span>



[<span data-ttu-id="3e099-122">FBadRow</span><span class="sxs-lookup"><span data-stu-id="3e099-122">FBadRow</span></span>](fbadrow.md)

