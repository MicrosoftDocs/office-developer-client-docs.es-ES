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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408449"
---
# <a name="paperkind-cell-print-properties-section"></a><span data-ttu-id="71e5c-103">Celda PaperKind (sección de propiedades de impresión)</span><span class="sxs-lookup"><span data-stu-id="71e5c-103">PaperKind Cell (Print Properties Section)</span></span>

<span data-ttu-id="71e5c-104">Especifica el tipo de papel donde imprimir la página.</span><span class="sxs-lookup"><span data-stu-id="71e5c-104">Specifies the type of paper on which to print the page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="71e5c-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="71e5c-105">Remarks</span></span>

<span data-ttu-id="71e5c-106">Esta configuración corresponde  a la configuración  tamaño de papel en el cuadro  de diálogo Configurar impresión  (en la ficha Diseño, haga clic en la flecha de configuración de página y, a continuación, en la ficha Configurar impresión, haga clic en el botón **Configurar).** </span><span class="sxs-lookup"><span data-stu-id="71e5c-106">This setting corresponds to the **Paper Size** setting in the **Print Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then on the **Print Setup** tab, click the **Setup** button).</span></span> 
  
<span data-ttu-id="71e5c-107">Los valores numéricos de esta celda se asignan a constantes (con el prefijo DMPAPER) definidas para las selecciones de papel en el archivo wingdi.h de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="71e5c-107">The numeric values in this cell map to constants (prefixed with DMPAPER) defined for paper selections in the Microsoft Windows wingdi.h file.</span></span> 
  
<span data-ttu-id="71e5c-108">Para obtener una referencia a la celda PaperKind por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="71e5c-108">To get a reference to the PaperKind cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="71e5c-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="71e5c-109">Cell name:</span></span>  <br/> |<span data-ttu-id="71e5c-110">PaperKind</span><span class="sxs-lookup"><span data-stu-id="71e5c-110">PaperKind</span></span>  <br/> |
   
<span data-ttu-id="71e5c-111">Para obtener una referencia desde un programa a la celda PaperKind por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="71e5c-111">To get a reference to the PaperKind cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="71e5c-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="71e5c-112">Section index:</span></span>  <br/> |<span data-ttu-id="71e5c-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="71e5c-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="71e5c-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="71e5c-114">Row index:</span></span>  <br/> |<span data-ttu-id="71e5c-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="71e5c-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="71e5c-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="71e5c-116">Cell index:</span></span>  <br/> |<span data-ttu-id="71e5c-117">**visPrintPropertiesPaperKind**</span><span class="sxs-lookup"><span data-stu-id="71e5c-117">**visPrintPropertiesPaperKind**</span></span> <br/> |
   

