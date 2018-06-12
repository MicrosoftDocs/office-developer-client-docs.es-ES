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
ms.openlocfilehash: f39109a296949d23142017661bb55f0708402d8f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823216"
---
# <a name="shdwforegnd-cell-fill-format-section"></a><span data-ttu-id="66d18-103">Celda ShdwForegnd (Sección de formato de relleno)</span><span class="sxs-lookup"><span data-stu-id="66d18-103">ShdwForegnd Cell (Fill Format Section)</span></span>

<span data-ttu-id="66d18-104">Determina el color utilizado para el primer plano (trazo) de la trama de relleno sombreado de la forma.</span><span class="sxs-lookup"><span data-stu-id="66d18-104">Determines the color used for the foreground (stroke) of the shape's drop shadow fill pattern.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="66d18-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="66d18-105">Remarks</span></span>

<span data-ttu-id="66d18-106">Para establecer el color, escriba un número entre 0 y 23, que corresponde al índice de la colección de colores.</span><span class="sxs-lookup"><span data-stu-id="66d18-106">To set the color, enter a number from 0 to 23, which is an index into a collection of colors.</span></span>
  
<span data-ttu-id="66d18-107">Para especificar un color personalizado, utilice la función RGB o HSL.</span><span class="sxs-lookup"><span data-stu-id="66d18-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="66d18-108">El valor de un color personalizado es su color RGB y RGB ( *r, g, b*), en lugar de un número, se mostrarán en la ventana ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="66d18-108">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="66d18-109">Cuando se usa en operaciones numéricas, los colores personalizados tienen valores de 24 y superior.</span><span class="sxs-lookup"><span data-stu-id="66d18-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="66d18-110">Puede establecer la transparencia del color de primer plano de la trama de relleno sombreado de la forma en la celda ShdwForegndTrans.</span><span class="sxs-lookup"><span data-stu-id="66d18-110">You can set the transparency of the foreground color of the shape's drop shadow fill pattern in the ShdwForegndTrans cell.</span></span>
  
<span data-ttu-id="66d18-111">Para obtener una referencia a la celda ShdwForegnd por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="66d18-111">To get a reference to the ShdwForegnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="66d18-112">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="66d18-112">Cell name:</span></span>  <br/> | <span data-ttu-id="66d18-113">ShdwForegnd</span><span class="sxs-lookup"><span data-stu-id="66d18-113">ShdwForegnd</span></span>  <br/> |
   
<span data-ttu-id="66d18-114">Para obtener una referencia a la celda ShdwForegnd por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="66d18-114">To get a reference to the ShdwForegnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="66d18-115">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="66d18-115">Section index:</span></span>  <br/> |<span data-ttu-id="66d18-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="66d18-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="66d18-117">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="66d18-117">Row index:</span></span>  <br/> |<span data-ttu-id="66d18-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="66d18-118">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="66d18-119">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="66d18-119">Cell index:</span></span>  <br/> |<span data-ttu-id="66d18-120">**visFillShdwForegnd**</span><span class="sxs-lookup"><span data-stu-id="66d18-120">**visFillShdwForegnd**</span></span> <br/> |
   

