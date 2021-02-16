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
ms.openlocfilehash: 293451b61def59ccfdf849dc597def9521fd22e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422218"
---
# <a name="uicode-cell-text-fields-section"></a><span data-ttu-id="d46b5-103">Celda UICode (Sección de campos de texto)</span><span class="sxs-lookup"><span data-stu-id="d46b5-103">UICode Cell (Text Fields Section)</span></span>

<span data-ttu-id="d46b5-104">Determina el código de un campo insertado en versiones de Visio anteriores a Visio 2000.</span><span class="sxs-lookup"><span data-stu-id="d46b5-104">Determines the code of an inserted field in versions of Visio earlier than Visio 2000.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d46b5-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d46b5-105">Remarks</span></span>

<span data-ttu-id="d46b5-p101">Esta celda no aparece en la ventana ShapeSheet. Utilice esta celda si necesita solucionar algún problema de compatibilidad con versiones anteriores, como guardar un dibujo de Visio versión 2000 en el formato de archivo de Visio versión 5.0.</span><span class="sxs-lookup"><span data-stu-id="d46b5-p101">This cell does not appear in the ShapeSheet window. Use this cell if you need to deal with backward capability issues, such as saving a Visio version 2000 drawing in Visio version 5.0 file format.</span></span>
  
<span data-ttu-id="d46b5-108">Para obtener una referencia a la celda UICode por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="d46b5-108">To get a reference to the UICode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d46b5-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="d46b5-109">Cell name:</span></span>  <br/> | <span data-ttu-id="d46b5-110">Fields.UICod[  *i*  ] donde  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d46b5-110">Fields.UICod[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d46b5-111">Para obtener una referencia desde un programa a la celda UICode por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="d46b5-111">To get a reference to the UICode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d46b5-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="d46b5-112">Section index:</span></span>  <br/> |<span data-ttu-id="d46b5-113">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="d46b5-113">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="d46b5-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="d46b5-114">Row index:</span></span>  <br/> |<span data-ttu-id="d46b5-115">**visRowField**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d46b5-115">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d46b5-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="d46b5-116">Cell index:</span></span>  <br/> |<span data-ttu-id="d46b5-117">**visFieldUICode**</span><span class="sxs-lookup"><span data-stu-id="d46b5-117">**visFieldUICode**</span></span> <br/> |
   

