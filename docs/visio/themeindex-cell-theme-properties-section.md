---
title: Celda ThemeIndex (sección Propiedades de tema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21002267-1400-4398-b937-f5b289cf0ed2
description: Almacena la enumeración del tema de Microsoft Visio integrada aplicado al documento, como un número entero. Cuando se elige un nuevo tema para el documento, la celda ThemeIndex para el documento y todas las páginas y las formas que contiene se actualiza con el índice del tema integrado.
ms.openlocfilehash: 8a9202631bc4d9131d52dea1f852983e1d7528e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823390"
---
# <a name="themeindex-cell-theme-properties-section"></a><span data-ttu-id="fbf3c-104">Celda ThemeIndex (sección Propiedades de tema)</span><span class="sxs-lookup"><span data-stu-id="fbf3c-104">ThemeIndex Cell (Theme Properties Section)</span></span>

<span data-ttu-id="fbf3c-105">Almacena la enumeración del tema de Microsoft Visio integrada aplicado al documento, como un número entero.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-105">Stores the enumeration of the built-in Microsoft Visio theme applied to the document, as an integer.</span></span> <span data-ttu-id="fbf3c-106">Cuando se elige un nuevo tema para el documento, la celda **ThemeIndex** para el documento y todas las páginas y las formas que contiene se actualiza con el índice del tema integrado.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-106">When a new theme is chosen for the document, the **ThemeIndex** cell for the document and all pages and shapes it contains is updated with the index of the built-in theme.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fbf3c-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fbf3c-107">Remarks</span></span>

<span data-ttu-id="fbf3c-108">Para obtener una referencia a la celda **ThemeIndex** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="fbf3c-108">To get a reference to the **ThemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fbf3c-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="fbf3c-109">Cell name:</span></span>  <br/> | <span data-ttu-id="fbf3c-110">ThemeIndex</span><span class="sxs-lookup"><span data-stu-id="fbf3c-110">ThemeIndex</span></span>  <br/> |
   
<span data-ttu-id="fbf3c-111">Para obtener una referencia a la celda **ThemeIndex** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="fbf3c-111">To get a reference to the **ThemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fbf3c-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="fbf3c-112">Section index:</span></span>  <br/> |<span data-ttu-id="fbf3c-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fbf3c-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fbf3c-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="fbf3c-114">Row index:</span></span>  <br/> |<span data-ttu-id="fbf3c-115">**visRowThemeProperties**</span><span class="sxs-lookup"><span data-stu-id="fbf3c-115">**visRowThemeProperties**</span></span> <br/> |
| <span data-ttu-id="fbf3c-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="fbf3c-116">Cell index:</span></span>  <br/> |<span data-ttu-id="fbf3c-117">**visThemeIndex**</span><span class="sxs-lookup"><span data-stu-id="fbf3c-117">**visThemeIndex**</span></span> <br/> |
   

