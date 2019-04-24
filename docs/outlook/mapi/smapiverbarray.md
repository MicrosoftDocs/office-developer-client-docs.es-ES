---
title: SMAPIVerbArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIVerbArray
api_type:
- COM
ms.assetid: 8736f75c-3e95-42dd-9bc1-2f0bd23c4a02
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7cba5dce60ce15ddb12776d619143849298aac9f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357480"
---
# <a name="smapiverbarray"></a><span data-ttu-id="5df4d-103">SMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="5df4d-103">SMAPIVerbArray</span></span>

  
  
<span data-ttu-id="5df4d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5df4d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5df4d-105">Contiene una matriz de estructuras [SMAPIVerb](smapiverb.md) que describen los verbos de MAPI.</span><span class="sxs-lookup"><span data-stu-id="5df4d-105">Contains an array of [SMAPIVerb](smapiverb.md) structures that describe MAPI verbs.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5df4d-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="5df4d-106">Header file:</span></span>  <br/> |<span data-ttu-id="5df4d-107">MAPIForm. h</span><span class="sxs-lookup"><span data-stu-id="5df4d-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="5df4d-108">Macro relacionada:</span><span class="sxs-lookup"><span data-stu-id="5df4d-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="5df4d-109">CbMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="5df4d-109">CbMAPIVerbArray</span></span>](cbmapiverbarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cMAPIVerb;
  SMAPIVerb aMAPIVerb[MAPI_DIM];
} SMAPIVerbArray, FAR * LPMAPIVERBARRAY;

```

## <a name="members"></a><span data-ttu-id="5df4d-110">Members</span><span class="sxs-lookup"><span data-stu-id="5df4d-110">Members</span></span>

 <span data-ttu-id="5df4d-111">**cForms**</span><span class="sxs-lookup"><span data-stu-id="5df4d-111">**cForms**</span></span>
  
> <span data-ttu-id="5df4d-112">Número de verbos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5df4d-112">Count of verbs in the array.</span></span>
    
 <span data-ttu-id="5df4d-113">**aFormInfo**</span><span class="sxs-lookup"><span data-stu-id="5df4d-113">**aFormInfo**</span></span>
  
> <span data-ttu-id="5df4d-114">Matriz de verbos MAPI.</span><span class="sxs-lookup"><span data-stu-id="5df4d-114">Array of MAPI verbs.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5df4d-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5df4d-115">Remarks</span></span>

<span data-ttu-id="5df4d-116">La estructura **SMAPIVerbArray** se pasa como un parámetro en el método [IMAPIFormInfo:: CalcVerbSet](imapiforminfo-calcverbset.md) .</span><span class="sxs-lookup"><span data-stu-id="5df4d-116">The **SMAPIVerbArray** structure is passed as a parameter in the [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5df4d-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="5df4d-117">See also</span></span>



[<span data-ttu-id="5df4d-118">SMAPIVerb</span><span class="sxs-lookup"><span data-stu-id="5df4d-118">SMAPIVerb</span></span>](smapiverb.md)


[<span data-ttu-id="5df4d-119">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="5df4d-119">MAPI Structures</span></span>](mapi-structures.md)

