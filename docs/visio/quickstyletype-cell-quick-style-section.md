---
title: Celda QuickStyleType (sección Estilos rápidos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7470417-0d70-433e-9496-604ca2eafee6
description: Determina el tipo de estilo rápido (dimensional 1, 2-dimensional o conector) que hereda de la forma.
ms.openlocfilehash: 211074800eee601d2658edbc03bb95d028920e54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822891"
---
# <a name="quickstyletype-cell-quick-style-section"></a><span data-ttu-id="645b7-103">Celda QuickStyleType (sección Estilos rápidos)</span><span class="sxs-lookup"><span data-stu-id="645b7-103">QuickStyleType Cell (Quick Style Section)</span></span>

<span data-ttu-id="645b7-104">Determina el tipo de estilo rápido (dimensional 1, 2-dimensional o conector) que hereda de la forma.</span><span class="sxs-lookup"><span data-stu-id="645b7-104">Determines the type of Quick Style (2-dimensional, 1-dimensional, or connector) that the shape inherits.</span></span> 
  
|<span data-ttu-id="645b7-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="645b7-105">**Value**</span></span>|<span data-ttu-id="645b7-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="645b7-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="645b7-107">0</span><span class="sxs-lookup"><span data-stu-id="645b7-107">0</span></span>  <br/> |<span data-ttu-id="645b7-108">Visio elige automáticamente</span><span class="sxs-lookup"><span data-stu-id="645b7-108">Visio chooses automatically</span></span>  <br/> |
|<span data-ttu-id="645b7-109">1</span><span class="sxs-lookup"><span data-stu-id="645b7-109">1</span></span>  <br/> |<span data-ttu-id="645b7-110">1-dimensional</span><span class="sxs-lookup"><span data-stu-id="645b7-110">1-dimensional</span></span>  <br/> |
|<span data-ttu-id="645b7-111">2</span><span class="sxs-lookup"><span data-stu-id="645b7-111">2</span></span>  <br/> |<span data-ttu-id="645b7-112">2-dimensional</span><span class="sxs-lookup"><span data-stu-id="645b7-112">2-dimensional</span></span>  <br/> |
|<span data-ttu-id="645b7-113">3</span><span class="sxs-lookup"><span data-stu-id="645b7-113">3</span></span>  <br/> |<span data-ttu-id="645b7-114">Conector</span><span class="sxs-lookup"><span data-stu-id="645b7-114">Connector</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="645b7-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="645b7-115">Remarks</span></span>

<span data-ttu-id="645b7-116">Para obtener una referencia a la celda **QuickStyleType** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="645b7-116">To get a reference to the **QuickStyleType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="645b7-117">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="645b7-117">Cell name:</span></span>  <br/> | <span data-ttu-id="645b7-118">QuickStyleType</span><span class="sxs-lookup"><span data-stu-id="645b7-118">QuickStyleType</span></span>  <br/> |
   
<span data-ttu-id="645b7-119">Para obtener una referencia a la celda **QuickStyleType** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="645b7-119">To get a reference to the **QuickStyleType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="645b7-120">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="645b7-120">Section index:</span></span>  <br/> |<span data-ttu-id="645b7-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="645b7-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="645b7-122">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="645b7-122">Row index:</span></span>  <br/> |<span data-ttu-id="645b7-123">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="645b7-123">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="645b7-124">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="645b7-124">Cell index:</span></span>  <br/> |<span data-ttu-id="645b7-125">**visQuickStyleType**</span><span class="sxs-lookup"><span data-stu-id="645b7-125">**visQuickStyleType**</span></span> <br/> |
   

