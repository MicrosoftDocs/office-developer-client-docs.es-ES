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
ms.openlocfilehash: ca6be0a95b33e173219f4bdc1ba042c7162941b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821692"
---
# <a name="buttonface-cell-action-tags-section"></a><span data-ttu-id="0739a-103">Celda ButtonFace (sección Etiquetas de acción)</span><span class="sxs-lookup"><span data-stu-id="0739a-103">ButtonFace Cell (Action Tags Section)</span></span>

<span data-ttu-id="0739a-104">Contiene el id. de la imagen de botón que aparece en el botón de etiqueta de acción.</span><span class="sxs-lookup"><span data-stu-id="0739a-104">Contains the ID of the button face image that appears on the action tag button.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0739a-105">En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="0739a-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0739a-106">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0739a-106">Remarks</span></span>

<span data-ttu-id="0739a-107">La cadena de la celda ButtonFace representa el identificador de una imagen de botón de Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="0739a-107">The string contained in the ButtonFace cell represents the ID of a Microsoft Office button face image.</span></span> <span data-ttu-id="0739a-108">Un valor de 0 (cero) o en blanco el valor predeterminado es el botón de información "i" de etiquetas de acción estándar ![](media/InfoPS_ZA10180114.gif).</span><span class="sxs-lookup"><span data-stu-id="0739a-108">A value of 0 (zero) or blank defaults to the standard action tag "i" info button ![](media/InfoPS_ZA10180114.gif).</span></span>
  
<span data-ttu-id="0739a-109">Los identificadores que pueden usarse en la celda ButtonFace son los mismos que los identificadores que se utiliza con la propiedad **FaceID** de un objeto **CommandBarButton** .</span><span class="sxs-lookup"><span data-stu-id="0739a-109">The IDs that can be used in the ButtonFace cell are the same as the IDs used with the **FaceID** property of a **CommandBarButton** object.</span></span> <span data-ttu-id="0739a-110">Para obtener más detalles acerca de estos identificadores, busque "trabajar con imágenes de botón de barra de comandos" en MSDN.</span><span class="sxs-lookup"><span data-stu-id="0739a-110">For more details about these IDs, search for "working with command bar button images" on MSDN.</span></span> 
  
<span data-ttu-id="0739a-111">Para obtener una referencia a la celda ButtonFace por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="0739a-111">To get a reference to the ButtonFace cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0739a-112">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="0739a-112">Cell name:</span></span>  <br/> | <span data-ttu-id="0739a-113">Etiquetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="0739a-113">SmartTags.</span></span>  <span data-ttu-id="0739a-114">*nombre* . ButtonFace donde SmartTags.</span><span class="sxs-lookup"><span data-stu-id="0739a-114">*name*  .ButtonFace           where SmartTags.</span></span> <span data-ttu-id="0739a-115">*nombre* es el nombre de la fila de etiquetas de acción</span><span class="sxs-lookup"><span data-stu-id="0739a-115">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="0739a-116">Para obtener una referencia desde un programa a la celda ButtonFace por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="0739a-116">To get a reference to the ButtonFace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0739a-117">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="0739a-117">Section index:</span></span>  <br/> |<span data-ttu-id="0739a-118">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="0739a-118">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="0739a-119">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="0739a-119">Row index:</span></span>  <br/> |<span data-ttu-id="0739a-120">**visRowSmartTag** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="0739a-120">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="0739a-121">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="0739a-121">Cell index:</span></span>  <br/> |<span data-ttu-id="0739a-122">**visSmartTagButtonFace**</span><span class="sxs-lookup"><span data-stu-id="0739a-122">**visSmartTagButtonFace**</span></span> <br/> |
   

