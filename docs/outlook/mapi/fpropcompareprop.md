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
ms.openlocfilehash: 7726811467324242037ec11a69ae0b1b123d7f21
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427160"
---
# <a name="fpropcompareprop"></a><span data-ttu-id="2648f-103">FPropCompareProp</span><span class="sxs-lookup"><span data-stu-id="2648f-103">FPropCompareProp</span></span>

<span data-ttu-id="2648f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2648f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2648f-105">Compara dos valores de propiedad mediante un operador relacional especificado.</span><span class="sxs-lookup"><span data-stu-id="2648f-105">Compares two property values using a specified relational operator.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2648f-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="2648f-106">Header file:</span></span>  <br/> |<span data-ttu-id="2648f-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="2648f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="2648f-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="2648f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2648f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2648f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2648f-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="2648f-110">Called by:</span></span>  <br/> |<span data-ttu-id="2648f-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="2648f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropCompareProp(
  LPSPropValue lpSPropValue1,
  ULONG ulRelOp,
  LPSPropValue lpSPropValue2
);
```

## <a name="parameters"></a><span data-ttu-id="2648f-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="2648f-112">Parameters</span></span>

<span data-ttu-id="2648f-113">_lpSPropValue1_</span><span class="sxs-lookup"><span data-stu-id="2648f-113">_lpSPropValue1_</span></span>
  
> <span data-ttu-id="2648f-114">[in] Puntero a una [estructura SPropValue](spropvalue.md) que define el primer valor de propiedad para la comparación.</span><span class="sxs-lookup"><span data-stu-id="2648f-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the first property value for comparison.</span></span> 
    
<span data-ttu-id="2648f-115">_ulRelOp_</span><span class="sxs-lookup"><span data-stu-id="2648f-115">_ulRelOp_</span></span>
  
> <span data-ttu-id="2648f-116">[in] Operador relacional que se usará en la comparación.</span><span class="sxs-lookup"><span data-stu-id="2648f-116">[in] The relational operator to use in the comparison.</span></span> <span data-ttu-id="2648f-117">Para obtener valores permitidos, vea la [estructura SComparePropsRestriction.](scomparepropsrestriction.md)</span><span class="sxs-lookup"><span data-stu-id="2648f-117">For allowable values, see the [SComparePropsRestriction](scomparepropsrestriction.md) structure.</span></span> 
    
<span data-ttu-id="2648f-118">_lpSPropValue2_</span><span class="sxs-lookup"><span data-stu-id="2648f-118">_lpSPropValue2_</span></span>
  
> <span data-ttu-id="2648f-119">[in] Puntero a una **estructura SPropValue** que define el segundo valor de propiedad para la comparación.</span><span class="sxs-lookup"><span data-stu-id="2648f-119">[in] Pointer to an **SPropValue** structure defining the second property value for comparison.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2648f-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2648f-120">Return value</span></span>

<span data-ttu-id="2648f-121">TRUE</span><span class="sxs-lookup"><span data-stu-id="2648f-121">TRUE</span></span> 
  
> <span data-ttu-id="2648f-122">Los valores de propiedad satisfacen la relación especificada.</span><span class="sxs-lookup"><span data-stu-id="2648f-122">The property values satisfy the specified relation.</span></span> 
    
<span data-ttu-id="2648f-123">FALSE</span><span class="sxs-lookup"><span data-stu-id="2648f-123">FALSE</span></span> 
  
> <span data-ttu-id="2648f-124">Los valores de propiedad no satisfacen la relación especificada.</span><span class="sxs-lookup"><span data-stu-id="2648f-124">The property values do not satisfy the specified relation.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2648f-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2648f-125">Remarks</span></span>

<span data-ttu-id="2648f-126">El método de comparación depende de los tipos de propiedad especificados en las definiciones de la propiedad [SPropValue.](spropvalue.md)</span><span class="sxs-lookup"><span data-stu-id="2648f-126">The comparison method depends on the property types specified in the [SPropValue](spropvalue.md) property definitions.</span></span> <span data-ttu-id="2648f-127">Las **funciones FPropCompareProp** y [FPropContainsProp](fpropcontainsprop.md) se pueden usar para preparar restricciones para generar una tabla.</span><span class="sxs-lookup"><span data-stu-id="2648f-127">The **FPropCompareProp** and [FPropContainsProp](fpropcontainsprop.md) functions can be used to prepare restrictions for generating a table.</span></span> 
  
<span data-ttu-id="2648f-128">El orden de comparación es  _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _.</span><span class="sxs-lookup"><span data-stu-id="2648f-128">The order of comparison is  _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _.</span></span> <span data-ttu-id="2648f-129">Si los tipos de propiedad de los valores de propiedad que se van a comparar no coinciden, la función **FPropCompareProp** devuelve FALSE.</span><span class="sxs-lookup"><span data-stu-id="2648f-129">If the property types of the property values to be compared do not match, the **FPropCompareProp** function returns FALSE.</span></span> 
  

