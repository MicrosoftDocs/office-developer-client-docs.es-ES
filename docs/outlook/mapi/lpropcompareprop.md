---
title: LPropCompareProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LPropCompareProp
api_type:
- COM
ms.assetid: f14ad568-fe45-4875-957d-415d39dc6f28
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7417ddeb814cafb954d5ab80a6dae771fd0f7a79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357438"
---
# <a name="lpropcompareprop"></a><span data-ttu-id="e6038-103">LPropCompareProp</span><span class="sxs-lookup"><span data-stu-id="e6038-103">LPropCompareProp</span></span>

  
  
<span data-ttu-id="e6038-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6038-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6038-105">Compara dos valores de propiedad para determinar si son iguales.</span><span class="sxs-lookup"><span data-stu-id="e6038-105">Compares two property values to determine whether they are equal.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e6038-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="e6038-106">Header file:</span></span>  <br/> |<span data-ttu-id="e6038-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="e6038-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e6038-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="e6038-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e6038-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e6038-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e6038-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="e6038-110">Called by:</span></span>  <br/> |<span data-ttu-id="e6038-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="e6038-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LONG LPropCompareProp(
  LPSPropValue lpSPropValueA,
  LPSPropValue lpSPropValueB
);
```

## <a name="parameters"></a><span data-ttu-id="e6038-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="e6038-112">Parameters</span></span>

 <span data-ttu-id="e6038-113">_lpSPropValueA_</span><span class="sxs-lookup"><span data-stu-id="e6038-113">_lpSPropValueA_</span></span>
  
> <span data-ttu-id="e6038-114">a Puntero a una estructura [SPropValue](spropvalue.md) que define el primer valor de la propiedad que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="e6038-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the first property value to be compared.</span></span> 
    
 <span data-ttu-id="e6038-115">_lpSPropValueB_</span><span class="sxs-lookup"><span data-stu-id="e6038-115">_lpSPropValueB_</span></span>
  
> <span data-ttu-id="e6038-116">a Puntero a una estructura **SPropValue** que define el segundo valor de la propiedad que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="e6038-116">[in] Pointer to an **SPropValue** structure defining the second property value to be compared.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e6038-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e6038-117">Return value</span></span>

 <span data-ttu-id="e6038-118">**LPropCompareProp** devuelve uno de los siguientes valores para la mayoría de los tipos de propiedades:</span><span class="sxs-lookup"><span data-stu-id="e6038-118">**LPropCompareProp** returns one of the following values for most property types:</span></span> 
  
- <span data-ttu-id="e6038-119">Menor que cero si el valor indicado por el parámetro _lpSPropValueA_ es menor que el indicado por el parámetro _lpSPropValueB_ .</span><span class="sxs-lookup"><span data-stu-id="e6038-119">Less than zero if the value indicated by the  _lpSPropValueA_ parameter is less than that indicated by the  _lpSPropValueB_ parameter.</span></span> 
    
- <span data-ttu-id="e6038-120">Mayor que cero si el valor indicado por _lpSPropValueA_ es mayor que el indicado por _lpSPropValueB_.</span><span class="sxs-lookup"><span data-stu-id="e6038-120">Greater than zero if the value indicated by  _lpSPropValueA_ is greater than that indicated by  _lpSPropValueB_.</span></span>
    
- <span data-ttu-id="e6038-121">Cero si el valor indicado por _lpSPropValueA_ es igual al valor indicado por _lpSPropValueB_.</span><span class="sxs-lookup"><span data-stu-id="e6038-121">Zero if the value indicated by  _lpSPropValueA_ equals the value indicated by  _lpSPropValueB_.</span></span> 
    
<span data-ttu-id="e6038-122">Para los tipos de propiedad que no tienen ninguna ordenación intrínseca, como los tipos booleanos o de error, la función **LPropCompareProp** devuelve un valor no definido si los dos valores de propiedad no son iguales.</span><span class="sxs-lookup"><span data-stu-id="e6038-122">For property types that have no intrinsic ordering, such as Boolean or error types, the **LPropCompareProp** function returns an undefined value if the two property values are not equal.</span></span> <span data-ttu-id="e6038-123">Este valor no definido es distinto de cero y es coherente en todas las llamadas.</span><span class="sxs-lookup"><span data-stu-id="e6038-123">This undefined value is nonzero and consistent across calls.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e6038-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e6038-124">Remarks</span></span>

<span data-ttu-id="e6038-125">Use la función **LPropCompareProp** sólo si los tipos de las dos propiedades que se van a comparar son iguales.</span><span class="sxs-lookup"><span data-stu-id="e6038-125">Use the **LPropCompareProp** function only if the types of the two properties to be compared are the same.</span></span> 
  
<span data-ttu-id="e6038-126">Antes de llamar a **LPropCompareProp**, una aplicación cliente o un proveedor de servicios debe recuperar primero las propiedades para la comparación con una llamada al método [IMAPIProp:: GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="e6038-126">Before calling **LPropCompareProp**, a client application or service provider must first retrieve the properties for comparison with a call to the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="e6038-127">Cuando un cliente o proveedor llama a **LPropCompareProp**, la función examina primero las etiquetas de propiedad para asegurarse de que la comparación de valores de propiedad es válida.</span><span class="sxs-lookup"><span data-stu-id="e6038-127">When a client or provider calls **LPropCompareProp**, the function first examines the property tags to make sure that the comparison of property values is valid.</span></span> <span data-ttu-id="e6038-128">A continuación, la función compara los valores de la propiedad y devuelve un valor adecuado.</span><span class="sxs-lookup"><span data-stu-id="e6038-128">The function then compares the property values, returning an appropriate value.</span></span> 
  
<span data-ttu-id="e6038-129">Si los valores de la propiedad no son iguales, **LPropCompareProp** determina cuál es el mayor.</span><span class="sxs-lookup"><span data-stu-id="e6038-129">If the property values are unequal, **LPropCompareProp** determines which one is the greater.</span></span> <span data-ttu-id="e6038-130">Las propiedades que comparan **LPropCompareProp** no tienen que pertenecer al mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="e6038-130">The properties that **LPropCompareProp** compares do not have to belong to the same object.</span></span> 
  

