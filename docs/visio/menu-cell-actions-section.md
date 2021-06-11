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
ms.openlocfilehash: adb6915c34946472ada8c4ab4d02fa88bab6651a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436331"
---
# <a name="menu-cell-actions-section"></a><span data-ttu-id="fa7b8-103">Celda Menu (sección de acciones)</span><span class="sxs-lookup"><span data-stu-id="fa7b8-103">Menu Cell (Actions Section)</span></span>

<span data-ttu-id="fa7b8-104">Define el nombre de un elemento de menú que aparece en un menú contextual o de etiqueta de acción para una forma o una página.</span><span class="sxs-lookup"><span data-stu-id="fa7b8-104">Defines the name of a menu item that appears on a shortcut or action tag menu for a shape or page.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="fa7b8-105">En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="fa7b8-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fa7b8-106">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fa7b8-106">Remarks</span></span>

<span data-ttu-id="fa7b8-p101">Para insertar un separador en el menú situado encima de este elemento, utilice la celda BeginGroup. Para mostrar el comando en la parte inferior del menú, coloque un carácter de porcentaje (%) como prefijo del nombre.</span><span class="sxs-lookup"><span data-stu-id="fa7b8-p101">To insert a separator into the menu above this item, use the BeginGroup cell. To display the command at the bottom of the menu, prefix the name with a percent character (%) .</span></span>
  
<span data-ttu-id="fa7b8-109">Para obtener una referencia a la celda Menu por su nombre desde otra fórmula, o desde un programa mediante la **propiedad CellsU,** use:</span><span class="sxs-lookup"><span data-stu-id="fa7b8-109">To get a reference to the Menu cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fa7b8-110">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="fa7b8-110">Cell name:</span></span>  <br/> |<span data-ttu-id="fa7b8-111">Acciones.</span><span class="sxs-lookup"><span data-stu-id="fa7b8-111">Actions.</span></span> <span data-ttu-id="fa7b8-112">*nombre*  . Menuwhere Actions.</span><span class="sxs-lookup"><span data-stu-id="fa7b8-112">*name*  .Menuwhere Actions.</span></span>  <span data-ttu-id="fa7b8-113">*nombre*  es el nombre de la fila Acciones</span><span class="sxs-lookup"><span data-stu-id="fa7b8-113">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="fa7b8-114">Para obtener una referencia desde un programa a la celda Menu por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="fa7b8-114">To get a reference to the Menu cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fa7b8-115">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="fa7b8-115">Section index:</span></span>  <br/> |<span data-ttu-id="fa7b8-116">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="fa7b8-116">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="fa7b8-117">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="fa7b8-117">Row index:</span></span>  <br/> |<span data-ttu-id="fa7b8-118">**visRowAction**  +   *i* donde i = 0, 1, 2, ...</span><span class="sxs-lookup"><span data-stu-id="fa7b8-118">**visRowAction** +  *i*  where i = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="fa7b8-119">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="fa7b8-119">Cell index:</span></span>  <br/> |<span data-ttu-id="fa7b8-120">**visActionMenu**</span><span class="sxs-lookup"><span data-stu-id="fa7b8-120">**visActionMenu**</span></span> <br/> |
   

