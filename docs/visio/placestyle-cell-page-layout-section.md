---
title: Celda PlaceStyle (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7dcd5a35-bd3d-447f-e4aa-986091d129de
description: Determina cómo se colocan las formas en la página cuando el usuario las diseña mediante el cuadro de diálogo Configurar diseño (en la ficha Diseño, en el grupo Diseño, haga clic en Redistribuir página y, a continuación, en Más opciones de diseño).
ms.openlocfilehash: 251bee427c732fe782c85c4991df07a1deb2a4dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822753"
---
# <a name="placestyle-cell-page-layout-section"></a><span data-ttu-id="6e672-103">Celda PlaceStyle (sección Diseño de página)</span><span class="sxs-lookup"><span data-stu-id="6e672-103">PlaceStyle Cell (Page Layout Section)</span></span>

<span data-ttu-id="6e672-104">Determina cómo se colocan las formas en la página cuando el usuario las diseña mediante el cuadro de diálogo **Configurar diseño** (en la ficha **Diseño**, en el grupo **Diseño**, haga clic en **Redistribuir página** y, a continuación, en **Más opciones de diseño**).</span><span class="sxs-lookup"><span data-stu-id="6e672-104">Determines how shapes are placed on the page when you are laying out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6e672-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6e672-105">Remarks</span></span>

<span data-ttu-id="6e672-106">También puede establecer el valor de esta celda en el cuadro de diálogo **Configurar diseño**.</span><span class="sxs-lookup"><span data-stu-id="6e672-106">You can also set the value of this cell in the **Configure Layout** dialog box.</span></span> 
  
<span data-ttu-id="6e672-107">Para obtener una referencia a la celda PlaceStyle por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="6e672-107">To get a reference to the PlaceStyle cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6e672-108">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="6e672-108">Cell name:</span></span>  <br/> |<span data-ttu-id="6e672-109">PlaceStyle</span><span class="sxs-lookup"><span data-stu-id="6e672-109">PlaceStyle</span></span>  <br/> |
   
<span data-ttu-id="6e672-110">Para obtener una referencia desde un programa a la celda PlaceStyle por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="6e672-110">To get a reference to the PlaceStyle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6e672-111">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="6e672-111">Section index:</span></span>  <br/> |<span data-ttu-id="6e672-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6e672-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="6e672-113">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="6e672-113">Row index:</span></span>  <br/> |<span data-ttu-id="6e672-114">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="6e672-114">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="6e672-115">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="6e672-115">Cell index:</span></span>  <br/> |<span data-ttu-id="6e672-116">**visPLOPlaceStyle**</span><span class="sxs-lookup"><span data-stu-id="6e672-116">**visPLOPlaceStyle**</span></span> <br/> |
   

