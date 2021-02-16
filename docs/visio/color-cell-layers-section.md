---
title: Celda Color (Sección de capas)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm165
localization_priority: Normal
ms.assetid: 61c19342-46fb-48d4-6375-c9ea8306286d
description: Especifica el color utilizado para mostrar la capa.
ms.openlocfilehash: a2eef24187165cabfdfc8dee49747a2381562d3e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435134"
---
# <a name="color-cell-layers-section"></a><span data-ttu-id="d026e-103">Celda Color (Sección de capas)</span><span class="sxs-lookup"><span data-stu-id="d026e-103">Color Cell (Layers Section)</span></span>

<span data-ttu-id="d026e-104">Especifica el color utilizado para mostrar la capa.</span><span class="sxs-lookup"><span data-stu-id="d026e-104">Specifies the color used to display the layer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d026e-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d026e-105">Remarks</span></span>

<span data-ttu-id="d026e-106">Para establecer el color, escriba un número entre el 0 y el 23.</span><span class="sxs-lookup"><span data-stu-id="d026e-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="d026e-107">Este valor de celda corresponde a  la configuración de **color** de capa  en el  cuadro de diálogo Propiedades de capa (en el grupo Edición de la ficha Inicio, haga clic en Capas y, a continuación, haga clic en Propiedades **de capa).** </span><span class="sxs-lookup"><span data-stu-id="d026e-107">This cell value corresponds to the **Layer color** setting in the **Layer Properties** dialog box (in the **Editing** group on the **Home** tab, click **Layers** and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="d026e-108">Para especificar un color personalizado, utilice la función RGB o HSL.</span><span class="sxs-lookup"><span data-stu-id="d026e-108">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="d026e-109">El valor de un color personalizado es su color RGB y RGB( *r, g, b*), en lugar de un número, se mostrará en la ventana ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="d026e-109">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="d026e-110">Cuando se utilizan en operaciones numéricas, los colores personalizados tienen valores iguales o mayores que 24.</span><span class="sxs-lookup"><span data-stu-id="d026e-110">When used in numeric operations, custom colors have values of 24 and above.</span></span> <span data-ttu-id="d026e-111">Un valor de 255 indica que la capa no tiene color.</span><span class="sxs-lookup"><span data-stu-id="d026e-111">A value of 255 indicates that the layer has no color.</span></span> 
  
<span data-ttu-id="d026e-112">Puede establecer la transparencia del color de la capa en la celda Transparency.</span><span class="sxs-lookup"><span data-stu-id="d026e-112">You can set the transparency of the layer color in the Transparency cell.</span></span>
  
<span data-ttu-id="d026e-113">Para obtener una referencia a la celda Color por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="d026e-113">To get a reference to the Color cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d026e-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="d026e-114">Cell name:</span></span>  <br/> |<span data-ttu-id="d026e-115">Layers.Color[ *i*  ] donde  *i*  = <1>, 2, 3, ...</span><span class="sxs-lookup"><span data-stu-id="d026e-115">Layers.Color[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="d026e-116">Para obtener una referencia desde un programa a la celda Color por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="d026e-116">To get a reference to the Color cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d026e-117">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="d026e-117">Section index:</span></span>  <br/> |<span data-ttu-id="d026e-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="d026e-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="d026e-119">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="d026e-119">Row index:</span></span>  <br/> |<span data-ttu-id="d026e-120">**visRowLayer**  +   *i* donde *i* = 0, 1, 2, ...</span><span class="sxs-lookup"><span data-stu-id="d026e-120">**visRowLayer** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="d026e-121">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="d026e-121">Cell index:</span></span>  <br/> |<span data-ttu-id="d026e-122">**visLayerColor**</span><span class="sxs-lookup"><span data-stu-id="d026e-122">**visLayerColor**</span></span> <br/> |
   

