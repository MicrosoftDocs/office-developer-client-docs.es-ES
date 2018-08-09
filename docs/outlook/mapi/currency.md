---
title: CURRENCY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CURRENCY
api_type:
- COM
ms.assetid: cffc05a0-95e4-4b9f-bf8f-c4272a75afa8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0789b566eb814fe984ae78670d22ad2937b0c3a5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816630"
---
# <a name="currency"></a><span data-ttu-id="4f7dd-103">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="4f7dd-103">CURRENCY</span></span>

  
  
<span data-ttu-id="4f7dd-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4f7dd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4f7dd-105">Contiene un entero de 64 bits con signo que representa un valor de moneda.</span><span class="sxs-lookup"><span data-stu-id="4f7dd-105">Contains a signed 64-bit integer representing a currency value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4f7dd-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="4f7dd-106">Header file:</span></span>  <br/> |<span data-ttu-id="4f7dd-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4f7dd-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct tagCY
{
  unsigned long Lo;
  long Hi;
} CURRENCY;

```

## <a name="members"></a><span data-ttu-id="4f7dd-108">Members</span><span class="sxs-lookup"><span data-stu-id="4f7dd-108">Members</span></span>

 <span data-ttu-id="4f7dd-109">**Lo**</span><span class="sxs-lookup"><span data-stu-id="4f7dd-109">**Lo**</span></span>
  
> <span data-ttu-id="4f7dd-110">32 bits de orden inferior del valor de moneda.</span><span class="sxs-lookup"><span data-stu-id="4f7dd-110">Low-order 32 bits of the currency value.</span></span> 
    
 <span data-ttu-id="4f7dd-111">**Hi**</span><span class="sxs-lookup"><span data-stu-id="4f7dd-111">**Hi**</span></span>
  
> <span data-ttu-id="4f7dd-112">32 bits de orden superior del valor de moneda.</span><span class="sxs-lookup"><span data-stu-id="4f7dd-112">High-order 32 bits of the currency value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4f7dd-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4f7dd-113">Remarks</span></span>

<span data-ttu-id="4f7dd-114">La estructura de **moneda** es una representación de entero con escala de un número decimal con cuatro dígitos a la derecha del separador decimal.</span><span class="sxs-lookup"><span data-stu-id="4f7dd-114">The **CURRENCY** structure is a scaled integer representation of a decimal number with four digits to the right of the decimal point.</span></span> <span data-ttu-id="4f7dd-115">Por ejemplo, un valor almacenado de 327500 es interpretarse como que representa un valor de moneda de 32.7500.</span><span class="sxs-lookup"><span data-stu-id="4f7dd-115">For example, a stored value of 327500 is to be construed as representing a currency value of 32.7500.</span></span> 
  
<span data-ttu-id="4f7dd-116">La estructura de **moneda** se usa para describir una propiedad de tipo PT_CURRENCY.</span><span class="sxs-lookup"><span data-stu-id="4f7dd-116">The **CURRENCY** structure is used to describe a property of type PT_CURRENCY.</span></span> <span data-ttu-id="4f7dd-117">Para obtener información acerca de los tipos de propiedad, vea [Información general sobre el tipo de propiedad MAPI](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4f7dd-117">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4f7dd-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f7dd-118">See also</span></span>



[<span data-ttu-id="4f7dd-119">SPropValue</span><span class="sxs-lookup"><span data-stu-id="4f7dd-119">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="4f7dd-120">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="4f7dd-120">MAPI Structures</span></span>](mapi-structures.md)

