---
title: FBadRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRow
api_type:
- COM
ms.assetid: 205d00df-488d-4888-8782-a1f70f54d720
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 153bcbfd87ea9e85d834cba2fd9028e98fa25750
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420622"
---
# <a name="fbadrow"></a><span data-ttu-id="7b9fc-103">FBadRow</span><span class="sxs-lookup"><span data-stu-id="7b9fc-103">FBadRow</span></span>

  
  
<span data-ttu-id="7b9fc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b9fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b9fc-105">Valida una fila de una tabla.</span><span class="sxs-lookup"><span data-stu-id="7b9fc-105">Validates a row in a table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7b9fc-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="7b9fc-106">Header file:</span></span>  <br/> |<span data-ttu-id="7b9fc-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="7b9fc-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="7b9fc-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="7b9fc-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7b9fc-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7b9fc-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7b9fc-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="7b9fc-110">Called by:</span></span>  <br/> |<span data-ttu-id="7b9fc-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="7b9fc-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadRow(
  LPSRow lprow
);
```

## <a name="parameters"></a><span data-ttu-id="7b9fc-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7b9fc-112">Parameters</span></span>

 <span data-ttu-id="7b9fc-113">_lprow_</span><span class="sxs-lookup"><span data-stu-id="7b9fc-113">_lprow_</span></span>
  
> <span data-ttu-id="7b9fc-114">[in] Puntero a una [estructura SRow](srow.md) que identifica la fila que se va a validar.</span><span class="sxs-lookup"><span data-stu-id="7b9fc-114">[in] Pointer to an [SRow](srow.md) structure identifying the row to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7b9fc-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7b9fc-115">Return value</span></span>

<span data-ttu-id="7b9fc-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="7b9fc-116">TRUE</span></span> 
  
> <span data-ttu-id="7b9fc-117">La fila especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="7b9fc-117">The specified row is invalid.</span></span>
    
<span data-ttu-id="7b9fc-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="7b9fc-118">FALSE</span></span> 
  
> <span data-ttu-id="7b9fc-119">La fila especificada es válida.</span><span class="sxs-lookup"><span data-stu-id="7b9fc-119">The specified row is valid.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7b9fc-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b9fc-120">See also</span></span>



[<span data-ttu-id="7b9fc-121">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="7b9fc-121">FBadRowSet</span></span>](fbadrowset.md)

