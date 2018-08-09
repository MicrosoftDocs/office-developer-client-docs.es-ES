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
description: Devuelve TRUE (1) si cualquiera de las expresiones lógicas que se pasan como parámetros son TRUE.
ms.openlocfilehash: 14646f553e76c8c395fdbde8762daf75114f9480
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822702"
---
# <a name="or-function"></a><span data-ttu-id="34a2d-103">Función OR</span><span class="sxs-lookup"><span data-stu-id="34a2d-103">OR Function</span></span>

<span data-ttu-id="34a2d-104">Devuelve TRUE (1) si cualquiera de las expresiones lógicas que se pasan como parámetros son TRUE.</span><span class="sxs-lookup"><span data-stu-id="34a2d-104">Returns TRUE (1) if any of the logical expressions passed as parameters are TRUE.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="34a2d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="34a2d-105">Syntax</span></span>

<span data-ttu-id="34a2d-106">O (** *logicalexpression1* **, ** *logicalexpression2* **,..., ** *logicalexpressionN* **)</span><span class="sxs-lookup"><span data-stu-id="34a2d-106">OR(** *logicalexpression1* **, ** *logicalexpression2* **,..., ** *logicalexpressionN* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="34a2d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="34a2d-107">Parameters</span></span>

|<span data-ttu-id="34a2d-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="34a2d-108">**Name**</span></span>|<span data-ttu-id="34a2d-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="34a2d-109">**Required/Optional**</span></span>|<span data-ttu-id="34a2d-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="34a2d-110">**Data Type**</span></span>|<span data-ttu-id="34a2d-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="34a2d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="34a2d-112">_logicalexpression1_</span><span class="sxs-lookup"><span data-stu-id="34a2d-112">_logicalexpression1_</span></span> <br/> |<span data-ttu-id="34a2d-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="34a2d-113">Required</span></span>  <br/> |<span data-ttu-id="34a2d-114">**String**</span><span class="sxs-lookup"><span data-stu-id="34a2d-114">**String**</span></span> <br/> |<span data-ttu-id="34a2d-115">La primera expresión cuya verdad desea evaluar.</span><span class="sxs-lookup"><span data-stu-id="34a2d-115">The first expression whose truth you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="34a2d-116">_logicalexpression2_</span><span class="sxs-lookup"><span data-stu-id="34a2d-116">_logicalexpression2_</span></span> <br/> |<span data-ttu-id="34a2d-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="34a2d-117">Required</span></span>  <br/> |<span data-ttu-id="34a2d-118">**String**</span><span class="sxs-lookup"><span data-stu-id="34a2d-118">**String**</span></span> <br/> |<span data-ttu-id="34a2d-119">La segunda expresión cuya verdad desea evaluar.</span><span class="sxs-lookup"><span data-stu-id="34a2d-119">The second expression whose truth you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="34a2d-120">_logicalexpressionN_</span><span class="sxs-lookup"><span data-stu-id="34a2d-120">_logicalexpressionN_</span></span> <br/> |<span data-ttu-id="34a2d-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="34a2d-121">Required</span></span>  <br/> |<span data-ttu-id="34a2d-122">**String**</span><span class="sxs-lookup"><span data-stu-id="34a2d-122">**String**</span></span> <br/> |<span data-ttu-id="34a2d-123">La expresión n cuya verdad desea evaluar.</span><span class="sxs-lookup"><span data-stu-id="34a2d-123">The Nth expression whose truth you want to evaluate.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="34a2d-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="34a2d-124">Return value</span></span>

<span data-ttu-id="34a2d-125">Booleano</span><span class="sxs-lookup"><span data-stu-id="34a2d-125">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="34a2d-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="34a2d-126">Remarks</span></span>

<span data-ttu-id="34a2d-p101">Cualquier expresión que dé como resultado un valor distinto de cero se considera verdadera. Si todas las expresiones lógicas son falsas o iguales a 0, esta función devuelve el valor FALSE.</span><span class="sxs-lookup"><span data-stu-id="34a2d-p101">Any expression that evaluates to a non-zero value is considered TRUE. If all of the logical expressions are FALSE or equal 0, this function returns FALSE.</span></span> 
  
## <a name="example"></a><span data-ttu-id="34a2d-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="34a2d-129">Example</span></span>

<span data-ttu-id="34a2d-130">O (alto \> 1, PinX \> 1)</span><span class="sxs-lookup"><span data-stu-id="34a2d-130">OR(Height \> 1,PinX \> 1)</span></span> 
  
<span data-ttu-id="34a2d-p102">Devuelve TRUE (1) si cualquiera de las expresiones es verdadera. Devuelve FALSE (0) sólo cuando ambas expresiones son falsas.</span><span class="sxs-lookup"><span data-stu-id="34a2d-p102">Returns TRUE (1) if either expression is TRUE. Returns FALSE (0) only if both expressions are FALSE.</span></span> 
  

