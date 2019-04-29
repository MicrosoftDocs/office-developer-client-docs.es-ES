---
title: SComparePropsRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SComparePropsRestriction
api_type:
- COM
ms.assetid: 3231a91a-1ef2-4dd8-9f3e-79ca56d2eae9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 513ec0db4e99e687d8aeb9e1d6acdef73df4d158
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33440006"
---
# <a name="scomparepropsrestriction"></a><span data-ttu-id="cd8cf-103">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="cd8cf-103">SComparePropsRestriction</span></span>

<span data-ttu-id="cd8cf-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd8cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd8cf-105">Describe una restricción de comparación de propiedades, que prueba dos propiedades mediante un operador relacional.</span><span class="sxs-lookup"><span data-stu-id="cd8cf-105">Describes a compare property restriction, which tests two properties using a relational operator.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cd8cf-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="cd8cf-106">Header file:</span></span>  <br/> |<span data-ttu-id="cd8cf-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="cd8cf-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SComparePropsRestriction
{
  ULONG relop;
  ULONG ulPropTag1;
  ULONG ulPropTag2;
} SComparePropsRestriction;

```

## <a name="members"></a><span data-ttu-id="cd8cf-108">Members</span><span class="sxs-lookup"><span data-stu-id="cd8cf-108">Members</span></span>

<span data-ttu-id="cd8cf-109">**relop**</span><span class="sxs-lookup"><span data-stu-id="cd8cf-109">**relop**</span></span>
  
> <span data-ttu-id="cd8cf-110">Operador relacional que se va a usar para comparar las dos propiedades.</span><span class="sxs-lookup"><span data-stu-id="cd8cf-110">Relational operator to use to compare the two properties.</span></span> <span data-ttu-id="cd8cf-111">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="cd8cf-111">Possible values are as follows:</span></span>
    
  - <span data-ttu-id="cd8cf-112">RELOP_GE: la comparación se realiza en función de un valor mayor o igual al primero.</span><span class="sxs-lookup"><span data-stu-id="cd8cf-112">RELOP_GE: The comparison is made based on a greater or equal first value.</span></span>
      
  - <span data-ttu-id="cd8cf-113">RELOP_GT: la comparación se realiza en función de un primer valor superior.</span><span class="sxs-lookup"><span data-stu-id="cd8cf-113">RELOP_GT: The comparison is made based on a greater first value.</span></span>
      
  - <span data-ttu-id="cd8cf-114">RELOP_LE: la comparación se realiza en función de un valor menor o igual al primero.</span><span class="sxs-lookup"><span data-stu-id="cd8cf-114">RELOP_LE: The comparison is made based on a lesser or equal first value.</span></span>
      
  - <span data-ttu-id="cd8cf-115">RELOP_LT: la comparación se realiza en función de un valor primero menor.</span><span class="sxs-lookup"><span data-stu-id="cd8cf-115">RELOP_LT: The comparison is made based on a lesser first value.</span></span>
      
  - <span data-ttu-id="cd8cf-116">RELOP_NE: la comparación se realiza en función de valores desiguales.</span><span class="sxs-lookup"><span data-stu-id="cd8cf-116">RELOP_NE: The comparison is made based on unequal values.</span></span>
      
  - <span data-ttu-id="cd8cf-117">RELOP_RE: la comparación se realiza en función de los valores LIKE (expresión regular).</span><span class="sxs-lookup"><span data-stu-id="cd8cf-117">RELOP_RE: The comparison is made based on LIKE (regular expression) values.</span></span>
      
  - <span data-ttu-id="cd8cf-118">RELOP_EQ: la comparación se realiza en función de los valores iguales.</span><span class="sxs-lookup"><span data-stu-id="cd8cf-118">RELOP_EQ: The comparison is made based on equal values.</span></span>
    
<span data-ttu-id="cd8cf-119">**ulPropTag1**</span><span class="sxs-lookup"><span data-stu-id="cd8cf-119">**ulPropTag1**</span></span>
  
> <span data-ttu-id="cd8cf-120">Etiqueta de propiedad de la primera propiedad que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="cd8cf-120">Property tag of the first property to be compared.</span></span> 
    
<span data-ttu-id="cd8cf-121">**ulPropTag2**</span><span class="sxs-lookup"><span data-stu-id="cd8cf-121">**ulPropTag2**</span></span>
  
> <span data-ttu-id="cd8cf-122">Etiqueta de propiedad de la segunda propiedad que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="cd8cf-122">Property tag of the second property to be compared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cd8cf-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cd8cf-123">Remarks</span></span>

<span data-ttu-id="cd8cf-124">El orden de comparación es _(etiqueta de propiedad 1) (operador relacional) (etiqueta de propiedad 2)_.</span><span class="sxs-lookup"><span data-stu-id="cd8cf-124">The comparison order is  _(property tag 1) (relational operator) (property tag 2)_.</span></span> <span data-ttu-id="cd8cf-125">Las propiedades que se van a comparar deben ser del mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="cd8cf-125">The properties to be compared must be of the same type.</span></span> <span data-ttu-id="cd8cf-126">Al intentar comparar propiedades de distintos tipos, MAPI o el proveedor de servicios devuelven el valor de error MAPI_E_TOO_COMPLEX del método [IMAPITable](imapitableiunknown.md) al que se pasa la estructura como parámetro.</span><span class="sxs-lookup"><span data-stu-id="cd8cf-126">Attempting to compare properties of different types causes MAPI or the service provider to return the error value MAPI_E_TOO_COMPLEX from the [IMAPITable](imapitableiunknown.md) method to which the structure is passed as a parameter.</span></span> 
  
<span data-ttu-id="cd8cf-127">El resultado de una restricción del valor de la propiedad Compare no está definido cuando no existe una o ambas propiedades.</span><span class="sxs-lookup"><span data-stu-id="cd8cf-127">The result of a compare property value restriction is undefined when one or both of the properties do not exist.</span></span> <span data-ttu-id="cd8cf-128">Cuando un cliente requiere un comportamiento bien definido para dicha restricción y no está seguro de si la propiedad existe (por ejemplo, no es una columna obligatoria de una tabla), debe crear una restricción **and** para unirse a la restricción de propiedad Compare con EXISTS. limitado.</span><span class="sxs-lookup"><span data-stu-id="cd8cf-128">When a client requires well-defined behavior for such a restriction and is not sure whether the property exists, (for example, it is not a required column of a table) it should create an **AND** restriction to join the compare property restriction with an exist restriction.</span></span> <span data-ttu-id="cd8cf-129">Use una estructura [SExistRestriction](sexistrestriction.md) para definir la restricción EXISTS y una estructura [SAndRestriction](sandrestriction.md) para definir la restricción **and** .</span><span class="sxs-lookup"><span data-stu-id="cd8cf-129">Use an [SExistRestriction](sexistrestriction.md) structure to define the exist restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="cd8cf-130">Las propiedades especificadas en los miembros **ulPropTag1** y **ulPropTag2** pueden tener varios valores si el proveedor de servicios lo admite.</span><span class="sxs-lookup"><span data-stu-id="cd8cf-130">The properties specified in the **ulPropTag1** and **ulPropTag2** members can be multi-valued if the service provider supports it.</span></span> 
  
<span data-ttu-id="cd8cf-131">Para obtener más información acerca de las restricciones y la estructura **SComparePropsRestriction** en general, consulte [About Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="cd8cf-131">For more information about the **SComparePropsRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cd8cf-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="cd8cf-132">See also</span></span>

- [<span data-ttu-id="cd8cf-133">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="cd8cf-133">SBitMaskRestriction</span></span>](sbitmaskrestriction.md)
- [<span data-ttu-id="cd8cf-134">SRestriction</span><span class="sxs-lookup"><span data-stu-id="cd8cf-134">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="cd8cf-135">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="cd8cf-135">MAPI Structures</span></span>](mapi-structures.md)

