---
title: Ventana Explorador de estilos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm60119
localization_priority: Normal
ms.assetid: bfdc1a63-c355-c759-bdfa-ce27e3ad10e7
description: La ventana Explorador de estilos ofrece la forma a los programadores una manera rápida de determinar qué celdas de formas hereda de un estilo determinado, o el estilo desde el que hereda su valor una celda determinada.
ms.openlocfilehash: 25af478b8ac4e35c7ae0b88bf69aad21d679da17
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821487"
---
# <a name="about-the-style-explorer-window"></a><span data-ttu-id="4b2d1-103">Ventana Explorador de estilos</span><span class="sxs-lookup"><span data-stu-id="4b2d1-103">About the Style Explorer Window</span></span>

<span data-ttu-id="4b2d1-104">La ventana **Explorador de estilos** ofrece la forma a los programadores una manera rápida de determinar qué celdas de formas hereda de un estilo determinado, o el estilo desde el que hereda su valor una celda determinada.</span><span class="sxs-lookup"><span data-stu-id="4b2d1-104">The **Style Explorer** window provides shape developers with a quick way to determine which shape cells inherit from a given style, or the style from which a given cell inherits its value.</span></span> 
  
<span data-ttu-id="4b2d1-p101">Los estilos son conjuntos de atributos de formato que tienen un nombre particular y se pueden aplicar a una forma. En Microsoft Visio, un solo estilo puede definir los atributos de texto, líneas y relleno para asegurar la coherencia de manera eficiente entre las formas. Además, es posible definir un estilo para cualquier clase de atributo (texto, línea o relleno), o cualquier combinación de atributos.</span><span class="sxs-lookup"><span data-stu-id="4b2d1-p101">Styles are named collections of formatting attributes that you can apply to a shape. In Microsoft Visio, a single style can define text, line, and fill attributes as an efficient way to ensure consistency in your shapes. Additionally, you can also define a style for any one class of attribute (text, line, or fill) or any combination of attributes.</span></span> 
  
<span data-ttu-id="4b2d1-108">Al contrario de lo que ocurre al aplicar por separado atributos de formato a una forma, las formas cuyo formato deriva de un estilo tienen garantizada la coherencia y, además, responden mejor cuando son creadas, movidas, giradas y cuando se cambia su escala.</span><span class="sxs-lookup"><span data-stu-id="4b2d1-108">Unlike shapes to which you've applied formatting attributes individually, shapes that derive their formatting from a style not only ensure consistency but also respond better when they are created, moved, scaled, or rotated.</span></span> 
  
<span data-ttu-id="4b2d1-109">La ventana **Explorador de estilos** ofrece la información que necesaria para comprender mejor las consecuencias de los cambios realizados a las formas.</span><span class="sxs-lookup"><span data-stu-id="4b2d1-109">The **Style Explorer** window provides the information you need to understand better the implications of changes you make to shapes.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4b2d1-110">Los valores de celdas que aparecen en negro en la ventana ShapeSheet son heredados y, los que aparecen en azul, locales.</span><span class="sxs-lookup"><span data-stu-id="4b2d1-110">Cell values that appear black in the ShapeSheet window are inherited; those that appear blue are local.</span></span> 
  
## <a name="using-the-style-explorer-window"></a><span data-ttu-id="4b2d1-111">Uso de la ventana Explorador de estilos</span><span class="sxs-lookup"><span data-stu-id="4b2d1-111">Using the Style Explorer window</span></span>

<span data-ttu-id="4b2d1-112">Para ver la ventana **Explorador de estilos** , con la ventana ShapeSheet activa, en la ficha **Diseño de herramientas de ShapeSheet** , en el grupo **Ver** , seleccione **Explorador de estilos**.</span><span class="sxs-lookup"><span data-stu-id="4b2d1-112">To view the **Style Explorer** window, with the ShapeSheet window active, on the **ShapeSheet Tools Design** tab, in the **View** group, select **Style Explorer**.</span></span> <span data-ttu-id="4b2d1-113">La ventana **Explorador de estilos** aparece acoplada en la ventana ShapeSheet de forma predeterminada, pero es una ventana anclada que puede se puede acoplar, flotar o combinadas con otras ventanas de ShapeSheet disponibles, por ejemplo, la ventana **Rastreo de fórmulas** .</span><span class="sxs-lookup"><span data-stu-id="4b2d1-113">The **Style Explorer** window appears docked in the ShapeSheet window by default, but is an anchored window that can be docked, floated, or merged with other available anchored ShapeSheet windows, for example, the **Formula Tracing** window.</span></span> <span data-ttu-id="4b2d1-114">La ventana **Explorador de estilos** contiene una vista en árbol de todos los estilos definidos en el dibujo actual.</span><span class="sxs-lookup"><span data-stu-id="4b2d1-114">The **Style Explorer** window contains a treeview display of all the styles defined in the current drawing.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4b2d1-115">Para obtener información sobre un estilo, puede haga clic en el estilo en la ventana **Explorador de estilos** para ver su ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="4b2d1-115">To get information about a style, you can right-click the style in the **Style Explorer** window to view its ShapeSheet.</span></span> 
  
<span data-ttu-id="4b2d1-116">La ventana **Explorador de estilos** ofrece la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="4b2d1-116">The **Style Explorer** window provides the following information:</span></span> 
  
- <span data-ttu-id="4b2d1-117">Las celdas que heredan sus valores de un estilo seleccionado. Cuando se selecciona un estilo en la ventana **Explorador de estilos** , todas las celdas en la ventana ShapeSheet que heredan de ese estilo aparecen sin trama, mientras que las celdas que no heredan de ese estilo aparecen con una ligera trama.</span><span class="sxs-lookup"><span data-stu-id="4b2d1-117">The cells that inherit their values from a selected style.When you select a style in the **Style Explorer** window, all cells in the ShapeSheet window that inherit from that style appear without hatching, while cells that do not inherit from that style appear lightly hatched.</span></span> 
    
- <span data-ttu-id="4b2d1-118">El estilo del cual hereda su valor una celda seleccionada.Al seleccionar una celda de ShapeSheet, el estilo cuyo valor hereda se muestra en la barra de tareas que hay bajo la ventana ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="4b2d1-118">The style from which a selected cell inherits its value.When you select a ShapeSheet cell, the style from which it inherits its value is displayed on the taskbar under the ShapeSheet window.</span></span> 
    

