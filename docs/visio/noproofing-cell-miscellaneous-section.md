---
title: Celda NoProofing (sección de varios)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 668f993c-b4d1-4762-9801-c578b17fdafd
description: Determina si se ha corregido automáticamente ortografía y si se muestran los errores de ortografía para la forma seleccionada. Toma un valor booleano.
ms.openlocfilehash: 6c27e6740b547af83058519de8edd38fc3522b32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/21/2018
ms.locfileid: "19822678"
---
# <a name="noproofing-cell-miscellaneous-section"></a><span data-ttu-id="0db44-104">Celda NoProofing (sección de varios)</span><span class="sxs-lookup"><span data-stu-id="0db44-104">NoProofing Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="0db44-105">Determina si se ha corregido automáticamente ortografía y si se muestran los errores de ortografía para la forma seleccionada.</span><span class="sxs-lookup"><span data-stu-id="0db44-105">Determines whether spelling is automatically corrected and whether spelling errors are displayed for the selected shape.</span></span> <span data-ttu-id="0db44-106">Toma un valor **booleano** .</span><span class="sxs-lookup"><span data-stu-id="0db44-106">Takes a **Boolean** value.</span></span> 
  
|<span data-ttu-id="0db44-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="0db44-107">**Value**</span></span>|<span data-ttu-id="0db44-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0db44-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0db44-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="0db44-109">TRUE</span></span>  <br/> |<span data-ttu-id="0db44-110">Ortografía no se corrige automáticamente y no se muestran errores de ortografía para la forma seleccionada.</span><span class="sxs-lookup"><span data-stu-id="0db44-110">Spelling is not automatically corrected and spelling errors are not displayed for the selected shape.</span></span>  <br/> |
|<span data-ttu-id="0db44-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="0db44-111">FALSE</span></span>  <br/> |<span data-ttu-id="0db44-112">Ortografía se corrige automáticamente y se muestran los errores de ortografía para la forma seleccionada.</span><span class="sxs-lookup"><span data-stu-id="0db44-112">Spelling is automatically corrected and spelling errors are displayed for the selected shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0db44-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0db44-113">Remarks</span></span>

<span data-ttu-id="0db44-114">Para obtener una referencia a la celda NoProofing por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="0db44-114">To get a reference to the NoProofing cell by name from another formula or from a program, by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0db44-115">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="0db44-115">Cell name:</span></span>  <br/> |<span data-ttu-id="0db44-116">NoProofing</span><span class="sxs-lookup"><span data-stu-id="0db44-116">NoProofing</span></span>  <br/> |
   
<span data-ttu-id="0db44-117">Para obtener una referencia a la celda NoProofing por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="0db44-117">To get a reference to the NoProofing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0db44-118">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="0db44-118">Section index:</span></span>  <br/> |<span data-ttu-id="0db44-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0db44-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="0db44-120">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="0db44-120">Row index:</span></span>  <br/> |<span data-ttu-id="0db44-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="0db44-121">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="0db44-122">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="0db44-122">Cell index:</span></span>  <br/> |<span data-ttu-id="0db44-123">**visObjNoProofing**</span><span class="sxs-lookup"><span data-stu-id="0db44-123">**visObjNoProofing**</span></span> <br/> |
   

