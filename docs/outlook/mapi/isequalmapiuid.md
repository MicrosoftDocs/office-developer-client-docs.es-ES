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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 635a4a872b83a2996b1a0198975a0ecd2cd906eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817957"
---
# <a name="isequalmapiuid"></a><span data-ttu-id="c6bf0-103">IsEqualMAPIUID</span><span class="sxs-lookup"><span data-stu-id="c6bf0-103">IsEqualMAPIUID</span></span>

  
  
<span data-ttu-id="c6bf0-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c6bf0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c6bf0-105">Prueba dos estructuras [MAPIUID](mapiuid.md) para determinar si contienen el mismo identificador.</span><span class="sxs-lookup"><span data-stu-id="c6bf0-105">Tests two [MAPIUID](mapiuid.md) structures to determine whether they contain the same identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c6bf0-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="c6bf0-106">Header file:</span></span>  <br/> |<span data-ttu-id="c6bf0-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c6bf0-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c6bf0-108">Estructura relacionado:</span><span class="sxs-lookup"><span data-stu-id="c6bf0-108">Related structure:</span></span>  <br/> |<span data-ttu-id="c6bf0-109">**MAPIUID**</span><span class="sxs-lookup"><span data-stu-id="c6bf0-109">**MAPIUID**</span></span> <br/> |
   
```cpp
IsEqualMAPIUID(lpuid1, lpuid2)
```

## <a name="parameters"></a><span data-ttu-id="c6bf0-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c6bf0-110">Parameters</span></span>

 <span data-ttu-id="c6bf0-111">_lpuid1_</span><span class="sxs-lookup"><span data-stu-id="c6bf0-111">_lpuid1_</span></span>
  
> <span data-ttu-id="c6bf0-112">Puntero a la primera estructura **MAPIUID** que se probará.</span><span class="sxs-lookup"><span data-stu-id="c6bf0-112">Pointer to the first **MAPIUID** structure to be tested.</span></span> 
    
 <span data-ttu-id="c6bf0-113">_lpuid2_</span><span class="sxs-lookup"><span data-stu-id="c6bf0-113">_lpuid2_</span></span>
  
> <span data-ttu-id="c6bf0-114">Puntero a la segunda estructura **MAPIUID** que se probará.</span><span class="sxs-lookup"><span data-stu-id="c6bf0-114">Pointer to the second **MAPIUID** structure to be tested.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c6bf0-115">Notas</span><span class="sxs-lookup"><span data-stu-id="c6bf0-115">Remarks</span></span>

<span data-ttu-id="c6bf0-116">La macro **IsEqualMAPIUID** devuelve TRUE si las dos estructuras **MAPIUID** contienen el mismo identificador y FALSE si no lo hace.</span><span class="sxs-lookup"><span data-stu-id="c6bf0-116">The **IsEqualMAPIUID** macro returns TRUE if the two **MAPIUID** structures contain the same identifier and FALSE if they do not.</span></span> 
  
<span data-ttu-id="c6bf0-117">La macro **IsEqualMAPIUID** requiere que el archivo de encabezado Memory.h se incluirán.</span><span class="sxs-lookup"><span data-stu-id="c6bf0-117">The **IsEqualMAPIUID** macro requires that the header file Memory.h be included.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c6bf0-118">Ver también</span><span class="sxs-lookup"><span data-stu-id="c6bf0-118">See also</span></span>



[<span data-ttu-id="c6bf0-119">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="c6bf0-119">MAPIUID</span></span>](mapiuid.md)


[<span data-ttu-id="c6bf0-120">Macros relacionadas con las estructuras</span><span class="sxs-lookup"><span data-stu-id="c6bf0-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

