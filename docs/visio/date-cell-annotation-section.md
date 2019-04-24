---
title: Celda Date (Sección de anotaciones)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60036
localization_priority: Normal
ms.assetid: f1f11803-614b-a40d-0a2d-131093e7609e
description: Contiene la fecha y la hora de la última vez que se modificó el comentario.
ms.openlocfilehash: 60fd726db1056075f96519050cffa67c76977126
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360343"
---
# <a name="date-cell-annotation-section"></a><span data-ttu-id="6e0f8-103">Celda Date (Sección de anotaciones)</span><span class="sxs-lookup"><span data-stu-id="6e0f8-103">Date Cell (Annotation Section)</span></span>

<span data-ttu-id="6e0f8-104">Contiene la fecha y la hora de la última vez que se modificó el comentario.</span><span class="sxs-lookup"><span data-stu-id="6e0f8-104">Contains the date and time the comment was last edited.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6e0f8-105">Esta celda se utiliza para realizar un seguimiento de los comentarios sólo cuando se abre un archivo. VSD en Microsoft Visio 2013 o cuando se guarda un archivo. vsdx en el formato de archivo. VSD.</span><span class="sxs-lookup"><span data-stu-id="6e0f8-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="6e0f8-106">No se usa para el seguimiento de comentarios en documentos. vsdx en Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="6e0f8-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6e0f8-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6e0f8-107">Remarks</span></span>

<span data-ttu-id="6e0f8-108">Sólo aparece la fecha en el cuadro de comentario de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="6e0f8-108">Only the date appears in the comment box in the user interface.</span></span>
  
<span data-ttu-id="6e0f8-109">Para obtener una referencia a la celda Date por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="6e0f8-109">To get a reference to the Date cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6e0f8-110">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="6e0f8-110">Cell name:</span></span>  <br/> | <span data-ttu-id="6e0f8-111">Annotation. Date [ *i* ] donde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="6e0f8-111">Annotation.Date[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="6e0f8-112">Para obtener una referencia desde un programa a la celda Date por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="6e0f8-112">To get a reference to the Date cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6e0f8-113">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="6e0f8-113">Section index:</span></span>  <br/> |<span data-ttu-id="6e0f8-114">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="6e0f8-114">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="6e0f8-115">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="6e0f8-115">Row index:</span></span>  <br/> |<span data-ttu-id="6e0f8-116">**visRowAnnotation** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="6e0f8-116">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="6e0f8-117">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="6e0f8-117">Cell index:</span></span>  <br/> |<span data-ttu-id="6e0f8-118">**visAnnotationDate**</span><span class="sxs-lookup"><span data-stu-id="6e0f8-118">**visAnnotationDate**</span></span> <br/> |
   

