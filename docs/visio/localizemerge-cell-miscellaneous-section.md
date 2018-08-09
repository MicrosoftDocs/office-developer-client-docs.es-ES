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
ms.openlocfilehash: 47593802e412c1871685f7218dd2a810bc2bc469
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822484"
---
# <a name="localizemerge-cell-miscellaneous-section"></a><span data-ttu-id="fecb6-103">Celda LocalizeMerge (sección Varios)</span><span class="sxs-lookup"><span data-stu-id="fecb6-103">LocalizeMerge Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="fecb6-104">Determina si las formas se traducen al copiarlas de un documento a otro.</span><span class="sxs-lookup"><span data-stu-id="fecb6-104">Determines whether shapes are localized when copied between documents.</span></span>
  
|<span data-ttu-id="fecb6-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="fecb6-105">**Value**</span></span>|<span data-ttu-id="fecb6-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fecb6-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="fecb6-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="fecb6-107">TRUE</span></span>  <br/> | <span data-ttu-id="fecb6-108">Traduce una forma al idioma del documento de destino.</span><span class="sxs-lookup"><span data-stu-id="fecb6-108">Localize a shape in the language of the destination document.</span></span>  <br/> |
| <span data-ttu-id="fecb6-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="fecb6-109">FALSE</span></span>  <br/> | <span data-ttu-id="fecb6-110">No traduce una forma en función del idioma del documento de destino (predeterminado).</span><span class="sxs-lookup"><span data-stu-id="fecb6-110">Do not localize a shape based on the language of the destination document (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fecb6-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fecb6-111">Remarks</span></span>

<span data-ttu-id="fecb6-112">Para obtener una referencia a la celda LocalizeMerge por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="fecb6-112">To get a reference to the LocalizeMerge cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fecb6-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="fecb6-113">Cell name:</span></span>  <br/> | <span data-ttu-id="fecb6-114">LocalizeMerge</span><span class="sxs-lookup"><span data-stu-id="fecb6-114">LocalizeMerge</span></span>  <br/> |
   
<span data-ttu-id="fecb6-115">Para obtener una referencia desde un programa a la celda LocalizeMerge por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="fecb6-115">To get a reference to the LocalizeMerge cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fecb6-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="fecb6-116">Section index:</span></span>  <br/> |<span data-ttu-id="fecb6-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fecb6-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fecb6-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="fecb6-118">Row index:</span></span>  <br/> |<span data-ttu-id="fecb6-119">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="fecb6-119">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="fecb6-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="fecb6-120">Cell index:</span></span>  <br/> |<span data-ttu-id="fecb6-121">**visObjLocalizeMerge**</span><span class="sxs-lookup"><span data-stu-id="fecb6-121">**visObjLocalizeMerge**</span></span> <br/> |
   

