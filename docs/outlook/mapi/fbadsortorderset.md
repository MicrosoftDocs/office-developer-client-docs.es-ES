---
title: FBadSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadSortOrderSet
api_type:
- COM
ms.assetid: b7f80e0a-8ddd-4b24-ab63-2078a8152058
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 31840923e24cddd0dc3dfa9cc67b610d0dcd7e47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428462"
---
# <a name="fbadsortorderset"></a><span data-ttu-id="bbd40-103">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="bbd40-103">FBadSortOrderSet</span></span>

  
  
<span data-ttu-id="bbd40-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bbd40-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bbd40-105">Valida un criterio de ordenación establecido mediante la comprobación de la asignación de memoria.</span><span class="sxs-lookup"><span data-stu-id="bbd40-105">Validates a sort order set by verifying its memory allocation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bbd40-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="bbd40-106">Header file:</span></span>  <br/> |<span data-ttu-id="bbd40-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="bbd40-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="bbd40-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="bbd40-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="bbd40-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="bbd40-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="bbd40-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="bbd40-110">Called by:</span></span>  <br/> |<span data-ttu-id="bbd40-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="bbd40-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadSortOrderSet(
  LPSSortOrderSet lpsos
);
```

## <a name="parameters"></a><span data-ttu-id="bbd40-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bbd40-112">Parameters</span></span>

 <span data-ttu-id="bbd40-113">_lpsos_</span><span class="sxs-lookup"><span data-stu-id="bbd40-113">_lpsos_</span></span>
  
> <span data-ttu-id="bbd40-114">a Puntero a una estructura [SSortOrderSet](ssortorderset.md) que identifica el criterio de ordenación establecido para validarse.</span><span class="sxs-lookup"><span data-stu-id="bbd40-114">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure identifying the sort order set to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bbd40-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bbd40-115">Return value</span></span>

<span data-ttu-id="bbd40-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="bbd40-116">TRUE</span></span> 
  
> <span data-ttu-id="bbd40-117">El conjunto de criterios de ordenación especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="bbd40-117">The specified sort order set is invalid.</span></span> 
    
<span data-ttu-id="bbd40-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="bbd40-118">FALSE</span></span> 
  
> <span data-ttu-id="bbd40-119">El conjunto de criterio de ordenación especificado es válido.</span><span class="sxs-lookup"><span data-stu-id="bbd40-119">The specified sort order set is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bbd40-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bbd40-120">Remarks</span></span>

<span data-ttu-id="bbd40-121">La función **FBadSortOrderSet** se puede usar para preparar una llamada a un método de ordenación como el método [IMAPITable:: SortTable](imapitable-sorttable.md) .</span><span class="sxs-lookup"><span data-stu-id="bbd40-121">The **FBadSortOrderSet** function can be used to prepare for a call to a sort method such as the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
  

