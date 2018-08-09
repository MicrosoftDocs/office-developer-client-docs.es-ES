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
ms.openlocfilehash: c3025c353c71958a19303c5e79cec319a3bf8015
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816814"
---
# <a name="fbadrow"></a><span data-ttu-id="820cf-103">FBadRow</span><span class="sxs-lookup"><span data-stu-id="820cf-103">FBadRow</span></span>

  
  
<span data-ttu-id="820cf-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="820cf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="820cf-105">Valida una fila en una tabla.</span><span class="sxs-lookup"><span data-stu-id="820cf-105">Validates a row in a table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="820cf-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="820cf-106">Header file:</span></span>  <br/> |<span data-ttu-id="820cf-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="820cf-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="820cf-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="820cf-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="820cf-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="820cf-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="820cf-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="820cf-110">Called by:</span></span>  <br/> |<span data-ttu-id="820cf-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="820cf-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadRow(
  LPSRow lprow
);
```

## <a name="parameters"></a><span data-ttu-id="820cf-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="820cf-112">Parameters</span></span>

 <span data-ttu-id="820cf-113">_lprow_</span><span class="sxs-lookup"><span data-stu-id="820cf-113">_lprow_</span></span>
  
> <span data-ttu-id="820cf-114">[entrada] Puntero a una estructura [SRow](srow.md) que identifica la fila que se va a validar.</span><span class="sxs-lookup"><span data-stu-id="820cf-114">[in] Pointer to an [SRow](srow.md) structure identifying the row to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="820cf-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="820cf-115">Return value</span></span>

<span data-ttu-id="820cf-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="820cf-116">TRUE</span></span> 
  
> <span data-ttu-id="820cf-117">La fila especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="820cf-117">The specified row is invalid.</span></span>
    
<span data-ttu-id="820cf-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="820cf-118">FALSE</span></span> 
  
> <span data-ttu-id="820cf-119">La fila especificada es válida.</span><span class="sxs-lookup"><span data-stu-id="820cf-119">The specified row is valid.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="820cf-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="820cf-120">See also</span></span>



[<span data-ttu-id="820cf-121">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="820cf-121">FBadRowSet</span></span>](fbadrowset.md)

