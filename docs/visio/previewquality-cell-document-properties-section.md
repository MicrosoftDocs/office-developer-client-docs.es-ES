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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356038"
---
# <a name="previewquality-cell-document-properties-section"></a><span data-ttu-id="5d87c-103">Celda PreviewQuality (Sección de propiedades del documento)</span><span class="sxs-lookup"><span data-stu-id="5d87c-103">PreviewQuality Cell (Document Properties Section)</span></span>

<span data-ttu-id="5d87c-104">Determina si la vista previa del dibujo tiene calidad de borrador o de detalle.</span><span class="sxs-lookup"><span data-stu-id="5d87c-104">Determines whether the drawing preview is draft quality or detailed.</span></span>
  
|<span data-ttu-id="5d87c-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="5d87c-105">**Value**</span></span>|<span data-ttu-id="5d87c-106">**Calidad de la vista previa**</span><span class="sxs-lookup"><span data-stu-id="5d87c-106">**Preview quality**</span></span>|<span data-ttu-id="5d87c-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="5d87c-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="5d87c-108">comprendi</span><span class="sxs-lookup"><span data-stu-id="5d87c-108">0</span></span>  <br/> | <span data-ttu-id="5d87c-109">Draft</span><span class="sxs-lookup"><span data-stu-id="5d87c-109">Draft</span></span>  <br/> |<span data-ttu-id="5d87c-110">**visDocPreviewQualityDraft**</span><span class="sxs-lookup"><span data-stu-id="5d87c-110">**visDocPreviewQualityDraft**</span></span> <br/> |
| <span data-ttu-id="5d87c-111">1</span><span class="sxs-lookup"><span data-stu-id="5d87c-111">1</span></span>  <br/> | <span data-ttu-id="5d87c-112">Detallada</span><span class="sxs-lookup"><span data-stu-id="5d87c-112">Detailed</span></span>  <br/> |<span data-ttu-id="5d87c-113">**visDocPreviewQualityDetailed**</span><span class="sxs-lookup"><span data-stu-id="5d87c-113">**visDocPreviewQualityDetailed**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5d87c-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5d87c-114">Remarks</span></span>

<span data-ttu-id="5d87c-115">También puede establecer este valor en la ficha **Resumen** del cuadro de diálogo **propiedades** (haga clic en el botón de **Office** , haga clic en la pestaña **información** , haga clic en **propiedades del documento**y, a continuación, haga clic en **propiedades avanzadas**).</span><span class="sxs-lookup"><span data-stu-id="5d87c-115">You can also set this value on the **Summary** tab in the **Properties** dialog box (click the **Office** button, click the **Info** tab, click **Document Properties**, and then click **Advanced Properties**).</span></span>
  
<span data-ttu-id="5d87c-116">Para obtener una referencia a la celda PreviewQuality por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="5d87c-116">To get a reference to the PreviewQuality cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5d87c-117">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="5d87c-117">Cell name:</span></span>  <br/> | <span data-ttu-id="5d87c-118">PreviewQuality</span><span class="sxs-lookup"><span data-stu-id="5d87c-118">PreviewQuality</span></span>  <br/> |
   
<span data-ttu-id="5d87c-119">Para obtener una referencia desde un programa a la celda PreviewQuality por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="5d87c-119">To get a reference to the PreviewQuality cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5d87c-120">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="5d87c-120">Section index:</span></span>  <br/> |<span data-ttu-id="5d87c-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5d87c-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5d87c-122">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="5d87c-122">Row index:</span></span>  <br/> |<span data-ttu-id="5d87c-123">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="5d87c-123">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="5d87c-124">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="5d87c-124">Cell index:</span></span>  <br/> |<span data-ttu-id="5d87c-125">**visDocPreviewQuality**</span><span class="sxs-lookup"><span data-stu-id="5d87c-125">**visDocPreviewQuality**</span></span> <br/> |
   

