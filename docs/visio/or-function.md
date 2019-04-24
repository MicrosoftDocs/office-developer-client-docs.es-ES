---
title: OR (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251476
localization_priority: Normal
ms.assetid: 6c2154fa-4190-0699-61f7-f2bdf87173ec
description: Devuelve TRUE (1) si alguna de las expresiones lógicas pasadas como parámetros son TRUE.
ms.openlocfilehash: 175a1c72f5109caca786b823966f07836f4737f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337215"
---
# <a name="or-function"></a><span data-ttu-id="21ccc-103">Función OR</span><span class="sxs-lookup"><span data-stu-id="21ccc-103">OR Function</span></span>

<span data-ttu-id="21ccc-104">Devuelve TRUE (1) si alguna de las expresiones lógicas pasadas como parámetros son TRUE.</span><span class="sxs-lookup"><span data-stu-id="21ccc-104">Returns TRUE (1) if any of the logical expressions passed as parameters are TRUE.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="21ccc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="21ccc-105">Syntax</span></span>

<span data-ttu-id="21ccc-106">OR (\* \* *logicalexpression1* \* \*, \* \* *logicalexpression2* \* \*,..., \* \* *logicalexpressionN* \* \*)</span><span class="sxs-lookup"><span data-stu-id="21ccc-106">OR(\*\* *logicalexpression1* \*\*, \*\* *logicalexpression2* \*\*,..., \*\* *logicalexpressionN* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="21ccc-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="21ccc-107">Parameters</span></span>

|<span data-ttu-id="21ccc-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="21ccc-108">**Name**</span></span>|<span data-ttu-id="21ccc-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="21ccc-109">**Required/Optional**</span></span>|<span data-ttu-id="21ccc-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="21ccc-110">**Data Type**</span></span>|<span data-ttu-id="21ccc-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="21ccc-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="21ccc-112">_logicalexpression1_</span><span class="sxs-lookup"><span data-stu-id="21ccc-112">_logicalexpression1_</span></span> <br/> |<span data-ttu-id="21ccc-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="21ccc-113">Required</span></span>  <br/> |<span data-ttu-id="21ccc-114">**String**</span><span class="sxs-lookup"><span data-stu-id="21ccc-114">**String**</span></span> <br/> |<span data-ttu-id="21ccc-115">La primera expresión cuya verdad desea evaluar.</span><span class="sxs-lookup"><span data-stu-id="21ccc-115">The first expression whose truth you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="21ccc-116">_logicalexpression2_</span><span class="sxs-lookup"><span data-stu-id="21ccc-116">_logicalexpression2_</span></span> <br/> |<span data-ttu-id="21ccc-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="21ccc-117">Required</span></span>  <br/> |<span data-ttu-id="21ccc-118">**String**</span><span class="sxs-lookup"><span data-stu-id="21ccc-118">**String**</span></span> <br/> |<span data-ttu-id="21ccc-119">La segunda expresión cuya verdad desea evaluar.</span><span class="sxs-lookup"><span data-stu-id="21ccc-119">The second expression whose truth you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="21ccc-120">_logicalexpressionN_</span><span class="sxs-lookup"><span data-stu-id="21ccc-120">_logicalexpressionN_</span></span> <br/> |<span data-ttu-id="21ccc-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="21ccc-121">Required</span></span>  <br/> |<span data-ttu-id="21ccc-122">**String**</span><span class="sxs-lookup"><span data-stu-id="21ccc-122">**String**</span></span> <br/> |<span data-ttu-id="21ccc-123">La expresión n cuya verdad desea evaluar.</span><span class="sxs-lookup"><span data-stu-id="21ccc-123">The Nth expression whose truth you want to evaluate.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="21ccc-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="21ccc-124">Return value</span></span>

<span data-ttu-id="21ccc-125">Booleano</span><span class="sxs-lookup"><span data-stu-id="21ccc-125">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="21ccc-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="21ccc-126">Remarks</span></span>

<span data-ttu-id="21ccc-p101">Cualquier expresión que dé como resultado un valor distinto de cero se considera verdadera. Si todas las expresiones lógicas son falsas o iguales a 0, esta función devuelve el valor FALSE.</span><span class="sxs-lookup"><span data-stu-id="21ccc-p101">Any expression that evaluates to a non-zero value is considered TRUE. If all of the logical expressions are FALSE or equal 0, this function returns FALSE.</span></span> 
  
## <a name="example"></a><span data-ttu-id="21ccc-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="21ccc-129">Example</span></span>

<span data-ttu-id="21ccc-130">O (altura \> 1, PinX \> 1)</span><span class="sxs-lookup"><span data-stu-id="21ccc-130">OR(Height \> 1,PinX \> 1)</span></span> 
  
<span data-ttu-id="21ccc-131">Devuelve TRUE (1) si cualquiera de las expresiones es verdadera.</span><span class="sxs-lookup"><span data-stu-id="21ccc-131">Returns TRUE (1) if either expression is TRUE.</span></span> <span data-ttu-id="21ccc-132">Devuelve FALSE (0) sólo cuando ambas expresiones son falsas.</span><span class="sxs-lookup"><span data-stu-id="21ccc-132">Returns FALSE (0) only if both expressions are FALSE.</span></span> 
  

