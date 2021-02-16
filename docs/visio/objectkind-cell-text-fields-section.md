---
title: Celda ObjectKind (Sección de campos de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60058
localization_priority: Normal
ms.assetid: cc4c373c-f073-e3c9-3aaa-a4abf050cd20
description: Indica el tipo de campo de texto.
ms.openlocfilehash: c2f891620f704a3c48861124b886e49d356960ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438515"
---
# <a name="objectkind-cell-text-fields-section"></a><span data-ttu-id="df989-103">Celda ObjectKind (Sección de campos de texto)</span><span class="sxs-lookup"><span data-stu-id="df989-103">ObjectKind Cell (Text Fields Section)</span></span>

<span data-ttu-id="df989-104">Indica el tipo de campo de texto.</span><span class="sxs-lookup"><span data-stu-id="df989-104">Indicates the type of text field.</span></span>
  
|<span data-ttu-id="df989-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="df989-105">**Value**</span></span>|<span data-ttu-id="df989-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="df989-106">**Description**</span></span>|<span data-ttu-id="df989-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="df989-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="df989-108">0</span><span class="sxs-lookup"><span data-stu-id="df989-108">0</span></span>  <br/> | <span data-ttu-id="df989-109">Estándar</span><span class="sxs-lookup"><span data-stu-id="df989-109">Standard</span></span>  <br/> |<span data-ttu-id="df989-110">**visTFOKStandard**</span><span class="sxs-lookup"><span data-stu-id="df989-110">**visTFOKStandard**</span></span> <br/> |
| <span data-ttu-id="df989-111">1 </span><span class="sxs-lookup"><span data-stu-id="df989-111">1</span></span>  <br/> |<span data-ttu-id="df989-112">Horizontal en vertical</span><span class="sxs-lookup"><span data-stu-id="df989-112">Horizontal in vertical</span></span>  <br/> |<span data-ttu-id="df989-113">**visTFOKHorizontaInVertical**</span><span class="sxs-lookup"><span data-stu-id="df989-113">**visTFOKHorizontaInVertical**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="df989-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="df989-114">Remarks</span></span>

<span data-ttu-id="df989-115">Los campos de texto pueden ser de uno de los dos siguientes tipos:</span><span class="sxs-lookup"><span data-stu-id="df989-115">Text fields can be one of the following types:</span></span>
  
- <span data-ttu-id="df989-116">Estándar, que indica que el campo se insertó por su categoría.</span><span class="sxs-lookup"><span data-stu-id="df989-116">Standard, indicating that the field was inserted by field category.</span></span>
    
- <span data-ttu-id="df989-117">Horizontal en vertical, que indica que el campo es de texto horizontal sobre texto vertical.</span><span class="sxs-lookup"><span data-stu-id="df989-117">Horizontal in vertical, indicating that the field is horizontal text set within vertical text.</span></span>
    
<span data-ttu-id="df989-118">Para obtener una referencia a la celda ObjectKind por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="df989-118">To get a reference to the ObjectKind cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="df989-119">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="df989-119">Cell name:</span></span>  <br/> | <span data-ttu-id="df989-120">Fields.ObjectKind[  *i*  ] donde  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="df989-120">Fields.ObjectKind[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="df989-121">Para obtener una referencia desde un programa a la celda ObjectKind por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="df989-121">To get a reference to the ObjectKind cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="df989-122">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="df989-122">Section index:</span></span>  <br/> |<span data-ttu-id="df989-123">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="df989-123">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="df989-124">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="df989-124">Row index:</span></span>  <br/> |<span data-ttu-id="df989-125">**visRowField**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="df989-125">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="df989-126">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="df989-126">Cell index:</span></span>  <br/> |<span data-ttu-id="df989-127">**visFieldObjectKind**</span><span class="sxs-lookup"><span data-stu-id="df989-127">**visFieldObjectKind**</span></span> <br/> |
   

