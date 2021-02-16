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
ms.openlocfilehash: b9b0c19aff5e3ab8a4c1e29d319eb42f7ee4a271
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424864"
---
# <a name="tip-cell-controls-section"></a><span data-ttu-id="be537-104">Celda Tip (Sección de controles)</span><span class="sxs-lookup"><span data-stu-id="be537-104">Tip Cell (Controls Section)</span></span>

<span data-ttu-id="be537-p102">Representa una cadena de texto descriptivo que aparece como información sobre herramientas cuando el usuario deja el puntero sobre el controlador de una forma. La aplicación agrega automáticamente comillas a la cadena de texto en la celda, pero las comillas no aparecen en la información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="be537-p102">Represents a descriptive text string that appears as a tool tip when a user pauses the pointer over a shape's control handle. The application automatically encloses the tip string in quotation marks in the cell, but the quotation marks are not displayed in the tool tip.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="be537-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="be537-107">Remarks</span></span>

<span data-ttu-id="be537-108">Para obtener una referencia a la celda Tip por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="be537-108">To get a reference to the Tip cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="be537-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="be537-109">Cell name:</span></span>  <br/> | <span data-ttu-id="be537-110">Controles.</span><span class="sxs-lookup"><span data-stu-id="be537-110">Controls.</span></span>  <span data-ttu-id="be537-111">*nombre*  . Sugerencia en los controles.</span><span class="sxs-lookup"><span data-stu-id="be537-111">*name*  .Tipwhere Controls.</span></span>  <span data-ttu-id="be537-112">*es*  el nombre de la fila de controles.</span><span class="sxs-lookup"><span data-stu-id="be537-112">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="be537-113">Para obtener una referencia desde un programa a la celda Tip por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="be537-113">To get a reference to the Tip cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="be537-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="be537-114">Section index:</span></span>  <br/> |<span data-ttu-id="be537-115">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="be537-115">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="be537-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="be537-116">Row index:</span></span>  <br/> |<span data-ttu-id="be537-117">**visRowControl**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="be537-117">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="be537-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="be537-118">Cell index:</span></span>  <br/> |<span data-ttu-id="be537-119">**visCtlTip**</span><span class="sxs-lookup"><span data-stu-id="be537-119">**visCtlTip**</span></span> <br/> |
   

