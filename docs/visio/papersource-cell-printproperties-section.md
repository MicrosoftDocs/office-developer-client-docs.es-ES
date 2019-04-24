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
ms.openlocfilehash: eb6e7daccb1743c43a30b34598e47187496e4aac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301466"
---
# <a name="papersource-cell-printproperties-section"></a><span data-ttu-id="cf928-103">Celda PaperSource (Sección de propiedades de impresión)</span><span class="sxs-lookup"><span data-stu-id="cf928-103">PaperSource Cell (PrintProperties Section)</span></span>

<span data-ttu-id="cf928-104">Determina el origen del papel para la página.</span><span class="sxs-lookup"><span data-stu-id="cf928-104">Determines the paper source for the page.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cf928-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cf928-105">Remarks</span></span>

<span data-ttu-id="cf928-106">Esta opción corresponde a la opción **Origen del papel** del cuadro de diálogo **Configurar impresión** (en el menú **Archivo**, haga clic en la flecha de **Configurar página** y, a continuación, en la ficha **Configurar impresión**, haga clic en el botón **Configurar**).</span><span class="sxs-lookup"><span data-stu-id="cf928-106">This setting corresponds to the **Paper Source** setting in the **Print Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then on the **Print Setup** tab, click **Setup**).</span></span>
  
<span data-ttu-id="cf928-107">Los valores numéricos de esta celda se asignan a constantes (con el prefijo DMBIN) definidas para las selecciones de bin en el archivo WinGDI. h de Microsoft Windows; por ejemplo, el valor 7 representa DMBIN_AUTO.</span><span class="sxs-lookup"><span data-stu-id="cf928-107">The numeric values in this cell map to constants (prefixed with DMBIN) defined for bin selections in the Microsoft Windows wingdi.h file; for example, the value 7 represents DMBIN_AUTO.</span></span> 
  
<span data-ttu-id="cf928-108">Para obtener una referencia a la celda PaperSource por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="cf928-108">To get a reference to the PaperSource cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cf928-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="cf928-109">Cell name:</span></span>  <br/> |<span data-ttu-id="cf928-110">PaperSource</span><span class="sxs-lookup"><span data-stu-id="cf928-110">PaperSource</span></span>  <br/> |
   
<span data-ttu-id="cf928-111">Para obtener una referencia desde un programa a la celda PaperSource por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="cf928-111">To get a reference to the PaperSource cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cf928-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="cf928-112">Section index:</span></span>  <br/> |<span data-ttu-id="cf928-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cf928-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="cf928-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="cf928-114">Row index:</span></span>  <br/> |<span data-ttu-id="cf928-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="cf928-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="cf928-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="cf928-116">Cell index:</span></span>  <br/> |<span data-ttu-id="cf928-117">**visPrintPropertiesPaperSource**</span><span class="sxs-lookup"><span data-stu-id="cf928-117">**visPrintPropertiesPaperSource**</span></span> <br/> |
   

