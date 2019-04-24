---
title: Celda Bullet (Sección de párrafo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm130
localization_priority: Normal
ms.assetid: 124a5ee1-6dd1-d17d-6f0e-dbaa5d95d9cd
description: Determina el estilo de viñetas.
ms.openlocfilehash: 03b7d046cd42458b614313c19b2100259730539c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338209"
---
# <a name="bullet-cell-paragraph-section"></a><span data-ttu-id="cc7fe-103">Celda Bullet (Sección de párrafo)</span><span class="sxs-lookup"><span data-stu-id="cc7fe-103">Bullet Cell (Paragraph Section)</span></span>

<span data-ttu-id="cc7fe-104">Determina el estilo de viñetas.</span><span class="sxs-lookup"><span data-stu-id="cc7fe-104">Determines the bullet style.</span></span>
  
|<span data-ttu-id="cc7fe-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="cc7fe-105">**Value**</span></span>|<span data-ttu-id="cc7fe-106">**Estilo de viñetas**</span><span class="sxs-lookup"><span data-stu-id="cc7fe-106">**Bullet style**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cc7fe-107">comprendi</span><span class="sxs-lookup"><span data-stu-id="cc7fe-107">0</span></span>  <br/> |<span data-ttu-id="cc7fe-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="cc7fe-108">None</span></span>  <br/> |
|<span data-ttu-id="cc7fe-109">1</span><span class="sxs-lookup"><span data-stu-id="cc7fe-109">1</span></span>  <br/> |![](media/IC_Bullet1_ZA07645847.gif)           <br/> |
|<span data-ttu-id="cc7fe-110">segundo</span><span class="sxs-lookup"><span data-stu-id="cc7fe-110">2</span></span>  <br/> |![](media/IC_Bullet2_ZA07645848.gif)           <br/> |
|<span data-ttu-id="cc7fe-111">3</span><span class="sxs-lookup"><span data-stu-id="cc7fe-111">3</span></span>  <br/> |![](media/IC_Bullet3_ZA07645849.gif)           <br/> |
|<span data-ttu-id="cc7fe-112">4</span><span class="sxs-lookup"><span data-stu-id="cc7fe-112">4</span></span>  <br/> |![](media/IC_Bullet4_ZA07645851.gif)           <br/> |
|<span data-ttu-id="cc7fe-113">2,5</span><span class="sxs-lookup"><span data-stu-id="cc7fe-113">5</span></span>  <br/> |![](media/IC_Bullet5_ZA07645852.gif)           <br/> |
|<span data-ttu-id="cc7fe-114">6,5</span><span class="sxs-lookup"><span data-stu-id="cc7fe-114">6</span></span>  <br/> |![](media/IC_Bullet6_ZA07645853.gif)           <br/> |
|<span data-ttu-id="cc7fe-115">0,7</span><span class="sxs-lookup"><span data-stu-id="cc7fe-115">7</span></span>  <br/> |![](media/IC_Bullet7_ZA07645854.gif)           <br/> |
   
|||
|:-----|:-----|
|<span data-ttu-id="cc7fe-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="cc7fe-116">Section index:</span></span>  <br/> |<span data-ttu-id="cc7fe-117">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="cc7fe-117">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="cc7fe-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="cc7fe-118">Row index:</span></span>  <br/> |<span data-ttu-id="cc7fe-119">**visRowParagraph** +  *i* donde *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="cc7fe-119">**visRowParagraph** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="cc7fe-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="cc7fe-120">Cell index:</span></span>  <br/> |<span data-ttu-id="cc7fe-121">**visBulletIndex**</span><span class="sxs-lookup"><span data-stu-id="cc7fe-121">**visBulletIndex**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cc7fe-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cc7fe-122">Remarks</span></span>

<span data-ttu-id="cc7fe-123">Asimismo, para establecer el valor de esta celda, haga clic con el botón secundario en una forma, elija **Formato**, haga clic en **Texto** y, a continuación, haga clic en la pestaña **Viñetas**.</span><span class="sxs-lookup"><span data-stu-id="cc7fe-123">You can also set the value of this cell by right-clicking a shape, pointing to **Format**, clicking **Text**, and then clicking the **Bullets** tab.</span></span> 
  
<span data-ttu-id="cc7fe-124">Para obtener una referencia a la celda Bullet por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="cc7fe-124">To get a reference to the Bullet cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cc7fe-125">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="cc7fe-125">Cell name:</span></span>  <br/> |<span data-ttu-id="cc7fe-126">Para. Bullet [ *i* ] donde *i* = <1>, 2, 3,...</span><span class="sxs-lookup"><span data-stu-id="cc7fe-126">Para.Bullet[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="cc7fe-127">Para obtener una referencia a la celda Bullet por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="cc7fe-127">To get a reference to the Bullet cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  

