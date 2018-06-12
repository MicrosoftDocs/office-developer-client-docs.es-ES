---
title: SETF (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251496
localization_priority: Normal
ms.assetid: fcf415c1-171f-b75f-6e40-2bbdbe8b1cfb
description: Establece la fórmula de una celda.
ms.openlocfilehash: a1e6a12014a77a20c0968b3ed2f7bc25badad8ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823127"
---
# <a name="setf-function"></a><span data-ttu-id="6e650-103">SETF (función)</span><span class="sxs-lookup"><span data-stu-id="6e650-103">SETF Function</span></span>

<span data-ttu-id="6e650-104">Establece la fórmula de una celda.</span><span class="sxs-lookup"><span data-stu-id="6e650-104">Sets a cell's formula.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6e650-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e650-105">Syntax</span></span>

<span data-ttu-id="6e650-106">SETF (GETREF (** *celda* **), ** *fórmula* **)</span><span class="sxs-lookup"><span data-stu-id="6e650-106">SETF( GETREF(** *cell* ** ), ** *formula* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6e650-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e650-107">Parameters</span></span>

|<span data-ttu-id="6e650-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="6e650-108">**Name**</span></span>|<span data-ttu-id="6e650-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="6e650-109">**Required/Optional**</span></span>|<span data-ttu-id="6e650-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="6e650-110">**Data Type**</span></span>|<span data-ttu-id="6e650-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6e650-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6e650-112">_celda_</span><span class="sxs-lookup"><span data-stu-id="6e650-112">_cell_</span></span> <br/> |<span data-ttu-id="6e650-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="6e650-113">Required</span></span>  <br/> |<span data-ttu-id="6e650-114">**String**</span><span class="sxs-lookup"><span data-stu-id="6e650-114">**String**</span></span> <br/> |<span data-ttu-id="6e650-115">La celda cuya fórmula desea establecer.</span><span class="sxs-lookup"><span data-stu-id="6e650-115">The cell whose formula to set.</span></span>  <br/> |
| <span data-ttu-id="6e650-116">_formula_</span><span class="sxs-lookup"><span data-stu-id="6e650-116">_formula_</span></span> <br/> |<span data-ttu-id="6e650-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="6e650-117">Required</span></span>  <br/> |<span data-ttu-id="6e650-118">**String**</span><span class="sxs-lookup"><span data-stu-id="6e650-118">**String**</span></span> <br/> |<span data-ttu-id="6e650-119">La fórmula que desea usar.</span><span class="sxs-lookup"><span data-stu-id="6e650-119">The formula to use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6e650-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6e650-120">Remarks</span></span>

<span data-ttu-id="6e650-121">Cuando se evalúa, el resultado de la expresión en la _fórmula_ se convierte en la nueva fórmula de _celda_.</span><span class="sxs-lookup"><span data-stu-id="6e650-121">When evaluated, the result of the expression in  _formula_ becomes the new formula in  _cell_.</span></span> <span data-ttu-id="6e650-122">Si la _fórmula_ está entre comillas, la expresión entrecomillada se escribe en la _celda_.</span><span class="sxs-lookup"><span data-stu-id="6e650-122">If  _formula_ is enclosed in quotation marks, the quoted expression is written to  _cell_.</span></span> <span data-ttu-id="6e650-123">Para establecer la _celda_ en una cadena, escriba la _fórmula_ en tres conjuntos de comillas dobles.</span><span class="sxs-lookup"><span data-stu-id="6e650-123">To set  _cell_ to a string, enclose  _formula_ in three sets of quotation marks.</span></span> 
  
<span data-ttu-id="6e650-p102">La celda de destino debe especificarse usando una referencia GETREF() o mediante una cadena para evitar las referencias circulares. Se aconseja utilizar GETREF ya que Microsoft Visio puede ajustar las referencias en el caso de que la forma se transfiera a otro documento distinto.</span><span class="sxs-lookup"><span data-stu-id="6e650-p102">The target cell must be specified using a GETREF() reference or as a string to avoid circularity. Using GETREF is preferred, because Microsoft Visio can adjust references when the shape is moved to a different document.</span></span>
  
<span data-ttu-id="6e650-126">Si no se especifica _celda_ mediante GETREF o como una cadena, la función devuelve un error y se cambia la fórmula de la celda no.</span><span class="sxs-lookup"><span data-stu-id="6e650-126">If  _cell_ is not specified using GETREF or as a string, the function returns an error, and no cell's formula is changed.</span></span> <span data-ttu-id="6e650-127">Si la _fórmula_ contiene un error de sintaxis, la función devuelve un error y no se cambia la fórmula de la _celda_ .</span><span class="sxs-lookup"><span data-stu-id="6e650-127">If  _formula_ contains a syntax error, the function returns an error, and the formula in  _cell_ is not changed.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="6e650-128">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="6e650-128">Example 1</span></span>

<span data-ttu-id="6e650-129">SETF (GETREF(Scratch.A1), 1,5 pda \* 6 + 1 ft)</span><span class="sxs-lookup"><span data-stu-id="6e650-129">SETF( GETREF(Scratch.A1), 1.5 in \* 6 + 1 ft)</span></span>
  
<span data-ttu-id="6e650-130">Establece la fórmula de Scratch.A1 y le da el valor 21 pulgadas.</span><span class="sxs-lookup"><span data-stu-id="6e650-130">Sets the formula of Scratch.A1 to 21 inches.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="6e650-131">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="6e650-131">Example 2</span></span>

<span data-ttu-id="6e650-132">SETF (GETREF(Scratch.A1), "1,5 pda \* 6 + 1 ft")</span><span class="sxs-lookup"><span data-stu-id="6e650-132">SETF( GETREF(Scratch.A1), "1.5 in \* 6 + 1 ft")</span></span>
  
<span data-ttu-id="6e650-133">Establece la fórmula de cero.</span><span class="sxs-lookup"><span data-stu-id="6e650-133">Sets the formula of Scratch.</span></span> <span data-ttu-id="6e650-134">A1 a la expresión 1,5 en\*6 + 1 ft.</span><span class="sxs-lookup"><span data-stu-id="6e650-134">A1 to the expression 1.5 in\*6+1 ft.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="6e650-135">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="6e650-135">Example 3</span></span>

<span data-ttu-id="6e650-136">SETF( GETREF(Scratch.A1); """Diga """"aaah""""""")</span><span class="sxs-lookup"><span data-stu-id="6e650-136">SETF( GETREF(Scratch.A1), """Say """"ahh""""""")</span></span>
  
<span data-ttu-id="6e650-137">Establece la fórmula de Scratch.A1 como el valor de la cadena "Diga ""aaah""", que se convierte en Diga "aaah".</span><span class="sxs-lookup"><span data-stu-id="6e650-137">Sets the formula of Scratch.A1 to the string "Say ""ahh""" which evaluates to Say "ahh".</span></span>
  

