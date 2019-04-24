---
title: Celda ButtonFace (sección de etiquetas de acción)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60026
localization_priority: Normal
ms.assetid: 26f370e1-5193-f47d-7b60-3597975be650
description: Contiene el id. de la imagen de botón que aparece en el botón de etiqueta de acción.
ms.openlocfilehash: e74b3281d894cebd8491112181198d427f0d337f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337544"
---
# <a name="buttonface-cell-action-tags-section"></a><span data-ttu-id="af2d7-103">Celda ButtonFace (sección de etiquetas de acción)</span><span class="sxs-lookup"><span data-stu-id="af2d7-103">ButtonFace Cell (Action Tags Section)</span></span>

<span data-ttu-id="af2d7-104">Contiene el id. de la imagen de botón que aparece en el botón de etiqueta de acción.</span><span class="sxs-lookup"><span data-stu-id="af2d7-104">Contains the ID of the button face image that appears on the action tag button.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="af2d7-105">En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="af2d7-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="af2d7-106">Comentarios</span><span class="sxs-lookup"><span data-stu-id="af2d7-106">Remarks</span></span>

<span data-ttu-id="af2d7-107">La cadena de la celda ButtonFace representa el id. de una imagen de botón de Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="af2d7-107">The string contained in the ButtonFace cell represents the ID of a Microsoft Office button face image.</span></span> <span data-ttu-id="af2d7-108">El valor predeterminado es 0 (cero) o en blanco para el botón de información "i" de la etiqueta de acción estándar</span><span class="sxs-lookup"><span data-stu-id="af2d7-108">A value of 0 (zero) or blank defaults to the standard action tag "i" info button</span></span> ![Botón de información "i" de la etiqueta de acción estándar](media/InfoPS_ZA10180114.gif)<span data-ttu-id="af2d7-110">.</span><span class="sxs-lookup"><span data-stu-id="af2d7-110"></span></span>
  
<span data-ttu-id="af2d7-111">Los Id. que se pueden utilizar en la celda ButtonFace son los mismos que los utilizados con la propiedad **FaceID** de un objeto **CommandBarButton**.</span><span class="sxs-lookup"><span data-stu-id="af2d7-111">The IDs that can be used in the ButtonFace cell are the same as the IDs used with the **FaceID** property of a **CommandBarButton** object.</span></span> <span data-ttu-id="af2d7-112">Para obtener más información sobre estos identificadores, busque "trabajar con imágenes de botones de la barra de comandos" en MSDN.</span><span class="sxs-lookup"><span data-stu-id="af2d7-112">For more details about these IDs, search for "working with command bar button images" on MSDN.</span></span> 
  
<span data-ttu-id="af2d7-113">Para obtener una referencia a la celda ButtonFace por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="af2d7-113">To get a reference to the ButtonFace cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="af2d7-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="af2d7-114">Cell name:</span></span>  <br/> | <span data-ttu-id="af2d7-115">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="af2d7-115">SmartTags.</span></span>  <span data-ttu-id="af2d7-116">*nombre* . ButtonFace donde SmartTags.</span><span class="sxs-lookup"><span data-stu-id="af2d7-116">*name*  .ButtonFace           where SmartTags.</span></span> <span data-ttu-id="af2d7-117">*nombre* es el nombre de la fila de la etiqueta de acción.</span><span class="sxs-lookup"><span data-stu-id="af2d7-117">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="af2d7-118">Para obtener una referencia desde un programa a la celda ButtonFace por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="af2d7-118">To get a reference to the ButtonFace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="af2d7-119">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="af2d7-119">Section index:</span></span>  <br/> |<span data-ttu-id="af2d7-120">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="af2d7-120">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="af2d7-121">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="af2d7-121">Row index:</span></span>  <br/> |<span data-ttu-id="af2d7-122">**visRowSmartTag** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="af2d7-122">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="af2d7-123">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="af2d7-123">Cell index:</span></span>  <br/> |<span data-ttu-id="af2d7-124">**visSmartTagButtonFace**</span><span class="sxs-lookup"><span data-stu-id="af2d7-124">**visSmartTagButtonFace**</span></span> <br/> |
   

