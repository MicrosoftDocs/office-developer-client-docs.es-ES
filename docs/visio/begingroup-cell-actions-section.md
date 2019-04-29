---
title: Celda BeginGroup (Sección de acciones)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60022
localization_priority: Normal
ms.assetid: 1ae7f629-fb9f-1a11-1194-b381d6c9de5b
description: Indica si se inserta un separador en el menú encima de esta acción.
ms.openlocfilehash: 115dbfe051201dc3ec2b127ff129b077e1067865
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407840"
---
# <a name="begingroup-cell-actions-section"></a><span data-ttu-id="a23cb-103">Celda BeginGroup (Sección de acciones)</span><span class="sxs-lookup"><span data-stu-id="a23cb-103">BeginGroup Cell (Actions Section)</span></span>

<span data-ttu-id="a23cb-104">Indica si se inserta un separador en el menú encima de esta acción.</span><span class="sxs-lookup"><span data-stu-id="a23cb-104">Indicates whether a separator is inserted into the menu above this action.</span></span> 
  
|<span data-ttu-id="a23cb-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a23cb-105">**Value**</span></span>|<span data-ttu-id="a23cb-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a23cb-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a23cb-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="a23cb-107">TRUE</span></span>  <br/> |<span data-ttu-id="a23cb-108">Se inserta un separador en el menú encima de esta acción.</span><span class="sxs-lookup"><span data-stu-id="a23cb-108">A separator is inserted into the menu above this action.</span></span>  <br/> |
|<span data-ttu-id="a23cb-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="a23cb-109">FALSE</span></span>  <br/> |<span data-ttu-id="a23cb-110">No se inserta un separador en el menú encima de esta acción (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="a23cb-110">A separator is not inserted into the menu above this action (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a23cb-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a23cb-111">Remarks</span></span>

<span data-ttu-id="a23cb-112">Para obtener una referencia a la celda BeginGroup por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="a23cb-112">To get a reference to the BeginGroup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a23cb-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="a23cb-113">Cell name:</span></span>  <br/> |<span data-ttu-id="a23cb-114">Actividades.</span><span class="sxs-lookup"><span data-stu-id="a23cb-114">Actions.</span></span> <span data-ttu-id="a23cb-115">*nombre*. BeginGroup donde acciones.</span><span class="sxs-lookup"><span data-stu-id="a23cb-115">*name*.BeginGroup where Actions.</span></span> <span data-ttu-id="a23cb-116">*nombre* es el nombre de la fila de acciones</span><span class="sxs-lookup"><span data-stu-id="a23cb-116">*name* is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="a23cb-117">Para obtener una referencia desde un programa a la celda BeginGroup por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="a23cb-117">To get a reference to the BeginGroup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a23cb-118">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="a23cb-118">Section index:</span></span>  <br/> |<span data-ttu-id="a23cb-119">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="a23cb-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="a23cb-120">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="a23cb-120">Row index:</span></span>  <br/> |<span data-ttu-id="a23cb-121">**visRowAction** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a23cb-121">**visRowAction** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="a23cb-122">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="a23cb-122">Cell index:</span></span>  <br/> |<span data-ttu-id="a23cb-123">**visActionBeginGroup**</span><span class="sxs-lookup"><span data-stu-id="a23cb-123">**visActionBeginGroup**</span></span> <br/> |
   

