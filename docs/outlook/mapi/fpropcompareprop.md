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
ms.openlocfilehash: adccbaf65adec2c517c4890f722198e8262092cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564608"
---
# <a name="fpropcompareprop"></a><span data-ttu-id="47ab5-103">FPropCompareProp</span><span class="sxs-lookup"><span data-stu-id="47ab5-103">FPropCompareProp</span></span>

<span data-ttu-id="47ab5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47ab5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47ab5-105">Compara dos valores de propiedad con un operador relacional especificado.</span><span class="sxs-lookup"><span data-stu-id="47ab5-105">Compares two property values using a specified relational operator.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="47ab5-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="47ab5-106">Header file:</span></span>  <br/> |<span data-ttu-id="47ab5-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="47ab5-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="47ab5-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="47ab5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="47ab5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="47ab5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="47ab5-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="47ab5-110">Called by:</span></span>  <br/> |<span data-ttu-id="47ab5-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="47ab5-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropCompareProp(
  LPSPropValue lpSPropValue1,
  ULONG ulRelOp,
  LPSPropValue lpSPropValue2
);
```

## <a name="parameters"></a><span data-ttu-id="47ab5-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47ab5-112">Parameters</span></span>

<span data-ttu-id="47ab5-113">_lpSPropValue1_</span><span class="sxs-lookup"><span data-stu-id="47ab5-113">_lpSPropValue1_</span></span>
  
> <span data-ttu-id="47ab5-114">[entrada] Puntero a una estructura de [SPropValue](spropvalue.md) definir el primer valor de la propiedad para realizar una comparación.</span><span class="sxs-lookup"><span data-stu-id="47ab5-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the first property value for comparison.</span></span> 
    
<span data-ttu-id="47ab5-115">_ulRelOp_</span><span class="sxs-lookup"><span data-stu-id="47ab5-115">_ulRelOp_</span></span>
  
> <span data-ttu-id="47ab5-116">[entrada] El operador relacional para usar en la comparación.</span><span class="sxs-lookup"><span data-stu-id="47ab5-116">[in] The relational operator to use in the comparison.</span></span> <span data-ttu-id="47ab5-117">Para los valores permitidos, vea la estructura [SComparePropsRestriction](scomparepropsrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="47ab5-117">For allowable values, see the [SComparePropsRestriction](scomparepropsrestriction.md) structure.</span></span> 
    
<span data-ttu-id="47ab5-118">_lpSPropValue2_</span><span class="sxs-lookup"><span data-stu-id="47ab5-118">_lpSPropValue2_</span></span>
  
> <span data-ttu-id="47ab5-119">[entrada] Puntero a una estructura de **SPropValue** define el segundo valor de la propiedad para realizar una comparación.</span><span class="sxs-lookup"><span data-stu-id="47ab5-119">[in] Pointer to an **SPropValue** structure defining the second property value for comparison.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="47ab5-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="47ab5-120">Return value</span></span>

<span data-ttu-id="47ab5-121">TRUE</span><span class="sxs-lookup"><span data-stu-id="47ab5-121">TRUE</span></span> 
  
> <span data-ttu-id="47ab5-122">Los valores de propiedad cumplen al objeto relation especificado.</span><span class="sxs-lookup"><span data-stu-id="47ab5-122">The property values satisfy the specified relation.</span></span> 
    
<span data-ttu-id="47ab5-123">FALSE</span><span class="sxs-lookup"><span data-stu-id="47ab5-123">FALSE</span></span> 
  
> <span data-ttu-id="47ab5-124">Los valores de propiedad no cumplen con el objeto relation especificado.</span><span class="sxs-lookup"><span data-stu-id="47ab5-124">The property values do not satisfy the specified relation.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="47ab5-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="47ab5-125">Remarks</span></span>

<span data-ttu-id="47ab5-126">El método de comparación depende de los tipos de propiedad especificados en las definiciones de la propiedad [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="47ab5-126">The comparison method depends on the property types specified in the [SPropValue](spropvalue.md) property definitions.</span></span> <span data-ttu-id="47ab5-127">Las funciones **FPropCompareProp** y [FPropContainsProp](fpropcontainsprop.md) se pueden usar para preparar las restricciones para generar una tabla.</span><span class="sxs-lookup"><span data-stu-id="47ab5-127">The **FPropCompareProp** and [FPropContainsProp](fpropcontainsprop.md) functions can be used to prepare restrictions for generating a table.</span></span> 
  
<span data-ttu-id="47ab5-128">El orden de comparación es _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _.</span><span class="sxs-lookup"><span data-stu-id="47ab5-128">The order of comparison is  _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _.</span></span> <span data-ttu-id="47ab5-129">Si no coinciden con los tipos de propiedad de los valores de propiedad que se va a comparar, la función **FPropCompareProp** devuelve FALSE.</span><span class="sxs-lookup"><span data-stu-id="47ab5-129">If the property types of the property values to be compared do not match, the **FPropCompareProp** function returns FALSE.</span></span> 
  

