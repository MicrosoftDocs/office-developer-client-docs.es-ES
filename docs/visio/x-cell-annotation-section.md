---
title: Celda X (Sección de anotación)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1028735
localization_priority: Normal
ms.assetid: f9db8623-9fcf-7037-2d11-d509f463025d
description: Coordenada x del marcador de comentario en las coordenadas de la página.
ms.openlocfilehash: fdd9e2850a3285a2fcf4cc05fa056accd71052a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341311"
---
# <a name="x-cell-annotation-section"></a><span data-ttu-id="9f338-103">Celda X (Sección de anotación)</span><span class="sxs-lookup"><span data-stu-id="9f338-103">X Cell (Annotation Section)</span></span>

<span data-ttu-id="9f338-104">Coordenada *x* del marcador de comentario en las coordenadas de la página.</span><span class="sxs-lookup"><span data-stu-id="9f338-104">The  *x*  -coordinate of the comment marker in page coordinates.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9f338-105">Esta celda se utiliza para realizar un seguimiento de los comentarios sólo cuando se abre un archivo. VSD en Microsoft Visio 2013 o cuando se guarda un archivo. vsdx en el formato de archivo. VSD.</span><span class="sxs-lookup"><span data-stu-id="9f338-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="9f338-106">No se usa para el seguimiento de comentarios en documentos. vsdx en Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="9f338-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9f338-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9f338-107">Remarks</span></span>

<span data-ttu-id="9f338-108">Para obtener una referencia a la celda X por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="9f338-108">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9f338-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="9f338-109">Cell name:</span></span>  <br/> | <span data-ttu-id="9f338-110">Annotation. X [ *i* ] donde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="9f338-110">Annotation.X[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="9f338-111">Para obtener una referencia desde un programa a la celda X por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="9f338-111">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9f338-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="9f338-112">Section index:</span></span>  <br/> |<span data-ttu-id="9f338-113">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="9f338-113">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="9f338-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="9f338-114">Row index:</span></span>  <br/> |<span data-ttu-id="9f338-115">**visRowAnnotation** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="9f338-115">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="9f338-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="9f338-116">Cell index:</span></span>  <br/> |<span data-ttu-id="9f338-117">**visAnnotationX**</span><span class="sxs-lookup"><span data-stu-id="9f338-117">**visAnnotationX**</span></span> <br/> |
   

