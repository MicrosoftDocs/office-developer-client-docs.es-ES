---
title: Celda DocLockReplace (sección de propiedades del documento)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74eae5e5-80ab-4e10-b292-e58a6d7607d2
description: Determina si la interfaz de usuario reemplazar forma debe estar deshabilitada para este documento.
ms.openlocfilehash: cfec9b3c51a170c549fdd0d1b0b3597c030c410c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338608"
---
# <a name="doclockreplace-cell-document-properties-section"></a><span data-ttu-id="3e63f-103">Celda DocLockReplace (sección de propiedades del documento)</span><span class="sxs-lookup"><span data-stu-id="3e63f-103">DocLockReplace Cell (Document Properties Section)</span></span>

<span data-ttu-id="3e63f-104">Determina si la interfaz de usuario reemplazar forma debe estar deshabilitada para este documento.</span><span class="sxs-lookup"><span data-stu-id="3e63f-104">Determines whether the replace shape UI should be disabled for this document.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3e63f-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="3e63f-105">TRUE</span></span>  <br/> |<span data-ttu-id="3e63f-106">El botón **reemplazar forma** está atenuado en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="3e63f-106">The **Replace Shape** button is grayed out in the UI.</span></span>  <br/> |
|<span data-ttu-id="3e63f-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="3e63f-107">FALSE</span></span>  <br/> |<span data-ttu-id="3e63f-108">El botón **reemplazar forma** está activo en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="3e63f-108">The **Replace Shape** button is active in the UI.</span></span> <span data-ttu-id="3e63f-109">Los usuarios pueden usar la característica reemplazar forma de este documento.</span><span class="sxs-lookup"><span data-stu-id="3e63f-109">Users can use the Replace Shape feature in this document.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3e63f-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3e63f-110">Remarks</span></span>

<span data-ttu-id="3e63f-111">Para obtener una referencia a la celda **DocLockReplace** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="3e63f-111">To get a reference to the **DocLockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3e63f-112">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="3e63f-112">Cell name:</span></span>  <br/> | <span data-ttu-id="3e63f-113">DocLocReplace</span><span class="sxs-lookup"><span data-stu-id="3e63f-113">DocLocReplace</span></span>  <br/> |
   
<span data-ttu-id="3e63f-114">Para obtener una referencia desde un programa a la celda **DocLocReplace** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="3e63f-114">To get a reference to the **DocLocReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3e63f-115">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="3e63f-115">Section index:</span></span>  <br/> |<span data-ttu-id="3e63f-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3e63f-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3e63f-117">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="3e63f-117">Row index:</span></span>  <br/> |<span data-ttu-id="3e63f-118">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="3e63f-118">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="3e63f-119">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="3e63f-119">Cell index:</span></span>  <br/> |<span data-ttu-id="3e63f-120">\* \* visDocLockReplace \* \*</span><span class="sxs-lookup"><span data-stu-id="3e63f-120">\*\*visDocLockReplace \*\*</span></span> <br/> |
   

