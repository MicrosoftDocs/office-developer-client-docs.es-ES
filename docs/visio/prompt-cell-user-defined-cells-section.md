---
title: Celda Prompt (Sección de celdas definidas por el usuario)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm840
localization_priority: Normal
ms.assetid: d0f91e7d-2373-cfef-e105-fb17e77c7f2d
description: Especifica un mensaje o comentario descriptivo para la celda definida por el usuario. La aplicación encierra automáticamente el texto del mensaje entre comillas () para indicar que se trata de una cadena de texto. Si escribe un signo igual (=) y omite las comillas, puede escribir una fórmula en esta celda que evalúe la aplicación.
ms.openlocfilehash: 7684025e03bd3f4f68893179b1df00cc0cb535e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435729"
---
# <a name="prompt-cell-user-defined-cells-section"></a><span data-ttu-id="b46e8-105">Celda Prompt (Sección de celdas definidas por el usuario)</span><span class="sxs-lookup"><span data-stu-id="b46e8-105">Prompt Cell (User-Defined Cells Section)</span></span>

<span data-ttu-id="b46e8-p102">Especifica un mensaje o comentario descriptivo para la celda definida por el usuario. La aplicación pone automáticamente el texto del mensaje entre comillas (" ") para indicar que se trata de una cadena de texto. Si escribe un signo de igual (=) y omite las comillas, podrá escribir una fórmula en esta celda que evaluará la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b46e8-p102">Specifies a descriptive prompt or comment for the user-defined cell. The application automatically encloses the prompt text in quotation marks (" ") to indicate that it is a text string. If you type an equal sign (=) and omit the quotation marks, you can enter a formula in this cell that the application evaluates.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b46e8-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b46e8-109">Remarks</span></span>

<span data-ttu-id="b46e8-110">Para obtener una referencia a la celda Prompt por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="b46e8-110">To get a reference to the Prompt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b46e8-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="b46e8-111">Cell name:</span></span>  <br/> | <span data-ttu-id="b46e8-112">Usuario.</span><span class="sxs-lookup"><span data-stu-id="b46e8-112">User.</span></span>  <span data-ttu-id="b46e8-113">*Nombre* . Pregunta en la que el usuario.</span><span class="sxs-lookup"><span data-stu-id="b46e8-113">*Name*  .Prompt            where User.</span></span>  <span data-ttu-id="b46e8-114">*Name* es el nombre de la fila</span><span class="sxs-lookup"><span data-stu-id="b46e8-114">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="b46e8-115">Para obtener una referencia desde un programa a la celda Prompt por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="b46e8-115">To get a reference to the Prompt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b46e8-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="b46e8-116">Section index:</span></span>  <br/> |<span data-ttu-id="b46e8-117">**visSectionUser**</span><span class="sxs-lookup"><span data-stu-id="b46e8-117">**visSectionUser**</span></span> <br/> |
| <span data-ttu-id="b46e8-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="b46e8-118">Row index:</span></span>  <br/> |<span data-ttu-id="b46e8-119">**visRowUser +** *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b46e8-119">**visRowUser +** *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b46e8-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="b46e8-120">Cell index:</span></span>  <br/> |<span data-ttu-id="b46e8-121">**visUserPrompt**</span><span class="sxs-lookup"><span data-stu-id="b46e8-121">**visUserPrompt**</span></span> <br/> |
   

