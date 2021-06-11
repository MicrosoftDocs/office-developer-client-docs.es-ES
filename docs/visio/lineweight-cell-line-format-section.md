---
title: Celda LineWeight (Sección de formato de línea)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm585
localization_priority: Normal
ms.assetid: 16b0e293-eeef-34b4-aeb0-4472815dd543
description: Determina el grosor de línea de una forma. Para establecer el grosor de línea, escriba un número con una unidad de medida válida.
ms.openlocfilehash: 654a93f939226bedab2e40ab591dad0e3f872267
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412250"
---
# <a name="lineweight-cell-line-format-section"></a><span data-ttu-id="08732-104">Celda LineWeight (Sección de formato de línea)</span><span class="sxs-lookup"><span data-stu-id="08732-104">LineWeight Cell (Line Format Section)</span></span>

<span data-ttu-id="08732-p102">Determina el grosor de línea de una forma. Para establecer el grosor de línea, escriba un número con una unidad de medida válida.</span><span class="sxs-lookup"><span data-stu-id="08732-p102">Determines the line weight of a shape. Set the line weight by entering a number with a valid unit of measure.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="08732-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="08732-107">Remarks</span></span>

<span data-ttu-id="08732-108">También puede establecer este valor de LineWeight en el cuadro de diálogo **Línea** (haga clic en la pestaña **Inicio** del grupo **Forma**, haga clic en **Línea**, vaya a **Grosor** y, a continuación, haga clic en **Más líneas**).</span><span class="sxs-lookup"><span data-stu-id="08732-108">You can also set the value of LineWeight in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="08732-109">Si no se especifica la unidad de medida, se usa la unidad de medida del  texto especificado en el cuadro de diálogo Opciones de **Visio** (haga clic en la pestaña Archivo y, a continuación, haga clic en **Opciones**).</span><span class="sxs-lookup"><span data-stu-id="08732-109">If the unit of measure is not entered, the unit of measure for text specified in the **Visio Options** dialog box is used (click the **File** tab, and then click **Options**).</span></span> <span data-ttu-id="08732-110">El grosor de línea no depende de la escala del dibujo.</span><span class="sxs-lookup"><span data-stu-id="08732-110">Line weight is independent of the scale of the drawing.</span></span> <span data-ttu-id="08732-111">Si se cambia la escala del dibujo, el grosor de línea permanece igual.</span><span class="sxs-lookup"><span data-stu-id="08732-111">If the drawing is scaled, the line weight remains the same.</span></span> 
  
<span data-ttu-id="08732-112">Para obtener una referencia a la celda LineWeight por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="08732-112">To get a reference to the LineWeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="08732-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="08732-113">Cell name:</span></span>  <br/> | <span data-ttu-id="08732-114">LineWeight</span><span class="sxs-lookup"><span data-stu-id="08732-114">LineWeight</span></span>  <br/> |
   
<span data-ttu-id="08732-115">Para obtener una referencia desde un programa a la celda LineWeight por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="08732-115">To get a reference to the LineWeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="08732-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="08732-116">Section index:</span></span>  <br/> |<span data-ttu-id="08732-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="08732-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="08732-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="08732-118">Row index:</span></span>  <br/> |<span data-ttu-id="08732-119">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="08732-119">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="08732-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="08732-120">Cell index:</span></span>  <br/> |<span data-ttu-id="08732-121">**visLineWeight**</span><span class="sxs-lookup"><span data-stu-id="08732-121">**visLineWeight**</span></span> <br/> |
   

