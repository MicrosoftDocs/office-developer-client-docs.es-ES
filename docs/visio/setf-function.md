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
ms.openlocfilehash: 63050de92394ebbdce6cfe053e15347ca3ce5c7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325840"
---
# <a name="setf-function"></a><span data-ttu-id="db9c3-103">Función SETF</span><span class="sxs-lookup"><span data-stu-id="db9c3-103">SETF Function</span></span>

<span data-ttu-id="db9c3-104">Establece la fórmula de una celda.</span><span class="sxs-lookup"><span data-stu-id="db9c3-104">Sets a cell's formula.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="db9c3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="db9c3-105">Syntax</span></span>

<span data-ttu-id="db9c3-106">SETF (GETREF (\* \* *celda* \* \*), \* \* *fórmula* \* \*)</span><span class="sxs-lookup"><span data-stu-id="db9c3-106">SETF( GETREF(\*\* *cell* \*\* ), \*\* *formula* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="db9c3-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="db9c3-107">Parameters</span></span>

|<span data-ttu-id="db9c3-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="db9c3-108">**Name**</span></span>|<span data-ttu-id="db9c3-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="db9c3-109">**Required/Optional**</span></span>|<span data-ttu-id="db9c3-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="db9c3-110">**Data Type**</span></span>|<span data-ttu-id="db9c3-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="db9c3-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="db9c3-112">_móviles_</span><span class="sxs-lookup"><span data-stu-id="db9c3-112">_cell_</span></span> <br/> |<span data-ttu-id="db9c3-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="db9c3-113">Required</span></span>  <br/> |<span data-ttu-id="db9c3-114">**String**</span><span class="sxs-lookup"><span data-stu-id="db9c3-114">**String**</span></span> <br/> |<span data-ttu-id="db9c3-115">La celda cuya fórmula desea establecer.</span><span class="sxs-lookup"><span data-stu-id="db9c3-115">The cell whose formula to set.</span></span>  <br/> |
| <span data-ttu-id="db9c3-116">_formula_</span><span class="sxs-lookup"><span data-stu-id="db9c3-116">_formula_</span></span> <br/> |<span data-ttu-id="db9c3-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="db9c3-117">Required</span></span>  <br/> |<span data-ttu-id="db9c3-118">**String**</span><span class="sxs-lookup"><span data-stu-id="db9c3-118">**String**</span></span> <br/> |<span data-ttu-id="db9c3-119">La fórmula que desea usar.</span><span class="sxs-lookup"><span data-stu-id="db9c3-119">The formula to use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db9c3-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="db9c3-120">Remarks</span></span>

<span data-ttu-id="db9c3-121">Cuando se evalúa, el resultado de la expresión de la _fórmula_ se convierte en la nueva fórmula en la _celda_.</span><span class="sxs-lookup"><span data-stu-id="db9c3-121">When evaluated, the result of the expression in  _formula_ becomes the new formula in  _cell_.</span></span> <span data-ttu-id="db9c3-122">Si la _fórmula_ se encuentra entre comillas, la expresión entrecomillada se escribe en la _celda_.</span><span class="sxs-lookup"><span data-stu-id="db9c3-122">If  _formula_ is enclosed in quotation marks, the quoted expression is written to  _cell_.</span></span> <span data-ttu-id="db9c3-123">Para establecer la _celda_ en una cadena, escriba una _fórmula_ en tres conjuntos de Comillas.</span><span class="sxs-lookup"><span data-stu-id="db9c3-123">To set  _cell_ to a string, enclose  _formula_ in three sets of quotation marks.</span></span> 
  
<span data-ttu-id="db9c3-p102">La celda de destino debe especificarse usando una referencia GETREF() o mediante una cadena para evitar las referencias circulares. Se aconseja utilizar GETREF ya que Microsoft Visio puede ajustar las referencias en el caso de que la forma se transfiera a otro documento distinto.</span><span class="sxs-lookup"><span data-stu-id="db9c3-p102">The target cell must be specified using a GETREF() reference or as a string to avoid circularity. Using GETREF is preferred, because Microsoft Visio can adjust references when the shape is moved to a different document.</span></span>
  
<span data-ttu-id="db9c3-126">Si no se especifica la _celda_ mediante GETREF o como una cadena, la función devuelve un error y no se cambia la fórmula de la celda.</span><span class="sxs-lookup"><span data-stu-id="db9c3-126">If  _cell_ is not specified using GETREF or as a string, the function returns an error, and no cell's formula is changed.</span></span> <span data-ttu-id="db9c3-127">Si la _fórmula_ contiene un error de sintaxis, la función devolverá un error y no se cambiará la fórmula de la _celda_ .</span><span class="sxs-lookup"><span data-stu-id="db9c3-127">If  _formula_ contains a syntax error, the function returns an error, and the formula in  _cell_ is not changed.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="db9c3-128">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="db9c3-128">Example 1</span></span>

<span data-ttu-id="db9c3-129">SETF (GETREF (Scratch. a1), 1,5 en \* 6 + 1 ft)</span><span class="sxs-lookup"><span data-stu-id="db9c3-129">SETF( GETREF(Scratch.A1), 1.5 in \* 6 + 1 ft)</span></span>
  
<span data-ttu-id="db9c3-130">Establece la fórmula de Scratch.A1 y le da el valor 21 pulgadas.</span><span class="sxs-lookup"><span data-stu-id="db9c3-130">Sets the formula of Scratch.A1 to 21 inches.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="db9c3-131">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="db9c3-131">Example 2</span></span>

<span data-ttu-id="db9c3-132">SETF (GETREF (Scratch. a1), "1,5 en \* 6 + 1 ft")</span><span class="sxs-lookup"><span data-stu-id="db9c3-132">SETF( GETREF(Scratch.A1), "1.5 in \* 6 + 1 ft")</span></span>
  
<span data-ttu-id="db9c3-133">Establece la fórmula de la grieta.</span><span class="sxs-lookup"><span data-stu-id="db9c3-133">Sets the formula of Scratch.</span></span> <span data-ttu-id="db9c3-134">A1 a la expresión 1,5 en\*6 + 1 ft.</span><span class="sxs-lookup"><span data-stu-id="db9c3-134">A1 to the expression 1.5 in\*6+1 ft.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="db9c3-135">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="db9c3-135">Example 3</span></span>

<span data-ttu-id="db9c3-136">SETF( GETREF(Scratch.A1); """Diga """"aaah""""""")</span><span class="sxs-lookup"><span data-stu-id="db9c3-136">SETF( GETREF(Scratch.A1), """Say """"ahh""""""")</span></span>
  
<span data-ttu-id="db9c3-137">Establece la fórmula de Scratch.A1 como el valor de la cadena "Diga ""aaah""", que se convierte en Diga "aaah".</span><span class="sxs-lookup"><span data-stu-id="db9c3-137">Sets the formula of Scratch.A1 to the string "Say ""ahh""" which evaluates to Say "ahh".</span></span>
  

