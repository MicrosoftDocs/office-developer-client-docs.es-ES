---
title: Celda SubAddress (Sección de hipervínculos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm985
localization_priority: Normal
ms.assetid: 949448fd-0f85-b56a-945e-1da0e48609e8
description: Especifica una ubicación del documento de destino con la que se establece el vínculo.
ms.openlocfilehash: 092a53bd7c9d5adb77ed35f3e2ef53888bd6ebea
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395269"
---
# <a name="subaddress-cell-hyperlinks-section"></a><span data-ttu-id="9aa16-103">Celda SubAddress (sección Hipervínculos)</span><span class="sxs-lookup"><span data-stu-id="9aa16-103">SubAddress Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="9aa16-104">Especifica una ubicación del documento de destino con la que se establece el vínculo.</span><span class="sxs-lookup"><span data-stu-id="9aa16-104">Specifies a location within the target document to link to.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9aa16-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9aa16-105">Remarks</span></span>

<span data-ttu-id="9aa16-106">Por ejemplo, si la celda Address es "Drawing1.vsdx", la celda SubAddress puede especificar un nombre de página como "Página 3".</span><span class="sxs-lookup"><span data-stu-id="9aa16-106">For example, if the Address cell is "Drawing1.vsdx", the SubAddress cell can specify a page name such as "Page-3".</span></span> <span data-ttu-id="9aa16-107">Si la celda Address es el archivo de Microsoft Excel "Samples.xlsx", el valor de esta celda puede ser una hoja de cálculo o un intervalo dentro de una hoja de cálculo, como "Funciones de hoja de cálculo" o "Sheet1! A1: D10 ".</span><span class="sxs-lookup"><span data-stu-id="9aa16-107">If the Address cell is the Microsoft Excel file "Samples.xlsx", the value of this cell can be a worksheet or range within a worksheet, such as "Worksheet Functions" or "Sheet1!A1:D10".</span></span> <span data-ttu-id="9aa16-108">Si la celda Address "https://www.microsoft.com/office/", el valor de esta celda puede ser un anclaje con nombre dentro del documento, como "soluciones".</span><span class="sxs-lookup"><span data-stu-id="9aa16-108">If the Address cell is "https://www.microsoft.com/office/", the value of this cell can be a named anchor within the document, such as "solutions".</span></span>
  
<span data-ttu-id="9aa16-109">También puede establecer el valor de esta celda en el cuadro de diálogo \*\* Hipervínculos\*\* (en el grupo **Vínculos** en la ficha **Insertar**, haga clic en **Hipervínculo**).</span><span class="sxs-lookup"><span data-stu-id="9aa16-109">You can also set the value of this cell in the **Hyperlinks** dialog box (in the **Links** group on the **Insert** tab, click **Hyperlink**).</span></span>
  
<span data-ttu-id="9aa16-110">Para obtener una referencia a la celda SubAddress por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="9aa16-110">To get a reference to the SubAddress cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9aa16-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="9aa16-111">Cell name:</span></span>  <br/> | <span data-ttu-id="9aa16-112">Hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="9aa16-112">Hyperlink.</span></span>  <span data-ttu-id="9aa16-113">*nombre* . Subdirección donde hipervínculo *.name* es el nombre de fila</span><span class="sxs-lookup"><span data-stu-id="9aa16-113">*name*  .SubAddress where Hyperlink  *.name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="9aa16-114">Para obtener una referencia a la celda **SubAddress** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="9aa16-114">To get a reference to the **SubAddress** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9aa16-115">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="9aa16-115">Section index:</span></span>  <br/> |<span data-ttu-id="9aa16-116">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="9aa16-116">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="9aa16-117">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="9aa16-117">Row index:</span></span>  <br/> |<span data-ttu-id="9aa16-118">**visRow1stHyperlink** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="9aa16-118">**visRow1stHyperlink** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="9aa16-119">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="9aa16-119">Cell index:</span></span>  <br/> |<span data-ttu-id="9aa16-120">**visHLinkSubAddress**</span><span class="sxs-lookup"><span data-stu-id="9aa16-120">**visHLinkSubAddress**</span></span> <br/> |
   

