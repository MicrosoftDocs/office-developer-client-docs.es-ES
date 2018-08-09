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
ms.openlocfilehash: 1767c86cb5390572b95530060f2295034ed35f43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820726"
---
# <a name="smapiverbarray"></a><span data-ttu-id="db9a8-103">SMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="db9a8-103">SMAPIVerbArray</span></span>

  
  
<span data-ttu-id="db9a8-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="db9a8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="db9a8-105">Contiene una matriz de estructuras [SMAPIVerb](smapiverb.md) que describen los verbos de MAPI.</span><span class="sxs-lookup"><span data-stu-id="db9a8-105">Contains an array of [SMAPIVerb](smapiverb.md) structures that describe MAPI verbs.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="db9a8-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="db9a8-106">Header file:</span></span>  <br/> |<span data-ttu-id="db9a8-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="db9a8-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="db9a8-108">Macro relacionado:</span><span class="sxs-lookup"><span data-stu-id="db9a8-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="db9a8-109">CbMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="db9a8-109">CbMAPIVerbArray</span></span>](cbmapiverbarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cMAPIVerb;
  SMAPIVerb aMAPIVerb[MAPI_DIM];
} SMAPIVerbArray, FAR * LPMAPIVERBARRAY;

```

## <a name="members"></a><span data-ttu-id="db9a8-110">Members</span><span class="sxs-lookup"><span data-stu-id="db9a8-110">Members</span></span>

 <span data-ttu-id="db9a8-111">**cForms**</span><span class="sxs-lookup"><span data-stu-id="db9a8-111">**cForms**</span></span>
  
> <span data-ttu-id="db9a8-112">Recuento de verbos en la matriz.</span><span class="sxs-lookup"><span data-stu-id="db9a8-112">Count of verbs in the array.</span></span>
    
 <span data-ttu-id="db9a8-113">**aFormInfo**</span><span class="sxs-lookup"><span data-stu-id="db9a8-113">**aFormInfo**</span></span>
  
> <span data-ttu-id="db9a8-114">Matriz de los verbos de MAPI.</span><span class="sxs-lookup"><span data-stu-id="db9a8-114">Array of MAPI verbs.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="db9a8-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="db9a8-115">Remarks</span></span>

<span data-ttu-id="db9a8-116">La estructura **SMAPIVerbArray** se pasa como un parámetro en el método [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) .</span><span class="sxs-lookup"><span data-stu-id="db9a8-116">The **SMAPIVerbArray** structure is passed as a parameter in the [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="db9a8-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="db9a8-117">See also</span></span>



[<span data-ttu-id="db9a8-118">SMAPIVerb</span><span class="sxs-lookup"><span data-stu-id="db9a8-118">SMAPIVerb</span></span>](smapiverb.md)


[<span data-ttu-id="db9a8-119">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="db9a8-119">MAPI Structures</span></span>](mapi-structures.md)

