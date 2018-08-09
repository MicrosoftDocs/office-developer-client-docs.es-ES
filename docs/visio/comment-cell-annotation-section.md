---
title: Celda Comment (Sección de anotaciones)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60033
localization_priority: Normal
ms.assetid: b367841a-f31c-4b55-4491-2abab5811dbe
description: Contiene el texto que aparece en un comentario.
ms.openlocfilehash: 443a229058a9ca910ba5b38b093706c9c2e3e95b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821782"
---
# <a name="comment-cell-annotation-section"></a><span data-ttu-id="b6332-103">Celda Comment (sección Anotación)</span><span class="sxs-lookup"><span data-stu-id="b6332-103">Comment Cell (Annotation Section)</span></span>

<span data-ttu-id="b6332-104">Contiene el texto que aparece en un comentario.</span><span class="sxs-lookup"><span data-stu-id="b6332-104">Contains the text that appears in a comment.</span></span>
  
> [!NOTE]
> <span data-ttu-id="b6332-105">Esta celda se utiliza para realizar un seguimiento de los comentarios sólo cuando se abre un archivo .vsd en Microsoft Visio 2013 o al guardar un archivo .vsdx en el formato de archivo .vsd.</span><span class="sxs-lookup"><span data-stu-id="b6332-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="b6332-106">No se usa para realizar un seguimiento de los comentarios de documentos .vsdx en Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="b6332-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b6332-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b6332-107">Remarks</span></span>

<span data-ttu-id="b6332-108">Para obtener una referencia a la celda Comment por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="b6332-108">To get a reference to the Comment cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b6332-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="b6332-109">Cell name:</span></span>  <br/> | <span data-ttu-id="b6332-110">Annotation.Comment [ *i* ] donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="b6332-110">Annotation.Comment[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="b6332-111">Para obtener una referencia desde un programa a la celda Comment por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="b6332-111">To get a reference to the Comment cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b6332-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="b6332-112">Section index:</span></span>  <br/> |<span data-ttu-id="b6332-113">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="b6332-113">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="b6332-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="b6332-114">Row index:</span></span>  <br/> |<span data-ttu-id="b6332-115">**visRowAnnotation** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b6332-115">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b6332-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="b6332-116">Cell index:</span></span>  <br/> |<span data-ttu-id="b6332-117">**visAnnotationComment**</span><span class="sxs-lookup"><span data-stu-id="b6332-117">**visAnnotationComment**</span></span> <br/> |
   

