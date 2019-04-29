---
title: Celda UIFormat (Sección de campos de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1080
localization_priority: Normal
ms.assetid: 0dddef20-c58e-2306-ab8e-6cac8e159f61
description: Determina el formato de un campo insertado en versiones de Visio anteriores a Visio 2000.
ms.openlocfilehash: 16cefc5f45d6b5f0f677e35bd5d0937d48fb2680
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426369"
---
# <a name="uiformat-cell-text-fields-section"></a><span data-ttu-id="a56c7-103">Celda UIFormat (Sección de campos de texto)</span><span class="sxs-lookup"><span data-stu-id="a56c7-103">UIFormat Cell (Text Fields Section)</span></span>

<span data-ttu-id="a56c7-104">Determina el formato de un campo insertado en versiones de Visio anteriores a Visio 2000.</span><span class="sxs-lookup"><span data-stu-id="a56c7-104">Determines the format of an inserted field in versions of Visio earlier than Visio 2000.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a56c7-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a56c7-105">Remarks</span></span>

<span data-ttu-id="a56c7-p101">Esta celda no aparece en la ventana ShapeSheet. Utilice esta celda si necesita solucionar algún problema de compatibilidad con versiones anteriores, como guardar un dibujo de Visio versión 2000 en el formato de archivo de Visio versión 5.0.</span><span class="sxs-lookup"><span data-stu-id="a56c7-p101">This cell does not appear in the ShapeSheet window. Use this cell if you need to deal with backward capability issues, such as saving a Visio version 2000 drawing in Visio version 5.0 file format.</span></span>
  
<span data-ttu-id="a56c7-108">Para obtener una referencia a la celda UIFormat por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="a56c7-108">To get a reference to the UIFormat cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a56c7-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="a56c7-109">Cell name:</span></span>  <br/> | <span data-ttu-id="a56c7-110">Fields. UIFmt [ *i* ] donde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="a56c7-110">Fields.UIFmt[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="a56c7-111">Para obtener una referencia desde un programa a la celda UIFormat por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="a56c7-111">To get a reference to the UIFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a56c7-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="a56c7-112">Section index:</span></span>  <br/> |<span data-ttu-id="a56c7-113">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="a56c7-113">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="a56c7-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="a56c7-114">Row index:</span></span>  <br/> |<span data-ttu-id="a56c7-115">**visRowField** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a56c7-115">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="a56c7-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="a56c7-116">Cell index:</span></span>  <br/> |<span data-ttu-id="a56c7-117">**visFieldUIFormat**</span><span class="sxs-lookup"><span data-stu-id="a56c7-117">**visFieldUIFormat**</span></span> <br/> |
   

