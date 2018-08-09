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
# <a name="locktextedit-cell-protection-section"></a><span data-ttu-id="50d4b-103">Celda LockTextEdit (sección Protección)</span><span class="sxs-lookup"><span data-stu-id="50d4b-103">LockTextEdit Cell (Protection Section)</span></span>

<span data-ttu-id="50d4b-104">Bloquea el texto de una forma para que no se pueda editar.</span><span class="sxs-lookup"><span data-stu-id="50d4b-104">Locks the text of a shape so that it cannot be edited.</span></span>
  
|<span data-ttu-id="50d4b-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="50d4b-105">**Value**</span></span>|<span data-ttu-id="50d4b-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="50d4b-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="50d4b-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="50d4b-107">TRUE</span></span>  <br/> |<span data-ttu-id="50d4b-108">El texto no se puede editar.</span><span class="sxs-lookup"><span data-stu-id="50d4b-108">Text cannot be edited.</span></span>  <br/> |
| <span data-ttu-id="50d4b-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="50d4b-109">FALSE</span></span>  <br/> | <span data-ttu-id="50d4b-110">El texto se puede editar.</span><span class="sxs-lookup"><span data-stu-id="50d4b-110">Text can be edited.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50d4b-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="50d4b-111">Remarks</span></span>

<span data-ttu-id="50d4b-112">No obstante, puede dar formato al texto al aplicarle un estilo mediante el cuadro de diálogo **Texto** (en la ficha **Inicio**, haga clic en la flecha de **Fuente**).</span><span class="sxs-lookup"><span data-stu-id="50d4b-112">You can still format text by applying a style in the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="50d4b-113">Para obtener una referencia a la celda LockTextEdit por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="50d4b-113">To get a reference to the LockTextEdit cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="50d4b-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="50d4b-114">Cell name:</span></span>  <br/> | <span data-ttu-id="50d4b-115">LockTextEdit</span><span class="sxs-lookup"><span data-stu-id="50d4b-115">LockTextEdit</span></span>  <br/> |
   
<span data-ttu-id="50d4b-116">Para obtener una referencia desde un programa a la celda LockTextEdit por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="50d4b-116">To get a reference to the LockTextEdit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="50d4b-117">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="50d4b-117">Section index:</span></span>  <br/> |<span data-ttu-id="50d4b-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="50d4b-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="50d4b-119">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="50d4b-119">Row index:</span></span>  <br/> |<span data-ttu-id="50d4b-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="50d4b-120">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="50d4b-121">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="50d4b-121">Cell index:</span></span>  <br/> |<span data-ttu-id="50d4b-122">**visLockTextEdit**</span><span class="sxs-lookup"><span data-stu-id="50d4b-122">**visLockTextEdit**</span></span> <br/> |
   

