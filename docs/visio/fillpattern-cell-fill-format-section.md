---
title: Celda FillPattern (Sección de formato de relleno)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm375
localization_priority: Normal
ms.assetid: dac82a4f-4508-541a-e118-7d79df987232
description: Determina la trama de relleno para la forma. Para especificar una trama de relleno personalizada, utilice la función USE en esta celda.
ms.openlocfilehash: 26429e06ad432eaf7fae9188ac676cb4be3201c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822142"
---
# <a name="fillpattern-cell-fill-format-section"></a><span data-ttu-id="87448-104">Celda FillPattern (sección Formato de relleno)</span><span class="sxs-lookup"><span data-stu-id="87448-104">FillPattern Cell (Fill Format Section)</span></span>

<span data-ttu-id="87448-p102">Determina la trama de relleno para la forma. Para especificar una trama de relleno personalizada, utilice la función USE en esta celda.</span><span class="sxs-lookup"><span data-stu-id="87448-p102">Determines the fill pattern for the shape. To specify a custom fill pattern, use the USE function in this cell.</span></span>
  
|<span data-ttu-id="87448-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="87448-107">**Value**</span></span>|<span data-ttu-id="87448-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="87448-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="87448-109">0</span><span class="sxs-lookup"><span data-stu-id="87448-109">0</span></span>  <br/> |<span data-ttu-id="87448-110">Ninguno (relleno transparente).</span><span class="sxs-lookup"><span data-stu-id="87448-110">None (transparent fill).</span></span>  <br/> |
|<span data-ttu-id="87448-111">1</span><span class="sxs-lookup"><span data-stu-id="87448-111">1</span></span>  <br/> |<span data-ttu-id="87448-112">Color de primer plano sólido.</span><span class="sxs-lookup"><span data-stu-id="87448-112">Solid foreground color.</span></span>  <br/> |
|<span data-ttu-id="87448-113">2 - 40</span><span class="sxs-lookup"><span data-stu-id="87448-113">2 - 40</span></span>  <br/> |<span data-ttu-id="87448-114">Varias tramas de relleno que se corresponden con entradas de índice en el cuadro de diálogo **Relleno**.</span><span class="sxs-lookup"><span data-stu-id="87448-114">Assorted fill patterns that correspond to indexed entries in the **Fill** dialog box.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="87448-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="87448-115">Remarks</span></span>

<span data-ttu-id="87448-116">También puede establecer este valor mediante el cuadro de diálogo **Relleno** (en la ficha **Inicio**, en el grupo **Forma**, haga clic en **Relleno** y, a continuación, en **Opciones de relleno**).</span><span class="sxs-lookup"><span data-stu-id="87448-116">You can also set this value using the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill** and then click **Fill Options**).</span></span>
  
<span data-ttu-id="87448-117">Para obtener una referencia a la celda FillPattern por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="87448-117">To get a reference to the FillPattern cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="87448-118">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="87448-118">Cell name:</span></span>  <br/> |<span data-ttu-id="87448-119">FillPattern</span><span class="sxs-lookup"><span data-stu-id="87448-119">FillPattern</span></span>  <br/> |
   
<span data-ttu-id="87448-120">Para obtener una referencia desde un programa a la celda FillPattern por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="87448-120">To get a reference to the FillPattern cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="87448-121">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="87448-121">Section index:</span></span>  <br/> |<span data-ttu-id="87448-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="87448-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="87448-123">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="87448-123">Row index:</span></span>  <br/> |<span data-ttu-id="87448-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="87448-124">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="87448-125">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="87448-125">Cell index:</span></span>  <br/> |<span data-ttu-id="87448-126">**visFillPattern**</span><span class="sxs-lookup"><span data-stu-id="87448-126">**visFillPattern**</span></span> <br/> |
   

