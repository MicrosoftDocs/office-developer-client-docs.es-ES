---
title: MAGNITUDE (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251461
localization_priority: Normal
ms.assetid: 9f443687-9861-5f51-94c4-f056805f736b
description: Devuelve la magnitud del vector cuya elevación es A y cuya ejecución es B, multiplicada por sus respectivas constantes constante de a y constante.
ms.openlocfilehash: f4c428b8b381af58958dab66a71ddd0bcaf715c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822566"
---
# <a name="magnitude-function"></a><span data-ttu-id="76531-103">MAGNITUDE (función)</span><span class="sxs-lookup"><span data-stu-id="76531-103">MAGNITUDE Function</span></span>

<span data-ttu-id="76531-104">Devuelve la magnitud del vector cuya elevación es _A_ y cuya ejecución es _B_, multiplicada por sus respectivas constantes _constante_ de a y _constante_.</span><span class="sxs-lookup"><span data-stu-id="76531-104">Returns the magnitude of the vector whose rise is  _A_ and whose run is  _B_, multiplied by the respective constants  _constantA_ and  _constantB_.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="76531-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="76531-105">Syntax</span></span>

<span data-ttu-id="76531-106">MAGNITUD (** *constante* **, ** *A* **, ** *constante* **, ** *B* **)</span><span class="sxs-lookup"><span data-stu-id="76531-106">MAGNITUDE(** *constantA* **, ** *A* **, ** *constantB* **, ** *B* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="76531-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="76531-107">Parameters</span></span>

|<span data-ttu-id="76531-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="76531-108">**Name**</span></span>|<span data-ttu-id="76531-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="76531-109">**Required/Optional**</span></span>|<span data-ttu-id="76531-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="76531-110">**Data Type**</span></span>|<span data-ttu-id="76531-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="76531-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="76531-112">_Constante_</span><span class="sxs-lookup"><span data-stu-id="76531-112">_constantA_</span></span> <br/> |<span data-ttu-id="76531-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="76531-113">Required</span></span>  <br/> |<span data-ttu-id="76531-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="76531-114">**Number**</span></span> <br/> |<span data-ttu-id="76531-115">La constante por la que multiplicar el aumento.</span><span class="sxs-lookup"><span data-stu-id="76531-115">The constant by which to multiply the rise.</span></span>  <br/> |
| <span data-ttu-id="76531-116">_A_</span><span class="sxs-lookup"><span data-stu-id="76531-116">_A_</span></span> <br/> |<span data-ttu-id="76531-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="76531-117">Required</span></span>  <br/> |<span data-ttu-id="76531-118">**Número**</span><span class="sxs-lookup"><span data-stu-id="76531-118">**Number**</span></span> <br/> |<span data-ttu-id="76531-119">El aumento.</span><span class="sxs-lookup"><span data-stu-id="76531-119">The rise.</span></span>  <br/> |
| <span data-ttu-id="76531-120">_constante de b_</span><span class="sxs-lookup"><span data-stu-id="76531-120">_constantB_</span></span> <br/> |<span data-ttu-id="76531-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="76531-121">Required</span></span>  <br/> |<span data-ttu-id="76531-122">**Número**</span><span class="sxs-lookup"><span data-stu-id="76531-122">**Number**</span></span> <br/> |<span data-ttu-id="76531-123">La constante por la que multiplicar la ejecución.</span><span class="sxs-lookup"><span data-stu-id="76531-123">The constant by which to multiply the run.</span></span>  <br/> |
| <span data-ttu-id="76531-124">_B_</span><span class="sxs-lookup"><span data-stu-id="76531-124">_B_</span></span> <br/> |<span data-ttu-id="76531-125">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="76531-125">Required</span></span>  <br/> |<span data-ttu-id="76531-126">**Número**</span><span class="sxs-lookup"><span data-stu-id="76531-126">**Number**</span></span> <br/> |<span data-ttu-id="76531-127">La ejecución.</span><span class="sxs-lookup"><span data-stu-id="76531-127">The run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76531-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="76531-128">Remarks</span></span>

<span data-ttu-id="76531-129">La MAGNITUD se calcula de acuerdo con la siguiente fórmula:</span><span class="sxs-lookup"><span data-stu-id="76531-129">MAGNITUDE is calculated according to the following formula:</span></span>
  
<span data-ttu-id="76531-130">SQRT ((constante \* A) ^ 2 + (constante de b \* B) ^ 2)</span><span class="sxs-lookup"><span data-stu-id="76531-130">SQRT((constantA \* A)^2 + (constantB \* B)^2)</span></span>
  
## <a name="example"></a><span data-ttu-id="76531-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="76531-131">Example</span></span>

<span data-ttu-id="76531-132">MAGNITUDE(1; 3; 1; 4)</span><span class="sxs-lookup"><span data-stu-id="76531-132">MAGNITUDE(1, 3, 1, 4)</span></span> 
  
<span data-ttu-id="76531-133">Devuelve 5.</span><span class="sxs-lookup"><span data-stu-id="76531-133">Returns 5.</span></span> 
  

