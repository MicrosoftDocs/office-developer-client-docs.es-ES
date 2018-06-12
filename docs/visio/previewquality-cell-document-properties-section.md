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
ms.openlocfilehash: bc8a53934b6dad06a0867cc73cdfacfa02d2b438
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822838"
---
# <a name="previewquality-cell-document-properties-section"></a><span data-ttu-id="2cf39-103">Celda PreviewQuality (Sección de propiedades del documento)</span><span class="sxs-lookup"><span data-stu-id="2cf39-103">PreviewQuality Cell (Document Properties Section)</span></span>

<span data-ttu-id="2cf39-104">Determina si la vista previa del dibujo tiene calidad de borrador o de detalle.</span><span class="sxs-lookup"><span data-stu-id="2cf39-104">Determines whether the drawing preview is draft quality or detailed.</span></span>
  
|<span data-ttu-id="2cf39-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="2cf39-105">**Value**</span></span>|<span data-ttu-id="2cf39-106">**Calidad de la vista previa**</span><span class="sxs-lookup"><span data-stu-id="2cf39-106">**Preview quality**</span></span>|<span data-ttu-id="2cf39-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="2cf39-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="2cf39-108">0</span><span class="sxs-lookup"><span data-stu-id="2cf39-108">0</span></span>  <br/> | <span data-ttu-id="2cf39-109">Borrador</span><span class="sxs-lookup"><span data-stu-id="2cf39-109">Draft</span></span>  <br/> |<span data-ttu-id="2cf39-110">**visDocPreviewQualityDraft**</span><span class="sxs-lookup"><span data-stu-id="2cf39-110">**visDocPreviewQualityDraft**</span></span> <br/> |
| <span data-ttu-id="2cf39-111">1</span><span class="sxs-lookup"><span data-stu-id="2cf39-111">1</span></span>  <br/> | <span data-ttu-id="2cf39-112">Detallada</span><span class="sxs-lookup"><span data-stu-id="2cf39-112">Detailed</span></span>  <br/> |<span data-ttu-id="2cf39-113">**visDocPreviewQualityDetailed**</span><span class="sxs-lookup"><span data-stu-id="2cf39-113">**visDocPreviewQualityDetailed**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2cf39-114">Notas</span><span class="sxs-lookup"><span data-stu-id="2cf39-114">Remarks</span></span>

<span data-ttu-id="2cf39-115">También puede establecer este valor en la ficha **Resumen** en el cuadro de diálogo **Propiedades** (haga clic en el botón de **Office** , haga clic en la ficha **información** , haga clic en **Propiedades del documento**y, a continuación, haga clic en **Propiedades avanzadas**).</span><span class="sxs-lookup"><span data-stu-id="2cf39-115">You can also set this value on the **Summary** tab in the **Properties** dialog box (click the **Office** button, click the **Info** tab, click **Document Properties**, and then click **Advanced Properties**).</span></span>
  
<span data-ttu-id="2cf39-116">Para obtener una referencia a la celda PreviewQuality por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="2cf39-116">To get a reference to the PreviewQuality cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2cf39-117">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="2cf39-117">Cell name:</span></span>  <br/> | <span data-ttu-id="2cf39-118">PreviewQuality</span><span class="sxs-lookup"><span data-stu-id="2cf39-118">PreviewQuality</span></span>  <br/> |
   
<span data-ttu-id="2cf39-119">Para obtener una referencia a la celda PreviewQuality por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="2cf39-119">To get a reference to the PreviewQuality cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2cf39-120">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="2cf39-120">Section index:</span></span>  <br/> |<span data-ttu-id="2cf39-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2cf39-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2cf39-122">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="2cf39-122">Row index:</span></span>  <br/> |<span data-ttu-id="2cf39-123">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="2cf39-123">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="2cf39-124">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="2cf39-124">Cell index:</span></span>  <br/> |<span data-ttu-id="2cf39-125">**visDocPreviewQuality**</span><span class="sxs-lookup"><span data-stu-id="2cf39-125">**visDocPreviewQuality**</span></span> <br/> |
   

