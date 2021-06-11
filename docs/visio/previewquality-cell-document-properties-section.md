---
title: Celda PreviewQuality (Sección de propiedades del documento)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm815
localization_priority: Normal
ms.assetid: b7d90666-a1bb-f0de-32da-b2855977f648
description: Determina si la vista previa del dibujo tiene calidad de borrador o de detalle.
ms.openlocfilehash: 9db2d3e1eb829bfd2ad787fcfc94cd9ba5abaf9e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416821"
---
# <a name="previewquality-cell-document-properties-section"></a><span data-ttu-id="f4831-103">Celda PreviewQuality (Sección de propiedades del documento)</span><span class="sxs-lookup"><span data-stu-id="f4831-103">PreviewQuality Cell (Document Properties Section)</span></span>

<span data-ttu-id="f4831-104">Determina si la vista previa del dibujo tiene calidad de borrador o de detalle.</span><span class="sxs-lookup"><span data-stu-id="f4831-104">Determines whether the drawing preview is draft quality or detailed.</span></span>
  
|<span data-ttu-id="f4831-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="f4831-105">**Value**</span></span>|<span data-ttu-id="f4831-106">**Calidad de la vista previa**</span><span class="sxs-lookup"><span data-stu-id="f4831-106">**Preview quality**</span></span>|<span data-ttu-id="f4831-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="f4831-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="f4831-108">0</span><span class="sxs-lookup"><span data-stu-id="f4831-108">0</span></span>  <br/> | <span data-ttu-id="f4831-109">Borrador</span><span class="sxs-lookup"><span data-stu-id="f4831-109">Draft</span></span>  <br/> |<span data-ttu-id="f4831-110">**visDocPreviewQualityDraft**</span><span class="sxs-lookup"><span data-stu-id="f4831-110">**visDocPreviewQualityDraft**</span></span> <br/> |
| <span data-ttu-id="f4831-111">1</span><span class="sxs-lookup"><span data-stu-id="f4831-111">1</span></span>  <br/> | <span data-ttu-id="f4831-112">Detallado</span><span class="sxs-lookup"><span data-stu-id="f4831-112">Detailed</span></span>  <br/> |<span data-ttu-id="f4831-113">**visDocPreviewQualityDetailed**</span><span class="sxs-lookup"><span data-stu-id="f4831-113">**visDocPreviewQualityDetailed**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4831-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f4831-114">Remarks</span></span>

<span data-ttu-id="f4831-115">También puede establecer este valor en la ficha Resumen del cuadro de diálogo Propiedades  (haga clic en el botón **Office,** haga clic en la pestaña Información, haga clic en Propiedades del documento y, a continuación, en **Propiedades avanzadas**).  </span><span class="sxs-lookup"><span data-stu-id="f4831-115">You can also set this value on the **Summary** tab in the **Properties** dialog box (click the **Office** button, click the **Info** tab, click **Document Properties**, and then click **Advanced Properties**).</span></span>
  
<span data-ttu-id="f4831-116">Para obtener una referencia a la celda PreviewQuality por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="f4831-116">To get a reference to the PreviewQuality cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f4831-117">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="f4831-117">Cell name:</span></span>  <br/> | <span data-ttu-id="f4831-118">PreviewQuality</span><span class="sxs-lookup"><span data-stu-id="f4831-118">PreviewQuality</span></span>  <br/> |
   
<span data-ttu-id="f4831-119">Para obtener una referencia desde un programa a la celda PreviewQuality por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="f4831-119">To get a reference to the PreviewQuality cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f4831-120">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="f4831-120">Section index:</span></span>  <br/> |<span data-ttu-id="f4831-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f4831-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f4831-122">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="f4831-122">Row index:</span></span>  <br/> |<span data-ttu-id="f4831-123">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="f4831-123">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="f4831-124">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="f4831-124">Cell index:</span></span>  <br/> |<span data-ttu-id="f4831-125">**visDocPreviewQuality**</span><span class="sxs-lookup"><span data-stu-id="f4831-125">**visDocPreviewQuality**</span></span> <br/> |
   

