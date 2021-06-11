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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434357"
---
# <a name="default-cell-hyperlinks-section"></a><span data-ttu-id="53329-104">Celda Default (Sección de hipervínculos)</span><span class="sxs-lookup"><span data-stu-id="53329-104">Default Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="53329-p102">Determina el hipervínculo predeterminado de una forma o página. Asigne a esta celda el valor TRUE para establecer un hipervínculo como predeterminado.</span><span class="sxs-lookup"><span data-stu-id="53329-p102">Determines the default hyperlink for a shape or page. Set the value of this cell to TRUE to set a hyperlink as the default.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="53329-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="53329-107">Remarks</span></span>

<span data-ttu-id="53329-p103">Para establecer el hipervínculo predeterminado, también puede seleccionar una forma, hacer clic en **Hipervínculos** en el menú **Insertar**, seleccionar un hipervínculo y, a continuación, hacer clic en **Predeterminado**. El hipervínculo predeterminado aparecerá en negrita.</span><span class="sxs-lookup"><span data-stu-id="53329-p103">You can also set the default hyperlink by selecting a shape, clicking **Hyperlink** on the **Insert** tab, selecting a hyperlink, and then clicking **Default**. The default hyperlink appears in bold text.</span></span>
  
<span data-ttu-id="53329-110">Para obtener una referencia a la celda Default por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="53329-110">To get a reference to the Default cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="53329-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="53329-111">Cell name:</span></span>  <br/> |<span data-ttu-id="53329-112">Hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="53329-112">Hyperlink.</span></span> <span data-ttu-id="53329-113">*Nombre*  . Valor predeterminado donde Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="53329-113">*Name*  .Default           where Hyperlink.</span></span> <span data-ttu-id="53329-114">*Name*  es el nombre de fila</span><span class="sxs-lookup"><span data-stu-id="53329-114">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="53329-115">Para obtener una referencia desde un programa a la celda Default por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="53329-115">To get a reference to the Default cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="53329-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="53329-116">Section index:</span></span>  <br/> |<span data-ttu-id="53329-117">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="53329-117">**visSectionHyperlink**</span></span> <br/> |
|<span data-ttu-id="53329-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="53329-118">Row index:</span></span>  <br/> |<span data-ttu-id="53329-119">**visRow1stHyperlink**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="53329-119">**visRow1stHyperlink** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="53329-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="53329-120">Cell index:</span></span>  <br/> |<span data-ttu-id="53329-121">**visHLinkDefault**</span><span class="sxs-lookup"><span data-stu-id="53329-121">**visHLinkDefault**</span></span> <br/> |
   

