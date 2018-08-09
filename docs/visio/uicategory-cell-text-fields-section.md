---
title: Celda UICategory (Sección de campos de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1070
localization_priority: Normal
ms.assetid: 365f7005-ba34-2311-4c5c-16344962fc3f
description: Determina la categoría de un campo insertado en versiones de Visio anteriores a Visio 2000.
ms.openlocfilehash: fc060ac1533732749d10e1855dc3841602051520
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823476"
---
# <a name="uicategory-cell-text-fields-section"></a><span data-ttu-id="2c873-103">Celda UICategory (sección Campos de texto)</span><span class="sxs-lookup"><span data-stu-id="2c873-103">UICategory Cell (Text Fields Section)</span></span>

<span data-ttu-id="2c873-104">Determina la categoría de un campo insertado en versiones de Visio anteriores a Visio 2000.</span><span class="sxs-lookup"><span data-stu-id="2c873-104">Determines the category of an inserted field in versions of Visio earlier than Visio 2000.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2c873-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2c873-105">Remarks</span></span>

<span data-ttu-id="2c873-p101">Esta celda no aparece en la ventana ShapeSheet. Utilice esta celda si necesita solucionar algún problema de compatibilidad con versiones anteriores, como guardar un dibujo de Visio versión 2000 en el formato de archivo de Visio versión 5.0.</span><span class="sxs-lookup"><span data-stu-id="2c873-p101">This cell does not appear in the ShapeSheet window. Use this cell if you need to deal with backward capability issues such as saving a Visio version 2000 drawing in Visio version 5.0 file format.</span></span>
  
<span data-ttu-id="2c873-108">Para obtener una referencia a la celda UICategory por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="2c873-108">To get a reference to the UICategory cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2c873-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="2c873-109">Cell name:</span></span>  <br/> | <span data-ttu-id="2c873-110">Fields.UICat [ *i* ] donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="2c873-110">Fields.UICat[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="2c873-111">Para obtener una referencia desde un programa a la celda UICategory por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="2c873-111">To get a reference to the UICategory cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2c873-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="2c873-112">Section index:</span></span>  <br/> |<span data-ttu-id="2c873-113">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="2c873-113">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="2c873-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="2c873-114">Row index:</span></span>  <br/> |<span data-ttu-id="2c873-115">**visRowField** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="2c873-115">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="2c873-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="2c873-116">Cell index:</span></span>  <br/> |<span data-ttu-id="2c873-117">**visFieldUICategory**</span><span class="sxs-lookup"><span data-stu-id="2c873-117">**visFieldUICategory**</span></span> <br/> |
   

