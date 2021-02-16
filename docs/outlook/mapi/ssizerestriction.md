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
ms.openlocfilehash: 24ceb7b5358447de3a240756227b86224d2c354c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439089"
---
# <a name="ssizerestriction"></a><span data-ttu-id="48144-103">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="48144-103">SSizeRestriction</span></span>

  
  
<span data-ttu-id="48144-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48144-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48144-105">Describe una restricción de tamaño que se usa para probar el tamaño de un valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="48144-105">Describes a size restriction which is used to test the size of a property value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="48144-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="48144-106">Header file:</span></span>  <br/> |<span data-ttu-id="48144-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="48144-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSizeRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  ULONG cb;
} SSizeRestriction;

```

## <a name="members"></a><span data-ttu-id="48144-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="48144-108">Members</span></span>

 <span data-ttu-id="48144-109">**reeste**</span><span class="sxs-lookup"><span data-stu-id="48144-109">**relop**</span></span>
  
> <span data-ttu-id="48144-110">Operador relacional que se usa en la comparación de tamaño.</span><span class="sxs-lookup"><span data-stu-id="48144-110">Relational operator that is used in the size comparison.</span></span> <span data-ttu-id="48144-111">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="48144-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="48144-112">RELOP_GE</span><span class="sxs-lookup"><span data-stu-id="48144-112">RELOP_GE</span></span> 
  
> <span data-ttu-id="48144-113">La comparación se realiza en función de un primer valor mayor o igual.</span><span class="sxs-lookup"><span data-stu-id="48144-113">The comparison is made based on a greater or equal first value.</span></span>
    
<span data-ttu-id="48144-114">RELOP_GT</span><span class="sxs-lookup"><span data-stu-id="48144-114">RELOP_GT</span></span> 
  
> <span data-ttu-id="48144-115">La comparación se realiza en función de un primer valor mayor.</span><span class="sxs-lookup"><span data-stu-id="48144-115">The comparison is made based on a greater first value.</span></span>
    
<span data-ttu-id="48144-116">RELOP_LE</span><span class="sxs-lookup"><span data-stu-id="48144-116">RELOP_LE</span></span> 
  
> <span data-ttu-id="48144-117">La comparación se realiza en función de un primer valor menor o igual.</span><span class="sxs-lookup"><span data-stu-id="48144-117">The comparison is made based on a lesser or equal first value.</span></span>
    
<span data-ttu-id="48144-118">RELOP_LT</span><span class="sxs-lookup"><span data-stu-id="48144-118">RELOP_LT</span></span> 
  
> <span data-ttu-id="48144-119">La comparación se realiza en función de un primer valor menor.</span><span class="sxs-lookup"><span data-stu-id="48144-119">The comparison is made based on a lesser first value.</span></span>
    
<span data-ttu-id="48144-120">RELOP_NE</span><span class="sxs-lookup"><span data-stu-id="48144-120">RELOP_NE</span></span> 
  
> <span data-ttu-id="48144-121">La comparación se realiza en función de valores no iguales.</span><span class="sxs-lookup"><span data-stu-id="48144-121">The comparison is made based on unequal values.</span></span>
    
<span data-ttu-id="48144-122">RELOP_RE</span><span class="sxs-lookup"><span data-stu-id="48144-122">RELOP_RE</span></span> 
  
> <span data-ttu-id="48144-123">La comparación se realiza en función de los valores LIKE (expresión regular).</span><span class="sxs-lookup"><span data-stu-id="48144-123">The comparison is made based on LIKE (regular expression) values.</span></span>
    
<span data-ttu-id="48144-124">RELOP_EQ</span><span class="sxs-lookup"><span data-stu-id="48144-124">RELOP_EQ</span></span> 
  
> <span data-ttu-id="48144-125">La comparación se realiza en función de valores iguales.</span><span class="sxs-lookup"><span data-stu-id="48144-125">The comparison is made based on equal values.</span></span>
    
 <span data-ttu-id="48144-126">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="48144-126">**ulPropTag**</span></span>
  
> <span data-ttu-id="48144-127">Etiqueta de propiedad que identifica la propiedad que se debe probar.</span><span class="sxs-lookup"><span data-stu-id="48144-127">Property tag identifying the property to test.</span></span>
    
 <span data-ttu-id="48144-128">**cb**</span><span class="sxs-lookup"><span data-stu-id="48144-128">**cb**</span></span>
  
> <span data-ttu-id="48144-129">Número de bytes en el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="48144-129">Count of bytes in the property value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="48144-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="48144-130">Remarks</span></span>

<span data-ttu-id="48144-131">Para obtener una explicación general de cómo funcionan las [restricciones,](about-restrictions.md)vea Acerca de las restricciones .</span><span class="sxs-lookup"><span data-stu-id="48144-131">For a general discussion of how restrictions work, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="48144-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="48144-132">See also</span></span>



[<span data-ttu-id="48144-133">SRestriction</span><span class="sxs-lookup"><span data-stu-id="48144-133">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="48144-134">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="48144-134">MAPI Structures</span></span>](mapi-structures.md)

