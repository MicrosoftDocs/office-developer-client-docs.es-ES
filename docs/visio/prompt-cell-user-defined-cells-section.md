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
description: Especifica un mensaje o comentario descriptivo para la celda definida por el usuario. La aplicación encierra automáticamente el texto del mensaje entre comillas () para indicar que es una cadena de texto. Si escribe un signo igual (=) y omite las comillas, puede escribir una fórmula en esta celda que da como resultado de la aplicación.
ms.openlocfilehash: a7f8757af3e324a89f49bf5d19185b7a22173ff5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822880"
---
# <a name="prompt-cell-user-defined-cells-section"></a><span data-ttu-id="2e196-105">Celda Prompt (sección Celdas definidas por el usuario)</span><span class="sxs-lookup"><span data-stu-id="2e196-105">Prompt Cell (User-Defined Cells Section)</span></span>

<span data-ttu-id="2e196-p102">Especifica un mensaje o comentario descriptivo para la celda definida por el usuario. La aplicación pone automáticamente el texto del mensaje entre comillas (" ") para indicar que se trata de una cadena de texto. Si escribe un signo de igual (=) y omite las comillas, podrá escribir una fórmula en esta celda que evaluará la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2e196-p102">Specifies a descriptive prompt or comment for the user-defined cell. The application automatically encloses the prompt text in quotation marks (" ") to indicate that it is a text string. If you type an equal sign (=) and omit the quotation marks, you can enter a formula in this cell that the application evaluates.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2e196-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2e196-109">Remarks</span></span>

<span data-ttu-id="2e196-110">Para obtener una referencia a la celda Prompt por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="2e196-110">To get a reference to the Prompt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2e196-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="2e196-111">Cell name:</span></span>  <br/> | <span data-ttu-id="2e196-112">Usuario.</span><span class="sxs-lookup"><span data-stu-id="2e196-112">User.</span></span>  <span data-ttu-id="2e196-113">*Nombre* . Where Prompt usuario.</span><span class="sxs-lookup"><span data-stu-id="2e196-113">*Name*  .Prompt            where User.</span></span>  <span data-ttu-id="2e196-114">*Nombre* es el nombre de fila</span><span class="sxs-lookup"><span data-stu-id="2e196-114">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="2e196-115">Para obtener una referencia desde un programa a la celda Prompt por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="2e196-115">To get a reference to the Prompt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2e196-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="2e196-116">Section index:</span></span>  <br/> |<span data-ttu-id="2e196-117">**visSectionUser**</span><span class="sxs-lookup"><span data-stu-id="2e196-117">**visSectionUser**</span></span> <br/> |
| <span data-ttu-id="2e196-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="2e196-118">Row index:</span></span>  <br/> |<span data-ttu-id="2e196-119">**visRowUser +** *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="2e196-119">**visRowUser +** *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="2e196-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="2e196-120">Cell index:</span></span>  <br/> |<span data-ttu-id="2e196-121">**visUserPrompt**</span><span class="sxs-lookup"><span data-stu-id="2e196-121">**visUserPrompt**</span></span> <br/> |
   

