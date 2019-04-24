---
title: Celda QuickStyleType (sección estilos rápidos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7470417-0d70-433e-9496-604ca2eafee6
description: Determina el tipo de estilo rápido (2D, unidimensional o conector) que hereda la forma.
ms.openlocfilehash: 95aced62c6397fc3229de29b98d3f18e5f69d05b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282582"
---
# <a name="quickstyletype-cell-quick-style-section"></a><span data-ttu-id="2eadf-103">Celda QuickStyleType (sección estilos rápidos)</span><span class="sxs-lookup"><span data-stu-id="2eadf-103">QuickStyleType Cell (Quick Style Section)</span></span>

<span data-ttu-id="2eadf-104">Determina el tipo de estilo rápido (2D, unidimensional o conector) que hereda la forma.</span><span class="sxs-lookup"><span data-stu-id="2eadf-104">Determines the type of Quick Style (2-dimensional, 1-dimensional, or connector) that the shape inherits.</span></span> 
  
|<span data-ttu-id="2eadf-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="2eadf-105">**Value**</span></span>|<span data-ttu-id="2eadf-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2eadf-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2eadf-107">comprendi</span><span class="sxs-lookup"><span data-stu-id="2eadf-107">0</span></span>  <br/> |<span data-ttu-id="2eadf-108">Visio elige automáticamente</span><span class="sxs-lookup"><span data-stu-id="2eadf-108">Visio chooses automatically</span></span>  <br/> |
|<span data-ttu-id="2eadf-109">1</span><span class="sxs-lookup"><span data-stu-id="2eadf-109">1</span></span>  <br/> |<span data-ttu-id="2eadf-110">1-dimensional</span><span class="sxs-lookup"><span data-stu-id="2eadf-110">1-dimensional</span></span>  <br/> |
|<span data-ttu-id="2eadf-111">segundo</span><span class="sxs-lookup"><span data-stu-id="2eadf-111">2</span></span>  <br/> |<span data-ttu-id="2eadf-112">2 dimensiones</span><span class="sxs-lookup"><span data-stu-id="2eadf-112">2-dimensional</span></span>  <br/> |
|<span data-ttu-id="2eadf-113">3</span><span class="sxs-lookup"><span data-stu-id="2eadf-113">3</span></span>  <br/> |<span data-ttu-id="2eadf-114">Connector</span><span class="sxs-lookup"><span data-stu-id="2eadf-114">Connector</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2eadf-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2eadf-115">Remarks</span></span>

<span data-ttu-id="2eadf-116">Para obtener una referencia a la celda **QuickStyleType** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="2eadf-116">To get a reference to the **QuickStyleType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2eadf-117">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="2eadf-117">Cell name:</span></span>  <br/> | <span data-ttu-id="2eadf-118">QuickStyleType</span><span class="sxs-lookup"><span data-stu-id="2eadf-118">QuickStyleType</span></span>  <br/> |
   
<span data-ttu-id="2eadf-119">Para obtener una referencia desde un programa a la celda **QuickStyleType** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="2eadf-119">To get a reference to the **QuickStyleType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2eadf-120">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="2eadf-120">Section index:</span></span>  <br/> |<span data-ttu-id="2eadf-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2eadf-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2eadf-122">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="2eadf-122">Row index:</span></span>  <br/> |<span data-ttu-id="2eadf-123">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="2eadf-123">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="2eadf-124">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="2eadf-124">Cell index:</span></span>  <br/> |<span data-ttu-id="2eadf-125">**visQuickStyleType**</span><span class="sxs-lookup"><span data-stu-id="2eadf-125">**visQuickStyleType**</span></span> <br/> |
   

