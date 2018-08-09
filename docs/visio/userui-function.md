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
description: Evalúa una de las dos expresiones dependiendo del valor de estado.
ms.openlocfilehash: 2cfdf23986a06dcc109106bd50a1a38e5af91313
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823500"
---
# <a name="userui-function"></a><span data-ttu-id="cbd6e-103">Función USERUI</span><span class="sxs-lookup"><span data-stu-id="cbd6e-103">USERUI Function</span></span>

<span data-ttu-id="cbd6e-104">Evalúa una de las dos expresiones dependiendo del valor de _estado_.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-104">Evaluates one of the two expressions depending on the value of  _state_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="cbd6e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cbd6e-105">Syntax</span></span>

<span data-ttu-id="cbd6e-106">USERUI (** *estado* **, ** *expresiónpredeterminada* **, ** *expresióndeusuario* **)</span><span class="sxs-lookup"><span data-stu-id="cbd6e-106">USERUI(** *state* **, ** *defaultexpression* **, ** *userexpression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="cbd6e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cbd6e-107">Parameters</span></span>

|<span data-ttu-id="cbd6e-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="cbd6e-108">**Name**</span></span>|<span data-ttu-id="cbd6e-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="cbd6e-109">**Required/Optional**</span></span>|<span data-ttu-id="cbd6e-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="cbd6e-110">**Data Type**</span></span>|<span data-ttu-id="cbd6e-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cbd6e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="cbd6e-112">_state_</span><span class="sxs-lookup"><span data-stu-id="cbd6e-112">_state_</span></span> <br/> |<span data-ttu-id="cbd6e-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="cbd6e-113">Required</span></span>  <br/> |<span data-ttu-id="cbd6e-114">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="cbd6e-114">**Boolean**</span></span> <br/> |<span data-ttu-id="cbd6e-115">Determina qué expresión se evalúe.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-115">Determines which expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="cbd6e-116">_expresiónpredeterminada_</span><span class="sxs-lookup"><span data-stu-id="cbd6e-116">_defaultexpression_</span></span> <br/> |<span data-ttu-id="cbd6e-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="cbd6e-117">Required</span></span>  <br/> |<span data-ttu-id="cbd6e-118">**String**</span><span class="sxs-lookup"><span data-stu-id="cbd6e-118">**String**</span></span> <br/> |<span data-ttu-id="cbd6e-119">La expresión de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-119">The default expression.</span></span>  <br/> |
| <span data-ttu-id="cbd6e-120">_expresióndeusuario_</span><span class="sxs-lookup"><span data-stu-id="cbd6e-120">_userexpression_</span></span> <br/> |<span data-ttu-id="cbd6e-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="cbd6e-121">Required</span></span>  <br/> |<span data-ttu-id="cbd6e-122">**String**</span><span class="sxs-lookup"><span data-stu-id="cbd6e-122">**String**</span></span> <br/> |<span data-ttu-id="cbd6e-123">Una expresión proporcionada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-123">An expression supplied by the user.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cbd6e-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cbd6e-124">Remarks</span></span>

<span data-ttu-id="cbd6e-125">Si el _estado_ es 0, la función USERUI evalúa _expresiónpredeterminada_.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-125">If  _state_ is 0, the USERUI function evaluates the  _defaultexpression_.</span></span> <span data-ttu-id="cbd6e-126">Si _es 1,_ evalúa _expresióndeusuario_.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-126">If  _state_ is 1, it evaluates the  _userexpression_.</span></span>
  
## <a name="example"></a><span data-ttu-id="cbd6e-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cbd6e-127">Example</span></span>

<span data-ttu-id="cbd6e-128">USERUI (1, si (ancho\>6pda, 6pda, Width), Width\*0,75)</span><span class="sxs-lookup"><span data-stu-id="cbd6e-128">USERUI(1, if(Width\>6in, 6in, Width), Width\*0.75)</span></span> 
  
<span data-ttu-id="cbd6e-129">Evalúa la expresión Width\*.075 y devuelve el resultado.</span><span class="sxs-lookup"><span data-stu-id="cbd6e-129">Evaluates the expression Width\*.075 and returns the result.</span></span> 
  

