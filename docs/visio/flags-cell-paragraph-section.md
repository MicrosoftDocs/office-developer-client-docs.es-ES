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
ms.openlocfilehash: b471d08556bedf68ce75595b9c211758297e8352
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822141"
---
# <a name="flags-cell-paragraph-section"></a><span data-ttu-id="cef46-103">Celda Flags (sección Párrafo)</span><span class="sxs-lookup"><span data-stu-id="cef46-103">Flags Cell (Paragraph Section)</span></span>

<span data-ttu-id="cef46-104">Indica si el texto se lee de izquierda a derecha o al revés.</span><span class="sxs-lookup"><span data-stu-id="cef46-104">Indicates whether the text direction is left to right or right to left.</span></span>
  
|<span data-ttu-id="cef46-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="cef46-105">**Value**</span></span>|<span data-ttu-id="cef46-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cef46-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cef46-107">0</span><span class="sxs-lookup"><span data-stu-id="cef46-107">0</span></span>  <br/> |<span data-ttu-id="cef46-108">El texto se lee de izquierda a derecha (predeterminado).</span><span class="sxs-lookup"><span data-stu-id="cef46-108">The text direction is left to right (the default).</span></span>  <br/> |
|<span data-ttu-id="cef46-109">1</span><span class="sxs-lookup"><span data-stu-id="cef46-109">1</span></span>  <br/> |<span data-ttu-id="cef46-110">El texto se lee de derecha a izquierda.</span><span class="sxs-lookup"><span data-stu-id="cef46-110">The text direction is right to left.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cef46-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cef46-111">Remarks</span></span>

<span data-ttu-id="cef46-112">El valor de esta celda corresponde a la opción **dirección** en la ficha de **párrafo** en el cuadro de diálogo **texto** (en la ficha **Inicio** , haga clic en la flecha de **fuente** ), que aparece únicamente si un idioma que utiliza complejas secuencias de comandos de texto ha sido se agregó en el cuadro de diálogo **Preferencias de idioma de Microsoft Office** .</span><span class="sxs-lookup"><span data-stu-id="cef46-112">The value in this cell corresponds to the **Direction** setting on the **Paragraph** tab in the **Text** dialog box (on the **Home** tab, click the **Font** arrow), which appears only if a language that uses complex scripts text has been added in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="cef46-113">(Haga clic en **Inicio**, haga clic en **Todos los programas**, haga clic en **Microsoft Office**, haga clic en **Herramientas de Microsoft Office**y, a continuación, haga clic en **Preferencias de idioma de Microsoft Office**.)</span><span class="sxs-lookup"><span data-stu-id="cef46-113">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.)</span></span> 
  
<span data-ttu-id="cef46-114">Para obtener una referencia a la celda Flags por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="cef46-114">To get a reference to the Flags cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cef46-115">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="cef46-115">Cell name:</span></span>  <br/> |<span data-ttu-id="cef46-116">Para.Flags [ *i* ] donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="cef46-116">Para.Flags[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="cef46-117">Para obtener una referencia desde un programa a la celda Flags por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="cef46-117">To get a reference to the Flags cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cef46-118">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="cef46-118">Section index:</span></span>  <br/> |<span data-ttu-id="cef46-119">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="cef46-119">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="cef46-120">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="cef46-120">Row index:</span></span>  <br/> |<span data-ttu-id="cef46-121">**visRowParagraph** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="cef46-121">**visRowParagraph** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="cef46-122">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="cef46-122">Cell index:</span></span>  <br/> |<span data-ttu-id="cef46-123">**visFlags**</span><span class="sxs-lookup"><span data-stu-id="cef46-123">**visFlags**</span></span> <br/> |
   

