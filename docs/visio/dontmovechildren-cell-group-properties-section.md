---
title: Celda DontMoveChildren (Sección de propiedades del grupo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm255
localization_priority: Normal
ms.assetid: ff5bbf05-4851-30ce-7ee1-f0ce7b2781ab
description: Determina si se puede utilizar el mouse (ratón) para arrastrar las formas de un grupo.
ms.openlocfilehash: df5d0d2b44e283ee8301d9c088d3ce55114e9a75
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822011"
---
# <a name="dontmovechildren-cell-group-properties-section"></a><span data-ttu-id="17210-103">Celda DontMoveChildren (sección Propiedades de grupo)</span><span class="sxs-lookup"><span data-stu-id="17210-103">DontMoveChildren Cell (Group Properties Section)</span></span>

<span data-ttu-id="17210-104">Determina si se puede utilizar el mouse (ratón) para arrastrar las formas de un grupo.</span><span class="sxs-lookup"><span data-stu-id="17210-104">Determines whether you can drag shapes in a group using the mouse.</span></span>
  
|<span data-ttu-id="17210-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="17210-105">**Value**</span></span>|<span data-ttu-id="17210-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="17210-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="17210-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="17210-107">TRUE</span></span>  <br/> | <span data-ttu-id="17210-108">No se permite el uso del mouse para arrastrar las formas de un grupo.</span><span class="sxs-lookup"><span data-stu-id="17210-108">Don't allow shapes in a group to be dragged using the mouse.</span></span>  <br/> |
| <span data-ttu-id="17210-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="17210-109">FALSE</span></span>  <br/> | <span data-ttu-id="17210-110">Se permite el uso del mouse para arrastrar las formas de un grupo.</span><span class="sxs-lookup"><span data-stu-id="17210-110">Allow shapes in a group to be dragged using the mouse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="17210-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="17210-111">Remarks</span></span>

<span data-ttu-id="17210-112">Si el valor de esta celda es TRUE, puede voltear, girar o cambiar el tamaño y la posición de las formas de los grupos mediante otros métodos.</span><span class="sxs-lookup"><span data-stu-id="17210-112">When the value of this cell is TRUE, you can still flip, rotate, resize, or reposition shapes in groups using other methods.</span></span>
  
<span data-ttu-id="17210-113">El valor de esta celda es TRUE para los grupos de los patrones e instancias de patrones que se crearon en versiones de Microsoft Visio anteriores a Visio 2000.</span><span class="sxs-lookup"><span data-stu-id="17210-113">The value of this cell is TRUE for groups in masters and groups in instances of masters that were created in versions of Visio earlier than version 2000.</span></span>
  
<span data-ttu-id="17210-114">Para obtener una referencia a la celda DontMoveChildren por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="17210-114">To get a reference to the DontMoveChildren cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="17210-115">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="17210-115">Cell name:</span></span>  <br/> | <span data-ttu-id="17210-116">DontMoveChildren</span><span class="sxs-lookup"><span data-stu-id="17210-116">DontMoveChildren</span></span>  <br/> |
   
<span data-ttu-id="17210-117">Para obtener una referencia desde un programa a la celda DontMoveChildren por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="17210-117">To get a reference to the DontMoveChildren cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="17210-118">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="17210-118">Section index:</span></span>  <br/> |<span data-ttu-id="17210-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="17210-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="17210-120">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="17210-120">Row index:</span></span>  <br/> |<span data-ttu-id="17210-121">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="17210-121">**visRowGroup**</span></span> <br/> |
| <span data-ttu-id="17210-122">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="17210-122">Cell index:</span></span>  <br/> |<span data-ttu-id="17210-123">**visGroupDontMoveChildren**</span><span class="sxs-lookup"><span data-stu-id="17210-123">**visGroupDontMoveChildren**</span></span> <br/> |
   

