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
ms.openlocfilehash: e6bc576982cad871804cbcbc5f3d9c6bceb558c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407616"
---
# <a name="action-cell-actions-section"></a><span data-ttu-id="54095-103">Celda Action (sección de acciones)</span><span class="sxs-lookup"><span data-stu-id="54095-103">Action Cell (Actions Section)</span></span>

<span data-ttu-id="54095-104">Contiene la fórmula que se va a ejecutar cuando un usuario elige un comando en un menú contextual o de etiquetas de acción.</span><span class="sxs-lookup"><span data-stu-id="54095-104">Contains the formula to be executed when a user chooses a command on a shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="54095-105">En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="54095-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="54095-106">Comentarios</span><span class="sxs-lookup"><span data-stu-id="54095-106">Remarks</span></span>

<span data-ttu-id="54095-107">La celda Action se evalúa sólo cuando ocurre la acción, no al especificar la fórmula.</span><span class="sxs-lookup"><span data-stu-id="54095-107">An Action cell is evaluated only when the action occurs, not when the formula is entered.</span></span>
  
<span data-ttu-id="54095-108">Para obtener una referencia a la celda Action por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="54095-108">To get a reference to the the Action cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="54095-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="54095-109">Cell name:</span></span>  <br/> | <span data-ttu-id="54095-110">Actividades.</span><span class="sxs-lookup"><span data-stu-id="54095-110">Actions.</span></span>  <span data-ttu-id="54095-111">*nombre* . Acción en la que las acciones.</span><span class="sxs-lookup"><span data-stu-id="54095-111">*name*  .Action           where Actions.</span></span> <span data-ttu-id="54095-112">*nombre* es el nombre de la fila de acciones.</span><span class="sxs-lookup"><span data-stu-id="54095-112">*name*  is the name of the actions row</span></span>  <br/> |
   
<span data-ttu-id="54095-113">Para obtener una referencia a la celda Action por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="54095-113">To get a reference to thethe Action cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="54095-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="54095-114">Section index:</span></span>  <br/> |<span data-ttu-id="54095-115">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="54095-115">**visSectionAction**</span></span> <br/> |
| <span data-ttu-id="54095-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="54095-116">Row index:</span></span>  <br/> |<span data-ttu-id="54095-117">**visRowAction** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="54095-117">**visRowAction** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="54095-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="54095-118">Cell index:</span></span>  <br/> |<span data-ttu-id="54095-119">**visActionAction**</span><span class="sxs-lookup"><span data-stu-id="54095-119">**visActionAction**</span></span> <br/> |
   

