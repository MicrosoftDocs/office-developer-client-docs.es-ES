---
title: SETATREFEXPR (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027317
localization_priority: Normal
ms.assetid: c1bd7819-b53b-bff1-69c1-6d78e8fb278b
description: Almacena un valor que se establece a través de una acción de la interfaz de usuario (UI) o la automatización.
ms.openlocfilehash: c664717afcc2b81e55495fd1957a86ef1b021d0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823142"
---
# <a name="setatrefexpr-function"></a><span data-ttu-id="219a0-103">SETATREFEXPR (función)</span><span class="sxs-lookup"><span data-stu-id="219a0-103">SETATREFEXPR Function</span></span>

<span data-ttu-id="219a0-104">Almacena un valor que se establece a través de una acción de la interfaz de usuario (UI) o la automatización.</span><span class="sxs-lookup"><span data-stu-id="219a0-104">Stores a value that is set through an action in the user interface (UI) or Automation.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="219a0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="219a0-105">Syntax</span></span>

<span data-ttu-id="219a0-106">SETATREFEXPR ([** *expr_opc* **])</span><span class="sxs-lookup"><span data-stu-id="219a0-106">SETATREFEXPR ([ ** *expr_opt* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="219a0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="219a0-107">Parameters</span></span>

|<span data-ttu-id="219a0-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="219a0-108">**Name**</span></span>|<span data-ttu-id="219a0-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="219a0-109">**Required/Optional**</span></span>|<span data-ttu-id="219a0-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="219a0-110">**Data Type**</span></span>|<span data-ttu-id="219a0-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="219a0-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="219a0-112">_expr_opc_</span><span class="sxs-lookup"><span data-stu-id="219a0-112">_expr_opt_</span></span> <br/> |<span data-ttu-id="219a0-113">Opcional</span><span class="sxs-lookup"><span data-stu-id="219a0-113">Optional</span></span>  <br/> |<span data-ttu-id="219a0-114">**Varía**</span><span class="sxs-lookup"><span data-stu-id="219a0-114">**Varies**</span></span> <br/> |<span data-ttu-id="219a0-115">Una expresión que se ha reemplazado por el valor o expresión que se va a asignar a la celda que se hace referencia en la función SETATREF.</span><span class="sxs-lookup"><span data-stu-id="219a0-115">An expression that is replaced by the value or expression being assigned to the referenced cell in the SETATREF function.</span></span> <span data-ttu-id="219a0-116">Si no se indica, su valor inicial es 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="219a0-116">If not indicated, its initial value is 0 (zero).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="219a0-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="219a0-117">Remarks</span></span>

<span data-ttu-id="219a0-118">El valor de una expresión SETATREFEXPR también se puede establecer desde una función SETATREF en otra celda que haga referencia a la celda que contiene la expresión SETATREFEXPR.</span><span class="sxs-lookup"><span data-stu-id="219a0-118">The value of a SETATREFEXPR expression can also be set from a SETATREF function in another cell that references the cell containing the SETATREFEXPR expression.</span></span> 
  
<span data-ttu-id="219a0-119">No está limitado al uso de la función SETATREFEXPR como un parámetro a la función SETATREF.</span><span class="sxs-lookup"><span data-stu-id="219a0-119">You are not limited to using the SETATREFEXPR function as a parameter to the SETATREF function.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="219a0-120">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="219a0-120">Example 1</span></span>

<span data-ttu-id="219a0-121">En el ejemplo siguiente, se usa la función SETATREFEXPR para garantizar que una forma tiene el ancho de su texto.</span><span class="sxs-lookup"><span data-stu-id="219a0-121">The following example uses the SETATREFEXPR function to ensure that a shape is as wide as its text.</span></span>
  
<span data-ttu-id="219a0-122">Width =MAX(TEXTWIDTH(TheText),SETATREFEXPR())</span><span class="sxs-lookup"><span data-stu-id="219a0-122">Width =MAX(TEXTWIDTH(TheText),SETATREFEXPR())</span></span>
  
## <a name="example-2"></a><span data-ttu-id="219a0-123">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="219a0-123">Example 2</span></span>

<span data-ttu-id="219a0-p102">En el ejemplo siguiente, se muestra cómo utilizar la función SETATREFEXPR para que las formas se ajusten a una cuadrícula personalizada. Las fórmulas SETATREFEXPR se colocan en las celdas PinX y PinY, lo cual produce que el eje de la forma se ajuste a la cuadrícula definida en User.GridX y User.GridY.</span><span class="sxs-lookup"><span data-stu-id="219a0-p102">The following example shows how you can use the SETATREFEXPR function to cause your shapes to snap to a custom grid. The SETATREFEXPR formulas are placed in the PinX and PinY cells, causing the shape's pin to snap to the grid defined in User.GridX and User.GridY.</span></span> 
  
<span data-ttu-id="219a0-126">User.GridX =2 pda</span><span class="sxs-lookup"><span data-stu-id="219a0-126">User.GridX =2 in</span></span>
  
<span data-ttu-id="219a0-127">User.GridY =2 pda</span><span class="sxs-lookup"><span data-stu-id="219a0-127">User.GridY =2 in</span></span>
  
<span data-ttu-id="219a0-128">PinX = INT (SETATREFEXPR () / User.GridX +.5)\*User.GridX</span><span class="sxs-lookup"><span data-stu-id="219a0-128">PinX =INT(SETATREFEXPR()/User.GridX + .5)\*User.GridX</span></span>
  
<span data-ttu-id="219a0-129">PinY = INT (SETATREFEXPR () / User.GridY +.5)\*User.GridY</span><span class="sxs-lookup"><span data-stu-id="219a0-129">PinY =INT(SETATREFEXPR()/User.GridY + .5)\*User.GridY</span></span>
  
## <a name="example-3"></a><span data-ttu-id="219a0-130">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="219a0-130">Example 3</span></span>

<span data-ttu-id="219a0-131">Para obtener un ejemplo de uso de la función SETATREFEXPR con la función SETATREF, vea la función [SETATREF](setatref-function.md) .</span><span class="sxs-lookup"><span data-stu-id="219a0-131">For an example using the SETATREFEXPR function with the SETATREF function, see the [SETATREF](setatref-function.md) function.</span></span> 
  

