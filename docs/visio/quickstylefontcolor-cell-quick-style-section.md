---
title: Celda QuickStyleFontColor (sección estilos rápidos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31c56d08-19ea-4b8b-8be7-42e1c736fbca
description: Determina el color de fuente de los estilos rápidos que hereda el texto de una forma del tema activo, como un entero de 0-1.
ms.openlocfilehash: bd645383df02260fcf6a2045764d9a1b44126090
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282638"
---
# <a name="quickstylefontcolor-cell-quick-style-section"></a><span data-ttu-id="18093-103">Celda QuickStyleFontColor (sección estilos rápidos)</span><span class="sxs-lookup"><span data-stu-id="18093-103">QuickStyleFontColor Cell (Quick Style Section)</span></span>

<span data-ttu-id="18093-104">Determina el color de fuente de los estilos rápidos que hereda el texto de una forma del tema activo, como un entero de 0-1.</span><span class="sxs-lookup"><span data-stu-id="18093-104">Determines the font color from the Quick Styles that a shape's text inherits from the active theme, as an integer from 0-1.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="18093-105">Valor</span><span class="sxs-lookup"><span data-stu-id="18093-105">Value</span></span>  <br/> |<span data-ttu-id="18093-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="18093-106">Description</span></span>  <br/> |
|<span data-ttu-id="18093-107">comprendi</span><span class="sxs-lookup"><span data-stu-id="18093-107">0</span></span>  <br/> |<span data-ttu-id="18093-108">El texto de la forma utiliza el color de fuente oscuro.</span><span class="sxs-lookup"><span data-stu-id="18093-108">The shape text uses the Dark font color.</span></span>  <br/> |
|<span data-ttu-id="18093-109">1</span><span class="sxs-lookup"><span data-stu-id="18093-109">1</span></span>  <br/> |<span data-ttu-id="18093-110">El texto de la forma usa el color de fuente claro.</span><span class="sxs-lookup"><span data-stu-id="18093-110">The shape text uses the Light font color.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18093-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="18093-111">Remarks</span></span>

<span data-ttu-id="18093-112">Para obtener una referencia a la celda **QuickStyleFontColor** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="18093-112">To get a reference to the **QuickStyleFontColor** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="18093-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="18093-113">Cell name:</span></span>  <br/> | <span data-ttu-id="18093-114">QuickStyleFontColor</span><span class="sxs-lookup"><span data-stu-id="18093-114">QuickStyleFontColor</span></span>  <br/> |
   
<span data-ttu-id="18093-115">Para obtener una referencia desde un programa a la celda **QuickStyleFontColor** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="18093-115">To get a reference to the **QuickStyleFontColor** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="18093-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="18093-116">Section index:</span></span>  <br/> |<span data-ttu-id="18093-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="18093-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="18093-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="18093-118">Row index:</span></span>  <br/> |<span data-ttu-id="18093-119">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="18093-119">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="18093-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="18093-120">Cell index:</span></span>  <br/> |<span data-ttu-id="18093-121">**visQuickStyleFontColor**</span><span class="sxs-lookup"><span data-stu-id="18093-121">**visQuickStyleFontColor**</span></span> <br/> |
   

