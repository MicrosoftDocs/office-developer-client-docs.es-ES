---
title: IsEqualMAPIUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IsEqualMAPIUID
api_type:
- COM
ms.assetid: 85d71b73-0630-4c5d-b0e3-b48d27a300d0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 44e3613338c8932bc80dd1150392033dfa3cd050
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426936"
---
# <a name="isequalmapiuid"></a><span data-ttu-id="e2d96-103">IsEqualMAPIUID</span><span class="sxs-lookup"><span data-stu-id="e2d96-103">IsEqualMAPIUID</span></span>

  
  
<span data-ttu-id="e2d96-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2d96-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2d96-105">Prueba dos [estructuras MAPIUID](mapiuid.md) para determinar si contienen el mismo identificador.</span><span class="sxs-lookup"><span data-stu-id="e2d96-105">Tests two [MAPIUID](mapiuid.md) structures to determine whether they contain the same identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e2d96-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="e2d96-106">Header file:</span></span>  <br/> |<span data-ttu-id="e2d96-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e2d96-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e2d96-108">Estructura relacionada:</span><span class="sxs-lookup"><span data-stu-id="e2d96-108">Related structure:</span></span>  <br/> |<span data-ttu-id="e2d96-109">**MAPIUID**</span><span class="sxs-lookup"><span data-stu-id="e2d96-109">**MAPIUID**</span></span> <br/> |
   
```cpp
IsEqualMAPIUID(lpuid1, lpuid2)
```

## <a name="parameters"></a><span data-ttu-id="e2d96-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="e2d96-110">Parameters</span></span>

 <span data-ttu-id="e2d96-111">_lpuid1_</span><span class="sxs-lookup"><span data-stu-id="e2d96-111">_lpuid1_</span></span>
  
> <span data-ttu-id="e2d96-112">Puntero a la primera estructura **MAPIUID** que se va a probar.</span><span class="sxs-lookup"><span data-stu-id="e2d96-112">Pointer to the first **MAPIUID** structure to be tested.</span></span> 
    
 <span data-ttu-id="e2d96-113">_lpuid2_</span><span class="sxs-lookup"><span data-stu-id="e2d96-113">_lpuid2_</span></span>
  
> <span data-ttu-id="e2d96-114">Puntero a la segunda estructura **MAPIUID** que se va a probar.</span><span class="sxs-lookup"><span data-stu-id="e2d96-114">Pointer to the second **MAPIUID** structure to be tested.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e2d96-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e2d96-115">Remarks</span></span>

<span data-ttu-id="e2d96-116">La **macro IsEqualMAPIUID** devuelve TRUE si las dos estructuras **MAPIUID** contienen el mismo identificador y FALSE si no lo hacen.</span><span class="sxs-lookup"><span data-stu-id="e2d96-116">The **IsEqualMAPIUID** macro returns TRUE if the two **MAPIUID** structures contain the same identifier and FALSE if they do not.</span></span> 
  
<span data-ttu-id="e2d96-117">La **macro IsEqualMAPIUID** requiere que se incluya el archivo de encabezado Memory.h.</span><span class="sxs-lookup"><span data-stu-id="e2d96-117">The **IsEqualMAPIUID** macro requires that the header file Memory.h be included.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e2d96-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2d96-118">See also</span></span>



[<span data-ttu-id="e2d96-119">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="e2d96-119">MAPIUID</span></span>](mapiuid.md)


[<span data-ttu-id="e2d96-120">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="e2d96-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

