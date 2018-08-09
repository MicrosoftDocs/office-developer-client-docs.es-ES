---
title: Celda UICode (Sección de campos de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1075
localization_priority: Normal
ms.assetid: 1d9717c1-4310-0d62-874f-4df77cd81627
description: Determina el código de un campo insertado en versiones de Visio anteriores a Visio 2000.
ms.openlocfilehash: ce05f779bfebd5720555f1a2d92b1f9f92cfbdfd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823471"
---
# <a name="uicode-cell-text-fields-section"></a><span data-ttu-id="3df87-103">Celda UICode (sección Campos de texto)</span><span class="sxs-lookup"><span data-stu-id="3df87-103">UICode Cell (Text Fields Section)</span></span>

<span data-ttu-id="3df87-104">Determina el código de un campo insertado en versiones de Visio anteriores a Visio 2000.</span><span class="sxs-lookup"><span data-stu-id="3df87-104">Determines the code of an inserted field in versions of Visio earlier than Visio 2000.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3df87-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3df87-105">Remarks</span></span>

<span data-ttu-id="3df87-p101">Esta celda no aparece en la ventana ShapeSheet. Utilice esta celda si necesita solucionar algún problema de compatibilidad con versiones anteriores, como guardar un dibujo de Visio versión 2000 en el formato de archivo de Visio versión 5.0.</span><span class="sxs-lookup"><span data-stu-id="3df87-p101">This cell does not appear in the ShapeSheet window. Use this cell if you need to deal with backward capability issues, such as saving a Visio version 2000 drawing in Visio version 5.0 file format.</span></span>
  
<span data-ttu-id="3df87-108">Para obtener una referencia a la celda UICode por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="3df87-108">To get a reference to the UICode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3df87-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="3df87-109">Cell name:</span></span>  <br/> | <span data-ttu-id="3df87-110">Fields.UICod [ *i* ] donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="3df87-110">Fields.UICod[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="3df87-111">Para obtener una referencia desde un programa a la celda UICode por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="3df87-111">To get a reference to the UICode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3df87-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="3df87-112">Section index:</span></span>  <br/> |<span data-ttu-id="3df87-113">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="3df87-113">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="3df87-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="3df87-114">Row index:</span></span>  <br/> |<span data-ttu-id="3df87-115">**visRowField** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="3df87-115">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="3df87-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="3df87-116">Cell index:</span></span>  <br/> |<span data-ttu-id="3df87-117">**visFieldUICode**</span><span class="sxs-lookup"><span data-stu-id="3df87-117">**visFieldUICode**</span></span> <br/> |
   

