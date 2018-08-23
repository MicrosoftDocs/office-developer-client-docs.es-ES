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
ms.openlocfilehash: 23b4ed78f4b65a5af4c2f3e11fa770030fe4eeee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590165"
---
# <a name="fbadrow"></a><span data-ttu-id="c4d08-103">FBadRow</span><span class="sxs-lookup"><span data-stu-id="c4d08-103">FBadRow</span></span>

  
  
<span data-ttu-id="c4d08-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4d08-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4d08-105">Valida una fila en una tabla.</span><span class="sxs-lookup"><span data-stu-id="c4d08-105">Validates a row in a table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c4d08-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="c4d08-106">Header file:</span></span>  <br/> |<span data-ttu-id="c4d08-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="c4d08-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="c4d08-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="c4d08-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c4d08-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c4d08-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c4d08-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="c4d08-110">Called by:</span></span>  <br/> |<span data-ttu-id="c4d08-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="c4d08-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadRow(
  LPSRow lprow
);
```

## <a name="parameters"></a><span data-ttu-id="c4d08-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c4d08-112">Parameters</span></span>

 <span data-ttu-id="c4d08-113">_lprow_</span><span class="sxs-lookup"><span data-stu-id="c4d08-113">_lprow_</span></span>
  
> <span data-ttu-id="c4d08-114">[entrada] Puntero a una estructura [SRow](srow.md) que identifica la fila que se va a validar.</span><span class="sxs-lookup"><span data-stu-id="c4d08-114">[in] Pointer to an [SRow](srow.md) structure identifying the row to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c4d08-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c4d08-115">Return value</span></span>

<span data-ttu-id="c4d08-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="c4d08-116">TRUE</span></span> 
  
> <span data-ttu-id="c4d08-117">La fila especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="c4d08-117">The specified row is invalid.</span></span>
    
<span data-ttu-id="c4d08-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="c4d08-118">FALSE</span></span> 
  
> <span data-ttu-id="c4d08-119">La fila especificada es válida.</span><span class="sxs-lookup"><span data-stu-id="c4d08-119">The specified row is valid.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c4d08-120">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="c4d08-120">See also</span></span>



[<span data-ttu-id="c4d08-121">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="c4d08-121">FBadRowSet</span></span>](fbadrowset.md)

