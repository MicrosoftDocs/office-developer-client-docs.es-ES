---
title: Celda Description (sección de etiquetas de acción)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60037
localization_priority: Normal
ms.assetid: feb29b91-0f6e-6353-3dd0-7a280843a517
description: Contiene una cadena que describe la etiqueta de acción, que aparece como información sobre herramientas cuando los usuarios sitúan el puntero sobre la etiqueta.
ms.openlocfilehash: 3c365d24170f912624a2abdeeadd75140bea9a85
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821977"
---
# <a name="description-cell-action-tags-section"></a><span data-ttu-id="5d16e-103">Celda Description (sección de etiquetas de acción)</span><span class="sxs-lookup"><span data-stu-id="5d16e-103">Description Cell (Action Tags Section)</span></span>

<span data-ttu-id="5d16e-104">Contiene una cadena que describe la etiqueta de acción, que aparece como información sobre herramientas cuando los usuarios sitúan el puntero sobre la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="5d16e-104">Contains a string that describes the action tag, which appears as a tool tip when users place their pointer over the tag.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5d16e-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5d16e-105">Remarks</span></span>

<span data-ttu-id="5d16e-106">Para obtener una referencia a la celda Description por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="5d16e-106">To get a reference to the Description cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5d16e-107">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="5d16e-107">Cell name:</span></span>  <br/> | <span data-ttu-id="5d16e-108">Etiquetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="5d16e-108">SmartTags.</span></span>  <span data-ttu-id="5d16e-109">*nombre* . Descripción donde SmartTags.</span><span class="sxs-lookup"><span data-stu-id="5d16e-109">*name*  .Description           where SmartTags.</span></span> <span data-ttu-id="5d16e-110">*nombre* es el nombre de la fila de etiquetas de acción</span><span class="sxs-lookup"><span data-stu-id="5d16e-110">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="5d16e-111">Para obtener una referencia a la celda Description por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="5d16e-111">To get a reference to the Description cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5d16e-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="5d16e-112">Section index:</span></span>  <br/> |<span data-ttu-id="5d16e-113">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="5d16e-113">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="5d16e-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="5d16e-114">Row index:</span></span>  <br/> |<span data-ttu-id="5d16e-115">**visRowSmartTag** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="5d16e-115">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="5d16e-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="5d16e-116">Cell index:</span></span>  <br/> |<span data-ttu-id="5d16e-117">**visSmartTagDescription**</span><span class="sxs-lookup"><span data-stu-id="5d16e-117">**visSmartTagDescription**</span></span> <br/> |
   

