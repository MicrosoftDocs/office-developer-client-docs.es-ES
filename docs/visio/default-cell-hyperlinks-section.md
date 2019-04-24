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
ms.openlocfilehash: 9991bd0e241c5dfd4fda65aeff8b6cc203ad3458
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360280"
---
# <a name="default-cell-hyperlinks-section"></a><span data-ttu-id="4f99e-104">Celda Default (Sección de hipervínculos)</span><span class="sxs-lookup"><span data-stu-id="4f99e-104">Default Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="4f99e-p102">Determina el hipervínculo predeterminado de una forma o página. Asigne a esta celda el valor TRUE para establecer un hipervínculo como predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4f99e-p102">Determines the default hyperlink for a shape or page. Set the value of this cell to TRUE to set a hyperlink as the default.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4f99e-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4f99e-107">Remarks</span></span>

<span data-ttu-id="4f99e-p103">Para establecer el hipervínculo predeterminado, también puede seleccionar una forma, hacer clic en **Hipervínculos** en el menú **Insertar**, seleccionar un hipervínculo y, a continuación, hacer clic en **Predeterminado**. El hipervínculo predeterminado aparecerá en negrita.</span><span class="sxs-lookup"><span data-stu-id="4f99e-p103">You can also set the default hyperlink by selecting a shape, clicking **Hyperlink** on the **Insert** tab, selecting a hyperlink, and then clicking **Default**. The default hyperlink appears in bold text.</span></span>
  
<span data-ttu-id="4f99e-110">Para obtener una referencia a la celda Default por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="4f99e-110">To get a reference to the Default cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4f99e-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="4f99e-111">Cell name:</span></span>  <br/> |<span data-ttu-id="4f99e-112">Hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="4f99e-112">Hyperlink.</span></span> <span data-ttu-id="4f99e-113">*Nombre* . Valor predeterminado donde HYPERLINK.</span><span class="sxs-lookup"><span data-stu-id="4f99e-113">*Name*  .Default           where Hyperlink.</span></span> <span data-ttu-id="4f99e-114">*Name* es el nombre de la fila</span><span class="sxs-lookup"><span data-stu-id="4f99e-114">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="4f99e-115">Para obtener una referencia desde un programa a la celda Default por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="4f99e-115">To get a reference to the Default cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4f99e-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="4f99e-116">Section index:</span></span>  <br/> |<span data-ttu-id="4f99e-117">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="4f99e-117">**visSectionHyperlink**</span></span> <br/> |
|<span data-ttu-id="4f99e-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="4f99e-118">Row index:</span></span>  <br/> |<span data-ttu-id="4f99e-119">**visRow1stHyperlink** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="4f99e-119">**visRow1stHyperlink** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="4f99e-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="4f99e-120">Cell index:</span></span>  <br/> |<span data-ttu-id="4f99e-121">**visHLinkDefault**</span><span class="sxs-lookup"><span data-stu-id="4f99e-121">**visHLinkDefault**</span></span> <br/> |
   

