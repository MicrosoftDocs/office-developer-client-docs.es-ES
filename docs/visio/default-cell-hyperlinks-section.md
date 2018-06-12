---
title: Celda Default (Sección de hipervínculos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251545
localization_priority: Normal
ms.assetid: 0edea0ea-58dd-15da-6d4f-185d40133452
description: Determina el hipervínculo predeterminado de una forma o página. Asigne a esta celda el valor TRUE para establecer un hipervínculo como predeterminado.
ms.openlocfilehash: a8bfc045559a2c2904ae4a97c489248fb6c446c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821947"
---
# <a name="default-cell-hyperlinks-section"></a><span data-ttu-id="48673-104">Celda Default (Sección de hipervínculos)</span><span class="sxs-lookup"><span data-stu-id="48673-104">Default Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="48673-p102">Determina el hipervínculo predeterminado de una forma o página. Asigne a esta celda el valor TRUE para establecer un hipervínculo como predeterminado.</span><span class="sxs-lookup"><span data-stu-id="48673-p102">Determines the default hyperlink for a shape or page. Set the value of this cell to TRUE to set a hyperlink as the default.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="48673-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="48673-107">Remarks</span></span>

<span data-ttu-id="48673-108">También puede establecer el hipervínculo predeterminado mediante la selección de una forma, hacer clic en **hipervínculo** en la ficha **Insertar** , seleccionar un hipervínculo y, a continuación, haciendo clic en **predeterminado**.</span><span class="sxs-lookup"><span data-stu-id="48673-108">You can also set the default hyperlink by selecting a shape, clicking **Hyperlink** on the **Insert** tab, selecting a hyperlink, and then clicking **Default**.</span></span> <span data-ttu-id="48673-109">El hipervínculo predeterminado aparece en negrita.</span><span class="sxs-lookup"><span data-stu-id="48673-109">The default hyperlink appears in bold text.</span></span>
  
<span data-ttu-id="48673-110">Para obtener una referencia a la celda Default por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="48673-110">To get a reference to the Default cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="48673-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="48673-111">Cell name:</span></span>  <br/> |<span data-ttu-id="48673-112">Hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="48673-112">Hyperlink.</span></span> <span data-ttu-id="48673-113">*Nombre* . Valor predeterminado donde hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="48673-113">*Name*  .Default           where Hyperlink.</span></span> <span data-ttu-id="48673-114">*Nombre* es el nombre de fila</span><span class="sxs-lookup"><span data-stu-id="48673-114">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="48673-115">Para obtener una referencia a la celda Default por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="48673-115">To get a reference to the Default cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="48673-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="48673-116">Section index:</span></span>  <br/> |<span data-ttu-id="48673-117">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="48673-117">**visSectionHyperlink**</span></span> <br/> |
|<span data-ttu-id="48673-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="48673-118">Row index:</span></span>  <br/> |<span data-ttu-id="48673-119">**visRow1stHyperlink** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="48673-119">**visRow1stHyperlink** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="48673-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="48673-120">Cell index:</span></span>  <br/> |<span data-ttu-id="48673-121">**visHLinkDefault**</span><span class="sxs-lookup"><span data-stu-id="48673-121">**visHLinkDefault**</span></span> <br/> |
   

