---
title: Celda LockCustProp (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60055
localization_priority: Normal
ms.assetid: d1c23f1d-485d-a897-594d-15d6e8d0fb3c
description: Determina si el usuario puede agregar, eliminar o modificar datos de formas en la interfaz de usuario con el cuadro de diálogo Definir datos de formas o con el menú contextual de la ventana Datos de formas.
ms.openlocfilehash: 001123f3bd08d35f6f8e4874e20f2ee073835494
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359609"
---
# <a name="lockcustprop-cell-protection-section"></a><span data-ttu-id="52de8-103">Celda LockCustProp (Sección de protección)</span><span class="sxs-lookup"><span data-stu-id="52de8-103">LockCustProp Cell (Protection Section)</span></span>

<span data-ttu-id="52de8-104">Determina si el usuario puede agregar, eliminar o modificar datos de formas en la interfaz de usuario con el cuadro de diálogo **Definir datos de formas** o con el menú contextual de la ventana **Datos de formas**.</span><span class="sxs-lookup"><span data-stu-id="52de8-104">Determines whether the user can add, delete, or modify shape data in the user interface (UI) by using the **Define Shape Data** dialog box or the shortcut menu for the **Shape Data** window.</span></span> 
  
|<span data-ttu-id="52de8-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="52de8-105">**Value**</span></span>|<span data-ttu-id="52de8-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="52de8-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="52de8-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="52de8-107">TRUE</span></span>  <br/> |<span data-ttu-id="52de8-108">El comando **Definir datos de formas** del menú contextual de la ventana **Datos de formas** está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="52de8-108">The **Define Shape Data** command on the shortcut menu in the **Shape Data** window is disabled.</span></span>  <br/> |
|<span data-ttu-id="52de8-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="52de8-109">FALSE</span></span>  <br/> |<span data-ttu-id="52de8-110">El comando **Definir datos de formas** del menú contextual de la ventana **Datos de formas** está habilitado (de forma predeterminada).</span><span class="sxs-lookup"><span data-stu-id="52de8-110">The **Define Shape Data** command on the shortcut menu in the **Shape Data** window is enabled (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52de8-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="52de8-111">Remarks</span></span>

<span data-ttu-id="52de8-112">El valor TRUE no impide al usuario cambiar el valor de un elemento de datos de formas ni cambiar la sección de datos de formas de la ventana ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="52de8-112">A value of TRUE does not prevent a user from changing the value of a shape data item or changing the Shape Data section in the ShapeSheet window.</span></span> 
  
<span data-ttu-id="52de8-113">Para obtener una referencia a la celda LockCustProp por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="52de8-113">To get a reference to the LockCustProp cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="52de8-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="52de8-114">Cell name:</span></span>  <br/> |<span data-ttu-id="52de8-115">LockCustProp</span><span class="sxs-lookup"><span data-stu-id="52de8-115">LockCustProp</span></span>  <br/> |
   
<span data-ttu-id="52de8-116">Para obtener una referencia desde un programa a la celda LockCustProp por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="52de8-116">To get a reference to the LockCustProp cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="52de8-117">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="52de8-117">Section index:</span></span>  <br/> |<span data-ttu-id="52de8-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="52de8-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="52de8-119">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="52de8-119">Row index:</span></span>  <br/> |<span data-ttu-id="52de8-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="52de8-120">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="52de8-121">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="52de8-121">Cell index:</span></span>  <br/> |<span data-ttu-id="52de8-122">**visLockCustProp**</span><span class="sxs-lookup"><span data-stu-id="52de8-122">**visLockCustProp**</span></span> <br/> |
   

