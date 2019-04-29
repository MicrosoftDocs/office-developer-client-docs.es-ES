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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420349"
---
# <a name="userui-function"></a><span data-ttu-id="05b2c-103">Función USERUI</span><span class="sxs-lookup"><span data-stu-id="05b2c-103">USERUI Function</span></span>

<span data-ttu-id="05b2c-104">Evalúa una de las dos expresiones según el valor de _Estado_.</span><span class="sxs-lookup"><span data-stu-id="05b2c-104">Evaluates one of the two expressions depending on the value of  _state_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="05b2c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="05b2c-105">Syntax</span></span>

<span data-ttu-id="05b2c-106">USERUI (\* \* *Estado* \* \*, \* \* *DefaultExpression* \* \*, \* \* *userexpression* \* \*)</span><span class="sxs-lookup"><span data-stu-id="05b2c-106">USERUI(\*\* *state* \*\*, \*\* *defaultexpression* \*\*, \*\* *userexpression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="05b2c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="05b2c-107">Parameters</span></span>

|<span data-ttu-id="05b2c-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="05b2c-108">**Name**</span></span>|<span data-ttu-id="05b2c-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="05b2c-109">**Required/Optional**</span></span>|<span data-ttu-id="05b2c-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="05b2c-110">**Data Type**</span></span>|<span data-ttu-id="05b2c-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="05b2c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="05b2c-112">_state_</span><span class="sxs-lookup"><span data-stu-id="05b2c-112">_state_</span></span> <br/> |<span data-ttu-id="05b2c-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="05b2c-113">Required</span></span>  <br/> |<span data-ttu-id="05b2c-114">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="05b2c-114">**Boolean**</span></span> <br/> |<span data-ttu-id="05b2c-115">Determina la expresión que se va a evaluar.</span><span class="sxs-lookup"><span data-stu-id="05b2c-115">Determines which expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="05b2c-116">_DefaultExpression_</span><span class="sxs-lookup"><span data-stu-id="05b2c-116">_defaultexpression_</span></span> <br/> |<span data-ttu-id="05b2c-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="05b2c-117">Required</span></span>  <br/> |<span data-ttu-id="05b2c-118">**String**</span><span class="sxs-lookup"><span data-stu-id="05b2c-118">**String**</span></span> <br/> |<span data-ttu-id="05b2c-119">La expresión predeterminada.</span><span class="sxs-lookup"><span data-stu-id="05b2c-119">The default expression.</span></span>  <br/> |
| <span data-ttu-id="05b2c-120">_userexpression_</span><span class="sxs-lookup"><span data-stu-id="05b2c-120">_userexpression_</span></span> <br/> |<span data-ttu-id="05b2c-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="05b2c-121">Required</span></span>  <br/> |<span data-ttu-id="05b2c-122">**String**</span><span class="sxs-lookup"><span data-stu-id="05b2c-122">**String**</span></span> <br/> |<span data-ttu-id="05b2c-123">Una expresión proporcionada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="05b2c-123">An expression supplied by the user.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05b2c-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="05b2c-124">Remarks</span></span>

<span data-ttu-id="05b2c-125">Si el _Estado_ es 0, la función USERUI evalúa _DefaultExpression_.</span><span class="sxs-lookup"><span data-stu-id="05b2c-125">If  _state_ is 0, the USERUI function evaluates the  _defaultexpression_.</span></span> <span data-ttu-id="05b2c-126">Si el _Estado_ es 1, evalúa _userexpression_.</span><span class="sxs-lookup"><span data-stu-id="05b2c-126">If  _state_ is 1, it evaluates the  _userexpression_.</span></span>
  
## <a name="example"></a><span data-ttu-id="05b2c-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="05b2c-127">Example</span></span>

<span data-ttu-id="05b2c-128">USERUI (1, if (width\>6pda, 6Pda, width), width\*0,75)</span><span class="sxs-lookup"><span data-stu-id="05b2c-128">USERUI(1, if(Width\>6in, 6in, Width), Width\*0.75)</span></span> 
  
<span data-ttu-id="05b2c-129">Evalúa el ancho\*de la expresión. 075 y devuelve el resultado.</span><span class="sxs-lookup"><span data-stu-id="05b2c-129">Evaluates the expression Width\*.075 and returns the result.</span></span> 
  

