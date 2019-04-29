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
description: Devuelve la magnitud del vector cuyo aumento es A y cuya ejecución es B, multiplicado por las respectivas constantes constante y constante.
ms.openlocfilehash: 6393c7827e2553ca4948c8b9c51075ca8e4783bd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420461"
---
# <a name="magnitude-function"></a><span data-ttu-id="51019-103">Función MAGNITUDE</span><span class="sxs-lookup"><span data-stu-id="51019-103">MAGNITUDE Function</span></span>

<span data-ttu-id="51019-104">Devuelve la magnitud del vector cuyo aumento es _a_ y cuya ejecución es _B_, multiplicado por las respectivas constantes _constante_ y _constante_.</span><span class="sxs-lookup"><span data-stu-id="51019-104">Returns the magnitude of the vector whose rise is  _A_ and whose run is  _B_, multiplied by the respective constants  _constantA_ and  _constantB_.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="51019-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="51019-105">Syntax</span></span>

<span data-ttu-id="51019-106">MAGNITUDe (\* \* *constante* \* \*, \* \* *A* \* \*, \* \* *constante* \* \*, \* \* *B* \* \*)</span><span class="sxs-lookup"><span data-stu-id="51019-106">MAGNITUDE(\*\* *constantA* \*\*, \*\* *A* \*\*, \*\* *constantB* \*\*, \*\* *B* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="51019-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="51019-107">Parameters</span></span>

|<span data-ttu-id="51019-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="51019-108">**Name**</span></span>|<span data-ttu-id="51019-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="51019-109">**Required/Optional**</span></span>|<span data-ttu-id="51019-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="51019-110">**Data Type**</span></span>|<span data-ttu-id="51019-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="51019-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="51019-112">_Constante_</span><span class="sxs-lookup"><span data-stu-id="51019-112">_constantA_</span></span> <br/> |<span data-ttu-id="51019-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="51019-113">Required</span></span>  <br/> |<span data-ttu-id="51019-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="51019-114">**Number**</span></span> <br/> |<span data-ttu-id="51019-115">La constante por la que multiplicar el aumento.</span><span class="sxs-lookup"><span data-stu-id="51019-115">The constant by which to multiply the rise.</span></span>  <br/> |
| <span data-ttu-id="51019-116">_A_</span><span class="sxs-lookup"><span data-stu-id="51019-116">_A_</span></span> <br/> |<span data-ttu-id="51019-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="51019-117">Required</span></span>  <br/> |<span data-ttu-id="51019-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="51019-118">**Number**</span></span> <br/> |<span data-ttu-id="51019-119">El aumento.</span><span class="sxs-lookup"><span data-stu-id="51019-119">The rise.</span></span>  <br/> |
| <span data-ttu-id="51019-120">_Constante_</span><span class="sxs-lookup"><span data-stu-id="51019-120">_constantB_</span></span> <br/> |<span data-ttu-id="51019-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="51019-121">Required</span></span>  <br/> |<span data-ttu-id="51019-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="51019-122">**Number**</span></span> <br/> |<span data-ttu-id="51019-123">La constante por la que multiplicar la ejecución.</span><span class="sxs-lookup"><span data-stu-id="51019-123">The constant by which to multiply the run.</span></span>  <br/> |
| <span data-ttu-id="51019-124">_B_</span><span class="sxs-lookup"><span data-stu-id="51019-124">_B_</span></span> <br/> |<span data-ttu-id="51019-125">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="51019-125">Required</span></span>  <br/> |<span data-ttu-id="51019-126">**Number**</span><span class="sxs-lookup"><span data-stu-id="51019-126">**Number**</span></span> <br/> |<span data-ttu-id="51019-127">La ejecución.</span><span class="sxs-lookup"><span data-stu-id="51019-127">The run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51019-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="51019-128">Remarks</span></span>

<span data-ttu-id="51019-129">La MAGNITUD se calcula de acuerdo con la siguiente fórmula:</span><span class="sxs-lookup"><span data-stu-id="51019-129">MAGNITUDE is calculated according to the following formula:</span></span>
  
<span data-ttu-id="51019-130">SQRT ((constante \* A) ^ 2 + (constante \* B) ^ 2)</span><span class="sxs-lookup"><span data-stu-id="51019-130">SQRT((constantA \* A)^2 + (constantB \* B)^2)</span></span>
  
## <a name="example"></a><span data-ttu-id="51019-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="51019-131">Example</span></span>

<span data-ttu-id="51019-132">MAGNITUDE(1; 3; 1; 4)</span><span class="sxs-lookup"><span data-stu-id="51019-132">MAGNITUDE(1, 3, 1, 4)</span></span> 
  
<span data-ttu-id="51019-133">Devuelve 5.</span><span class="sxs-lookup"><span data-stu-id="51019-133">Returns 5.</span></span> 
  

