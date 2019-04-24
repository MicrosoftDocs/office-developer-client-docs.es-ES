---
title: Celda PaperKind (Sección de propiedades de impresión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60067
localization_priority: Normal
ms.assetid: b2c9616f-a144-eb99-54b6-b53745c7b4d6
description: Especifica el tipo de papel donde imprimir la página.
ms.openlocfilehash: 694aa1fb8b52f5ae323c47e9aab8715b4a48dfb0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327065"
---
# <a name="paperkind-cell-print-properties-section"></a><span data-ttu-id="d6878-103">Celda PaperKind (sección de propiedades de impresión)</span><span class="sxs-lookup"><span data-stu-id="d6878-103">PaperKind Cell (Print Properties Section)</span></span>

<span data-ttu-id="d6878-104">Especifica el tipo de papel donde imprimir la página.</span><span class="sxs-lookup"><span data-stu-id="d6878-104">Specifies the type of paper on which to print the page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d6878-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d6878-105">Remarks</span></span>

<span data-ttu-id="d6878-106">Esta opción corresponde a la configuración del **tamaño del papel** en el cuadro de diálogo **Configurar impresión** (en la ficha **diseño** , haga clic en la flecha de **Configurar página** y, a continuación, en la ficha **Configurar impresión** , haga clic en el botón **configurar** ).</span><span class="sxs-lookup"><span data-stu-id="d6878-106">This setting corresponds to the **Paper Size** setting in the **Print Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then on the **Print Setup** tab, click the **Setup** button).</span></span> 
  
<span data-ttu-id="d6878-107">Los valores numéricos de esta celda se asignan a constantes (con el prefijo DMPAPER) definidas para las selecciones de papel en el archivo WinGDI. h de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d6878-107">The numeric values in this cell map to constants (prefixed with DMPAPER) defined for paper selections in the Microsoft Windows wingdi.h file.</span></span> 
  
<span data-ttu-id="d6878-108">Para obtener una referencia a la celda PaperKind por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="d6878-108">To get a reference to the PaperKind cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d6878-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="d6878-109">Cell name:</span></span>  <br/> |<span data-ttu-id="d6878-110">PaperKind</span><span class="sxs-lookup"><span data-stu-id="d6878-110">PaperKind</span></span>  <br/> |
   
<span data-ttu-id="d6878-111">Para obtener una referencia desde un programa a la celda PaperKind por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="d6878-111">To get a reference to the PaperKind cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d6878-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="d6878-112">Section index:</span></span>  <br/> |<span data-ttu-id="d6878-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d6878-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="d6878-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="d6878-114">Row index:</span></span>  <br/> |<span data-ttu-id="d6878-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="d6878-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="d6878-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="d6878-116">Cell index:</span></span>  <br/> |<span data-ttu-id="d6878-117">**visPrintPropertiesPaperKind**</span><span class="sxs-lookup"><span data-stu-id="d6878-117">**visPrintPropertiesPaperKind**</span></span> <br/> |
   

