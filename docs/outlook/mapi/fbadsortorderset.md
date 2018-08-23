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
ms.openlocfilehash: 3b3f88495cafbd6ea764ca8901ac67c23749aebe
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578580"
---
# <a name="fbadsortorderset"></a><span data-ttu-id="0d27d-103">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="0d27d-103">FBadSortOrderSet</span></span>

  
  
<span data-ttu-id="0d27d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d27d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d27d-105">Valida un criterio de ordenación establecer comprobando su asignación de memoria.</span><span class="sxs-lookup"><span data-stu-id="0d27d-105">Validates a sort order set by verifying its memory allocation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0d27d-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="0d27d-106">Header file:</span></span>  <br/> |<span data-ttu-id="0d27d-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="0d27d-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="0d27d-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="0d27d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0d27d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0d27d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0d27d-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="0d27d-110">Called by:</span></span>  <br/> |<span data-ttu-id="0d27d-111">Proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="0d27d-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadSortOrderSet(
  LPSSortOrderSet lpsos
);
```

## <a name="parameters"></a><span data-ttu-id="0d27d-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0d27d-112">Parameters</span></span>

 <span data-ttu-id="0d27d-113">_lpsos_</span><span class="sxs-lookup"><span data-stu-id="0d27d-113">_lpsos_</span></span>
  
> <span data-ttu-id="0d27d-114">[entrada] Puntero a una estructura [SSortOrderSet](ssortorderset.md) que identifica el criterio de ordenación establecer que se va a validar.</span><span class="sxs-lookup"><span data-stu-id="0d27d-114">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure identifying the sort order set to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0d27d-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0d27d-115">Return value</span></span>

<span data-ttu-id="0d27d-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="0d27d-116">TRUE</span></span> 
  
> <span data-ttu-id="0d27d-117">El conjunto de criterio de ordenación especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="0d27d-117">The specified sort order set is invalid.</span></span> 
    
<span data-ttu-id="0d27d-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="0d27d-118">FALSE</span></span> 
  
> <span data-ttu-id="0d27d-119">El conjunto de criterio de ordenación especificado es válido.</span><span class="sxs-lookup"><span data-stu-id="0d27d-119">The specified sort order set is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0d27d-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0d27d-120">Remarks</span></span>

<span data-ttu-id="0d27d-121">La función **FBadSortOrderSet** se puede usar para preparar una llamada a un método de ordenación como el método [SortTable](imapitable-sorttable.md) .</span><span class="sxs-lookup"><span data-stu-id="0d27d-121">The **FBadSortOrderSet** function can be used to prepare for a call to a sort method such as the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
  

