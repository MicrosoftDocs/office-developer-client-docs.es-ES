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
ms.openlocfilehash: d214cb5d449e2f7e42e7ee72774fdc146495adb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818053"
---
# <a name="lpropcompareprop"></a><span data-ttu-id="fa15e-103">LPropCompareProp</span><span class="sxs-lookup"><span data-stu-id="fa15e-103">LPropCompareProp</span></span>

  
  
<span data-ttu-id="fa15e-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fa15e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fa15e-105">Compara dos valores de propiedad para determinar si son iguales.</span><span class="sxs-lookup"><span data-stu-id="fa15e-105">Compares two property values to determine whether they are equal.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fa15e-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="fa15e-106">Header file:</span></span>  <br/> |<span data-ttu-id="fa15e-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="fa15e-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="fa15e-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="fa15e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fa15e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="fa15e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="fa15e-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="fa15e-110">Called by:</span></span>  <br/> |<span data-ttu-id="fa15e-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="fa15e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LONG LPropCompareProp(
  LPSPropValue lpSPropValueA,
  LPSPropValue lpSPropValueB
);
```

## <a name="parameters"></a><span data-ttu-id="fa15e-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fa15e-112">Parameters</span></span>

 <span data-ttu-id="fa15e-113">_lpSPropValueA_</span><span class="sxs-lookup"><span data-stu-id="fa15e-113">_lpSPropValueA_</span></span>
  
> <span data-ttu-id="fa15e-114">[entrada] Puntero a una estructura de [SPropValue](spropvalue.md) definir el primer valor de propiedad que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="fa15e-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the first property value to be compared.</span></span> 
    
 <span data-ttu-id="fa15e-115">_lpSPropValueB_</span><span class="sxs-lookup"><span data-stu-id="fa15e-115">_lpSPropValueB_</span></span>
  
> <span data-ttu-id="fa15e-116">[entrada] Puntero a una estructura de **SPropValue** define el segundo valor de propiedad que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="fa15e-116">[in] Pointer to an **SPropValue** structure defining the second property value to be compared.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fa15e-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fa15e-117">Return value</span></span>

 <span data-ttu-id="fa15e-118">**LPropCompareProp** devuelve uno de los siguientes valores para la mayoría de los tipos de propiedad:</span><span class="sxs-lookup"><span data-stu-id="fa15e-118">**LPropCompareProp** returns one of the following values for most property types:</span></span> 
  
- <span data-ttu-id="fa15e-119">Menor que cero si el valor indicado por el parámetro _lpSPropValueA_ es menor que la indicada por el parámetro _lpSPropValueB_ .</span><span class="sxs-lookup"><span data-stu-id="fa15e-119">Less than zero if the value indicated by the  _lpSPropValueA_ parameter is less than that indicated by the  _lpSPropValueB_ parameter.</span></span> 
    
- <span data-ttu-id="fa15e-120">Mayor que cero si el valor indicado por _lpSPropValueA_ es mayor que el indicado por _lpSPropValueB_.</span><span class="sxs-lookup"><span data-stu-id="fa15e-120">Greater than zero if the value indicated by  _lpSPropValueA_ is greater than that indicated by  _lpSPropValueB_.</span></span>
    
- <span data-ttu-id="fa15e-121">Cero si el valor indicado por _lpSPropValueA_ es igual al valor indicado por _lpSPropValueB_.</span><span class="sxs-lookup"><span data-stu-id="fa15e-121">Zero if the value indicated by  _lpSPropValueA_ equals the value indicated by  _lpSPropValueB_.</span></span> 
    
<span data-ttu-id="fa15e-122">Para los tipos de propiedad que no tienen ningún orden intrínsecas, como Boolean o error, la función **LPropCompareProp** devuelve un valor undefined si los valores de dos propiedad no son iguales.</span><span class="sxs-lookup"><span data-stu-id="fa15e-122">For property types that have no intrinsic ordering, such as Boolean or error types, the **LPropCompareProp** function returns an undefined value if the two property values are not equal.</span></span> <span data-ttu-id="fa15e-123">Este valor undefined es distinto de cero y coherente a través de llamadas.</span><span class="sxs-lookup"><span data-stu-id="fa15e-123">This undefined value is nonzero and consistent across calls.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fa15e-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fa15e-124">Remarks</span></span>

<span data-ttu-id="fa15e-125">Use la función **LPropCompareProp** sólo si los tipos de las dos propiedades que se va a comparar son las mismas.</span><span class="sxs-lookup"><span data-stu-id="fa15e-125">Use the **LPropCompareProp** function only if the types of the two properties to be compared are the same.</span></span> 
  
<span data-ttu-id="fa15e-126">Antes de llamar a **LPropCompareProp**, una aplicación de cliente o un proveedor de servicios en primer lugar debe recuperar las propiedades para realizar una comparación con una llamada al método [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="fa15e-126">Before calling **LPropCompareProp**, a client application or service provider must first retrieve the properties for comparison with a call to the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="fa15e-127">Cuando un cliente o proveedor de llamadas **LPropCompareProp**, la función primero examina las etiquetas de propiedad para asegurarse de la comparación de valores de propiedad es válida.</span><span class="sxs-lookup"><span data-stu-id="fa15e-127">When a client or provider calls **LPropCompareProp**, the function first examines the property tags to make sure that the comparison of property values is valid.</span></span> <span data-ttu-id="fa15e-128">La función, a continuación, compara los valores de propiedad, devolver un valor apropiado.</span><span class="sxs-lookup"><span data-stu-id="fa15e-128">The function then compares the property values, returning an appropriate value.</span></span> 
  
<span data-ttu-id="fa15e-129">Si los valores de propiedad no son iguales, **LPropCompareProp** determina cuál es el mayor.</span><span class="sxs-lookup"><span data-stu-id="fa15e-129">If the property values are unequal, **LPropCompareProp** determines which one is the greater.</span></span> <span data-ttu-id="fa15e-130">No es necesario que las propiedades que se comparan **LPropCompareProp** pertenecen al mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="fa15e-130">The properties that **LPropCompareProp** compares do not have to belong to the same object.</span></span> 
  

