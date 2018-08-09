---
title: FPropCompareProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropCompareProp
api_type:
- COM
ms.assetid: 17cb53c4-7154-4a4e-b4ec-de720fa055cb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 69bbed644a8173bf9291ca48a63960f693108318
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816870"
---
# <a name="fpropcompareprop"></a><span data-ttu-id="dc010-103">FPropCompareProp</span><span class="sxs-lookup"><span data-stu-id="dc010-103">FPropCompareProp</span></span>

<span data-ttu-id="dc010-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dc010-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dc010-105">Compara dos valores de propiedad con un operador relacional especificado.</span><span class="sxs-lookup"><span data-stu-id="dc010-105">Compares two property values using a specified relational operator.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dc010-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="dc010-106">Header file:</span></span>  <br/> |<span data-ttu-id="dc010-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="dc010-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="dc010-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="dc010-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="dc010-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="dc010-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="dc010-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="dc010-110">Called by:</span></span>  <br/> |<span data-ttu-id="dc010-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="dc010-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropCompareProp(
  LPSPropValue lpSPropValue1,
  ULONG ulRelOp,
  LPSPropValue lpSPropValue2
);
```

## <a name="parameters"></a><span data-ttu-id="dc010-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dc010-112">Parameters</span></span>

<span data-ttu-id="dc010-113">_lpSPropValue1_</span><span class="sxs-lookup"><span data-stu-id="dc010-113">_lpSPropValue1_</span></span>
  
> <span data-ttu-id="dc010-114">[entrada] Puntero a una estructura de [SPropValue](spropvalue.md) definir el primer valor de la propiedad para realizar una comparación.</span><span class="sxs-lookup"><span data-stu-id="dc010-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the first property value for comparison.</span></span> 
    
<span data-ttu-id="dc010-115">_ulRelOp_</span><span class="sxs-lookup"><span data-stu-id="dc010-115">_ulRelOp_</span></span>
  
> <span data-ttu-id="dc010-116">[entrada] El operador relacional para usar en la comparación.</span><span class="sxs-lookup"><span data-stu-id="dc010-116">[in] The relational operator to use in the comparison.</span></span> <span data-ttu-id="dc010-117">Para los valores permitidos, vea la estructura [SComparePropsRestriction](scomparepropsrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="dc010-117">For allowable values, see the [SComparePropsRestriction](scomparepropsrestriction.md) structure.</span></span> 
    
<span data-ttu-id="dc010-118">_lpSPropValue2_</span><span class="sxs-lookup"><span data-stu-id="dc010-118">_lpSPropValue2_</span></span>
  
> <span data-ttu-id="dc010-119">[entrada] Puntero a una estructura de **SPropValue** define el segundo valor de la propiedad para realizar una comparación.</span><span class="sxs-lookup"><span data-stu-id="dc010-119">[in] Pointer to an **SPropValue** structure defining the second property value for comparison.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dc010-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dc010-120">Return value</span></span>

<span data-ttu-id="dc010-121">TRUE</span><span class="sxs-lookup"><span data-stu-id="dc010-121">TRUE</span></span> 
  
> <span data-ttu-id="dc010-122">Los valores de propiedad cumplen al objeto relation especificado.</span><span class="sxs-lookup"><span data-stu-id="dc010-122">The property values satisfy the specified relation.</span></span> 
    
<span data-ttu-id="dc010-123">FALSE</span><span class="sxs-lookup"><span data-stu-id="dc010-123">FALSE</span></span> 
  
> <span data-ttu-id="dc010-124">Los valores de propiedad no cumplen con el objeto relation especificado.</span><span class="sxs-lookup"><span data-stu-id="dc010-124">The property values do not satisfy the specified relation.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dc010-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dc010-125">Remarks</span></span>

<span data-ttu-id="dc010-126">El método de comparación depende de los tipos de propiedad especificados en las definiciones de la propiedad [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="dc010-126">The comparison method depends on the property types specified in the [SPropValue](spropvalue.md) property definitions.</span></span> <span data-ttu-id="dc010-127">Las funciones **FPropCompareProp** y [FPropContainsProp](fpropcontainsprop.md) se pueden usar para preparar las restricciones para generar una tabla.</span><span class="sxs-lookup"><span data-stu-id="dc010-127">The **FPropCompareProp** and [FPropContainsProp](fpropcontainsprop.md) functions can be used to prepare restrictions for generating a table.</span></span> 
  
<span data-ttu-id="dc010-128">El orden de comparación es _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _.</span><span class="sxs-lookup"><span data-stu-id="dc010-128">The order of comparison is  _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _.</span></span> <span data-ttu-id="dc010-129">Si no coinciden con los tipos de propiedad de los valores de propiedad que se va a comparar, la función **FPropCompareProp** devuelve FALSE.</span><span class="sxs-lookup"><span data-stu-id="dc010-129">If the property types of the property values to be compared do not match, the **FPropCompareProp** function returns FALSE.</span></span> 
  

