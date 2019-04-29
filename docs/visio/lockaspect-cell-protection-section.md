---
title: Celda LockAspect (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251218
localization_priority: Normal
ms.assetid: e9bfced5-af29-f86c-8604-44ec9a573229
description: Bloquea la relación de aspecto de la forma de manera que solo se puede ajustar el tamaño de manera proporcional; no se puede ajustar el tamaño en una única dimensión.
ms.openlocfilehash: 83ce1aaf555cfaaa0109423e74ae930450b4c1e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411585"
---
# <a name="lockaspect-cell-protection-section"></a><span data-ttu-id="1ae74-103">Celda LockAspect (Sección de protección)</span><span class="sxs-lookup"><span data-stu-id="1ae74-103">LockAspect Cell (Protection Section)</span></span>

<span data-ttu-id="1ae74-104">Bloquea la relación de aspecto de la forma de manera que solo se puede ajustar el tamaño de manera proporcional; no se puede ajustar el tamaño en una única dimensión.</span><span class="sxs-lookup"><span data-stu-id="1ae74-104">Locks the aspect ratio of the shape so that the shape can only be sized proportionally; it cannot be sized in a single dimension.</span></span>
  
|<span data-ttu-id="1ae74-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="1ae74-105">**Value**</span></span>|<span data-ttu-id="1ae74-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1ae74-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="1ae74-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="1ae74-107">TRUE</span></span>  <br/> | <span data-ttu-id="1ae74-108">La relación de aspecto se encuentra bloqueada.</span><span class="sxs-lookup"><span data-stu-id="1ae74-108">Aspect ratio is locked.</span></span>  <br/> |
| <span data-ttu-id="1ae74-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="1ae74-109">FALSE</span></span>  <br/> | <span data-ttu-id="1ae74-110">La relación de aspecto no se encuentra bloqueada.</span><span class="sxs-lookup"><span data-stu-id="1ae74-110">Aspect ratio is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1ae74-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1ae74-111">Remarks</span></span>

<span data-ttu-id="1ae74-112">Para obtener una referencia a la celda LockAspect por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**,utilice:</span><span class="sxs-lookup"><span data-stu-id="1ae74-112">To get a reference to the LockAspect cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1ae74-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="1ae74-113">Cell name:</span></span>  <br/> | <span data-ttu-id="1ae74-114">LockAspect</span><span class="sxs-lookup"><span data-stu-id="1ae74-114">LockAspect</span></span>  <br/> |
   
<span data-ttu-id="1ae74-115">Para obtener una referencia desde un programa a la celda LockAspect por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="1ae74-115">To get a reference to the LockAspect cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1ae74-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="1ae74-116">Section index:</span></span>  <br/> |<span data-ttu-id="1ae74-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1ae74-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1ae74-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="1ae74-118">Row index:</span></span>  <br/> |<span data-ttu-id="1ae74-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="1ae74-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="1ae74-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="1ae74-120">Cell index:</span></span>  <br/> |<span data-ttu-id="1ae74-121">**visLockAspect**</span><span class="sxs-lookup"><span data-stu-id="1ae74-121">**visLockAspect**</span></span> <br/> |
   

