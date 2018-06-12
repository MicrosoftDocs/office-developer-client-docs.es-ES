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
ms.openlocfilehash: 7f8800f0b260e808a46ec123d27784f3dd92e847
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822530"
---
# <a name="locktextedit-cell-protection-section"></a><span data-ttu-id="eb624-103">Celda LockTextEdit (Sección de protección)</span><span class="sxs-lookup"><span data-stu-id="eb624-103">LockTextEdit Cell (Protection Section)</span></span>

<span data-ttu-id="eb624-104">Bloquea el texto de una forma para que no se pueda editar.</span><span class="sxs-lookup"><span data-stu-id="eb624-104">Locks the text of a shape so that it cannot be edited.</span></span>
  
|<span data-ttu-id="eb624-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="eb624-105">**Value**</span></span>|<span data-ttu-id="eb624-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="eb624-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="eb624-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="eb624-107">TRUE</span></span>  <br/> |<span data-ttu-id="eb624-108">El texto no se puede editar.</span><span class="sxs-lookup"><span data-stu-id="eb624-108">Text cannot be edited.</span></span>  <br/> |
| <span data-ttu-id="eb624-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="eb624-109">FALSE</span></span>  <br/> | <span data-ttu-id="eb624-110">El texto se puede editar.</span><span class="sxs-lookup"><span data-stu-id="eb624-110">Text can be edited.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eb624-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eb624-111">Remarks</span></span>

<span data-ttu-id="eb624-112">Todavía se puede formatear texto, aplicando un estilo en el cuadro de diálogo **texto** (en la ficha **Inicio** , haga clic en la flecha de **fuente** ).</span><span class="sxs-lookup"><span data-stu-id="eb624-112">You can still format text by applying a style in the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="eb624-113">Para obtener una referencia a la celda LockTextEdit por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="eb624-113">To get a reference to the LockTextEdit cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="eb624-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="eb624-114">Cell name:</span></span>  <br/> | <span data-ttu-id="eb624-115">LockTextEdit</span><span class="sxs-lookup"><span data-stu-id="eb624-115">LockTextEdit</span></span>  <br/> |
   
<span data-ttu-id="eb624-116">Para obtener una referencia a la celda LockTextEdit por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="eb624-116">To get a reference to the LockTextEdit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="eb624-117">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="eb624-117">Section index:</span></span>  <br/> |<span data-ttu-id="eb624-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="eb624-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="eb624-119">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="eb624-119">Row index:</span></span>  <br/> |<span data-ttu-id="eb624-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="eb624-120">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="eb624-121">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="eb624-121">Cell index:</span></span>  <br/> |<span data-ttu-id="eb624-122">**visLockTextEdit**</span><span class="sxs-lookup"><span data-stu-id="eb624-122">**visLockTextEdit**</span></span> <br/> |
   

