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
ms.openlocfilehash: dccb6b19af72d0f748a3a513b7f3d78904ebc789
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315137"
---
# <a name="currency"></a><span data-ttu-id="d8b14-103">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="d8b14-103">CURRENCY</span></span>

  
  
<span data-ttu-id="d8b14-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8b14-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8b14-105">Contiene un entero de 64 bits firmado que representa un valor de moneda.</span><span class="sxs-lookup"><span data-stu-id="d8b14-105">Contains a signed 64-bit integer representing a currency value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d8b14-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d8b14-106">Header file:</span></span>  <br/> |<span data-ttu-id="d8b14-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="d8b14-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct tagCY
{
  unsigned long Lo;
  long Hi;
} CURRENCY;

```

## <a name="members"></a><span data-ttu-id="d8b14-108">Members</span><span class="sxs-lookup"><span data-stu-id="d8b14-108">Members</span></span>

 <span data-ttu-id="d8b14-109">**Mínimos**</span><span class="sxs-lookup"><span data-stu-id="d8b14-109">**Lo**</span></span>
  
> <span data-ttu-id="d8b14-110">32 bits de orden inferior del valor de moneda.</span><span class="sxs-lookup"><span data-stu-id="d8b14-110">Low-order 32 bits of the currency value.</span></span> 
    
 <span data-ttu-id="d8b14-111">**Tal**</span><span class="sxs-lookup"><span data-stu-id="d8b14-111">**Hi**</span></span>
  
> <span data-ttu-id="d8b14-112">32 bits de orden superior del valor de moneda.</span><span class="sxs-lookup"><span data-stu-id="d8b14-112">High-order 32 bits of the currency value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d8b14-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d8b14-113">Remarks</span></span>

<span data-ttu-id="d8b14-114">La estructura de **moneda** es una representación de enteros a escala de un número decimal con cuatro dígitos a la derecha de la coma decimal.</span><span class="sxs-lookup"><span data-stu-id="d8b14-114">The **CURRENCY** structure is a scaled integer representation of a decimal number with four digits to the right of the decimal point.</span></span> <span data-ttu-id="d8b14-115">Por ejemplo, un valor almacenado de 327500 se debe interpretar como que representa un valor de moneda de 32,7500.</span><span class="sxs-lookup"><span data-stu-id="d8b14-115">For example, a stored value of 327500 is to be construed as representing a currency value of 32.7500.</span></span> 
  
<span data-ttu-id="d8b14-116">La estructura de **divisa** se usa para describir una propiedad de tipo PT_CURRENCY.</span><span class="sxs-lookup"><span data-stu-id="d8b14-116">The **CURRENCY** structure is used to describe a property of type PT_CURRENCY.</span></span> <span data-ttu-id="d8b14-117">Para obtener información acerca de los tipos de propiedades, consulte [MAPI Property Type Overview](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d8b14-117">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d8b14-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8b14-118">See also</span></span>



[<span data-ttu-id="d8b14-119">SPropValue</span><span class="sxs-lookup"><span data-stu-id="d8b14-119">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="d8b14-120">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="d8b14-120">MAPI Structures</span></span>](mapi-structures.md)

