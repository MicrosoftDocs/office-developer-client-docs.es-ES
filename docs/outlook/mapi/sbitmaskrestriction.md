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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: f0cf6fa03d8f38b7d160a8747111445cfdac1ae9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820558"
---
# <a name="sbitmaskrestriction"></a><span data-ttu-id="c68d3-103">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="c68d3-103">SBitMaskRestriction</span></span>

  
  
<span data-ttu-id="c68d3-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c68d3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c68d3-105">Describe una restricción de máscara de bits que se usa para realizar una operación **AND** bit a bit y el resultado de la prueba.</span><span class="sxs-lookup"><span data-stu-id="c68d3-105">Describes a bitmask restriction, which is used to perform a bitwise **AND** operation and test the result.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c68d3-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="c68d3-106">Header file:</span></span>  <br/> |<span data-ttu-id="c68d3-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c68d3-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBitMaskRestriction
{
  ULONG relBMR;
  PT_LONG ulPropTag;
  ULONG ulMask;
} SBitMaskRestriction;

```

## <a name="members"></a><span data-ttu-id="c68d3-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="c68d3-108">Members</span></span>

 <span data-ttu-id="c68d3-109">**relBMR**</span><span class="sxs-lookup"><span data-stu-id="c68d3-109">**relBMR**</span></span>
  
> <span data-ttu-id="c68d3-110">Operador relacional que describe cómo debe aplicarse la máscara especificada en el miembro **ulMask** en la etiqueta de propiedad.</span><span class="sxs-lookup"><span data-stu-id="c68d3-110">Relational operator that describes how the mask specified in the **ulMask** member should be applied to the property tag.</span></span> <span data-ttu-id="c68d3-111">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="c68d3-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="c68d3-112">BMR_EQZ</span><span class="sxs-lookup"><span data-stu-id="c68d3-112">BMR_EQZ</span></span> 
  
> <span data-ttu-id="c68d3-113">Realice una operación **AND** bit a bit de la máscara en el miembro **ulMask** con la propiedad representada por el miembro de **ulPropTag** y pruebas para es igual a cero.</span><span class="sxs-lookup"><span data-stu-id="c68d3-113">Perform a bitwise **AND** operation of the mask in the **ulMask** member with the property represented by the **ulPropTag** member and test for being equal to zero.</span></span> 
    
<span data-ttu-id="c68d3-114">BMR_NEZ</span><span class="sxs-lookup"><span data-stu-id="c68d3-114">BMR_NEZ</span></span> 
  
> <span data-ttu-id="c68d3-115">Realice una operación **AND** bit a bit de la máscara en el miembro **ulMask** con la propiedad representada por el miembro de **ulPropTag** y pruebas para no es igual a cero.</span><span class="sxs-lookup"><span data-stu-id="c68d3-115">Perform a bitwise **AND** operation of the mask in the **ulMask** member with the property represented by the **ulPropTag** member and test for being not equal to zero.</span></span> 
    
 <span data-ttu-id="c68d3-116">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="c68d3-116">**ulPropTag**</span></span>
  
> <span data-ttu-id="c68d3-117">Etiqueta de la propiedad de la propiedad a la que se aplica la máscara de bits.</span><span class="sxs-lookup"><span data-stu-id="c68d3-117">Property tag of the property to which the bitmask is applied.</span></span>
    
 <span data-ttu-id="c68d3-118">**ulMask**</span><span class="sxs-lookup"><span data-stu-id="c68d3-118">**ulMask**</span></span>
  
> <span data-ttu-id="c68d3-119">Máscara de bits que se aplican a la propiedad identificada por **ulPropTag**.</span><span class="sxs-lookup"><span data-stu-id="c68d3-119">Bitmask to apply to the property identified by **ulPropTag**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c68d3-120">Notas</span><span class="sxs-lookup"><span data-stu-id="c68d3-120">Remarks</span></span>

<span data-ttu-id="c68d3-121">La estructura **SBitMaskRestriction** realiza una operación **AND** bit a bit con la máscara de bits que se describen en el miembro **ulMask** y el valor de la propiedad descrito por el miembro **ulPropTag** .</span><span class="sxs-lookup"><span data-stu-id="c68d3-121">The **SBitMaskRestriction** structure performs a bitwise **AND** operation using the bitmask described in the **ulMask** member and the value of the property described by the **ulPropTag** member.</span></span> <span data-ttu-id="c68d3-122">Si el resultado es cero, se cumple BMR_EQZ.</span><span class="sxs-lookup"><span data-stu-id="c68d3-122">If the result is zero, BMR_EQZ is satisfied.</span></span> <span data-ttu-id="c68d3-123">Si es distinto de cero, es decir, si el valor de la propiedad tiene al menos uno de los mismos bits establecer como **ulMask**, a continuación, BMR_NEZ está satisfecho.</span><span class="sxs-lookup"><span data-stu-id="c68d3-123">If it is nonzero, that is, if the property value has at least one of the same bits set as **ulMask**, then BMR_NEZ is satisfied.</span></span>
  
<span data-ttu-id="c68d3-124">Para obtener más información sobre la estructura de **SBitMaskRestriction** y restricciones en general, vea [Acerca de las restricciones](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="c68d3-124">For more information about the **SBitMaskRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c68d3-125">Ver también</span><span class="sxs-lookup"><span data-stu-id="c68d3-125">See also</span></span>



[<span data-ttu-id="c68d3-126">SRestriction</span><span class="sxs-lookup"><span data-stu-id="c68d3-126">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="c68d3-127">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="c68d3-127">MAPI Structures</span></span>](mapi-structures.md)

