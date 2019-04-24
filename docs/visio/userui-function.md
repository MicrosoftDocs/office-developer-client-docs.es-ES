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
description: Evalúa una de las dos expresiones según el valor de estado.
ms.openlocfilehash: 544bb2b19dc610591afc78c407301098fac9c7c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331328"
---
# <a name="userui-function"></a><span data-ttu-id="71ed6-103">Función USERUI</span><span class="sxs-lookup"><span data-stu-id="71ed6-103">USERUI Function</span></span>

<span data-ttu-id="71ed6-104">Evalúa una de las dos expresiones según el valor de _Estado_.</span><span class="sxs-lookup"><span data-stu-id="71ed6-104">Evaluates one of the two expressions depending on the value of  _state_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="71ed6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71ed6-105">Syntax</span></span>

<span data-ttu-id="71ed6-106">USERUI (\* \* *Estado* \* \*, \* \* *DefaultExpression* \* \*, \* \* *userexpression* \* \*)</span><span class="sxs-lookup"><span data-stu-id="71ed6-106">USERUI(\*\* *state* \*\*, \*\* *defaultexpression* \*\*, \*\* *userexpression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="71ed6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="71ed6-107">Parameters</span></span>

|<span data-ttu-id="71ed6-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="71ed6-108">**Name**</span></span>|<span data-ttu-id="71ed6-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="71ed6-109">**Required/Optional**</span></span>|<span data-ttu-id="71ed6-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="71ed6-110">**Data Type**</span></span>|<span data-ttu-id="71ed6-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="71ed6-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="71ed6-112">_state_</span><span class="sxs-lookup"><span data-stu-id="71ed6-112">_state_</span></span> <br/> |<span data-ttu-id="71ed6-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="71ed6-113">Required</span></span>  <br/> |<span data-ttu-id="71ed6-114">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="71ed6-114">**Boolean**</span></span> <br/> |<span data-ttu-id="71ed6-115">Determina la expresión que se va a evaluar.</span><span class="sxs-lookup"><span data-stu-id="71ed6-115">Determines which expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="71ed6-116">_DefaultExpression_</span><span class="sxs-lookup"><span data-stu-id="71ed6-116">_defaultexpression_</span></span> <br/> |<span data-ttu-id="71ed6-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="71ed6-117">Required</span></span>  <br/> |<span data-ttu-id="71ed6-118">**String**</span><span class="sxs-lookup"><span data-stu-id="71ed6-118">**String**</span></span> <br/> |<span data-ttu-id="71ed6-119">La expresión predeterminada.</span><span class="sxs-lookup"><span data-stu-id="71ed6-119">The default expression.</span></span>  <br/> |
| <span data-ttu-id="71ed6-120">_userexpression_</span><span class="sxs-lookup"><span data-stu-id="71ed6-120">_userexpression_</span></span> <br/> |<span data-ttu-id="71ed6-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="71ed6-121">Required</span></span>  <br/> |<span data-ttu-id="71ed6-122">**String**</span><span class="sxs-lookup"><span data-stu-id="71ed6-122">**String**</span></span> <br/> |<span data-ttu-id="71ed6-123">Una expresión proporcionada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="71ed6-123">An expression supplied by the user.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="71ed6-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="71ed6-124">Remarks</span></span>

<span data-ttu-id="71ed6-125">Si el _Estado_ es 0, la función USERUI evalúa _DefaultExpression_.</span><span class="sxs-lookup"><span data-stu-id="71ed6-125">If  _state_ is 0, the USERUI function evaluates the  _defaultexpression_.</span></span> <span data-ttu-id="71ed6-126">Si el _Estado_ es 1, evalúa _userexpression_.</span><span class="sxs-lookup"><span data-stu-id="71ed6-126">If  _state_ is 1, it evaluates the  _userexpression_.</span></span>
  
## <a name="example"></a><span data-ttu-id="71ed6-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="71ed6-127">Example</span></span>

<span data-ttu-id="71ed6-128">USERUI (1, if (width\>6pda, 6Pda, width), width\*0,75)</span><span class="sxs-lookup"><span data-stu-id="71ed6-128">USERUI(1, if(Width\>6in, 6in, Width), Width\*0.75)</span></span> 
  
<span data-ttu-id="71ed6-129">Evalúa el ancho\*de la expresión. 075 y devuelve el resultado.</span><span class="sxs-lookup"><span data-stu-id="71ed6-129">Evaluates the expression Width\*.075 and returns the result.</span></span> 
  

