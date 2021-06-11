---
title: Celda Value (Sección de campos de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1095
localization_priority: Normal
ms.assetid: 3ca662c8-1ce4-89a9-3264-1ba533fcd444
description: Contiene la función de un campo.
ms.openlocfilehash: d5a09dd0d59341125db897484f74addff22328de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430948"
---
# <a name="value-cell-text-fields-section"></a><span data-ttu-id="b3ed9-103">Celda Value (Sección de campos de texto)</span><span class="sxs-lookup"><span data-stu-id="b3ed9-103">Value Cell (Text Fields Section)</span></span>

<span data-ttu-id="b3ed9-104">Contiene la función de un campo.</span><span class="sxs-lookup"><span data-stu-id="b3ed9-104">Contains the function for a field.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b3ed9-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b3ed9-105">Remarks</span></span>

<span data-ttu-id="b3ed9-106">Puede establecer el valor de esta celda mediante el cuadro de diálogo **Campo** (en la ficha **Insertar**, en el grupo **Texto**, haga clic en **Campo**).</span><span class="sxs-lookup"><span data-stu-id="b3ed9-106">You can set the value of this cell using the **Field** dialog box (on the **Insert** tab, in the **Text** group, click **Field**).</span></span>
  
<span data-ttu-id="b3ed9-107">Para obtener una referencia a la celda Value por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="b3ed9-107">To get a reference to the Value cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b3ed9-108">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="b3ed9-108">Cell name:</span></span>  <br/> |<span data-ttu-id="b3ed9-109">Fields.Value[ *i*  ] donde  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="b3ed9-109">Fields.Value[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="b3ed9-110">Para obtener una referencia desde un programa a la celda Value por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="b3ed9-110">To get a reference to the Value cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b3ed9-111">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="b3ed9-111">Section index:</span></span>  <br/> |<span data-ttu-id="b3ed9-112">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="b3ed9-112">**visSectionTextField**</span></span> <br/> |
|<span data-ttu-id="b3ed9-113">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="b3ed9-113">Row index:</span></span>  <br/> |<span data-ttu-id="b3ed9-114">**visRowField**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b3ed9-114">**visRowField** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="b3ed9-115">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="b3ed9-115">Cell index:</span></span>  <br/> |<span data-ttu-id="b3ed9-116">**visFieldCell**</span><span class="sxs-lookup"><span data-stu-id="b3ed9-116">**visFieldCell**</span></span> <br/> |
   

