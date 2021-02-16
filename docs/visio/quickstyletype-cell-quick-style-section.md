---
title: Celda QuickStyleType (Sección de estilo rápido)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7470417-0d70-433e-9496-604ca2eafee6
description: Determina el tipo de estilo rápido (bidimensional, unidimensional o conector) que hereda la forma.
ms.openlocfilehash: 95aced62c6397fc3229de29b98d3f18e5f69d05b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410507"
---
# <a name="quickstyletype-cell-quick-style-section"></a><span data-ttu-id="17b8f-103">Celda QuickStyleType (Sección de estilo rápido)</span><span class="sxs-lookup"><span data-stu-id="17b8f-103">QuickStyleType Cell (Quick Style Section)</span></span>

<span data-ttu-id="17b8f-104">Determina el tipo de estilo rápido (bidimensional, unidimensional o conector) que hereda la forma.</span><span class="sxs-lookup"><span data-stu-id="17b8f-104">Determines the type of Quick Style (2-dimensional, 1-dimensional, or connector) that the shape inherits.</span></span> 
  
|<span data-ttu-id="17b8f-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="17b8f-105">**Value**</span></span>|<span data-ttu-id="17b8f-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="17b8f-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="17b8f-107">0</span><span class="sxs-lookup"><span data-stu-id="17b8f-107">0</span></span>  <br/> |<span data-ttu-id="17b8f-108">Visio elige automáticamente</span><span class="sxs-lookup"><span data-stu-id="17b8f-108">Visio chooses automatically</span></span>  <br/> |
|<span data-ttu-id="17b8f-109">1 </span><span class="sxs-lookup"><span data-stu-id="17b8f-109">1</span></span>  <br/> |<span data-ttu-id="17b8f-110">1 dimensional</span><span class="sxs-lookup"><span data-stu-id="17b8f-110">1-dimensional</span></span>  <br/> |
|<span data-ttu-id="17b8f-111">2 </span><span class="sxs-lookup"><span data-stu-id="17b8f-111">2</span></span>  <br/> |<span data-ttu-id="17b8f-112">2 dimensiones</span><span class="sxs-lookup"><span data-stu-id="17b8f-112">2-dimensional</span></span>  <br/> |
|<span data-ttu-id="17b8f-113">3 </span><span class="sxs-lookup"><span data-stu-id="17b8f-113">3</span></span>  <br/> |<span data-ttu-id="17b8f-114">Connector</span><span class="sxs-lookup"><span data-stu-id="17b8f-114">Connector</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="17b8f-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="17b8f-115">Remarks</span></span>

<span data-ttu-id="17b8f-116">Para obtener una referencia a la celda **QuickStyleType** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** o desde un programa mediante la propiedad **CellsU,** utilice:</span><span class="sxs-lookup"><span data-stu-id="17b8f-116">To get a reference to the **QuickStyleType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="17b8f-117">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="17b8f-117">Cell name:</span></span>  <br/> | <span data-ttu-id="17b8f-118">QuickStyleType</span><span class="sxs-lookup"><span data-stu-id="17b8f-118">QuickStyleType</span></span>  <br/> |
   
<span data-ttu-id="17b8f-119">Para obtener una referencia desde un programa a la **celda QuickStyleType** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="17b8f-119">To get a reference to the **QuickStyleType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="17b8f-120">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="17b8f-120">Section index:</span></span>  <br/> |<span data-ttu-id="17b8f-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="17b8f-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="17b8f-122">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="17b8f-122">Row index:</span></span>  <br/> |<span data-ttu-id="17b8f-123">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="17b8f-123">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="17b8f-124">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="17b8f-124">Cell index:</span></span>  <br/> |<span data-ttu-id="17b8f-125">**visQuickStyleType**</span><span class="sxs-lookup"><span data-stu-id="17b8f-125">**visQuickStyleType**</span></span> <br/> |
   

