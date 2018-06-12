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
description: Devuelve TRUE (1) si todas las expresiones lógicas suministradas son TRUE. Si alguna de las expresiones lógicas es falso o 0, la función y devuelve FALSE (0).
ms.openlocfilehash: 27b2ef97ef1d0afde37596b18674c6de26355a1b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821540"
---
# <a name="and-function"></a><span data-ttu-id="8a299-104">AND (función)</span><span class="sxs-lookup"><span data-stu-id="8a299-104">AND Function</span></span>

<span data-ttu-id="8a299-105">Devuelve TRUE (1) si todas las expresiones lógicas suministradas son TRUE.</span><span class="sxs-lookup"><span data-stu-id="8a299-105">Returns TRUE (1) if all of the logical expressions supplied are TRUE.</span></span> <span data-ttu-id="8a299-106">Si alguna de las expresiones lógicas es falso o 0, la función y devuelve FALSE (0).</span><span class="sxs-lookup"><span data-stu-id="8a299-106">If any of the logical expressions are FALSE or 0, the AND function returns FALSE (0).</span></span>
  
## <a name="syntax"></a><span data-ttu-id="8a299-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a299-107">Syntax</span></span>

<span data-ttu-id="8a299-108">Y (** *expression1 lógica* **, ** *Expresión2 lógica* **,..., ** *expresiónn lógico* **)</span><span class="sxs-lookup"><span data-stu-id="8a299-108">AND(** *logical expression1* **, ** *logical expression2* **,..., ** *logical expressionN* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8a299-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a299-109">Parameters</span></span>

|<span data-ttu-id="8a299-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="8a299-110">**Name**</span></span>|<span data-ttu-id="8a299-111">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="8a299-111">**Required/Optional**</span></span>|<span data-ttu-id="8a299-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="8a299-112">**Data Type**</span></span>|<span data-ttu-id="8a299-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8a299-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8a299-114">_expresión lógica_</span><span class="sxs-lookup"><span data-stu-id="8a299-114">_logical expression_</span></span> <br/> |<span data-ttu-id="8a299-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="8a299-115">Required</span></span>  <br/> |<span data-ttu-id="8a299-116">**String**</span><span class="sxs-lookup"><span data-stu-id="8a299-116">**String**</span></span> <br/> | <span data-ttu-id="8a299-p103">Combinación de constantes, operadores, funciones y referencias a celdas de ShapeSheet que da como resultado un valor. Cualquier expresión que al evaluarse se convierta en un valor distinto de cero se considera verdadera.</span><span class="sxs-lookup"><span data-stu-id="8a299-p103">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value. Any expression that evaluates to a non-zero value is considered to be TRUE.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="8a299-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8a299-119">Example</span></span>

<span data-ttu-id="8a299-120">Y (alto \> 1, PinX \> 1)</span><span class="sxs-lookup"><span data-stu-id="8a299-120">AND(Height \> 1, PinX \> 1)</span></span>
  
<span data-ttu-id="8a299-p104">Devuelve TRUE si ambas expresiones son verdaderas. Devuelve FALSE si cualquiera de las expresiones es falsa.</span><span class="sxs-lookup"><span data-stu-id="8a299-p104">Returns TRUE if both expressions are TRUE. Returns FALSE if either expression is FALSE.</span></span>
  

