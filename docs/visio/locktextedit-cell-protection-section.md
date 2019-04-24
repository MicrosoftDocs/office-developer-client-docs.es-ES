---
title: Celda LockTextEdit (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm665
localization_priority: Normal
ms.assetid: d8de5fa4-826b-e869-4d9f-997361d05fd8
description: Bloquea el texto de una forma para que no se pueda editar.
ms.openlocfilehash: f6e5176e3ab654b76c0641b8f642abcf6b1050dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348317"
---
# <a name="locktextedit-cell-protection-section"></a><span data-ttu-id="60875-103">Celda LockTextEdit (Sección de protección)</span><span class="sxs-lookup"><span data-stu-id="60875-103">LockTextEdit Cell (Protection Section)</span></span>

<span data-ttu-id="60875-104">Bloquea el texto de una forma para que no se pueda editar.</span><span class="sxs-lookup"><span data-stu-id="60875-104">Locks the text of a shape so that it cannot be edited.</span></span>
  
|<span data-ttu-id="60875-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="60875-105">**Value**</span></span>|<span data-ttu-id="60875-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="60875-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="60875-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="60875-107">TRUE</span></span>  <br/> |<span data-ttu-id="60875-108">El texto no se puede editar.</span><span class="sxs-lookup"><span data-stu-id="60875-108">Text cannot be edited.</span></span>  <br/> |
| <span data-ttu-id="60875-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="60875-109">FALSE</span></span>  <br/> | <span data-ttu-id="60875-110">El texto se puede editar.</span><span class="sxs-lookup"><span data-stu-id="60875-110">Text can be edited.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="60875-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="60875-111">Remarks</span></span>

<span data-ttu-id="60875-112">No obstante, puede dar formato al texto al aplicarle un estilo mediante el cuadro de diálogo **Texto** (en la ficha **Inicio**, haga clic en la flecha de **Fuente**).</span><span class="sxs-lookup"><span data-stu-id="60875-112">You can still format text by applying a style in the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="60875-113">Para obtener una referencia a la celda LockTextEdit por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="60875-113">To get a reference to the LockTextEdit cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="60875-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="60875-114">Cell name:</span></span>  <br/> | <span data-ttu-id="60875-115">LockTextEdit</span><span class="sxs-lookup"><span data-stu-id="60875-115">LockTextEdit</span></span>  <br/> |
   
<span data-ttu-id="60875-116">Para obtener una referencia desde un programa a la celda LockTextEdit por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="60875-116">To get a reference to the LockTextEdit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="60875-117">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="60875-117">Section index:</span></span>  <br/> |<span data-ttu-id="60875-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="60875-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="60875-119">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="60875-119">Row index:</span></span>  <br/> |<span data-ttu-id="60875-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="60875-120">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="60875-121">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="60875-121">Cell index:</span></span>  <br/> |<span data-ttu-id="60875-122">**visLockTextEdit**</span><span class="sxs-lookup"><span data-stu-id="60875-122">**visLockTextEdit**</span></span> <br/> |
   

