---
title: SBitMaskRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBitMaskRestriction
api_type:
- COM
ms.assetid: ddd42180-6e4f-410c-9f78-d868a91452dc
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: afac8c352ad0a07fcb1cd98683b6a5c87940ab4d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424479"
---
# <a name="sbitmaskrestriction"></a><span data-ttu-id="bf31f-103">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="bf31f-103">SBitMaskRestriction</span></span>

  
  
<span data-ttu-id="bf31f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf31f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf31f-105">Describe una restricción de máscara de bits, que se usa para \*\*\*\* realizar una operación and bit a bit y probar el resultado.</span><span class="sxs-lookup"><span data-stu-id="bf31f-105">Describes a bitmask restriction, which is used to perform a bitwise **AND** operation and test the result.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bf31f-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="bf31f-106">Header file:</span></span>  <br/> |<span data-ttu-id="bf31f-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="bf31f-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBitMaskRestriction
{
  ULONG relBMR;
  PT_LONG ulPropTag;
  ULONG ulMask;
} SBitMaskRestriction;

```

## <a name="members"></a><span data-ttu-id="bf31f-108">Members</span><span class="sxs-lookup"><span data-stu-id="bf31f-108">Members</span></span>

 <span data-ttu-id="bf31f-109">**relBMR**</span><span class="sxs-lookup"><span data-stu-id="bf31f-109">**relBMR**</span></span>
  
> <span data-ttu-id="bf31f-110">Operador relacional que describe cómo se debe aplicar la máscara especificada en el miembro **ulMask** a la etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="bf31f-110">Relational operator that describes how the mask specified in the **ulMask** member should be applied to the property tag.</span></span> <span data-ttu-id="bf31f-111">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="bf31f-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="bf31f-112">BMR_EQZ</span><span class="sxs-lookup"><span data-stu-id="bf31f-112">BMR_EQZ</span></span> 
  
> <span data-ttu-id="bf31f-113">Realice una operación \*\*\*\* and bit a bit de la máscara en el miembro **ulMask** con la propiedad representada por el miembro **ulPropTag** y pruebe si es igual a cero.</span><span class="sxs-lookup"><span data-stu-id="bf31f-113">Perform a bitwise **AND** operation of the mask in the **ulMask** member with the property represented by the **ulPropTag** member and test for being equal to zero.</span></span> 
    
<span data-ttu-id="bf31f-114">BMR_NEZ</span><span class="sxs-lookup"><span data-stu-id="bf31f-114">BMR_NEZ</span></span> 
  
> <span data-ttu-id="bf31f-115">Realice una operación \*\*\*\* and bit a bit de la máscara en el miembro **ulMask** con la propiedad representada por el miembro **ulPropTag** y pruebe si no es igual a cero.</span><span class="sxs-lookup"><span data-stu-id="bf31f-115">Perform a bitwise **AND** operation of the mask in the **ulMask** member with the property represented by the **ulPropTag** member and test for being not equal to zero.</span></span> 
    
 <span data-ttu-id="bf31f-116">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="bf31f-116">**ulPropTag**</span></span>
  
> <span data-ttu-id="bf31f-117">Etiqueta de propiedad de la propiedad a la que se aplica la máscara de la máscara.</span><span class="sxs-lookup"><span data-stu-id="bf31f-117">Property tag of the property to which the bitmask is applied.</span></span>
    
 <span data-ttu-id="bf31f-118">**ulMask**</span><span class="sxs-lookup"><span data-stu-id="bf31f-118">**ulMask**</span></span>
  
> <span data-ttu-id="bf31f-119">Máscara de máscara para aplicar a la propiedad identificada por **ulPropTag**.</span><span class="sxs-lookup"><span data-stu-id="bf31f-119">Bitmask to apply to the property identified by **ulPropTag**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bf31f-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bf31f-120">Remarks</span></span>

<span data-ttu-id="bf31f-121">La estructura **SBitMaskRestriction** realiza una operación \*\*\*\* and bit a bit mediante la máscara de bits descrita en el miembro **ulMask** y el valor de la propiedad descrito por el miembro **ulPropTag** .</span><span class="sxs-lookup"><span data-stu-id="bf31f-121">The **SBitMaskRestriction** structure performs a bitwise **AND** operation using the bitmask described in the **ulMask** member and the value of the property described by the **ulPropTag** member.</span></span> <span data-ttu-id="bf31f-122">Si el resultado es cero, BMR_EQZ se cumple.</span><span class="sxs-lookup"><span data-stu-id="bf31f-122">If the result is zero, BMR_EQZ is satisfied.</span></span> <span data-ttu-id="bf31f-123">Si es distinto de cero, es decir, si el valor de la propiedad tiene al menos uno de los mismos bits establecidos que **ulMask**, entonces BMR_NEZ se cumple.</span><span class="sxs-lookup"><span data-stu-id="bf31f-123">If it is nonzero, that is, if the property value has at least one of the same bits set as **ulMask**, then BMR_NEZ is satisfied.</span></span>
  
<span data-ttu-id="bf31f-124">Para obtener más información acerca de las restricciones y la estructura **SBitMaskRestriction** en general, consulte [About Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="bf31f-124">For more information about the **SBitMaskRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bf31f-125">Ver también</span><span class="sxs-lookup"><span data-stu-id="bf31f-125">See also</span></span>



[<span data-ttu-id="bf31f-126">SRestriction</span><span class="sxs-lookup"><span data-stu-id="bf31f-126">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="bf31f-127">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="bf31f-127">MAPI Structures</span></span>](mapi-structures.md)

