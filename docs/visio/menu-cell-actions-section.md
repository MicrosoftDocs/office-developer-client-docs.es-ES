---
title: Celda Menu (sección de acciones)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm690
localization_priority: Normal
ms.assetid: 29af746c-b081-24cf-a30d-a56353ee849e
description: Define el nombre de un elemento de menú que aparece en un menú contextual o de etiqueta de acción para una forma o una página.
ms.openlocfilehash: 195af94c4c36bb3c29a4fadab3c68f8334742952
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822680"
---
# <a name="menu-cell-actions-section"></a><span data-ttu-id="62984-103">Celda Menu (sección Acciones)</span><span class="sxs-lookup"><span data-stu-id="62984-103">Menu Cell (Actions Section)</span></span>

<span data-ttu-id="62984-104">Define el nombre de un elemento de menú que aparece en un menú contextual o de etiqueta de acción para una forma o una página.</span><span class="sxs-lookup"><span data-stu-id="62984-104">Defines the name of a menu item that appears on a shortcut or action tag menu for a shape or page.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="62984-105">En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="62984-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="62984-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62984-106">Remarks</span></span>

<span data-ttu-id="62984-p101">Para insertar un separador en el menú situado encima de este elemento, utilice la celda BeginGroup. Para mostrar el comando en la parte inferior del menú, coloque un carácter de porcentaje (%) como prefijo del nombre.</span><span class="sxs-lookup"><span data-stu-id="62984-p101">To insert a separator into the menu above this item, use the BeginGroup cell. To display the command at the bottom of the menu, prefix the name with a percent character (%) .</span></span>
  
<span data-ttu-id="62984-109">Para obtener una referencia a la celda Menu por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="62984-109">To get a reference to the Menu cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="62984-110">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="62984-110">Cell name:</span></span>  <br/> |<span data-ttu-id="62984-111">Acciones.</span><span class="sxs-lookup"><span data-stu-id="62984-111">Actions.</span></span> <span data-ttu-id="62984-112">*nombre* . Acciones de Menuwhere.</span><span class="sxs-lookup"><span data-stu-id="62984-112">*name*  .Menuwhere Actions.</span></span>  <span data-ttu-id="62984-113">*nombre* es el nombre de la fila de acciones</span><span class="sxs-lookup"><span data-stu-id="62984-113">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="62984-114">Para obtener una referencia desde un programa a la celda Menu por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="62984-114">To get a reference to the Menu cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="62984-115">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="62984-115">Section index:</span></span>  <br/> |<span data-ttu-id="62984-116">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="62984-116">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="62984-117">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="62984-117">Row index:</span></span>  <br/> |<span data-ttu-id="62984-118">**visRowAction** +  *i* donde = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="62984-118">**visRowAction** +  *i*  where i = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="62984-119">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="62984-119">Cell index:</span></span>  <br/> |<span data-ttu-id="62984-120">**visActionMenu**</span><span class="sxs-lookup"><span data-stu-id="62984-120">**visActionMenu**</span></span> <br/> |
   

