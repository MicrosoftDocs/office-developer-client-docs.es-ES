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
description: Almacena un valor que se establece a través de una acción en la interfaz de usuario (UI) o automatización.
ms.openlocfilehash: 5ca7b59d0ced9c3da346c416826ac89e6b4001da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326008"
---
# <a name="setatrefexpr-function"></a><span data-ttu-id="f845c-103">Función SETATREFEXPR</span><span class="sxs-lookup"><span data-stu-id="f845c-103">SETATREFEXPR Function</span></span>

<span data-ttu-id="f845c-104">Almacena un valor que se establece a través de una acción en la interfaz de usuario (UI) o automatización.</span><span class="sxs-lookup"><span data-stu-id="f845c-104">Stores a value that is set through an action in the user interface (UI) or Automation.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="f845c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f845c-105">Syntax</span></span>

<span data-ttu-id="f845c-106">SETATREFEXPR ([\* \* *expr_opt* \* \*])</span><span class="sxs-lookup"><span data-stu-id="f845c-106">SETATREFEXPR ([ \*\* *expr_opt* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f845c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f845c-107">Parameters</span></span>

|<span data-ttu-id="f845c-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="f845c-108">**Name**</span></span>|<span data-ttu-id="f845c-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="f845c-109">**Required/Optional**</span></span>|<span data-ttu-id="f845c-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="f845c-110">**Data Type**</span></span>|<span data-ttu-id="f845c-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f845c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f845c-112">_expr_opt_</span><span class="sxs-lookup"><span data-stu-id="f845c-112">_expr_opt_</span></span> <br/> |<span data-ttu-id="f845c-113">Opcional</span><span class="sxs-lookup"><span data-stu-id="f845c-113">Optional</span></span>  <br/> |<span data-ttu-id="f845c-114">**Diferencias**</span><span class="sxs-lookup"><span data-stu-id="f845c-114">**Varies**</span></span> <br/> |<span data-ttu-id="f845c-115">Expresión que se reemplaza por el valor o la expresión que se asigna a la celda a la que se hace referencia en la función SETATREF.</span><span class="sxs-lookup"><span data-stu-id="f845c-115">An expression that is replaced by the value or expression being assigned to the referenced cell in the SETATREF function.</span></span> <span data-ttu-id="f845c-116">Si no se indica, su valor inicial es 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="f845c-116">If not indicated, its initial value is 0 (zero).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f845c-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f845c-117">Remarks</span></span>

<span data-ttu-id="f845c-118">El valor de una expresión SETATREFEXPR también se puede establecer desde una función SETATREF en otra celda que haga referencia a la celda que contiene la expresión SETATREFEXPR.</span><span class="sxs-lookup"><span data-stu-id="f845c-118">The value of a SETATREFEXPR expression can also be set from a SETATREF function in another cell that references the cell containing the SETATREFEXPR expression.</span></span> 
  
<span data-ttu-id="f845c-119">No está limitado a usar la función SETATREFEXPR como un parámetro para la función SETATREF.</span><span class="sxs-lookup"><span data-stu-id="f845c-119">You are not limited to using the SETATREFEXPR function as a parameter to the SETATREF function.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="f845c-120">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="f845c-120">Example 1</span></span>

<span data-ttu-id="f845c-121">En el ejemplo siguiente, se usa la función SETATREFEXPR para garantizar que una forma tiene el ancho de su texto.</span><span class="sxs-lookup"><span data-stu-id="f845c-121">The following example uses the SETATREFEXPR function to ensure that a shape is as wide as its text.</span></span>
  
<span data-ttu-id="f845c-122">Width =MAX(TEXTWIDTH(TheText),SETATREFEXPR())</span><span class="sxs-lookup"><span data-stu-id="f845c-122">Width =MAX(TEXTWIDTH(TheText),SETATREFEXPR())</span></span>
  
## <a name="example-2"></a><span data-ttu-id="f845c-123">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="f845c-123">Example 2</span></span>

<span data-ttu-id="f845c-p102">En el ejemplo siguiente, se muestra cómo utilizar la función SETATREFEXPR para que las formas se ajusten a una cuadrícula personalizada. Las fórmulas SETATREFEXPR se colocan en las celdas PinX y PinY, lo cual produce que el eje de la forma se ajuste a la cuadrícula definida en User.GridX y User.GridY.</span><span class="sxs-lookup"><span data-stu-id="f845c-p102">The following example shows how you can use the SETATREFEXPR function to cause your shapes to snap to a custom grid. The SETATREFEXPR formulas are placed in the PinX and PinY cells, causing the shape's pin to snap to the grid defined in User.GridX and User.GridY.</span></span> 
  
<span data-ttu-id="f845c-126">User.GridX =2 pda</span><span class="sxs-lookup"><span data-stu-id="f845c-126">User.GridX =2 in</span></span>
  
<span data-ttu-id="f845c-127">User.GridY =2 pda</span><span class="sxs-lookup"><span data-stu-id="f845c-127">User.GridY =2 in</span></span>
  
<span data-ttu-id="f845c-128">PinX = INT (SETATREFEXPR ()/User.GridX + 5)\*User. GridX</span><span class="sxs-lookup"><span data-stu-id="f845c-128">PinX =INT(SETATREFEXPR()/User.GridX + .5)\*User.GridX</span></span>
  
<span data-ttu-id="f845c-129">PinY = INT (SETATREFEXPR ()/User.GridY + 0,5)\*User. GridY</span><span class="sxs-lookup"><span data-stu-id="f845c-129">PinY =INT(SETATREFEXPR()/User.GridY + .5)\*User.GridY</span></span>
  
## <a name="example-3"></a><span data-ttu-id="f845c-130">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="f845c-130">Example 3</span></span>

<span data-ttu-id="f845c-131">Para conocer un ejemplo sobre el uso de la función SETATREFEXPR con la función SETATREF, vea el tema que trata la función [SETATREF](setatref-function.md).</span><span class="sxs-lookup"><span data-stu-id="f845c-131">For an example using the SETATREFEXPR function with the SETATREF function, see the [SETATREF](setatref-function.md) function.</span></span> 
  

