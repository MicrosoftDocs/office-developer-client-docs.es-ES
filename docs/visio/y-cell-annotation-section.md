---
title: Celda Y (Sección de anotación)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60095
localization_priority: Normal
ms.assetid: 527a4615-2013-a4b4-81cd-7f5d71c1803c
description: Coordenada y del marcador de comentario en coordenadas de página.
ms.openlocfilehash: 48a37c261078cd1000331920b33549cee2c1da03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429204"
---
# <a name="y-cell-annotation-section"></a><span data-ttu-id="5d1d5-103">Celda Y (Sección de anotación)</span><span class="sxs-lookup"><span data-stu-id="5d1d5-103">Y Cell (Annotation Section)</span></span>

<span data-ttu-id="5d1d5-104">*Coordenada y* del marcador de comentario en coordenadas de página.</span><span class="sxs-lookup"><span data-stu-id="5d1d5-104">The  *y*  -coordinate of the comment marker in page coordinates.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5d1d5-105">Esta celda se usa para realizar el seguimiento de comentarios solo al abrir un archivo .vsd en Microsoft Visio 2013 o al guardar un archivo .vsdx en el formato de archivo .vsd.</span><span class="sxs-lookup"><span data-stu-id="5d1d5-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="5d1d5-106">No se usa para realizar el seguimiento de comentarios en documentos .vsdx en Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="5d1d5-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5d1d5-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5d1d5-107">Remarks</span></span>

<span data-ttu-id="5d1d5-108">Para obtener una referencia desde un programa a la celda Y por su índice, utilice la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="5d1d5-108">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5d1d5-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="5d1d5-109">Cell name:</span></span>  <br/> | <span data-ttu-id="5d1d5-110">Annotation.Y [  *i*  ] donde  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="5d1d5-110">Annotation.Y [  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="5d1d5-111">Para obtener una referencia desde un programa a la celda Y por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="5d1d5-111">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5d1d5-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="5d1d5-112">Section index:</span></span>  <br/> |<span data-ttu-id="5d1d5-113">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="5d1d5-113">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="5d1d5-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="5d1d5-114">Row index:</span></span>  <br/> |<span data-ttu-id="5d1d5-115">**visRowAnnotation**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="5d1d5-115">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="5d1d5-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="5d1d5-116">Cell index:</span></span>  <br/> |<span data-ttu-id="5d1d5-117">**visAnnotationY**</span><span class="sxs-lookup"><span data-stu-id="5d1d5-117">**visAnnotationY**</span></span> <br/> |
   

