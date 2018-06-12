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
description: Determina si el usuario puede agregar, eliminar o modificar datos de formas en la interfaz de usuario (UI) mediante el cuadro de diálogo Definir datos de formas o en el menú contextual de la ventana datos de formas.
ms.openlocfilehash: a88da9e4973f819b398b5bdeda434ede14640797
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822506"
---
# <a name="lockcustprop-cell-protection-section"></a><span data-ttu-id="4fc4b-103">Celda LockCustProp (Sección de protección)</span><span class="sxs-lookup"><span data-stu-id="4fc4b-103">LockCustProp Cell (Protection Section)</span></span>

<span data-ttu-id="4fc4b-104">Determina si el usuario puede agregar, eliminar o modificar datos de formas en la interfaz de usuario (UI) mediante el cuadro de diálogo **Definir datos de formas** o en el menú contextual de la ventana **Datos de formas** .</span><span class="sxs-lookup"><span data-stu-id="4fc4b-104">Determines whether the user can add, delete, or modify shape data in the user interface (UI) by using the **Define Shape Data** dialog box or the shortcut menu for the **Shape Data** window.</span></span> 
  
|<span data-ttu-id="4fc4b-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="4fc4b-105">**Value**</span></span>|<span data-ttu-id="4fc4b-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4fc4b-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4fc4b-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="4fc4b-107">TRUE</span></span>  <br/> |<span data-ttu-id="4fc4b-108">El comando **Definir datos de formas** en el menú contextual en la ventana **Datos de formas** está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="4fc4b-108">The **Define Shape Data** command on the shortcut menu in the **Shape Data** window is disabled.</span></span>  <br/> |
|<span data-ttu-id="4fc4b-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="4fc4b-109">FALSE</span></span>  <br/> |<span data-ttu-id="4fc4b-110">El comando **Definir datos de formas** en el menú contextual en la ventana **Datos de formas** está habilitado (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="4fc4b-110">The **Define Shape Data** command on the shortcut menu in the **Shape Data** window is enabled (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4fc4b-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4fc4b-111">Remarks</span></span>

<span data-ttu-id="4fc4b-112">El valor TRUE no impide al usuario cambiar el valor de un elemento de datos de formas ni cambiar la sección de datos de formas de la ventana ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="4fc4b-112">A value of TRUE does not prevent a user from changing the value of a shape data item or changing the Shape Data section in the ShapeSheet window.</span></span> 
  
<span data-ttu-id="4fc4b-113">Para obtener una referencia a la celda LockCustProp por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="4fc4b-113">To get a reference to the LockCustProp cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4fc4b-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="4fc4b-114">Cell name:</span></span>  <br/> |<span data-ttu-id="4fc4b-115">LockCustProp</span><span class="sxs-lookup"><span data-stu-id="4fc4b-115">LockCustProp</span></span>  <br/> |
   
<span data-ttu-id="4fc4b-116">Para obtener una referencia a la celda LockCustProp por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="4fc4b-116">To get a reference to the LockCustProp cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4fc4b-117">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="4fc4b-117">Section index:</span></span>  <br/> |<span data-ttu-id="4fc4b-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4fc4b-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="4fc4b-119">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="4fc4b-119">Row index:</span></span>  <br/> |<span data-ttu-id="4fc4b-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="4fc4b-120">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="4fc4b-121">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="4fc4b-121">Cell index:</span></span>  <br/> |<span data-ttu-id="4fc4b-122">**visLockCustProp**</span><span class="sxs-lookup"><span data-stu-id="4fc4b-122">**visLockCustProp**</span></span> <br/> |
   

