---
title: SSizeRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSizeRestriction
api_type:
- COM
ms.assetid: 4e7340d1-3cb9-4276-b83f-1c8f94acb909
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 134eb844ef7b72d396c300b27a87a3a7ae320cf1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820766"
---
# <a name="ssizerestriction"></a><span data-ttu-id="c3beb-103">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="c3beb-103">SSizeRestriction</span></span>

  
  
<span data-ttu-id="c3beb-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c3beb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c3beb-105">Describe una restricción de tamaño que se usa para probar el tamaño de un valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="c3beb-105">Describes a size restriction which is used to test the size of a property value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c3beb-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="c3beb-106">Header file:</span></span>  <br/> |<span data-ttu-id="c3beb-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c3beb-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSizeRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  ULONG cb;
} SSizeRestriction;

```

## <a name="members"></a><span data-ttu-id="c3beb-108">Members</span><span class="sxs-lookup"><span data-stu-id="c3beb-108">Members</span></span>

 <span data-ttu-id="c3beb-109">**RelOp**</span><span class="sxs-lookup"><span data-stu-id="c3beb-109">**relop**</span></span>
  
> <span data-ttu-id="c3beb-110">Operador relacional que se usa en la comparación de tamaño.</span><span class="sxs-lookup"><span data-stu-id="c3beb-110">Relational operator that is used in the size comparison.</span></span> <span data-ttu-id="c3beb-111">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="c3beb-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="c3beb-112">RELOP_GE</span><span class="sxs-lookup"><span data-stu-id="c3beb-112">RELOP_GE</span></span> 
  
> <span data-ttu-id="c3beb-113">Se realice a la comparación en un primer valor mayor o igual.</span><span class="sxs-lookup"><span data-stu-id="c3beb-113">The comparison is made based on a greater or equal first value.</span></span>
    
<span data-ttu-id="c3beb-114">RELOP_GT</span><span class="sxs-lookup"><span data-stu-id="c3beb-114">RELOP_GT</span></span> 
  
> <span data-ttu-id="c3beb-115">Se realice a la comparación en un primer valor mayor.</span><span class="sxs-lookup"><span data-stu-id="c3beb-115">The comparison is made based on a greater first value.</span></span>
    
<span data-ttu-id="c3beb-116">RELOP_LE</span><span class="sxs-lookup"><span data-stu-id="c3beb-116">RELOP_LE</span></span> 
  
> <span data-ttu-id="c3beb-117">Se realice a la comparación en un primer valor menor o igual.</span><span class="sxs-lookup"><span data-stu-id="c3beb-117">The comparison is made based on a lesser or equal first value.</span></span>
    
<span data-ttu-id="c3beb-118">RELOP_LT</span><span class="sxs-lookup"><span data-stu-id="c3beb-118">RELOP_LT</span></span> 
  
> <span data-ttu-id="c3beb-119">Se realice a la comparación en un primer valor menor.</span><span class="sxs-lookup"><span data-stu-id="c3beb-119">The comparison is made based on a lesser first value.</span></span>
    
<span data-ttu-id="c3beb-120">RELOP_NE</span><span class="sxs-lookup"><span data-stu-id="c3beb-120">RELOP_NE</span></span> 
  
> <span data-ttu-id="c3beb-121">Se realice a la comparación en valores iguales.</span><span class="sxs-lookup"><span data-stu-id="c3beb-121">The comparison is made based on unequal values.</span></span>
    
<span data-ttu-id="c3beb-122">RELOP_RE</span><span class="sxs-lookup"><span data-stu-id="c3beb-122">RELOP_RE</span></span> 
  
> <span data-ttu-id="c3beb-123">La comparación se realiza en función de como valores (expresión regular).</span><span class="sxs-lookup"><span data-stu-id="c3beb-123">The comparison is made based on LIKE (regular expression) values.</span></span>
    
<span data-ttu-id="c3beb-124">RELOP_EQ</span><span class="sxs-lookup"><span data-stu-id="c3beb-124">RELOP_EQ</span></span> 
  
> <span data-ttu-id="c3beb-125">Se realice a la comparación de valores iguales.</span><span class="sxs-lookup"><span data-stu-id="c3beb-125">The comparison is made based on equal values.</span></span>
    
 <span data-ttu-id="c3beb-126">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="c3beb-126">**ulPropTag**</span></span>
  
> <span data-ttu-id="c3beb-127">Etiqueta de la propiedad que identifica la propiedad que se debe probar.</span><span class="sxs-lookup"><span data-stu-id="c3beb-127">Property tag identifying the property to test.</span></span>
    
 <span data-ttu-id="c3beb-128">**cb**</span><span class="sxs-lookup"><span data-stu-id="c3beb-128">**cb**</span></span>
  
> <span data-ttu-id="c3beb-129">Recuento de bytes en el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="c3beb-129">Count of bytes in the property value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c3beb-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c3beb-130">Remarks</span></span>

<span data-ttu-id="c3beb-131">Para obtener una descripción general de cómo funcionan las restricciones, vea [Restricciones de sobre](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="c3beb-131">For a general discussion of how restrictions work, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c3beb-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3beb-132">See also</span></span>



[<span data-ttu-id="c3beb-133">SRestriction</span><span class="sxs-lookup"><span data-stu-id="c3beb-133">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="c3beb-134">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="c3beb-134">MAPI Structures</span></span>](mapi-structures.md)

