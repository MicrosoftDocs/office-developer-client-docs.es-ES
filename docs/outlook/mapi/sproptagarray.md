---
title: SPropTagArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropTagArray
api_type:
- COM
ms.assetid: 4a9e1579-bebe-4a51-8ced-6dba9c3bcb63
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9a5be98298ab1f9333ac1c223a6ef594e60dd86a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430703"
---
# <a name="sproptagarray"></a><span data-ttu-id="d88f2-103">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="d88f2-103">SPropTagArray</span></span>

  
  
<span data-ttu-id="d88f2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d88f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d88f2-105">Contiene una matriz de etiquetas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="d88f2-105">Contains an array of property tags.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d88f2-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d88f2-106">Header file:</span></span>  <br/> |<span data-ttu-id="d88f2-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="d88f2-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="d88f2-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="d88f2-108">Related macros:</span></span>  <br/> |<span data-ttu-id="d88f2-109">[CbNewSPropTagArray](cbnewsproptagarray.md), [CbSPropTagArray](cbsproptagarray.md), [SizedSPropTagArray](sizedsproptagarray.md)</span><span class="sxs-lookup"><span data-stu-id="d88f2-109">[CbNewSPropTagArray](cbnewsproptagarray.md), [CbSPropTagArray](cbsproptagarray.md), [SizedSPropTagArray](sizedsproptagarray.md)</span></span> <br/> |
   
```cpp
typedef struct _SPropTagArray
{
  ULONG cValues;
  ULONG aulPropTag[MAPI_DIM];
} SPropTagArray, FAR *LPSPropTagArray;

```

## <a name="members"></a><span data-ttu-id="d88f2-110">Members</span><span class="sxs-lookup"><span data-stu-id="d88f2-110">Members</span></span>

 <span data-ttu-id="d88f2-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="d88f2-111">**cValues**</span></span>
  
> <span data-ttu-id="d88f2-112">Número de etiquetas de propiedad en la matriz indicada por el miembro **aulPropTag** .</span><span class="sxs-lookup"><span data-stu-id="d88f2-112">Count of property tags in the array indicated by the **aulPropTag** member.</span></span> 
    
 <span data-ttu-id="d88f2-113">**aulPropTag**</span><span class="sxs-lookup"><span data-stu-id="d88f2-113">**aulPropTag**</span></span>
  
> <span data-ttu-id="d88f2-114">Matriz de etiquetas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="d88f2-114">Array of property tags.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d88f2-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d88f2-115">Remarks</span></span>

<span data-ttu-id="d88f2-116">Una etiqueta de propiedad es un entero de 32 bits sin signo que consta de dos partes:</span><span class="sxs-lookup"><span data-stu-id="d88f2-116">A property tag is a 32-bit unsigned integer that consists of two parts:</span></span> 
  
- <span data-ttu-id="d88f2-117">Un identificador en los 16 bits de orden superior.</span><span class="sxs-lookup"><span data-stu-id="d88f2-117">An identifier in the high-order 16 bits.</span></span>
    
- <span data-ttu-id="d88f2-118">Un tipo en los 16 bits de orden inferior.</span><span class="sxs-lookup"><span data-stu-id="d88f2-118">A type in the low-order 16 bits.</span></span>
    
<span data-ttu-id="d88f2-119">El identificador es un valor numérico en un intervalo determinado.</span><span class="sxs-lookup"><span data-stu-id="d88f2-119">The identifier is a numeric value in a particular range.</span></span> <span data-ttu-id="d88f2-120">MAPI define los intervalos de los identificadores para describir para qué se usa la propiedad y quién es responsable de su mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="d88f2-120">MAPI defines ranges for identifiers to describe what the property is used for and who is responsible for maintaining it.</span></span> <span data-ttu-id="d88f2-121">MAPI define restricciones para cada una de las etiquetas de propiedad que admite en el archivo de encabezado Mapitags. h.</span><span class="sxs-lookup"><span data-stu-id="d88f2-121">MAPI defines constraints for each of the property tags that it supports in the Mapitags.h header file.</span></span>
  
<span data-ttu-id="d88f2-122">El tipo indica el formato del valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="d88f2-122">The type indicates the format for the property's value.</span></span> <span data-ttu-id="d88f2-123">MAPI define constantes para cada uno de los tipos de propiedad que admite en el archivo de encabezado Mapidefs. h.</span><span class="sxs-lookup"><span data-stu-id="d88f2-123">MAPI defines constants for each of the property types that it supports in the Mapidefs.h header file.</span></span> 
  
<span data-ttu-id="d88f2-124">Para obtener más información acerca de las etiquetas de propiedad y sus componentes, consulte uno de los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="d88f2-124">For more information about property tags and their components, see one of the following topics:</span></span> 
  
[<span data-ttu-id="d88f2-125">Etiquetas de propiedad MAPI</span><span class="sxs-lookup"><span data-stu-id="d88f2-125">MAPI Property Tags</span></span>](mapi-property-tags.md)
  
[<span data-ttu-id="d88f2-126">Información general del identificador de propiedad MAPI</span><span class="sxs-lookup"><span data-stu-id="d88f2-126">MAPI Property Identifier Overview</span></span>](mapi-property-identifier-overview.md)
  
[<span data-ttu-id="d88f2-127">Información general del tipo de propiedad MAPI</span><span class="sxs-lookup"><span data-stu-id="d88f2-127">MAPI Property Type Overview</span></span>](mapi-property-type-overview.md)
  
<span data-ttu-id="d88f2-128">Para obtener una lista completa de los tipos de propiedad de valor único y de varios valores, vea el apéndice, [identificadores y tipos de propiedades](property-identifiers-and-types.md).</span><span class="sxs-lookup"><span data-stu-id="d88f2-128">For a complete list of the single-valued and multi-valued property types, see the appendix, [Property Identifiers and Types](property-identifiers-and-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d88f2-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="d88f2-129">See also</span></span>



[<span data-ttu-id="d88f2-130">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="d88f2-130">MAPI Structures</span></span>](mapi-structures.md)

