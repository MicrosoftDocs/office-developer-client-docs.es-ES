---
title: Celda ShdwForegnd (Sección de formato de relleno)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251244
localization_priority: Normal
ms.assetid: ea153390-631d-79fd-c1ba-4c281239a24e
description: Determina el color utilizado para el primer plano (trazo) de la trama de relleno sombreado de la forma.
ms.openlocfilehash: 602df83dcb88d4137b0609f9a8b1084a40148a10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422253"
---
# <a name="shdwforegnd-cell-fill-format-section"></a><span data-ttu-id="3f1fd-103">Celda ShdwForegnd (Sección de formato de relleno)</span><span class="sxs-lookup"><span data-stu-id="3f1fd-103">ShdwForegnd Cell (Fill Format Section)</span></span>

<span data-ttu-id="3f1fd-104">Determina el color utilizado para el primer plano (trazo) de la trama de relleno sombreado de la forma.</span><span class="sxs-lookup"><span data-stu-id="3f1fd-104">Determines the color used for the foreground (stroke) of the shape's drop shadow fill pattern.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3f1fd-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3f1fd-105">Remarks</span></span>

<span data-ttu-id="3f1fd-106">Para establecer el color, escriba un número entre 0 y 23, que corresponde al índice de la colección de colores.</span><span class="sxs-lookup"><span data-stu-id="3f1fd-106">To set the color, enter a number from 0 to 23, which is an index into a collection of colors.</span></span>
  
<span data-ttu-id="3f1fd-107">Para especificar un color personalizado, utilice la función RGB o HSL.</span><span class="sxs-lookup"><span data-stu-id="3f1fd-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="3f1fd-108">El valor de un color personalizado es su color RGB y RGB( *r, g, b*), en lugar de un número, se mostrará en la ventana ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="3f1fd-108">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="3f1fd-109">Cuando se utilizan en operaciones numéricas, los colores personalizados tienen valores iguales o mayores que 24.</span><span class="sxs-lookup"><span data-stu-id="3f1fd-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="3f1fd-110">Puede establecer la transparencia del color de primer plano de la trama de relleno sombreado de la forma en la celda ShdwForegndTrans.</span><span class="sxs-lookup"><span data-stu-id="3f1fd-110">You can set the transparency of the foreground color of the shape's drop shadow fill pattern in the ShdwForegndTrans cell.</span></span>
  
<span data-ttu-id="3f1fd-111">Para obtener una referencia a la celda ShdwForegnd por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="3f1fd-111">To get a reference to the ShdwForegnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3f1fd-112">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="3f1fd-112">Cell name:</span></span>  <br/> | <span data-ttu-id="3f1fd-113">ShdwForegnd</span><span class="sxs-lookup"><span data-stu-id="3f1fd-113">ShdwForegnd</span></span>  <br/> |
   
<span data-ttu-id="3f1fd-114">Para obtener una referencia desde un programa a la celda ShdwForegnd por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="3f1fd-114">To get a reference to the ShdwForegnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3f1fd-115">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="3f1fd-115">Section index:</span></span>  <br/> |<span data-ttu-id="3f1fd-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3f1fd-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3f1fd-117">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="3f1fd-117">Row index:</span></span>  <br/> |<span data-ttu-id="3f1fd-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="3f1fd-118">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="3f1fd-119">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="3f1fd-119">Cell index:</span></span>  <br/> |<span data-ttu-id="3f1fd-120">**visFillShdwForegnd**</span><span class="sxs-lookup"><span data-stu-id="3f1fd-120">**visFillShdwForegnd**</span></span> <br/> |
   

