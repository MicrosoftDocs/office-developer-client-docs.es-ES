---
title: Celda PaperSource (Sección de propiedades de impresión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60068
localization_priority: Normal
ms.assetid: 771a2ab4-578d-51c3-fabd-138f7952bb11
description: Determina el origen del papel para la página.
ms.openlocfilehash: f1dedf210dfe0dd8cac3d36fdec03fb497f6572c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822724"
---
# <a name="papersource-cell-printproperties-section"></a><span data-ttu-id="15607-103">Celda PaperSource (sección Propiedades de impresión)</span><span class="sxs-lookup"><span data-stu-id="15607-103">PaperSource Cell (PrintProperties Section)</span></span>

<span data-ttu-id="15607-104">Determina el origen del papel para la página.</span><span class="sxs-lookup"><span data-stu-id="15607-104">Determines the paper source for the page.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="15607-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="15607-105">Remarks</span></span>

<span data-ttu-id="15607-106">Esta opción corresponde a la opción **Origen del papel** del cuadro de diálogo **Configurar impresión** (en el menú **Archivo**, haga clic en la flecha de **Configurar página** y, a continuación, en la ficha **Configurar impresión**, haga clic en el botón **Configurar**).</span><span class="sxs-lookup"><span data-stu-id="15607-106">This setting corresponds to the **Paper Source** setting in the **Print Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then on the **Print Setup** tab, click **Setup**).</span></span>
  
<span data-ttu-id="15607-107">Los valores numéricos de esta celda están asignados a constantes (prefijadas por DMBIN) definidos para selecciones en el archivo wingdi.h de Microsoft Windows; Por ejemplo, el valor 7 representa a DMBIN_AUTO.</span><span class="sxs-lookup"><span data-stu-id="15607-107">The numeric values in this cell map to constants (prefixed with DMBIN) defined for bin selections in the Microsoft Windows wingdi.h file; for example, the value 7 represents DMBIN_AUTO.</span></span> 
  
<span data-ttu-id="15607-108">Para obtener una referencia a la celda PaperSource por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="15607-108">To get a reference to the PaperSource cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="15607-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="15607-109">Cell name:</span></span>  <br/> |<span data-ttu-id="15607-110">PaperSource</span><span class="sxs-lookup"><span data-stu-id="15607-110">PaperSource</span></span>  <br/> |
   
<span data-ttu-id="15607-111">Para obtener una referencia desde un programa a la celda PaperSource por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="15607-111">To get a reference to the PaperSource cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="15607-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="15607-112">Section index:</span></span>  <br/> |<span data-ttu-id="15607-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="15607-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="15607-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="15607-114">Row index:</span></span>  <br/> |<span data-ttu-id="15607-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="15607-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="15607-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="15607-116">Cell index:</span></span>  <br/> |<span data-ttu-id="15607-117">**visPrintPropertiesPaperSource**</span><span class="sxs-lookup"><span data-stu-id="15607-117">**visPrintPropertiesPaperSource**</span></span> <br/> |
   

