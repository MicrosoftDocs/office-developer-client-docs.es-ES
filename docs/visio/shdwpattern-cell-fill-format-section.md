---
title: Celda ShdwPattern (Sección de formato de relleno)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm935
localization_priority: Normal
ms.assetid: eca73b80-9835-9011-1dce-187ccee92e76
description: Determina la trama de relleno para la sombra de una forma.
ms.openlocfilehash: c2591fbc9f208b1bf9c7d0c85e6de765cd9825f6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349045"
---
# <a name="shdwpattern-cell-fill-format-section"></a><span data-ttu-id="cd745-103">Celda ShdwPattern (Sección de formato de relleno)</span><span class="sxs-lookup"><span data-stu-id="cd745-103">ShdwPattern Cell (Fill Format Section)</span></span>

<span data-ttu-id="cd745-104">Determina la trama de relleno para la sombra de una forma.</span><span class="sxs-lookup"><span data-stu-id="cd745-104">Determines the fill pattern for a shape's shadow.</span></span>
  
|<span data-ttu-id="cd745-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="cd745-105">**Value**</span></span>|<span data-ttu-id="cd745-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cd745-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd745-107">comprendi</span><span class="sxs-lookup"><span data-stu-id="cd745-107">0</span></span>  <br/> |<span data-ttu-id="cd745-108">Ninguno (relleno transparente)</span><span class="sxs-lookup"><span data-stu-id="cd745-108">None (transparent fill)</span></span>  <br/> |
|<span data-ttu-id="cd745-109">1</span><span class="sxs-lookup"><span data-stu-id="cd745-109">1</span></span>  <br/> |<span data-ttu-id="cd745-110">Color de primer plano sólido</span><span class="sxs-lookup"><span data-stu-id="cd745-110">Solid foreground color</span></span>  <br/> |
|<span data-ttu-id="cd745-111">2 -40</span><span class="sxs-lookup"><span data-stu-id="cd745-111">2 - 40</span></span>  <br/> |<span data-ttu-id="cd745-112">Varias tramas</span><span class="sxs-lookup"><span data-stu-id="cd745-112">Assorted patterns</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd745-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cd745-113">Remarks</span></span>

<span data-ttu-id="cd745-p101">Para establecer la trama de relleno, escriba un número entre 0 y 40, que corresponde al índice de la colección de tramas. También puede ver la colección de tramas de relleno en el cuadro de diálogo **Relleno** (en la ficha **Inicio**, en el grupo **Forma**, haga clic en **Relleno** y, a continuación, en **Opciones de relleno**).</span><span class="sxs-lookup"><span data-stu-id="cd745-p101">To set the fill pattern, enter a number from 0 to 40, which is an index into a collection of patterns. You can view the fill pattern collection in the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill**, and then click **Fill Options**).</span></span>
  
<span data-ttu-id="cd745-116">Para obtener una referencia a la celda ShdwPattern por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="cd745-116">To get a reference to the ShdwPattern cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cd745-117">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="cd745-117">Cell name:</span></span>  <br/> |<span data-ttu-id="cd745-118">ShdwPattern</span><span class="sxs-lookup"><span data-stu-id="cd745-118">ShdwPattern</span></span>  <br/> |
   
<span data-ttu-id="cd745-119">Para obtener una referencia desde un programa a la celda ShdwPattern por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="cd745-119">To get a reference to the ShdwPattern cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cd745-120">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="cd745-120">Section index:</span></span>  <br/> |<span data-ttu-id="cd745-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cd745-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="cd745-122">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="cd745-122">Row index:</span></span>  <br/> |<span data-ttu-id="cd745-123">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="cd745-123">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="cd745-124">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="cd745-124">Cell index:</span></span>  <br/> |<span data-ttu-id="cd745-125">**visFillShdwPattern**</span><span class="sxs-lookup"><span data-stu-id="cd745-125">**visFillShdwPattern**</span></span> <br/> |
   

