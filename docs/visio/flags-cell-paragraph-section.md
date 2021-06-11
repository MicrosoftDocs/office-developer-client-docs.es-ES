---
title: Celda Flags (Sección de párrafo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033782
localization_priority: Normal
ms.assetid: 898bf89d-d00f-9769-a89d-787ef708eca5
description: Indica si el texto se lee de izquierda a derecha o al revés.
ms.openlocfilehash: af1e79b13d3d8bab2e7271eb79e68cf931871806
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413118"
---
# <a name="flags-cell-paragraph-section"></a><span data-ttu-id="abf02-103">Celda Flags (Sección de párrafo)</span><span class="sxs-lookup"><span data-stu-id="abf02-103">Flags Cell (Paragraph Section)</span></span>

<span data-ttu-id="abf02-104">Indica si el texto se lee de izquierda a derecha o al revés.</span><span class="sxs-lookup"><span data-stu-id="abf02-104">Indicates whether the text direction is left to right or right to left.</span></span>
  
|<span data-ttu-id="abf02-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="abf02-105">**Value**</span></span>|<span data-ttu-id="abf02-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="abf02-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="abf02-107">0</span><span class="sxs-lookup"><span data-stu-id="abf02-107">0</span></span>  <br/> |<span data-ttu-id="abf02-108">El texto se lee de izquierda a derecha (predeterminado).</span><span class="sxs-lookup"><span data-stu-id="abf02-108">The text direction is left to right (the default).</span></span>  <br/> |
|<span data-ttu-id="abf02-109">1</span><span class="sxs-lookup"><span data-stu-id="abf02-109">1</span></span>  <br/> |<span data-ttu-id="abf02-110">El texto se lee de derecha a izquierda.</span><span class="sxs-lookup"><span data-stu-id="abf02-110">The text direction is right to left.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="abf02-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="abf02-111">Remarks</span></span>

<span data-ttu-id="abf02-112">El valor de esta celda  corresponde a  la configuración  Dirección de la  ficha Párrafo del cuadro de diálogo Texto (en la ficha Inicio, haga clic en la flecha Fuente), que solo aparece si se ha agregado un idioma que usa texto de scripts complejos en el cuadro de diálogo Preferencias de idioma de **Microsoft Office.** </span><span class="sxs-lookup"><span data-stu-id="abf02-112">The value in this cell corresponds to the **Direction** setting on the **Paragraph** tab in the **Text** dialog box (on the **Home** tab, click the **Font** arrow), which appears only if a language that uses complex scripts text has been added in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="abf02-113">(Haga clic **en Inicio**, **en Todos** los programas, haga clic en **Microsoft Office**, haga clic en **Microsoft Office Herramientas** y, a continuación, haga clic **Microsoft Office Preferencias de idioma**.)</span><span class="sxs-lookup"><span data-stu-id="abf02-113">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.)</span></span> 
  
<span data-ttu-id="abf02-114">Para obtener una referencia a la celda Flags por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="abf02-114">To get a reference to the Flags cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="abf02-115">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="abf02-115">Cell name:</span></span>  <br/> |<span data-ttu-id="abf02-116">Para.Flags[ *i*  ] donde  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="abf02-116">Para.Flags[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="abf02-117">Para obtener una referencia desde un programa a la celda Flags por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="abf02-117">To get a reference to the Flags cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="abf02-118">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="abf02-118">Section index:</span></span>  <br/> |<span data-ttu-id="abf02-119">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="abf02-119">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="abf02-120">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="abf02-120">Row index:</span></span>  <br/> |<span data-ttu-id="abf02-121">**visRowParagraph**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="abf02-121">**visRowParagraph** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="abf02-122">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="abf02-122">Cell index:</span></span>  <br/> |<span data-ttu-id="abf02-123">**visFlags**</span><span class="sxs-lookup"><span data-stu-id="abf02-123">**visFlags**</span></span> <br/> |
   

