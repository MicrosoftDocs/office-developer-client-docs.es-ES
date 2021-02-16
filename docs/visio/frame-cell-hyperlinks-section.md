---
title: Celda Frame (Sección de hipervínculos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm405
localization_priority: Normal
ms.assetid: f71d8737-92ef-1124-ba4a-b7e17305bd0a
description: Representa el nombre de un marco de destino cuando la aplicación se abre como documento Active en una aplicación contenedora. El valor predeterminado es una cadena vacía.
ms.openlocfilehash: 8f41e5bf854e31e1f17eabb2aecbded55175ebaf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432859"
---
# <a name="frame-cell-hyperlinks-section"></a><span data-ttu-id="f5012-104">Celda Frame (Sección de hipervínculos)</span><span class="sxs-lookup"><span data-stu-id="f5012-104">Frame Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="f5012-p102">Representa el nombre de un marco de destino cuando la aplicación se abre como documento Active en una aplicación contenedora. El valor predeterminado es una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="f5012-p102">Represents the name of a frame to target when the application is open as an Active document in a container application. The default is an empty string.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f5012-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f5012-107">Remarks</span></span>

<span data-ttu-id="f5012-108">Para obtener una referencia a la celda Frame por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="f5012-108">To get a reference to the Frame cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f5012-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="f5012-109">Cell name:</span></span>  <br/> | <span data-ttu-id="f5012-110">Hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="f5012-110">Hyperlink.</span></span>  <span data-ttu-id="f5012-111">*nombre*  . Marco donde Hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="f5012-111">*name*  .Frame            where Hyperlink.</span></span>  <span data-ttu-id="f5012-112">*nombre*  es el nombre de fila</span><span class="sxs-lookup"><span data-stu-id="f5012-112">*name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="f5012-113">Para obtener una referencia desde un programa a la celda Frame por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="f5012-113">To get a reference to the Frame cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f5012-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="f5012-114">Section index:</span></span>  <br/> |<span data-ttu-id="f5012-115">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="f5012-115">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="f5012-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="f5012-116">Row index:</span></span>  <br/> |<span data-ttu-id="f5012-117">**visRow1stHyperlink**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f5012-117">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="f5012-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="f5012-118">Cell index:</span></span>  <br/> |<span data-ttu-id="f5012-119">**visHLinkFrame**</span><span class="sxs-lookup"><span data-stu-id="f5012-119">**visHLinkFrame**</span></span> <br/> |
   

