---
title: SETATREF (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60113
localization_priority: Normal
ms.assetid: 1ecfdb05-2533-470a-006b-e554026944d8
description: Redirige los valores actualizados resultantes de acciones en la interfaz de usuario (UI) o automatización a otra celda.
ms.openlocfilehash: c4f5fe94aba90ce0a69983d6637a5399b6e42707
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416807"
---
# <a name="setatref-function"></a><span data-ttu-id="c2caa-103">Función SETATREF</span><span class="sxs-lookup"><span data-stu-id="c2caa-103">SETATREF Function</span></span>

<span data-ttu-id="c2caa-104">Redirige los valores actualizados resultantes de acciones en la interfaz de usuario (UI) o automatización a otra celda.</span><span class="sxs-lookup"><span data-stu-id="c2caa-104">Redirects updated values resulting from actions in the user interface (UI) or Automation to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c2caa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c2caa-105">Syntax</span></span>

<span data-ttu-id="c2caa-106">REFERENCIA SETATREF(\*\*  \*\* [, \*\* *set_expression* \*\* [, \*\* *ignore_eval* \*\* ]])</span><span class="sxs-lookup"><span data-stu-id="c2caa-106">SETATREF(\*\* *reference* \*\* [, \*\* *set_expression* \*\* [, \*\* *ignore_eval* \*\* ]])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c2caa-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c2caa-107">Parameters</span></span>

|<span data-ttu-id="c2caa-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="c2caa-108">**Name**</span></span>|<span data-ttu-id="c2caa-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="c2caa-109">**Required/Optional**</span></span>|<span data-ttu-id="c2caa-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="c2caa-110">**Data Type**</span></span>|<span data-ttu-id="c2caa-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c2caa-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c2caa-112">_reference_</span><span class="sxs-lookup"><span data-stu-id="c2caa-112">_reference_</span></span> <br/> |<span data-ttu-id="c2caa-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="c2caa-113">Required</span></span>  <br/> |<span data-ttu-id="c2caa-114">**String**</span><span class="sxs-lookup"><span data-stu-id="c2caa-114">**String**</span></span> <br/> |<span data-ttu-id="c2caa-115">Referencia a la celda adonde se redirigen las actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="c2caa-115">A reference to the cell where updates are redirected.</span></span>  <br/> |
| <span data-ttu-id="c2caa-116">_set_expression_</span><span class="sxs-lookup"><span data-stu-id="c2caa-116">_set_expression_</span></span> <br/> |<span data-ttu-id="c2caa-117">Opcional</span><span class="sxs-lookup"><span data-stu-id="c2caa-117">Optional</span></span>  <br/> |<span data-ttu-id="c2caa-118">**String**</span><span class="sxs-lookup"><span data-stu-id="c2caa-118">**String**</span></span> <br/> |<span data-ttu-id="c2caa-119">Expresión que se asigna a  _la referencia_.</span><span class="sxs-lookup"><span data-stu-id="c2caa-119">An expression that is assigned to  _reference_.</span></span>  <br/> |
| <span data-ttu-id="c2caa-120">_ignore_eval_</span><span class="sxs-lookup"><span data-stu-id="c2caa-120">_ignore_eval_</span></span> <br/> |<span data-ttu-id="c2caa-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="c2caa-121">Optional</span></span>  <br/> |<span data-ttu-id="c2caa-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="c2caa-122">**Boolean**</span></span> <br/> |<span data-ttu-id="c2caa-123">Si es TRUE, la función SETATREF se evalúa en (0) cero; si FALSE (valor predeterminado) la función SETATREF evalúa el valor de  _referencia_.</span><span class="sxs-lookup"><span data-stu-id="c2caa-123">If TRUE, the SETATREF function evaluates to (0) zero; if FALSE (the default) the SETATREF function evaluates to the value of  _reference_.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c2caa-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c2caa-124">Remarks</span></span>

<span data-ttu-id="c2caa-125">Cuando una acción del usuario en la ventana de dibujo o un método de automatización hace que Microsoft Visio actualice una celda que contiene una fórmula SETATREF, el valor se redirige en su lugar a la celda a la que hace referencia la fórmula SETATREF _(_ referencia ).</span><span class="sxs-lookup"><span data-stu-id="c2caa-125">When a user action in the drawing window, or an Automation method, causes Microsoft Visio to update a cell containing a SETATREF formula, the value is instead redirected to the cell referenced by the SETATREF formula ( _reference_).</span></span> <span data-ttu-id="c2caa-126">La fórmula de la celda que contiene la función SETATREF permanece intacta.</span><span class="sxs-lookup"><span data-stu-id="c2caa-126">The formula in the cell containing the SETATREF function remains intact.</span></span>
  
<span data-ttu-id="c2caa-127">Si  _set_expression_ se omite, el valor establecido en la interfaz de usuario o mediante automatización se asigna a la celda a la que se hace referencia; de lo contrario, el  _contenido set_expression_ se asigna a la celda a la que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="c2caa-127">If  _set_expression_ is omitted, the value set in the UI or by using Automation is assigned to the referenced cell; otherwise, the contents of  _set_expression_ are assigned to the referenced cell.</span></span> <span data-ttu-id="c2caa-128">Esto permite modificar o transformar el nuevo valor antes de asignarlo a la celda de referencia.</span><span class="sxs-lookup"><span data-stu-id="c2caa-128">This allows the new value to be modified or transformed before being assigned to the referenced cell.</span></span> 
  
<span data-ttu-id="c2caa-129">La función SETATREF cuenta con dos funciones relacionadas:</span><span class="sxs-lookup"><span data-stu-id="c2caa-129">The SETATREF function has two related functions:</span></span> 
  
- <span data-ttu-id="c2caa-130">La función SETATREFEXPR, que puede usar para representar el nuevo valor dentro de  _set_expression_.</span><span class="sxs-lookup"><span data-stu-id="c2caa-130">The SETATREFEXPR function, which you can use to represent the new value within  _set_expression_.</span></span> <span data-ttu-id="c2caa-131">Por ejemplo, una  _set_expression_ de SETATREFEXPR()-2 in.</span><span class="sxs-lookup"><span data-stu-id="c2caa-131">For example, a  _set_expression_ of SETATREFEXPR()-2 in.</span></span> <span data-ttu-id="c2caa-132">podría usarse para restar 2 pulgadas del resultado SETATREFEXPR.</span><span class="sxs-lookup"><span data-stu-id="c2caa-132">could be used to subtract 2 inches from the SETATREFEXPR result.</span></span> 
    
- <span data-ttu-id="c2caa-133">La función SETATREFEVAL, que puede usar para  indicar que una parte de set_expression debe evaluarse y reemplazarse por su resultado.</span><span class="sxs-lookup"><span data-stu-id="c2caa-133">The SETATREFEVAL function, which you can use to indicate that some portion of  _set_expression_ should be evaluated and replaced by its result.</span></span> 
    
<span data-ttu-id="c2caa-134">La función SETATREF está diseñada para su uso en celdas que pueden cambiar las acciones del usuario en la ventana de dibujo.</span><span class="sxs-lookup"><span data-stu-id="c2caa-134">The SETATREF function is designed for use in cells that can be changed by user actions in the drawing window.</span></span> <span data-ttu-id="c2caa-135">Se admiten las siguientes celdas:</span><span class="sxs-lookup"><span data-stu-id="c2caa-135">The following cells are supported:</span></span>
  
- <span data-ttu-id="c2caa-136">Sección de transformación de forma: celdas Width, Height, Angle, PinX y PinY</span><span class="sxs-lookup"><span data-stu-id="c2caa-136">ShapeTransform section—Width, Height, Angle, PinX, and PinY cells</span></span>
    
- <span data-ttu-id="c2caa-137">Sección de transformación de texto: celdas TxtWidth, TxtHeight, TxtAngle, TxtPinX y TxtPinY</span><span class="sxs-lookup"><span data-stu-id="c2caa-137">Text Transform section—TxtWidth, TxtHeight, TxtAngle, TxtPinX, and TxtPinY cells</span></span>
    
- <span data-ttu-id="c2caa-138">Sección de extremos 1D: celdas BeginX, BeginY, EndX y EndY</span><span class="sxs-lookup"><span data-stu-id="c2caa-138">1-D Endpoints section—BeginX, BeginY, EndX, and EndY cells</span></span>
    
- <span data-ttu-id="c2caa-139">Sección de controles: celdas Controls.X y Controls.Y</span><span class="sxs-lookup"><span data-stu-id="c2caa-139">Controls section—Controls.X and Controls.Y cells</span></span>
    
- <span data-ttu-id="c2caa-140">Sección de datos de formas</span><span class="sxs-lookup"><span data-stu-id="c2caa-140">Shape Data section</span></span>
    
<span data-ttu-id="c2caa-141">Dado que SETATREF cambia la ubicación donde cambian los valores de celda, afecta al desencadenamiento de eventos.</span><span class="sxs-lookup"><span data-stu-id="c2caa-141">Because SETATREF changes the location where cell values change, it affects event firing.</span></span> <span data-ttu-id="c2caa-142">Si una celda contiene SETATREF, los eventos **FormulaChanged** y **CellChanged** se desencadenan para la celda a la que hace referencia SETATREF, no para la que contiene SETATREF.</span><span class="sxs-lookup"><span data-stu-id="c2caa-142">If a cell contains SETATREF, the **FormulaChanged** and **CellChanged** events fire for the cell that is referenced by SETATREF, not the cell containing SETATREF.</span></span> <span data-ttu-id="c2caa-143">Si una celda que contiene SETATREF también contiene SETATREFEXPR, el evento **FormulaChanged** también se activa para la celda que contiene SETATREF porque se cambia un parámetro de función.</span><span class="sxs-lookup"><span data-stu-id="c2caa-143">If a cell containing SETATREF also contains SETATREFEXPR, the **FormulaChanged** event also fires for the cell containing SETATREF because a function parameter is changed.</span></span> 
  
<span data-ttu-id="c2caa-144">A continuación se describen algunos puntos adicionales que conviene tener en cuenta al respecto de la función SETATREF:</span><span class="sxs-lookup"><span data-stu-id="c2caa-144">Other important points to note about the SETATREF function include the following:</span></span>
  
- <span data-ttu-id="c2caa-145">Las funciones SETATREF pueden encadenar hasta un máximo de 10 referencias a otras funciones SETATREF.</span><span class="sxs-lookup"><span data-stu-id="c2caa-145">SETATREF functions can chain up to 10 references to other SETATREF functions.</span></span> 
    
- <span data-ttu-id="c2caa-146">Las celdas pueden contener otras expresiones además de la función SETATREF, incluidas varias apariciones de SETATREF en una misma celda.</span><span class="sxs-lookup"><span data-stu-id="c2caa-146">Cells can contain other expressions in addition to the SETATREF function, including multiple occurrences of SETATREF in a single cell.</span></span>
    
- <span data-ttu-id="c2caa-147">Si las formas están pegadas, Visio sigue la cadena de referencias de SETATREF dentro de la misma hoja y coloca fórmulas de pegado en la celda referida.</span><span class="sxs-lookup"><span data-stu-id="c2caa-147">If shapes are glued, Visio follows the SETATREF reference chain within the same sheet and places glue formulas in the referenced cell.</span></span> 
    
- <span data-ttu-id="c2caa-148">La automatización reconoce la función SETATREF y sigue la cadena de celdas a las que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="c2caa-148">Automation recognizes the SETATREF function and follows the chain of referenced cells.</span></span> 
    
- <span data-ttu-id="c2caa-149">Al igual que ocurre con GUARD, SETATREF no protege las celdas de los cambios realizados mediante la función SETF en ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="c2caa-149">Like GUARD, SETATREF does not protect cells from changes made by using the SETF function in the ShapeSheet.</span></span>
    
## <a name="example1"></a><span data-ttu-id="c2caa-150">Ejemplo1</span><span class="sxs-lookup"><span data-stu-id="c2caa-150">Example1</span></span>

<span data-ttu-id="c2caa-151">Supongamos que una forma posee una propiedad personalizada llamada Width, y la celda Width de la sección de transformación de forma contiene la siguiente fórmula:</span><span class="sxs-lookup"><span data-stu-id="c2caa-151">Let's say that a shape has a custom property called Width, and that the Width cell in the Shape Transform section contains the following formula:</span></span>
  
<span data-ttu-id="c2caa-152">=SETATREF(Prop.Width)</span><span class="sxs-lookup"><span data-stu-id="c2caa-152">=SETATREF(Prop.Width)</span></span>
  
<span data-ttu-id="c2caa-153">Si un usuario cambiara el ancho de la forma en la interfaz de usuario, el nuevo valor se asigna a la celda Prop.Width, no a la celda Width de la sección ShapeTransform; la fórmula de la celda Width permanece sin cambios.</span><span class="sxs-lookup"><span data-stu-id="c2caa-153">If a user were to change the shape's width in the UI, the new value is assigned to the Prop.Width cell, not to the Width cell in the ShapeTransform section; the formula in the Width cell remains unchanged.</span></span> <span data-ttu-id="c2caa-154">También es posible establecer el ancho de la forma mediante los datos de formas.</span><span class="sxs-lookup"><span data-stu-id="c2caa-154">You can also set the shape's width by using shape data.</span></span>
  
## <a name="example2"></a><span data-ttu-id="c2caa-155">Ejemplo2</span><span class="sxs-lookup"><span data-stu-id="c2caa-155">Example2</span></span>

<span data-ttu-id="c2caa-p107">Las soluciones de Visio suelen contar con formas relacionadas jerárquicamente, y así se precisa que las formas secundarias se muevan cuando lo hace una principal. A continuación se muestra un ejemplo de cómo se puede administrar esta relación con la función SETATREF en ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="c2caa-p107">Visio solutions often have shapes that have a hierarchical relationship, requiring child shapes to move when a parent shape is moved. Following is an example of how you might manage this relationship using the SETATREF function in the ShapeSheet.</span></span> 
  
<span data-ttu-id="c2caa-p108">Las siguientes fórmulas se encuentran en la sección de transformación de formas de la forma secundaria. Además, definimos unas celdas de usuario llamadas Usuario.DeltaX y Usuario.DeltaY, que rastrean la cota de desplazamiento de ParentShape. Esto permite a la forma secundaria moverse cuando lo hace la principal, además de preservar la jerarquía si se mueve la secundaria.</span><span class="sxs-lookup"><span data-stu-id="c2caa-p108">The following formulas are contained in the Shape Transform section of the child shape. Also, we define user cells called User.DeltaX and User.DeltaY, which track the offset dimension from ParentShape. This allows the child shape to move when the parent shape is moved, and also to preserve the hierarchical relationship if the child shape is moved.</span></span>
  
<span data-ttu-id="c2caa-161">PinX =SETATREF(Usuario.DeltaX; SETATREFEVAL(SETATREFEXPR() - ParentShape!PinX)) + ParentShape!PinX</span><span class="sxs-lookup"><span data-stu-id="c2caa-161">PinX =SETATREF(User.DeltaX, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinX)) + ParentShape!PinX</span></span>
  
<span data-ttu-id="c2caa-162">PinY =SETATREF(Usuario.DeltaY; SETATREFEVAL(SETATREFEXPR() - ParentShape!PinY)) + ParentShape!PinY</span><span class="sxs-lookup"><span data-stu-id="c2caa-162">PinY =SETATREF(User.DeltaY, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinY)) + ParentShape!PinY</span></span>
  
<span data-ttu-id="c2caa-163">Cuando la forma secundaria se mueve mediante la interfaz de usuario, los nuevos valores PinX y PinY se establecen como parámetro en la función SETATREFEXPR.</span><span class="sxs-lookup"><span data-stu-id="c2caa-163">When the child shape is moved using the UI, the new PinX and PinY values are set as the parameter in the SETATREFEXPR function.</span></span> <span data-ttu-id="c2caa-164">La función SETATREF evalúa la fórmula incluida en SETATREFEVAL y reemplaza PinX y PinY con sus resultados y, a continuación, la fórmula resultante se asigna a las celdas de usuario a las que se hace referencia en la función SETATREF: User.DeltaX y User.DeltaY.</span><span class="sxs-lookup"><span data-stu-id="c2caa-164">The SETATREF function evaluates the formula enclosed in SETATREFEVAL and replaces PinX and PinY with their results, and then the resulting formula is assigned to the user cells referenced in the SETATREF function—User.DeltaX and User.DeltaY.</span></span> <span data-ttu-id="c2caa-165">Por último, los valores devueltos por SETATREF (User.DeltaX o User.DeltaY) se agregan a la ubicación de patillas de ParentShape para calcular la ubicación del pin de la forma secundaria.</span><span class="sxs-lookup"><span data-stu-id="c2caa-165">Lastly, the values returned by SETATREF (User.DeltaX or User.DeltaY) are added to the pin location of ParentShape to calculate the child shape's pin location.</span></span>
  

