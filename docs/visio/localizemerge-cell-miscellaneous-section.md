---
title: Celda LocalizeMerge (Sección de varios)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033773
localization_priority: Normal
ms.assetid: 734d4415-05dd-4c4d-763e-e035fa56dcec
description: Determina si las formas se traducen al copiarlas de un documento a otro.
ms.openlocfilehash: ddd6041ec6531652deb38a0c16be2c741bac91a6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405677"
---
# <a name="localizemerge-cell-miscellaneous-section"></a><span data-ttu-id="53487-103">Celda LocalizeMerge (Sección de varios)</span><span class="sxs-lookup"><span data-stu-id="53487-103">LocalizeMerge Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="53487-104">Determina si las formas se traducen al copiarlas de un documento a otro.</span><span class="sxs-lookup"><span data-stu-id="53487-104">Determines whether shapes are localized when copied between documents.</span></span>
  
|<span data-ttu-id="53487-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="53487-105">**Value**</span></span>|<span data-ttu-id="53487-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="53487-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="53487-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="53487-107">TRUE</span></span>  <br/> | <span data-ttu-id="53487-108">Traduce una forma al idioma del documento de destino.</span><span class="sxs-lookup"><span data-stu-id="53487-108">Localize a shape in the language of the destination document.</span></span>  <br/> |
| <span data-ttu-id="53487-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="53487-109">FALSE</span></span>  <br/> | <span data-ttu-id="53487-110">No localice una forma según el idioma del documento de destino (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="53487-110">Do not localize a shape based on the language of the destination document (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53487-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="53487-111">Remarks</span></span>

<span data-ttu-id="53487-112">Para obtener una referencia a la celda LocalizeMerge por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="53487-112">To get a reference to the LocalizeMerge cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="53487-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="53487-113">Cell name:</span></span>  <br/> | <span data-ttu-id="53487-114">LocalizeMerge</span><span class="sxs-lookup"><span data-stu-id="53487-114">LocalizeMerge</span></span>  <br/> |
   
<span data-ttu-id="53487-115">Para obtener una referencia desde un programa a la celda LocalizeMerge por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="53487-115">To get a reference to the LocalizeMerge cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="53487-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="53487-116">Section index:</span></span>  <br/> |<span data-ttu-id="53487-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="53487-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="53487-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="53487-118">Row index:</span></span>  <br/> |<span data-ttu-id="53487-119">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="53487-119">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="53487-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="53487-120">Cell index:</span></span>  <br/> |<span data-ttu-id="53487-121">**visObjLocalizeMerge**</span><span class="sxs-lookup"><span data-stu-id="53487-121">**visObjLocalizeMerge**</span></span> <br/> |
   

