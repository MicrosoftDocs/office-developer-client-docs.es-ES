---
title: Celda Action (sección de acciones)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm5
localization_priority: Normal
ms.assetid: 435e49ee-0b51-8ce3-0589-3f0717026f4a
description: Contiene la fórmula que se va a ejecutar cuando un usuario elige un comando en un menú contextual o de etiquetas de acción.
ms.openlocfilehash: 123b05f9a08c4ffa656e08a51f019f888cf83ed4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821504"
---
# <a name="action-cell-actions-section"></a><span data-ttu-id="76262-103">Celda Action (sección de acciones)</span><span class="sxs-lookup"><span data-stu-id="76262-103">Action Cell (Actions Section)</span></span>

<span data-ttu-id="76262-104">Contiene la fórmula que se va a ejecutar cuando un usuario elige un comando en un menú contextual o de etiquetas de acción.</span><span class="sxs-lookup"><span data-stu-id="76262-104">Contains the formula to be executed when a user chooses a command on a shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="76262-105">En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="76262-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="76262-106">Comentarios</span><span class="sxs-lookup"><span data-stu-id="76262-106">Remarks</span></span>

<span data-ttu-id="76262-107">La celda Action se evalúa sólo cuando ocurre la acción, no al especificar la fórmula.</span><span class="sxs-lookup"><span data-stu-id="76262-107">An Action cell is evaluated only when the action occurs, not when the formula is entered.</span></span>
  
<span data-ttu-id="76262-108">Para obtener una referencia a la celda Action por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="76262-108">To get a reference to the the Action cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="76262-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="76262-109">Cell name:</span></span>  <br/> | <span data-ttu-id="76262-110">Acciones.</span><span class="sxs-lookup"><span data-stu-id="76262-110">Actions.</span></span>  <span data-ttu-id="76262-111">*nombre* . Acción donde acciones.</span><span class="sxs-lookup"><span data-stu-id="76262-111">*name*  .Action           where Actions.</span></span> <span data-ttu-id="76262-112">*nombre* es el nombre de la fila de acciones</span><span class="sxs-lookup"><span data-stu-id="76262-112">*name*  is the name of the actions row</span></span>  <br/> |
   
<span data-ttu-id="76262-113">Para obtener una referencia a la celda Action por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="76262-113">To get a reference to thethe Action cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="76262-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="76262-114">Section index:</span></span>  <br/> |<span data-ttu-id="76262-115">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="76262-115">**visSectionAction**</span></span> <br/> |
| <span data-ttu-id="76262-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="76262-116">Row index:</span></span>  <br/> |<span data-ttu-id="76262-117">**visRowAction** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="76262-117">**visRowAction** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="76262-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="76262-118">Cell index:</span></span>  <br/> |<span data-ttu-id="76262-119">**visActionAction**</span><span class="sxs-lookup"><span data-stu-id="76262-119">**visActionAction**</span></span> <br/> |
   

