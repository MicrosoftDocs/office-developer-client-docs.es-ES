---
title: Celda Tip (Sección de controles)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1010
localization_priority: Normal
ms.assetid: 7fd11650-fffa-1316-d302-3122ac5feb14
description: Representa una cadena de texto descriptivo que aparece como información sobre herramientas cuando el usuario deja el puntero sobre el controlador de una forma. La aplicación agrega automáticamente comillas a la cadena de texto en la celda, pero las comillas no aparecen en la información sobre herramientas.
ms.openlocfilehash: ff593ee95dc27ba7192ee31d35791127b666eac0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823418"
---
# <a name="tip-cell-controls-section"></a><span data-ttu-id="d7afa-104">Celda Tip (sección Controles)</span><span class="sxs-lookup"><span data-stu-id="d7afa-104">Tip Cell (Controls Section)</span></span>

<span data-ttu-id="d7afa-p102">Representa una cadena de texto descriptivo que aparece como información sobre herramientas cuando el usuario deja el puntero sobre el controlador de una forma. La aplicación agrega automáticamente comillas a la cadena de texto en la celda, pero las comillas no aparecen en la información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="d7afa-p102">Represents a descriptive text string that appears as a tool tip when a user pauses the pointer over a shape's control handle. The application automatically encloses the tip string in quotation marks in the cell, but the quotation marks are not displayed in the tool tip.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d7afa-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d7afa-107">Remarks</span></span>

<span data-ttu-id="d7afa-108">Para obtener una referencia a la celda Tip por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="d7afa-108">To get a reference to the Tip cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d7afa-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="d7afa-109">Cell name:</span></span>  <br/> | <span data-ttu-id="d7afa-110">Controles.</span><span class="sxs-lookup"><span data-stu-id="d7afa-110">Controls.</span></span>  <span data-ttu-id="d7afa-111">*nombre* . Controles de Tipwhere.</span><span class="sxs-lookup"><span data-stu-id="d7afa-111">*name*  .Tipwhere Controls.</span></span>  <span data-ttu-id="d7afa-112">*nombre* es el nombre de la fila de controles.</span><span class="sxs-lookup"><span data-stu-id="d7afa-112">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="d7afa-113">Para obtener una referencia desde un programa a la celda Tip por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="d7afa-113">To get a reference to the Tip cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d7afa-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="d7afa-114">Section index:</span></span>  <br/> |<span data-ttu-id="d7afa-115">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="d7afa-115">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="d7afa-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="d7afa-116">Row index:</span></span>  <br/> |<span data-ttu-id="d7afa-117">**visRowControl** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d7afa-117">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d7afa-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="d7afa-118">Cell index:</span></span>  <br/> |<span data-ttu-id="d7afa-119">**visCtlTip**</span><span class="sxs-lookup"><span data-stu-id="d7afa-119">**visCtlTip**</span></span> <br/> |
   

