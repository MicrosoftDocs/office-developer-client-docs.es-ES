---
title: USERUI (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251511
localization_priority: Normal
ms.assetid: c01dd938-677c-b2ba-8f56-4638e7e988fd
description: Evalúa una de las dos expresiones en función del valor de estado.
ms.openlocfilehash: 544bb2b19dc610591afc78c407301098fac9c7c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420349"
---
# <a name="userui-function"></a><span data-ttu-id="ca9d0-103">Función USERUI</span><span class="sxs-lookup"><span data-stu-id="ca9d0-103">USERUI Function</span></span>

<span data-ttu-id="ca9d0-104">Evalúa una de las dos expresiones según el valor de  _estado_.</span><span class="sxs-lookup"><span data-stu-id="ca9d0-104">Evaluates one of the two expressions depending on the value of  _state_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="ca9d0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ca9d0-105">Syntax</span></span>

<span data-ttu-id="ca9d0-106">USERUI(\*\* *state* \*\*, \*\* *defaultexpression* \*\*, \*\* *userexpression* \*\* )</span><span class="sxs-lookup"><span data-stu-id="ca9d0-106">USERUI(\*\* *state* \*\*, \*\* *defaultexpression* \*\*, \*\* *userexpression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ca9d0-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ca9d0-107">Parameters</span></span>

|<span data-ttu-id="ca9d0-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="ca9d0-108">**Name**</span></span>|<span data-ttu-id="ca9d0-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="ca9d0-109">**Required/Optional**</span></span>|<span data-ttu-id="ca9d0-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="ca9d0-110">**Data Type**</span></span>|<span data-ttu-id="ca9d0-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ca9d0-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ca9d0-112">_state_</span><span class="sxs-lookup"><span data-stu-id="ca9d0-112">_state_</span></span> <br/> |<span data-ttu-id="ca9d0-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="ca9d0-113">Required</span></span>  <br/> |<span data-ttu-id="ca9d0-114">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="ca9d0-114">**Boolean**</span></span> <br/> |<span data-ttu-id="ca9d0-115">Determina qué expresión evaluar.</span><span class="sxs-lookup"><span data-stu-id="ca9d0-115">Determines which expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="ca9d0-116">_defaultexpression_</span><span class="sxs-lookup"><span data-stu-id="ca9d0-116">_defaultexpression_</span></span> <br/> |<span data-ttu-id="ca9d0-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="ca9d0-117">Required</span></span>  <br/> |<span data-ttu-id="ca9d0-118">**String**</span><span class="sxs-lookup"><span data-stu-id="ca9d0-118">**String**</span></span> <br/> |<span data-ttu-id="ca9d0-119">Expresión predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ca9d0-119">The default expression.</span></span>  <br/> |
| <span data-ttu-id="ca9d0-120">_userexpression_</span><span class="sxs-lookup"><span data-stu-id="ca9d0-120">_userexpression_</span></span> <br/> |<span data-ttu-id="ca9d0-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="ca9d0-121">Required</span></span>  <br/> |<span data-ttu-id="ca9d0-122">**String**</span><span class="sxs-lookup"><span data-stu-id="ca9d0-122">**String**</span></span> <br/> |<span data-ttu-id="ca9d0-123">Expresión proporcionada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="ca9d0-123">An expression supplied by the user.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca9d0-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ca9d0-124">Remarks</span></span>

<span data-ttu-id="ca9d0-125">Si  _el_ estado es 0, la función USERUI evalúa la  _expresión predeterminada_.</span><span class="sxs-lookup"><span data-stu-id="ca9d0-125">If  _state_ is 0, the USERUI function evaluates the  _defaultexpression_.</span></span> <span data-ttu-id="ca9d0-126">Si _el_ estado es 1, evalúa la _expresión user ._</span><span class="sxs-lookup"><span data-stu-id="ca9d0-126">If  _state_ is 1, it evaluates the  _userexpression_.</span></span>
  
## <a name="example"></a><span data-ttu-id="ca9d0-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ca9d0-127">Example</span></span>

<span data-ttu-id="ca9d0-128">USERUI(1, if(Width \> 6in, 6in, Width), Width \* 0.75)</span><span class="sxs-lookup"><span data-stu-id="ca9d0-128">USERUI(1, if(Width\>6in, 6in, Width), Width\*0.75)</span></span> 
  
<span data-ttu-id="ca9d0-129">Evalúa la expresión Width \* .075 y devuelve el resultado.</span><span class="sxs-lookup"><span data-stu-id="ca9d0-129">Evaluates the expression Width\*.075 and returns the result.</span></span> 
  

