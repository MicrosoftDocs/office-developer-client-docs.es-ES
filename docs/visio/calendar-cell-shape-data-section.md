---
title: Celda Calendar (Sección de datos de formas)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60027
localization_priority: Normal
ms.assetid: f5dcc6d9-474a-9ecb-21f5-56415d934890
description: Determina el calendario que se usa para los datos de la forma cuando el tipo de datos es fecha.
ms.openlocfilehash: 2ddbd578053e2ae37514194450bd95dc9cdf441d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337509"
---
# <a name="calendar-cell-shape-data-section"></a><span data-ttu-id="e16c0-103">Celda Calendar (Sección de datos de formas)</span><span class="sxs-lookup"><span data-stu-id="e16c0-103">Calendar Cell (Shape Data Section)</span></span>

<span data-ttu-id="e16c0-104">Determina el calendario que se usa para los datos de la forma cuando el tipo de datos es fecha.</span><span class="sxs-lookup"><span data-stu-id="e16c0-104">Determines the calendar that is used for shape data when the data type is Date.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e16c0-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e16c0-105">Remarks</span></span>

<span data-ttu-id="e16c0-106">Los valores posibles son: 0 (Occidental), 1 (Hijri árabe), 2 (Hebreo lunar), 3 (Calendario de Taiwán), 4 (Japonés imperial), 5 (Budista tailandés), 6 (Danki coreano), 7 (Saka), 8 (Transliteración al inglés) y 9 (Transliteración al francés).</span><span class="sxs-lookup"><span data-stu-id="e16c0-106">The possible values are: 0 (Western), 1 (Arabic Hijri), 2 (Hebrew Lunar), 3 (Taiwan Calendar), 4 (Japanese Emperor Reign), 5 (Thai Buddhist), 6 (Korean Danki), 7 (Saka Era), 8 (English transliterated), and 9 (French transliterated ).</span></span> 
  
<span data-ttu-id="e16c0-107">Para obtener una referencia a la celda Calendar por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="e16c0-107">To get a reference to the Calendar cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e16c0-108">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="e16c0-108">Cell name:</span></span>  <br/> | <span data-ttu-id="e16c0-109">Polyprop.  *nombre* . Calendario donde prop.  *Name* es el nombre de la fila</span><span class="sxs-lookup"><span data-stu-id="e16c0-109">Prop.  *name*  .Calendar            where Prop.  *name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="e16c0-110">Para obtener una referencia desde un programa a la celda Calendar por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="e16c0-110">To get a reference to the Calendar cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e16c0-111">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="e16c0-111">Section index:</span></span>  <br/> |<span data-ttu-id="e16c0-112">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="e16c0-112">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="e16c0-113">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="e16c0-113">Row index:</span></span>  <br/> |<span data-ttu-id="e16c0-114">**visRowProp** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e16c0-114">**visRowProp** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="e16c0-115">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="e16c0-115">Cell index:</span></span>  <br/> |<span data-ttu-id="e16c0-116">**visCustPropsCalendar**</span><span class="sxs-lookup"><span data-stu-id="e16c0-116">**visCustPropsCalendar**</span></span> <br/> |
   

