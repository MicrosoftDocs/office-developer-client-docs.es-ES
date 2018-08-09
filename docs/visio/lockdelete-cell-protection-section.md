---
title: Celda LockDelete (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251219
localization_priority: Normal
ms.assetid: 596c62b7-8d42-1854-d709-592db09a6a84
description: Bloquea la forma de manera que ésta no pueda ser eliminada.
ms.openlocfilehash: 00229dcabf45d2a3435039ffe05fd7eb4de75808
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822505"
---
# <a name="lockdelete-cell-protection-section"></a><span data-ttu-id="f9a32-103">Celda LockDelete (sección Protección)</span><span class="sxs-lookup"><span data-stu-id="f9a32-103">LockDelete Cell (Protection Section)</span></span>

<span data-ttu-id="f9a32-104">Bloquea la forma de manera que ésta no pueda ser eliminada.</span><span class="sxs-lookup"><span data-stu-id="f9a32-104">Locks the shape so that it cannot be deleted.</span></span>
  
|<span data-ttu-id="f9a32-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="f9a32-105">**Value**</span></span>|<span data-ttu-id="f9a32-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f9a32-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="f9a32-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="f9a32-107">TRUE</span></span>  <br/> | <span data-ttu-id="f9a32-108">La forma no se puede eliminar</span><span class="sxs-lookup"><span data-stu-id="f9a32-108">Shape cannot be deleted</span></span>  <br/> |
| <span data-ttu-id="f9a32-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="f9a32-109">FALSE</span></span>  <br/> | <span data-ttu-id="f9a32-110">La forma puede ser eliminada.</span><span class="sxs-lookup"><span data-stu-id="f9a32-110">Shape can be deleted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f9a32-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f9a32-111">Remarks</span></span>

<span data-ttu-id="f9a32-112">Para obtener una referencia a la celda LockDelete por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** utilice:</span><span class="sxs-lookup"><span data-stu-id="f9a32-112">To get a reference to the LockDelete cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f9a32-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="f9a32-113">Cell name:</span></span>  <br/> | <span data-ttu-id="f9a32-114">LockDelete</span><span class="sxs-lookup"><span data-stu-id="f9a32-114">LockDelete</span></span>  <br/> |
   
<span data-ttu-id="f9a32-115">Para obtener una referencia desde un programa a la celda LockDelete por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="f9a32-115">To get a reference to the LockDelete cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f9a32-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="f9a32-116">Section index:</span></span>  <br/> |<span data-ttu-id="f9a32-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f9a32-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f9a32-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="f9a32-118">Row index:</span></span>  <br/> |<span data-ttu-id="f9a32-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="f9a32-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="f9a32-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="f9a32-120">Cell index:</span></span>  <br/> |<span data-ttu-id="f9a32-121">**visLockDelete**</span><span class="sxs-lookup"><span data-stu-id="f9a32-121">**visLockDelete**</span></span> <br/> |
   

