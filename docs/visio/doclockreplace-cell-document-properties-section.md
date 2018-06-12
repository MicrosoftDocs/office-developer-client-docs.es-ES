---
title: Celda DocLockReplace (sección Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74eae5e5-80ab-4e10-b292-e58a6d7607d2
description: Determina si la forma de reemplazar la interfaz de usuario debe deshabilitarse para este documento.
ms.openlocfilehash: 41552ddad4e48680960c45869ded5cf4f80d760f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822025"
---
# <a name="doclockreplace-cell-document-properties-section"></a><span data-ttu-id="388a4-103">Celda DocLockReplace (sección Document Properties)</span><span class="sxs-lookup"><span data-stu-id="388a4-103">DocLockReplace Cell (Document Properties Section)</span></span>

<span data-ttu-id="388a4-104">Determina si la forma de reemplazar la interfaz de usuario debe deshabilitarse para este documento.</span><span class="sxs-lookup"><span data-stu-id="388a4-104">Determines whether the replace shape UI should be disabled for this document.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="388a4-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="388a4-105">TRUE</span></span>  <br/> |<span data-ttu-id="388a4-106">El botón **Reemplazar forma** está atenuado en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="388a4-106">The **Replace Shape** button is grayed out in the UI.</span></span>  <br/> |
|<span data-ttu-id="388a4-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="388a4-107">FALSE</span></span>  <br/> |<span data-ttu-id="388a4-108">El botón **Reemplazar forma** está activo en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="388a4-108">The **Replace Shape** button is active in the UI.</span></span> <span data-ttu-id="388a4-109">Los usuarios pueden usar la característica de la forma de reemplazar en este documento.</span><span class="sxs-lookup"><span data-stu-id="388a4-109">Users can use the Replace Shape feature in this document.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="388a4-110">Notas</span><span class="sxs-lookup"><span data-stu-id="388a4-110">Remarks</span></span>

<span data-ttu-id="388a4-111">Para obtener una referencia a la celda **DocLockReplace** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="388a4-111">To get a reference to the **DocLockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="388a4-112">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="388a4-112">Cell name:</span></span>  <br/> | <span data-ttu-id="388a4-113">DocLocReplace</span><span class="sxs-lookup"><span data-stu-id="388a4-113">DocLocReplace</span></span>  <br/> |
   
<span data-ttu-id="388a4-114">Para obtener una referencia a la celda **DocLocReplace** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="388a4-114">To get a reference to the **DocLocReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="388a4-115">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="388a4-115">Section index:</span></span>  <br/> |<span data-ttu-id="388a4-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="388a4-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="388a4-117">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="388a4-117">Row index:</span></span>  <br/> |<span data-ttu-id="388a4-118">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="388a4-118">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="388a4-119">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="388a4-119">Cell index:</span></span>  <br/> |<span data-ttu-id="388a4-120">** visDocLockReplace **</span><span class="sxs-lookup"><span data-stu-id="388a4-120">**visDocLockReplace **</span></span> <br/> |
   

