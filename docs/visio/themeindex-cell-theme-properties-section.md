---
title: Celda ThemeIndex (sección Propiedades de tema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21002267-1400-4398-b937-f5b289cf0ed2
description: Almacena la enumeración del tema integrado de Microsoft Visio que se ha aplicado al documento como un entero. Cuando se elige un nuevo tema para el documento, la celda ThemeIndex del documento y todas las páginas y formas que contiene se actualiza con el índice del tema integrado.
ms.openlocfilehash: 6ddede864a54fbd7127552499d3ee1ae3d36efc1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411914"
---
# <a name="themeindex-cell-theme-properties-section"></a><span data-ttu-id="2d896-104">Celda ThemeIndex (sección Propiedades de tema)</span><span class="sxs-lookup"><span data-stu-id="2d896-104">ThemeIndex Cell (Theme Properties Section)</span></span>

<span data-ttu-id="2d896-105">Almacena la enumeración del tema integrado de Microsoft Visio que se ha aplicado al documento como un entero.</span><span class="sxs-lookup"><span data-stu-id="2d896-105">Stores the enumeration of the built-in Microsoft Visio theme applied to the document, as an integer.</span></span> <span data-ttu-id="2d896-106">Cuando se elige un nuevo tema para el documento, la celda **ThemeIndex** del documento y todas las páginas y formas que contiene se actualiza con el índice del tema integrado.</span><span class="sxs-lookup"><span data-stu-id="2d896-106">When a new theme is chosen for the document, the **ThemeIndex** cell for the document and all pages and shapes it contains is updated with the index of the built-in theme.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2d896-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2d896-107">Remarks</span></span>

<span data-ttu-id="2d896-108">Para obtener una referencia a la celda **ThemeIndex** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="2d896-108">To get a reference to the **ThemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2d896-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="2d896-109">Cell name:</span></span>  <br/> | <span data-ttu-id="2d896-110">ThemeIndex</span><span class="sxs-lookup"><span data-stu-id="2d896-110">ThemeIndex</span></span>  <br/> |
   
<span data-ttu-id="2d896-111">Para obtener una referencia desde un programa a la celda **ThemeIndex** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="2d896-111">To get a reference to the **ThemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2d896-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="2d896-112">Section index:</span></span>  <br/> |<span data-ttu-id="2d896-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2d896-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2d896-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="2d896-114">Row index:</span></span>  <br/> |<span data-ttu-id="2d896-115">**visRowThemeProperties**</span><span class="sxs-lookup"><span data-stu-id="2d896-115">**visRowThemeProperties**</span></span> <br/> |
| <span data-ttu-id="2d896-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="2d896-116">Cell index:</span></span>  <br/> |<span data-ttu-id="2d896-117">**visThemeIndex**</span><span class="sxs-lookup"><span data-stu-id="2d896-117">**visThemeIndex**</span></span> <br/> |
   

