---
title: AND (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251391
localization_priority: Normal
ms.assetid: 434d7ceb-1050-c667-fb3d-b6634440c18e
description: Devuelve TRUE (1) si todas las expresiones lógicas proporcionadas son TRUE. Si alguna de las expresiones lógicas es FALSE o 0, la función AND devuelve FALSE (0).
ms.openlocfilehash: 74e8301718e69a2ab61f6bf9992d0d6855bbc6f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422015"
---
# <a name="and-function"></a><span data-ttu-id="3f099-104">Función AND</span><span class="sxs-lookup"><span data-stu-id="3f099-104">AND Function</span></span>

<span data-ttu-id="3f099-105">Devuelve TRUE (1) si todas las expresiones lógicas proporcionadas son TRUE.</span><span class="sxs-lookup"><span data-stu-id="3f099-105">Returns TRUE (1) if all of the logical expressions supplied are TRUE.</span></span> <span data-ttu-id="3f099-106">Si alguna de las expresiones lógicas es FALSE o 0, la función AND devuelve FALSE (0).</span><span class="sxs-lookup"><span data-stu-id="3f099-106">If any of the logical expressions are FALSE or 0, the AND function returns FALSE (0).</span></span>
  
## <a name="syntax"></a><span data-ttu-id="3f099-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3f099-107">Syntax</span></span>

<span data-ttu-id="3f099-108">AND(\*\* *logical expression1* \*\*, \*\* *logical expression2* \*\*,..., \*\* *logical expressionN* \*\* )</span><span class="sxs-lookup"><span data-stu-id="3f099-108">AND(\*\* *logical expression1* \*\*, \*\* *logical expression2* \*\*,..., \*\* *logical expressionN* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3f099-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3f099-109">Parameters</span></span>

|<span data-ttu-id="3f099-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="3f099-110">**Name**</span></span>|<span data-ttu-id="3f099-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="3f099-111">**Required/Optional**</span></span>|<span data-ttu-id="3f099-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="3f099-112">**Data Type**</span></span>|<span data-ttu-id="3f099-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3f099-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3f099-114">_expresión lógica_</span><span class="sxs-lookup"><span data-stu-id="3f099-114">_logical expression_</span></span> <br/> |<span data-ttu-id="3f099-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="3f099-115">Required</span></span>  <br/> |<span data-ttu-id="3f099-116">**String**</span><span class="sxs-lookup"><span data-stu-id="3f099-116">**String**</span></span> <br/> | <span data-ttu-id="3f099-p103">Combinación de constantes, operadores, funciones y referencias a celdas de ShapeSheet que da como resultado un valor. Cualquier expresión que al evaluarse se convierta en un valor distinto de cero se considera verdadera.</span><span class="sxs-lookup"><span data-stu-id="3f099-p103">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value. Any expression that evaluates to a non-zero value is considered to be TRUE.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="3f099-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3f099-119">Example</span></span>

<span data-ttu-id="3f099-120">AND(Height \> 1, PinX \> 1)</span><span class="sxs-lookup"><span data-stu-id="3f099-120">AND(Height \> 1, PinX \> 1)</span></span>
  
<span data-ttu-id="3f099-121">Devuelve TRUE si ambas expresiones son verdaderas.</span><span class="sxs-lookup"><span data-stu-id="3f099-121">Returns TRUE if both expressions are TRUE.</span></span> <span data-ttu-id="3f099-122">Devuelve FALSE si cualquiera de las expresiones es falsa.</span><span class="sxs-lookup"><span data-stu-id="3f099-122">Returns FALSE if either expression is FALSE.</span></span>
  

