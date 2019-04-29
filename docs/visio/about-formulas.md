---
title: Fórmulas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251823
localization_priority: Normal
ms.assetid: ec0de3e1-21dc-c5d6-2c2a-d5fef80d89bd
description: La clave para controlar las acciones de una forma es escribir las fórmulas que definen el comportamiento deseado. Puede modificar la fórmula de una celda para cambiar su valor y, en consecuencia, cambiar el comportamiento de la forma correspondiente. Por ejemplo, la celda Height de la sección de transformación de forma contiene una fórmula que puede cambiar para modificar el alto de la forma.
ms.openlocfilehash: e8e1a2b77cc355e930af6f31f0b375dfba321e74
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426264"
---
# <a name="about-formulas"></a><span data-ttu-id="bd650-105">Fórmulas</span><span class="sxs-lookup"><span data-stu-id="bd650-105">About Formulas</span></span>

<span data-ttu-id="bd650-p102">La clave para controlar las acciones de una forma es escribir las fórmulas que definen el comportamiento deseado. Puede modificar la fórmula de una celda para cambiar su valor y, en consecuencia, cambiar el comportamiento de la forma correspondiente. Por ejemplo, la celda Height de la sección de transformación de forma contiene una fórmula que puede cambiar para modificar el alto de la forma.</span><span class="sxs-lookup"><span data-stu-id="bd650-p102">The key to controlling shape actions is to write formulas that define the behavior you want. You can edit a cell's formula to change the value of the cell and, as a result, change a particular shape's behavior. For example, the Height cell in the Shape Transform section contains a formula that you can change to alter the shape's height.</span></span>
  
<span data-ttu-id="bd650-p103">Las fórmulas de Microsoft Visio son muy similares a las habituales en las hojas de cálculo. Visio considera todo el contenido de una celda como una fórmula, incluso si sólo es un valor numérico o una simple referencia a otra celda.</span><span class="sxs-lookup"><span data-stu-id="bd650-p103">Microsoft Visio formulas are similar to typical spreadsheet formulas in many ways. Visio regards anything in a cell, even if it is a numeric value or simple cell reference, as a formula.</span></span>
  
<span data-ttu-id="bd650-p104">La fórmula de una celda puede heredarse de la celda equivalente de un patrón o estilo, o puede definirse localmente. Visio evalúa la fórmula y convierte el resultado en un valor adecuado para la celda, con las unidades correspondientes. En la ventana ShapeSheet, puede mostrar el contenido de las celdas como fórmulas o como valores.</span><span class="sxs-lookup"><span data-stu-id="bd650-p104">A formula in a cell can be inherited from the equivalent cell of a master or a style or defined locally. Visio evaluates the formula and then converts the results to an appropriate value and appropriate units for the cell. In a ShapeSheet window, you can display cell contents as either formulas or values.</span></span>
  
## <a name="elements-of-a-formula"></a><span data-ttu-id="bd650-114">Elementos de una fórmula</span><span class="sxs-lookup"><span data-stu-id="bd650-114">Elements of a formula</span></span>

<span data-ttu-id="bd650-p105">Una fórmula siempre comienza por un signo igual, que se inserta automáticamente. Una fórmula puede contener cualquiera de los elementos siguientes:</span><span class="sxs-lookup"><span data-stu-id="bd650-p105">A formula always starts with an equal sign, which is inserted automatically. A formula can include any of the following elements:</span></span>
  
- <span data-ttu-id="bd650-117">Números</span><span class="sxs-lookup"><span data-stu-id="bd650-117">Numbers</span></span>
    
- <span data-ttu-id="bd650-118">Unas</span><span class="sxs-lookup"><span data-stu-id="bd650-118">Coordinates</span></span>
    
- <span data-ttu-id="bd650-119">Valores booleanos</span><span class="sxs-lookup"><span data-stu-id="bd650-119">Boolean values</span></span>
    
- <span data-ttu-id="bd650-120">Operadores</span><span class="sxs-lookup"><span data-stu-id="bd650-120">Operators</span></span>
    
- <span data-ttu-id="bd650-121">Funciones</span><span class="sxs-lookup"><span data-stu-id="bd650-121">Functions</span></span>
    
- <span data-ttu-id="bd650-122">Cadenas</span><span class="sxs-lookup"><span data-stu-id="bd650-122">Strings</span></span>
    
- <span data-ttu-id="bd650-123">Referencias a celdas</span><span class="sxs-lookup"><span data-stu-id="bd650-123">Cell references</span></span>
    
- <span data-ttu-id="bd650-124">Unidades de medida</span><span class="sxs-lookup"><span data-stu-id="bd650-124">Units of measure</span></span>
    
## <a name="default-formulas"></a><span data-ttu-id="bd650-125">Fórmulas predeterminadas</span><span class="sxs-lookup"><span data-stu-id="bd650-125">Default formulas</span></span>

<span data-ttu-id="bd650-p106">Al crear una forma, Visio crea fórmulas para ella de manera predeterminada. Para ver estas fórmulas predeterminadas, dibuje una forma simple (como un rectángulo, una elipse o una línea recta) y abra la ventana ShapeSheet (en la ficha [Programador](run-in-developer-mode-display-the-developer-tab.md), haga clic en **Mostrar ShapeSheet**).</span><span class="sxs-lookup"><span data-stu-id="bd650-p106">When you create a shape, Visio creates formulas for it by default. To see what the default formulas are, draw a simple shape (such as a rectangle, ellipse, or straight line) and open its ShapeSheet window (on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, click **Show ShapeSheet**).</span></span>
  
## <a name="inherited-formulas"></a><span data-ttu-id="bd650-128">Fórmulas heredadas</span><span class="sxs-lookup"><span data-stu-id="bd650-128">Inherited formulas</span></span>

<span data-ttu-id="bd650-p107">Visio utiliza la herencia de fórmulas siempre que es posible. En lugar de hacer una copia local de cada fórmula de la instancia, ésta hereda fórmulas de su patrón en la galería de símbolos de documento y hereda el formato de la definición de estilo almacenada con el dibujo. Así los archivos son más pequeños y, además, los cambios en las fórmulas del patrón o en la definición del estilo se propagan a todas las instancias.</span><span class="sxs-lookup"><span data-stu-id="bd650-p107">Visio inherits formulas whenever possible. Rather than make a local copy of every formula in the instance, an instance inherits formulas from its master on the document stencil and inherits formatting from the style definition stored with the drawing. This behavior results in smaller files, but also allows changes to the master's formulas or the style definition to be propagated to all instances.</span></span>
  
<span data-ttu-id="bd650-132">Las fórmulas heredadas aparecen en las celdas con texto negro.</span><span class="sxs-lookup"><span data-stu-id="bd650-132">Black text in a cell indicates an inherited formula.</span></span>
  
## <a name="local-formulas"></a><span data-ttu-id="bd650-133">Fórmulas locales</span><span class="sxs-lookup"><span data-stu-id="bd650-133">Local formulas</span></span>

<span data-ttu-id="bd650-p108">Al escribir una fórmula local para una instancia, reemplazará la fórmula heredada en la celda por otra que la suplanta. Los cambios posteriores a la celda en el patrón o el estilo no afectarán a esta instancia, porque con la fórmula local se ha bloqueado la herencia para esa celda.</span><span class="sxs-lookup"><span data-stu-id="bd650-p108">When you write a local formula for an instance, you are replacing the inherited formula in the cell with a local override. Future changes to that cell in the master or style do not affect this instance because it has blocked inheritance for the cell with the local override.</span></span>
  
<span data-ttu-id="bd650-136">Al aplicar un estilo se eliminan todas las fórmulas locales de las celdas relacionadas a menos que use la función GUARD para protegerlas.</span><span class="sxs-lookup"><span data-stu-id="bd650-136">Applying a style deletes all local formulas in the related cells unless you use the GUARD function to protect them.</span></span>
  
<span data-ttu-id="bd650-137">El texto azul indica que la fórmula es local, como resultado de modificar la fórmula en la ventana ShapeSheet o por algún cambio en la forma que haya causado que Visio cambie la fórmula de esa celda.</span><span class="sxs-lookup"><span data-stu-id="bd650-137">Blue text indicates a local formula, either the result of editing the formula in a ShapeSheet window or some change to the shape that caused Visio to reset the formula for that cell.</span></span>
  
## <a name="automatic-updates-to-formulas"></a><span data-ttu-id="bd650-138">Actualizaciones automáticas de las fórmulas</span><span class="sxs-lookup"><span data-stu-id="bd650-138">Automatic updates to formulas</span></span>

 <span data-ttu-id="bd650-p109">Visio actualiza automáticamente algunas celdas cuando se cambia una forma en un dibujo. Esto significa que, en algunas circunstancias, las fórmulas que escriba pueden ser reemplazadas. Por ejemplo, si arrastra el controlador de una esquina para cambiar el tamaño de una forma, Visio restablece las fórmulas de las celdas PinX, PinY, Width y Height.</span><span class="sxs-lookup"><span data-stu-id="bd650-p109">Visio automatically updates certain cells whenever you change a shape in a drawing. This means that under some circumstances formulas you enter can be replaced. For example, if you drag a corner handle to resize a shape, Visio resets formulas in the PinX, PinY, Width, and Height cells.</span></span> 
  
<span data-ttu-id="bd650-142">Si es necesario, puede proteger las fórmulas para evitar cambios mediante la función GUARD.</span><span class="sxs-lookup"><span data-stu-id="bd650-142">If necessary, you can protect formulas against changes by using the GUARD function.</span></span>
  

