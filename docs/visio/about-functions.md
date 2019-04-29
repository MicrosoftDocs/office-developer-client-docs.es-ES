---
title: Funciones
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251825
localization_priority: Normal
ms.assetid: 871b8601-8117-bc51-17b9-6002234b4bfb
description: 'Una función realiza una sola tarea bien definida. La mayor parte de las funciones precisan algunos argumentos como entrada. Aunque el tipo y el número de argumentos depende de la función, todas tienen la misma sintaxis general:'
ms.openlocfilehash: 14995b0f7e3c1cc8346d47965038902b8ca4e8bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415981"
---
# <a name="about-functions"></a><span data-ttu-id="33b9c-105">Funciones</span><span class="sxs-lookup"><span data-stu-id="33b9c-105">About Functions</span></span>

<span data-ttu-id="33b9c-p102">Una función realiza una sola tarea bien definida. La mayor parte de las funciones precisan algunos argumentos como entrada. Aunque el tipo y el número de argumentos depende de la función, todas tienen la misma sintaxis general:</span><span class="sxs-lookup"><span data-stu-id="33b9c-p102">A function performs a single well-defined task. Most functions take a number of arguments as input. Although the type and number of arguments depend on the function, all functions have the same general syntax:</span></span>
  
 <span data-ttu-id="33b9c-109">**Función (** _argumento1_, _argument2_,...</span><span class="sxs-lookup"><span data-stu-id="33b9c-109">**FUNCTION(** _argument1_,  _argument2_, …</span></span>  <span data-ttu-id="33b9c-110">_argumenton_ [, __ |  __ argumento argumento **])**</span><span class="sxs-lookup"><span data-stu-id="33b9c-110">_argumentN_ [,  _argumentA_ |  _argument_ **])**</span></span>
  
|<span data-ttu-id="33b9c-111">**Elemento de sintaxis**</span><span class="sxs-lookup"><span data-stu-id="33b9c-111">**Syntax element**</span></span>|<span data-ttu-id="33b9c-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="33b9c-112">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="33b9c-113">( )</span><span class="sxs-lookup"><span data-stu-id="33b9c-113"></span></span>  <br/> | <span data-ttu-id="33b9c-114">Si una función no tiene argumentos, debe ir seguida de paréntesis vacíos ().</span><span class="sxs-lookup"><span data-stu-id="33b9c-114">If a function takes no arguments, it must be followed by an empty set of parentheses ( ).</span></span>  <br/> |
| <span data-ttu-id="33b9c-115">,</span><span class="sxs-lookup"><span data-stu-id="33b9c-115"></span></span>  <br/> | <span data-ttu-id="33b9c-116">Los argumentos se separan con comas.</span><span class="sxs-lookup"><span data-stu-id="33b9c-116">Arguments are separated by a comma.</span></span>  <br/> |
| <span data-ttu-id="33b9c-117">...</span><span class="sxs-lookup"><span data-stu-id="33b9c-117"></span></span>  <br/> | <span data-ttu-id="33b9c-118">Sólo se utiliza para la notación, no lo incluya en una función.</span><span class="sxs-lookup"><span data-stu-id="33b9c-118">Used for notation only; do not include in a function.</span></span>  <br/> |
| <span data-ttu-id="33b9c-119">[ ]</span><span class="sxs-lookup"><span data-stu-id="33b9c-119"></span></span>  <br/> | <span data-ttu-id="33b9c-p104">Argumento opcional. Sólo se utiliza para la notación, no lo incluya en una función.</span><span class="sxs-lookup"><span data-stu-id="33b9c-p104">Optional argument. Used for notation only; do not include in a function.</span></span>  <br/> |
| |  <br/> | <span data-ttu-id="33b9c-122">Una opción; puede incluir _argument_ o _argumento_.</span><span class="sxs-lookup"><span data-stu-id="33b9c-122">A choice; you can include  _argumentA_ or  _argument_.</span></span> <span data-ttu-id="33b9c-123">Sólo se utiliza para la notación, no lo incluya en una función.</span><span class="sxs-lookup"><span data-stu-id="33b9c-123">Used for notation only; do not include in a function.</span></span>  <br/> |
   
<span data-ttu-id="33b9c-p106">Muchas de las funciones que pueden utilizarse en las fórmulas son similares a las habituales en los programas de hoja de cálculo: matemáticas, como SUM o SQRT, trigonométricas, como SIN o COS, o lógicas, como IF o NOT. Muchas otras funciones son únicas de Microsoft Office Visio, como GUARD, GRAVITY y RUNADDON.</span><span class="sxs-lookup"><span data-stu-id="33b9c-p106">Many functions that you can use in formulas resemble those you have seen in spreadsheet programs: mathematical, such as SUM or SQRT; trigonometric, such as SIN or COS; or logical, such as IF or NOT. Many other functions are unique to Microsoft Office Visio, such as GUARD, GRAVITY, and RUNADDON.</span></span>
  
<span data-ttu-id="33b9c-126">Para obtener más información acerca de funciones específicas, vea esta Referencia de ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="33b9c-126">For more information on specific functions, see this ShapeSheet Reference.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="33b9c-127">Algunas funciones aparecen en las fórmulas generadas por Visio, pero no se muestran en el cuadro de diálogo **Editar fórmula** ni se describen en esta referencia porque están reservadas para uso interno y no deben usarse en otras fórmulas.</span><span class="sxs-lookup"><span data-stu-id="33b9c-127">Certain functions appear in formulas generated by Visio, but are not shown in the **Edit Formula** dialog box or described in this reference because they are reserved for internal use and should not be used in other formulas.</span></span> <span data-ttu-id="33b9c-128">Los siguientes son algunos ejemplos: ELLIPSE_THETA, _ELLIPSE_ECC, _UCON_C1 y _SHAPEMIN.</span><span class="sxs-lookup"><span data-stu-id="33b9c-128">Following are examples: ELLIPSE_THETA, _ELLIPSE_ECC, _UCON_C1, and _SHAPEMIN.</span></span> 
  

