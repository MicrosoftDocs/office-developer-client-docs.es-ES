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
ms.openlocfilehash: 6ebc4e9cbc79a71a91f1f2f3eec0d40de979ab18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820586"
---
# <a name="scomparepropsrestriction"></a><span data-ttu-id="b185d-103">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="b185d-103">SComparePropsRestriction</span></span>

<span data-ttu-id="b185d-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b185d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b185d-105">Describe una restricción de propiedad compare, que comprueba las propiedades de dos con un operador relacional.</span><span class="sxs-lookup"><span data-stu-id="b185d-105">Describes a compare property restriction, which tests two properties using a relational operator.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b185d-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="b185d-106">Header file:</span></span>  <br/> |<span data-ttu-id="b185d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b185d-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SComparePropsRestriction
{
  ULONG relop;
  ULONG ulPropTag1;
  ULONG ulPropTag2;
} SComparePropsRestriction;

```

## <a name="members"></a><span data-ttu-id="b185d-108">Members</span><span class="sxs-lookup"><span data-stu-id="b185d-108">Members</span></span>

<span data-ttu-id="b185d-109">**RelOp**</span><span class="sxs-lookup"><span data-stu-id="b185d-109">**relop**</span></span>
  
> <span data-ttu-id="b185d-110">Operador relacional debe usar para comparar las dos propiedades.</span><span class="sxs-lookup"><span data-stu-id="b185d-110">Relational operator to use to compare the two properties.</span></span> <span data-ttu-id="b185d-111">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b185d-111">Possible values are as follows:</span></span>
    
  - <span data-ttu-id="b185d-112">RELOP_GE: Se realiza la comparación basándose en el primer valor mayor o igual.</span><span class="sxs-lookup"><span data-stu-id="b185d-112">RELOP_GE: The comparison is made based on a greater or equal first value.</span></span>
      
  - <span data-ttu-id="b185d-113">RELOP_GT: Se realiza la comparación basándose en un valor mayor de primera.</span><span class="sxs-lookup"><span data-stu-id="b185d-113">RELOP_GT: The comparison is made based on a greater first value.</span></span>
      
  - <span data-ttu-id="b185d-114">RELOP_LE: Se realiza la comparación basándose en el primer valor menor o igual.</span><span class="sxs-lookup"><span data-stu-id="b185d-114">RELOP_LE: The comparison is made based on a lesser or equal first value.</span></span>
      
  - <span data-ttu-id="b185d-115">RELOP_LT: Se realiza la comparación basándose en un valor menor de primera.</span><span class="sxs-lookup"><span data-stu-id="b185d-115">RELOP_LT: The comparison is made based on a lesser first value.</span></span>
      
  - <span data-ttu-id="b185d-116">RELOP_NE: Se realiza la comparación basándose en valores desiguales.</span><span class="sxs-lookup"><span data-stu-id="b185d-116">RELOP_NE: The comparison is made based on unequal values.</span></span>
      
  - <span data-ttu-id="b185d-117">RELOP_RE: La comparación se realiza en función de como valores (expresión regular).</span><span class="sxs-lookup"><span data-stu-id="b185d-117">RELOP_RE: The comparison is made based on LIKE (regular expression) values.</span></span>
      
  - <span data-ttu-id="b185d-118">RELOP_EQ: Se realiza la comparación basándose en valores iguales.</span><span class="sxs-lookup"><span data-stu-id="b185d-118">RELOP_EQ: The comparison is made based on equal values.</span></span>
    
<span data-ttu-id="b185d-119">**ulPropTag1**</span><span class="sxs-lookup"><span data-stu-id="b185d-119">**ulPropTag1**</span></span>
  
> <span data-ttu-id="b185d-120">Etiqueta de propiedad de la primera propiedad que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="b185d-120">Property tag of the first property to be compared.</span></span> 
    
<span data-ttu-id="b185d-121">**ulPropTag2**</span><span class="sxs-lookup"><span data-stu-id="b185d-121">**ulPropTag2**</span></span>
  
> <span data-ttu-id="b185d-122">Etiqueta de propiedad de la segunda propiedad que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="b185d-122">Property tag of the second property to be compared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b185d-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b185d-123">Remarks</span></span>

<span data-ttu-id="b185d-124">El orden de comparación es _(etiqueta de la propiedad (1) (operador relacional) (etiqueta de la propiedad 2)_.</span><span class="sxs-lookup"><span data-stu-id="b185d-124">The comparison order is  _(property tag 1) (relational operator) (property tag 2)_.</span></span> <span data-ttu-id="b185d-125">Las propiedades que se va a comparar con deben ser del mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="b185d-125">The properties to be compared must be of the same type.</span></span> <span data-ttu-id="b185d-126">Si se intenta comparar las propiedades de distintos tipos hace que MAPI o el proveedor de servicios devolver el valor de error MAPI_E_TOO_COMPLEX desde el método [IMAPITable](imapitableiunknown.md) a la que la estructura se pasa como un parámetro.</span><span class="sxs-lookup"><span data-stu-id="b185d-126">Attempting to compare properties of different types causes MAPI or the service provider to return the error value MAPI_E_TOO_COMPLEX from the [IMAPITable](imapitableiunknown.md) method to which the structure is passed as a parameter.</span></span> 
  
<span data-ttu-id="b185d-127">El resultado de una restricción de valor de propiedad de compare no está definido cuando uno o ambos de las propiedades no existen.</span><span class="sxs-lookup"><span data-stu-id="b185d-127">The result of a compare property value restriction is undefined when one or both of the properties do not exist.</span></span> <span data-ttu-id="b185d-128">Cuando un cliente requiere un comportamiento bien definido para esta restricción y no está seguro de si existe la propiedad, (por ejemplo, no es una columna de una tabla necesaria) debe crear una restricción **y** para unirse a la restricción de propiedad comparar con un existe restricción.</span><span class="sxs-lookup"><span data-stu-id="b185d-128">When a client requires well-defined behavior for such a restriction and is not sure whether the property exists, (for example, it is not a required column of a table) it should create an **AND** restriction to join the compare property restriction with an exist restriction.</span></span> <span data-ttu-id="b185d-129">Usar una estructura [SExistRestriction](sexistrestriction.md) para definir la restricción existe y una estructura [SAndRestriction](sandrestriction.md) para definir la restricción de **y** .</span><span class="sxs-lookup"><span data-stu-id="b185d-129">Use an [SExistRestriction](sexistrestriction.md) structure to define the exist restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="b185d-130">Las propiedades especificadas en los miembros **ulPropTag1** y **ulPropTag2** pueden ser multivalor si lo admite el proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="b185d-130">The properties specified in the **ulPropTag1** and **ulPropTag2** members can be multi-valued if the service provider supports it.</span></span> 
  
<span data-ttu-id="b185d-131">Para obtener más información sobre la estructura de **SComparePropsRestriction** y restricciones en general, vea [Acerca de las restricciones](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="b185d-131">For more information about the **SComparePropsRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b185d-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="b185d-132">See also</span></span>

- [<span data-ttu-id="b185d-133">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="b185d-133">SBitMaskRestriction</span></span>](sbitmaskrestriction.md)
- [<span data-ttu-id="b185d-134">SRestriction</span><span class="sxs-lookup"><span data-stu-id="b185d-134">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="b185d-135">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="b185d-135">MAPI Structures</span></span>](mapi-structures.md)

