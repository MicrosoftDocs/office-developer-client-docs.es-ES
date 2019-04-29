---
title: Celda LockPreview (Sección de propiedades del documento)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251742
localization_priority: Normal
ms.assetid: 5a2bb1a7-e688-d32f-f231-ac6916d838a6
description: Determina si una vista previa se guarda automáticamente al guardar un dibujo.
ms.openlocfilehash: 91362d8a88cf6db2f4807c655a6d071ebbc731f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418865"
---
# <a name="lockpreview-cell-document-properties-section"></a><span data-ttu-id="7b9c0-103">Celda LockPreview (sección de propiedades del documento)</span><span class="sxs-lookup"><span data-stu-id="7b9c0-103">LockPreview Cell (Document Properties Section)</span></span>

<span data-ttu-id="7b9c0-104">Determina si una vista previa se guarda automáticamente al guardar un dibujo.</span><span class="sxs-lookup"><span data-stu-id="7b9c0-104">Determines whether a preview is saved each time you save a drawing.</span></span>
  
|<span data-ttu-id="7b9c0-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="7b9c0-105">**Value**</span></span>|<span data-ttu-id="7b9c0-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7b9c0-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="7b9c0-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="7b9c0-107">TRUE</span></span>  <br/> | <span data-ttu-id="7b9c0-108">No guardar una vista previa cada vez que se guarde un dibujo.</span><span class="sxs-lookup"><span data-stu-id="7b9c0-108">Do not save a preview each time a drawing is saved.</span></span>  <br/> |
| <span data-ttu-id="7b9c0-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="7b9c0-109">FALSE</span></span>  <br/> | <span data-ttu-id="7b9c0-110">Guardar una vista previa cada vez que se guarde un dibujo.</span><span class="sxs-lookup"><span data-stu-id="7b9c0-110">Save a preview each time a drawing is saved.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b9c0-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7b9c0-111">Remarks</span></span>

<span data-ttu-id="7b9c0-112">Para obtener una referencia a la celda LockPreview por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="7b9c0-112">To get a reference to the LockPreview cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7b9c0-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="7b9c0-113">Cell name:</span></span>  <br/> | <span data-ttu-id="7b9c0-114">LockPreview</span><span class="sxs-lookup"><span data-stu-id="7b9c0-114">LockPreview</span></span>  <br/> |
   
<span data-ttu-id="7b9c0-115">Para obtener una referencia desde un programa a la celda LockPreview por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="7b9c0-115">To get a reference to the LockPreview cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7b9c0-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="7b9c0-116">Section index:</span></span>  <br/> |<span data-ttu-id="7b9c0-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7b9c0-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7b9c0-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="7b9c0-118">Row index:</span></span>  <br/> |<span data-ttu-id="7b9c0-119">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="7b9c0-119">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="7b9c0-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="7b9c0-120">Cell index:</span></span>  <br/> |<span data-ttu-id="7b9c0-121">**visDocLockPreview**</span><span class="sxs-lookup"><span data-stu-id="7b9c0-121">**visDocLockPreview**</span></span> <br/> |
   

