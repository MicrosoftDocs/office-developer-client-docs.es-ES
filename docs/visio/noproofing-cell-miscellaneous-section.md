---
title: Celda NoProofing (sección Varios)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 668f993c-b4d1-4762-9801-c578b17fdafd
description: Determina si la ortografía se corrige automáticamente y si se muestran errores ortográficos para la forma seleccionada. Toma un valor booleano.
ms.openlocfilehash: 8d7eebcc349c54db3cd48d6c5fa3c8fa6f4f760e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431256"
---
# <a name="noproofing-cell-miscellaneous-section"></a><span data-ttu-id="a350a-104">Celda NoProofing (sección Varios)</span><span class="sxs-lookup"><span data-stu-id="a350a-104">NoProofing Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="a350a-105">Determina si la ortografía se corrige automáticamente y si se muestran errores ortográficos para la forma seleccionada.</span><span class="sxs-lookup"><span data-stu-id="a350a-105">Determines whether spelling is automatically corrected and whether spelling errors are displayed for the selected shape.</span></span> <span data-ttu-id="a350a-106">Toma un **valor booleano.**</span><span class="sxs-lookup"><span data-stu-id="a350a-106">Takes a **Boolean** value.</span></span> 
  
|<span data-ttu-id="a350a-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a350a-107">**Value**</span></span>|<span data-ttu-id="a350a-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a350a-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a350a-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="a350a-109">TRUE</span></span>  <br/> |<span data-ttu-id="a350a-110">La ortografía no se corrige automáticamente y los errores ortográficos no se muestran para la forma seleccionada.</span><span class="sxs-lookup"><span data-stu-id="a350a-110">Spelling is not automatically corrected and spelling errors are not displayed for the selected shape.</span></span>  <br/> |
|<span data-ttu-id="a350a-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="a350a-111">FALSE</span></span>  <br/> |<span data-ttu-id="a350a-112">La ortografía se corrige automáticamente y los errores ortográficos se muestran para la forma seleccionada.</span><span class="sxs-lookup"><span data-stu-id="a350a-112">Spelling is automatically corrected and spelling errors are displayed for the selected shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a350a-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a350a-113">Remarks</span></span>

<span data-ttu-id="a350a-114">Para obtener una referencia a la celda NoProofing por su nombre desde otra fórmula o desde un programa, mediante la **propiedad CellsU,** use:</span><span class="sxs-lookup"><span data-stu-id="a350a-114">To get a reference to the NoProofing cell by name from another formula or from a program, by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a350a-115">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="a350a-115">Cell name:</span></span>  <br/> |<span data-ttu-id="a350a-116">NoProofing</span><span class="sxs-lookup"><span data-stu-id="a350a-116">NoProofing</span></span>  <br/> |
   
<span data-ttu-id="a350a-117">Para obtener una referencia desde un programa a la celda NoProofing por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="a350a-117">To get a reference to the NoProofing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a350a-118">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="a350a-118">Section index:</span></span>  <br/> |<span data-ttu-id="a350a-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a350a-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a350a-120">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="a350a-120">Row index:</span></span>  <br/> |<span data-ttu-id="a350a-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="a350a-121">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="a350a-122">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="a350a-122">Cell index:</span></span>  <br/> |<span data-ttu-id="a350a-123">**visObjNoProofing**</span><span class="sxs-lookup"><span data-stu-id="a350a-123">**visObjNoProofing**</span></span> <br/> |
   

