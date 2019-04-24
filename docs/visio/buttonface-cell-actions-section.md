---
title: Celda ButtonFace (sección de acciones)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60025
localization_priority: Normal
ms.assetid: cf15b879-a47e-a5a5-bfdd-1d7ea423742f
description: Identifica el icono que aparece junto a un elemento en un menú contextual o de etiquetas de acción.
ms.openlocfilehash: 7ee9c4e7e857acb34ce75429aa0aaf679320b0e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337551"
---
# <a name="buttonface-cell-actions-section"></a><span data-ttu-id="571a6-103">Celda ButtonFace (sección de acciones)</span><span class="sxs-lookup"><span data-stu-id="571a6-103">ButtonFace Cell (Actions Section)</span></span>

<span data-ttu-id="571a6-104">Identifica el icono que aparece junto a un elemento en un menú contextual o de etiquetas de acción.</span><span class="sxs-lookup"><span data-stu-id="571a6-104">Identifies the icon that appears next to an item on a shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="571a6-105">En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="571a6-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="571a6-106">Comentarios</span><span class="sxs-lookup"><span data-stu-id="571a6-106">Remarks</span></span>

<span data-ttu-id="571a6-p101">La cadena de la celda ButtonFace representa el identificador de una imagen de botón de Microsoft Office. Si el valor es cero (0) o si no hay ningún valor, no aparecerá ningún icono.</span><span class="sxs-lookup"><span data-stu-id="571a6-p101">The string contained in the ButtonFace cell represents the ID of a Microsoft Office button face image. A value of zero (0) or blank means no icon appears.</span></span> 
  
<span data-ttu-id="571a6-109">Los Id. que se pueden utilizar en la celda ButtonFace son los mismos que los utilizados con la propiedad **FaceID** de un objeto **CommandBarButton**.</span><span class="sxs-lookup"><span data-stu-id="571a6-109">The IDs that can be used in the ButtonFace cell are the same as the IDs used with the **FaceID** property of a **CommandBarButton** object.</span></span> <span data-ttu-id="571a6-110">Para obtener más información sobre estos identificadores, busque "trabajar con imágenes de botones de la barra de comandos" en MSDN.</span><span class="sxs-lookup"><span data-stu-id="571a6-110">For more details about these IDs, search for "working with command bar button images" on MSDN.</span></span> 
  
<span data-ttu-id="571a6-111">Para obtener una referencia a la celda ButtonFace por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="571a6-111">To get a reference to the ButtonFace cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="571a6-112">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="571a6-112">Cell name:</span></span>  <br/> |<span data-ttu-id="571a6-113">**Acciones**.</span><span class="sxs-lookup"><span data-stu-id="571a6-113">**Actions**.</span></span>  <span data-ttu-id="571a6-114">*nombre* .</span><span class="sxs-lookup"><span data-stu-id="571a6-114">*name*  .</span></span> <span data-ttu-id="571a6-115">**ButtonFace** donde **acciones**.</span><span class="sxs-lookup"><span data-stu-id="571a6-115">**ButtonFace**         where **Actions**.</span></span>  <span data-ttu-id="571a6-116">*nombre* es el nombre de la fila de acciones.</span><span class="sxs-lookup"><span data-stu-id="571a6-116">*name*  is the name of the actions row</span></span>  <br/> |
   
<span data-ttu-id="571a6-117">Para obtener una referencia desde un programa a la celda ButtonFace por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="571a6-117">To get a reference to the ButtonFace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="571a6-118">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="571a6-118">Section index:</span></span>  <br/> |<span data-ttu-id="571a6-119">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="571a6-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="571a6-120">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="571a6-120">Row index:</span></span>  <br/> |<span data-ttu-id="571a6-121">**visRowAction** +  *i* donde **i** = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="571a6-121">**visRowAction** +  *i*           where **i** = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="571a6-122">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="571a6-122">Cell index:</span></span>  <br/> |<span data-ttu-id="571a6-123">**visActionButtonFace**</span><span class="sxs-lookup"><span data-stu-id="571a6-123">**visActionButtonFace**</span></span> <br/> |
   

